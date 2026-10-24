# Archivos originales (no modificar)

Copiados tal cual los subió el estudiante (se quitó solo el prefijo aleatorio del nombre de carga).
Permisos de solo lectura. La huella SHA-256 permite comprobar que no cambiaron.

| Archivo | Fuente | Contenido principal |
|---|---|---|
| `Datos_Adicionales_BANREP.xlsx` | BanRep (portal de estadísticas), descargado 16-oct-2026 | TPM (mensual, diaria…), tasas de crédito por modalidad |
| `Datos_BANREP_2.xlsx` | BanRep con datos del DANE, descargado 16-oct-2026 | IPC, inflación, consumo final, PIB, desempleo |
| `Cartera_hasta_agosto_Superfinanciera.xlsx` | SFC, cifras reportadas al 25-sep-2026 | Cartera bruta, vencida, deterioro por tipo de crédito |
| `anex-GastoConstantes-IItrim2026.xlsx` | DANE, PIB_T enfoque del gasto, volumen; actualizado 18-ago-2026 | Gasto de consumo final de los hogares (Cuadro 2) |
| `anex-ProduccionCorriente-IItrim2026.xlsx` | DANE, PIB_T enfoque de la producción, precios corrientes | No se usa |
| `base_de_datos_taller_2_monitor.xlsx` | Base enviada por el monitor (Alejandro Ríos), 22-oct-2026 | TPM diaria, tasa de consumo, cartera vencida (millones $), consumo hogares, IPC, inflación. Sin cartera bruta. Se usa para cotejo: coincide al 100 % |

Huellas completas en `SHA256SUMS`. Comprobación: `cd data/raw && sha256sum -c SHA256SUMS`
