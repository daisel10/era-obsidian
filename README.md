# Era para Obsidian

Cuadernos con páginas para dibujar, escribir y trabajar con imágenes y PDFs dentro de Obsidian.

Este repositorio distribuye el plugin compilado. No necesitas instalar herramientas de desarrollo ni compilarlo.

## Instalar con BRAT

Requiere Obsidian **1.8.7 o posterior** y los plugins de la comunidad habilitados.

1. En Obsidian, abre **Configuración → Plugins de la comunidad → Explorar**.
2. Busca **BRAT**, instálalo y actívalo.
3. Abre la paleta de comandos con **Ctrl + P** (o **Cmd + P** en macOS).
4. Ejecuta **BRAT: Add a beta plugin for testing**.
5. Pega `https://github.com/daisel10/era-obsidian`.
6. Selecciona la última versión disponible y pulsa **Add Plugin**.
7. Activa **Era** en **Configuración → Plugins de la comunidad**, si todavía no está activado.

Para actualizar Era, usa las opciones de actualización de BRAT.

## Empezar a usar Era

1. Abre la paleta de comandos y ejecuta **Era: Crear cuaderno**, o pulsa el icono del lápiz.
2. Dibuja en el Lienzo y elige herramientas, colores y grosor en la Rueda de herramientas.
3. Añade páginas desde **+ Página** en el Panel lateral.
4. Usa **Recursos** para incorporar PDFs, imágenes o textos al cuaderno.
5. Los cambios se guardan automáticamente. También puedes usar **Guardar cuaderno**.

Para volver a un cuaderno, abre su archivo `.era` desde el explorador de Obsidian o ejecuta **Era: Abrir cuaderno**.

## Descarga e instalación manual

[Descargar Era 0.1.1](https://github.com/daisel10/era-obsidian/releases/download/0.1.1/era-0.1.1.zip) · [Ver versiones](https://github.com/daisel10/era-obsidian/releases)

Si prefieres instalarlo manualmente, extrae el ZIP y coloca la carpeta `era` dentro de `<vault>/.obsidian/plugins/`. Recarga Obsidian y activa Era en Plugins de la comunidad. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

## Novedades de 0.1.1

- Más herramientas de tinta y mejoras de fluidez al dibujar en páginas con muchos trazos.
- Figuras regulares al dibujar y mantener el lápiz quieto durante medio segundo.
- Mejoramiento de letra con cinco perfiles, incluyendo Cursiva redonda, y recuperación de los trazos originales.
- Idioma de escritura español o inglés por página o cuaderno. El reconocimiento de palabras funciona localmente en Obsidian para Windows y requiere el componente de escritura a mano del idioma elegido.
- Borrado de tinta mediante un garabato de tachado, configurable en los gestos.
- Pegado de referencias, enlaces con vistas previas, imágenes y PDFs.
- Rueda de herramientas con agarre para moverla también en selección y en el lector PDF; acciones cerca de la selección, bloqueo individual de trazos y capas más claras.

Los cuadernos anteriores se siguen abriendo. Los estilos de letra, el idioma inglés y los bloqueos individuales pueden utilizar los formatos v14/v15: los equipos que abran esos cuadernos también necesitan esta actualización.

## Estado de esta versión

**0.1.1 es una beta para pruebas**, todavía fuera del catálogo oficial de plugins de Obsidian. La experiencia en móvil y con lápices físicos sigue en validación.

El motor WebAssembly y las dependencias de ejecución están incluidos en el plugin. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Puedes comunicar problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Obsidian, sistema operativo y pasos para reproducirlos.
