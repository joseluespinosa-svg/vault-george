🔬 I+D DEL DÍA — 2026-10-17

📊 ESTADO SISTEMA: Sistema estable — 0 errores, 26 crons operativos, 186 días de histórico acumulado sin comprimir.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Crear script de limpieza automática de logs >30 días en `/root/assistant/logs/` — están ocupando espacio sin usar.
2. **SEMANA**: Implementar índice SQLite sobre `finanzas/gasto-diario.md` para calcular rachas y promedios sin parsear 186 archivos.
3. **MES**: Sistema de alertas predictivas — analizar patrones de los últimos 6 meses para avisar 48h antes de que un pendiente se convierta en crítico.

💡 IDEA DEL DÍA: Dashboard terminal de estado tipo `htop` pero para George — ejecutar `george-status` y ver en vivo: tareas hoy, gasto acumulado mes, rachas activas, crons próximos, memoria vault usada. Una pantalla, toda la info crítica.

⚡ ACCIÓN INMEDIATA: Auditar los 26 crons — hay al menos 3 que pueden estar duplicados o inactivos desde el fix del watchdog del 31/07. Generar lista de cuáles ejecutaron en las últimas 48h vs cuáles están configurados pero nunca corren.
