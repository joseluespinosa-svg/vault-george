🔬 **I+D DEL DÍA — 2026-10-05**

📊 **ESTADO SISTEMA:** Saludable técnicamente (24 scripts, 26 crons, 490 archivos, 173 días de historia, 0 errores) pero **coach financiero MUERTO desde hace 41 días** — gasto-diario.md congelado el 25/08.

🚀 **3 MEJORAS CONCRETAS:**

1. **HOY — Reactivar coach financiero:** El mensaje automático de las 21:30 ("¿Cuánto gastaste hoy?") no se está enviando. Sin datos de gasto no hay marca de ahorro, sin marca no hay millón. Script de cierre de día caído o deshabilitado. **Verificar cron + logs del heartbeat.**

2. **SEMANA — Dashboard patrimonio neto:** Crear `finanzas/patrimonio-neto.md` con cálculo automático (valor piso San Antonio ~420k según critico.md + saldos bancarios - deudas). Actualización semanal vía script. El horizonte 30/07/2031 son **1.733 días** — cada día sin medir es un día ciego hacia el millón.

3. **MES — Sistema de cierre automático:** Los datos en critico.md llevan 5 días sin actualizar, parking tiene temas de hace 61 días. Crear `scripts/cierre_semanal.sh` que ejecute el barrido de viernes automáticamente: gasto/categoría, parking (hacer/delegar/matar), rachas, informe del sistema. José Luis solo confirma decisiones, no produce el informe.

💡 **IDEA DEL DÍA:** **Grafo de dependencias financieras** — mapear en Obsidian las relaciones San Antonio → desahucio → Ginés → recuperación → división/mudanza → ahorro 1.000€/mes. Visualizar qué bloquea qué. Un nodo rojo paraliza 4 cosas downstream.

⚡ **ACCIÓN INMEDIATA:** Verificar por qué el mensaje de las 21:30 no se envía desde el 24/08. Revisar:
```bash
grep "21:30" /etc/crontab
grep "gasto" /root/assistant/scripts/*.sh
tail -50 /root/assistant/logs/heartbeat.log
```

Si el cron existe pero no dispara, el problema es silencioso y crítico — **el sistema cree que está midiendo pero no lo está**. 41 días sin métrica = 41 días sin poder cumplir la marca de ahorro.
