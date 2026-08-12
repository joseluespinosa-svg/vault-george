---
tipo: referencia
actualizado: 2026-08-11
---

# Usuarios MAIA (Hospital Cas Serres · EULEN)

⚠️ Fuente de verdad: `/root/maia/data.json` en el servidor (tabla `users`), NO las conversaciones antiguas del vault. Las contraseñas se cambian desde el panel admin y los mensajes viejos quedan obsoletos.

Verificado directamente contra la base de datos el 11/08/2026:

| usuario | nombre | rol | contraseña actual |
|---|---|---|---|
| jose | José Luis | admin | maia2026 |
| paco | Paco | tecnico | 0000 |
| fabian | Fabián | tecnico | 0000 |
| hospital-demo | Hospital Valencia Demo | cliente | (hash distinto, no verificada aquí) |

## Notas
- El 12/05/2026 se creó una cuenta `fabian` con contraseña `maia2026` (ver conversaciones/2026-05-12.md) — ese dato quedó **obsoleto**, la contraseña real hoy es `0000` (igual que Paco, probablemente nunca se cambió del alta inicial del 11/05).
- Antes de dar una contraseña a José Luis, comprobar el hash real en `/root/maia/data.json` con `hashPwd()` (HMAC-SHA256 con `JWT_SECRET` del `.env`), no fiarse de logs de conversación pasados.
