# Review notes

## Current release: 1.6.13

Notebook naming is inline in the existing header surface, with matching typography and no confirm/cancel buttons. Enter and leaving the field commit the title, Escape cancels, and empty titles keep the previous name. Outside pointer contacts commit before the drawing input starts, so the first pen stroke is preserved.

The horizontal palette is placed below the header with a 12 px gap, including expanded/restored views and all four PDF dock positions. The dock hint follows that anchor. The initial circular wheel placement also respects the header; users can still move and dock it freely. The header no longer shifts below the tools when a PDF is docked.

Matching private source: tag `1.6.13` in `daisel10/era`, commit `cf2d8552c94ca600b4701c40589dc98c421205be`.
`main.js` SHA-256: `c5f2058b61586df7634a2c1df0c4c650adc094addebc51e61f00ee2bcb55370d`.

Validation: 235 UI and 110 plugin tests pass, plus five focused checks after the final title-input change. Angular/plugin compilation, both host type checks and formatting checks pass. Chrome at density 2 checks native Enter, leaving the title directly into a full pen stroke, toolbar/header separation at 1180 and 640 px in expanded/restored views, and all four dock positions. Existing PDF writing/erasing, COPIC scrolling and citation origin checks also pass with a controlled PDF backend. Physical iPad verification remains pending; prior Apple Pencil native-gesture limitations remain unchanged.

The complete ZIP contains 21 verified files, including existing recognition models, runtime and licenses. Notebook formats, Obsidian minimum 1.8.7 and recognition behavior are unchanged.

## Previous release: 1.6.12

The canvas tool wheel is now shared with the docked and expanded PDF reader. PDF-only drawing favorites and the separate text-selection shortcut have been removed; document actions, native ink, eraser properties and independent undo remain available. The selected brush, width, opacity and color apply to either surface. PDF pen input uses the shared input state machine, including pen priority, standard barrel buttons and physical erasers.

Horizontal COPIC is a scrollable rectangular palette grouped by color family. RGB/HSL arcs have additional spacing when there is room. Default quick colors are #000000, #2346b4 and #e90101 without overwriting saved choices. The notebook title is editable in the header and menu surfaces stay opaque on light or dark paper. Expanded writing hides only the recognition preview.

PDF citation origins navigate and highlight the current reader without requiring an inline card or changing the dock. Moving an inline PDF by its name preserves the host scroll position and canvas camera. One-millimeter grid settings remain valid in the engine; triangle/isometric geometry stays fixed in world coordinates across zoom and pan. Optional measurement snapping uses the same lattice.

Matching private source: tag `1.6.12` in `daisel10/era`, commit `58d4694536e5765ab242362e171e956c03300285`.
`main.js` SHA-256: `354836d07a50e50c7df9976761d200dc5ec3a375a0f29157e8fcb4a6a0be5bc0`.

Validation: 235 UI, 110 plugin and 14 native notebook-engine tests pass. WebAssembly was rebuilt; Angular/plugin builds, both host type checks and formatting checks pass. Chrome at density 2 uses native CDP pen input with the real editor and a controlled PDF backend to verify writing, barrel-button erasing and one shared wheel across left/right/top/bottom/full layouts, COPIC scrolling, menu surfaces and source references without inline cards. These tests do not certify physical iPad/Apple Pencil behavior.

Apple Pencil double tap and squeeze are not implemented. They require the native UIPencilInteraction interface, which this Obsidian plugin has no exposed bridge for. Existing standard pointer-button support must not be presented as support for those Apple hardware gestures.

The complete ZIP contains 21 verified files, including the existing recognition models, runtime and licenses. Notebook formats, Obsidian minimum 1.8.7, recognition privacy and native-provider priority remain unchanged. BRAT prepares missing recognition files with pinned URLs and SHA-256 verification. Handwriting remains experimental. No community-directory approval is claimed.

## Previous release: 1.6.11

