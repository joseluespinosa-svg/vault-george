🔬 I+D DEL DÍA — 2026-09-06

📊 ESTADO SISTEMA: Infraestructura sana (0 errores, 55 scripts, 26 crons activos) pero **usuario desconectado** — 13 días sin gasto diario, barrido de hoy sin respuesta, patrimonio neto sin actualizar.

🚀 3 MEJORAS CONCRETAS:

1. **HOY:** Script captura automática SMS banco → extrae importe/comercio de notificaciones de compra, escribe directo a `gasto-diario.md` sin preguntar. Elimina la pregunta de las 21:30.

2. **SEMANA:** Dashboard web local en `/root/assistant/web/` — 3 números grandes (patrimonio neto, ahorro mes actual, días sin dato), actualizable desde Telegram con comando `/estado`. Visualizar el problema en vez de pedirlo.

3. **MES:** Integrar Tesseract (ya está en MAIA) para OCR de tickets — foto de ticket por Telegram → extrae comercio+importe → confirma con A/B → registra. Convertir fricción (escribir número) en un tap (foto).

💡 IDEA DEL DÍA: **Modo "sin datos = sin asistente"** — si lleva >7 días sin actualizar patrimonio neto o >3 días sin gasto diario, George responde a TODO con "Primero el patrimonio neto. Después hablamos de [lo que sea que preguntó]". Bloqueo proactivo anti-desvío.

⚡ ACCIÓN INMEDIATA: Leer `/root/vault/cerebro/alertas.md` y enviar mensaje Telegram con los 2 pendientes más urgentes de hoy (Higinio/AENA vencido ayer + Ginés fecha demanda comprometida hace 5 días) en formato A/B: "¿Cuál cerramos primero: A) Higinio B) Ginés?"
