---
description: Qué responde cada sección del menú y qué revisar en cada una.
icon: compass
---

# Navegación de la plataforma

El menú lateral izquierdo organiza la plataforma en seis secciones. Cada una responde a una pregunta distinta, y conviene saber cuál para no perder tiempo buscando en el sitio equivocado.

| Sección | La pregunta que responde |
|---|---|
| **Dashboard** | ¿Cómo está mi cuenta ahora mismo? |
| **Portfolio** | ¿Qué tengo y cómo se reparte? |
| **Balances** | ¿Cuadra lo que calcula la plataforma con la realidad? |
| **Accounts** | ¿Qué fuentes he conectado y en qué estado están? |
| **Transactions** | ¿Qué ocurrió exactamente, operación por operación? |
| **Reports** | ¿Qué declaro? |

---

## 7.1 Dashboard

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FZraUvr098dLFUvm6ipLb%2Fimage.png?alt=media&token=fa653a5f-b8c9-45a1-a4b5-dccb1d39ffa9" alt="Dashboard de Investaxes"><figcaption></figcaption></figure>

**Qué es.** La pantalla a la que llegas al entrar en la plataforma. Es el panel de control: una vista de conjunto del estado de tu cuenta, con el menú de secciones a la izquierda.

**Para qué la usas.** Para orientarte. Te dice de un vistazo si hay algo que requiere tu atención —importaciones en curso, avisos pendientes— y te da acceso al resto de secciones.

**Qué revisar aquí.** Es la primera parada de cada sesión de trabajo: si hay avisos, atiéndelos antes de ponerte a hacer otra cosa. Lo que no debes hacer es sacar conclusiones fiscales del Dashboard. Los números que ves son una foto del estado actual de tu cartera, no un cálculo fiscal. El cálculo fiscal vive en Reports y sigue reglas distintas (FIFO, valores de adquisición, ejercicio cerrado).

---

## 7.2 Portfolio

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FXfgSNJMAgUFqrqOdIjfw%2Fimage.png?alt=media&token=5c538db5-be02-411e-ad04-ed2dc5d988c9" alt="Portfolio"><figcaption></figcaption></figure>

**Qué es.** La composición de tu cartera: qué activos tienes y cómo se reparte tu patrimonio entre ellos, entre las distintas redes y entre las distintas cuentas.

**Para qué la usas.** Para entender tu posición de conjunto. Es la sección más "de inversor" de la plataforma: te dice dónde está concentrado tu riesgo y qué peso tiene cada activo.

**Qué revisar aquí — y esto sí es útil fiscalmente.** El Portfolio es un buen detector de problemas de datos, porque los errores de importación suelen manifestarse como rarezas en la composición:

- **Activos que no reconoces.** Si aparece un token que no recuerdas haber tenido, puede ser un airdrop que no sabías que recibiste —y que tributa (casilla 0304)— o una clasificación errónea
- **Un activo con un peso desproporcionado.** Suele indicar un duplicado o una cantidad mal importada
- **Activos que deberían estar y no están.** Señal de que falta una fuente por importar
- **Concentración en una red que no esperabas.** Quizá tengas actividad en una blockchain que no has importado en todas sus redes

Trabaja el Portfolio antes de bajar al detalle: es más rápido detectar aquí que algo falta que descubrirlo revisando miles de transacciones.

---

## 7.3 Balances

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2F0AKPcQlicrYk5JSnp1z4%2Fimage.png?alt=media&token=1692de5e-cd61-48a2-bf47-3a0817b7e7bc" alt="Balances"><figcaption></figcaption></figure>

**Qué es.** Tus saldos, desglosados por cuenta y por criptomoneda. A diferencia del Portfolio —que te enseña la foto agregada—, Balances te enseña **cuánto hay de cada activo en cada sitio**.

**Para qué la usas.** Esta es, de todas las secciones, la **herramienta de verificación más importante de la plataforma**. Aquí es donde compruebas si lo que ha calculado Investaxes coincide con lo que tienes realmente en cada exchange y en cada wallet.

**Cómo usarla, que es lo que de verdad importa:**

Cada vez que importas una fuente, vienes aquí y comparas, moneda a moneda, con el saldo real de esa plataforma. El razonamiento es estadístico y es la base de todo el capítulo 11: el saldo final de una cuenta es el resultado acumulado de todas sus transacciones. **Si el saldo cuadra, es altísimamente probable que todas las transacciones sean correctas.** Si no cuadra, tienes un error, y lo tienes acotado a una sola fuente.

**Qué revisar aquí:**

- Que cada saldo coincida con el real, cuenta por cuenta
- Que no haya **saldos negativos**: un saldo negativo es matemáticamente imposible y significa que faltan entradas o sobran salidas
- Que no aparezcan activos con saldo en cuentas donde no deberías tener nada
- Al cerrar el ejercicio, que los saldos a 31 de diciembre coincidan con la realidad: son los que van al Impuesto sobre el Patrimonio y al Modelo 721

> Si solo vas a revisar una sección de toda la plataforma, revisa esta. Un saldo que cuadra vale más que cien transacciones revisadas a mano.

---

## 7.4 Accounts

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FLeeFotwIojlNE74FIQPd%2Fimage.png?alt=media&token=e5557959-1e29-4b1f-8627-1d03a209a879" alt="Accounts"><figcaption></figcaption></figure>

