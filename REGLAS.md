# REGLAS DEL VAULT — George W System

## Convenciones de nombres
- **Kebab-case obligatorio**: `lobato-dental.md`, `perfil-economico.md` (NO "Lobato Dental.md")
- Fechas en formato ISO: `2026-04-16-reunion-cliente.md`
- Sin acentos en nombres de archivo

## Estructura de carpetas
| Carpeta | Contenido |
|---|---|
| `personal/` | Perfil, salud, relaciones, objetivos, finanzas |
| `clientes/` | Una subcarpeta por cliente |
| `proyectos/` | Proyectos transversales |
| `sistemas/` | Documentación interna de George |
| `plantillas/` | Templates reutilizables |
| `recursos/` | Snippets, prompts, referencias |
| `tecnico/` | Troubleshooting, seguridad, configs |
| `tareas/` | Auto-generado por George — NO editar a mano |
| `tareas/diario/` | Logs diarios de actividad |
| `conversaciones/` | Log automático de Telegram |
| `salud/` | Datos Garmin, registros médicos |
| `archivo/` | Archivos obsoletos (>30 días sin tocar) |
| `ideas-futuro/` | Parking de ideas sin prioridad |

## Frontmatter (obligatorio en clientes y proyectos)
```yaml
---
type: cliente | proyecto | personal | referencia
tags: [tag1, tag2]
created: 2026-04-16
description: Una línea describiendo el archivo
---
```

## Links internos
- Usar `[[nombre-archivo]]` en vez de rutas absolutas
- MOCs (Maps of Content) auto-generados por George cada noche

## Archivado automático
- vault_janitor.py corre cada noche a las 04:00
- Archivos sin links entrantes + >30 días sin tocar → se mueven a `archivo/`
- INDEX.md maestro se regenera automáticamente

## Idioma
- Español por defecto
- Inglés solo para código y configuraciones técnicas
