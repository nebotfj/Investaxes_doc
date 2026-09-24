---
description: Síntoma, causa, impacto fiscal y solución de cada error habitual.
icon: triangle-exclamation
---

# Catálogo de errores: diagnóstico y corrección

## 12.1 Errores de importación

### La subida del archivo da error

Ya está desarrollado en **6.5**, pero conviene repetir el diagnóstico porque es el error más frecuente:

| | Concepto nuevo detectado | Archivo incorrecto |
|---|---|---|
| **Qué pasa** | El sistema no tiene integrado todavía ese tipo de operación | El archivo no corresponde al exchange, tiene formato distinto o está incompleto |
| **Qué haces** | **Nada.** Esperar | **Revisar** y volver a subir |
| **Se resuelve solo** | Sí, se incorpora automáticamente | **No** |
| **Si lo ignoras** | Se integra igualmente | **Ese exchange se queda fuera del cálculo** |

**La causa más común del segundo caso:** subir el CSV de un exchange bajo otro exchange distinto.

### Missing transactions

**Síntoma.** Los saldos no cuadran con lo que tienes realmente.

**Causa.** El exchange no exportó correctamente, la exportación cubrió solo parte del periodo, o hay discrepancia entre la blockchain y el histórico exportado.

**Impacto fiscal.** Alto. Cada movimiento ausente rompe el encadenado FIFO.

**Cómo corregirlo:**
1. Identifica en qué activo y fecha se produce el descuadre
2. Contrasta con un explorador de blockchain o con el histórico original
3. Localiza qué movimientos faltan
4. Impórtalos; si el exchange no los exporta, usa la plantilla genérica
5. Vuelve a comprobar el saldo

### Transacciones duplicadas

**Síntoma.** La misma operación aparece dos o más veces.

**Causa.** El mismo archivo importado más de una vez, o periodos solapados.

**Impacto fiscal.** Alto. Infla tu inventario: el sistema cree que tienes más unidades de las que tienes.

**Cómo corregirlo:**
1. Filtra en **Transactions** por fecha y activo
2. **Verifica el hash de transacción**: es único, así que dos registros con el mismo hash son el mismo movimiento
3. Elimina las copias sobrantes
4. Comprueba que el saldo vuelve a cuadrar

### Depósitos negativos

**Síntoma.** Depósitos con importe negativo.

**Causa.** Error de formato en la exportación, habitual en productos de tipo *Earn*.

**Cómo corregirlo:** localiza los movimientos afectados y corrige el signo.

### Sincronización fallida o incompleta

**Síntoma.** La cuenta deja de actualizarse o faltan movimientos recientes.

**Impacto fiscal.** Alto si pasa desapercibido: la cuenta parece cargada pero tiene un corte.

**Cómo corregirlo:** revisa el estado en **Accounts** y completa el periodo con una exportación de archivos.

---

## 12.2 Errores de trazabilidad

### Ventas vacías

**Síntoma.** El informe avisa de una venta o salida de cripto **de la que no existen compras anteriores**.

**Causas, tal como las describe el propio informe:**
- Falta por subir información de otros exchanges, billeteras o blockchains
- Aparecen ventas de criptoactivos que no tienen una compra anterior

**Impacto fiscal.** **El más alto de todos.** Sin coste de adquisición localizado, prácticamente toda la venta se convierte en ganancia, y el error se propaga a todas las operaciones posteriores de ese activo.

**Qué debo hacer — revisar la trazabilidad y buscar transacciones perdidas:**

| Qué buscar | Qué suele ser en realidad |
|---|---|
| **Retiros que no tienen un depósito posterior** | La cuenta de destino no está importada |
| **Depósitos que no tienen un retiro anterior** | La cuenta de origen no está importada |
| **Retiros que son realmente otro tipo de movimiento** | Un pago (`EXPENSE`), una aportación a un pool, o un bridge entre tokens: retiras BTC y te depositan WBTC, **que tiene que ir como `SWAP`** |
| **Depósitos que son otro tipo de movimiento** | Un ingreso, un interés, un airdrop… |

**Cómo corregirlo:**
1. Identifica qué activo y qué cantidad no tienen origen
2. Pregúntate de dónde salió ese activo
3. Vuelve al inventario del capítulo 5: casi siempre la respuesta es una fuente sin importar
4. Revisa si el movimiento está mal tipificado según la tabla anterior
5. Regenera el informe y comprueba si la alerta ha desaparecido

### Transferencias sin emparejar

**Síntoma.** Salidas hacia cuentas propias sin entrada correspondiente, o al revés.

**Impacto fiscal.** Alto. Una sola transferencia grande sin emparejar puede inflar la ganancia de forma notable.

