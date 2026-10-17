# Taller 2 – Política Económica (Univalle, 2026-2)
**Crédito, consumo y morosidad en Colombia**

Estructura:

| Carpeta | Contenido |
|---|---|
| `docs/` | Enunciado del taller (PDF) y notas de trabajo por etapa |
| `data/raw/` | Archivos originales descargados (BanRep, SFC, DANE). **No se modifican** (solo lectura) |
| `data/processed/` | Bases construidas a partir de `data/raw/` (etapa 3) |
| `scripts/` | Código que construye la base y las figuras (etapa 3) |
| `output/` | Excel final y figuras (etapa 3) |

Etapas: 1) inventario → 2) verificación contra la guía → 3) construcción de la base.
Ver `docs/paso1_inventario.md` y `docs/paso2_verificacion.md`.

## Cómo reproducir la base (paso 3)

```bash
pip install -r requirements.txt
python scripts/construir_base.py
```

Produce `output/Taller2_base_trimestral.xlsx` (base con fórmulas, ficha de fuentes, figuras y controles),
`output/figuras/*.png` y `data/processed/*.csv`. Explicación de cada cálculo: `docs/paso3_construccion.md`.
