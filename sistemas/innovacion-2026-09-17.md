🔬 **I+D DEL DÍA — 2026-09-17**

📊 **ESTADO SISTEMA:** 57 scripts, 26 crons, 447 archivos vault, 156 días conversación, 0 errores 24h — sistema estable pero gasto diario lleva 24 días sin registro (última entrada 24/08).

🚀 **3 MEJORAS CONCRETAS:**

1. **HOY** → Dashboard racha ahorro: archivo `/root/vault/finanzas/racha.md` que calcule automáticamente días seguidos con dato, ahorro acumulado del mes, y distancia a la marca 1.000€. Se actualiza cada vez que se registre un gasto. José Luis ve progreso sin preguntar.

2. **SEMANA** → Auditoría scripts/crons: los 57 scripts y 26 crons llevan en parking desde 11/08 pendientes de limpieza. Script que detecte última ejecución de cada uno (`grep` en logs), marque los que llevan >30 días sin uso, genere lista de candidatos a borrar. Reduce ruido y mejora mantenimiento.

3. **MES** → Búsqueda vault: 447 archivos .md son demasiados para navegar manualmente. Implementar `vault-search.sh` que indexe títulos + primeras líneas, búsqueda fuzzy tipo `fzf`. Encuentra un dato en <5 segundos vs recorrer el cerebro a mano.

💡 **IDEA DEL DÍA:** Sistema anti-bloqueo TDAH — cuando algo lleve >7 días en parking, George extrae automáticamente el PRIMER paso de <10min (llamada, foto, búsqueda Google, mensaje) y lo pone como tarea HOY sin esperar al viernes. Ejemplo: "división piso" → "mandar foto del plano a George (2 min)". Rompe parálisis por magnitud.

⚡ **ACCIÓN INMEDIATA:** Crear `/root/vault/finanzas/racha.md` con cálculo automático de racha de ahorro actual (ahora mismo: 0 días seguidos, última entrada hace 24 días). Se actualiza vía script cada vez que José Luis registre gasto.
