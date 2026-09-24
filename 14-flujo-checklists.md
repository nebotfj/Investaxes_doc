---
description: El proceso de principio a fin y las listas de comprobación antes de declarar.
icon: flag-checkered
---

# Flujo completo, checklists y conclusión

## El proceso, de principio a fin

**Fase 1 — Preparar**
1. Configura país, moneda base, método de coste, año fiscal y zona horaria
2. Elabora el inventario escrito de todas las fuentes que has usado alguna vez

**Fase 2 — Importar**
3. Importa los exchanges, uno a uno, verificando el saldo después de cada uno
4. Atiende las alertas de subida: si es concepto nuevo, espera; si el archivo es incorrecto, corrígelo
5. Importa las wallets, en todas las redes donde hayan operado, verificando el saldo
6. Importa el resto de plataformas

**Fase 3 — Revisar**
7. Reconcilia saldos cuenta por cuenta
8. Empareja las transferencias entre cuentas propias
9. Comprueba la coherencia temporal y resuelve las ventas vacías
10. Revisa la clasificación, empezando por `TRADE`/`SWAP`

**Fase 4 — Corregir**
11. Aplica el orden aguas arriba: fuentes que faltan → transferencias → clasificaciones → costes cero

**Fase 5 — Declarar**
12. Genera el informe del ejercicio
13. Revísalo empezando por notas y conciliaciones
14. Traslada los importes a las casillas (capítulo 10)
15. Presenta el Modelo 721 y el de Patrimonio si te aplican

**Fase 6 — Archivar**
16. Guarda informe, archivos originales, capturas, denuncias y declaración

## Checklist de importación

- [ ] Configuración inicial revisada (país, moneda, método, año fiscal, zona horaria)
- [ ] Inventario de fuentes escrito y completo
- [ ] Todos los exchanges importados, cubriendo todos los años
- [ ] **Cada archivo subido bajo el exchange que le corresponde**
- [ ] **Ninguna alerta de archivo incorrecto sin atender**
- [ ] Todas las wallets importadas, en todas sus redes
- [ ] Saldo verificado después de cada fuente
- [ ] Ninguna información cargada dos veces por vías distintas

## Checklist de revisión

- [ ] Cada saldo coincide con el real
- [ ] No hay saldos negativos
- [ ] Cada `WITHDRAWAL` relevante tiene su `DEPOSIT`
- [ ] No hay activos sin origen
- [ ] El informe no contiene alertas de venta vacía
- [ ] No hay `Unit Cost` a cero sin explicación
- [ ] No hay duplicados
- [ ] Permutas como `TRADE`, envoltorios como `SWAP`
- [ ] Staking e intereses como `INTEREST / STAKING`, no como `INCOME`
- [ ] Comisiones de compraventa como `PURCHASE_FEE`, las de retirada como `CASH_FLOW_FEE`
- [ ] Posiciones de liquidez agrupadas y completas

## Checklist previo a declarar

- [ ] El informe es posterior a la última corrección
- [ ] No hay alertas de venta vacía
- [ ] Las operaciones de mayor importe cuadran al revisarlas una a una
- [ ] Sé qué importe va a la casilla 0033
- [ ] Sé qué importes van a las casillas 0304 y 0305
- [ ] Tengo el detalle de las fichas 1802-1809, con su clave N o B
- [ ] Si operé con futuros o NFTs, tengo el bloque 1612-1640
- [ ] Si declaro pérdidas por robo, tengo denuncia o sentencia
- [ ] He comprobado si me aplican Modelo 721 y Patrimonio
- [ ] He anotado las pérdidas pendientes de aplicar para próximos ejercicios
- [ ] Tengo archivado todo el soporte documental

## Los ocho errores que más dinero cuestan

1. **Importar solo algunas fuentes.** El exchange olvidado suele contener el coste de adquisición de lo que vendiste en otro sitio. El FIFO es global, no por plataforma
2. **Ignorar una alerta de archivo incorrecto.** Un exchange entero que se queda fuera del cálculo
3. **No emparejar las transferencias.** Una sola transferencia huérfana puede inflar la ganancia notablemente
4. **Ignorar las alertas de venta vacía.** Sin coste localizado, el cálculo asume el peor escenario y el error se propaga
5. **No revisar los costes a cero.** Convierten el importe íntegro de la venta en ganancia
6. **Confundir TRADE con SWAP.** Permutar cripto por cripto tributa; envolver un token no
7. **Olvidar que pagar con cripto es transmitir.** Tiene incluso clave propia en el modelo: la B
8. **Mezclar staking con ingresos generales.** Van a bases distintas y tributan a escalas distintas

