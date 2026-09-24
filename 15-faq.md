---
description: Respuestas rápidas a las dudas más habituales sobre tributación y uso de la plataforma.
icon: circle-question
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
