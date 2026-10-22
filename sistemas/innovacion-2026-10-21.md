🔬 I+D DEL DÍA — 2026-10-21

📊 ESTADO SISTEMA: Sistema estable (0 errores/24h), 190 días de data acumulada, infraestructura madura (55 scripts, 26 crons) — listos para fase analítica.

🚀 3 MEJORAS CONCRETAS:
1. **Script analizador de patrones**: procesar las 190 conversaciones para extraer los 5 bloqueos más frecuentes de José Luis (excusas en finanzas, tareas que arrastra 3+ días, temas que esquiva). Output: JSON con patrones + frecuencia. Ejecutar hoy.

2. **Auto-tracking gasto diario**: integrar el mensaje 21:30 con OCR de tickets (foto del ticket → extrae importe → propone anotarlo). Reduce fricción para mantener la racha. Base: el OCR de MAIA ya funciona. Implementar esta semana.

3. **Dashboard patrimonio neto**: página HTML estática en `/root/vault/dashboard.html` que carga desde SQLite y muestra: patrimonio actual, proyección lineal a 30/07/2031, brecha vs 1M€, ritmo de ahorro últimos 3 meses. Actualización diaria vía cron. Listo en 30 días.

💡 IDEA DEL DÍA: **"Modo avión" para José Luis** — cuando detectes que lleva 3+ mensajes desviándose o proponiendo mejoras a George en vez de trabajar, activar automáticamente un bloqueo de 2 horas donde George solo responde a: gastos, cobros, y la tarea de HOY. Sin opciones, sin I+D, sin "mejorar el sistema". Se levanta solo o él lo cancela.

⚡ ACCIÓN INMEDIATA: Crear `/root/assistant/scripts/analizar_patrones.py` que procese `/root/vault/conversaciones/*.md` y extraiga las 5 frases/excusas que más se repiten cuando José Luis no cierra una tarea financiera. Ejecutarlo y guardar resultado en `sistemas/patrones-bloqueo.md`.
