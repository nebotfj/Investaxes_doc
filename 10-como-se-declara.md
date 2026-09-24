---
description: El mapa de cada operación a su casilla concreta.
icon: file-invoice
---

# Cómo se declara: Modelo 100, Patrimonio y Modelo 721

## 10.1 El cuadro de resultado financiero

El informe abre con un cuadro que resume los rendimientos globales y estima el impuesto:

**PARTE GENERAL**

| Concepto | Qué recoge |
|---|---|
| Ganancias que no derivan de una transmisión | Total del bloque siguiente |
| — Ingresos generales (Airdrops) | `AIRDROP / GIFT`, `INCOME` |
| — Actividad Económica (Minería) | `MINING` |
| Pérdidas no derivadas de transmisión | Total del bloque siguiente |
| — Robo | `STOLEN` |
| — Pérdida | `LOST` |
| **TOTAL** | Base general |
| **IMPUESTO** | Estimación |

**PARTE DEL AHORRO**

| Concepto | Qué recoge |
|---|---|
| Rendimientos de capital mobiliario | Total del bloque siguiente |
| — Intereses | `INTEREST` |
| — Staking | `STAKING` |
| Ganancias y pérdidas derivados de transmisión | Total del bloque siguiente |
| — Ganancias y pérdidas de capital | `TRADE`, `EXPENSE`, `DONATE` |
| — Ganancias por derivados | `DERIVATIVES PROFIT` |
| — Pérdidas por derivados | `DERIVATIVES LOSS`, `LIQUIDATION` |
| — Compensado | Importe efectivamente compensado en el ejercicio |
| — Pérdidas pendientes de aplicar | Saldo negativo que se arrastra |
| **TOTAL** | Base del ahorro |
| **IMPUESTO** | Estimación |
| **RETENCIONES PRACTICADAS** | Retenciones soportadas |

> **Sobre el impuesto estimado.** Se calcula estimando un **30 % para la parte general** y aplicando **los tramos correspondientes al año para la parte del ahorro**. Es orientativo: el importe real depende del resto de tus rentas y de tu comunidad autónoma.

Fíjate en **Compensado** y **Pérdidas pendientes de aplicar**: si tienes pérdidas que no han podido compensarse este ejercicio, ahí aparece el saldo que puedes arrastrar. Anótalo de un año para otro.

---

## 10.2 Rendimientos del capital mobiliario → casilla 0033

**Apartado B del Modelo 100.**

| Concepto | Casilla |
|---|---|
| Otros rendimientos de capital mobiliario a integrar | **33** |

Aquí va la suma de tus `INTEREST`, `STAKING` y cashbacks, valorados al FMV de recepción. El informe detalla el desglose por activo.

---

## 10.3 Ganancias y pérdidas que NO derivan de transmisión → casillas 0304 y 0305

**Apartado F.1 del Modelo 100.**

| Concepto | Casilla |
|---|---|
| Importe ganancias | **304** |
| Importe pérdidas | **305** |

**Qué va en la 304:** airdrops, *rewards*, ingresos de *play2earn*, premios recibidos.

**Qué va en la 305:** robos y hackeos sufridos.

> **Aviso.** Si incluyes pérdidas deducibles por robo o hackeo, **deberás tener denuncia presentada o sentencia judicial firme**. En caso contrario la AEAT no te permitirá deducirlas. Revisa también los criterios de imputación temporal de 9.4.

La minería se declara en el **apartado D (Actividades económicas)**, no aquí.

---

## 10.4 Transmisión de monedas virtuales → casillas 1802 a 1809

**Apartado F.2 del Modelo 100**, bloque *derivadas de la transmisión o permuta de monedas virtuales por particulares*.

Se rellena **una ficha por cada elemento patrimonial** —cada combinación de moneda transmitida y clave de contraprestación:

| Campo | Casilla |
|---|---|
| Denominación de la moneda virtual que se transmite | **1802** |
| Identificación de lo recibido a cambio. Clave tipo contraprestación | **1803** |
| Valor de transmisión | **1804** |
| Valor de adquisición | **1806** |
| Pérdida patrimonial obtenida `[1804] - [1806]` | **1807** |
| Ganancia patrimonial obtenida `[1804] - [1806]` | **1809** |

### Las claves de contraprestación (casilla 1803)

| Clave | Categoría | Qué operación es | Movimiento en Investaxes |
|---|---|---|---|
| **N** | CRYPTO → OTRA MONEDA VIRTUAL | Permuta entre criptoactivos | `TRADE` cripto-cripto |
| **B** | CRYPTO → BIENES O SERVICIOS | Pago de un bien o servicio con cripto | `EXPENSE` |

Que exista una clave específica para "bienes o servicios" confirma que **pagar con criptomonedas es una transmisión declarable**, con su propio código en el modelo.

### Ejemplo real de cómo lo presenta el informe

