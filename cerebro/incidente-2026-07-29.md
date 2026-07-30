# Incidente — Canal Telegram roto y reiniciado — 29/07/2026

## Qué pasó
Sobre las 07:22-07:23 del 29/07/2026, George (yo) probó a mano el script `barrido_interactivo.sh` (parte del "orden de trabajo" que pidió José Luis para automatizar los barridos por cron). Ese script lanza un `claude -p` (proceso headless nuevo) que arranca SU PROPIO servidor MCP de Telegram — y Telegram solo permite una conexión de long-polling activa por bot, así que el proceso nuevo echó a la conexión de la sesión principal (la que habla con José Luis). El servidor de Telegram de la sesión principal se cayó y no se reconectó solo.

## Qué se hizo
1. Se revirtió el crontab al estado anterior (briefing_proactivo.sh 8h, checkin_nocturno.sh 21h) — el intento de automatización nueva NO se dejó activo, no pasó la prueba.
2. Se mató el proceso bun huérfano del test.
3. Como la sesión principal no recuperó la conexión de Telegram sola, se reinició la sesión con `/root/start_george.sh` (el mecanismo normal de reinicio, el mismo `tmux kill-session -t george && tmux new-session...`).

## Si estás leyendo esto (nueva sesión, 29/07/2026 o después)
Dile a José Luis, en cuanto puedas (por Telegram, chat_id 6801069092):
- Que el canal se cayó por una prueba tuya (headless invocando su propio servidor de Telegram, chocó con la conexión principal), no por nada que él hiciera.
- Que ya está arreglado (reinicio de sesión).
- Que los scripts nuevos (`barrido_interactivo.sh`, `cierre_interactivo.sh`, `semanal_interactivo.sh`) quedaron guardados en `/root/assistant/scripts/` pero SIN activar en cron — necesitan otra vía (probablemente inyectar el prompt en la sesión viva vía `tmux send-keys` en vez de lanzar un `claude -p` nuevo, para no volver a chocar con la conexión de Telegram y para no depender de crédito de API aparte).
- Sigue pendiente responder sus 2 preguntas abiertas de antes del incidente: (1) si quiere el tono duro del CLAUDE.md que mandó o mantener el estilo actual, (2) si el objetivo del patrimonio es 5 años en firme o el rango de 10 (5-7 rápido) que ya teníamos.
- Retomar el "orden de trabajo" (punto 1: cron interactivo) con la vía de tmux send-keys en vez de claude -p headless.

## Ver también
- [[../proyectos/plan-financiero-2026/plan-1M-10anos|Plan 1M€]]
- CLAUDE.md — pendiente decidir si se sustituye por el propuesto por José Luis o se mantiene el actual con las piezas ya integradas
