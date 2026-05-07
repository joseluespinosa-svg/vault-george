# MAIA — Conceptos y decisiones de diseño

## Workflow (definición José Luis, 2026-05-06)

Secuencia A→B→C→D→E→F por cada intervención técnica:
A) Técnico llega → abre orden asignada en MAIA
B) Sigue checklist según tipo (correctivo/preventivo/conductivo/aviso)
C) Introduce lecturas (presiones, temperaturas)
D) IA analiza → propone diagnóstico con explicación paso a paso
E) Técnico valida o corrige → feedback entrena la IA
F) Cierra orden → MAIA programa automáticamente el siguiente preventivo

## Principios IA

- IA PROPONE, técnico VALIDA (nunca actúa sola en decisiones técnicas)
- Control sesgos: muestra nivel de confianza %, datos usados, opción "incorrecto"
- Explicabilidad: no solo el resultado, también el razonamiento
- Aprendizaje continuo: cada corrección mejora el modelo
- Colaboración humano-IA: IA como copiloto, no como sustituto

## Próximas funciones a construir

1. Checklist guiado por tipo de intervención
2. Pantalla diagnóstico IA dentro de la orden
3. Sistema validación + feedback del técnico
4. Historial de aprendizaje por equipo
