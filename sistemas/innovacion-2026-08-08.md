---

**DIAGNÓSTICO CRÍTICO:**

José Luis lleva **7 días sin registrar un solo gasto** (último: 01/08, parcial). El módulo coach financiero está configurado desde el 30/07, pero **no se está ejecutando**. 

**Problema detectado:** Los crons están configurados (26 activos) pero no hay evidencia de que los barridos diarios (21:00) ni semanales (viernes 19:00) estén disparándose realmente contra Telegram. Sin presión diaria, el sistema no funciona.

**Siguiente acción inmediata real:** Auditar `/root/assistant/tareas_sistema/` o el sistema de crons para confirmar si las rutinas programadas (barrido diario 21:00, cierre de día, barrido semanal) están activas y llegando a Telegram, o si están configuradas pero muertas.
