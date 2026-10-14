**🔍 DIAGNÓSTICO LOGS (ahora mismo):**
Top errores repetidos: `bad ref .git/logs/INDEX.md` (72×), `repack failed` (18×), `OAuth expired` (18×). 

**Causa:** git intentando versionar el vault de Obsidian (INDEX.md se regenera cada 4h, git se confunde). 

**Fix aplicable hoy:** añadir `/root/vault/.gitignore` con `INDEX.md` y `*.log`, limpiar refs rotas con `git gc --prune=now`. Los 463 errores bajan a <20.

¿Quieres que ejecute el fix ahora o prefieres revisarlo primero?
