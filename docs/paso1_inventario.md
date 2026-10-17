# Paso 1 – Inventario de archivos (aprobado)

Clasificación: **(a)** sirve para el taller · **(b)** extensión opcional o control · **(c)** no sirve.

## `Datos_Adicionales_BANREP.xlsx` (diario, 01/01/2021–15/10/2026, 22 series)
| Serie | Clasificación | Motivo |
|---|---|---|
| Tasa de política monetaria, dato diario | (a) | Base del promedio mensual elegido (decisión 1) |
| TPM "Dato mes", fin de mes, fin de trimestre/semestre/año, semanal | (b) | Control: comparación con el promedio diario |
| Crédito de consumo, tasa de interés, promedio mensual (69 meses) | (a) | Tasa de consumo; **excluye tarjetas de crédito** |
| Crédito de consumo, tasa semanal | (b) | Control de la agregación |
| TIB diaria | (b) | Extensión de transmisión |
| Cartera comercial; tasas comerciales, microcrédito, productivo | (c) | No son crédito de consumo |

## `Datos_BANREP_2.xlsx` (mensual, ene-2021–sep-2026, 21 series)
| Serie | Clasificación | Motivo |
|---|---|---|
| IPC índice fin de mes (base dic-2018 = 100) | (a) | Deflactor |
| IPC variación anual = Inflación total anual | (a) | Inflación (columnas idénticas) |
| Consumo final real / nominal | (c) / (b) contraste | Es consumo **total** (hogares + Gobierno); coincide con el DANE Cuadro 2, fila P.3 |
| PIB, crecimiento PIB, desempleo, crédito doméstico, meta de inflación | (b) | Contexto |

## `Cartera_hasta_agosto_Superfinanciera.xlsx` (cifras al 25-sep-2026)
| Hoja | Clasificación | Motivo |
|---|---|---|
| C5 – cartera por tipo de crédito, mensual ene-2016–ago-2026 | (a) | Consumo: bruta, vencida, deterioro, indicadores |
| C4 – total establecimientos de crédito (sin IOE), mensual | (b) | Control de cobertura (C5 suma exactamente C4) |
| C2, C3, C6 – cortes por tipo de entidad / entidad / calificación | (c) | Un solo mes, sin serie de consumo |
| C1 – solo una imagen | (c) | Sin datos |

## `anex-GastoConstantes-IItrim2026.xlsx` (DANE, actualizado 18-ago-2026)
| Cuadro | Clasificación | Motivo |
|---|---|---|
| Cuadro 2 – volumen, ajustado por estacionalidad y calendario | (a) | Fila "Gasto de consumo final individual de los hogares; gasto de consumo final de las ISFLSH" |
| Cuadro 4 – hogares por finalidad y durabilidad, ajustado | (b) | Extensión "consumo por durabilidad" |
| Cuadros 1, 3, 5, 7 (datos originales); 6, 8 | (c) | Sin ajuste estacional, u otros componentes |

## `anex-ProduccionCorriente-IItrim2026.xlsx`
(c). Es el PIB por el enfoque de la **producción** a precios **corrientes**. El taller pide el enfoque del gasto en volumen.

## Decisiones del estudiante
1. TPM mensual = promedio de la serie diaria de cada mes; trimestre = promedio de esos 3 meses.
2. La tasa de consumo excluye tarjetas y la cartera SFC las incluye. Se documenta como limitación y se prioriza la SFC para crédito y morosidad.
3. Consumo de los hogares: DANE, Cuadro 2 del anexo de gasto en volumen.
4. Trabajo en el repositorio, sin modificar `data/raw/`.
