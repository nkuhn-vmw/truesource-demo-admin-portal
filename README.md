# truesource-demo-admin-portal

Demo internal admin portal for [TrueSource Viewer](https://github.com/nkuhn-vmw/truesource-viewer-hub-edition).

**Intentionally vulnerable demo. Do not deploy it, do not install from it.** It contains only
manifests and lock files, written by hand: the lock files have no integrity hashes, and the
versions named below are pinned on purpose so that the viewer has something to find.

A React front end, versions locked with Yarn 1.

| File | Pins | What the viewer should report |
|---|---|---|
| `yarn.lock` | `eslint-config-prettier` 8.10.1 (OSV `MAL-2025-6022`), `is` 3.3.1 (`MAL-2025-6020`) | Malicious versions published in the July 2025 maintainer phishing wave; listed first among new and unverified components |
| `yarn.lock` | `axios` 0.21.1, `follow-redirects` 1.14.0, `node-fetch` 2.6.0, `minimist` 1.2.5, `moment` 2.29.1 | Known vulnerabilities |
| `Dockerfile` | `node:16.20.2-alpine` | Node.js 16 is past its end of life |

The malicious versions were removed from the npm registry; this repository only names them.
