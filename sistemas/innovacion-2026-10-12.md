🔬 I+D DEL DÍA — 2026-10-12

📊 **ESTADO SISTEMA**: Técnico OK (0 errores, 24 scripts, 505 archivos vault) — **Financiero ROTO** (49 días sin dato gasto, coach parado desde agosto)

🚀 **3 MEJORAS CONCRETAS**:

1. **HOY** — Reactivar módulo coach con pregunta reducida: "¿Gastaste más o menos de 100€ ayer?" (A/B, 2 caracteres). Si falla 2 días → asumir gasto medio y seguir sin preguntar 3ª vez (ya está en CLAUDE.md pero no se ejecuta)

2. **ESTA SEMANA** — Script `patrimonio_neto.sh` que calcule automático: saldo cuentas (via API Bankinter si existe) + valor piso San Antonio (420k fijo) - hipoteca restante. Sin preguntas. Output: un número en `/root/vault/finanzas/patrimonio-neto.md`. Cron semanal viernes 18:00.

3. **ESTE MES** — Dashboard visual tipo Franklin (ver memory): 3 métricas top, colores rojo/verde, PDF auto-generado cada viernes. Métricas: Ahorro mes actual vs 1.000€ marca | Patrimonio neto vs objetivo 2031 | Racha días con dato. José Luis lo ve, no lo produce.

💡 **IDEA DEL DÍA**: Sistema de "trabajo invisible" — todo lo que haces por Maia/Pitifred sin poder facturar (1.000€/mes perdidos) se registra como "horas banco". Cuando llegues a 100h acumuladas, George te obliga a elegir: abrir autónomo o parar de aceptar trabajos. Convierte el problema difuso en decisión binaria con deadline automático.

⚡ **ACCIÓN INMEDIATA**: Calcular ahora cuántos días faltan para llegar a 1M€ patrimonio objetivo (30/07/2031) y cuánto ahorro/mes real se necesita con el patrimonio actual desconocido. Si no hay dato patrimonio actual → asumir 420k (solo piso San Antonio) y calcular desde ahí. Presentar el número a José Luis: "Necesitas X€/mes de ahorro real durante Y meses para llegar".

---

**DIAGNÓSTICO DURO**: El sistema técnico funciona perfecto. El problema es que lleva 49 días midiendo cosas que no importan y 0 días midiendo lo único que importa: ¿va a llegar a 1M€ en 2031? Sin datos financieros George es solo un chatbot caro.
