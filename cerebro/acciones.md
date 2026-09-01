# ACCIONES — Sistema de ejecución
_Actualizado: 2026-08-31

---

TAREA: HOY 2026-08-01 — 3 tareas del día (barrido no contestado, fijadas por George a petición directa)
ESTADO: en curso — 2 de 3 cerradas (01/08/2026 17:32)
RESPONSABLE: Jose Luis
FECHA_LIMITE: 2026-08-01
NOTAS:
1. Publicar reseña Google Hostal Talamanca (texto ya listo) — HECHO (confirmado 01/08 17:32)
2. Llamar a ING — ¿computan renta futura para el DSTI? — HECHO (confirmado 01/08 17:32, resultado de la llamada sin detallar todavía)
3. Recurso de reposición multa aeropuerto Ibiza (plazo 14/08, quedan 13 días) — PENDIENTE
Caen a SEMANA: tasación San Antonio, perfil Google My Business PitiClean/PitiFred, BBVA gastos cancelación hipoteca.

---

TAREA: HOY 2026-08-02 — 3 tareas del día (barrido contestado 11:10)
ESTADO: 1 de 3 cerrada (multa presentada 03/08), 2 abiertas
RESPONSABLE: Jose Luis
FECHA_LIMITE: 2026-08-02
NOTAS:
1. Presentar recurso de reposición multa aeropuerto (plazo 14/08) — ✅ HECHO 03/08/2026 (registro 2026-E-RE-11977), confirmado de nuevo por audio 04/08
2. Llamar a Ginés — fecha real de presentación de la demanda de desahucio (no el estado, ya confirmado 2 veces) — EN CURSO: audio 04/08 y texto 05/08 (mismo dato, ahora confirmado por escrito a petición de George) — "24, 25" sin mes claro, agosto los juzgados parados/inactivos. Sigue sin fecha exacta ni firme. No repetir pregunta de estado, solo pedir fecha cuando la tenga.
3. Dar el resultado de la llamada a ING — ✅ CONTESTADO 05/08/2026 22:03, tras esquivarlo 4 veces: **ING da 230.000€**. Coincide EXACTO con el supuesto ya usado en `plan-1M-10anos.md` (rehipoteca a 230k → libera ~165k de liquidez para el Flip 1) — confirma el número, no lo cambia. Pendiente aclarar: si es cifra en firme (con renta San Antonio ya computada) o simulación preliminar, y si depende de que Laura salga o vale ya con el contrato de alquiler actual.

⚠️ INCOHERENCIA DETECTADA 05/08: `plan-1M-10anos.md` está redactado a 10 años (vía rápida 5-7), pero el horizonte firme de CLAUDE.md es 5 años (30/07/2031). El ritmo de flips escrito no cuadra con el plazo firme. Revisar en barrido semanal viernes 07/08 — ajustar el plan al plazo real o renegociar el plazo (CLAUDE.md dice que NO se renegocia a la baja, así que lo que hay que ajustar es el ritmo/escala del plan, no la fecha).
Caen a PARKING: barca/kayak (72h vencida 03/08 sin decisión, ver entrada de barca), Google My Business (aclarar antes contradicción de las llamadas).

---

TAREA: Llamar al gestor — declaración renta 2025
ESTADO: ✅ completado (confirmado por José Luis 02/08/2026 — hecha ~2 meses antes, devueltos 500€)
RESPONSABLE: Jose Luis
FECHA_COMPLETADO: ~junio 2026 (fecha exacta no dada)
NOTAS: Declarar ingreso alquiler San Antonio. Factura Sacha 1203 ya resuelta. Esta tarea llevaba semanas repitiéndose como pendiente por una entrada desactualizada en critico.md — corregido.

---

