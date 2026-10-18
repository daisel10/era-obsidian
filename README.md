# Era para Obsidian

**Versión 1.6.0.** Cuadernos con páginas para dibujar, escribir y trabajar con imágenes, textos y PDFs dentro de Obsidian.

Este repositorio distribuye el plugin compilado, listo para instalar.

[Descargar Era 1.6.0](https://github.com/daisel10/era-obsidian/releases/download/1.6.0/era-1.6.0.zip) · [Notas de versión](https://github.com/daisel10/era-obsidian/releases/tag/1.6.0)

## Installation

Requires **Obsidian 1.8.7 or later on desktop**. Era is currently installed through BRAT or manually while community-directory review is pending.

For the complete plugin, including local equation recognition:

1. Download [era-1.6.0.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.0/era-1.6.0.zip).
2. Disable Era if it is already running, then extract the ZIP's `era` folder into `<vault>/.obsidian/plugins/`.
3. Copy the entire folder, including `equations/`. When updating, merge/replace the distributed files and preserve `data.json` and notebook files.
4. Reload Obsidian and enable Era in **Settings → Community plugins**. Use your vault's configuration folder if it differs from `.obsidian`.

**BRAT:** add `https://github.com/daisel10/era-obsidian` using **BRAT: Add a beta plugin for testing**, or check for updates if already installed. BRAT installs the main plugin files; local equation recognition additionally requires the matching `equations/` folder from the complete ZIP. Copy it after installing/updating, then reload Obsidian. A ZIP-only installation is sufficient; BRAT is optional.

## Usage

1. Run **Era: Crear cuaderno** from Obsidian's command palette, or click the pencil ribbon icon.
2. Draw on the canvas. The tool wheel provides three independent brush presets, selection, eraser and the **+** menu for text and references.
3. Add notebook pages with **+ Página** in the sidebar. Use **Recursos** to import PDFs, images and text files.
4. Open a PDF in the expanded reader to annotate it and navigate its pages.
5. For handwritten formulas, enable the mathematics option in handwriting settings; it uses the locally installed `equations/` files.
6. Run **Era: Abrir Estudio** to import Anki `.apkg` decks, create cards and review with daily goals. Estudio can be disabled in Era settings.
7. Notebook changes are saved automatically; **Guardar cuaderno** forces a save.

Open an existing `.era` file from Obsidian or run **Era: Abrir cuaderno** to return to a notebook.

## License

Era uses a **custom free-use license**: personal, educational and professional use and backup copies are permitted; modification and redistribution rights for Era remain with the author. See the authoritative [LICENSE](LICENSE) and its [plain-language explanation](LICENSE-EXPLAINED.md). Third-party components retain their own license terms. A custom license may continue to appear as unrecognized in GitHub's automated license detection.

Era's source repository is private and can be provided through Obsidian's private-source review process. Catalogue approval is still pending.

## Network and process disclosures

Web previews and linked-resource imports contact the HTTP/HTTPS URL explicitly supplied by the user. Drawing, notebook storage, PDF processing and handwriting recognition run locally. Era does not include telemetry, ads or its own account requirement.

On Windows, handwriting recognition starts a local Windows PowerShell process through `node:child_process`, using a fixed bundled Windows Ink script. Stroke coordinates and the selected language are sent as JSON through standard input, rather than inserted into a shell command. This process capability is disclosed for review; the automatic shell-execution warning may remain.

Angular also formats version-specific documentation links. The inspected split/join pattern parses Angular's version number. These observations and the limits of the domain-warning investigation are documented in [Review notes](REVIEW-NOTES.md).

## Instalar con BRAT

Requiere Obsidian **1.8.7 o posterior para escritorio** y los plugins de la comunidad habilitados.

1. Abre **Configuración → Plugins de la comunidad → Explorar** en Obsidian.
2. Busca **BRAT**, instálalo y actívalo.
3. Abre la paleta de comandos con **Ctrl + P** (**Cmd + P** en macOS).
4. Ejecuta **BRAT: Add a beta plugin for testing**.
5. Pega `https://github.com/daisel10/era-obsidian`.
6. Selecciona `1.6.0` o la última versión y pulsa **Add Plugin**.
7. Para usar el reconocimiento de ecuaciones, descarga también el ZIP completo de esta versión y copia su carpeta `equations/` dentro de `<vault>/.obsidian/plugins/era/`. BRAT no instala esa carpeta.
8. Recarga Obsidian y activa **Era** en Plugins de la comunidad si todavía no está activado.

Para actualizar una instalación existente, busca actualizaciones desde BRAT y sustituye también `equations/` por la carpeta del ZIP de la misma versión. Si fijaste Era a una versión anterior, selecciona `1.6.0` o la última disponible. El comando de BRAT conserva la palabra «beta» aunque esta publicación es una versión normal.

## Empezar a usar Era

1. Ejecuta **Era: Crear cuaderno** desde la paleta de comandos, o pulsa el icono del lápiz.
2. Dibuja en el Lienzo. La Rueda de herramientas ofrece tres pinceles con propiedades independientes, Seleccionar, Borrador y «+» para texto/referencias.
3. Pulsa de nuevo el pincel activo para abrir la biblioteca. El color central abre COPIC, HSL, RGB, favoritos y cuentagotas.
4. Añade páginas con **+ Página** en el Panel lateral y usa **Recursos** para incorporar PDFs, imágenes y textos.
5. Abre un PDF en el lector ampliado para trabajar con sus favoritos, anotaciones, miniaturas e historial.
6. Los cambios del cuaderno se guardan automáticamente; **Guardar cuaderno** fuerza el guardado.

Para volver a un cuaderno, abre su archivo `.era` desde Obsidian o ejecuta **Era: Abrir cuaderno**.

## Novedades de 1.6.0

- Integración del tema de Obsidian conservada durante el montaje del editor.
- Colores de texto explícitos en los menús de Capas, cambiar capa y pegar; fondo, texto y borde del tema en los campos de Capas.
- Selectores CSS de integración actualizados a la clase `.era-editor`, con comprobación de regresión sobre el plugin compilado.

## Funciones incorporadas en 1.5.0

- Reconocimiento local de ecuaciones manuscritas a LaTeX y contornos vectoriales, con edición, reintento y recuperación de los trazos originales.
- Conexiones persistentes entre trazos, ayudas de escritura y refinamientos de la Rueda de herramientas, colores y controles táctiles.
- Herramientas PDF ampliadas: borrador configurable, texto, comentarios, páginas y lectura al ancho.
- Diccionario inglés/español sin conexión, con traducciones, sentidos, definiciones y sinónimos.
- Estudio opcional con importación/exportación de mazos Anki, tarjetas desde el Lienzo, repasos FSRS y metas diarias o semanales.

Se conservan la licencia de uso gratuito y el saneamiento de HTML publicados en 1.0.1. La distribución sigue declarada para escritorio. La adaptación de controles a pantallas pequeñas no implica compatibilidad validada con Obsidian móvil.

La aprobación en el directorio sigue pendiente. La revisión automática de 1.0.1 mostrada el 17 de octubre de 2026 no pudo completarse y señala que un administrador la investigará. Esta publicación no implica que Era haya sido aprobada por Obsidian.

## Funciones incluidas

- Rueda de tres pinceles independientes y ajustes con vista previa del motor.
- Selector radial COPIC/HSL/RGB, colores favoritos y cuentagotas.
- Lector PDF con favoritos, propiedades, miniaturas, selección de texto y navegación; preferencias separadas del Lienzo e historial de anotaciones.
- Mejoramiento de letra con Mi letra y cuatro estilos manuscritos, intensidad configurable y originales recuperables.
- Selector del Vault integrado en Recursos, uso táctil y acceso al Panel lateral en expansión.
- Refinamientos de disposición y comportamiento de herramientas y controles.

El reconocimiento de palabras funciona localmente en Obsidian para Windows y necesita el componente de escritura a mano del idioma elegido, español o inglés. Esta versión es para escritorio; la validación con lápices físicos sigue en curso.

Los cuadernos anteriores se siguen abriendo. Las funciones recientes de letra y bloqueo requieren una versión actualizada de Era en todos los equipos que abran esos cuadernos.

## Instalación manual

Descarga [era-1.6.0.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.0/era-1.6.0.zip), desactiva Era si ya está abierto y copia la carpeta `era` **completa, incluida `equations/`**, en `<vault>/.obsidian/plugins/`. Recarga Obsidian y activa Era. Para actualizar, combina la carpeta y sustituye los archivos distribuidos; conserva `data.json`, tus cuadernos y los datos de Estudio. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

No descargues los archivos «Source code» que GitHub genera automáticamente. Usa el ZIP `era-1.6.0.zip` de los archivos adjuntos de la publicación.

## Licencia, privacidad y acceso

Era se ofrece para uso gratuito personal, educativo y profesional. No requiere pagos ni una cuenta propia de Era. La [licencia de uso gratuito](LICENSE) permite instalar, utilizar y conservar copias de respaldo; el autor conserva los derechos de modificación y redistribución del código y del compilado de Era. Los componentes de terceros mantienen sus propias licencias y los derechos que estas conceden.

El código fuente original se conserva en un repositorio privado. La revisión por Obsidian podrá realizarse mediante la vía de repositorio privado de la aplicación GitHub del directorio de la comunidad. Esta publicación distribuye el compilado; no afirma que Era sea un producto creado o aprobado por el equipo de Obsidian.

**Red.** El dibujo, los cuadernos, la renderización de PDFs y Windows Ink funcionan localmente. Al pegar un enlace y pedir una vista previa, Era consulta la página HTTP/HTTPS indicada para obtener título y descripción. Al importar un recurso mediante un enlace, descarga el archivo de esa dirección. Las solicitudes van al servidor de la dirección elegida, que recibe la solicitud de red habitual. No se utiliza un servicio remoto de reconocimiento de escritura ni se envían los cuadernos para estas funciones. Pegar solo texto o enlace evita solicitar la vista previa.

**Archivos y portapapeles.** Era lee y guarda cuadernos y recursos dentro del Vault y puede modificar los PDFs que anotas. Conserva copias previas de los PDFs en `.era/pdf-backups/`. Puedes seleccionar archivos del equipo desde el selector del sistema para importarlos al Vault, y exportar dibujos mediante la descarga elegida. El acceso al portapapeles se usa al ejecutar acciones de pegado. No se escanean carpetas externas al Vault.

**Almacenamiento local.** Estudio guarda sus mazos, multimedia y repasos en `Era/Estudio/`, dentro del Vault; su sincronización depende del mecanismo del Vault. Las preferencias de herramientas y colores se guardan localmente. Si falla el guardado de un cuaderno, puede conservarse una copia de recuperación en el almacenamiento local de Obsidian; el comando de recuperación permite devolverla al Vault. Estas copias no se sincronizan automáticamente.

La versión 1.6.0 no incorpora telemetría ni anuncios. En Windows, el reconocimiento de palabras utiliza un proceso local de Windows Ink y los componentes de escritura a mano instalados para español o inglés. No descarga ni instala esos componentes.

## Distribución y soporte

Era todavía no está en el catálogo oficial de plugins de Obsidian. Se instala mediante BRAT o la descarga manual.

El motor WebAssembly está incluido en `main.js`. Los modelos y el runtime de reconocimiento matemático se incluyen en `equations/` dentro del ZIP completo; no se descargan durante el reconocimiento. Estudio incluye su SQLite/WASM en el bundle y no se conecta a AnkiWeb. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Comunica problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Era y Obsidian, sistema operativo y pasos para reproducirlos.
