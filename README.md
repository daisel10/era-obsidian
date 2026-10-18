# Era para Obsidian

**Versión 1.6.4.** Cuadernos con páginas para dibujar, escribir y trabajar con imágenes, textos y PDFs dentro de Obsidian.

Este repositorio distribuye el plugin compilado, listo para instalar.

[Descargar Era 1.6.4](https://github.com/daisel10/era-obsidian/releases/download/1.6.4/era-1.6.4.zip) · [Notas de versión](https://github.com/daisel10/era-obsidian/releases/tag/1.6.4)

## Installation

Requires **Obsidian 1.8.7 or later**. Desktop and mobile loading are enabled; physical mobile-device validation is still pending. Windows Ink is limited to Windows desktop. Era is currently installed through BRAT or manually while community-directory review is pending.

For the complete plugin, including local equation recognition:

1. Download [era-1.6.4.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.4/era-1.6.4.zip).
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

Era selects a handwriting provider by its actual availability and page language. Windows Ink has priority on Windows; a browser handwriting provider is an alternative only when the hosting browser exposes its API and supports the language. If no provider works, the ink is preserved and the reason is shown. No new Era-operated remote recognition service is added.

On Windows, handwriting recognition starts a local Windows PowerShell process through `node:child_process`, using a fixed bundled Windows Ink script. Stroke coordinates and the selected language are sent as JSON through standard input, rather than inserted into a shell command. This process capability is disclosed for review; the automatic shell-execution warning may remain.

The author retains Windows Ink word recognition and discloses its process capability. See the [historical review response for release 1.6.0](REVIEW-RESPONSE.md), including the exact bundle hash, the inspected Angular split/join expression and the restrictive-license assessment.

Angular also formats version-specific documentation links. The inspected split/join pattern parses Angular's version number. These observations and the limits of the domain-warning investigation are documented in [Review notes](REVIEW-NOTES.md).

## Instalar con BRAT

Requiere Obsidian **1.8.7 o posterior** y los plugins de la comunidad habilitados. La carga está habilitada en escritorio y móvil; la validación física de móvil sigue pendiente.

1. Abre **Configuración → Plugins de la comunidad → Explorar** en Obsidian.
2. Busca **BRAT**, instálalo y actívalo.
3. Abre la paleta de comandos con **Ctrl + P** (**Cmd + P** en macOS).
4. Ejecuta **BRAT: Add a beta plugin for testing**.
5. Pega `https://github.com/daisel10/era-obsidian`.
6. Selecciona `1.6.4` o la última versión y pulsa **Add Plugin**.
7. Para usar el reconocimiento de ecuaciones, descarga también el ZIP completo de esta versión y copia su carpeta `equations/` dentro de `<vault>/.obsidian/plugins/era/`. BRAT no instala esa carpeta.
8. Recarga Obsidian y activa **Era** en Plugins de la comunidad si todavía no está activado.

Para actualizar una instalación existente, busca actualizaciones desde BRAT y sustituye también `equations/` por la carpeta del ZIP de la misma versión. Si fijaste Era a una versión anterior, selecciona `1.6.4` o la última disponible. El comando de BRAT conserva la palabra «beta» aunque esta publicación es una versión normal.

## Empezar a usar Era

1. Ejecuta **Era: Crear cuaderno** desde la paleta de comandos, o pulsa el icono del lápiz.
2. Dibuja en el Lienzo. La Rueda de herramientas ofrece tres pinceles con propiedades independientes, Seleccionar, Borrador y «+» para texto/referencias.
3. Pulsa de nuevo el pincel activo para abrir la biblioteca. El color central abre COPIC, HSL, RGB, favoritos y cuentagotas.
4. Añade páginas con **+ Página** en el Panel lateral y usa **Recursos** para incorporar PDFs, imágenes y textos.
5. Abre un PDF en el lector ampliado para trabajar con sus favoritos, anotaciones, miniaturas e historial.
6. Los cambios del cuaderno se guardan automáticamente; **Guardar cuaderno** fuerza el guardado.

Para volver a un cuaderno, abre su archivo `.era` desde Obsidian o ejecuta **Era: Abrir cuaderno**.

## Novedades de 1.6.4

- Borrado con botón del lápiz y tachado de palabras convertidas, con recuperación de contactos y correcciones para pinceles exóticos.
- Lecturas alternativas y palabras manuscritas tipografiadas sin saltos automáticos de línea.
- Reintentos de guardado, recuperación estable por cuaderno y protección ante ecos o recargas de sincronización externa.
- Copiar texto, imágenes, regiones PDF y selecciones mixtas; mantener el lápiz quieto dos segundos abre pegado sin tinta accidental.
- Carga habilitada en móvil, con Windows Ink limitado a escritorio Windows. La validación física con iPad/Android y sincronización real sigue pendiente.

## Escritura incorporada en 1.6.4

- Estilos de escritura ampliados en Redondas y Pegadas, con nuevas fuentes incluidas y sus licencias.
- Bloques de escritura recuperables y mejoras de transcripción, presentación y exportación.
- Selección de reconocedores según disponibilidad e idioma, conservando Windows Ink y usando la API web como alternativa cuando existe y admite el idioma.
- Mejoras de lectura de fórmulas, notación y vistas previas de escritura.

Las nuevas fuentes requieren formato `.era` v19 y los bloques de escritura requieren v20. Los equipos que abran cuadernos con estas funciones necesitan Era 1.6.4 o posterior. Si no hay un reconocedor disponible, la tinta se conserva; Mi letra continúa funcionando. La alternativa web no está disponible en todos los dispositivos. La carga en móvil está habilitada, pero no se integra ML Kit ni se garantiza la API web en todos los dispositivos.

## Mejoras conservadas de 1.6.2

- Exploración de carpetas del Vault, navegación por ruta y búsqueda por nombre o carpeta sin distinguir tildes ni mayúsculas.
- Más resultados para carpetas con más de 100 archivos y retorno a la carpeta explorada al salir de la búsqueda.
- Volver a vincular PDFs desde el Vault o desde el equipo, validando la copia antes de importarla y conservando las referencias del cuaderno.

## Mejoras conservadas de 1.6.1

- Renombrado de recursos en el Vault y actualización de referencias en cuadernos abiertos y cerrados, conservando los nombres personalizados de capas.
- Conexiones que conservan los lados elegidos al arrastrar y acompañan a los objetos al moverlos o cambiar su tamaño.
- Favoritos compactos con etiquetas y giro; paletas y controles adaptados al borde de la Rueda de herramientas.
- Navegación del Lienzo con trackpad: desplazamiento con dos dedos y zoom alrededor del cursor, conservando el desplazamiento normal de paneles y campos.

Al guardar conexiones con lados explícitos, el cuaderno usa formato `.era` v18 y requiere Era 1.6.1 o posterior en los equipos que lo abran. Abrir conexiones anteriores no cambia su formato automáticamente.

## Mejoras conservadas de 1.6.0

- Integración del tema de Obsidian conservada durante el montaje del editor.
- Colores de texto explícitos en los menús de Capas, cambiar capa y pegar; fondo, texto y borde del tema en los campos de Capas.
- Selectores CSS de integración actualizados a la clase `.era-editor`, con comprobación de regresión sobre el plugin compilado.

## Funciones incorporadas en 1.5.0

- Reconocimiento local de ecuaciones manuscritas a LaTeX y contornos vectoriales, con edición, reintento y recuperación de los trazos originales.
- Conexiones persistentes entre trazos, ayudas de escritura y refinamientos de la Rueda de herramientas, colores y controles táctiles.
- Herramientas PDF ampliadas: borrador configurable, texto, comentarios, páginas y lectura al ancho.
- Diccionario inglés/español sin conexión, con traducciones, sentidos, definiciones y sinónimos.
- Estudio opcional con importación/exportación de mazos Anki, tarjetas desde el Lienzo, repasos FSRS y metas diarias o semanales.

Se conservan la licencia de uso gratuito y el saneamiento de HTML publicados en 1.0.1. La distribución permite cargar en móvil con Windows Ink limitado a escritorio Windows. Las pruebas simuladas no certifican los dispositivos físicos iOS/Android.

La aprobación en el directorio sigue pendiente. La revisión automática de 1.0.1 mostrada el 17 de octubre de 2026 no pudo completarse y señala que un administrador la investigará. Esta publicación no implica que Era haya sido aprobada por Obsidian.

## Funciones incluidas

- Rueda de tres pinceles independientes y ajustes con vista previa del motor.
- Selector radial COPIC/HSL/RGB, colores favoritos y cuentagotas.
- Lector PDF con favoritos, propiedades, miniaturas, selección de texto y navegación; preferencias separadas del Lienzo e historial de anotaciones.
- Mejoramiento de letra con Mi letra y cuatro estilos manuscritos, intensidad configurable y originales recuperables.
- Selector del Vault integrado en Recursos, uso táctil y acceso al Panel lateral en expansión.
- Refinamientos de disposición y comportamiento de herramientas y controles.

Windows Ink reconoce palabras localmente en Obsidian para Windows y necesita el componente de escritura a mano del idioma elegido, español o inglés. La alternativa web solo se ofrece si el navegador expone la API y admite el idioma; no se promete su disponibilidad en un dispositivo concreto. La validación con lápices físicos y dispositivos móviles sigue en curso.

Los cuadernos anteriores se siguen abriendo. Las funciones recientes de letra y bloqueo requieren una versión actualizada de Era en todos los equipos que abran esos cuadernos.

## Instalación manual

Descarga [era-1.6.4.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.4/era-1.6.4.zip), desactiva Era si ya está abierto y copia la carpeta `era` **completa, incluida `equations/`**, en `<vault>/.obsidian/plugins/`. Recarga Obsidian y activa Era. Para actualizar, combina la carpeta y sustituye los archivos distribuidos; conserva `data.json`, tus cuadernos y los datos de Estudio. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

No descargues los archivos «Source code» que GitHub genera automáticamente. Usa el ZIP `era-1.6.4.zip` de los archivos adjuntos de la publicación.

## Licencia, privacidad y acceso

Era se ofrece para uso gratuito personal, educativo y profesional. No requiere pagos ni una cuenta propia de Era. La [licencia de uso gratuito](LICENSE) permite instalar, utilizar y conservar copias de respaldo; el autor conserva los derechos de modificación y redistribución del código y del compilado de Era. Los componentes de terceros mantienen sus propias licencias y los derechos que estas conceden.

El código fuente original se conserva en un repositorio privado. La revisión por Obsidian podrá realizarse mediante la vía de repositorio privado de la aplicación GitHub del directorio de la comunidad. Esta publicación distribuye el compilado; no afirma que Era sea un producto creado o aprobado por el equipo de Obsidian.

**Red.** El dibujo, los cuadernos, la renderización de PDFs y Windows Ink funcionan localmente. Al pegar un enlace y pedir una vista previa, Era consulta la página HTTP/HTTPS indicada para obtener título y descripción. Al importar un recurso mediante un enlace, descarga el archivo de esa dirección. Las solicitudes van al servidor de la dirección elegida, que recibe la solicitud de red habitual. No se utiliza un servicio remoto de reconocimiento de escritura ni se envían los cuadernos para estas funciones. Pegar solo texto o enlace evita solicitar la vista previa.

**Archivos y portapapeles.** Era lee y guarda cuadernos y recursos dentro del Vault y puede modificar los PDFs que anotas. Conserva copias previas de los PDFs en `.era/pdf-backups/`. Puedes seleccionar archivos del equipo desde el selector del sistema para importarlos al Vault, y exportar dibujos mediante la descarga elegida. El acceso al portapapeles se usa al ejecutar las acciones de copiar o pegar. No se escanean carpetas externas al Vault.

**Almacenamiento local.** Estudio guarda sus mazos, multimedia y repasos en `Era/Estudio/`, dentro del Vault; su sincronización depende del mecanismo del Vault. Las preferencias de herramientas y colores se guardan localmente. Si falla el guardado de un cuaderno, se conserva una recuperación estable por cuaderno en el almacenamiento local; si ese almacén falla, se intenta `.era/recovery/` dentro del Vault. El comando de recuperación permite abrir las copias conservadas. Estas copias no se sincronizan automáticamente.

La versión 1.6.4 no incorpora telemetría ni anuncios. En Windows, el reconocimiento de palabras utiliza un proceso local de Windows Ink y los componentes de escritura a mano instalados para español o inglés. No descarga ni instala esos componentes.

## Distribución y soporte

Era todavía no está en el catálogo oficial de plugins de Obsidian. Se instala mediante BRAT o la descarga manual.

El motor WebAssembly está incluido en `main.js`. Los modelos y el runtime de reconocimiento matemático se incluyen en `equations/` dentro del ZIP completo; no se descargan durante el reconocimiento. Estudio incluye su SQLite/WASM en el bundle y no se conecta a AnkiWeb. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Comunica problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Era y Obsidian, sistema operativo y pasos para reproducirlos.
