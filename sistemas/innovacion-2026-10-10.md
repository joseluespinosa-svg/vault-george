🔬 I+D DEL DÍA — 2026-10-10

📊 ESTADO SISTEMA: Salud técnica óptima (0 errores/24h), pero infraestructura hinchada: 55 scripts + 26 crons = riesgo de cascada silenciosa.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Dashboard financiero en vault (`finanzas/PANEL.md`) con 3 números actualizados diario: patrimonio neto / ahorro mes actual / días seguidos con gasto registrado. Un vistazo = estado completo, sin buscar.
2. **SEMANA**: Auditoría de crons duplicados/zombies — 26 es demasiado. Consolidar los que hacen lo mismo, matar los que no aportan. Objetivo: <15 crons, documentar cada uno en `sistemas/crons-activos.md`.
3. **MES**: Sistema de alertas financieras automáticas (si gasto diario >150€ dos días seguidos, o si ahorro mensual <500€ a día 20) → mensaje Telegram sin esperar barrido semanal.

💡 IDEA DEL DÍA: **Patrón de desvío como métrica**: registrar automáticamente cada vez que José Luis pide mejoras técnicas en vez de trabajar finanzas/tareas → en 30 días, el patrón se vuelve visible y accionable (¿cuándo pasa? ¿qué lo dispara?). No para reprocharlo, para cortocircuitarlo antes.

⚡ ACCIÓN INMEDIATA: Leer `/root/vault/finanzas/gasto-diario.md` y verificar si hay registro de los últimos 7 días — si falta dato, aplicar regla de asumir promedio histórico y seguir (no preguntar una tercera vez).

---

**Pero antes de cualquier I+D**: ¿cuántos días llevas sin revisión financiera completa? Mejorar George no cuenta como trabajo hecho. Si hace más de 7 días: patrimonio neto primero, luego hablamos de scripts.