| Activo | Categoría | Letra | Coste | Ingreso | Resultado |
|---|---|---|---|---|---|
| SOL | CRYPTO → OTRA MONEDA VIRTUAL | N | 1.080,39 € | 1.092,02 € | 11,62 € |
| USDC | CRYPTO → OTRA MONEDA VIRTUAL | N | 734,81 € | 702,85 € | −31,96 € |
| PEPE | CRYPTO → OTRA MONEDA VIRTUAL | N | 652,98 € | 333,23 € | −319,74 € |
| BTC | CRYPTO → BIENES O SERVICIOS | B | 243,25 € | 121,63 € | −121,63 € |
| ETH | CRYPTO → BIENES O SERVICIOS | B | 14,40 € | 7,20 € | −7,20 € |

El mismo activo puede aparecer dos veces con letras distintas: el BTC permutado va con clave N y el BTC con el que pagaste algo va con clave B. Son elementos patrimoniales separados.

### El límite de 25 criptoactivos

Para inversores con **más de 25 criptoactivos intercambiados** en un año natural, el informe detalla los de mayor volumen y **agrupa el resto en un último elemento patrimonial denominado "otros"**, por cada categoría, hasta un total de 13.

---

## 10.5 Futuros y NFTs → casillas 1612 a 1640

**Apartado F.2, bloque de transmisiones de otros elementos patrimoniales.**

| Campo | Casilla |
|---|---|
| Contribuyente del elemento patrimonial transmitido | **1624** |
| Tipo de elemento. Clave | **1626** |
| Tipo de operación: transmisión intervivos onerosa | **1612** |
| Fecha de transmisión (día/mes/año) | **1631** |
| Fecha de adquisición (día/mes/año) | **1632** |
| Valor de transmisión | **1633** |
| Valor de adquisición | **1637** |
| Pérdida patrimonial obtenida `[1633] - [1637]` | **1638** |
| Ganancia patrimonial obtenida `[1633] - [1637]` | **1640** |

A diferencia de las monedas virtuales, aquí **sí se piden fechas**. Para la operativa de futuros a lo largo del año, el informe consolida el resultado del ejercicio con fecha de adquisición 1 de enero y de transmisión 31 de diciembre.

---

## 10.6 Impuesto sobre el Patrimonio (Modelo 714) → apartado Q

**1. Bienes y derechos. Q. Saldos en monedas virtuales.**

| Columna | Contenido |
|---|---|
| Clave % titularidad | `P-100` si eres titular al 100 % |
| Denominación tipo de moneda virtual | BTC, ETH, SOL… |
| Nº de unidades | Saldo a 31 de diciembre |
| Valor (euros) | Valoración a precio de mercado a 31 de diciembre |

Se declara **todo el saldo**, con independencia de dónde esté custodiado. Es un criterio distinto al del Modelo 721: aquí cuenta lo que tienes, no quién lo custodia.

---

## 10.7 Modelo 721

| Columna | Contenido |
|---|---|
| Siglas moneda | BTC, ETH, USDC… |
| Nº de monedas virtuales | Saldo a 31 de diciembre |
| Valor moneda virtual (€) | Cotización unitaria |
| Saldo moneda virtual | Valor total de la posición |
| Origen | Plataforma donde está custodiada |

La columna **Origen** es la clave: identifica el custodio. Recuerda los dos requisitos de 9.7. Las posiciones en monederos cuyas claves controlas tú no entran en este modelo.

---

## 10.8 Tabla maestra: de la operación a la casilla

| Lo que hiciste | Movimiento | Base | Casilla |
|---|---|---|---|
| Vendiste cripto por euros | `TRADE` | Ahorro | 1802-1809 |
| Permutaste una cripto por otra | `TRADE` | Ahorro | 1802-1809, clave **N** |
| Pagaste un bien o servicio con cripto | `EXPENSE` | Ahorro | 1802-1809, clave **B** |
| Donaste cripto | `DONATE` | Ahorro | 1802-1809 |
| Recibiste recompensas de staking | `STAKING` | Ahorro | **0033** |
| Recibiste intereses o cashbacks | `INTEREST` | Ahorro | **0033** |
| Cerraste un futuro con ganancia | `DERIVATIVES PROFIT` | Ahorro | 1612-1640 |
| Cerraste un futuro con pérdida | `DERIVATIVES LOSS` | Ahorro | 1612-1640 |
| Te liquidaron una posición | `LIQUIDATION` | Ahorro | 1612-1640 |
| Recibiste un airdrop | `AIRDROP / GIFT` | General | **0304** |
| Recibiste un premio o ingreso play2earn | `INCOME` | General | **0304** |
| Minaste | `MINING` | General | Apartado D |
| Te robaron o hackearon | `STOLEN` | General | **0305** (con denuncia) |
| Perdiste el acceso a tus fondos | `LOST` | General | **0305** (con prueba) |
| Moviste fondos entre cuentas tuyas | `DEPOSIT` / `WITHDRAWAL` | — | Ninguna |
| Envolviste un token (ETH→WETH) | `SWAP` | — | Ninguna |
| Recibiste el principal de un préstamo | `INCOME_NOT_TAXABLE` | — | Ninguna |
| Quemaste un LP token | `EXPENSE_NOT_TAXABLE` | — | Ninguna |
| Acuñaste un NFT o LP token | `MINTING` | — | Ninguna |
| Tenías saldo a 31/12 | — | — | Modelo 714 apartado Q y/o Modelo 721 |

