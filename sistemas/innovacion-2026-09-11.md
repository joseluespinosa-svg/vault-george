🔬 I+D DEL DÍA — 2026-09-11

📊 ESTADO SISTEMA: 55 scripts, 433 archivos vault, 26 crons activos, 0 errores 24h — sistema estable, 150 días de conversaciones acumuladas

🚀 3 MEJORAS CONCRETAS:
1. **Script auto-limpieza vault** — detectar notas huérfanas sin enlaces en INDEX.md, archivar automáticamente cada 30 días
2. **Dashboard financiero HTML** — un solo archivo que lea `finanzas/gasto-diario.md` y `finanzas/YYYY-MM.md`, muestre gráfica de gasto diario + racha + proyección mes vs 1.000€
3. **Sistema detección patrones esquiva** — analizar conversaciones últimos 30 días, detectar temas que José Luis menciona pero no cierra 2+ veces, alertar en barrido semanal

💡 IDEA DEL DÍA: **Vault-to-SQLite sincronización automática** — los archivos críticos del vault (finanzas, clientes, tareas) se sincronizan a SQLite cada noche, permitiendo queries rápidas tipo "patrimonio neto evolución últimos 6 meses" o "rachas de ahorro por trimestre" sin leer 150 markdown

⚡ ACCIÓN INMEDIATA: Crear `finanzas/dashboard.html` con gráfica de gasto diario de los últimos 30 días + contador de racha + proyección del mes — una sola pantalla para ver si va a cumplir los 1.000€ sin necesidad de preguntar
