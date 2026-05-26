🔬 I+D DEL DÍA — 2026-05-25

📊 ESTADO SISTEMA: ✅ 100% operativo — 0 errores, 49 scripts activos, 19 crons funcionando, 42 días de memoria consolidada

🚀 3 MEJORAS CONCRETAS:
1. **HOY** → Automatizar alertas pre-evento: script que envíe recordatorio Telegram 24h antes de citas críticas (Junta Arbitral 03/06, Examen B2 29/05, Psicología 09/06)
2. **ESTA SEMANA** → Sistema de seguimiento subastas: cron que monitorice alertasubastas.com + eActivos y envíe resumen diario Telegram con oportunidades <150k€ en Ibiza
3. **ESTE MES** → Dashboard financiero en Obsidian: vista dinámica de ingresos/gastos/pendientes que se actualice desde tareas.db + facturas + conversaciones (evitar que José Luis pregunte "¿cuánto llevo gastado?")

💡 IDEA DEL DÍA: **MAIA-Local** → Fork de MAIA que procese documentos locales (contratos, facturas, notas simples) con OCR Tesseract y los indexe en el vault automáticamente. José Luis acaba de recibir nota simple.pdf — podría extraerse automáticamente y guardarse en /vault/propiedades/cas-serres/

⚡ ACCIÓN INMEDIATA: Crear script `/root/assistant/scripts/alerta_pre_evento.py` que lea alertas.md y envíe recordatorio Telegram 24h antes de cada cita (primer recordatorio: Examen B2, dentro de 4 días)
