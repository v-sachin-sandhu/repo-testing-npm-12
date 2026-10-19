# lockfile-v4-repro

Minimal npm project for testing Dependabot behavior with `lockfileVersion: 4`.

- `package.json` declares `patchDependencies` (npm's native patch system), which makes npm 12+ emit a `lockfileVersion: 4` lockfile.
- `package-lock.json` is a `lockfileVersion: 4` lockfile with an outdated dependency (`is-odd@2.0.0`, latest is newer) so Dependabot has something to update.