Automatic touch navigation now shares pen detection between the canvas and PDF reader and across canvas reattachment. Choosing a brush no longer arms finger ink after pen use in Automatic mode; explicit Draw with finger remains available. Focus preserves the scroll offset of the embedding host.

Long ordinary pen and fountain-pen drafts repaint only changed pixels and cull segments outside that damage rectangle. Earlier ink crossing the rectangle is recomposited in its actual layer, preserving pressure and opacity. Camera, viewport size, density, style and guide changes invalidate reuse; art brushes retain full rendering.

Matching private source: tag `1.6.11` in `daisel10/era`, commit `0f28569b5e12371e8d8ae1ad1471bbcff3481867`.
`main.js` SHA-256: `7c289757411babae3d1e397c9e92598eb33bb7cd72d0bd61b6484d341fd1a4b9`.

Validation: 229 UI and 110 plugin tests pass, Angular/plugin compilation and both host type checks. Chrome runs native CDP pen and touch input with the real editor and a simulated PDF through the actual reader, density 2, three window sizes and four PDF docking positions. It checks coordinate alignment, camera stability, scroll offsets, bitmap resolution and finger navigation without ink. Partial/full repaint comparisons exercise pressure, overlap, alpha and edited sample tails at zoom 0.5/1/2; interior colors match, with Skia antialiasing differences confined to a backing-pixel edge. A 1500-move stroke reduced the paint-time p95 from 23.7 ms to 0.4 ms in this run. Isolated outliers remain. This does not certify physical pen hardware or all documents; the user's actual device/PDF retest remains pending.

The complete ZIP contains 21 verified files, including the existing recognition models, runtime and licenses. Notebook formats, Obsidian minimum 1.8.7, recognition privacy and native-provider priority remain unchanged. BRAT prepares missing recognition files with pinned URLs and SHA-256 verification. Handwriting remains experimental. No community-directory approval is claimed.

## Previous release: 1.6.10

This release separates Retina ink bitmaps from CSS-transformed objects and invalidates raster caches on size, density and viewport zoom changes. It adds an experimental local handwriting fallback, verified first-use model provisioning and shape recognition on pen lift. Obsidian minimum remains 1.8.7; notebook formats are unchanged.

Matching private source: tag `1.6.10` in `daisel10/era`, commit `18fbaf1c51de4374a0392f71526245e9e5b8ee21`.
`main.js` SHA-256: `f4e190013f81ab49f65c1ce5d5c8546927f6bf1f9c8a08f0cd01462f36ad480a`.

Validation: 227 UI and 110 plugin tests pass, plus focused recognizer tests, Angular/plugin compilation and both host type checks. Chrome exercises actual pen CDP input at Retina density, zoom 0.5/1/2 and viewport rotation, plus actual local word/math inference without Windows Ink. The English fixture reads hello; hola appears among the Spanish alternatives. This is not a general accuracy claim. The local WebKit test could not launch due to missing system libraries; Chrome simulation does not certify physical iPad/Apple Pencil behavior.

The complete ZIP contains 21 verified files, including equations and handwriting models, runtime and licenses. BRAT installs the main files; missing recognition resources are downloaded from immutable upstream URLs and checked against bundled SHA-256 hashes. Strokes are not uploaded. Model preparation needs Internet the first time and stores verified files beside the plugin for offline reuse. SHA-256 also works without WebCrypto. Native/browser recognizers retain priority.

The text fallback uses quantized TrOCR-small trained on IAM and remains experimental, particularly for Spanish. Alternatives and original ink remain recoverable. Windows Ink remains limited to Windows desktop. ML Kit and an Apple native bridge are not integrated. The existing free-use license and private-source model remain, with the applicable MIT and other third-party notices preserved. No community-directory approval is claimed.

## Evidence for 1.6.0

