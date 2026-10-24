# Cotejo con la base del monitor (22-oct-2026)

Archivo: `data/raw/base_de_datos_taller_2_monitor.xlsx`, original sin modificar. El cotejo se repite solo cada vez que
se corre `python scripts/construir_base.py`; el resultado está en la hoja `Cotejo_monitor` del Excel.

## Resultado: las cifras son las mismas

| Serie | Base del monitor | Nuestra base | Diferencia máxima |
|---|---|---|---|
| TPM diaria | 2.007 días, 01/01/2021–30/06/2026 | Misma fuente (BanRep) | 0 |
| Tasa de consumo sin tarjetas | 66 meses, % | Misma | 0 |
| Cartera vencida de consumo | 66 meses, **millones** de COP corrientes | **Miles de millones** (SFC C5) | 0, tras dividir la del monitor entre 1.000 |
| IPC (dic-2018 = 100) | 66 meses | Mismo | 0 |
| Inflación anual | 66 meses | Misma | 0 |
| Consumo de los hogares | 23 trimestres (2020-IV a 2026-II), ref. 2015 | Mismo (DANE, Cuadro 2) | 0 |

Diferencias de forma, que no cambian ningún número:
- El monitor fecha el IPC y la inflación el día 1 de cada mes; nosotros por mes calendario.
- El monitor marca el estado de cada cifra de consumo: definitivo hasta 2023, provisional en 2024, preliminar en 2025–2026. Coincide con las marcas p y pr del DANE.

**Lo que falta en la base del monitor: la cartera bruta de consumo.** Sin ella no se puede calcular la morosidad (100 × V/B) ni la Figura 2. La tomamos de la misma hoja de la SFC (C5) de donde sale su cartera vencida. Su vencida coincide exactamente con la nuestra, así que la cobertura es la misma: establecimientos de crédito sin IOE, incluye leasing. Conviene confirmarlo con el monitor.

## Advertencia 1: pesos corrientes ≠ poder adquisitivo
Ya estaba resuelto: real = S × IPC(jun-2026) / IPC(mes del saldo). Ejemplo de 2021-I a 2026-II (hoja `Unidades`):

| Concepto | Cambio |
|---|---|
| Cartera bruta en pesos corrientes | +39,0 % |
| Nivel de precios (IPC) | +48,9 % |
| **Cartera bruta real** | **−6,7 %** |
| Cartera vencida en pesos corrientes | +13,7 % |
| **Cartera vencida real** | **−23,6 %** |

En palabras: los bancos tienen más pesos prestados que en 2021, pero esos pesos compran menos. En poder adquisitivo, la cartera es más pequeña.

## Advertencia 2: unidades y años de referencia distintos
- **Cartera.** El monitor la da en millones y la SFC en miles de millones. Se divide entre 1.000 y se trabaja en una sola unidad.
- **Consumo de los hogares.** Está en volumen con "pesos de referencia 2015". Esos pesos no son los mismos que los pesos de junio de 2026 de la cartera real, así que **no se comparan niveles en pesos** entre consumo y cartera. Se comparan **índices 2021-I = 100** o **tasas de crecimiento**, que no tienen unidades.
- **IPC.** La base dic-2018 = 100 no importa: se usa como cociente entre dos meses y la base se cancela.
- **Tasas.** TPM y tasa de consumo están en la misma unidad (% efectivo anual nominal). Para compararlas con la inflación se usa la tasa real (Figura E1).

La tabla completa, serie por serie, está en la hoja `Unidades` del Excel.