**Qué es.** El inventario de fuentes conectadas: todos los exchanges y todas las direcciones de blockchain que has incorporado a tu cuenta.

**Para qué la usas.** Es el punto de entrada de los datos y el sitio donde compruebas qué tienes conectado. Desde aquí importas direcciones de blockchain, con el flujo que vimos en 6.7.

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FWy7XXDv9AmBaB0sFtqon%2Fimage.png?alt=media&token=179dd312-352d-4a19-a40b-7312dc08c480" alt="Importar transacciones"><figcaption></figcaption></figure>

**El flujo de importación:** pulsa **Importar transacciones**, selecciona la red, introduce la dirección pública y pulsa **🚀 Iniciar importación**.

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FRmoCYkp1r81qTYetPMcz%2Fimage.png?alt=media&token=0a28b921-2abf-4b8d-903c-31a53c9c03cb" alt="Selección de red e importación"><figcaption></figcaption></figure>

**Qué revisar aquí:**

- **Contrasta esta lista con tu inventario del capítulo 5.** Es la comprobación más rentable de toda la plataforma: si una fuente de tu lista escrita no aparece en Accounts, tienes un agujero garantizado en el cálculo
- **Comprueba que cada wallet está importada en todas las redes donde operaste.** Este es el olvido más habitual: la misma dirección `0x...` puede tener historial en Ethereum, Polygon, Arbitrum y Base a la vez, y si solo la importaste en una, el resto de su actividad no existe para el sistema
- **Revisa el estado de cada cuenta.** Una importación que no terminó, o una conexión que dejó de actualizarse, deja la cuenta a medias: parece cargada, pero tiene un corte en la mitad del historial
- **Vigila las cuentas duplicadas.** La misma dirección importada dos veces genera transacciones repetidas

---

## 7.5 Transactions

<figure><img src="https://1069131240-files.gitbook.io/~/files/v0/b/gitbook-x-prod.appspot.com/o/spaces%2FF1Q2dlYB2duyEqJswk4i%2Fuploads%2FSpIOjukDi6QNa4at0EgS%2Fimage.png?alt=media&token=d7622442-145c-4f13-98e8-2d1adfdffe59" alt="Transactions"><figcaption></figcaption></figure>

**Qué es.** El registro completo de todos tus movimientos, de todas las cuentas, ordenados en el tiempo. **Es tu fuente de verdad**: lo que aparezca aquí es lo que entra en el cálculo, y lo que no aparezca no existe a efectos del informe.

**Para qué la usas.** Para tres cosas distintas:

1. **Revisar.** Filtras por tipo, fecha, cuenta o moneda y examinas bloques de operaciones
2. **Corregir.** Reclasificas movimientos mal tipificados, ajustas precios que falten, eliminas duplicados
3. **Generar el informe.** El botón **Generar Reporte** está aquí, en la esquina superior izquierda

**Qué revisar aquí.** Es donde se ejecutan las capas 2, 3 y 4 de validación del capítulo 11. En orden de impacto:

- **Filtra por `WITHDRAWAL`** y comprueba que cada salida relevante tiene su `DEPOSIT` en la cuenta de destino (apartado 11.3)
- **Filtra por `TRADE` y `SWAP`** y comprueba que cada permuta está bien clasificada. Recuerda: si cambiaste de exposición económica es `TRADE` y tributa; solo los envoltorios técnicos son `SWAP`
- **Filtra por `INCOME`** y comprueba que no hay dentro rendimientos de staking o intereses, que van a otra base imponible
- **Busca los `Unit Cost` a cero.** Convierten el importe íntegro de la venta en ganancia
- **Revisa las operaciones de DeFi** agrupadas por protocolo, usando las etiquetas si las pusiste al importar

**Consejo de método.** Revisa por bloques, no operación por operación. Filtrar por un tipo de movimiento y mirar cincuenta a la vez te permite detectar el patrón raro; ir una por una es inviable en cuanto tienes algo de volumen y no aporta más.

---

## 7.6 Reports

**Qué es.** El archivo de informes generados. Cada informe es una fotografía del cálculo en el momento en que se generó, para un ejercicio concreto.

**Para qué la usas.** Para generar, descargar y consultar tus informes fiscales.

**Estados posibles:**

| Estado | Color | Significado |
|---|---|---|
| Completado | Verde | Listo para descargar |
| Pendiente | Amarillo | Procesando — espera unos minutos |
| Error | Rojo | Ha fallado la generación |

**Acciones disponibles:** **Descargar** (PDF) y **Eliminar** (no recuperable).

**Qué revisar aquí:**

- **Comprueba la fecha de generación.** Un informe generado antes de tu última corrección contiene los datos antiguos. Tras cualquier cambio en Transactions hay que generar uno nuevo
- **Genera un informe por ejercicio.** Cada uno es independiente
- **Guarda el PDF.** Es tu soporte documental ante la AEAT y conviene conservarlo durante el plazo de prescripción

> **La confusión más común:** corregir un error y volver a abrir el informe anterior esperando ver el cambio. No lo verás. Los informes no se actualizan: se generan de nuevo.

El contenido del informe, bloque a bloque, y el orden en que conviene leerlo están en el capítulo 13.

