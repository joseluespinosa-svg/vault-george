🔬 I+D DEL DÍA — 2026-10-15

📊 ESTADO SISTEMA: Infraestructura robusta (55 scripts, 26 crons, 0 errores) pero subusada — medio año de histórico sin explotación analítica.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Script `vault_salud.sh` que detecte archivos huérfanos (sin enlaces desde INDEX.md) y los marque para revisión — el vault crece (513 archivos) pero sin curación se vuelve ruido.
2. **SEMANA**: Dashboard SQLite `finanzas_vista.db` que una gastos diarios + patrimonio + marca 1.000€/mes — ahora están dispersos en MD, consultar es fricción, y José Luis no consulta lo que cuesta ver.
3. **MES**: Sistema de "anclas temporales" — cada domingo, foto automática del patrimonio neto + top 3 gastos + racha ahorro, guardada como PNG en Drive con enlace permanente — para que Karina y José Luis vean la película sin rebuscar en 184 días de logs.

💡 IDEA DEL DÍA: Convertir el barrido semanal en un diff visual (antes/después en columnas) en vez de lista de texto — el cerebro TDAH procesa cambios más rápido que estados absolutos, y reduce la resistencia a abrir el reporte.

⚡ ACCIÓN INMEDIATA: Revisar `/root/vault/finanzas/gasto-diario.md` — si hay huecos >2 días en la última semana, rellenarlos con media histórica marcada como `[est]` y notificar a José Luis la racha real vs estimada, porque sin datos completos el programa financiero sigue en falso arranque.
