# Era para Obsidian

**Versión 1.0.0.** Cuadernos con páginas para dibujar, escribir y trabajar con imágenes, textos y PDFs dentro de Obsidian.

Este repositorio distribuye el plugin compilado, listo para instalar.

[Descargar Era 1.0.0](https://github.com/daisel10/era-obsidian/releases/download/1.0.0/era-1.0.0.zip) · [Notas de versión](https://github.com/daisel10/era-obsidian/releases/tag/1.0.0)

## Instalar con BRAT

Requiere Obsidian **1.8.7 o posterior** y los plugins de la comunidad habilitados.

1. Abre **Configuración → Plugins de la comunidad → Explorar** en Obsidian.
2. Busca **BRAT**, instálalo y actívalo.
3. Abre la paleta de comandos con **Ctrl + P** (**Cmd + P** en macOS).
4. Ejecuta **BRAT: Add a beta plugin for testing**.
5. Pega `https://github.com/daisel10/era-obsidian`.
6. Selecciona `1.0.0` o la última versión y pulsa **Add Plugin**.
7. Activa **Era** en Plugins de la comunidad si todavía no está activado.

Para actualizar una instalación existente, busca actualizaciones desde BRAT. Si fijaste Era a una versión anterior, selecciona `1.0.0` o la última disponible. El comando de BRAT conserva la palabra «beta» aunque esta publicación es una versión normal.

## Empezar a usar Era

1. Ejecuta **Era: Crear cuaderno** desde la paleta de comandos, o pulsa el icono del lápiz.
2. Dibuja en el Lienzo. La Rueda de herramientas ofrece tres pinceles con propiedades independientes, Seleccionar, Borrador y «+» para texto/referencias.
3. Pulsa de nuevo el pincel activo para abrir la biblioteca. El color central abre COPIC, HSL, RGB, favoritos y cuentagotas.
4. Añade páginas con **+ Página** en el Panel lateral y usa **Recursos** para incorporar PDFs, imágenes y textos.
5. Abre un PDF en el lector ampliado para trabajar con sus favoritos, anotaciones, miniaturas e historial.
6. Los cambios del cuaderno se guardan automáticamente; **Guardar cuaderno** fuerza el guardado.

Para volver a un cuaderno, abre su archivo `.era` desde Obsidian o ejecuta **Era: Abrir cuaderno**.

## Novedades de 1.0.0

- Rueda de tres pinceles independientes y ajustes con vista previa del motor.
- Selector radial COPIC/HSL/RGB, colores favoritos y cuentagotas.
- Lector PDF con favoritos, propiedades, miniaturas, selección de texto y navegación; preferencias separadas del Lienzo e historial de anotaciones.
- Mejoramiento de letra con Mi letra y cuatro estilos manuscritos, intensidad configurable y originales recuperables.
- Selector del Vault integrado en Recursos, uso táctil y acceso al Panel lateral en expansión.
- Refinamientos de disposición y comportamiento de herramientas y controles.

El reconocimiento de palabras funciona localmente en Obsidian para Windows y necesita el componente de escritura a mano del idioma elegido, español o inglés. La validación de móvil y lápices físicos sigue en curso.

Los cuadernos anteriores se siguen abriendo. Las funciones recientes de letra y bloqueo requieren una versión actualizada de Era en todos los equipos que abran esos cuadernos.

## Instalación manual

Descarga el ZIP de la publicación, extrae su carpeta `era` en `<vault>/.obsidian/plugins/`, recarga Obsidian y activa Era. Para actualizar, sustituye los archivos del plugin y conserva los cuadernos y la configuración. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

## Distribución y soporte

Era todavía no está en el catálogo oficial de plugins de Obsidian. Se instala mediante BRAT o la descarga manual.

El motor WebAssembly y las dependencias de ejecución están incluidos en el plugin. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Comunica problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Era y Obsidian, sistema operativo y pasos para reproducirlos.
