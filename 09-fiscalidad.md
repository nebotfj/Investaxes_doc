---
description: El fundamento jurídico de cada tratamiento, con artículos y consultas vinculantes.
icon: scale-balanced
---

# Fiscalidad: cómo tributa cada operación y por qué

Este capítulo explica el fundamento de cada tratamiento. No es teoría: es lo que permite defender tu declaración si te la revisan.

## 9.0 De dónde viene cada criptoactivo

La calificación fiscal depende de **cómo adquiriste** el activo:

- **Compraventa** — un contratante entrega una cosa determinada y el otro paga un precio cierto (art. 1445 del Código Civil)
- **Permuta** — cada contratante se obliga a dar una cosa para recibir otra (art. 1538 CC)

Y además: ingresos por prestación de servicios, prueba de trabajo (*Proof of Work*), prueba de participación (*Proof of Stake*, distinguiendo entre delegación y masternodo), donaciones, repartos gratuitos (*airdrops*), intereses recibidos y cashbacks.

Del resultado de las operaciones de transmisión se obtiene una renta gravada en el IRPF para quienes cumplan los criterios de residencia (arts. 6 a 9 y 72 LIRPF), durante el año natural (art. 12 LIRPF).

**La calificación, valoración, compensación e integración** de esas rentas —generales o del ahorro (art. 44 LIRPF)— depende de la forma en que se hayan adquirido. Al margen de la actividad económica, estaremos ante **rendimientos del capital mobiliario** o ante **ganancias y pérdidas patrimoniales**.

---

## 9.1 Ganancias patrimoniales derivadas de transmisión

**Qué son.** Las variaciones en el valor del patrimonio que se pongan de manifiesto con ocasión de cualquier alteración en su composición, salvo que se califiquen como rendimientos (art. 33 LIRPF).

**Cuándo se imputan.** Al período impositivo en que tenga lugar la alteración patrimonial (art. 14.1.c LIRPF). No cuando cobras: cuando transmites.

**Cómo se calculan.** Diferencia entre los valores de adquisición y de transmisión (art. 34 LIRPF).

**Qué incluye cada valor (art. 35 LIRPF):**

```
Valor de adquisición = importe real de la adquisición
                     + coste de las inversiones y los gastos y tributos
                       inherentes a la adquisición (excluidos los intereses)

Valor de transmisión = importe real por el que se efectuó la enajenación
```

### Las comisiones: cuáles computan y cuáles no

La Dirección General de Tributos, en contestación a consulta de **11 de junio de 2018**, establece que las comisiones de compra y venta que cobran los exchanges, *"si los citados gastos se originan por la realización de dichas operaciones, guardando, por tanto, relación directa con las mismas y son satisfechos por el consultante, serán computables para determinar los respectivos valores de adquisición y de transmisión"*.

De ahí se desprende lo contrario para el resto:

| Tipo de comisión | ¿Computa? | Movimiento en Investaxes |
|---|---|---|
| Comisión de compra o venta en exchange | **Sí** | `PURCHASE_FEE` |
| Comisión de depósito o retiro | **No** | `CASH_FLOW_FEE` |
| Comisión de transferencia entre carteras | **No** | `CASH_FLOW_FEE` |

Esta es la razón por la que Investaxes separa `PURCHASE_FEE` de `CASH_FLOW_FEE`: es la diferencia entre un importe que reduce tu ganancia y uno que no.

### Las permutas tienen su propia regla de valoración

Para las permutas entre criptoactivos, el art. 37.1.h LIRPF establece que la ganancia o pérdida se determina por la diferencia entre el valor de adquisición del bien que se cede y **el mayor** de:

- el valor de mercado del bien o derecho **entregado**
- el valor de mercado del bien o derecho **que se recibe a cambio**

No es "el valor de lo que recibes" sin más: es el mayor de los dos. En mercados líquidos suelen coincidir, pero en tokens poco negociados la diferencia puede ser relevante.

### FIFO y la homogeneidad entre exchanges

La DGT razona que los criptoactivos *"computables por unidades o fracciones de unidades, tienen su origen en un mismo protocolo específico y poseen todos ellos las mismas características, siendo iguales entre sí"*, lo que les confiere **naturaleza de bienes homogéneos**.

Cuando existen bienes homogéneos, el art. 37.2 LIRPF determina que **los transmitidos son los adquiridos en primer lugar** — el método FIFO.

