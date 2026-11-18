![koala](koala.png)

- CrowdSec with the iptables firewall bouncer, from the CrowdSec apt repository
- Console enrollment for CrowdSec (`mise run setup-machine`)
- mise, activated in zsh
- zsh as root's login shell, with Oh My Zsh
- Podman, with QEMU and virtiofsd
- Bun, Claude Code and ripgrep, installed globally
- git and curl
- koala login banner, replacing the default
- SSH last-login message turned off

```sh
apt update && apt install -y git curl ca-certificates
curl -fsSL https://mise.run | sh
git clone https://github.com/ericbstie/koala.git ~/koala
cd ~/koala
~/.local/bin/mise trust
~/.local/bin/mise bootstrap --yes
```
