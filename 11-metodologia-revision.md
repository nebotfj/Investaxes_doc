---
description: Las cuatro capas de validación y el orden de corrección que ahorra más trabajo.
icon: magnifying-glass
---

# Metodología de revisión: qué mirar y en qué orden

## 11.1 El principio rector: verificar saldos fuente a fuente

**Cada vez que cargues información de una fuente, ve a Balances y comprueba que el saldo coincide con el que tienes realmente en esa plataforma.**

La razón es estadística: el saldo final es el resultado acumulado de todas las transacciones de esa cuenta. **Si el saldo cuadra, es altísimamente probable que todas las transacciones sean correctas.** Si no cuadra, tienes un error localizado en una sola fuente.

Lo que **no** debes hacer es cargarlo todo y revisar al final. En ese escenario, cuando algo no cuadra, no sabes qué fuente lo causó.

## 11.2 Las cuatro capas de validación

| Capa | Qué comprueba | Qué errores detecta |
|---|---|---|
| **1. Reconciliación de saldos** | Que el saldo calculado coincida con el real | Transacciones que faltan, duplicados, importaciones parciales |
| **2. Emparejamiento de transferencias** | Que cada salida entre cuentas propias tenga su entrada | Ventas simuladas, costes a cero |
| **3. Coherencia temporal** | Que hubiera saldo suficiente en cada operación | Ventas vacías, huecos en el historial |
| **4. Clasificación** | Que cada movimiento esté en su tipo correcto | Errores de tributación |

## 11.3 Capa 2 — El emparejamiento de transferencias

**El concepto.** Un movimiento entre dos cuentas tuyas no es una venta. **El coste de adquisición tiene que viajar con las monedas.**

| Situación | Cómo lo interpreta el sistema | Consecuencia |
|---|---|---|
| `WITHDRAWAL` sin su `DEPOSIT` | Salida sin destino conocido | **Venta simulada** |
| `DEPOSIT` sin su `WITHDRAWAL` | Entrada sin origen conocido | **Coste de adquisición cero** |

**Qué revisar:**

1. Filtra en **Transactions** por tipo `WITHDRAWAL`
2. Localiza el `DEPOSIT` correspondiente en la cuenta de destino
3. Comprueba: **misma cantidad** (descontando gas), **misma fecha aproximada**, **mismo activo**
4. Empieza por las transferencias de mayor importe

**Grados de coincidencia:**

| Situación | Qué significa | Qué hacer |
|---|---|---|
| Coincidencia completa | Cantidad, fecha y activo cuadran | Nada |
| Diferencia del 1-10 % | Comisión de red descontada en tránsito | Normal. Verifica que corresponde al gas |
| Desfase horario | Envío y recepción en horas distintas | Normal entre redes. Comprueba que no cruza el 31 de diciembre |
| Sin coincidencia | Falta uno de los dos extremos | **Corregir** |

## 11.4 Capa 3 — La coherencia temporal

Verificar que **en el momento de cada operación existía saldo suficiente**. Si el sistema registra que vendiste 2 ETH el 15 de marzo pero tu historial solo acumula 1 ETH adquirido, falta una compra.

**Qué revisar:**

- Operaciones cuyo activo no aparece adquirido en ninguna fecha anterior
- Saldos que se vuelven negativos en algún punto
- Activos que aparecen de la nada sin `DEPOSIT` ni compra previa

## 11.5 Capa 4 — La clasificación

**Por orden de impacto fiscal:**

1. **TRADE frente a SWAP.** El error más caro
2. **EXPENSE frente a EXPENSE_NOT_TAXABLE.** Devolver un préstamo computa; quemar un LP token no
3. **INCOME frente a INCOME_NOT_TAXABLE.** El principal de un préstamo no es renta
4. **STAKING/INTEREST frente a INCOME.** El primero va a la base del ahorro (0033) y el segundo a la general (0304)
5. **PURCHASE_FEE frente a CASH_FLOW_FEE.** El primero reduce tu ganancia; el segundo no computa
6. **Transferencias internas mal tipificadas**

## 11.6 El orden de corrección: aguas arriba primero

```
1. Conectar las fuentes que faltan
        ↓
2. Emparejar las transferencias
        ↓
3. Corregir las clasificaciones
        ↓
4. Resolver a mano los costes cero que queden
```

Cada paso aguas arriba resuelve decenas de problemas aguas abajo. Si importas el exchange que faltaba, docenas de ventas vacías desaparecen solas.

