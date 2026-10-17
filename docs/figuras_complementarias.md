# Figuras complementarias E1–E4 (extensiones opcionales)

Complementan las 4 figuras obligatorias y **no las reemplazan**. Se construyen con los mismos archivos de
`data/raw/`, sin fuentes nuevas. Están en `output/figuras/figuraE*.png` y en la hoja `Complementarias` del
Excel, junto con una tabla de **puntos de giro** calculada con fórmulas. Esa tabla sirve para fechar etapas y rezagos.

## E1. Costo real del crédito y traslado de la tasa
- **Qué es:**
  - Tasa real ex post = 100 × [(1 + i)/(1 + π) − 1], con π = inflación anual del último mes del trimestre.
  - Diferencial = tasa de consumo − TPM, en puntos porcentuales.
- **Qué muestra:**
  - La TPM real fue negativa de 2021-II a 2023-I y es positiva desde 2023-II.
  - La tasa real de consumo pasó de 7,6 % (2022-I) a entre 13,0 % y 15,6 % desde 2023-I, y sigue en 14,4 % en 2026-II, aunque la tasa nominal bajó de 30,2 % a 21,4 %.
  - El diferencial llegó a 17,6 p.p. en 2023-I y se comprimió a entre 9,6 y 10,6 p.p. desde 2024-II.
- **Para qué sirve:** distinguir "tasas altas" en términos nominales de "tasas altas" en términos reales. La caída de la inflación mantuvo alto el costo real del crédito aunque la tasa nominal bajara.
- **Cuidado:** es ex post, porque usa la inflación pasada; los hogares deciden con la inflación esperada.

## E2. Crédito de consumo vs. consumo de los hogares
- **Qué muestra:**
  - Hasta 2022 se mueven juntos.
  - Desde 2023 se separan: la cartera real cae hasta −11,1 % anual (2024-II), mientras el consumo apenas se estanca (−0,7 % anual como mínimo, en 2023-IV).
  - En 2026-II la cartera real está 6,7 % por debajo de 2021-I y el consumo 24,3 % por encima.
- **Para qué sirve:** es un resultado que **limita** la hipótesis, como pide el taller. El consumo agregado no cayó en proporción al crédito, y eso hay que explicarlo. Posibles explicaciones, que deben sostenerse con literatura: ingreso, remesas, ahorro acumulado, otras fuentes de financiamiento, o hogares sin deuda.

## E3. ¿Por qué cambia la morosidad?
- **Qué es:** la variación anual de la morosidad se descompone exactamente en Δln(M) = Δln(V) − Δln(B), en log × 100. Las barras suman exactamente la línea.
- **Qué muestra:**
  - **2022-IV a 2023-IV:** la morosidad sube sobre todo por el **numerador**. El saldo vencido creció entre 38 % y 54 % anual (log × 100).
  - **2023-IV a 2025-I:** la **contracción de la cartera bruta** sumó a la morosidad (barras azules positivas). Ese aporte es pequeño (1,5–5,2 puntos log).
  - **2024-IV a 2025-III:** la baja de la morosidad viene casi toda de la reducción del saldo vencido.
  - **Desde 2025-II:** el crecimiento de la cartera bruta también ayuda a bajarla.
- **Para qué sirve:** responde la pregunta de la sustentación sobre si sube la morosidad sin que suba el saldo vencido. Muestra cuándo pesa el numerador y cuándo el denominador.

## E4. Consumo de los hogares por durabilidad (DANE, Cuadro 4)
- **Qué muestra:**
  - Los bienes **durables** cayeron 14,7 % entre 2022-II y 2023-IV.
  - Los **semidurables** cayeron 18,7 % entre 2022-II y 2023-IV.
  - Los **no durables** (−2,1 %) y los **servicios** (−1,1 %) casi no cayeron.
  - Desde 2024 los durables lideran la recuperación: 148,2 en 2026-II, con 2021-I = 100.
- **Para qué sirve:** el agregado de la Figura 4 esconde un ajuste fuerte en los bienes que más se financian con crédito. Esa relación es una hipótesis a sustentar con literatura.
- **Cuidado:** es el gasto en el territorio económico, sin ISFLSH, un concepto distinto al de la Figura 4. Las series encadenadas no se suman entre sí.

## Decisiones metodológicas de estas figuras (a validar por el grupo)
1. **Tasa real con la fórmula de Fisher exacta**, en lugar de la resta simple i − π. La diferencia es pequeña (~1 p.p. cuando la inflación era 13 %).
2. **Inflación del último mes del trimestre**, para ser consistente con la base. Otra opción es el promedio de los 3 meses.
3. **Crecimientos anuales desde 2022-I.** No se usan datos de 2020 para no salir de la ventana del taller.
