---
description: INFLOW, OUTFLOW y TRADE: qué es cada movimiento y si llega o no a la declaración.
icon: arrow-right-arrow-left
---

# Tipos de movimiento y su tratamiento fiscal

Investaxes organiza **todos** los movimientos en tres familias, según cómo afectan a tu patrimonio:

| Familia | Qué ocurre |
|---|---|
| **INFLOW** | Entran activos en tu patrimonio |
| **OUTFLOW** | Salen activos de tu patrimonio |
| **TRADE** | Hay entrada y salida simultáneas: un activo se intercambia por otro |

Cada movimiento se registra en columnas propias: `Inflow Quantity`, `Inflow Asset`, `Inflow Unitary Cost` para lo que entra; `Outflow Quantity`, `Outflow Asset`, `Outflow Unitary Cost` para lo que sale.

Lo esencial: **una entrada fija el coste de adquisición; una salida lo consume**. De ahí que clasificar mal un movimiento no solo afecte a ese movimiento, sino a todos los posteriores que dependan de ese coste.

---

## 8.1 Movimientos de tipo INFLOW

### A. Inflows por transferencia — no son renta

#### DEPOSIT

**Qué es.** Transferencia de cripto que llega desde otra wallet o cuenta de exchange **de tu propiedad**. No cambia de dueño: solo cambia de ubicación.

**Ejemplos.** Enviar BTC de tu cold wallet a tu cuenta de exchange. Mover USDC entre dos wallets tuyas.

**Qué hace Investaxes.** Mantiene el coste histórico previo. No crea un coste nuevo.

**Consecuencia fiscal.** **No hay evento fiscal.** Es un traslado interno.

#### INCOME_NOT_TAXABLE

**Qué es.** Una entrada de activos que **no constituye renta**. Recibes algo, pero ese algo no es un ingreso: es dinero que ya era tuyo, o dinero prestado que tendrás que devolver.

**Ejemplos.**
- Recibir el principal de un préstamo en un protocolo de lending (por ejemplo, AAVE): el protocolo te entrega fondos, pero son deuda, no ganancia
- Reembolso del principal que habías depositado
- Aportaciones de fondos que no suponen incremento patrimonial

**Qué hace Investaxes.** Registra la entrada y la valora a FMV, **exactamente igual que un INCOME**. La diferencia está en el destino: este valor no se traslada a la declaración.

**Consecuencia fiscal.** **No genera evento fiscal.** No tributa y **no se incorpora a ninguna casilla**.

> **Regla mental:** `INCOME_NOT_TAXABLE` hace mecánicamente lo mismo que `INCOME` —entra, se valora, fija coste— pero **no tributa**.

### B. Inflows por rendimiento — sí son renta

Todos se valoran a **FMV en el momento de la recepción**, y ese FMV se convierte en su coste fiscal de adquisición.

#### INCOME

**Qué es.** Ingreso gravado que no encaja en ninguna de las categorías específicas siguientes.

**Ejemplos.** Cobro de un servicio profesional en cripto. Ingresos de *play2earn*. Premios recibidos.

**Consecuencia fiscal.** Tributa. El FMV de recepción es la base imponible y a la vez el coste de adquisición para la venta futura.

#### MINING

**Qué es.** Recompensas obtenidas por minar: recompensas de bloque y comisiones de transacción percibidas por validar.

**Consecuencia fiscal.** Rendimiento de **actividad económica**. Base **general**. Detalle en 9.5.

#### AIRDROP / GIFT

**Qué es.** Tokens recibidos por campañas de distribución o por aparecer en un *snapshot* de titulares.

**Consecuencia fiscal.** **Ganancia patrimonial no derivada de transmisión**, a precio de mercado en el momento de recepción. Base **general**, casilla 0304. Detalle en 9.3.

#### INTEREST / STAKING

**Qué es.** Rendimientos obtenidos por ceder tus activos: lending, cuentas remuneradas, productos CeFi, recompensas de staking. También los **cashbacks**.

**Consecuencia fiscal.** **Rendimiento del capital mobiliario**, al FMV recibido. Base del **ahorro**, casilla **0033**. Detalle en 9.2.

#### MINTING

**Qué es.** Creación de un token nuevo: un NFT que acuñas, un LP token que recibes al aportar liquidez a un pool.

**Qué hace Investaxes.** El coste del token acuñado equivale al **colateral aportado más las comisiones de gas**.

**Consecuencia fiscal.** No es renta: es una transformación de valor que ya tenías.

### C. Inflows de derivados

#### DERIVATIVES PROFIT

**Qué es.** Ganancia neta realizada en productos derivados al cerrar la posición.

**Qué hace Investaxes.** Registra la entrada con el valor ya realizado. No se recalcula por FIFO.

