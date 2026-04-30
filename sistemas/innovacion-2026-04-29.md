🔬 I+D DEL DÍA — 2026-04-29

📊 ESTADO SISTEMA: Sistema estable (0 errores), 49 scripts activos, 21 crons configurados — operativo al 100%

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Dashboard visual de alertas — script que genere cada mañana un PNG con pendientes críticos del día (gestor, citas, cobros) y lo envíe por Telegram automáticamente a las 08:00
2. **SEMANA**: Detector de ingresos/gastos — parser que lea conversaciones Telegram buscando "cobrado X€" o "pagado X€" y actualice automáticamente /root/vault/cerebro/critico.md sin intervención manual
3. **MES**: Motor de predicción de cash-flow — análisis de los 16 días de conversaciones + patrones de cobro/gasto para alertar cuando el ritmo de gasto supere el de ingresos proyectados

💡 IDEA DEL DÍA: **Modo "José Luis olvidó"** — cron diario que compara alertas de hace 3+ días con conversaciones recientes; si una alerta sigue sin ejecutar y José Luis no la mencionó en 72h, envía recordatorio Telegram automático con contexto completo tipo "Hace 5 días quedó pendiente llamar al gestor — ¿sigue vigente o lo marco resuelto?"

⚡ ACCIÓN INMEDIATA: Crear script `/root/assistant/scripts/dashboard_diario.py` que genere imagen visual con top 3 pendientes urgentes y lo programe en cron para 08:00 cada mañana
