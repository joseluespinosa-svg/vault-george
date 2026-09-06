🔬 I+D DEL DÍA — 2026-09-05

📊 ESTADO SISTEMA: Operativo pero desfasado — regla 2.1 (31/08) sin aplicar en scripts de mensajería; 289 errores en logs 24h (no 0); patrimonio neto 36 días sin dato completo.

🚀 3 MEJORAS CONCRETAS:
1. **HOY**: Actualizar `barrido_interactivo.sh` y `cierre_interactivo.sh` — siguen enviando 3 preguntas del formato viejo, necesitan aplicar regla 2.1 (08:00 = tarea de HOY ya redactada; 21:30 = solo gasto de hoy).
2. **SEMANA**: Módulo patrimonio neto automatizado — script que calcule desde fuentes reales (saldo BBVA API, valoración coches desde factura/Wallapop, hipoteca desde extracto) en vez de preguntar. Evita el bucle "no tengo el número exacto".
3. **MES**: Panel anti-desvío — antes de responder a propuestas de infraestructura (rehipotecar, comprar, herramientas nuevas), validar automáticamente: ¿hay patrimonio neto actualizado (<7 días)? ¿hay 3 meses ahorro demostrado? Si no → bloquear respuesta y redirigir a lo básico.

💡 IDEA DEL DÍA: **Sistema de "costes de oportunidad visibles"** — cuando José Luis proponga una mejora técnica o idea de inversión, calcular cuántos días de ahorro de 1.000€ cuesta ejecutarla (en tiempo, no en dinero) y mostrarlo ANTES de discutirla. Ejemplo: "Auditar 26 crons = 2 días de tu tiempo = 2.000€ de ahorro no conseguido. ¿Seguro que es prioridad?" Convierte el desvío en decisión informada.

⚡ ACCIÓN INMEDIATA: Investigar los 289 errores detectados en logs últimas 24h (el dato decía 0, pero grep encuentra 289 líneas con error/fail/exception) y actualizar los 2 scripts de mensajería para que apliquen regla 2.1 desde mañana.