Y el punto decisivo: *"el hecho de que los bitcoin se adquieran y transmitan en diferentes casas de cambio o exchanges no constituye una circunstancia que altere la homogeneidad"*. Por tanto, **habrán de tenerse en cuenta todos los adquiridos, sin distinguir en función de las diferentes casas de cambio**.

Esto es lo que hace que no puedas declarar exchange por exchange. Tu FIFO es uno solo, global.

**Integración.** Renta del ahorro (art. 46.b LIRPF), compensada e integrada en la base imponible del ahorro (art. 49 LIRPF).

---

## 9.2 Rendimientos del capital mobiliario

**Qué son.** Según el art. 25.2 LIRPF, *"las contraprestaciones de todo tipo, cualquiera que sea su denominación o naturaleza, dinerarias o en especie, como los intereses y cualquier otra forma de retribución pactada como remuneración por tal cesión"*.

**Qué entra aquí:**

- **Staking por delegación (Proof of Stake).** Delegar criptoactivos supone aumentar el poder de participación para validar bloques y obtener las recompensas que se reparten por ello
- **Intereses recibidos** de lending y cuentas remuneradas
- **Cashbacks.** Recompensa por usar una tarjeta que devuelve un porcentaje del capital gastado a cambio de cumplir requisitos, habitualmente bloquear una cantidad de criptoactivo para acceder a distintos niveles de ventajas. Cada cashback **se anota como rendimiento del capital mobiliario con el valor en euros que tenga en el momento de la recepción**

**Integración.** Renta del ahorro (art. 46.a LIRPF), compensada e integrada en la base imponible del ahorro (art. 49 LIRPF). Casilla **0033**.

> **El doble papel del FMV, en términos jurídicos.** La diferencia entre el valor de adquisición de estos rendimientos —el valor en euros con el que los anotaste al recibirlos— y su posterior valor de transmisión constituye una **ganancia o pérdida patrimonial**. Por eso el FMV de recepción tiene que estar bien: fija dos cosas a la vez.

---

## 9.3 Ganancias patrimoniales que NO derivan de transmisión

Aquí está el tratamiento de los **airdrops**.

Un airdrop —reparto gratuito de activos— consiste en una alteración en el valor del patrimonio. Se computa como ganancia patrimonial **el valor de mercado en el momento de su recepción, valorado en euros**, al tratarse de incorporaciones que no derivan de una transmisión (art. 37.1.l LIRPF).

**Integración.** Forma parte de la **renta general** y se integra en la base imponible general (arts. 45 y 48 LIRPF). Casilla **0304**.

Es una diferencia importante respecto al staking: aunque ambos sean "cripto que te llega sin comprarla", el staking es rendimiento del capital mobiliario (base del ahorro) y el airdrop es ganancia no derivada de transmisión (base general). Tributan en escalas distintas.

---

## 9.4 Pérdidas patrimoniales que NO derivan de transmisión

Aquí están los **hackeos, robos y estafas**, incluidos los esquemas Ponzi.

**El criterio es restrictivo.** La DGT, en contestación a consulta de **25 de junio de 2015**, señala que *"el importe de un crédito no devuelto a su vencimiento no constituye de forma automática una pérdida patrimonial, al mantener el acreedor su derecho de crédito, y sólo cuando ese derecho de crédito resulte judicialmente incobrable será cuando produzca sus efectos"*.

Que te hayan estafado no basta: hace falta que el crédito resulte **judicialmente incobrable**.

**Cuándo se puede imputar.** El art. 14.2.k LIRPF permite imputar las pérdidas derivadas de créditos vencidos y no cobrados al período en que *"se cumpla el plazo de un año desde el inicio del procedimiento judicial distinto de los de concurso que tenga por objeto la ejecución del crédito sin que este haya sido satisfecho"*.

**Si luego cobras.** Se imputa una ganancia patrimonial por el importe cobrado en el período en que se produzca el cobro.

**Integración.** Renta general (arts. 45 y 48 LIRPF). Casilla **0305**.

> **Aviso práctico.** Para incluir estas pérdidas necesitas **denuncia presentada o sentencia judicial firme**. Sin ese soporte, la AEAT no permite la deducción.

---

## 9.5 Rendimientos por actividad económica: la minería

Minar requiere equipos ASIC o tarjetas GPU, lo que supone una inversión elevada.

