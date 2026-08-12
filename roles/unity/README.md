---
namespace: mps
collection: development
role: unity
---

# `mps.development.unity`

Install Unity Hub + VSCode for Debian 13 (trixie)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `unity_enable_vscode` | `true` | Also install VSCode (matches source stage7-extras behavior) |
| `unity_key_path` | `/usr/share/keyrings/Unity_Technologies_ApS.gpg` | Where the dearmored Unity GPG key is stored |
| `unity_key_url` | `https://hub.unity3d.com/linux/keys/public` | Unity Technologies GPG key URL |
| `unity_packages` | `- unityhub` | Apt packages to install from the Unity Hub repo |
| `unity_repo_components` | `- stable<br>- main` | APT repository components for the Unity Hub repo |
| `unity_repo_state` | `present` | State of the Unity Hub APT repository entry |
| `unity_repo_url` | `https://hub.unity3d.com/linux/repos/deb` | Unity Hub APT repository base URL |
| `unity_vscode_deb_url` | `https://go.microsoft.com/fwlink/?LinkID=760868` | Direct .deb URL for the VSCode package |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.development.unity
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 64

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
