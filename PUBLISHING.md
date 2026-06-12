# Publishing Model

This repository is the Home Assistant install target.

Each add-on should keep its implementation in its own source repository and publish only its installable Home Assistant folder into this repo at the root.

## Current source mappings

| Source repo | Published folder(s) in this repo | Publish method |
| --- | --- | --- |
| `parnunu/home-assistant-matter-hub` | `hamh/`, `hamh-beta/` | Source release workflow dispatches version/changelog updates into this repo |
| `parnunu/ha-addon-openclaw` | `openclaw/` | Source repo sync workflow commits the published folder into this repo |
| `parnunu/Home-Assistance-Realfeel-Temperature-Sensor` | `realfeel_temperature/` | Source repo publishes a compatibility-installer add-on folder into this repo |
| `parnunu/ssh-tunnel-gateway-addon` | `ssh_tunnel_gateway/` | Source repo sync workflow commits the published folder into this repo |
| `parnunu/ha-addon-web-proxy` | `lightweight_web_proxy/` | Source repo sync workflow commits the published folder into this repo |

## Required source-repo secret

Use the same secret name in source repositories:

- `CENTRAL_REPO_PAT`

Recommended token shape:

- fine-grained PAT
- repository access: `parnunu/home-assistant-addons`
- repository permission: `Contents: Read and write`

A classic PAT with `repo` scope also works if you prefer that, but the fine-grained token is tighter.

## Adding another add-on later

1. Keep the new add-on's source in its own repository.
2. Put a Home Assistant-ready published folder in that source repo.
3. Add a GitHub Actions workflow in the source repo that syncs the published folder into this repo root.
4. Update this repo's root `README.md` so the new add-on appears in the public list.
5. Keep the folder name stable and based on the published slug unless there is a compatibility reason not to.

## Notes

- Avoid submodules here. This repo should stay simple for Home Assistant and for users inspecting it.
- Matter Hub already had a partial central-release path; this repo keeps that model instead of replacing it.
- RealFeel Temperature is a source custom integration, so its published add-on is explicitly a compatibility installer rather than a native long-running service.
