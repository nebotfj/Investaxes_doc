# DeFi y sus Desafíos Fiscales

Si has usado wallets descentralizadas como **MetaMask, TrustWallet, Ledger**, has operado en **DeFi**.

## ¿Qué es DeFi?

**Definición:** Finanzas Descentralizadas. Operaciones financieras en blockchain sin intermediarios bancarios.

**Características:**
- ✅ No hay exchange central que guarde tus datos
- ✅ Transacciones directas entre wallets
- ✅ Plataformas como Uniswap, Aave, PancakeSwap, etc.
- ✅ Smart contracts automatizan las operaciones
- ❌ No hay un "informe fiscal" centralizado

## Problemas de DeFi para la declaración

### Problema 1: Falta de historial centralizado

En un exchange como Binance, recibes un CSV con todas tus operaciones. En DeFi, **no existe ese CSV**. Las transacciones solo están en la blockchain pública.

### Problema 2: Aplicar método FIFO es complicado

Cuando haces un swap en Uniswap:
- La blockchain registra: "1 ETH salió, 2000 USDC entraron"
- **Pero NO registra:** El precio original del ETH que compraste
- Para calcular ganancia, necesitas recordar: ¿cuándo compré este ETH? ¿A qué precio?

### Problema 3: Múltiples blockchains y wallets

Tu actividad DeFi se distribuye entre:
- Ethereum, Polygon, Solana, Arbitrum, etc.
- MetaMask, TrustWallet, wallets de hard wallet, etc.
- Múltiples plataformas (Uniswap, Aave, Curve, etc.)

Reconstruir todo manualmente es **prácticamente imposible**.

## Ejemplo real de error en DeFi

```
Situación: Operaste en DeFi sin trazabilidad

1. Enero 2023: Compras 1 ETH a €1,000 en Coinbase
2. Febrero 2023: Transfieres a MetaMask
3. Marzo 2023: En Uniswap, cambias 1 ETH por 20 USDC (ETH vale €2,000)
   Ganancia real: €2,000 - €1,000 = €1,000

SIN TRAZABILIDAD:
- MetaMask solo muestra: "1 ETH salió, 20 USDC entraron"
- No sabe que compraste ETH a €1,000
- Calcula ganancia como: €2,000 (precio actual de venta) - €0 = €2,000

IMPACTO:
- Impuesto pagado correctamente: €1,000 × 21% = €210
- Impuesto pagado sin trazabilidad: €2,000 × 21% = €420
- Diferencia: €210 PAGADO DE MENOS = Multa + intereses + sanción
```

## Cómo Investaxes resuelve DeFi

1. **Conexión de wallets:** Importas tu dirección blockchain (sin claves privadas)
2. **Escaneo on-chain:** Investaxes analiza toda la blockchain de esa dirección
3. **Reconstrucción:** Conecta cada operación DeFi con su origen (compra en exchange)
4. **Cálculo FIFO:** Aplica automáticamente FIFO a través de todas tus operaciones
5. **Reporte unificado:** Un único reporte con DeFi + exchanges

