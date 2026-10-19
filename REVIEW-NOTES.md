# Review notes

## Current release: 1.6.6

This release restores drawing and erasing after failed pointer operations, reuses
exotic-brush geometry and compact previews, restores square COPIC samples, and
preserves APKG cards with shared source GUIDs and ordinals as independent cards.
The notebook format and minimum supported Obsidian version remain unchanged.

The matching private source is tag `1.6.6` in `daisel10/era`, commit
`8c554b9d77011f7a368a258ef7f9246557244bf6`. The compiled `main.js` SHA-256 is
`2d40dbe692b9f969b67d3bcf4bd57f86ca298ac0297c954791aa5b362767f12c`.

Validation: 207 UI tests, 102 plugin tests and 186 Rust workspace tests pass.
WASM, Angular AOT and plugin compilation, host type checks, formatting and Clippy
pass. All 15 ZIP entries match the distribution byte for byte; the nine equation
assets match the hashes recorded in their asset manifest.

The complete ZIP includes `equations/`, with local models, runtime and licenses.
BRAT's main-file installation also needs `equations/` from the matching ZIP.
Windows Ink remains limited to Windows desktop; browser handwriting depends on
API and language availability. ML Kit is not integrated.

The custom free-use license, private-source model and process capability remain
in place. Physical pen/mobile and real external-sync validation remain pending.
Directory approval is pending. Historical hashes and scanner observations below
do not establish directory approval for this release.

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