**Cómo corregirlo:** aplica la revisión de 11.3, identifica la cuenta del otro extremo e impórtala.

### Direcciones de blockchain no identificadas

**Síntoma.** Aparece una dirección truncada sin vincular, del tipo `0x8...605 @ POLYGON`.

**Cómo corregirlo:**
1. Búscala en el explorador de esa red
2. Determina si es tuya, de un exchange o de un contrato de protocolo
3. Si es tuya: impórtala. Probablemente resuelva varias ventas vacías de golpe

### Desincronización entre on-chain y off-chain

**Síntoma.** Transacciones visibles en la blockchain que no aparecen en el histórico del exchange.

**Cómo corregirlo:** reconcilia ambas fuentes e importa manualmente lo que falte.

---

## 12.3 Errores de clasificación

### Operaciones mal clasificadas

**Síntoma.** Transacciones que no encajan en su categoría: una permuta que aparece como depósito, un ingreso de staking registrado como `INCOME` genérico.

**Impacto fiscal.** Alto y **silencioso**: los saldos siguen cuadrando, así que la capa 1 no lo detecta.

**Cómo corregirlo:** ve a **Transactions**, filtra por tipo y revisa por bloques, empezando por los de más impacto fiscal (11.5).

### Confusión TRADE / SWAP

**Impacto fiscal.** **El más caro de los errores de clasificación.** Clasificar un `TRADE` como `SWAP` elimina una ganancia que sí tributa.

**Cómo corregirlo:** aplica la pregunta de 8.3 a cada permuta: *¿he cambiado de exposición económica?*

### Pools de liquidez desagrupadas

**Síntoma.** Múltiples transacciones sueltas de liquidez sin estructura reconocible.

**Cómo corregirlo:**
1. Identifica todos los movimientos de un mismo pool
2. Comprueba que el LP token tiene como coste el colateral aportado más el gas
3. Comprueba que la quema final está como `EXPENSE_NOT_TAXABLE`
4. Usa `Tags` para revisarlos como bloque

---

## 12.4 Errores de valoración

### Precios unitarios faltantes o a cero

**Síntoma.** `Unit Cost` a 0, o valores anómalos.

**Impacto fiscal.** **Muy alto.** Un coste de adquisición a cero convierte el importe íntegro de la venta en ganancia.

**Cómo corregirlo:**
1. Filtra las transacciones con `Unit Cost` a cero
2. Busca el precio histórico del activo en esa fecha exacta
3. Introdúcelo manualmente
4. Si no hay precio localizable, documenta el criterio de valoración aplicado

### Conversión de divisas incorrecta

**Síntoma.** Valoraciones en euros que no coinciden con el precio real de la fecha.

**Impacto fiscal.** Medio pero sistemático: afecta a todas las operaciones de esa fuente.

**Cómo corregirlo:** verifica el tipo de cambio histórico y ajusta.

---

## 12.5 Errores técnicos

### El informe no se genera

**Cómo corregirlo:** espera entre cinco y diez minutos, limpia la caché y reintenta. Si persiste, contacta con soporte.

### El informe se genera vacío

**Causa.** El período seleccionado no contiene transacciones.

**Cómo corregirlo:** verifica que existan transacciones en ese ejercicio y revisa los filtros.

---

## 12.6 Tabla de referencia rápida

| Síntoma | Error probable | Apartado |
|---|---|---|
| Alerta al subir un archivo | Concepto nuevo (esperar) o archivo incorrecto (revisar) | 6.5 / 12.1 |
| El saldo no cuadra con la realidad | Missing transactions o duplicados | 12.1 |
| La misma operación aparece dos veces | Duplicados | 12.1 |
| Depósitos con importe negativo | Error de formato de exportación | 12.1 |
| Falta actividad reciente de una cuenta | Sincronización fallida | 12.1 |
| Venta sin compra previa | Venta vacía | 12.2 |
| Salida sin entrada correspondiente | Transferencia sin emparejar | 12.2 |
| Retiras BTC y te llega WBTC | Bridge mal clasificado: es `SWAP` | 12.2 |
| Dirección `0x...` sin identificar | Cuenta no vinculada | 12.2 |
| Ganancia mucho mayor de la esperada | Coste cero o transferencia sin emparejar | 12.2 / 12.4 |
| Una permuta no aparece como ganancia | `TRADE` clasificado como `SWAP` | 12.3 |
| Movimientos de pool dispersos | Pool desagrupada | 12.3 |
| Staking tributando en base general | Clasificado como `INCOME` en vez de `STAKING` | 12.3 |
| `Unit Cost` a 0 | Precio histórico no obtenido | 12.4 |
| Valoraciones en EUR extrañas | Conversión de divisa incorrecta | 12.4 |

