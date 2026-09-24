---
description: Registro, acceso y los parámetros que condicionan cómo se calculan todos tus informes.
icon: right-to-bracket
---

# Primeros pasos: registro y configuración inicial

## Registro y acceso

1. Entra en **https://investaxes.com/** y pulsa **Dashboard**
2. Si aún no tienes cuenta, regístrate con tu correo electrónico y crea tu contraseña
3. Para entrar al sistema: **https://app.investaxes.com/sign-in**

<figure><img src=".gitbook/assets/investaxes/INVESTAXES_image (9).png" alt="Inicio de sesión en Investaxes"><figcaption></figcaption></figure>

## Formulario inicial

La primera vez que uses la plataforma tendrás que completar un formulario que permite establecer una prioridad sobre los exchanges más importantes para ti. Esto orienta el orden en que se trabajan las integraciones.

## Configuración crítica antes de importar nada

Hay parámetros que condicionan **cómo se calculan todos los informes**. Revísalos antes de cargar el primer archivo, no después:

| Parámetro | Valor correcto | Por qué importa |
|---|---|---|
| **País de residencia fiscal** | España | Determina qué reglas se aplican. Un país incorrecto genera informes con normativa equivocada, y el error no salta a la vista |
| **Moneda base** | EUR | Todas las valoraciones y el informe final deben expresarse en euros |
| **Método de coste** | FIFO | Es el exigido por la AEAT |
| **Año fiscal** | 1 enero – 31 diciembre | El ejercicio fiscal español es el año natural |
| **Zona horaria** | La tuya | Una transacción de las 23:50 del 31 de diciembre puede caer en un ejercicio u otro según la zona horaria |

> El error de configuración más caro es el país. Si los informes se generan con reglas de otra jurisdicción, los números pueden parecer razonables y estar sistemáticamente mal.

