---
description: Los tres conceptos que sostienen todo el cálculo fiscal. Si uno falla, el informe entero falla.
icon: lightbulb
---

# Conceptos clave: trazabilidad, FIFO y FMV

Tres conceptos sostienen todo el cálculo. Si alguno falla, el informe entero falla.

## Trazabilidad

La trazabilidad consiste en **volcar, revisar y corregir** toda la información relacionada con tus transacciones para reconstruir el historial completo: el origen de cada unidad de criptomoneda (cuándo se adquirió, a qué precio, dónde), todas las transferencias entre plataformas y wallets, y la fecha y precio de cada transmisión.

No es un proceso automático. Es un trabajo de reconstrucción que requiere revisión.

**Por qué es imprescindible:**

```
1. Compras 1 BTC el 1/1/2023 a 30.000 € en el Exchange A
2. Lo transfieres el 15/2/2023 al Exchange B
3. Lo vendes el 1/3/2023 por 42.000 €

Ganancia real: 42.000 - 30.000 = 12.000 €

Si solo usas el informe del Exchange B:
- Sabe que vendiste 1 BTC por 42.000 €
- NO sabe cuándo, ni dónde, ni a qué precio lo compraste
- Asume coste de adquisición 0
- Calcula una ganancia de 42.000 € en lugar de 12.000 €
```

El exchange donde vendes no tiene forma de saber lo que ocurrió antes de que el activo llegara a él. Esa laguna es la que rellena la trazabilidad.

**Los cinco pasos del proceso:**

1. Consolidar las transacciones de todos los exchanges y wallets, calientes y frías
2. Identificar los errores de importación
3. Analizar la cadena para localizar las transacciones perdidas
4. Clasificar correctamente cada tipo de operativa (trading, staking, DeFi)
5. Recalcular ganancias y pérdidas aplicando FIFO

Los capítulos 11 y 12 desarrollan cada uno de estos pasos.

## Método FIFO (First In, First Out)

Cuando transmites una criptomoneda, se considera que transmites **las primeras unidades que adquiriste**.

```
Historial de Bitcoin:
- Enero 2023:  compras 1 BTC a 30.000 €
- Marzo 2023:  compras 1 BTC a 35.000 €
- Mayo 2023:   compras 1 BTC a 40.000 €

Junio 2023: vendes 2 BTC a 45.000 € cada uno

Con FIFO:
- 1.ª venta ← compra de enero:  45.000 - 30.000 = 15.000 € de ganancia
- 2.ª venta ← compra de marzo:  45.000 - 35.000 = 10.000 € de ganancia
- Ganancia total: 25.000 €
- Queda 1 BTC en cartera, con coste 40.000 €
```

**Por qué FIFO y por qué es global.** La ley establece que, cuando existen bienes homogéneos, se consideran transmitidos los adquiridos en primer lugar. Los criptoactivos del mismo protocolo son bienes homogéneos entre sí. Y hay un matiz decisivo: **que los adquieras y transmitas en exchanges distintos no altera esa homogeneidad**. El cálculo es global sobre toda tu cartera, sin separar por plataforma.

Eso convierte la trazabilidad completa en un requisito, no en una buena práctica: no puedes calcular bien un exchange aislado, porque su FIFO depende de lo que compraste en los demás. El detalle jurídico está en el capítulo 9.

**La consecuencia que casi nadie anticipa:** como cada venta consume la compra más antigua disponible, **un error en una transacción de 2021 desplaza el cálculo de todas las ventas posteriores**. No son errores aislados: se propagan hacia adelante. Por eso el orden de corrección importa tanto (capítulo 11).

## FMV (Fair Market Value)

El **FMV** es el valor de mercado del activo en el momento exacto en que entra en tu patrimonio. Es el dato que fija el **coste de adquisición** de todo lo que recibes sin comprarlo: una recompensa de staking, un airdrop, una recompensa de minería.

El FMV cumple doble función: es la **base imponible del ingreso** el día que lo recibes, y es el **coste de adquisición** el día que lo vendas. Si recibes un token valorado en 100 € y lo vendes después por 150 €, tributas 100 € como ingreso y 50 € como ganancia patrimonial —no 150 € dos veces.

