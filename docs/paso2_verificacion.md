# Paso 2 – Verificación contra la guía empírica

Ventana: 2021-I a 2026-II (2020-IV solo para la primera variación del consumo). Información publicada hasta el 7-oct-2026.

## 1. Tasa de intervención y tasa de crédito de consumo
| Punto de la guía | Resultado |
|---|---|
| Tasas comparables, % efectivo anual | Las tasas de colocación del BanRep se publican como **promedio mensual en % efectivo anual, ponderado por monto desembolsado**. Fuente: notas metodológicas históricas del BanRep, porque el archivo solo dice "%". Las publicaciones históricas del BanRep también presentan las tasas de intervención en efectivo anual. **Pendiente:** confirmarlo en la ficha de la serie del portal antes de entregar. |
| Cobertura de la tasa de consumo | "No incluye tarjetas de crédito" (hoja Información). Son créditos **nuevos** (desembolsos), no el costo del saldo vivo. Esto importa para el mecanismo: la tasa mide el costo marginal del crédito, no lo que pagan las deudas ya contratadas a tasa fija. |
| Promedio trimestral de tasas mensuales | Tasa de consumo: 69 meses completos (ene-2021–sep-2026), sin vacíos. TPM: promedio diario por mes (2.114 días completos) y luego promedio de 3 meses. |
| Agregación desde datos diarios | La diferencia frente al "Dato mes" es como máximo 0,15 p.p. (2022-IV, por las subidas a mitad de mes); en 17 de 22 trimestres es menor a 0,02 p.p. |

## 2. Cartera bruta y vencida de consumo (SFC, hoja C5)
| Punto | Resultado |
|---|---|
| Saldo del último mes del trimestre | Serie mensual completa: se toman mar, jun, sep y dic. Hay datos de 2020-12 a 2026-08 sin huecos. |
| Igual cobertura institucional | Establecimientos de crédito, **sin IOE** (instituciones oficiales especiales), **incluye leasing**. Bruta y vencida salen de la misma hoja y cobertura. Verificación: la suma de los 4 tipos de C5 = total C4, que declara "no incluye IOE's". |
| Unidad | El título de C5 dice "millones", pero los valores son **miles de millones de pesos**: C5 suma exactamente C4, rotulada "miles de millones" (consumo ago-2026 = 228.796 ≈ $229 billones). La morosidad no se ve afectada porque es un cociente. |
| Vencida vs. riesgosa vs. provisiones | **Vencida** = saldo de créditos en mora (columna CONSUMO-VENCIDA). **Riesgosa** = calificaciones B a E (base del "indicador calidad calificación"). **Provisiones** = columna DETERIORO. Solo se usa la vencida. |
| Definición de vencimiento | El archivo no la trae. La SFC considera cartera vencida los créditos con **más de 30 días de mora** (criterio SARC, ratificado por la SFC en 2017 al crear "mora temprana"). La CE 014/2023, transitoria hasta jul-2024, cambió el umbral de *incumplimiento* (90 días) para provisiones, no el de vencida. **Pendiente:** citar la Circular Básica Contable y Financiera, Cap. II. |
| Control del cálculo | 100 × vencida/bruta reproduce exactamente el "indicador calidad tradicional" de C5 (6,0867 % en mar-2021; 4,9801 % en jun-2026). |
| Notas de la fuente | Fusiones, conversiones y nuevas entidades (Lulo Bank nov-2021, BTG y Bancar dic-2021, Banco Unión jul-2022, Rappipay sin reporte mar-2023). Pueden mover saldos sin reflejar cambios de comportamiento. |

## 3. Consumo final de los hogares (DANE, Cuadro 2)
| Punto | Resultado |
|---|---|
| En volumen | Sí: series encadenadas de volumen, año de referencia 2015, miles de millones de pesos. |
| Ajustada por estacionalidad y calendario | Sí: Cuadro 2 = "Datos ajustados por efecto estacional y calendario". |
| ¿Incluye ISFLSH? | **Sí.** La fila es "Gasto de consumo final individual de los hogares; gasto de consumo final de las ISFLSH" (P.311 + P.313 + P.323). No se pueden separar con este archivo. |
| No es consumo total | Correcto: se usa esa fila, no P.3 "Gasto de consumo final", que incluye al Gobierno (P.312 + P.322). |
| No deflactar de nuevo | Ya es volumen; solo se rebasa a 2021-I = 100. |
| 2020-IV disponible | Sí: 157.576,2. Variación 2021-I propia = 2,5639 %, igual a la publicada por el DANE. |
| Estado de las cifras | 2024 provisional, 2025–2026 preliminares: pueden revisarse. |
| Publicación | Actualizado el 18-ago-2026, antes del corte del 7-oct. |

## 4. IPC nacional
| Punto | Resultado |
|---|---|
| Índice para deflactar | IPC fin de mes, base dic-2018 = 100, 69 meses sin vacíos. Se usa el IPC del mismo mes que el saldo (mar, jun, sep, dic). |
| Inflación del último mes de cada trimestre | Variación anual del IPC de mar, jun, sep y dic. Es idéntica a "Inflación total anual". |
| Fecha de consulta | Los archivos del BanRep se descargaron el 16-oct-2026, después del corte. No afecta: las cifras hasta jun-2026 ya estaban publicadas antes del 7-oct. Los datos de jul a sep-2026 no se usan. |

## Decisión pendiente para el paso 3
- **IPC base fijo.** Al rebasar a 2021-I = 100 el índice real no depende de la base elegida, porque se cancela. La base solo cambia en qué pesos se leen los saldos reales. Propuesta: **pesos de junio de 2026** (IPC = 159,53).
