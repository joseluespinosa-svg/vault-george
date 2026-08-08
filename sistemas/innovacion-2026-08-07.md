🔬 I+D DEL DÍA — 2026-08-07

📊 ESTADO SISTEMA: 57 scripts + 26 crons + 116 días de historial — 0 errores 24h, pero **9 pendientes críticos sin cierre desde julio** (cuello de botella: Ginés sin fecha demanda).

🚀 3 MEJORAS CONCRETAS:
1. **HOY:** Script auto-notificación pendientes parados >7 días → envía por Telegram sin esperar el barrido (evita que José Luis esquive la pregunta)
2. **ESTA SEMANA:** Dashboard financiero txt `/root/vault/finanzas/DASHBOARD.md` autogenerado diario con: gasto últimas 24h, ritmo mes, días sin registrar, racha cumplida — en una pantalla, sin preguntar
3. **ESTE MES:** Sistema anti-bucle para Ginés/ING/tasaciones — cuando José Luis mencione uno de estos 3 temas, George primero lee `critico.md` línea del tema + última conversación donde salió, y si no hay dato nuevo desde entonces, bloquea con "Ya preguntaste eso el día X, sin respuesta. Siguiente acción concreta o lo aparcamos."

💡 IDEA DEL DÍA: **Grafo de bloqueos automático** — cada pendiente crítico declara de qué depende (ej: `tasación SAN ANTONIO ← demanda Ginés`). Cuando José Luis pregunte por algo bloqueado, George detecta la cadena y dice: "Eso está 3 niveles abajo de Ginés. La única acción útil hoy: llamar a Ginés para fecha demanda."

⚡ ACCIÓN INMEDIATA: Crear `/root/assistant/scripts/alertas_pendientes_criticos.sh` que lea `critico.md` + `conversaciones/` últimos 7 días, extraiga pendientes sin actualización desde hace >7 días y envíe 1 mensaje Telegram ahora mismo con los 3 más antiguos (sin esperar barrido manual).