## Advertencia final

La Agencia Tributaria dispone de información directa de los exchanges y puede analizar la blockchain pública. El coste de regularizar a posteriori —recargo, intereses y sanción— es muy superior al de declarar correctamente desde el principio.

Y una observación práctica: casi todos los casos de factura fiscal desproporcionada no vienen de haber ganado mucho, sino de **datos incompletos**. Una ganancia inflada por ventas vacías o costes a cero se paga igual que una ganancia real. Por eso los capítulos 11 y 12 son, en la práctica, los que más dinero ahorran.

---

# Preguntas frecuentes

**Me ha dado error al subir un CSV. ¿Qué hago?**
Depende del motivo. Si la alerta dice que se ha detectado un concepto nuevo, no tienes que hacer nada: el equipo lo integra y las transacciones se incorporan solas. Si la alerta indica que el archivo no es correcto, revísalo —lo más probable es que lo estés subiendo bajo un exchange que no le corresponde— y vuelve a subirlo.

**¿Tributa cambiar una cripto por otra?**
Sí. Es un `TRADE` y se declara con clave de contraprestación **N**. La permuta está expresamente contemplada en el art. 37.1.h LIRPF.

**¿Y convertir ETH en WETH, o BTC en WBTC?**
No. Es un `SWAP`: sigues expuesto exactamente al mismo activo.

**¿Tributa pagar un producto con criptomonedas?**
Sí. Es un `EXPENSE` y se considera una venta en el momento en que se produce. Tiene su propia clave: **B**.

**¿Y quemar un LP token al cerrar una posición de liquidez?**
No. Es un `EXPENSE_NOT_TAXABLE`: se calcula por FIFO para mantener el inventario cuadrado, pero el resultado no se incorpora a la declaración.

**¿Tributa recibir el principal de un préstamo en DeFi?**
No. Es un `INCOME_NOT_TAXABLE`. Cuando devuelves ese principal se registra como `EXPENSE` y sí computa.

**¿Puedo declarar solo el exchange donde vendí?**
No. Los criptoactivos del mismo protocolo son bienes homogéneos, y operar en distintos exchanges no altera esa homogeneidad. El FIFO se calcula sobre el conjunto de tu cartera.

**¿Se deducen las comisiones?**
Las de compra y venta sí, porque guardan relación directa con la operación. Las de depósito, retiro y transferencia entre carteras no.

**¿El staking y los airdrops tributan igual?**
No. El staking es rendimiento del capital mobiliario y va a la base del ahorro (casilla 0033). Los airdrops son ganancia no derivada de transmisión y van a la base general (casilla 0304).

**¿Los cashbacks de tarjetas cripto tributan?**
Sí, como rendimiento del capital mobiliario, con el valor en euros del momento de la recepción.

**¿Puedo deducir una pérdida por robo, hackeo o estafa piramidal?**
Potencialmente, pero el criterio es restrictivo: el crédito debe resultar judicialmente incobrable, y la imputación puede hacerse cuando se cumpla un año desde el inicio del procedimiento judicial de ejecución sin que se haya satisfecho. Necesitas denuncia o sentencia firme.

**¿Tengo que declarar mi hardware wallet en el Modelo 721?**
Depende de quién custodie las claves, no de si el monedero está conectado a internet. Si controlas tú las claves privadas, esos saldos no se computan ni se informan. La obligación surge cuando un tercero no residente presta el servicio de salvaguarda de claves.

**¿Y en el Impuesto sobre el Patrimonio?**
Ahí sí entra todo, con independencia de quién lo custodie, valorado a precio de mercado a 31 de diciembre.

**¿Tengo que importar un exchange que usé tres meses hace años?**
Sí, y es probablemente el más importante. Si compraste allí monedas que vendiste después en otro sitio, ese exchange tiene el coste de adquisición de esas ventas.

**¿Por qué mi ganancia es mucho mayor de lo que esperaba?**
Las causas habituales son transferencias sin emparejar y costes de adquisición a cero. Revisa 11.3 y 12.4.

**¿Cada cuánto debo revisar todo esto?**
La revisión completa se hace una vez, al construir el histórico. Después basta con verificar los saldos al cerrar cada ejercicio y revisar las operaciones nuevas de protocolos que no hubieras usado antes.
