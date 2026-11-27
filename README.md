<div align="center">

[🇪🇸 Español](#mpvnet-desuka) | [🇬🇧 English](#mpvnet-desuka-en)

[![Downloads](https://img.shields.io/github/downloads/AlwaysBorderRadius/mpvnet-desuka/total?style=for-the-badge)](https://github.com/AlwaysBorderRadius/mpvnet-desuka/releases) [![Release](https://img.shields.io/github/v/release/AlwaysBorderRadius/mpvnet-desuka?style=for-the-badge)](https://github.com/AlwaysBorderRadius/mpvnet-desuka/releases) [![Stars](https://img.shields.io/github/stars/AlwaysBorderRadius/mpvnet-desuka?style=for-the-badge)](https://github.com/AlwaysBorderRadius/mpvnet-desuka/stargazers)

# ✨MPV DESUKA✨

</div>

**mpv desuka** es una versión personalizada de mpv, que engloba varios proyectos en un solo paquete mas accesible. Creado con el objetivo de ver anime en la mejor calidad y mayor comodidad posible.  

Remasteriza a 4k la imagen original con el uso de shaders en tiempo real, sin perder detalles del fondo de la escena ni de las texturas, a la vez que se eliminan los artefactos mas visibles que puedan haber. Incluye tambien, una interfaz moderna y funciones extra, convirtiendolo asi en un reproductor completo y fácil de usar, a diferencia del mpv/mpvnet base. 

> 📝 *Tambien apto para pelis y series de accion real, pero no uses los shaders ahi eh.*

<img width="2674" height="1383" alt="Captura de pantalla (427)" src="https://github.com/user-attachments/assets/195fad87-b80a-42a7-88ba-d2e7e4601df4" />

[ModernX Demo.webm](https://github.com/user-attachments/assets/62ef7985-2fb5-4f2a-93ca-3e86ef8f28c4)

## 📦 Descargas

|          | Full portable (Windows / Linux (wine/proton)) | Patch (sobre AJN v3.12.5) |
| ---------- | ----------------------------------------------- | --------------------------- |
| Archivo  | [mpv-desuka-v2.0-ajn-v3.12.5-full.7z](https://github.com/AlwaysBorderRadius/mpv-desuka/releases/download/v2.0/mpv-desuka-v2.0-ajn-v3.12.5-full.7z)                                              | [mpv-desuka-v2.0-ajn-v3.12.5-patch.zip](https://github.com/AlwaysBorderRadius/mpv-desuka/releases/download/v2.0/mpv-desuka-v2.0-ajn-v3.12.5-patch.zip)                          |
| Requiere | nada (base incluida)                          | [AJN v3.12.5](https://github.com/the-database/mpv-upscale-2x_animejanai/releases/tag/3.12.5)                          |

> 📝 Base probada: [AJN v3.12.5](https://github.com/the-database/mpv-upscale-2x_animejanai/releases/tag/3.12.5). No mezclar con otra base; si AJN se actualiza, espera la actualización de mpv Desuka.

## 🧰 Instalación

1. Puedes instalar la versión portable completa o bien descargar la versión [v3.12.5 de AnimeJaNai](https://github.com/the-database/mpv-upscale-2x_animejanai/releases/tag/3.12.5) en tu formato favorito (instalador/portable) y según tu sistema operativo, y aplicar el patch de mpv Desuka encima, sobrescribiendo los archivos.

2. Una vez todo colocado, lo primero que debes hacer es abrir `mpv desuka\AnimeJaNaiManager.exe` e ir a la pestaña **Components**. Ahí (o directamente al abrir), si tienes una GPU NVIDIA te saltará un popup donde te pedirá que instales unas dependencias; si no, probablemente no te pida nada, pero si te pide algo, tú instala.

3. Despues de eso cierra y ya puedes arrancar el mpv. Disfruta del anime! :D

4. Extra: revisa "[🧩 ¿Qué incluye? > Custom Config · Configuración](####Custom-Config-Configuración)" para habilitar funcionalidades extra que quizas podrian interesarte como "watch later" y "guardado de nivel de volumen entre sesiones" o  personalizar el "orden de carga automatico de pistas". Puedes revisar tambien el resto de la seccion para aprender mas sobre las funciones de las diferentes piezas de mpv desuka y personalizarlas.

## 🧩 ¿Qué incluye?

### [AnimeJaNai](https://github.com/the-database/mpv-upscale-2x_animejanai) · Base 

> **Version:** v3.12.5  

Version modificada de los reproductores mpv/mpvnet por AnimeJaNai.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

- AnimeJaNai inluye su propio updater, pero lo he desactivado por defecto, pues sobrescribiria parte de nuestros cambios, y si en el futuro cambia la estructura de la aplicación otra vez, se rompería todo. Dejo un archivo de configuracion para que, si eres un usuario avanzado y deseas trastear con la aplicación, puedas hacerlo.

  - En: `portable_config\script-opts\animejanai_update.conf`
	
---
	
</details>

### [AnimeJaNai V2, V3.1 & SD V1](https://github.com/the-database/mpv-upscale-2x_animejanai) · Shader ONNX

> **Fuente:** V2 incluidos de [2x_AnimeJaNai_V2_ModelsOnly.zip](https://github.com/the-database/mpv-upscale-2x_animejanai/releases/download/2.0.0/2x_AnimeJaNai_V2_ModelsOnly.zip) (AJN v2.0.0). AJN ya no los distribuye y aquí los conservamos.  
> **Version:** V2, V3.1 y SD V1  

Shaders basados en redes neuronales. Son modelos entrenados específicamente para reescalar anime a 4K en tiempo real, durante la reproduccion. Es la opción de máxima calidad, limpian artefactos, recuperan detalle y afinan el line-art, a cambio de necesitar mas potencia de la GPU.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

**V2:** Remasteriza la imagen a 4K aumentando drasticamente la nitidez y el nivel de detalle, a la vez que elimina artefactos, pero en algunos casos puede verse raro en escenas con blur o con aberracion cromatica.  

**V3.1:** Recomendado para puristas. Remasteriza la imagen a 4K manteniendo todos los detalles, arreglando el line art, eliminando bordes de sierra y otros artefactos que puedan haber, mientras preserva los efectos originales de blur (difuminado), aberracion cromatica. Aunque cuesta apreciar la diferencia en la variante Standard, por suerte, incluye una variante Sharp (habilitada por defecto) que ofrece lo mismo con un poco mas de nitidez.  

**SD V1:** Lo mismo que V2, pero diseñado para animes antiguos (retro) con resolucion inferior a 1080p. Incluye un componente opcional extra llamado "Temporal Fix", que se encarga de limpiar artefactos típicos en los animes viejos para no contaminar el upscale.

https://github.com/user-attachments/assets/13f05267-cd61-4de9-ad7f-ce8030102465

  - Ahora el modelo SD V1 tiene 3 perfiles (Retro SD V1 Quality/Balanced/Performance):
    - **Retro SD V1 Quality:**  aplica el Temporal Fix sobre el frame upscaleado.
    - **Retro SD V1 Balanced:**  lo aplica antes del upscale a resolución original.
    - **Retro SD V1 Performance:**  no lo usa.

- Las variantes de los modelos V3 conviven en los perfiles predeterminados ("Default Profiles"). Si deseas usar la variante Standard, abre el AnimeJaNai Manager y en sus perfiles, cambia el botón **Model Preset** de `Sharp` a `Standard`.

---

</details>

### [**Anime4K**](https://github.com/bloc97/Anime4K) · Shader GLSL

> **Version:** v4.0.1  

Shaders ligeros que combinan filtros ligeros con pequeñas redes neuronales. Limpian artefactos y rescalan la imagen en tiempo real, sin necesidad de hardware potente. A cambio, tienden a suavizar la imagen y pueden perder detalle de fondos y texturas.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

</details>

### **ModernX** · Script

> **Fuente:** [Fork](https://github.com/zydezu/ModernX) mas mantenida a dia de hoy como base  
> **Version:** ([739a201](https://github.com/zydezu/ModernX/commit/739a201b15547cccf39cd37cd2e6b32d0ab623e3) · Jul 25, 2026) + modificaciones Desuka  

Interfaz moderna para mpv, con MUCHAS modificaciones propias.

[ModernX Demo.webm](https://github.com/user-attachments/assets/62ef7985-2fb5-4f2a-93ca-3e86ef8f28c4)

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Diferencias respecto a la version base

- **Menús**

  - Añadido botón en la esquina superior izquierda que abre un menú avanzado con todas las funciones y opciones del reproductor

  - El menú avanzado tambien incluye acciones propias de mpv Desuka como:
    - Acceso a lo modos de Anime4K.
    - Activar/Desactivar Discord Rich Presence para la sesion.
    - Buscar actualizaciones de mpv Desuka.
    - Acceso directo a la página de releases.
   
  - Ahora los botones de subs/audio/vídeo despliegan un menú desde donde puedes escoger directamente la pista que quieres.

  - Cuando las pistas no tienen ni nombre ni idioma asociado, se muestra p.ej: Pista de audio 1, Pista de vídeo 1...

  - Nuevo menú para escoger shaders (AnimeJaNai y Anime4K). Con los perfiles vacíos de AnimeJaNai ocultos hasta que les cambies el nombre cuando los modifiques.
 
  - Los menús soportan submenús, scroll y cierre al hacer clic fuera de ellos.

  - Y su apariencia también es personalizable.

- **Nuevos botones**

  - Selector de pista de vídeo (útil si un mismo archivo tiene versiones SDR/HDR) y con tooltip.
  - Selector de shaders, con un tooltip que muestra el shader o combinación de shaders en uso.
  - Acceso directo al nuevo `quick_subtitle_edit.lua` para editar subtítulos desde el reproductor (sí, no es broma, más detalles abajo).

- He añadido tooltips también al botón de audio.

- He reajustado la altura entre los botones y la barra de progreso, para que los tooltips quepan y no solapen el tiempo ni los capítulos.

- Ahora los tooltips aparecen fijos, anclados al botón, en vez de moverse junto al ratón (mejor accesibilidad y optimización).

- **Notificaciones modernas y unificadas**

  - Un único sistema de notificaciones para toda la interfaz. Los "mensajes" de los comandos, botones y scripts ahora utilizan un mismo canal, evitando que se acumulen textos unos encima de otros. Ahora casi todo usa una cápsula de notificación moderna en vez de imprimir el texto en pantalla.

  - Cada notificación utiliza un color según su categoría (info, éxito, aviso, error).

  <img width="3132" height="370" alt="imagen" src="https://github.com/user-attachments/assets/69f33d45-6941-4aef-9c2e-f58e2dfac4fa" />

  - El estilo de las notificaciones es completamente personalizable.
  
  <img width="3132" height="228" alt="imagen" src="https://github.com/user-attachments/assets/7f2809ea-48f7-4272-92a6-c27a89482a23" />

- **Animaciones para todo, como en las aplicaciones modernas!**

  - Los botones ya no cambian de tamaño ni muestran su efecto glow al instante: ahora utilizan transiciones rápidas y suaves.

  - Los botones de ventana ahora tienen un nuevo glow coloreado de fondo al pasar el ratón por encima (preferencia visual y mejora en la accesibilidad).

  - Los menús tienen una animación de entrada y desvanecimiento, acorde a su posición.

  - Las notificaciones también tienen animación de entrada y desvanecimiento, sin repetirse cuando ya hay notificaciones en pantalla.

  - Y puedes editar el comportamiento de las animaciones.

- Ahora la interfaz es visible también en reposo, cuando no hay ningún vídeo reproduciéndose, como en cualquier otro reproductor. Antes, al no salir la interfaz, no podías cerrar la ventana y solo se podía cerrar desde la barra de tareas.

- Actualizado el script base original, que incluye de nuevo:
  - Varios bugfixes menores.
  - Nuevo estilo de la barra de reproducción (capítulos estilo YouTube).

- Nueva barra de volumen dinámica con iconos contextuales y posición personalizable.

- Nueva barra de progreso dinámica con iconos contextuales y posición personalizable.

- Opción para ocultar la extensión del nombre del archivo, activada por defecto.

- Interfaz completamente traducida al español.

- **Banderas de idioma** en tooltips, menús y notificaciones!
  - 72 idiomas cubiertos, incluyendo regionales españoles y alguno de otros países.
  - Ahora puedes elegir cómo identificar el idioma de las pistas.
    - **Banderas:**  `[es]` → 🇪🇸, `[en]` → 🇬🇧, `[es-419]` → 🇲🇽.
    - **Nombre del idioma:**  español, inglés, español latinoamericano, etc. (solo disponible en español e inglés).
    - **Código:**  `[es]`, `[en]`, `[es-419]`, etc.

- **Personalización!**   Ponte la interfaz a tu gusto editando todo lo mencionado arriba en `mpv desuka\portable_config\script-opts\modernx.conf`

- Bug fixes y optimizaciones:
  - Optimizado cómo se calcula el tiempo de vida de la interfaz. Antes al estar en pausa, podía congelarse en medio del desvanecimiento, cosa que en ocasiones podía congelar la aplicación entera.

  - Corregido el problema por el que la interfaz permanecía visible durante la pausa cuando debería desaparecer.

  - Generación de thumbnails optimizada bajo demanda, pues podía contribuir a sobrecargar la interfaz con peticiones inútiles.

#### ⚙️ Algunos detalles importantes

- Algunos botones de la interfaz tienen **dos funciones**:  
  → **Click derecho** = función principal  
  → **Click izquierdo** = función alternativa

---

</details>

### [**Thumbfast**](https://github.com/po5/thumbfast) · Script

> **Version:** ([0f711de](https://github.com/po5/thumbfast/commit/0f711de3138c9bd6718209d819ac54022c23ded2) · Jun 28, 2026) + modificaciones Desuka  

Muestra miniaturas en la barra de progreso, como en YouTube. En mi version arregle el infame error "ERROR! cannot create mpv subprocess", esta vez sí, 100% real, no fake.

### **Custom Screenshots Folder** · Script

> **Fuente:** Mix propio de [customscreenshot.lua](https://github.com/jonniek/mpv-scripts/blob/master/customscreenshot.lua) y [screenshotfolder.lua](https://github.com/zydezu/mpvconfig/blob/main/scripts/screenshotfolder.lua)  
> **Version:** last ([bc8bfe2](https://github.com/jonniek/mpv-scripts/commit/bc8bfe265cc45e51152acf885f7715339843dca7) · Apr 6, 2019) +  ([f9b38cf](https://github.com/zydezu/mpvconfig/commit/f9b38cf6b55755ee27ff9f879cd44bb36798e65c) · Jul 10, 2026) + modificaciones Desuka  

Capturas organizadas por serie y temporada según el modo elegido.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

- Capturas organizadas por serie y temporada según el modo elegido.
  - Por serie: `<Screenshot folder> / <Series> / <Series> (N).png`

    - Ej: `mpv screenshots / Jujutsu Kaisen / Jujutsu Kaisen (1).png`

  - Por temporada: `<Screenshot folder> / <Series> / <Series> <Season> / <Series> <Season> (N).png`

    - Ej: `mpv screenshots / Jujutsu Kaisen / Jujutsu Kaisen: Shimetsu Kaiyuu - Zenpen / Jujutsu Kaisen: Shimetsu Kaiyuu - Zenpen (1).png`

  - El script viene configurado para funcionar directamente con la estructura de mi biblioteca, organizada con mi otro proyecto [AniListRenamer-for-Shoko](https://github.com/AlwaysBorderRadius/AniListRenamer-for-Shoko):

    ```
    📁 Jujutsu Kaisen\
    ├──📁 Jujutsu Kaisen\
    │   ├──🎞️ Jujutsu Kaisen - 01 - Ryomen Sukuna.mkv
    │   └──🎞️ Jujutsu Kaisen - 02 - Por mí.mkv
    ├──📁 Jujutsu Kaisen 2nd Season\
    │   ├──🎞️ Jujutsu Kaisen 2nd Season - 01 - El tesoro escondido (1).mkv
    │   └──🎞️ Jujutsu Kaisen 2nd Season - 02 - El tesoro escondido (2).mkv
    └──📁 Jujutsu Kaisen: Shimetsu Kaiyuu - Zenpen\
        ├──🎞️ Jujutsu Kaisen: Shimetsu Kaiyuu - Zenpen - 01 - Ejecución.mkv
        └──🎞️ Jujutsu Kaisen: Shimetsu Kaiyuu - Zenpen - 02 - Otra vez.mkv
    ```

    El script lee el nombre de la carpeta de la serie para identificar la serie y la carpeta de la temporada para identificar la temporada.

  - También incluye compatibilidad con nombres genéricos, típicos del anime descargado, como:

    - `[sam] Vinland Saga [BD 1080p FLAC]\[sam] Vinland Saga - 01 [BD 1080p FLAC] [B78ACE46].mkv`
    - `[Foxtrot] Vinland Saga S2 [BD 1080p]\[Foxtrot] Vinland Saga - S02E01 [BD 1080p].mkv`

    Pero estas reglas vienen desactivadas por defecto. Para habilitarlas:

    - Abre `mpv desuka\portable_config\scripts\custom_screenshot_folder.lua`
    - Busca la tabla `custom_rules` en la línea 168.
    - Ahí dentro, cada bloque es una regla, y arriba de cada hay un comentario con un ejemplo para el caso que esta hecha. Cada bloque tiene una clave `enabled` para activar o desactivar la regla (gana la primera regla activa que coincida).

  - Y si ninguna es útil en tu caso, pásale el script a tu IA y pídele que te haga una regla nueva xd.

- En caso de que ningúna regla consiga identificar la serie o el vídeo no tiene una carpeta contenedora, la captura se guardará en una carpeta genérica llamada `_unmatched`, donde iran todas las capturas sin clasificar (`mpv screenshots / _unmatched / <Filename> (N).ext`).
  - Puedes cambiar el nombre de la carpeta en `mpv desuka\portable_config\script-opts\custom_screenshot_folder.conf` cambiando el valor de `quarantine_name=_unmatched`.

- Con Ctrl+S y el botón en la interfaz, se saca captura del vídeo sin subtítulos a resolución nativa, y con S se captura toda la ventana incluyendo los subtítulos y la interfaz visibles, como una captura de pantalla.

- Notificaciones en español e inglés.

- Las capturas se guardan por defecto en `mpv screenshots` dentro de tu carpeta de Imágenes.

- Compatible con la ubicación nativa de la carpeta Imágenes tanto en Windows como en Linux. Funciona incluso en reubicaciones personalizadas.

---

</details>

### **Quick Subtitle Edit** · Script

> **Fuente:** Script propio  

Editor de subtítulos en tiempo real! Directamente desde el reproductor!

[Quick Subtitle Edit Demo.webm](https://github.com/user-attachments/assets/d96072f8-10e9-40c3-830e-fca1f4f00339)

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

- Tiene dos modos de uso:
  - **Modo nativo:**  (botón de lápiz/Ctrl+Z) renderiza los subtítulos tal cual los ves en pantalla. Respeta tamaños, estilos y fuentes, incluso embebidas y hasta carteles simples (como en subs de Crunchyroll y otros fansubs), pero mejor no lo uses en karaokes o carteles muy profesionales (en el caso de fansubs muy talentosos).
  - **Modo OSD:**  (clic izquierdo en el botón/Ctrl+Shift+Z) muestra los subtitulos en el OSD, osea escritos en pantalla. Útil para editar subtítulos más complejos que aún no se puedan renderizar correctamente en el modo nativo.

- Soporta escenas con múltiples líneas a la vez. Puedes saltar entre ellas y editarlas al mismo tiempo, manteniendo los cambios visibles y guardándolos todos al finalizar la edición.

- Cuenta con salvaguardas que pausan el vídeo al instante, impiden mostrar la interfaz en medio de la edición y bloquean teclas peligrosas mientras editas.

- También usa las nuevas notificaciones para mostrar mensajes de carga y de éxito.

- Incluye una leyenda con keybinds para la edición.

- Soporte para letras latinas (incluye ñ, acentuadas, ü, ¿¡), números y símbolos del teclado ES/US.

- Interpreta saltos de línea y soporta mantener pulsadas las teclas, desde letras hasta las flechas de movilidad.

- Funciona extrayendo del mkv la pista de subs y las fuentes usadas en pantalla (si no las tienes instaladas) para renderizarlo de forma auténtica y las carga al video sin darte cuenta. Si hay varias lineas, se crean archivos con las otras lineas para usar como máscaras. Al final, todos los archivos temporales se eliminan automáticamente y solo se conserva el subtítulo editado (si no editaste nada, también se borra solo).

---

</details>

### [**Autoload**](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autoload.lua) · Script

> **Version:** [867990d](https://github.com/mpv-player/mpv/commit/867990d949e9ad99406e0f26e5528e95046b30a7) · Oct 15, 2026  

Carga automáticamente todos los archivos de vídeo en la carpeta a la lista de reproducción.

### [**DiscordRPC**](https://github.com/tnychn/mpv-discord) · Script

> **Version:** first and last (9224b11 · Oct 12, 2024) (repo archivado, sin más updates) + modificaciones Desuka  

Integración con Discord Rich Presence. *(integracion con modernX)*

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Diferencias respecto a la version base

- Arranque silencioso: ya no espamea cada vez que inicies un vídeo.

- Usa las nuevas notificaciones.

- Socket único por instancia: cada ventana nueva que abras se mostrará en tu estado de Discord y no fallará en silencio.

- Ahora la ruta al .exe es portable, con lo cual ya no tendrás que configurar nada para usarlo.

#### ⚙️ Algunos detalles importantes

- Nota: si usas el reproductor junto a Seanime (el mejor reemplazo del explorador de archivos para ver el anime descargado), cosa que recomiendo, desactiva la función de Discord de mpv Desuka en `mpv desuka\portable_config\script-opts\discord.conf` (`active=no`), pues el Discord Rich Presence de Seanime es mucho mejor.

---

</details>

### **Update Checker** · Script

> **Fuente:** Script propio  

Buscador de actualizaciones de mpv Desuka.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

- Revisa en cada inicio si hay actualizaciones (activable/desactivable) y solo notifica si detecta una versión superior.

- Configurable (on/off y más) desde `mpv desuka\portable_config\script-opts\update_checker.conf`.

- Comprobación manual con `Alt+U` o desde el menú avanzado (Desuka > Check Updates), con indicador animado durante el proceso.

- Notificaciones en español e inglés.

---

</details>

### Custom Config · Configuración

> **Fuente:** AnimeJaNai se encarga de las configuraciones tecnicas automaticamente + modificaciones Desuka en el comportamiento.  

Comportamiento del reproductor personalizado, a traves de modificaciones en: `mpv.conf`, `mpvnet.conf`, `input.conf` y `animejanai.conf`.

<details><summary> ➡️ Clica para expandir ⬅️ </summary>

#### ⚙️ Algunos detalles importantes

- El guardado del **nivel de volumen** entre sesiones está desactivado por defecto.  
  → Si quieres activarlo, abre `mpvnet.conf` y cambia `remember-volume=no` a `yes`.

- La función **“watch later”** también está desactivada por defecto.  
  → Para activarla, abre `mpv.conf`, cambia `resume-playback=no` a `yes` y descomenta `watch-later-options=start`.

- Las pistas de Audio y Subtitulos se cargaran automatiamente en este orden, independientemente de su posición (puedes cambiarlo en `mpv.conf`):  
  → **Audio:** `Japones`, `Ingles`, `Español`, etc.  
  → **Subtitulos:** `Español`, `Latino`, `Ingles`, etc.

---

</details>

## 🎞️ Comparaciones entre Shaders

[Mejor encode vs AnimeJaNai V3.1 & V2 vs Anime4k](https://slow.pics/s/BOdM6ZwS)

> 📝 ***Mejor Encode:** El mejor encode que existe, segun Sneedex y SeaDex. Uso la mejor version que existe del anime para que veas la diferencia que hay con los shaders, a pesar de ser la mejor version del anime que se puede descargar.*  

> 📝 *Recomiendo usar la opción de Slider, que esta abajo del todo.*  

> 📝 *Fijate sobre todo en los fondos, los primeros planos y las lineas del dibujado (line art).*  

| Shaders | Nitidez | Generacion de artefactos nuevos | Potencia requerida | Notas |
|-|-|-|-|-|
| AnimeJaNai Quality V2 | ★★★★★ | ★★★★ | ★★★★★ | El mas nitido, pero demasiado. Puede generar muchos artefactos. |
| AnimeJaNai Balanced V2 | ★★★★ | ★★ | ★★★★ | El mejor balance entre nitidez y artefactos, en mi opinion. En movimiento, no se notan, solo pegado a la pantalla y con el frame pausado. Lo recomiendo si ves anime a cierta distancia y para pantallas 4k grandes. |
| AnimeJaNai Performance V2 | ★★★⯪ | ★ | ★★★ | No tan perfecto en fondos y texturas como el Balanced V2, pero mantiene buen balance. |
| Anime4k Mode A | ★★★ | ★★★★★ | ☆ | Muy nitido a coste 0 de potencia, pero a cambio de una perdida enorme de detalles en texturas, fondos y a veces un line art irregular. |
| AnimeJaNai Balanced V3.1 (Sharp) | ★★ | ☆ | ★★★★ | El mejor balance entre fidelidad y nitidez. Lo recomiendo como alternativa al Balanced V2. |
| AnimeJaNai Performance V3.1 (Sharp) | ★ | ☆ | ★★★ |  |
| AnimeJaNai Balanced V3.1 (Standard) | ☆ | ☆ | ★★★★ |  |
| AnimeJaNai Performance V3.1 (Standard) | ☆ | ☆ | ★★★ |  |

> 📝 *Más ★ = más nitidez / más artefactos / más potencia. ☆ = nada.*

> 📝 *Las variantes de AnimeJaNai V3.1 (Standard) no mejoran la nitidez, su funcion es la de eliminar todos los artefactos que pueda tener la imagen.*

> 📝 *Mis favoritos son el AnimeJaNai Balanced V2 y el AnimeJaNai Balanced V3.1 (Sharp). Si te limita la GPU, baja a sus versiones Performance, y si aun así no puedes, Anime4k siempre está ahí*

> 📝 *La potencia real depende de la resolución de tu pantalla: a menor resolucion, una grafica menos potente sera suficiente*

## ⌨️ Keybinds importantes

> 📝 *Todo se puede hacer desde la interfaz.*

<details><summary>Click para abrir</summary>
	
- `Click derecho`, `Espacio` ➝ Pausa  
- `↑` ➝ Subir volumen (+2)  
- `↓` ➝ Bajar volumen (−2)  
- `Ctrl + ↑` ➝ Subir volumen (+10).
- `Ctrl + ↓` ➝ Bajar volumen (−10).
- `Ctrl + Alt + ↑` ➝ Subir volumen (+50).
- `Ctrl + Alt + ↓` ➝ Bajar volumen (−50).
- `→` ➝ Avanzar 5 segundos  
- `←` ➝ Retroceder 5 segundos  
- `Ctrl + →` ➝ Avanzar 85 segundos  
- `Ctrl + ←` ➝ Retroceder 85 segundos
- `Shift + →` ➝ Avanzar un fotograma  
- `Shift + ←` ➝ Retroceder un fotograma
- `1–6` ➝ Activa los diferentes modos de Anime4K  
- `0` ➝ Desactiva Anime4K  
- `Alt + 1 / 2 / 3` ➝ Activa AnimeJaNai V3.1 ( Quality (Balanced) / Balanced / Performance ) - variante Sharp habilitada por defecto.
- `Ctrl + 1 / 2 / 3` ➝ Activa AnimeJaNai V2 ( Quality / Balanced / Performance ).
- `Ctrl + 4 / 5 / 6` ➝ Activa AnimeJaNai V1 SD para animes Retro ( Quality / Balanced / Performance ).
- `Ctrl + 0` ➝ Desactiva AnimeJaNai
- `Ctrl + E` ➝ Abre el menú de AnimeJaNai  
- `Ctrl + J` ➝ Muestra qué modelo de AnimeJaNai está activo  
- `D` ➝ Activa o desactiva Discord Rich Presence para la sesion.  
- `Ctrl + S` ➝ Captura del vídeo sin subtítulos, a resolución nativa.
- `S` ➝ Captura de toda la ventana (si se ven subtítulos o la interfaz, se capturan también, es como una captura de pantalla).
- `Ctrl + Z` ➝ Arranca el editor de subtítulos.
- `Ctrl + Shift + Z` ➝ Arranca el editor de subtítulos en modo OSD.
- `Alt + U` ➝ Revisa si hay actualizaciones de mpv Desuka.
- `Ctrl + Click derecho` ➝ Abre el menú contextual con todos los ajustes
- `C` ➝ Abre el menú de mpvnet *(porfa no toques nada o puedes romper la config 😭🙏🏻 y será culpa tuya, no mía)*

> 📝 *AnimeJaNai y anime4k se pueden usar en conjunto, pero es muy criminal, mejor no lo hagas.*

</details>

## 🗺️ Roadmap

Ideas futuras: [ROADMAP.md](ROADMAP.md).
¿Como podemos mejorar mas mpv desuka? Hazmelo saber en un issue.

## ☕ **APOYA MI TRABAJO**

> Si te gusta mi trabajo y quieres darme las gracias, puedes invitarme a un café :D\
> [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/elgamereduard)

---

<div align="center">

# ✨MPVNET DESUKA (EN)✨

</div>

**mpvnet desuka** is a custom build of mpvnet made to watch anime in the best possible quality and comfort.  
It upscales to 4k the original image using real-time shaders, without losing any details in the background or textures, while eliminating the most noticeable artifacts that may be present. It also includes a modern interface and extra features, making it a complete and easy-to-use player, unlike the base mpv/mpvnet. 

> 📝 *Also suitable for movies and series.*

<img width="2674" height="1383" alt="Captura de pantalla (427)" src="https://github.com/user-attachments/assets/195fad87-b80a-42a7-88ba-d2e7e4601df4" />

### 🎞️ Comparisons

| Scenarios | Best Encode* vs AnimeJaNai V2 UC vs Anime4k Mode A (the sharpest ones) |
|-|-|
| Close-ups | [Link](https://slow.pics/c/Cb703Qla) |
| Backgrounds and Textures | [Link](https://slow.pics/c/AR9TAsPZ) |

> 📝 ***Best Encode:** The best encode available according to Sneedex and SeaDex.*  

| Shaders | Extra Comparisons |
|-|-|
| Best Encode vs AnimeJaNai V3 C vs AnimeJaNai V2 UC vs Anime4k Mode A | [Link](https://slow.pics/c/XJtobDb0) |
| Best Encode vs AnimeJaNai V3 C vs AnimeJaNai V3 Sharp SUC / UC / C vs AnimeJaNai V2 UC | [Link](https://slow.pics/c/3Cz5SCTY) |
| Best Encode vs Anime4k Mode A vs AnimeJaNai V2 SUC vs AnimeJaNai V2 UC | [Link](https://slow.pics/c/QgO4Wf5i) |

> 📝 *If you have a hard time seeing the differences between, for example, the 2nd and 4th, 5th... screenshots, use the Slider option.*  

### My recommendation:  

| Recommended Option | Shader and Model | Use cases |
|-|-|-|
| Option 1 | AnimeJaNai V2 UC | The sharpest, without being excessive (in my opinion, AnimeJaNai V2 C is too much). |
| Option 2 | AnimeJaNai V3 Sharp C > UC > SUC | Recommended if you are more purist and want a good balance between sharpness and fidelity. |
| Option 3 | AnimeJaNai V2 SUC > Anime4k | Recommended if you want more sharpness, but are limited by your GPU. (Both options blur the backgrounds a little, especially Anime4k). |
| Option 4 | AnimeJaNai V3 C > UC > SUC | Recommended if you are really purist and only want to polish the image and remove all the artifacts that the encoding may have. |

## 🧰 Installation

> 🪟 **Made for Windows**  
> 💻 *Although it also works on Linux using WINE or Proton.*

1. **Extract** the `mpvnet desuka` folder wherever you want.  
   - Recommended: `C:\Program Files\mpvnet desuka` or `C:\APPs\mpvnet desuka` if you’re special like me.

2. If you saved it in a different path:
   - Go to `portable_config/script-opts/discord.conf`
   - Edit the line: `binary_path=C:\Program Files\mpvnet desuka\mpv-discord.exe`

3. For **AMD GPUs**:
   - Open `mpvnet desuka > ctrl+E > Global Settings`
   - Change `Upscaling Backend` from `TensorRT` to `DirectML`

4. In **NVIDIA GPUs RTX**:
   - The first time you load any **AnimeJaNai** model, a terminal window will pop up. Don’t panic, the engine is creating a `.engine` profile for your PC.
   
- Keep in mind AnimeJaNai is heavy: every time you enable it, it’ll take a few seconds to apply.  
  Pause the video before switching models, and do not maximize nor enter full screen while the shader is still loading.

- The AnimeJaNai build of mpvnet is very "sensitive", so treat it with care.  
  If it’s doing something like loading a model or fading the interface, wait until it finishes before doing something else like seeking backward/forward.

5. Now it’s time to learn the **keybinds** so you can actually fully use it :)  
Also check the **changelog** (very interesting!) and the **documentation** + the documentation of what's included if you want to know more.

### 🧯 Troubleshooting

- If AnimeJaNai doesn’t work (no load or no visible effect):  
  ➝ Delete all `.engine` files in `mpvnet desuka/animejanai/onnx` (only for NVIDIA RTX GPUs).

- If mpvnet or the interface freezes:  
  ➝ Open Task Manager and kill the mpvnet and mpv-discord.exe processes.  

## 📖 Documentation

### 🔧 Recommended Requirements

- **AnimeJaNai**:

| Model | GPU |
|-|-|
| Compact (C) | RTX 4090 |
| Ultra Compact (UC) | RTX 3080 |
| Super Ultra Compact (SUC) | RTX 3060 |

- **Anime4K** *(lighter)*:

| Your Screen Resolution | Mode | GPU |
|-|-|-|
| 4K | Any Mode | Mid-high to high-end GPU |
| 1080p | Any Mode | Mid-low to mid-range GPU |

### 🧩 What's included?

| | Tipo | Descripción |
|-|-|-|
| [**AnimeJaNai V2 & V3**](https://github.com/the-database/mpv-upscale-2x_animejanai) | Shader ONNX | Remasters the image to 4K, drastically increasing the level of detail and sharpness while removing artifacts, but in some cases it may look strange in scenes with blur or chromatic aberration. V3: Recommended for purists. Remasters the image to 4K, maintaining all the details, fixing the line art, removing jagged edges and other artifacts that may be present, while preserving the original effects of blur, dithering, chromatic aberration... Although it's hard to see the difference. On the other hand, the Sharp version offers the same thing, but with a little more sharpness. |
| [**Anime4K**](https://github.com/h5mcbox/anime4k) | Shader GLSL | Sharpens and removes artifacts, but softens the image a lot, losing some background and texture details. |
| [**autoload**](https://github.com/mpv-player/mpv/blob/master/TOOLS/lua/autoload.lua) | Script | Automatically loads all video files in the folder into the playlist. |
| [**modernX**](https://github.com/zydezu/ModernX) | Script | Modern mpvnet interface with custom modifications. *(Using the most maintained branch.)* |
| [**thumbfast**](https://github.com/po5/thumbfast) | Script | Displays thumbnails on the progress bar, just like YouTube. *(Using a previous commit to fix a bug.)* |
| [**DiscordRPC**](https://github.com/tnychn/mpv-discord) | Script |  Discord Rich Presence integration. |
| **Custom Config** | Configuración | Custom player behavior, through modifications to: mpv.conf, mpvnet.conf, input.conf, animejanai.conf, and script-opts. Sources: [Ref1](https://github.com/the-database/mpv-upscale-2x_animejanai) · [Ref2](https://github.com/Tsubajashi/mpv-settings) |
| [**mpvnet**](https://github.com/the-database/mpv-upscale-2x_animejanai) | Base player | AnimeJaNai modified version of mpvnet. |

### ⌨️ Keybinds

- `Right Click`, `Space` ➝ Pause  
- `Ctrl + Right Click` ➝ Opens contextual menu with all settings  
- `Ctrl + E` ➝ Opens AnimeJaNai menu  
- `Ctrl + J` ➝ Shows which AnimeJaNai model is active  
- `C` ➝ Opens mpvnet menu *(please don’t mess around or you might break the config 😭🙏🏻 and it’ll be your fault, not mine)*  
- `Ctrl + 1 / 2 / 3` ➝ Enable AnimeJaNai V2 (C / UC / SUC)
- `Ctrl + 4 / 5 / 6` ➝ Enable AnimeJaNai V3 Sharp (C / UC / SUC)
- `Ctrl + 7 / 8` ➝ Empty AnimeJaNai profiles, in case you want to chain several models into a new profile from the AnimeJaNai menu.
- `Ctrl + 7` ➝ Enable AnimeJaNai V1 SD Beta  
- `Shift + 1 / 2 / 3` ➝ Enable AnimeJaNai V3 (C / UC / SUC)  
- `Ctrl + 0` ➝ Disable AnimeJaNai  
- `1–6` ➝ Enable different Anime4K modes  
- `0` ➝ Disable Anime4K  
- `D` ➝ Toggle Discord Rich Presence  
- `S` ➝ Take screenshots from the player  
- `Up` ➝ Volume +2  
- `Down` ➝ Volume −2  
- `Shift + Up` ➝ Volume +50  
- `Shift + Down` ➝ Volume −50  
- `Right` ➝ Jump +5 seconds  
- `Left` ➝ Jump −5 seconds  
- `Ctrl + Right` ➝ Jump +85 seconds  
- `Ctrl + Left` ➝ Jump −85 seconds
- `Shift + Right` ➝ Frame-step forward  
- `Shift + Left` ➝ Frame-step backward  

> 📝 *You technically can use AnimeJaNai and Anime4K together, but that’s ilegal. Don’t.*

### ⚙️ Additional Notes

- Saving the current **volume level** for the next session is disabled by default.  
  → To enable it, open `mpvnet.conf` and change `remember-volume=no` to `yes`.  

- The **“watch later”** feature is disabled by default.  
  → To enable it, open `mpv.conf`, change `resume-playback=no` to `yes` and uncomment `watch-later-options=start`.

- Some buttons in the interface have **dual functions**:  
  → **Right Click** = primary action  
  → **Left Click** = alternate action

- Audio and subtitle tracks will load automatically in this order, regardless of their position (you can change it in `mpv.conf`):  
  → **Audio:** `Japanese`, `English`, `Spanish`, etc.  
  → **Subtitles:** `Spanish`, `Latin Spanish`, `English`, etc.

- You may want to change the language (of just few words) from `Spanish` to `English`:
   → Go to `script-opts/modernx.conf` and add/change `language=es` to `en`.

<div align="center">

## ☕ **SUPPORT MY WORK**

> If you like my work and want to say thank you, you can buy me a coffee :D\
> [![ko-fi](https://ko-fi.com/img/githubbutton_sm.svg)](https://ko-fi.com/elgamereduard)

---

<div align="center">

### 🇪🇸 MADE IN (S)PAIN 🇪🇸

</div>
