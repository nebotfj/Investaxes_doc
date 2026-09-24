# Tipos de movimientos y su tratamiento fiscal

Investaxes clasifica tus transacciones en tipos que tienen implicaciones **legales específicas** en España.

## INFLOW (Entrada de activos - Actividades gravadas)

### Internal Transfer
- **Qué es:** Transferencia entre tus propias cuentas
- **Ejemplo:** Binance → Tu wallet MetaMask
- **Impuesto:** ✅ NO tributa
- **Declaración:** No requiere declaración especial

### Taxable Income
- **Qué es:** Ingreso que genera obligación fiscal
- **Ejemplos:** 
  - Pago por trabajo/servicios en cripto
  - Mining
  - Recompensas de airdrops
- **Impuesto:** ✅ SÍ tributa como "Rendimiento del trabajo" o "Actividad económica"
- **Valor:** Precio de mercado en el momento de recepción
- **Declaración:** Modelo 100, línea "Actividad económica" o "Rendimientos del trabajo"

### Non-Taxable Income
- **Qué es:** Ingreso que no genera IRPF
- **Ejemplos:** Herencia (aunque tiene su propio impuesto), Donación
- **Impuesto:** ❌ NO IRPF (pero sí Impuesto de Sucesiones/Donaciones)
- **Declaración:** Modelo 651 (Sucesiones y Donaciones)

### Financial Income
- **Qué es:** Rendimientos de operaciones financieras
- **Ejemplos:**
  - Staking rewards (bloqueo de activos)
  - Intereses de lending (préstamos)
  - Rewards de yield farming
- **Impuesto:** ✅ SÍ tributa como "Rendimiento del capital mobiliario"
- **Valor:** Precio de mercado cuando se reciben
- **Declaración:** Modelo 100, casilla "Rendimientos del capital"

## OUTFLOW (Salida de activos)

### Internal Transfer
- **Qué es:** Envío entre tus propias cuentas
- **Ejemplo:** Tu wallet → Kraken
- **Impuesto:** ✅ NO tributa
- **Nota:** No es una "venta" desde perspectiva fiscal

### Liquidation
- **Qué es:** Conversión a dinero fiat (EUR)
- **Ejemplo:** Vender 1 BTC por euros
- **Impuesto:** ✅ SÍ tributa como "Ganancia/Pérdida patrimonial"
- **Cálculo:** Precio venta - Precio compra original - Comisiones
- **Declaración:** Modelo 100, casilla "Ganancias/Pérdidas patrimoniales"

### Non-Taxable Outflow
- **Qué es:** Salida sin obligación fiscal
- **Ejemplo:** Donación a terceros
- **Impuesto:** ✅ NO IRPF (pero puede afectar patrimonio)

### Financial Expense
- **Qué es:** Gastos financieros
- **Ejemplo:** Comisiones en ciertos contextos
- **Impuesto:** Depende del contexto

## TRADE / SWAP (Intercambio criptomoneda-a-criptomoneda)

**ESTE ES EL MÁS IMPORTANTE PARA IMPUESTOS.**

### Concepto fiscal

Cambiar una criptomoneda por otra (sin pasar por EUR) **TRIBUTA** como si hubieras vendido.

### Ejemplo completo

```
1/1/2024: Compras 1 BTC por €30,000
15/6/2024: Cambias 1 BTC por 15 ETH en Uniswap

En el momento del swap:
- 1 BTC vale: €45,000
- 15 ETH cuestan: €45,000 cada uno (€3,000 cada)

Desde perspectiva fiscal:
- SALIDA: 1 BTC (precio venta: €45,000)
- ENTRADA: 15 ETH (precio compra: €45,000)
- GANANCIA: €45,000 - €30,000 = €15,000
- IMPUESTO (21%): €3,150

El hecho de que no recibiste euros es IRRELEVANTE.
La ley dice que "transmisión de activos" tributa.
```

### Tabla resumen: Tributación fiscal de cada tipo

| Tipo de Movimiento | ¿Tributa? | Modelo | Impuesto |
|---|---|---|---|
| Buy (Compra) | ❌ NO | Ninguno | Ninguno |
| Hold (Retención) | ❌ NO | Ninguno | Ninguno |
| Internal Transfer | ❌ NO | Modelo 721 (si >€50k en exchange extranjero) | Ninguno |
| Sell (Venta por EUR) | ✅ SÍ | Modelo 100, línea 400-449 | 19-28% sobre ganancia |
| Swap/Trade (Cripto a Cripto) | ✅ SÍ | Modelo 100, línea 400-449 | 19-28% sobre ganancia |
| Staking/Rewards | ✅ SÍ | Modelo 100, línea 450-459 | 19-47% progresivo |
| Mining | ✅ SÍ | Modelo 100 (Actividad económica) | 19-47% progresivo |
| Airdrop | ✅ SÍ | Modelo 100, línea 400-404 | 19-28% |
| Herencia | Especial | Modelo 651 | Impuesto Sucesiones (5-34%) |
| Donación | Especial | Modelo 651 | Impuesto Donaciones (7-34%) |

