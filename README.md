# Era para Obsidian

**Versión 1.0.1.** Cuadernos con páginas para dibujar, escribir y trabajar con imágenes, textos y PDFs dentro de Obsidian.

Este repositorio distribuye el plugin compilado, listo para instalar.

[Descargar Era 1.0.1](https://github.com/daisel10/era-obsidian/releases/download/1.0.1/era-1.0.1.zip) · [Notas de versión](https://github.com/daisel10/era-obsidian/releases/tag/1.0.1)

## Instalar con BRAT

Requiere Obsidian **1.8.7 o posterior para escritorio** y los plugins de la comunidad habilitados.

1. Abre **Configuración → Plugins de la comunidad → Explorar** en Obsidian.
2. Busca **BRAT**, instálalo y actívalo.
3. Abre la paleta de comandos con **Ctrl + P** (**Cmd + P** en macOS).
4. Ejecuta **BRAT: Add a beta plugin for testing**.
5. Pega `https://github.com/daisel10/era-obsidian`.
6. Selecciona `1.0.1` o la última versión y pulsa **Add Plugin**.
7. Activa **Era** en Plugins de la comunidad si todavía no está activado.

Para actualizar una instalación existente, busca actualizaciones desde BRAT. Si fijaste Era a una versión anterior, selecciona `1.0.1` o la última disponible. El comando de BRAT conserva la palabra «beta» aunque esta publicación es una versión normal.

## Empezar a usar Era

1. Ejecuta **Era: Crear cuaderno** desde la paleta de comandos, o pulsa el icono del lápiz.
2. Dibuja en el Lienzo. La Rueda de herramientas ofrece tres pinceles con propiedades independientes, Seleccionar, Borrador y «+» para texto/referencias.
3. Pulsa de nuevo el pincel activo para abrir la biblioteca. El color central abre COPIC, HSL, RGB, favoritos y cuentagotas.
4. Añade páginas con **+ Página** en el Panel lateral y usa **Recursos** para incorporar PDFs, imágenes y textos.
5. Abre un PDF en el lector ampliado para trabajar con sus favoritos, anotaciones, miniaturas e historial.
6. Los cambios del cuaderno se guardan automáticamente; **Guardar cuaderno** fuerza el guardado.

Para volver a un cuaderno, abre su archivo `.era` desde Obsidian o ejecuta **Era: Abrir cuaderno**.

## Preparación del catálogo en 1.0.1

- El HTML del portapapeles y de los metadatos de enlaces se sanea antes de procesarlo.
- La exportación construye los elementos del documento de forma explícita y sanea su contenido.
- La distribución incluye la licencia de uso gratuito y los avisos de terceros, también dentro del plugin.
- Se declara compatibilidad de escritorio por el uso de Node.js en Windows Ink. Móvil queda fuera de esta publicación.

La solicitud al directorio sigue pendiente de envío y revisión. Esta actualización no implica que Era haya sido aprobada por Obsidian.

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

Descarga el ZIP de la publicación, extrae su carpeta `era` en `<vault>/.obsidian/plugins/`, recarga Obsidian y activa Era. Para actualizar, sustituye los archivos del plugin y conserva los cuadernos y la configuración. Si tu vault usa otra carpeta de configuración, úsala en lugar de `.obsidian`.

## Licencia, privacidad y acceso

Era se ofrece para uso gratuito personal, educativo y profesional. No requiere pagos ni una cuenta propia de Era. La [licencia de uso gratuito](LICENSE) permite instalar, utilizar y conservar copias de respaldo; el autor conserva los derechos de modificación y redistribución del código y del compilado de Era. Los componentes de terceros mantienen sus propias licencias y los derechos que estas conceden.

El código fuente original se conserva en un repositorio privado. La revisión por Obsidian podrá realizarse mediante la vía de repositorio privado de la aplicación GitHub del directorio de la comunidad. Esta publicación distribuye el compilado; no afirma que Era sea un producto creado o aprobado por el equipo de Obsidian.

**Red.** El dibujo, los cuadernos, la renderización de PDFs y Windows Ink funcionan localmente. Al pegar un enlace y pedir una vista previa, Era consulta la página HTTP/HTTPS indicada para obtener título y descripción. Al importar un recurso mediante un enlace, descarga el archivo de esa dirección. Las solicitudes van al servidor de la dirección elegida, que recibe la solicitud de red habitual. No se utiliza un servicio remoto de reconocimiento de escritura ni se envían los cuadernos para estas funciones. Pegar solo texto o enlace evita solicitar la vista previa.

**Archivos y portapapeles.** Era lee y guarda cuadernos y recursos dentro del Vault y puede modificar los PDFs que anotas. Conserva copias previas de los PDFs en `.era/pdf-backups/`. Puedes seleccionar archivos del equipo desde el selector del sistema para importarlos al Vault, y exportar dibujos mediante la descarga elegida. El acceso al portapapeles se usa al ejecutar acciones de pegado. No se escanean carpetas externas al Vault.

**Almacenamiento local.** Las preferencias de herramientas y colores se guardan localmente. Si falla el guardado de un cuaderno, puede conservarse una copia de recuperación en el almacenamiento local de Obsidian; el comando de recuperación permite devolverla al Vault. Estas copias no se sincronizan automáticamente.

La versión 1.0.1 no incorpora telemetría ni anuncios. En Windows, el reconocimiento de palabras utiliza un proceso local de Windows Ink y los componentes de escritura a mano instalados para español o inglés. No descarga ni instala esos componentes.

## Distribución y soporte

Era todavía no está en el catálogo oficial de plugins de Obsidian. Se instala mediante BRAT o la descarga manual.

El motor WebAssembly y las dependencias de ejecución están incluidos en el plugin. Los avisos de terceros acompañan la distribución y están incorporados en `main.js`.

Comunica problemas desde [Issues](https://github.com/daisel10/era-obsidian/issues), indicando versión de Era y Obsidian, sistema operativo y pasos para reproducirlos.