**Consecuencia fiscal.** Base del ahorro, casillas 1612-1640 (ver 10.5).

---

## 8.2 Movimientos de tipo OUTFLOW

### A. Outflows por transferencia

#### WITHDRAWAL

**Qué es.** Salida de cripto hacia otra wallet o cuenta de exchange **de tu propiedad**.

**Consecuencia fiscal.** **No hay evento fiscal.** Es el espejo exacto de `DEPOSIT`.

> Todo `WITHDRAWAL` debería casar con un `DEPOSIT` en la cuenta de destino. Si no casa, tienes un problema de trazabilidad grave (11.3).

#### EXPENSE_NOT_TAXABLE

**Qué es.** Un gasto **fiscalmente irrelevante**. El activo sale de tu patrimonio de forma definitiva, pero esa salida no debe producir efectos en tu declaración.

**Ejemplos.** Quema de LP Token Pool: cuando retiras liquidez de un pool, el LP token que representaba tu participación se destruye. Ese token desaparece, pero su desaparición no es una operación económica real.

**Qué hace Investaxes — importante.** Se procesa **como una venta**: consume inventario y se casa por FIFO contra tus adquisiciones previas. La diferencia está en el tratamiento del resultado: **la ganancia o pérdida que arroja ese cálculo FIFO no se incorpora a los estados financieros ni a la declaración**. Se calcula para mantener el inventario cuadrado, y se descarta a efectos fiscales.

**Consecuencia fiscal.** **No tributa y no aparece en ninguna casilla.**

> **Regla mental:** `EXPENSE_NOT_TAXABLE` hace mecánicamente lo mismo que `EXPENSE` —sale, se casa por FIFO, consume coste— pero **su resultado no llega a la declaración**.

### B. Outflows por comisiones

#### PURCHASE_FEE

**Qué es.** Comisiones específicas de compra o venta en un exchange (comisiones *maker* / *taker*).

**Consecuencia fiscal.** **Sí computan.** Suman al valor de adquisición cuando compras y restan del valor de transmisión cuando vendes. Fundamento en 9.1.

#### CASH_FLOW_FEE

**Qué es.** Comisiones ligadas a movimientos de retirada, de cripto o de fiat.

**Consecuencia fiscal.** **No computan.** No guardan relación directa con una operación de transmisión. Fundamento en 9.1.

#### TRANSACTION_FEE

**Qué es.** Gas fees o comisiones de red de cualquier operación en blockchain.

**Consecuencia fiscal.** Se asocia a la transacción principal a la que acompaña.

#### EXPENSE

**Qué es.** Salida del valor pagado. **Se considera una venta en el momento en que se produce**: entregas un activo con valor de mercado a cambio de algo, y eso realiza la plusvalía latente.

**Ejemplos.**
- Devolución del principal de un préstamo en un protocolo de lending
- Pagar un bien o un servicio con criptomonedas

**Consecuencia fiscal.** **Sí tributa.** El resultado del FIFO **sí se incorpora**. Se declara con **clave de contraprestación B** (bienes o servicios). Ver 10.4.

> Pagar un café con Bitcoin es una transmisión. Si ese BTC valía menos cuando lo compraste, has realizado una ganancia patrimonial aunque solo estuvieras desayunando.

### C. Outflows de derivados

#### DERIVATIVES LOSS

**Qué es.** Pérdida neta realizada en futuros, perpetuals u opciones.

**Consecuencia fiscal.** Pérdida computable en la base del ahorro.

#### LIQUIDATION

**Qué es.** Cierre forzoso de una posición, típicamente por un *margin call*.

**Qué hace Investaxes.** Registra la **pérdida total del colateral**.

**Consecuencia fiscal.** Pérdida computable.

### D. Outflows especiales

#### LOST

**Qué es.** Pérdida por error propio: envío a una wallet equivocada, pérdida de claves privadas.

**Consecuencia fiscal.** Pérdida no derivada de transmisión (casilla 0305), **deducible solo con prueba**.

#### STOLEN

**Qué es.** Fondos sustraídos por terceros: hackeo, estafa, phishing, esquemas Ponzi.

**Consecuencia fiscal.** Casilla 0305. **Requiere denuncia presentada o sentencia judicial firme.** Criterios de imputación en 9.4.

#### DONATE

**Qué es.** Donación de criptomonedas a un tercero.

**Qué hace Investaxes.** Calcula el resultado a **precio de mercado menos coste de adquisición**.

**Consecuencia fiscal.** **Genera ganancia o pérdida patrimonial para quien dona.** El receptor queda sujeto al Impuesto sobre Sucesiones y Donaciones, un tributo distinto y autonómico.

---

## 8.3 Movimientos de tipo TRADE — y la diferencia con SWAP

