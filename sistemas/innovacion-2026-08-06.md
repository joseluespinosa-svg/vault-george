🔬 I+D DEL DÍA — 2026-08-06

📊 ESTADO SISTEMA: Saludable — 24 scripts activos, 353 docs vault, 26 crons, 0 errores 24h, 115 días de conversaciones guardadas. Un solo fallo registrado desde julio (watchdog duplicado, resuelto).

🚀 3 MEJORAS CONCRETAS:

1. **HOY**: Crear `/root/vault/sistemas/metricas-diarias.md` con contador automático de preguntas esquivadas por José Luis — se detectan en conversaciones pero no se miden. Patrón confirmado (ING 4 veces, gastos-base 5 veces) pero sin número objetivo ni umbral. Script que cuente líneas "Es la segunda/tercera vez" en conversaciones últimos 7 días → guardar métrica, avisar si >5 en una semana.

2. **ESTA SEMANA**: Automatizar validación de datos críticos antes de aceptar un "pendiente cerrado". Ejemplo real: José Luis dice "Ginés, 24-25" → George acepta sin mes, sin por escrito, sin acta. Fallo de QA del sistema. Crear checklist en `acciones.md` que bloquee marcado-como-hecho si faltan campos obligatorios (fecha, documento, importe confirmado).

3. **ESTE MES**: Sistema de cierre automático de bucles de 72h (regla anti-compra-impulso). Ahora George lo apunta en el vault pero depende de que lo recuerde. Crear tabla SQLite con campos: `item | fecha_inicio | fecha_vencimiento | estado | accion_cierre`. Cron diario que busca vencidos y genera el recordatorio automático o cierra directamente si José Luis no contestó (ejemplo: barca → cerrada por George tras vencer).

💡 IDEA DEL DÍA: **Sistema de "deuda de contexto"** — métrica nueva para medir el coste real de cada pendiente no cerrado. Cada día que un pendiente sigue abierto, George lo repregunta o lo salta → eso consume tokens, tiempo, atención. Crear contador de "tokens gastados por no cerrar X" para enseñarle a José Luis el coste real de esquivar (ejemplo: "ING llevaba 5 días abierto, 4 mensajes repetidos, ~8.000 tokens gastados — contestarlo el día 1 hubiera costado 0"). Gamificación inversa: mostrar la factura invisible de la indecisión.

⚡ ACCIÓN INMEDIATA: Crear el contador de preguntas esquivadas ahora mismo — es la mejora #1, implementable en 10 minutos, y el barrido semanal de mañana viernes necesita ese número para el "Informe semanal del sistema" (temas que José Luis esquivó 2+ veces).
