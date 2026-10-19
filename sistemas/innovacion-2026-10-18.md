🔬 I+D DEL DÍA — 2026-10-18

📊 **ESTADO SISTEMA**: Verde. 57 scripts, 9.660 archivos vault, 26 crons, 0 errores 24h. Infraestructura sólida.

🚀 **3 MEJORAS CONCRETAS**:

1. **HOY** — Script `vault_orphan_check.sh`: detectar archivos .md sin enlaces entrantes (huérfanos en el grafo). Ejecuta búsqueda inversa de `[[nombre]]` en todo el vault, reporta los que tienen 0 menciones. Limpia ruido, densifica red.

2. **ESTA SEMANA** — Módulo `finanzas_snapshot.py`: cada viernes a las 19:00, lee SQLite de gastos + `critico.md`, calcula patrimonio neto estimado (San Antonio 420k - hipoteca + ahorros - deudas), lo guarda en `finanzas/snapshots/YYYY-MM-DD.json`. Histórico automático sin preguntar.

3. **ESTE MES** — Dashboard `/root/assistant/web/dashboard.html`: vista única con 4 widgets (tareas hoy, gasto acumulado mes, días desde último dato financiero, crons fallidos últimas 48h). Un `python -m http.server` y lo ve desde el móvil. Menos preguntas, más visibilidad.

💡 **IDEA DEL DÍA**: Sistema de "puntos calientes" en el vault — script que analiza qué archivos .md se modificaron en los últimos 7 días, genera `cerebro/HEAT_MAP.md` con ranking de zonas activas vs zonas muertas. Si un archivo crítico (critico.md, activo.md) lleva >30 días sin tocarse, alerta automática. El vault se autorregula.

⚡ **ACCIÓN INMEDIATA**: Crear `vault_orphan_check.sh` ahora mismo. 15 min, entrega lista de huérfanos hoy.

---

**⚠️ ALERTA ANTI-DESVÍO**: Llevas 55 días sin dato de gasto diario (último: 24/08, 120€ comida). Mejorar a George nunca cuenta como trabajo hecho. ¿Patrimonio neto hoy?
