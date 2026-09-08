# WoWok Desktop — Downloads

Official download mirror for the [WoWok Desktop](https://wowok.net/products.html) client (Windows / macOS / Linux). The same signed installers are also published at [download.wowok.net](https://download.wowok.net/latest/latest.json) — pick whichever is fastest for you. Artifacts are attached to each [Release](https://github.com/wowok-ai/download/releases).

| Platform | File | Size | Download |
|---|---|---|---|
| Windows 10/11 (x64) | `WoWok_x64-setup.exe` | 37.8 MB | [Download](https://github.com/wowok-ai/download/releases/latest/download/WoWok_x64-setup.exe) |
| macOS 11+ (Apple Silicon & Intel) | `WoWok_universal.dmg` | 110.8 MB | [Download](https://github.com/wowok-ai/download/releases/latest/download/WoWok_universal.dmg) |
| Linux (x64, AppImage) | `WoWok_amd64.AppImage` | 134.4 MB | [Download](https://github.com/wowok-ai/download/releases/latest/download/WoWok_amd64.AppImage) |

> `releases/latest/` always points at the newest version. The versioned files live under each release tag (e.g. `…/download/v1.0.1/…`).

## Verify your download

Every artifact is published with its SHA-256. Compare against the checksums below (Windows installers are also minisign-signed — the `.sig` sits next to the asset).

| File | SHA-256 |
|---|---|
| `WoWok_x64-setup.exe` | `a6f18829c952a7cab2fb979d01685ecb7d494c27fc1ed1cc33572be4343e4c5e` |
| `WoWok_universal.dmg` | `84a1fb6b1cd86481d2d7250236aad357d167df7238fac2f34e6c91295401a586` |
| `WoWok_amd64.AppImage` | `b484d4fef56e1a53f5d19cd2971445c29985ce2669b21db2c19474270ddf057a` |

```sh
# macOS / Linux
shasum -a 256 WoWok_universal.dmg

# Windows (PowerShell)
certutil -hashfile WoWok_x64-setup.exe SHA256
```

## First run

- **Windows** — run the installer and follow the wizard.
- **macOS** — open the DMG and drag WoWok into *Applications*. The app is Developer ID signed and Apple-notarized, so Gatekeeper will not block it.
- **Linux** — make the AppImage executable and run it:

```sh
chmod +x WoWok_amd64.AppImage
./WoWok_amd64.AppImage
```

## Sources & mirror policy

- **Official primary**: [download.wowok.net](https://download.wowok.net) (managed release pipeline).
- **This repository**: automatic mirror of every release (managed by `scripts/release/mirror-gh.mjs`).
- **Note**: this repo hosts **installers only** — no source code.

For the airdrop, skills or the SDK, see [wowok.net](https://wowok.net).
