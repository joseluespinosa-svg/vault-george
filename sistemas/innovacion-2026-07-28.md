🔬 I+D DEL DÍA — 2026-07-28

📊 ESTADO SISTEMA: ✅ Operativo al 100% — 122 scripts, 1.4GB vault (326 MD), 23 crons, 0 errores 24h, conversaciones desde abril activas

🚀 3 MEJORAS CONCRETAS:
1. **[HOY]** Dashboard financiero automático: script que calcule en tiempo real ingresos fijos (2.200€) + trabajos clima + gastos fijos + pendientes de cobro = estado de caja mensual. Actualización diaria 8:00.
2. **[ESTA SEMANA]** Alertas inteligentes de impago: monitorizar fecha 5 de cada mes para alquiler C/ del Far (Laura/Susan) + cualquier otro ingreso recurrente. Si día 10 no hay confirmación de pago → notificación Telegram automática.
3. **[ESTE MES]** Sistema de facturación provisional: mientras José Luis no se da de alta (rechaza autónomo, primo ya no disponible) → crear registro privado de trabajos extra con cliente/importe/fecha/estado, exportable a Excel para cuando encuentre vía de facturación legal.

💡 IDEA DEL DÍA: **Perfil de riesgo financiero automático** — George analiza cada domingo: ratio ingresos fijos/variables, días sin nuevo trabajo, cobros pendientes >30 días, tendencia gastos. Genera un "semáforo" 🟢🟡🔴 que José Luis ve sin tener que preguntar. Si 🔴 dos semanas seguidas → activa modo "búsqueda agresiva" de trabajos.

⚡ ACCIÓN INMEDIATA: Crear script `/root/assistant/scripts/finanzas_dashboard.sh` que lea vault/cerebro/critico.md + conversaciones últimos 30 días, extraiga todos los importes (regex `\d+[,.]?\d*€`) y genere resumen JSON con: ingresos_mes_actual, gastos_mes_actual, pendiente_cobro, saldo_estimado. Ejecutar y guardar en `/root/assistant/data/finanzas_snapshot_$(date +%Y-%m-%d).json`.
