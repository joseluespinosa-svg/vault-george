🔬 I+D DEL DÍA — 2026-08-25

📊 ESTADO SISTEMA: Sistema estable, 0 errores, pero 397 archivos en vault y 133 días de logs pesan — toca limpieza.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Script auto-extractor de gasto diario del vault → tabla SQLite para que coach financiero calcule sin leer 133 archivos cada vez
2. **ESTA SEMANA**: Dashboard de 3 líneas en el barrido diario: ahorro del mes / días sin registrar gasto / racha cumplida (sin que José Luis tenga que preguntar)
3. **ESTE MES**: Archivo auto-rotación vault — conversaciones >90 días a `/vault/archivo/YYYY/` para que el INDEX cargue rápido

💡 IDEA DEL DÍA: Detector de excusas repetidas — si en `finanzas/excusas.md` aparece 3 veces la misma frase (ej. "este mes ha sido raro"), George lo menciona sin juzgar: "Eso ya lo dijiste en junio y julio, ¿qué cambiamos?"

⚡ ACCIÓN INMEDIATA: Crear `finanzas/gastos-base.md` y script `registrar_gasto_diario.sh` para que José Luis pueda anotar el gasto de ayer en 10 segundos por Telegram sin abrir el vault.
