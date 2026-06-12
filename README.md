# Home Assistant Add-ons by parnunu

This is the Home Assistant custom add-on repository you add in Home Assistant.

Repository URL:

- `https://github.com/parnunu/home-assistant-addons`

## Install in Home Assistant

1. Open **Settings -> Add-ons -> Add-on Store**.
2. Open the top-right menu -> **Repositories**.
3. Paste `https://github.com/parnunu/home-assistant-addons`.
4. Refresh the add-on store.
5. Install the add-on you want.

## Available add-ons

| Add-on | Folder | Slug | Source repo | Notes |
| --- | --- | --- | --- | --- |
| Home-Assistant-Matter-Hub | `hamh` | `hamh` | `https://github.com/parnunu/home-assistant-matter-hub` | Stable channel |
| Home-Assistant-Matter-Hub (Beta) | `hamh-beta` | `hamh-beta` | `https://github.com/parnunu/home-assistant-matter-hub` | Rework / beta channel |
| OpenClaw | `openclaw` | `openclaw` | `https://github.com/parnunu/ha-addon-openclaw` | Published from its source add-on repo |
| RealFeel Temperature | `realfeel_temperature` | `realfeel_temperature` | `https://github.com/parnunu/Home-Assistance-Realfeel-Temperature-Sensor` | Compatibility installer for a custom integration source repo |
| SSH Tunnel Gateway | `ssh_tunnel_gateway` | `ssh_tunnel_gateway` | `https://github.com/parnunu/ssh-tunnel-gateway-addon` | Exposes remote services to your LAN through SSH local forwards |
| Lightweight Forward Proxy | `lightweight_forward_proxy` | `lightweight_forward_proxy` | `https://github.com/parnunu/ha-addon-web-proxy` | Lightweight HTTP/HTTPS forward proxy |

## Publishing model

This repository is the install target for Home Assistant.

Each add-on keeps its source of truth in a separate repository and publishes its installable folder into this repo at the root level. New add-ons should follow the same pattern instead of turning this repo into the source-development home for each project.

Publishing details, folder mappings, and required GitHub secrets are documented in [PUBLISHING.md](PUBLISHING.md).

## Fork limitation

GitHub still marks this repository as a fork of `t0bst4r/home-assistant-addons`. GitHub does not provide a true in-place defork operation for this case, so the fork lineage remains visible. That limitation does not stop this repository from working as the central Home Assistant add-on repository you paste into Home Assistant.
