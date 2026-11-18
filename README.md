# koala

This sets up my Debian server "koala" from a fresh install: it adds CrowdSec to block known attackers, makes zsh with Oh My Zsh the login shell, and installs Podman, Bun, Claude Code and ripgrep. It also replaces the login banner with a koala, and everything is described in one config file so the same server can be rebuilt any time.

```sh
apt update && apt install -y git curl ca-certificates
curl -fsSL https://mise.run | sh
~/.local/bin/mise bootstrap --from https://github.com/ericbstie/koala.git --yes
```
