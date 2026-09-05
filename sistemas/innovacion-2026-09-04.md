🔬 **I+D DEL DÍA — 2026-09-04**

📊 **ESTADO SISTEMA:** Crons activos (26), conversaciones guardadas (143 días), 0 errores críticos excepto heartbeat roto desde 26/08 (401 Unauthorized × 10 días seguidos) + MOD-09 muere por memoria

🚀 **3 MEJORAS CONCRETAS:**
1. **HOY — Arreglar heartbeat Telegram:** Token expirado/revocado desde 26/08. Verificar TELEGRAM_BOT_TOKEN en `/root/.env`, regenerar si es necesario en @BotFather, recargar watchdog. El pulso del sistema lleva 10 días sordo.
2. **SEMANA — Reducir huella MOD-09:** Indexación vectorial muere por RAM (script embeddings). Opciones: batch más pequeño (50→25 archivos), skip de archivos >100KB, o mover a cron nocturno con límite de memoria explícito.
3. **MES — Auto-escalador de plazos:** Cuando un pendiente con fecha (Ginés, Higinio, B2 examen) lleva 3+ días sin cierre, cambiar de recordatorio pasivo a bloqueo activo: "esto o aquello,elige ahora". Sistema de cierre forzado, no de lista de pendientes.

💡 **IDEA DEL DÍA:** Modo "un pendiente, un día" — cuando José Luis esquiva algo 2+ veces, George bloquea cualquier nueva tarea hasta que cierre esa. No más parking infinito: o se hace o se mata, pero no se arrastra. El TDAH necesita carriles únicos, no listas largas.

⚡ **ACCIÓN INMEDIATA:** Verificar token de Telegram del heartbeat — llevas 10 días sin pulso diario, el sistema está medio ciego.
