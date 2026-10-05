🔬 I+D DEL DÍÍ — 2026-10-04

📊 ESTADO SISTEMA: 55 scripts, 26 crons, 0 errores 24h — sistema estable pero infrautilizado (173 días de datos sin exprimir)

🚀 3 MEJORAS CONCRETAS:
1. **Hoy**: Script que detecte patrones de gasto por día de semana (173 días dan muestra) — te dice qué días te pasas del presupuesto antes de que pase
2. **Esta semana**: Dashboard texto plano que calcule distancia real al 1M€ por mes (patrimonio actual → ritmo ahorro → fecha llegada vs 30/07/2031) — número duro cada viernes
3. **Este mes**: Integrar SQLite tareas.db con finanzas — cerrar tarea de <10min que suma dinero = notificación priorizada; tarea sin dinero = al final de la cola

💡 IDEA DEL DÍA: Los 485 archivos vault + 173 días conversaciones = entrenar modelo local que prediga tu próxima excusa para no ahorrar (basado en `finanzas/excusas.md`) y te la cite ANTES de que la uses

⚡ ACCIÓN INMEDIATA: Analizar `finanzas/gasto-diario.md` últimos 30 días y sacar el patrón de qué día de semana gastas más — dato para el mensaje del viernes
