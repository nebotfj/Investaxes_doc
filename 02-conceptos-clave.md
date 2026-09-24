# Conceptos clave: Trazabilidad y Método FIFO

Antes de usar Investaxes, necesitas entender DOS conceptos fundamentales que Hacienda exige.

## ¿Qué es la Trazabilidad?

**Definición:** La trazabilidad es reconstruir el **historial completo** de tu actividad criptográfica para obtener un registro claro y detallado de:
- El **origen** de cada criptomoneda (precio de compra, fecha, dónde se compró)
- Todas las **transferencias** entre plataformas y wallets
- La **fecha y precio** de cada venta o intercambio
- Cálculo correcto de **ganancias/pérdidas**

### ¿Por qué es imprescindible la trazabilidad?

Imagina este escenario:

```
1. Compras 1 BTC el 1/1/2023 a €30,000 en Binance
2. Transferencias ese BTC el 15/2/2023 a Kraken
3. Vendes ese BTC el 1/3/2023 a €42,000

¿Cuál es tu ganancia?
Correcta: €42,000 - €30,000 = €12,000

PERO...
Si solo usas el informe de Kraken:
- Kraken sabe que vendiste 1 BTC por €42,000
- Pero Kraken NO sabe dónde lo compraste ni a qué precio
- Kraken asume que el precio de compra es €0
- Por lo tanto, calcula ganancia como €42,000 (INCORRECTO)
- Pagarías impuesto sobre €42,000 en lugar de €12,000
- ¡Diferencia: €6,300 de impuesto extra!
```

**Este es exactamente el problema que Investaxes resuelve.**

## Método FIFO (First In, First Out)

### ¿Qué es?

FIFO significa que cuando vendes una criptomoneda, se asume que vendes las **primeras unidades que compraste**.

### Ejemplo práctico

```
Historial de Bitcoin:
- Enero 2023: Compras 1 BTC a €30,000
- Marzo 2023: Compras 1 BTC a €35,000
- Mayo 2023: Compras 1 BTC a €40,000

Total: 3 BTC por €105,000

Luego en Junio 2023, vendes 2 BTC a €45,000 cada uno = €90,000 total

Con FIFO:
- El primer BTC vendido (€45,000) viene de la compra de enero (€30,000)
  Ganancia: €45,000 - €30,000 = €15,000
- El segundo BTC vendido (€45,000) viene de la compra de marzo (€35,000)
  Ganancia: €45,000 - €35,000 = €10,000
- Total ganancia: €25,000

Total BTC restante: 1 BTC (el de mayo a €40,000)
```

### ¿Por qué FIFO y no LIFO o Average Cost?

La Agencia Tributaria española (AEAT) acepta explícitamente **SOLO FIFO** para criptomonedas. Es un requisito legal, no opcional.

### ¿Cómo Investaxes aplica FIFO?

Investaxes automáticamente:
1. Rastrea el orden cronológico de cada compra
2. Cuando vendes, empareja la venta con la compra más antigua disponible
3. Calcula ganancia/pérdida para esa pareja específica
4. Repite para cada unidad vendida
