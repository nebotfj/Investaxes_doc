---
description: Por qué operar en protocolos descentralizados complica la trazabilidad y cómo se resuelve.
icon: network-wired
---

# DeFi y sus desafíos fiscales

Si has usado wallets autocustodiadas (MetaMask, Ledger, Trust Wallet), has operado en DeFi.

## Los tres problemas estructurales

**1. No hay informe central.** Un exchange te entrega un archivo con tus operaciones. Los protocolos descentralizados no resumen nada: las transacciones solo existen en la blockchain.

**2. Aplicar FIFO es difícil.** Cuando haces una permuta en un DEX, la cadena registra "salió 1 ETH, entraron 2.000 USDC", pero no registra a qué precio compraste ese ETH ni cuándo. Determinar el coste original se complica aún más cuando los fondos han pasado por varios monederos.

**3. La importación deja lagunas.** Al volcar datos de múltiples redes y protocolos aparecen errores y huecos que hay que detectar y corregir manualmente.

## Ejemplo de error por falta de trazabilidad

```
1. Enero 2023:  compras 1 ETH a 1.000 € en un exchange
2. Febrero 2023: lo transfieres a tu wallet
3. Marzo 2023:  permutas 1 ETH por USDC (ETH vale 2.000 €)

Resultado real: 2.000 - 1.000 = 1.000 € de ganancia

Sin trazabilidad:
- La wallet solo ve "salió 1 ETH, entraron USDC"
- No conoce el coste de adquisición
- Calcula 2.000 € de ganancia en lugar de 1.000 €
```

## Las operaciones DeFi que más problemas dan

| Operación | Por qué complica la trazabilidad |
|---|---|
| **Pools de liquidez** | Generan un token nuevo (`MINTING`), recompensas periódicas y una quema al cerrar. Si no se leen como una posición única, aparecen como decenas de movimientos sueltos |
| **Lending** | El principal recibido no es renta (`INCOME_NOT_TAXABLE`) pero su devolución sí computa (`EXPENSE`). Confundirlos altera el resultado en ambos extremos |
| **Bridges y envoltorios** | Retiras BTC y te llega WBTC. No es una venta: es un `SWAP`. Si se lee como retirada sin destino, genera una venta vacía |
| **Staking en protocolo** | El bloqueo puede emitir un token de representación. Ese token no es un ingreso, pero las recompensas sí |
| **Permutas en DEX** | Coloquialmente se llaman *swaps*, pero fiscalmente casi siempre son `TRADE` y tributan (capítulo 8) |

## Cómo lo resuelve Investaxes

1. Importas tu dirección pública de blockchain (nunca claves privadas)
2. El sistema escanea toda la actividad on-chain de esa dirección
3. Enlaza cada operación DeFi con su origen en exchange
4. Aplica FIFO de forma transversal a todas tus cuentas
5. Genera un informe unificado que integra DeFi y exchanges