TAREA: Arreglar watchdog limitador.sh (orden de trabajo #2, 29/07/2026)
ESTADO: completado — verificado con evidencia real, no solo revisión de código
NOTAS:
- Fallo A1 (solo revivía si veía "sin tokens" en pantalla): arreglado 29/07 13:55 — añadido chequeo `has-session`, arranca ante cualquier caída.
- Fallo A2 (llamaba a start-george.sh con guion, el script viejo sin sonnet): arreglado 29/07 13:55 — ahora llama a start_george.sh (guion bajo, con --model sonnet).
- PRUEBA REAL (Tarea C) ya ocurrió sola: 29/07 13:56 sesión viva → 13:58 sesión caída → limitador.sh detectó y arrancó sola, log confirma "Sesión inexistente → arranque". Sin intervención SSH.
- Fichero fantasma start-george.sh (con guion): José Luis decidió 30/07 dejarlo muerto ahí, no se borra (congelación 30 días, no se toca nada).
- 30/07 06:43: sesión "george" se recreó de nuevo sola (vía @reboot o watchdog) sin incidencias.
30/07/2026: reenviada la orden #2 (el 29/07 se cortó la sesión justo al recibirla) — respondido con este estado, no hace falta repetir la orden.

30/07/2026 06:48 — ORDEN #3 ANULA LA #2 POR COMPLETO: el diagnóstico real era otro (sesión viva, canal Telegram colgado — no crash). limitador.sh restaurado desde backup (vuelve a start-george.sh sin el chequeo has-session). NO se hizo kill-session de prueba. CONGELACIÓN DE INFRAESTRUCTURA 30 días, hasta 30/08/2026: no tocar limitador.sh, start_george.sh, crontab, systemd, ni scripts/mejoras nuevas. Si José Luis pide un cambio de infra en ese plazo → responder "Congelado hasta el 30/08. ¿Qué hay del email FEIN?" y nada más.

Protocolo si George deja de responder (fijado 30/07): tmux kill-session -t george && /root/start_george.sh, esperar 60s, mandar ping. Si no responde, PARAR, no investigar (plugin channels es experimental).

---

TAREA: Orden #4 — Heartbeat de canal + tono duro (30/07/2026, excepción única a la congelación)
ESTADO: completado, con un aviso importante
NOTAS:
- CONFLICTO DETECTADO: la orden pedía crear /root/assistant/scripts/heartbeat.sh, pero ese fichero YA EXISTÍA — es el script del "buenos días" (Gmail+calendario+tareas, cron 8:00 diario). Sobrescribirlo lo habría destruido. Se creó en su lugar /root/assistant/scripts/heartbeat_canal.sh con la misma lógica que pedía la orden.
- Variables .env: se usaron las que ya existían (BOT_TOKEN, ANTHROPIC_API_KEY) en vez de TELEGRAM_TOKEN; se añadió CHAT_ID=6801069092. Permisos del .env corregidos a 600.
- Cron: línea nueva "20 * * * * /bin/bash /root/assistant/scripts/heartbeat_canal.sh", ninguna otra tocada.
- TAREA 1.4 (prueba manual) NO ejecutada por George: esta sesión de George corre DENTRO de la sesión tmux "george" que el script comprobaría. Ejecutarlo desde aquí bloquea el agente 45s mientras espera el marcador HB-, lo que casi seguro da falso "COLGADO" y mata la sesión a mitad — exactamente el riesgo que la propia orden advertía evitar. La prueba real llega sola con el primer disparo de cron (próximo :20) o José Luis puede lanzarlo a mano por SSH.
- CLAUDE.md actualizado: tono duro y directivo (sección 3), horizonte 1M€/30-07-2031 firme + regla anti-desvío (sección 10, FINANZAS), regla de ignorar mensajes HB- en silencio (sección 2, Telegram).

---

TAREA: Orden #5 — Verificar heartbeat + FEIN pausado + registro de fallos (30/07/2026)
ESTADO: en curso (esperando disparo de cron :20 para cerrar Tarea 1)
NOTAS:
- Tarea 1 (verificar heartbeat): PENDIENTE del primer disparo real a las :20. OJO: la orden dice comprobar /root/assistant/logs/heartbeat.log pero el script real (por la colisión de nombres de la orden #4) es heartbeat_canal.sh y su log es /root/assistant/logs/heartbeat_canal.log. Se comprobará ese. No lanzado a mano (mismo riesgo de siempre: mataría esta sesión).
- Tarea 2: Email FEIN PAUSADO hasta 30/08/2026. No preguntar, no sacarlo en barridos/cierres. Reabrir el 30/08 con: "Email FEIN, un mes parado. ¿Se manda o se cierra?"
- Tarea 3: creado /root/vault/sistemas/registro-fallos.md (carpeta "sistemas/" ya existente en minúscula, no "Sistema/" como decía la orden — mismo criterio que con heartbeat.sh, seguir la convención real del vault).
- Tarea 4: añadido a CLAUDE.md sección 8 (barrido semanal) el informe de 5 líneas del sistema, viernes 19:00.
- CONGELACIÓN reforzada sin excepciones hasta 30/08/2026. Respuesta fija ante petición de mejora: "Congelado hasta el 30/08. Llevo N fallos registrados. El viernes te doy los datos y decides con hechos. ¿Patrimonio neto hoy?"

---

TAREA: Módulo COACH FINANCIERO añadido a CLAUDE.md (30/07/2026)
ESTADO: aplicado (comportamiento, no toca infraestructura congelada)
NOTAS:
- Añadido a sección 10 (FINANZAS) del CLAUDE.md. Marca: 1.000€/mes ahorro, 3 meses seguidos antes de desbloquear cualquier operación.
- Creados finanzas/gasto-diario.md y finanzas/excusas.md (carpeta finanzas/ ya existente en minúscula, no "Finanzas/").
- ✅ gastos-base.md RECIBIDO 31/07/2026 18:30 y ya creado — ver `finanzas/gastos-base.md`. Total gasto identificado (su parte): 3.360€/mes (seguro 360 + alquiler 1.000 + tarjeta 2.000, esta última ya incluye luz/comida). Contra 2.200€/mes de sueldo fijo: **-1.160€/mes en rojo**. NO volver a pedir este dato — está cerrado. (05/08/2026: George lo pidió por error en el barrido matutino pese a estar ya recibido — corregido, no repetir.)
- ⚠️ CONTRADICCIÓN DE DATOS sin resolver: el documento original decía ingresos hogar ~5.000€/mes netos (José Luis 37.000 + Karina ~23.000 brutos/año). El vault (finanzas/2026-07.md) tiene CONFIRMADO el 24/07/2026: José Luis 2.200€/mes neto + Karina 1.600€/mes neto = 3.800€/mes neto total hogar. Pendiente que José Luis confirme cuál es la buena — sin esto no se sabe si el déficit de -1.160€ individual se compensa con el hogar conjunto o no. Repreguntado 05/08.
RESPONSABLE: Jose Luis
FECHA_COMPLETADO: 2026-04-21
NOTAS: Cobro cerrado. Total ~1.400€ cobrado.

---

TAREA: Recibir firma contrato Laura/Jamie
ESTADO: pendiente
RESPONSABLE: Jose Luis
FECHA_LIMITE: antes de mayo 2026

---

TAREA: Publicar reseña Google — Hostal Talamanca
ESTADO: completado — confirmado 01/08/2026
RESPONSABLE: Jose Luis
FECHA_COMPLETADO: 2026-08-01
NOTAS: Texto ya preparado. Google Maps → buscar "Hostal Talamanca Ibiza" → 1 estrella.

---

TAREA: Crear perfil Google My Business — PitiClean / PitiFred
ESTADO: pendiente — pero OJO contradicción (02/08/2026)
RESPONSABLE: Jose Luis + George
FECHA_LIMITE: esta semana
NOTAS: business.google.com — añadir nombre, dirección Ibiza, teléfono. Después generar link de reseña para clientes.
02/08/2026: José Luis dice que esta semana le están llamando mucho para vaciado de piso pero casi nada para arreglar aires. Si el perfil sigue "pendiente" de crear, no debería estar generando llamadas — sin aclarar. Posible que ya exista un perfil o listado (Google/otro directorio) mal categorizado como vaciados en vez de climatización. Pendiente de que José Luis aclare de dónde vienen esas llamadas antes de dar la tarea por no-empezada.
09/08/2026: sigue sin aclarar el origen de las llamadas. Añade motivo de fondo: no quiere darse de alta como autónomo (miedo a Hacienda, impuestos, multas), prefiere facturar trabajos puntuales "en B" en vez de montar algo formal ("en A"). Pide ayuda para estudiar cómo hacerlo. Ver decisión en `decisiones.md` 09/08/2026 — pendiente de estudio conjunto, no resuelto. Esto es la razón real de por qué no hay vía de facturación desde que cayó lo del primo Miguel (24/07).

---

TAREA: Conectar Obsidian móvil vía Remotely Save
ESTADO: pendiente
RESPONSABLE: George + Jose Luis
FECHA_LIMITE: mañana 2026-04-21
NOTAS: Bóveda vacía creada en iPhone. Instalar plugin Remotely Save → URL: http://217.65.146.176:8080

---

TAREA: Llamar Centro de Salud Es Viver — confirmar próxima cita psicología/psiquiatría
ESTADO: en curso
RESPONSABLE: Jose Luis
FECHA_LIMITE: 2026-07-22
NOTAS: Teléfono directo Es Viver: 971 39 16 32 (dato dado por José Luis 22/07). Tel general cambios: 971.22.57.22. Aún sin fecha confirmada de la próxima cita — pendiente resultado de la llamada.
09/08/2026: la cita de seguimiento ya está confirmada para el 21/08 13:30 (ver alertas.md), pero José Luis dice que probablemente no tenga permiso del trabajo para esa hora — riesgo de tener que cambiarla. Quedan 12 días. Acción: llamar al 971 22 57 22 para resolver el permiso o mover la cita.

---

TAREA: Seguimiento caso moto/AENA con abogado Higinio (Palma)
ESTADO: en curso — ✅ contactado 22/07/2026
RESPONSABLE: Jose Luis
FECHA_LIMITE: —
NOTAS: Higinio Muñoz, HM Advocats (higinio@hmadvocats.es). Tel: 971 72 68 44 / 609 316 486. Expediente JAC-188/26 contra AENA (caída de moto, aeropuerto Ibiza, 06/02/2025). José Luis llamó el 22/07/2026 — Higinio dijo que mandará el resultado por correo. PENDIENTE: revisar email cuando llegue.

---

TAREA: Reclamar gastos de cancelación de hipoteca BBVA
ESTADO: pendiente
RESPONSABLE: Jose Luis
FECHA_LIMITE: sin definir
NOTAS: José Luis tiene pendiente un abogado para reclamar a BBVA los gastos de cancelación de una hipoteca. Faltan datos: nombre del abogado, importe reclamado, fecha de cancelación — pendiente de que José Luis los aporte.
09/08/2026: dice "eso está en marcha" — sin aportar ninguno de los datos que faltaban. No cerrar la tarea, solo anotar que según él ya está en curso.

---

TAREA: Plan patrimonio 1M€ a 10 años — acordado 26/07/2026, sustituye a la idea abierta anterior
ESTADO: en curso — plan de fases definido, checklist del mes activa
RESPONSABLE: Jose Luis + George
FECHA_LIMITE: checklist semana 1 de julio-agosto 2026
NOTAS: Ver [[../proyectos/plan-financiero-2026/plan-1M-10anos|plan completo]]. Regla activa: cero operaciones nuevas hasta tasación oficial San Antonio + FEIN por escrito.

---

TAREA: Checklist mes (semana 1) — plan 1M€
ESTADO: pendiente, sin confirmar ningún punto todavía (26/07/2026)
RESPONSABLE: Jose Luis
FECHA_LIMITE: revisar 30/07/2026 (cierre de bucle a 3 días si no hay confirmación)
NOTAS:
1. Email al bróker pidiendo FEIN por escrito — PRIORIDAD 1. George le redactó el texto 28/07/2026, pendiente que José Luis lo envíe.
2. Encargar tasación oficial San Antonio a 2 tasadoras (~400€) — pendiente que confirme día
3. Llamar a ING: ¿computan renta futura para el DSTI? ¿qué %? (con 56% el Escenario A del Excel Alicante se vuelve financiable) — LLAMADA HECHA (confirmado 01/08/2026 17:32), falta que diga el resultado (% computado)
4. Cita con Ginés: demanda de desahucio lista desde el burofax — confirmado otra vez por José Luis 02/08/2026, no volver a preguntar "¿cómo va?". Cuello de botella real de tasación San Antonio y del resto del plan 1M€: sin que Laura/Susan salgan del piso, no se puede tasar. Próxima acción: preguntar a Ginés FECHA de presentación, no el estado.
09/08/2026: repite el mismo dato de siempre ("24, 25" sin mes claro) + razona que si es agosto los juzgados están parados, así que en la práctica no se presenta hasta septiembre. Sin fecha exacta todavía — van 7 días sin novedad real desde el 02/08. Sigue siendo el cuello de botella de ING, tasación y apalancamiento para subastas.
5. Idealista 20 min/día — solo guardar 2 pisos de 80-100k, no actuar
MÉTODO 28/07/2026: mismo sistema que el catalán — cada tarea con día/hora concreto que José Luis confirma, George revisa esa noche.

---

TAREA: Seguimiento subida salarial convenio metal Baleares (EULEN, categoría ENCARGADO G. Tarifa 04)
ESTADO: en curso — acuerdo firmado 26/07/2026, pendiente publicación BOIB
RESPONSABLE: George
FECHA_LIMITE: revisar cada 1-2 semanas
NOTAS: Subida 18% en 4 años (5% 2026, 4,5% 2027, 4,5% 2028, 4% 2029). Referencia histórica: el convenio anterior tardó ~3,5 meses entre firma (29/06/2023) y publicación BOIB (14/10/2023).
28/07/2026: patrón confirmado cruzando 3 nóminas — Gratificación Voluntaria = exactamente 60% del Salario Base en los 3 tramos comprobados (fórmula automática, no importe fijo). Proyección con esto (base+complemento+guardia+gratificación): hoy 2.778,16€/mes → 3.312,93€/mes en 2029 (+535€/mes bruto, +452€/mes neto aprox.).
Legalmente NO hay protección automática (art. 26.5 ET permite absorción por defecto si el contrato no dice lo contrario, y el suyo es genérico) — pero José Luis decidió NO preguntar a RRHH y esperar a ver qué pasa en la nómina cuando llegue la subida. Decisión suya, respetada. No insistir más en esto — solo revisar su nómina cuando el convenio se publique en BOIB.

**28/07/2026 — José Luis mandó el texto completo del convenio del metal Baleares. Hallazgos:**
- Art. 7 (Garantías personales): confirma EXPLÍCITAMENTE que "las mejoras voluntarias que tengan actualmente concedidas las empresas podrán ser absorbidas por el aumento de salario". EULEN puede absorber legalmente la Gratificación Voluntaria — confirmado por escrito, no solo por la ley general.
- Tabla salarial categoría 4.3 (Encargado/Jefe de almacén): base mínima de convenio = 1.243,59€/mes. Su salario base real (1.542,91€) ya está ~299€ por encima de tabla. Por el mismo art. 7, si en cómputo anual ya supera el nivel del convenio, la subida se puede considerar absorbida sin más — legalmente podrían no subirle nada.
- Festivos que caen en fin de semana: NO hay cláusula en este convenio sobre eso — lo regula el calendario laboral oficial anual (Govern Balear/ayuntamiento), no el convenio del metal.
- Conclusión realista: el patrón del 60% (ver nómina mayo) sigue jugando a su favor EN LA PRÁCTICA (fórmula automática de nómina), pero el convenio da cobertura legal para no subirle nada. Expectativas ajustadas a la baja.

---

TAREA: Modelar San Antonio tras desahucio — alquiler tradicional vs por habitaciones
ESTADO: pendiente — pedido por José Luis 26/07/2026, aparcado hasta tener llaves
RESPONSABLE: George
FECHA_LIMITE: tener modelo listo antes de que acabe el desahucio (sin fecha exacta, 6-10 meses estimados)
NOTAS: Pedido: vacancia realista por estacionalidad, coste de gestión, impacto en renta computable por el banco, sensibilidad al seguro de impago, conclusión con número. Ver [[../proyectos/plan-financiero-2026/plan-1M-10anos|plan 1M€]] sección 3.
09/08/2026: José Luis añade plan y preferencias, sigue aparcado hasta llaves: (1) quedarse unos meses viviendo en San Antonio tras el desahucio para ahorrar antes de mover ficha con ING; (2) buscar plaza de parking para los coches; (3) dividir la habitación principal en dos habitaciones pequeñas y pasar la cocina-comedor a dormitorio de matrimonio. Meter esto en el modelo cuando se pueda empezar.

---

TAREA: Recordatorio 72h — compra barca/kayak inflable (no planificada)
ESTADO: ✅ CERRADO — NO SE COMPRA (decidido por George 05/08/2026, José Luis dijo "no sé qué hacer" tras vencer las 72h; motivo: regla 72h vencida + números rojos -1.160€/mes + regla del mes plan 1M€. No reabrir salvo que José Luis lo traiga con datos nuevos y decisión firme propia.)
RESPONSABLE: Jose Luis
FECHA_LIMITE: revisar 2026-08-03 (72h desde aviso)
NOTAS: 31/07/2026 12:56-13:30 José Luis mandó fotos de varias barcas/kayak inflables en venta (Wallapop: "Zodiac Zoom 3,10m" 950€ Alberto F.; "Jago semirrígida 2,7m" 700€ Victor P.; kayak Bestway Lite-Rapid X2; más una barca tipo Novurania sin precio visible). No estaba prevista. Aplicada regla 72h (CLAUDE.md sección 10): no dar visto bueno en caliente. Revisar el 03/08/2026 si sigue queriéndola. Contradice además la regla activa del plan 1M€ (cero operaciones nuevas hasta tasación San Antonio + FEIN por escrito) — no es la misma categoría de "operación" pero sí gasto no planificado en medio del plan de ahorro.

02/08/2026 11:10 — SEGUIMIENTO: José Luis manda capturas de la misma Zodiac Novurania (3,60m, motor Yamaha), ahora con precio: publicada a 2.000€, chat de Wallapop muestra que ya está negociando activamente — ofreció 1.600€ + un MacBook Pro, el vendedor pide 2.300€ o 1.800€+MacBook. Es decir: está regateando en firme DURANTE el propio periodo de 72h que él mismo tiene pendiente hasta mañana. Además él mismo dice que la quiere PLEGABLE (para meterla en un trastero) y esta no lo es — contradice su propio criterio. No dar visto bueno. Regla 72h sigue en pie hasta 2026-08-03.

04/08/2026 08:54 — SEGUIMIENTO (audio, transcripción imperfecta): la regla 72h venció ayer 03/08 sin que él confirmara si sigue queriéndola o no. Menciona ahora dos opciones sin cerrar ("una de ~500€" y "una semirrígida de ~1000€") — cifras y modelos no coinciden con los de las capturas anteriores (Jago 700€, Zodiac 950€/2.000€), no fiable el detalle por audio. Sigue sin decidir. Pedida confirmación explícita: comprar sí/no y cuál.

---

TAREA: HOY 2026-08-25 — 3 tareas del día (barrido contestado 07:24)
ESTADO: en curso
RESPONSABLE: Jose Luis
FECHA_LIMITE: 2026-08-25
NOTAS:
1. WhatsApp a Ginés pidiendo fecha exacta demanda desahucio — José Luis dice "ahora lo hago" (07:24). Comprometido para hoy. Comprobar más tarde si lo mandó.
2. Simulacro expressió escrita B2 — José Luis dice "luego lo hago" (07:24). Comprometido para hoy, sin hora fija.
3. Gasto de ayer (24/08): ✅ dado, 120€ comida semana — ver finanzas/gasto-diario.md. Patrimonio neto de hoy: sigue sin darlo (26 días desde 30/07).

---

---

TAREA: Escribir a Ginés pidiendo fecha de demanda y plazo hasta lanzamiento
ESTADO: comprometido para mañana 2026-09-01
RESPONSABLE: Jose Luis
FECHA_LIMITE: 2026-09-01
NOTAS: Compromiso dado 31/08/2026 21:47. Pide recordatorio a las 09:00 del 01/09 — usar como tarea fija de las 08:00 (ver CLAUDE.md 2.1). Comprobar a los 3 días (04/09) si lo hizo, solo una vez (CIERRE DE BUCLE).

---

## Ver también
- [[critico|CRÍTICO — Dinero y clientes]]
- [[activo|Estado activo]]
- [[alertas|Alertas activas]]
- [[../proyectos/trabajos/formentera-sacha-savines-2026/trabajo|Trabajo Sacha Formentera]]
- [[../temas/laura-contrato|Contrato Laura/Jamie]]
- [[../personal/perfil-economico|Perfil económico]]
