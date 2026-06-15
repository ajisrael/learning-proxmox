# Tmux

## Install

```bash
sudo apt update && sudo apt install -y tmux
```

## Useful Config

Add to `~/.tmux.conf`:

```
set -g mouse on
set -g default-terminal "tmux-256color"
```

## Common Commands

| Action | Command |
|---|---|
| Start a session | `tmux` |
| Create a named session | `tmux new -s <name>` |
| Detach from session | `Ctrl-b d` |
| Reattach to session | `tmux attach -t <name>` |
| List sessions | `tmux ls` |
| Split pane horizontally | `Ctrl-b %` |
| Split pane vertically | `Ctrl-b "` |
| Move between panes | `Ctrl-b <arrow>` |
| Resize pane | `Ctrl-b <Ctrl-arrow>` |
| Create new window | `Ctrl-b c` |
| Rename window | `Ctrl-b ,` |
| Next / previous window | `Ctrl-b n` / `Ctrl-b p` |
| Kill pane | `Ctrl-b x` |
| Enter scroll mode | `Ctrl-b [` (then `PgUp`/`PgDn`, `q` to quit) |
| Reload config | `Ctrl-b :source ~/.tmux.conf` |
