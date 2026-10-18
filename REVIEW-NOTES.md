# Review notes

## Current release: 1.6.4

This stable release consolidates approved handwriting styles/providers, recoverable blocks, eraser/pen corrections, save recovery, clipboard actions and guarded mobile loading. Windows Ink is created only on Windows desktop; browser handwriting remains conditional on API and language availability. ML Kit is not integrated. The custom free-use license and disclosed process capability remain in place. Directory approval is pending.

The matching private source reference is tag `1.6.4` in `daisel10/era`, commit `985d8abf86068222dbf0207c5e3d35b2b8a1cf56`. Validation passed 185 native, 99 plugin and 203 UI tests (487 total), Clippy, types and formatting. The tested bundle includes simulated mobile and recovery scenarios, and frozen installation preserves plugin data. The complete ZIP includes `equations/` with local models, runtime and licenses; handwriting fonts and their notices are incorporated into the compiled distribution. BRAT's main-file installation additionally requires copying `equations/` from the matching ZIP.

New font choices and recoverable handwriting blocks require notebook formats v19 and v20 respectively. Use 1.6.4 or later to open notebooks using these features. Simulated mobile/provider/sync checks do not certify physical devices or real external synchronization services.

The hashes and scanner observations below are historical. They do not assert that 1.6.4 has passed directory review or resolved prior warnings.

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
