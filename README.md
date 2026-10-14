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

[Descargar Era 0.1.0](https://github.com/daisel10/era-obsidian/releases/download/0.1.0/era-0.1.0.zip) · [Ver versiones](https://github.com/daisel10/era-obsidian/releases)

Si prefieres instalarlo manualmente, extrae el ZIP y coloca la carpeta `era` dentro de `<vault>/.obsidian/plugins/`. Recarga Obsidian y activa Era en Plugins de la comunidad. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

## Estado de esta versión

**0.1.0 es una beta para pruebas**, todavía fuera del catálogo oficial de plugins de Obsidian. La experiencia en móvil y con lápices físicos sigue en validación.

El motor WebAssembly y las dependencias de ejecución están incluidos en el plugin. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Puedes comunicar problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Obsidian, sistema operativo y pasos para reproducirlos.
