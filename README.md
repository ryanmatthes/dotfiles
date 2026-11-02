# dotfiles

Managed with [chezmoi](https://www.chezmoi.io/). One repo for WSL (Linux) and Windows.

- WSL only: `.bashrc`, `.profile`, `.config/mise/config.toml`
- Windows only: VS Code user settings (`AppData/Roaming/Code/User/settings.json`)
- Both: `.gitconfig` (template; WSL adds the Windows Git Credential Manager path)
- `windows/` (never applied by chezmoi; run by hand with `winget configure -f <file>` in an elevated PowerShell):
  - `base.winget`: PowerShell 7 + chezmoi. Any machine.
  - `visual-studio.home.winget`: Developer Mode + Visual Studio Community 2026 + workloads. **Home only** (Community isn't licensed for company use).

New machine: `chezmoi init --apply ryanmatthes`. It asks once: machine type (home/work)
and the git email for that machine (saved in `~/.config/chezmoi/chezmoi.toml`, not in this repo).
