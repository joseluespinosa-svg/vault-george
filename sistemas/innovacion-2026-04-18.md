🔬 I+D DEL DÍA — 2026-04-18

📊 ESTADO SISTEMA: 46 scripts activos, 19 crons, 0 errores 24h — salud óptima ✅

🚀 3 MEJORAS CONCRETAS:
1. **Hoy**: Script auto-cobro post-trabajo → alerta si pasan 30min tras finalizar sin registrar ingreso (evitar olvidar los 700€ de Sacha)
2. **Esta semana**: Dashboard visual /root/vault/dashboard.md con métricas clave (ingresos mes, gastos, trabajos pendientes, alertas activas) — generación automática cada mañana
3. **Este mes**: Sistema predictivo de gastos → analizar patrones últimos 3 meses y alertar cuando gasto semanal supere media + 20% antes del viernes

💡 IDEA DEL DÍA: **Modo "Pre-Trabajo"** — Al detectar trabajo próximo (24h antes), George genera checklist automática: material confirmado, ruta óptima, clima, contacto cliente verificado, recordatorio cobro. Todo en 1 mensaje Telegram.

⚡ ACCIÓN INMEDIATA: Crear script `/root/assistant/scripts/alerta_cobro_pendiente.sh` que se active cuando José Luis envíe "trabajo terminado" por Telegram → cuenta 30min y alerta si no hay registro de cobro.