**Para personas físicas.** Se consideran rendimientos de actividades económicas, dado que proceden del trabajo personal y del capital conjuntamente —o de uno solo de estos factores— suponiendo la ordenación por cuenta propia de medios de producción y de recursos humanos, con la finalidad de intervenir en la producción o distribución de bienes o servicios (art. 27 LIRPF).

**Cómo se determina.** Según las normas del Impuesto sobre Sociedades, con carácter general por **estimación directa** (arts. 28 y 30 LIRPF).

**Para personas jurídicas.** Definición equivalente en el art. 5 LIS. La base imponible se calcula corrigiendo el resultado contable determinado conforme al Código de Comercio (art. 10 LIS).

**Cuándo se registran los criptoactivos recibidos.** Al período en que se produzca su **devengo**, con arreglo a la normativa contable, **con independencia de la fecha de su pago o cobro** (art. 11 LIS; art. 14.1.b LIRPF).

**Integración.** Renta general (arts. 45 y 48 LIRPF).

---

## 9.6 Impuesto sobre el Patrimonio

El hecho imponible está constituido por la titularidad, en el momento del devengo, del conjunto de bienes y derechos de contenido económico atribuibles al sujeto pasivo, con deducción de cargas, gravámenes y deudas (arts. 1 y 3 de la Ley 19/1991).

Según las contestaciones a consulta de **1 de febrero de 2018** y **3 de agosto de 2018**, los criptoactivos *"habrán de declararse junto con el resto de los bienes de titularidad de la persona física, de la misma forma que se haría con un capital en divisas, valorándose en el impuesto a precio de mercado a la fecha del devengo, es decir, a 31 de diciembre de cada año"* (art. 24 de la Ley 19/1991).

**Es un impuesto cedido** a las Comunidades Autónomas (art. 2 LIP). De ahí que los umbrales y bonificaciones varíen tanto según dónde residas.

---

## 9.7 Modelo 721: criptoactivos en el extranjero

**Quiénes están obligados** (art. 42 quater del RGAT, aprobado por Real Decreto 1065/2007): personas físicas y jurídicas residentes en territorio español, establecimientos permanentes en dicho territorio de no residentes, y entidades del art. 35.4 LGT, que a 31 de diciembre sean:

- **titulares** de monedas virtuales en el extranjero, o
- **beneficiarios, autorizados** o de alguna otra forma ostenten **poder de disposición**, o
- **titulares reales**

cuando esas monedas estén **custodiadas por personas o entidades que proporcionan servicios para salvaguardar claves criptográficas privadas en nombre de terceros**.

**También obliga a quienes lo fueron durante el año.** Si tuviste esa condición en cualquier momento del año y la perdiste a 31 de diciembre, informas igualmente, con los datos a la fecha en que se produjo la extinción.

**Qué es un "titular real".** Quien tenga esa consideración conforme al art. 4.2 de la Ley 10/2010 de prevención del blanqueo de capitales.

### Los dos requisitos que determinan la obligación

Deben concurrir **ambos**:

1. Que las monedas sean **custodiadas por personas o entidades que presten servicios de salvaguarda de claves criptográficas privadas en nombre de terceros**
2. Que esas personas o entidades **no sean residentes en España** ni establecimientos permanentes en territorio español

### Hot wallet o cold wallet da igual

Existe la idea extendida de que la obligación depende de si el monedero está conectado a internet. **No es así.**

Los monederos se distinguen en dos ejes independientes: **custodios frente a no custodios** (según si la custodia de los criptoactivos o sus claves la mantiene un tercero o el propio usuario) y **hot frente a cold** (según si están conectados a internet). En la práctica los *cold wallets* suelen funcionar como no custodios, pero lo que decide es el primer eje.

**Por tanto:** con independencia de si es hot o cold wallet, las monedas virtuales que mantengas en monederos **cuyas claves privadas controlas tú** **no se computan en los saldos ni se informan** en el Modelo 721.

Lo que determina la obligación es **quién custodia las claves**, no dónde está el monedero.

### Casos particulares

| Situación | ¿Obligación? |
|---|---|
| **Domiciliados en País Vasco y Navarra** | Sí, con arreglo a la normativa estatal o foral a la que estén sometidos |
| **Herencias yacentes** | Sí, en la medida en que son entidades del art. 35.4 LGT |
| **Herederos y legatarios** | Sí, desde que exista aceptación tácita o expresa de la herencia |

