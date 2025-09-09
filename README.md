# 🌌 SauzerOS Package Manager

> **Modified [KISS](https://kisslinux.github.io/wiki/package-manager) by Dylan Araps & the KISS Community**  
> ⚠️ *All code written with AI 😅 

---

## ✨ Main Changes

- ✅ **GNU tools required**: `coreutils`, `grep`, `tar`, `bash`  
- ✅ **Global environment flags** in **`/etc/kiss/flags`**  
- ✅ **Configurable paths** for binaries, logs, and sources  
- ✅ Support for **alternate tmpdir builds** (`/etc/kiss/BIG_PKGS`)  
- ✅ **Deduplicated source downloads** (shared cache across packages)  
- ✅ Tracks **all library dependencies** per package  
  - Stored in `/var/db/kiss/installed/pkg/libdeps`  
- ✅ Update check: warns if a removed library is still needed  
- ✅ Shows **build time** after each build  

---

## ⚙️ Environment Flags

| Variable          | Default / Values   | Description |
|-------------------|-------------------|-------------|
| **`KISS_INSTALL`** | `1` (default) <br> `0` (build only) | Controls installation prompt |
| **`KISS_AUTO`**    | `0` (prompt) <br> `1` (auto install) | Auto-install without prompt |
| **`KISS_TMPDIR`**  | — | Build directory |
| **`KISS_TMPDIR2`** | — | Build directory for packages in `/etc/kiss/BIG_PKGS` |
| **`KISS_DL`**      | — | Source download tool |
| **`KISS_DIRS`**    | — | Path to bin/logs/source directories |
| **`KISS_QUIET`**   | `0` (default: output) <br> `1` (silent build) | Controls build verbosity |
| **`KISS_SU`**      | — | Superuser tool used for install |
| **`KISS_COMPRESSION`** | — | Package compression method |
| **`KISS_STRIP`**   | `1` (default: strip binaries) <br> `0` (disable) | Can be overridden with `:> nostrip` in build file |

---

