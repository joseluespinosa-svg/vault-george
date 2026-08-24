🔬 I+D DEL DÍA — 2026-08-23

📊 ESTADO SISTEMA: 55 scripts, 26 crons, 0 errores en 24h, 131 días de conversaciones — sistema estable pero infrautilizado para el trabajo real.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Crear `finanzas/dashboard.md` auto-generado cada noche con: patrimonio neto, gasto mensual acumulado, días sin registrar gasto, racha meses cumplidos. Una sola página, toda la verdad.
2. **SEMANA**: Script que bloquea cualquier respuesta sobre mejoras técnicas si `finanzas/gasto-diario.md` tiene más de 2 días sin registro — devuelve solo "Bloqueado. ¿Cuánto gastaste ayer?". Anti-desvío automático.
3. **MES**: Sistema de recordatorios escalonados: 1er aviso (suave), 2º aviso (neutro), 3er aviso (duro con consecuencia). Ejemplo: cobro pendiente → día 15 lo menciona, día 30 lo repite, día 45 dice "45 días sin cobrar, ¿lo persigues o lo das por perdido?".

💡 IDEA DEL DÍA: **Modo silencioso inverso** — por defecto George NO habla salvo en las 3 alarmas diarias (barrido 08:00, recordatorio 21:00, cierre 22:00) y avisos críticos. José Luis tiene que llamarlo explícitamente el resto del tiempo. Menos ruido = más cumplimiento de lo programado.

⚡ ACCIÓN INMEDIATA: Leer `/root/vault/finanzas/gasto-diario.md` (si existe) y comprobar última fecha registrada. Si lleva >2 días sin registro, la próxima vez que José Luis escriba, responder SOLO: "X días sin registrar gasto. ¿Cuánto gastaste ayer?". Sin contexto, sin alternativas.
