![koala](koala.png)

Server configuration files for first time setups.

```sh
apt update && apt install -y git curl ca-certificates
curl -fsSL https://mise.run | sh
git clone https://github.com/ericbstie/koala.git ~/koala
cd ~/koala
~/.local/bin/mise trust
~/.local/bin/mise bootstrap --yes
```

## What is set up

- CrowdSec with the iptables firewall bouncer, from the CrowdSec apt repository
- Console enrollment for CrowdSec (`mise run setup-machine`)
- Tailscale, from the Tailscale apt repository; join the tailnet with `mise run setup-tailscale`
- mise, activated in zsh
- zsh as root's login shell, with Oh My Zsh
- Podman, with QEMU and virtiofsd
- Docker, only for Coolify, and a password-less `coolify` user in the docker group (reach it with `sudo -iu coolify`)
- Bun, Claude Code, the Hetzner `hcloud` CLI and ripgrep, installed globally
- git and curl
- koala login banner, replacing the default
- SSH last-login message turned off
