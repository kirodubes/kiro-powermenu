# Changelog

## 2026.06.23

### What Changed
- **Fixed the Hyprland logout in `powermenu.sh`** so it matches archlinux-logout's behavior. The
  `hyprland)` case did a bare `hyprctl dispatch exit`, which Hyprland 0.55+ (Lua config) rejects —
  `hyprctl dispatch <X>` is parsed as Lua `hl.dispatch(X)`, so `exit` errors out and logout does nothing.

### Technical Details
- The `hyprland)` case now mirrors archlinux-logout's `_get_logout()`: `uwsm stop` when the session is
  uwsm-managed (checked with a `systemctl --user is-active` query on the uwsm-created Hyprland wayland-wm
  unit), else `hyprctl dispatch 'hl.dsp.exit()'` on Hyprland **0.55+**, else legacy `hyprctl dispatch exit`.
- Version gate parses the first `X.Y.Z` from `hyprctl version` and compares `(major,minor) >= (0,55)`
  in awk; an unparseable/empty version falls back to the legacy command (same default as archlinux-logout).
- `bash -n` clean; version logic verified against 0.55.0 / 0.54.9 / 0.60.1 / 1.0.0 / 0.41.2 / empty.

### Files Modified
- etc/skel/.config/powermenu/powermenu.sh

## 2026.05.21

### What Changed
- Initial markdown scaffold added per the ecosystem MD-scaffold rule ([HQ/CLAUDE.md](/home/erik/Insync/Kiro/Kiro-HQ/CLAUDE.md#required-markdown-scaffold-every-repo)).
- Stubs created for `CHANGELOG.md`, `CLAUDE.md`, `IDEAS.md`, `TODO.md` (whichever were missing).
- README rewritten with real install/usage content (replaced earlier one-line stub) where applicable.

### Files Modified
- CHANGELOG.md (created)
- CLAUDE.md (created where missing)
- IDEAS.md (created where missing)
- TODO.md (created where missing)
- README.md (rewritten where it was a stub)
