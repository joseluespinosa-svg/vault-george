🔬 **I+D DEL DÍA — 2026-10-20**

📊 **ESTADO SISTEMA:** Infraestructura sólida (0 errores, 55 scripts, 26 crons activos) pero el módulo financiero lleva 57 días muerto desde última entrada.

🚀 **3 MEJORAS CONCRETAS:**

1. **HOY** — Reactivar gasto diario con captura por voz: esta noche a las 21:30 el mensaje no es "¿cuánto gastaste?", es "di solo el número y graba audio 3 segundos" → Whisper transcribe → se guarda automático. Para TDAH, hablar es más fácil que escribir.

2. **ESTA SEMANA** — Detector automático de clientes zombi: script que escanea `/root/vault/proyectos/trabajos/` cada 48h, busca carpetas sin actividad en `activo.md` y genera recordatorio de seguimiento en el mensaje de las 08:00. Aprovecha tu hiperfoco en sistemas para automatizar lo que olvidas.

3. **ESTE MES** — Dashboard financiero que se pinta solo: script Python que lee `gasto-diario.md` + SQLite de tareas + git log del vault → genera un PNG con 4 números (gasto mes / ritmo / ahorro proyectado / patrimonio neto) y lo manda por Telegram cada viernes 19:00. Ver es más fácil que calcular.

💡 **IDEA DEL DÍA:** Sistema de "aparcamiento inteligente" — cuando José Luis está en hiperfoco (>30 min en una tarea no urgente), George detecta el patrón (viendo commits del vault o mensajes largos) y envía automático: "Llevas X min en esto. Pendiente crítico: [el de hoy]. ¿Parking o ahora? P/A". Le da la opción sin romperle el flow.

⚡ **ACCIÓN INMEDIATA:** Preparar el mensaje de las 21:30 de hoy con la nueva mecánica de audio → probar si la captura por voz rompe el bloqueo del gasto diario que lleva 2 meses atascado.
