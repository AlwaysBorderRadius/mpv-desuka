Archivo histórico, se conserva por historia; desde v1.2 ver Releases

## 🆕 Changelog (Pre-GitHub)

<details>
  <summary><strong>MPVNET DESUKA V1.2 - 4/10/2025</strong></summary>

- Añadida una keybind faltante de mi anterior mpv
</details>

<details>
  <summary><strong>MPVNET DESUKA V1.1 - 15/09/2025</strong></summary>

- Añadida compatibilidad con los bordes redondeados de w11
- Retocado diseño de los thumbnails
</details>

<details>
  <summary><strong>🆕 MPVNET DESUKA V1 (RELEASE) - 25/08/2025</strong></summary>

- MPVNET AnimeJaNai v3.2.0 (MPVNET v7.1.1.3-beta + AnimeJaNai V3 + VapourSynth R70 + etc)
- ModernX 0.4.3 (actualizado)
- Thumbfast Feb 4, 2025 (actualizado)
- Se ha añadido el shader de AnimeJaNai V2 (la version buena), el mejor oversharpener.
- Se ha migrado de mpv average a mpvnet.
- Se han migrado TODAS las modificaciones anteriores a este nuevo mpvnet.
- ModernX:
  - Añadido boton de screenshot.
  - Añadido boton de pinear ventana.
  - Nuevos iconos para los botones.
  - Nueva font.
  - Nuevos efectos de hover.
  - Nuevo diseño para los thumbnails.
  - Añadida descripcion del capitulo o peso del archivo (este ultimo esta deshabilitado).
  - Se ha añadido el nombre del chapter.
  - Se ha mejorado el tamaño de la interfaz, textos y mensajes.
  - Se ha arreglado el overlap ente Titulo y Descripcion.
  - Se ha arreglado sin querer (un poco) la estabilidad del mpvnet con animejanai funcionando al pasar de ventana a fullscreen y al reves. Ahora ya no crashea.
  - Se ha arreglado sin querer (un poco) la fluidez al avanzar/retroceder en el video cuando se usa el shader de animejanai.
  - Se ha traducido la interfaz de mpvnet al español.
- mpv.conf:
  - Se han fusionado mis cambios con los de AnimeJaNai.
  - Ahora se usa una GPU API y un proceso de renderizado mas eficiente.
  - Existe la funcion "Watch later" que guarda por donde has dejado el video, para continuar desde el punto donde lo dejaste, pero lo he deshabilitado por defecto.
- mpvnet.conf:
  - No guarda el volumen de la anterior sesion.
Nuevas keybinds importantes:
  - ctrl+right_click:           abre un menu contextual con todos los ajustes.
  - ctrl+E:                     abre el menu de animejanai.
  - ctrl+J:                     AnimeJaNai status.
  - C:                          abre el menu de mpvnet (porfa no toques nada o romperas el archivo de config 😭🙏🏻 y sera culpa tuya, no mia).
  - S:                          Toma captura de pantalla.
  - M:                          Mutea el video.
  - ctrl+1, ctrl+2, ctrl+3:     inicia animejanai v2.
  - shift+1, shift+2, shift+3:  inicia animejanai v3.
  - ctrl+0:                     quita animejanai.
  - 1 - 6:                      inicia anime4k.
  - 0:                          quita anime4k.
- DiscordRPC:
  - Se ha cambiado la key de On/Off a 'D'.
- Y seguramente mas cosas...
</details>

<details>
  <summary><strong>MPV v5.1</strong></summary>

- Varios fixes a las keybinds sobretodo.
- Vuelta a la version antigua del Autoload, carga lo que ha de cargar. La nueva no es configurable y se lo traga todo.
</details>

<details>
  <summary><strong>MPV v5</strong></summary>

- Versión de MPV: 64-bit V3 2024-08 (la V3 tiene mejor rendimiento con shaders, en teoría).
- Custom Config:
  - input.conf:
    - Eliminadas opciones peligrosas y configuradas combinaciones de teclas más seguras (a prueba de errores, evitando dañar el video accidentalmente al presionar una tecla incorrecta).
    - Añadidas más opciones útiles y simplificadas otras:
      - Avance por fotogramas.
      - Avance/retroceso de 5 segundos arreglado, ahora es exacto.
      - Los shaders de Anime4K son ahora más fáciles de usar.
      - Funciones para ajustar subtítulos y audios en caso de desincronización.
    - Compatibilidad con Linux
  - mpv.conf:
    - Mejora en la preferencia de idioma en subtítulos y audios.
    - Ajustado tiempo de escondido de la interfaz y raton.
    - Mejorado el estilo de los mensajes en pantalla.
    - Ajustes varios en el estilo de la ventana.
    - Opción para aumentar/disminuir el tamaño de los subtítulos (desactivada por defecto porque sobrescribe las fuentes de los subs).
	- Archivo bastante toqueteado, creo que he quitado cosas innecesarias, he reordenado y he actualizado un par de cosas como lo de vo=GPU-Next y profile=high-quality
- ModernX:
  - Ahora se utiliza una rama más reciente con más funciones.
  - Íconos redondeados.
  - Efectos hover en los botones.
  - Mejor degradado.
  - Opción para mover los subtítulos al salir la interfaz (desactivada por defecto, lo que he hecho yo es más cómodo).
  - Tamaño del título del archivo ajustado.
  - Ahora, los botones de avanzar/retroceder del ratón cambian de capítulo.
- ModernX personalizado:
  - Ahora se parece más a la versión anterior.
  - Lista subtítulos y audios al cambiar.
  - Estilos de los mensajes en pantalla ajustados (más agradables).
  - La interfaz (OSC) se desvanece en la pausa.
  - Arreglada la función de los botones centrales.
  - Efecto hover eliminado de elementos que no son botones.
- Thumbfast:
  - Se ha añadido Thumbfast a ModernX, ahora aparecerán miniaturas en la barra de tiempo como en YouTube.
- Autoload:
  - Nueva versión de Autoload.
</details>