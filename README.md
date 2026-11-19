# Vimu 12.50 — de-licensed build (security research on our own product)

License check removed: `H3/f.smali` stubbed to permanent `Key Purchased (FULL)`, all license
classes (Q1 / R1 / Play-LVL / AccountProvider) stripped from the dex, LVL + license endpoints
unreachable, Firebase Analytics/Crashlytics upload disabled. OpenSubtitles, FFmpeg engine,
local 8087 proxy untouched.

## Assets

- `Vimu-12.50-delic.apk` — the mod (signed v1+v2+v3, debug-style key `CN=Vimu Mod`)
- `Vimu-12.50-control.apk` — re-signed original with **zero** edits; if a file fails on the
  mod, install the control on the same file to tell "re-sign broke it" from "patch broke it"

Install note: uninstall the store version first (signatures differ). The mod never contacts
`get.vimu.tv` / `lic.vimu.tv` / Play LVL and sends no license status to Firebase.

Gate evidence, patch plan, and the full device-test checklist live in the build workspace
(`~/.pi/projects/vimu-mod/research/`), not in this repo.
