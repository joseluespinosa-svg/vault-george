# Estrategia a medio plazo — ¿piso en Ibiza, Alicante, o edificio completo?
_Abierto: 2026-07-21_

## Planteamiento de José Luis
De aquí a unos años, ¿qué compensa más?
1. Comprar un piso en Ibiza (para vivir o alquilar)
2. Seguir invirtiendo en Alicante (ya hay precedente: piso Carolinas Altas ~40k mirado en julio 2026)
3. Comprar un edificio entero (varias unidades) en vez de un piso suelto — más control, más unidades de alquiler, economía de escala en gestión

## Contexto relacionado
- Búsqueda activa de vivienda principal ya en curso en Ibiza (Can Misses, Figueretes) — ver [[../busqueda-vivienda/INDEX|proyecto búsqueda vivienda]]
- Estructura financiera actual: rehipoteca ING 230k + nueva hipoteca ~130k = 360k disponibles — ver [[../busqueda-vivienda/estructura-financiera|estructura financiera]]
- Plan a 10 años ya existe — ver [[GEORGE_DIRECTRICES_PLAN_10_ANOS|directrices plan 10 años]]

## Pendiente de desarrollar
- Definir si esto es una operación adicional (aparte de la compra de vivienda principal) o alternativa a ella
- Comparar rentabilidad: 1 piso Ibiza vs 1 piso Alicante vs edificio completo (nº unidades, coste por unidad, gestión)
- Ver qué financiación quedaría libre después de la operación de vivienda principal (recordar: se reserva 100k líquido para 2ª operación con Karina)

## Modelo financiero (24/07/2026)
Archivo: `ALICANTE_MODELO_2026-07-24.xlsx` (mismo directorio) — 6 pestañas con fórmulas vivas: Inputs, Rehipoteca, Capacidad de deuda, Comparativa 3 escenarios (200k/275k/350k), Cronograma de caja 36 meses, Estrés.

**Conclusión del cálculo base (nóminas: José Luis 2.200€ + Karina 1.600€, techo DSTI 35%):**
- Cuota nueva San Antonio tras ampliar a 230k (supuesto 25 años/3,5%, plazo/tipo reales pendientes de confirmar con ING): ~1.151€/mes (antes 360€).
- Margen que queda del techo de endeudamiento (1.330€) para una hipoteca nueva: solo ~179€/mes → capital hipotecable adicional ~34.700€. Insuficiente para cualquiera de los 3 escenarios usando solo nóminas.
- Liquidez neta de la rehipoteca tras cancelar hipoteca actual y gastos: ~165.810€. No cubre los fondos propios necesarios en ningún escenario (faltan entre ~79k y ~157k según el escenario).
- **Los 3 escenarios salen "NO financiables" con este cálculo — pero el cálculo usa solo nóminas.** Los bancos suelen contar parte de la renta futura del edificio en el DSTI para hipotecas de inversión: esto es lo primero que hay que verificar con el banco antes de descartar la operación.
- Además, estos 230k ya están comprometidos en el plan de compra de vivienda principal (230k+130k=360k) — hay que decidir prioridad entre ambos proyectos.

## Revisión v2 (24/07/2026) — correcciones de José Luis + escenarios D/E/F
José Luis revisó el Excel y pidió correcciones. Mismo archivo `ALICANTE_MODELO_2026-07-24.xlsx`, ahora 10 pestañas (0_Resumen...9_Sensibilidad).

**Hallazgo más importante (nuevo):** con el supuesto de LTV 80% para vivienda habitual, **ni siquiera a 350.000€ de tasación llega la ampliación a 230.000€** (máximo real ~220.000€). La incoherencia que señaló José Luis (350k vs 200k manejados en otras conversaciones) es aún más crítica de lo que parecía — el propio modelo, en su mejor caso, no llega al importe solicitado. Posibles explicaciones: ING usa un LTV mayor (85-90%) por ser cliente, o valora el inmueble por encima de 350k, o el criterio no es LTV puro. Pendiente confirmar con ING.

**Escenario D (150k, al contado):** la cuota (solo San Antonio, sin hipoteca nueva) SÍ entra en el techo de endeudamiento, pero la liquidez de la rehipoteca (165.810€) no cubre los fondos propios necesarios (~305.500€, sobre todo por la reforma) — faltan ~140.000€.

**Escenario E (flip — comprar/reformar/vender):** ROI anualizado 20,7% (A) / 32,1% (B) / 51,3% (C) — muy superior a la rentabilidad de alquilar (3,4-4,5% neto). Es el hallazgo más relevante de toda la revisión: vender tras reformar bate claramente a alquilar en este modelo. Sigue sujeto a la misma limitación de financiación/liquidez que A/B/C.

**% de renta que el banco tendría que contar en el DSTI para que cada escenario sea financiable:** A 56,5% / B 67,5% / C 68,3%. Es la pregunta concreta que llevar al banco.

**Rentabilidad neta vs tipo libre de riesgo (3%):** solo el Escenario C (4,45%) lo bate con margen; A (3,45%) y B (3,80%) apenas.
