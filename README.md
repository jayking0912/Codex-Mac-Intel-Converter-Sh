# Codex App for Mac Intel (Unofficial)

Minimal helper repo to rebuild the official `Codex.dmg` into an Intel-compatible macOS app image.

This is an unofficial adaptation approach, similar in spirit to the Linux community port:  
[Codex App for Linux (unofficial)](https://github.com/areu01or00/Codex-App-Linux/)

## What is included

- `build-intel.sh` — main build script
- `.gitignore` — ignores build artifacts and local temp files
- `package.json` — optional convenience `npm` script wrapper

## Requirements

- macOS
- `bash`, `curl`, `hdiutil`, `ditto`, `codesign`
- Node.js + npm (used by the script to fetch Electron/runtime dependencies)
- Internet access to download the official `Codex.dmg`

## Quick usage

1. Run:

```bash
chmod +x ./build-intel.sh
./build-intel.sh
```

The script now downloads the latest official `Codex.dmg` from:

`https://persistent.oaistatic.com/codex-app-prod/Codex.dmg`

on every run, deletes any existing local `Codex.dmg` in the repo root first, mounts the fresh download, and then rebuilds the app into an Intel-compatible DMG.

## Output

- `CodexAppMacIntel.dmg` — rebuilt Intel-targeted output
- `log.txt` — full build log
- `.tmp/` — temporary build workspace

If you have problems, ask your current Codex :)
