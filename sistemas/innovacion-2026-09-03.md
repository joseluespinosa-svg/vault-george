🔬 I+D DEL DÍA — 2026-09-03

📊 ESTADO SISTEMA: Estable (0 fallos/24h), pero captura de datos del coach financiero casi muerta — solo 5 registros de gasto desde agosto.

🚀 3 MEJORAS CONCRETAS:
1. **Hoy:** Extracción silenciosa de gastos — que George registre automáticamente cuando José Luis mencione un gasto de pasada ("gasté 50€ en el súper") sin tener que preguntarlo formalmente. Reduce fricción, aumenta captura.

2. **Esta semana:** Limpiar parking del 11/08 (hace 23 días) — auditoría de crons/scripts redundantes + analizador de patrones. Decidir: hacer/delegar/matar, no arrastrar más.

3. **Este mes:** Construir el analizador de patrones sobre 142 días de conversaciones (top 3 temas esquivados, cuántas veces desvió hacia herramientas en vez de dinero, tareas más arrastradas). Ya está en el parking, tiene valor real.

💡 IDEA DEL DÍA: **Modo "piloto automático financiero"** — si José Luis no responde al gasto del día después de 2 intentos, George lo calcula automáticamente sumando gastos mencionados ese día en conversación + gasto medio del histórico para el resto, marca como "estimado" y sigue. Sin bloqueos, sin insistir, solo avanzar.

⚡ ACCIÓN INMEDIATA: Implementar extracción silenciosa de gastos — modificar el hook de guardado de conversaciones para detectar patrones tipo "gasté X€", "pagué X€", "X€ de [cosa]" y registrarlos automáticamente en gasto-diario.md con flag "(auto)".
