🔬 I+D DEL DÍA — 2026-08-05

📊 ESTADO SISTEMA: ✅ Infraestructura sana (57 scripts, 26 crons, 0 errores 24h) pero **José Luis lleva 9 pendientes abiertos sin cerrar, 4 veces sin dar los 5 gastos base — el coach financiero NO ha arrancado nunca**.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Script `detector_esquivas.sh` que cuenta cuántas veces José Luis no contesta cada pregunta del barrido diario → genera métrica "esquivas/tema" en el vault y la enseña al 3er día.
2. **SEMANA**: Módulo `cierre_forzado.py` — a las 21:00, si hay pendientes de 7+ días, bloquea el barrido del día siguiente hasta que cierre UNO (no todos, solo uno) de la lista. Sin excepción.
3. **MES**: Dashboard `/vault/panel.html` generado cada viernes: patrimonio neto vs horizonte 1M€ (30/07/2031), gráfico de ahorro mensual, lista de esquivas del mes, top 3 gastos no planificados — una sola pantalla, sin login, para Karina también.

💡 IDEA DEL DÍA: **Pacto de datos con Karina** — ella ve el panel financiero en tiempo real (ahorro, gastos mes, patrimonio) si José Luis registra todo antes de las 21:00 cada día. Si no registra 2 días seguidos, el panel se apaga automáticamente hasta que se ponga al día. Incentivo externo sin depender de la voluntad de José Luis.

⚡ ACCIÓN INMEDIATA: Crear `detector_esquivas.sh` ahora — 15 minutos de inversión, se ejecuta en cada barrido, escribe a `/root/vault/sistemas/metricas-esquivas.md` con fecha/tema/contador, y George lo lee antes de enviar el mensaje diario.