See [Review response](REVIEW-RESPONSE.md) for the exact 1.6.0 bundle hash, the Angular version-parser expression at line 13648, Windows Ink process boundaries and the author's decision to retain word recognition. Its scanner mapping is still unconfirmed. The current license remains unchanged while standard restrictive alternatives are assessed.

## Historical review of 1.0.1

These notes explain the existing 1.0.1 distribution for review. They do not change the runtime, CSS, executable assets, dependencies, version or packaging. Catalogue approval remains pending.

## Installation and usage

The [README](README.md) now contains explicit English **Installation** and **Usage** sections, in addition to the Spanish instructions. This addresses the missing-instructions warning without changing the plugin.

## Custom license

The [LICENSE](LICENSE) retains the author's selected free-use terms. [License explanation](LICENSE-EXPLAINED.md) distinguishes permitted use and backups from the modification and redistribution rights retained by the author. GitHub's recognized-license warning may remain because the license is custom; this requires reviewer assessment rather than a runtime change.

## Runtime domain assembly warning

The screenshot reports **split/join domain assembly**, without a source location. Inspection of the exact published `main.js` found one literal `.join(".")` occurrence, at line **13081**, inside Angular's version parser:

<!-- prettier-ignore -->
```js
let t = e.split(".");
this.major = t[0], this.minor = t[1], this.patch = t.slice(2).join(".");
```

The nearby Angular code formats version-specific documentation URLs such as `https://v21.angular.dev` and appends `/errors`. The inspected functions parse version strings and format documentation links; they do not issue a network request. The corresponding installed dependency is Angular 21.2.25, in `@angular/core/fesm2022/_effect-chunk2.mjs`, originating from Angular's `version.ts` and `error_details_base_url.ts`.

This is a candidate explanation, not a confirmed mapping to the scanner finding. A file/line or exact scanner match is needed to establish which expression triggered it. No expression has been rewritten or hidden to avoid detection.

Era's actual web requests are the user-triggered link-preview and linked-resource imports disclosed in the README. They use the HTTP/HTTPS URL supplied by the user; the server at that URL receives the normal network request. Local drawing, PDFs and Windows Ink do not require a remote service.

## Shell execution / child_process

The handwriting integration uses `node:child_process` to launch Windows PowerShell from the Windows system directory. The process is hidden and noninteractive, runs without a PowerShell profile, and receives an encoded copy of the fixed script bundled with the plugin through its command arguments. Encoding transports the fixed script as UTF-16; it does not encode a command assembled from user text.

The script uses Windows Runtime's `Windows.UI.Input.Inking` APIs. Its standard input contains JSON requests with an identifier, stroke coordinates and language (`es` or `en`). Those fields are parsed as data rather than evaluated as PowerShell commands. The script limits request size and stroke count; the host has a recognition timeout and rejects pending requests and terminates the process when the recognizer is disposed.

The inspected script does not download code, invoke an arbitrary user-supplied command, request elevation or install handwriting components. Recognition uses the user's installed Windows handwriting components. It runs with the permissions of the Obsidian process; spawning a process remains a capability that warrants review.

The shell-execution warning is expected while this integration is present. This documentation does not remove that capability or imply that Obsidian has approved it.

## Matching private source

The source corresponding to the published 1.0.1 assets is private tag `1.0.1`, commit `7d917b6551a6afa666d837804f4ed7bb98343dfc`. The private-source review should be associated with this reference. A different source revision is not evidence that these assets reproduce from that source. These notes do not confirm which reference the directory currently uses.

## Remaining review items

CSS selector warnings, bundle size, extra release assets, artifact attestations and storage behavior are outside this documentation-only update. The existing compiled files and release 1.0.1 are preserved.

The review screenshot states that automated review could not be completed and an administrator will investigate. The listed warnings alone do not establish the cause of that incomplete review. See Obsidian's [review guidance](https://docs.obsidian.md/community-directory/manage-entry) and [developer policies](https://docs.obsidian.md/community-directory/developer-policies).
