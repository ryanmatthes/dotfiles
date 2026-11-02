# dotfiles

Managed with [chezmoi](https://www.chezmoi.io/). One repo for WSL (Linux) and Windows.

- WSL only: `.bashrc`, `.profile`, `.config/mise/config.toml`
- Windows only: VS Code user settings (`AppData/Roaming/Code/User/settings.json`)
- Both: `.gitconfig` (template; WSL adds the Windows Git Credential Manager path)
- `windows/dev-setup.winget`: WinGet configuration (not applied by chezmoi; run with `winget configure`)

New machine: `chezmoi init --apply ryanmatthes`. It asks once: machine type (home/work)
and the git email for that machine (saved in `~/.config/chezmoi/chezmoi.toml`, not in this repo).
