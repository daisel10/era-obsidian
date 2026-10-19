# Review response for Era 1.6.0

Historical evidence for 1.6.0. The current release is 1.6.5; the hash, line numbers and source reference below describe the older release and have not been remapped to the current bundle. See [README](README.md) and [Review notes](REVIEW-NOTES.md) for the current release.

This report describes the exact released files. It does not assert that scanner warnings have been cleared or that directory approval has been granted. The author confirmed that Windows Ink word recognition must be retained. The existing license remains in force while restrictive standard-license alternatives are assessed.

## Matching release

- Public distribution: https://github.com/daisel10/era-obsidian/releases/tag/1.6.0
- Private source tag: `1.6.0`, commit `4438147a5aacb4a5aab8c450a3c1c58555e6a5f7`.
- `main.js`: 27,774,206 bytes; SHA-256 `2229657c4c2b2497bfb1b60c654acbaab008bd93f0b6d707b604d3adef3c2f64`.
- The public repository's `main.js` was compared byte for byte with the frozen release.

## License detection

GitHub's license API reports `NOASSERTION` for the existing custom free-use LICENSE. The file exists; the warning is about recognition of its terms, rather than an absent license. The author chose free personal, educational and professional use while reserving modification and redistribution rights. The existing LICENSE and third-party permissions remain unchanged.

Obsidian's [FAQ](https://docs.obsidian.md/community-directory/faq) explains that custom licenses can trigger this warning. Its [policies](https://docs.obsidian.md/community-directory/developer-policies) require a LICENSE and compliance with third-party terms, and assess private source on a case-by-case basis. This report does not promise acceptance of this particular license. Replacing it with MIT would grant additional modification and redistribution permissions and needs the author's choice.

## Split/join and dynamic domains

The exact released `main.js` contains one literal `.join(".")`, at line **13648**, in Angular 21.2.25's `Version` constructor:

<!-- prettier-ignore -->
```js
let t = e.split(".");
this.major = t[0], this.minor = t[1], this.patch = t.slice(2).join(".");
```

The input used here is Angular's version, `21.2.25`. This operation reconstructs the version's patch component. The corresponding installed dependency is `@angular/core/fesm2022/_effect-chunk2.mjs`, lines 13–32.

Nearby Angular code does construct its documentation origin from the version; for this stable build it evaluates to `https://v21.angular.dev`, with the error-reference path `/errors`. This code formats documentation URLs. The inspected version and documentation-base functions do not send network requests.

These are candidate explanations for the warning. The scanner message supplied by the author has no file/line or matched expression, so a confirmed mapping remains pending. Please provide the exact scanner match before treating the version-parser expression as an obfuscated network endpoint.

Era's application requests in `integrations/obsidian/src/main.ts` accept a URL explicitly provided by the user, validate HTTP/HTTPS, and request that URL for link previews or resource imports. There is no fixed service domain to substitute for a user-selected URL. Word and equation recognition run locally. This inspection is scoped to the cited paths and bundle expressions, rather than a claim that every dependency has been exhaustively audited.

## Shell execution capability

The warning reflects a real capability. Era starts Windows PowerShell through `node:child_process` for local Windows Ink word recognition on Windows. The executable is in the Windows system directory. The fixed bundled script is passed as UTF-16 base64 with `-NoLogo`, `-NoProfile` and `-NonInteractive`; the encoding transports that fixed script. Stroke samples and the selected language arrive separately as JSON through standard input and are not evaluated as commands.

The host starts this process lazily, reuses it, validates responses, applies a 15-second recognition timeout, and terminates it on disposal or failure. The script uses installed Windows handwriting components for Spanish or English; the inspected script does not download code, install components or request elevation. The process runs with Obsidian's permissions; these bounds do not remove the process-execution capability or its warning.

The author explicitly chose to retain this backend and its word-recognition feature. Removing this backend from the distribution would remove Windows Ink word recognition. Local equation recognition uses a separate Web Worker/ONNX backend and would remain available. A setting that merely disables Windows Ink would leave the capability in the distributed code; hiding its import would not resolve the underlying review concern.

## Review request

Please assess the custom license and disclosed Windows Ink capability, and identify the precise expression behind the split/join warning. Windows Ink is intentionally retained and its process capability is disclosed. The license terms have not been changed. Please assess these disclosed capabilities rather than interpreting this report as a claim that the warnings disappeared.

Obsidian's [review guidance](https://docs.obsidian.md/community-directory/manage-entry) says warnings alone do not block submission. That does not guarantee acceptance or determine the cause of any separate failed or incomplete review. No review message has been sent on the author's behalf.

## Restrictive standard-license assessment

The author asked whether a known restrictive license can preserve the intended permissions while removing the recognition warning. A standardized name and GitHub auto-detection are different requirements.

- PolyForm Strict 1.0.0 is a software license that withholds modification and distribution rights, but limits permitted purposes to noncommercial use (with its stated personal/organization provisions). It is absent from the reviewed Licensee vendored license catalog. Switching would change the current professional-use permissions and is not a demonstrated fix for GitHub recognition.
- GPL-3.0 is present in that detection catalog, but grants modification, redistribution and commercial use and imposes source-code obligations when distributing covered object code. It does not preserve the current compiled-only, reserved-rights model.
- The current custom license preserves the author's existing permissions, but the GitHub `NOASSERTION` warning remains for human assessment. No suitable standard license satisfying all those requirements was identified in this assessment.

References: [GitHub's license detection](https://docs.github.com/en/repositories/managing-your-repositorys-settings-and-features/customizing-your-repository/licensing-a-repository#detecting-a-license), [Licensee's catalog](https://github.com/licensee/licensee/tree/main/vendor/choosealicense.com/_licenses), [PolyForm Strict terms](https://polyformproject.org/licenses/strict/1.0.0), and [GPL-3.0 terms](https://choosealicense.com/licenses/gpl-3.0/). These observations do not change any license terms or guarantee directory approval.
