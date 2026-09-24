---
description: Cómo se genera, qué contiene cada bloque y en qué orden conviene revisarlo.
icon: file-lines
---

# El informe fiscal: estructura y lectura

## Cómo se genera

1. Ve a la sección **Transacciones** en el menú lateral
2. Pulsa **Generar Reporte** (botón azul, esquina superior izquierda)
3. Se abre el modal **Generar informe**
4. Selecciona el **año fiscal** (solo aparecen años con transacciones registradas)
5. Confirma y espera al procesamiento

> **Importante:** al generar un informe se incluyen **todas las transacciones desde el inicio de tu historial** hasta el final del período seleccionado. El sistema necesita el histórico completo para calcular los costes de adquisición por FIFO. Después filtra los resultados por el ejercicio solicitado.

## Los cinco bloques del informe

| Bloque | Contenido |
|---|---|
| **1. Resultado financiero de tus operaciones** | Resultados agregados objeto de gravamen y **notas y conciliaciones** |
| **2. IRPF (Modelo 100)** | Casillas para operaciones derivadas de la transmisión de criptoactivos como elemento patrimonial |
| **3. Impuesto sobre el Patrimonio y Modelo 721** | Saldos a 31 de diciembre y declaración informativa de monedas virtuales en el extranjero |
| **4. Obligaciones fiscales y criterios** | Comentarios sobre obligaciones existentes, metodología de cálculo y referencias a las consultas vinculantes de la AEAT |
| **5. Historial completo de operaciones** | Trazabilidad de todos los movimientos realizados durante el año natural |

Dentro del bloque 1 encontrarás, además del cuadro de resultado financiero (10.1), el desglose de ganancias y pérdidas patrimoniales por activo y categoría, los rendimientos de capital mobiliario por activo y la parte general.

## En qué orden revisarlo

**No empieces por el resultado. Empieza por los problemas.**

| Orden | Qué miras | Qué buscas |
|---|---|---|
| 1.º | **Notas y conciliaciones** | Alertas de venta vacía. Si hay alguna, todo lo demás está construido sobre datos incompletos |
| 2.º | **Ganancias y pérdidas patrimoniales** | Que las operaciones grandes cuadren. Valores de adquisición sospechosamente bajos |
| 3.º | **Rendimientos de capital mobiliario** | Que esté todo el staking, los intereses y los cashbacks |
| 4.º | **Parte general** | Minería, airdrops, robos y pérdidas |
| 5.º | **Patrimonio y Modelo 721** | Solo si te aplican |
| 6.º | **Resultado financiero** | Ahora sí: el resumen, una vez validado lo anterior |

## La alerta de venta vacía

Si todo está correcto, el informe dice literalmente:

> *"Este informe se ha generado correctamente y no contiene ninguna alerta de venta vacía."*

Esa frase es tu luz verde. Si en su lugar aparece un listado de alertas, no presentes nada: ve a 12.2.

## Columnas del historial de operaciones

| Columna | Significado |
|---|---|
| Exchange | Cuenta o red de origen |
| Fecha | Fecha y hora exacta |
| Operación | Tipo de movimiento |
| Entradas: Activo / Cantidad / Valor | Lo que entra y su valoración en euros |
| Salidas: Activo / Cantidad / Valor | Lo que sale y su valoración en euros |

## Sobre la elaboración del informe

El informe se elabora aplicando los métodos establecidos por la AEAT, utilizando como elementos de valoración **las consultas vinculantes, la legislación vigente y una interpretación razonable de la normativa tributaria**. Está elaborado en colaboración con **ECIJA TECH | Crypto**, firma especialista en legislación y tributación sobre criptoactivos, a la que puedes escribir a `crypto@ecija.com`.

> La información del informe no sustituye a servicios contables, fiscales, de auditoría o de asesoramiento profesional.

## Preguntas frecuentes sobre el informe

**"Muestra ganancias y no sé de dónde salen."**
Cada adquisición registra un coste. Cada venta se empareja con la compra más antigua no consumida (FIFO). Si el número te sorprende, revisa primero si hay ventas vacías o costes a cero.

**"El informe incluye transacciones de años anteriores."**
Es correcto y necesario: el sistema analiza desde tu primera transacción para calcular bien los costes.

**"He corregido errores pero el informe sigue igual."**
Los informes son fotografías de un momento. Tras cualquier corrección hay que **generar uno nuevo**.

**"Aparece una línea 'otros' en las ganancias."**
Normal si intercambiaste más de 25 criptoactivos en el año (ver 10.4).

## Qué conservar

- El informe anual en PDF
- Los archivos originales exportados de cada exchange
- Las capturas de pantalla de cualquier movimiento introducido manualmente
- La denuncia o sentencia, si has declarado pérdidas por robo
- La declaración presentada
- El registro de tus direcciones públicas de blockchain

