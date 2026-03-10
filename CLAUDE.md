# AppleScripts - Claude Notes

## Overview
macOS automation toolkit. 16 CLI tools behind a unified `mac` dispatcher. 2276 LOC. v2.0.0.

## Run
```bash
mac <tool> <command> [args]
# e.g. mac music play drake, mac win left Terminal
```

Tools can also be called directly: `musicctl play drake`, `winctl left Terminal`.

Install: `./install.sh` symlinks bin/* to ~/.local/bin. Tab completions in `completions/` (bash + zsh).

## Tools
- **mac** -- dispatcher, routes to correct tool binary
- **musicctl** -- Apple Music playback, search, queue, playlists
- **appctl** -- app launcher and manager
- **winctl** -- window management (left/right/max/center)
- **clipctl** -- clipboard manager
- **finderctl** -- Finder and file management
- **sysctl** -- system controls (volume, brightness, dark mode, DND)
- **diskctl** -- storage management
- **netctl** -- network utilities (WiFi, IP, speed)
- **procctl** -- process management
- **keyctl** -- macOS Keychain operations
- **inputctl** -- trackpad, mouse, keyboard settings
- **mac-status** -- one-line system status
- **mac-context** -- save/restore desktop state
- **macflow** -- workflow engine (multi-step automation)
- **auto-dj-daemon** -- background music queueing by mood/genre

## Workflows
`macflow run <name>`. 5 built-in: morning, focus, present, code, wind-down. Custom workflows go in `~/.local/share/macflow/workflows/`.

## Status
v2.0.0 -- Stable, actively used.
