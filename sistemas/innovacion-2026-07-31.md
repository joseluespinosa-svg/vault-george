🔬 I+D DEL DÍA — 2026-07-31

📊 ESTADO SISTEMA: Estable con fallos recurrentes — 1 incidente resuelto hoy (watchdog), 9 días consecutivos de mejora_diaria.sh fallando (401 Unauthorized), memoria_vector.log con batch-overflow desde abril sin corregir

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Matar mejora_diaria.sh — 9 días clavado enviando a bot roto (401), gasta cron y llena logs de basura inútil; o corregir el BOT_TOKEN en el script (línea que lee el .env) y probarlo UNA vez
2. **ESTA SEMANA**: Implementar rotación automática de janitor-log.md cuando pase de 5KB — es el archivo que revienta memoria_vector.sh cada 2 meses (batch excede 5461 tokens), necesita split automático por fecha o truncado semanal
3. **ESTE MES**: Dashboard `/vault/sistemas/salud.md` generado cada viernes con el informe semanal del sistema (el que pide CLAUDE.md punto 8) — ahora ese reporte no existe en ningún sitio, no hay histórico de caídas/relanzamientos/fallos para medir si mejora o empeora

💡 IDEA DEL DÍA: Convertir el parking semanal en un cron autónomo — script que lee `/vault/cerebro/parking.md`, detecta ítems con +21 días sin moverse, y manda mensaje Telegram a las 19:00 del viernes con "3 cosas que llevan un mes aparcadas, elige una para matar o hacer". José Luis esquiva el parking cuando lo pregunta George, pero un cron externo con lista numerada fuerza decisión sin negociación.

⚡ ACCIÓN INMEDIATA: Corregir o matar mejora_diaria.sh antes del próximo disparo (mañana 09:03) — 9 días de error 401 no es ruido, es código muerto ocupando cron.
