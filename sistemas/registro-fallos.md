# Registro de fallos del sistema

Una línea por fallo. Sin análisis, sin propuestas de arreglo — eso se decide el viernes con datos, no en caliente.

Formato: `FECHA HORA | qué falló | cómo se detectó | qué pasó`

---

2026-07-31 06:46 | Sesión George (pid 31798) perdió conexión MCP telegram tras probar manualmente george_watchdog.sh (creó sesión tmux duplicada "george" con segundo proceso claude escuchando el mismo bot token, conflicto de long-polling) | Detectado por reminder de sistema "MCP server disconnected" tras matar la sesión duplicada | Se mató la sesión duplicada, se relanzó una sesión nueva en tmux "george" (pid 32609) que sí quedó con telegram operativo. La sesión original (31798) queda sin canal telegram pero sigue viva.
