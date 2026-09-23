# configs

Personal dotfiles and tool configs.

## Contents

- `.vimrc` — Vim settings
- `terminal-aliases.sh` — shell aliases and functions
- `vscode-settings.json` — VS Code settings
- `vscode-keyboard-shortcuts-mac.json` — VS Code keybindings (macOS)
- `claude/settings.json` — Claude Code settings (goes in `~/.claude/settings.json`)
- `claude/skills/unslop/` — custom Claude Code skill that strips AI writing tells (goes in `~/.claude/skills/unslop/`)

## Usage

Symlink or copy the files you want into place, e.g.:

```sh
ln -sf "$(pwd)/.vimrc" ~/.vimrc
ln -sf "$(pwd)/claude/settings.json" ~/.claude/settings.json
ln -sf "$(pwd)/claude/skills/unslop" ~/.claude/skills/unslop
```
