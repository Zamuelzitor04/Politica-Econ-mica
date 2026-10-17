# Paso 3 – Construcción de la base trimestral (explicación para la sustentación)

Todo lo produce `scripts/construir_base.py` a partir de `data/raw/`. En el Excel cada cifra calculada es
una **fórmula** que se puede seguir hasta el dato original:
- **azul:** dato copiado de la fuente;
- **negro:** fórmula en la misma hoja;
- **verde:** vínculo a otra hoja.

## Paso a paso (con un ejemplo numérico)

| # | Qué se hace | Por qué | Ejemplo |
|---|---|---|---|
| 1 | **TPM mensual** = promedio de la TPM de todos los días del mes (hoja `TPM_diaria` → `Mensual`, col. C) | La tasa cambia a mitad de mes; el promedio diario pondera cuántos días rigió cada nivel | Dic-2022: 11 % del 1 al 18 y 12 % del 19 al 31 → (18×11 + 13×12)/31 = 11,42 % |
| 2 | **TPM y tasa de consumo trimestrales** = promedio de los 3 meses | La guía pide el promedio de las tasas mensuales | 2026-II: TPM = (11,25+11,25+11,25)/3 = 11,25 % |
| 3 | **Saldos del último mes** del trimestre (mar, jun, sep, dic) | Un saldo es una foto a una fecha; sumar meses contaría tres veces la misma deuda | 2026-II usa la cartera de jun-2026 |
| 4 | **Saldo real** = S × IPC(jun-2026) / IPC(mes del saldo) | Quita el efecto de la inflación: todo queda en pesos de jun-2026 | Bruta 2023-I: 213.106,8 × 159,53 / 131,77 = 258.002,1 |
| 5 | **Índice** = 100 × real_t / real(2021-I) | Permite comparar series de tamaños distintos (bruta vs. vencida) | Bruta 2023-I: 100 × 258.002,1 / 240.728,6 = 107,2 |
| 6 | **Morosidad** = 100 × V / B | Proporción de la cartera que está vencida | 2026-II: 100 × 11.187,7 / 224.646,1 = 4,98 % |
| 7 | **Consumo**: el dato del DANE ya está en volumen; solo se rebasa a 2021-I = 100 | Deflactarlo de nuevo quitaría la inflación dos veces | 2026-II: 100 × 200.930,5 / 161.616,3 = 124,3 |
| 8 | **Variación trimestral** = 100 × (C_t / C_t-1 − 1) | Crecimiento frente al trimestre anterior; 2020-IV solo sirve para 2021-I | 2026-II: 100 × (200.930,5 / 199.985,3 − 1) = 0,47 % |

Notas sobre los pasos 4, 6 y 7:
- **Paso 4:** el mes base no cambia el índice 2021-I = 100, porque el IPC base se cancela en el cociente.
- **Paso 6:** da lo mismo con saldos nominales o reales, porque el IPC se cancela.
- **Paso 7:** el DANE lo publica ajustado por estacionalidad y calendario.

## Controles (hoja `Controles`)
- La morosidad propia reproduce el "indicador de calidad tradicional" de la SFC. La diferencia máxima es 0,00005 p.p., y se debe solo al redondeo de la SFC.
- La variación del consumo reproduce la variación trimestral publicada por el DANE. La diferencia es 0.
- La TPM con promedio diario difiere del "Dato mes" del BanRep en máximo 0,15 p.p. (2022-IV).
- No hay datos faltantes en 2021-I a 2026-II. No se interpoló ni imputó nada.

## Preguntas típicas de la sustentación (respuestas con los datos)
- **¿Puede subir la morosidad sin que suba el saldo vencido?** Sí, porque la morosidad es un cociente.
  - De 2023-IV a 2024-I, la vencida nominal casi no cambió (17.183 → 17.199; en términos reales cayó: índice 135,8 → 132,4). Aun así, la morosidad subió de 8,23 % a 8,42 %, porque la cartera bruta se contrajo (el denominador).
- **¿Desaceleración o caída del consumo?**
  - **Caída:** variación trimestral negativa. Ocurrió en 2021-II, 2023-I, 2023-II, 2023-III y 2025-IV.
  - **Desaceleración:** crecimiento positivo pero menor. Por ejemplo, de 1,96 % en 2022-II a 0,52 % en 2022-IV.
  - Mirar las dos cosas: el nivel (panel A) y la variación (panel B).
- **¿Qué no se observa?**
  - El servicio de la deuda por hogar, los ahorros, las refinanciaciones y la distribución por tipo de hogar.
  - La tasa de consumo es la de créditos nuevos, no la que pagan las deudas viejas a tasa fija.
  - La tasa excluye tarjetas de crédito; la cartera de la SFC las incluye.

## Pendientes antes de entregar
- Completar en `Ficha_fuentes` la URL exacta y la fecha de consulta de cada fuente. Los campos están marcados con [ ].
- Citar la definición de vencimiento de la SFC (Circular Básica Contable y Financiera, Cap. II) y confirmar en el portal del BanRep que las tasas están en % efectivo anual.
