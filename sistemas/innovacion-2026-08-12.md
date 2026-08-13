🔬 I+D DEL DÍA — 2026-08-12

📊 ESTADO SISTEMA: 55 scripts, 369 archivos vault, 26 crons, 0 errores en 24h — Sistema estable, 121 días de historial acumulado.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Script de recordatorio automático de gastos (21:00) que dispare notificación Telegram si no hay registro en `finanzas/gasto-diario.md` — evita que José Luis lo esquive.
2. **SEMANA**: Dashboard automático de patrimonio neto semanal (viernes 19:00) que genere PNG visual y lo envíe por Telegram antes del barrido — el número primero, no el sistema.
3. **MES**: Detector de patrones de evasión: script que analice conversaciones y detecte cuándo José Luis desvía hacia "mejorar herramientas" en vez de hablar de dinero — registra automáticamente en `finanzas/excusas.md`.

💡 IDEA DEL DÍA: Sistema de "puntos de fricción" que lea automáticamente las conversaciones cada noche y extraiga temas mencionados 2+ veces sin cerrarse — genera alerta semanal de "esquives recurrentes" sin que José Luis tenga que pedirlo.

⚡ ACCIÓN INMEDIATA: Crear `/root/assistant/scripts/recordatorio_gastos.sh` que compruebe si existe entrada de hoy en `finanzas/gasto-diario.md` y dispare notificación Telegram a las 21:00 si falta — añadirlo a cron ahora mismo.
