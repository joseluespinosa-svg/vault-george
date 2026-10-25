🔬 **I+D DEL DÍA — 2026-10-24**

📊 **ESTADO SISTEMA:** 532 archivos, 1.4GB vault, 26 crons activos, 24 días octubre registrados — PERO módulo financiero muerto desde hace 2 meses y sistema de mensajes fijos roto (0/2 crons críticos activos).

🚀 **3 MEJORAS CONCRETAS:**

1. **HOY** — Restaurar crons desaparecidos de 08:00 (tarea del día) y 21:30 (gasto diario). Están en CLAUDE.md 2.1 pero no en crontab desde hace semanas. Causa probable del 0/7 mensajes semana pasada.

2. **ESTA SEMANA** — Arreglar watchdog loop: el 22/10 relanzó 182 veces por documento sin respuesta. Añadir timeout de abandono (3 intentos máx) + log de documentos perdidos para recovery manual.

3. **ESTE MES** — Reactivar módulo coach financiero: gasto-diario.md lleva desde 24/08 sin dato nuevo (61 días muerto). Script nocturno debe forzar pregunta aunque no haya respuesta al anterior (regla 2.1: "asumir estimado al 2º día sin dato").

💡 **IDEA DEL DÍA:** Sistema de "salud de módulos" en vault — un dashboard automático que marca rojo/verde cada módulo según última actividad (>7 días sin uso = rojo). Genera métrica semanal: % módulos vivos vs zombies. Permite matar formalmente lo que no funciona en vez de dejarlo pudrir.

⚡ **ACCIÓN INMEDIATA:** Revisar crontab completo ahora mismo y comparar contra módulos declarados activos en CLAUDE.md — restaurar los 2 crons fijos antes de que termine el día.