#### TRADE

**Qué es.** La acción genérica para operaciones de mercado donde existe **un cambio económico real**. Cubre compraventas (EUR ↔ cripto) y permutas (cripto ↔ cripto).

**Ejemplos.** BTC → USDT. ETH → DAI. BTC → EUR.

**Consecuencia fiscal.** **Genera ganancia o pérdida patrimonial sujeta a tributación.** Se calcula por FIFO y se declara en las casillas 1802-1809 con **clave N** (otra moneda virtual) o **B** (bienes o servicios).

**Permutar una cripto por otra tributa.** Que no hayas recibido euros es irrelevante.

#### SWAP

**Qué es.** Se reserva para **intercambios no imponibles entre activos económicamente equivalentes**. No hay variación patrimonial ni cambio de exposición económica.

**Ejemplos.** ETH ↔ WETH. WETH ↔ aWETH. BTC ↔ WBTC.

**Consecuencia fiscal.** **No tributa.**

#### El criterio práctico

| Pregunta | Respuesta | Clasificación |
|---|---|---|
| ¿He cambiado realmente de activo o de exposición económica? | Sí | **TRADE** |
| ¿Solo ha cambiado la forma técnica del mismo activo? | Sí | **SWAP** |

> **Atención:** el uso coloquial de "swap" en DeFi no coincide con este criterio. Cambiar ETH por USDC en un DEX se llama coloquialmente *swap*, pero es un **TRADE**.

---

## 8.4 Tabla resumen de todos los movimientos

| Movimiento | Familia | Qué es | ¿Llega a la declaración? |
|---|---|---|---|
| **DEPOSIT** | INFLOW · transferencia | Entrada desde cuenta propia | No — traslado interno |
| **INCOME_NOT_TAXABLE** | INFLOW · transferencia | Entrada que no es renta | No |
| **INCOME** | INFLOW · rendimiento | Ingreso gravado no categorizado | Sí — base general |
| **MINING** | INFLOW · rendimiento | Recompensas de minería | Sí — actividad económica |
| **AIRDROP / GIFT** | INFLOW · rendimiento | Tokens por campaña o snapshot | Sí — casilla 0304 |
| **INTEREST / STAKING** | INFLOW · rendimiento | Lending, staking, cashbacks | Sí — casilla 0033 |
| **MINTING** | INFLOW · rendimiento | Creación de token (NFT, LP) | No — coste = colateral + gas |
| **DERIVATIVES PROFIT** | INFLOW · derivados | Ganancia en derivados | Sí — casillas 1612-1640 |
| **WITHDRAWAL** | OUTFLOW · transferencia | Salida hacia cuenta propia | No — traslado interno |
| **EXPENSE_NOT_TAXABLE** | OUTFLOW · transferencia | Gasto irrelevante (quema LP) | **No** — se calcula FIFO pero el resultado se descarta |
| **PURCHASE_FEE** | OUTFLOW · comisiones | Comisión maker/taker | Sí, indirecto |
| **CASH_FLOW_FEE** | OUTFLOW · comisiones | Comisión de retirada | No — no computable |
| **TRANSACTION_FEE** | OUTFLOW · comisiones | Gas / comisión de red | Indirecto |
| **EXPENSE** | OUTFLOW · comisiones | Valor pagado; **se considera venta** | **Sí** — casillas 1802-1809, clave B |
| **DERIVATIVES LOSS** | OUTFLOW · derivados | Pérdida en derivados | Sí — casillas 1612-1640 |
| **LIQUIDATION** | OUTFLOW · derivados | Cierre forzoso | Sí |
| **LOST** | OUTFLOW · especial | Pérdida por error propio | Casilla 0305, con prueba |
| **STOLEN** | OUTFLOW · especial | Robo, hack, estafa | Casilla 0305, con denuncia |
| **DONATE** | OUTFLOW · especial | Donación a un tercero | Sí — a valor de mercado |
| **TRADE** | TRADE | Cambio económico real | **Sí** — casillas 1802-1809 |
| **SWAP** | TRADE | Conversión técnica equivalente | **No** |

## 8.5 Las dos parejas que hay que tener claras

**Pareja 1 — entradas:** `INCOME` y `INCOME_NOT_TAXABLE` hacen lo mismo mecánicamente. Solo difieren en si ese valor se declara como renta. El principal de un préstamo entra igual que un cobro por servicios; lo que cambia es que uno hay que devolverlo.

**Pareja 2 — salidas:** `EXPENSE` y `EXPENSE_NOT_TAXABLE` hacen lo mismo mecánicamente. Solo difieren en si ese resultado llega a los estados financieros. Pagar un servicio con cripto realiza la ganancia; quemar un LP token no.

