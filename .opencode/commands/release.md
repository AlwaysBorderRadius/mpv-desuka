---
description: Congela main+tag, empaqueta full+patch y crea/actualiza el draft (siempre draft)
---
Flujo /release (el agente principal lo ejecuta paso a paso, nada es automatico):

0. Auditoria de versiones (fail-fast, aborta si algo difiere) y bump del README a
   vN/vM (tablas de Descargas, enlaces de base, "Base probada"). Cruza cada linea
   `Version:` del README.es.md contra su fuente (el README.md en ingles es espejo
   via /translate: no auditar contra el hasta que exista):
   - ModernX/thumbfast/autoload/discord -> cabeceras `Upstream:` en
     portable_config/scripts/*.lua (tabla de AGENTS.md como referencia).
   - Anime4K -> portable_config/shaders/UPSTREAM.
   - Custom Screenshots Folder -> comentario `Mix of` con pins en
     portable_config/scripts/custom_screenshot_folder.lua.
   - Base AJN -> version.txt == manifest.json package_version == AJN_VER.
   - V2 ModelsOnly -> presencia de los 3 `V2_*.onnx` en animejanai/onnx (+ AGENTS.md).
1. Precondiciones: rama `dev` limpia de lo que se va a publicar, README.es.md ya editado
   (vale editarlo en la web de GitHub apuntando a rama `dev`), `current_version` en
   portable_config/script-opts/update_checker.conf igual al tag previsto. Si el ES del
   draft se pulio en la web, esa es la version buena.
2. Merge `dev` -> `main` con mensaje `[vN] merge dev: <resumen>` + tag anotado `vN` en
   lockstep (workflow en .docs/workflow.md). Solo cuando el usuario lo ordene.
3. Ejecutar `.tools/New-DesukaRelease.ps1 -Version N` (modo normal: exige main limpio +
   tag en HEAD). Artefactos full+patch+dev quedan en `.dist/vN/`.
4. Cuerpo del draft: delega en el subagente `releaser` pasandole en el prompt el LOG
   (`git log --no-color <ultimo-publicado>..vN --oneline`), DESUKA_VER, AJN_VER
   (version.txt), FULL_NAME, PATCH_NAME y AJN_URL. Guarda su salida en `.dist/vN-body.md`.
5. `gh release create vN --draft --title "vN" -F .dist/vN-body.md <full> <patch>`
   (dev.zip NO se sube: backup local).
   Si existe draft del MISMO tag: respalda su cuerpo en `.dist/` y actualiza in place
   (`gh release edit` + re-subida de assets homonimos); si el cuerpo fue editado a mano
   en la web, solo regenera el esqueleto fijo (nav de idiomas, separadores `---`,
   bloques `## Descargas`/`## Downloads`, TODOs EN) y conserva las secciones ES
   editadas; nunca regeneres todo sin orden explicita. Draft de OTRO tag: no tocar. Tag ya
   publicado: abortar. Jamas publicar (el publish es clic manual del usuario).
6. Deja la URL del draft para revision. Verificacion + `/review` antes del push a `main`.
