# Era para Obsidian

**Versión 1.6.9.** Cuadernos para escribir, dibujar y trabajar con imágenes,
textos y PDF dentro de Obsidian. Este repositorio distribuye el plugin
compilado, listo para instalar.

[Descargar Era 1.6.9](https://github.com/daisel10/era-obsidian/releases/download/1.6.9/era-1.6.9.zip)
· [Notas de versión](https://github.com/daisel10/era-obsidian/releases/tag/1.6.9)

## Installation

Requires **Obsidian 1.8.7 or later**. Desktop and mobile loading are enabled;
physical mobile-device validation is still pending. Windows Ink is available
on Windows desktop. Community-directory approval is pending.

1. Save your notebook and disable Era before updating.
2. Download [era-1.6.9.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.9/era-1.6.9.zip).
3. Extract the complete `era` folder into `<vault>/.obsidian/plugins/`, including
   `equations/`. Merge and replace the distributed files while preserving
   `data.json`, notebooks and Study data. Use your vault's configuration folder
   if it differs from `.obsidian`.
4. Reload Obsidian and enable Era in **Settings → Community plugins**.

**BRAT:** add `https://github.com/daisel10/era-obsidian` through **BRAT: Add a beta
plugin for testing**, or check for updates. Select `1.6.9` if using a pinned
version. BRAT installs the main files; local equation recognition also needs
`equations/` from the complete ZIP of the same version. Copy that folder and
reload Obsidian. Manual ZIP installation is sufficient; BRAT is optional.

Use the attached `era-1.6.9.zip`, rather than GitHub's automatic “Source code”
archives.

## Usage

- Run **Era: Crear cuaderno**, or click the pencil ribbon icon. Open an existing
  `.era` file directly or use **Era: Abrir cuaderno**.
- Use the tool wheel to switch between three independent brush presets,
  selection and eraser. Use **+** or hold the pen still for two seconds to open
  paste actions.
- Add pages with **+ Página** and import PDFs, images and text through
  **Recursos**. Selected objects and PDF regions offer **Copiar**.
- Open PDFs from Resources or drag their name to dock them beside the canvas. Use the shared tool palette to write, select text and navigate.
- Enable mathematics in handwriting settings to recognize formulas using the
  locally installed `equations/` files.
- Use **Era: Abrir Estudio** for Anki imports, cards and FSRS review. Study is
  optional and can be disabled in Era settings.
- Notebook changes save automatically; **Guardar cuaderno** requests a save.

## Qué cambia en 1.6.9

- PDF dividido a izquierda, derecha, arriba o abajo arrastrando su nombre. Durante el movimiento aparecen zonas transparentes y una previsualización del espacio que ocupará; al soltar se acopla. El divisor ajusta el tamaño y Ampliar recupera la pantalla completa.
- Apertura directa desde Recursos en cualquiera de los cuatro lados, flotante o a pantalla completa. Los controles frecuentes de páginas, zoom, ajuste, índice, miniaturas, selección de texto, comentarios, lectura y extracción quedan accesibles fuera de los menús. Las barras estrechas conservan el desplazamiento con el scrollbar oculto.
- Rueda de herramientas compartida entre PDF y Lienzo en la vista dividida. El historial actúa sobre el último documento tocado y la tinta PDF conserva su guardado nativo. La Rueda se acopla arriba como una barra horizontal o al separador como un círculo; la guía de acoplamiento aparece durante el arrastre.
- Barra horizontal más pequeña, con herramientas principales e historial blanco sobre fondo oscuro. Una segunda barra fina reúne grosor, sensibilidad o suavizado, opacidad y tres colores rápidos personalizables. Marcador y flecha tienen accesos directos sin reemplazar los pinceles guardados.
- Panel de colores horizontal desplegado debajo de una línea, con bandas curvas y controles flotantes. Mantiene Favoritos, COPIC por familias, búsqueda, HSL/RGB con gradientes y valores exactos, cuentagotas y selección por toque y teclado. La rueda circular conserva su distribución.
- Zoom del PDF más fluido: agrupa los eventos por fotograma, conserva la imagen durante el gesto y refina su resolución después de una pausa, con un límite de píxeles por página.
- Con un PDF abierto, el primer contacto de los dedos y el cambio entre PDF y Lienzo empiezan en movimiento. Elegir explícitamente una herramienta permite usarla con los dedos hasta cambiar de superficie. El lápiz conserva su herramienta sin este reinicio.


## Escritura, dibujo y portapapeles

- Catorce fuentes de escritura incluidas, agrupadas en Redondas y Pegadas,
  además de **Mi letra** para conservar la tinta original.
- Bloques de escritura editables y recuperables, lecturas alternativas y
  palabras como «Patrick» en una sola línea con Patrick Hand y Kalam.
- Reconocedor elegido por disponibilidad e idioma: Windows Ink en Windows y
  la API web como alternativa cuando el navegador la expone y admite el idioma.
  Si no hay un reconocedor disponible, la tinta se conserva. ML Kit no está
  integrado.
- Fórmulas recuperables con LaTeX, edición, reintento y reconocimiento local.
- Borrado con el botón lateral del lápiz, incluso después de dibujar con
  Confeti u otros pinceles exóticos; tachado para borrar palabras convertidas.
- **Copiar** conserva texto como texto, imágenes y PDF como PNG y selecciones
  mixtas como una imagen. Las fórmulas reconocidas se copian como LaTeX.
- Mantener la punta quieta durante dos segundos abre el menú de pegado junto al
  punto, sin dejar tinta accidental. **Pegar** incorpora referencias;
  **Pegar solo texto o enlace** solicita texto.

## Instalar y empezar

1. Guarda el cuaderno y desactiva Era antes de actualizar.
2. Descarga [era-1.6.9.zip](https://github.com/daisel10/era-obsidian/releases/download/1.6.9/era-1.6.9.zip)
   y copia su carpeta `era` completa, incluida `equations/`, en
   `<vault>/.obsidian/plugins/`.
3. Combina y sustituye los archivos distribuidos; conserva `data.json`, los
   cuadernos y los datos de Estudio. Recarga Obsidian y activa Era.
4. Ejecuta **Era: Crear cuaderno**. La Rueda de herramientas ofrece pinceles,
   Seleccionar, Borrador y «+». El Panel lateral organiza las páginas.
5. Usa **Recursos** para incorporar PDF, imágenes y textos. Pulsa de nuevo el
   pincel activo para abrir la biblioteca de pinceles.

También puedes instalar con BRAT desde la paleta de comandos: **BRAT: Add a beta
plugin for testing** → `https://github.com/daisel10/era-obsidian` → `1.6.9`.
Para ecuaciones, añade `equations/` del ZIP completo de la misma versión;
BRAT no instala esa carpeta. Después, recarga Obsidian.

## Compatibilidad y funciones conservadas

Se requiere **Obsidian 1.8.7 o posterior**. Las nuevas fuentes utilizan `.era`
v19 y los bloques recuperables v20, compatibles con Era 1.6.4 y posteriores.
Los cuadernos anteriores se siguen abriendo. Actualiza Era en los equipos que
abran cuadernos con estas funciones.

Se conservan el lector PDF con anotaciones e historial, las conexiones entre
objetos y trazos, las paletas COPIC/HSL/RGB, los favoritos y el cuentagotas, la
navegación con trackpad, la exploración del Vault y el renombrado y revinculado
de recursos. Estudio incluye mazos Anki, tarjetas y repasos FSRS. El diccionario
inglés/español funciona sin conexión.

La carga está habilitada en escritorio y móvil. La comprobación física de
lápices, iPad/Android y servicios reales de sincronización sigue pendiente;
las pruebas automatizadas no certifican esos entornos. La API web no está
disponible en todos los dispositivos.

## Guardado y recuperación

Era reintenta el guardado y detecta cambios externos para evitar sobrescribirlos.
Si falla, conserva una recuperación estable por cuaderno en el almacenamiento
local de Obsidian. Si ese almacenamiento falla, intenta `.era/recovery/` dentro
del Vault; solo usa un cuaderno visible de recuperación como último recurso.
**Era: Recuperar dibujos del almacenamiento local** permite abrir las copias
conservadas. Las copias del almacenamiento local no se sincronizan automáticamente.

## License

Era uses a **custom free-use license** for personal, educational and professional
use and backups. Modification and redistribution rights for Era remain with
the author. See the authoritative [LICENSE](LICENSE) and its
[plain-language explanation](LICENSE-EXPLAINED.md). Third-party components retain
their own terms. The original source repository is private and can be provided
through Obsidian's private-source review process. Directory approval is pending.

## Privacidad, red y archivos

Era no requiere una cuenta propia ni incorpora telemetría o anuncios. El dibujo,
los cuadernos, el procesamiento de PDF, Windows Ink y el reconocimiento de
fórmulas funcionan localmente. La alternativa web de escritura depende del
proveedor expuesto por el navegador; Era no añade un servicio remoto propio.

Las vistas previas de enlaces y las importaciones de recursos consultan la
dirección HTTP/HTTPS que el usuario indica. El servidor de esa dirección recibe
la solicitud habitual. **Pegar solo texto o enlace** evita solicitar la vista
previa.

Era lee y guarda cuadernos y recursos dentro del Vault y puede modificar los PDF
que anotas. Conserva copias previas de los PDF en `.era/pdf-backups/`. Los archivos
del equipo se incorporan mediante el selector del sistema y las exportaciones
se guardan en el destino elegido. No se escanean carpetas externas al Vault.
El portapapeles se utiliza al ejecutar copiar o pegar.

Estudio guarda sus mazos, multimedia y repasos en `Era/Estudio/`, dentro del Vault;
su sincronización depende del mecanismo del Vault. Las preferencias de herramientas
y colores se guardan localmente. Los dibujos y recursos conservan la estructura
de archivos del Vault.

## Network and process disclosures

On Windows desktop, word recognition starts a local Windows PowerShell process
through `node:child_process`, using a fixed bundled Windows Ink script. Stroke
coordinates and language are JSON on standard input, rather than interpolated
shell commands. The process uses installed Spanish/English handwriting components;
Era does not install them. The process capability remains disclosed for review.

User-requested link previews and linked-resource imports contact the supplied
HTTP/HTTPS URL. Local drawing, PDF processing and equation recognition do not
require an Era recognition server. Browser handwriting availability depends on
the host and supported language.

[Review notes](REVIEW-NOTES.md) document the current source reference and validation.
The [review response for 1.6.0](REVIEW-RESPONSE.md) retains historical bundle hashes,
Angular expression evidence and process/license analysis. Those observations do
not assert that later releases cleared scanner warnings or received directory
approval.

## Distribución y soporte

El motor WebAssembly y las fuentes están incorporados en `main.js`. El ZIP incluye
los modelos de ecuaciones, su runtime y licencias en `equations/`; no se descargan
al reconocer fórmulas. [Avisos de terceros](THIRD_PARTY_NOTICES.txt).

Era todavía no está en el catálogo oficial. Usa BRAT o el ZIP completo para
instalar y [abre un issue](https://github.com/daisel10/era-obsidian/issues) para
informar un problema. Incluye la versión, el dispositivo y los pasos para repetirlo.
