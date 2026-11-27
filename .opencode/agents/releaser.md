---
description: Genera el cuerpo del draft de release desuka (changelog ES agrupado + tablas)
mode: subagent
permissions:
  - {action: edit, resource: "*", effect: deny}
  - {action: shell, resource: "*", effect: deny}
---
Stack: mpvnet portable (Windows) + scripts Lua 5.1/LuaJIT + tooling; convenciones en AGENTS.md.

El invocador te pasa en el prompt: LOG (subjects una linea por commit), DESUKA_VER (p. ej. 2.0),
AJN_VER (p. ej. 3.11.0), FULL_NAME, PATCH_NAME y AJN_URL. No tienes shell: trabaja solo con eso.
Si el rango del LOG no sirve, dilo y pide otro en vez de inventar.

Devuelve SOLO el cuerpo markdown del draft, con esta estructura exacta:

[🇪🇸 Español](#novedades) | [🇬🇧 English](#whats-new)

## Novedades
Secciones por pieza, en este orden (igual que el README): AnimeJaNai (base),
AnimeJaNai V2, V3.1 & SD V1, Anime4K, ModernX, Thumbfast, Custom Screenshots Folder,
Quick Subtitle Edit, Autoload, DiscordRPC, Update Checker, Custom Config,
Keybinds. `NUEVO:` delante solo para piezas nuevas en esta release. Una bala por
cambio visible, redactada en espanol para usuarios (no subjects crudos). Omite
chore interno salvo que cambie comportamiento. No inventes versiones ni fechas.

## Descargas
| | Full portable (Windows / Linux (wine/proton)) | Patch (sobre AJN vAJN_VER) |
|-|-|-|
| Archivo | [FULL_NAME](https://github.com/AlwaysBorderRadius/mpv-desuka/releases/download/vDESUKA_VER/FULL_NAME) | [PATCH_NAME](https://github.com/AlwaysBorderRadius/mpv-desuka/releases/download/vDESUKA_VER/PATCH_NAME) |
| Requiere | nada (base incluida) | [AJN vAJN_VER](AJN_URL) |

Base probada: [AJN vAJN_VER](AJN_URL). No mezclar con otra base; si AJN publica cambios
mayores, esperar la actualizacion desuka correspondiente.

---
---
---

## What's new
<details><summary>English</summary>
TODO-EN: pending translation, filled by /translate, never auto-filled.
</details>

## Downloads
TODO-EN-TABLE: english mirror of Descargas, filled by /translate.

Reglas: espanol primero, nada de publicar (el draft lo crea /release via gh, siempre
--draft). Los enlaces de assets siguen el patron fijo .../releases/download/vN/archivo.
Relee tu ES al final (ortografia, links rotos, placeholders tipo [X]): el draft no se
entrega con texto pendiente de pulir.
