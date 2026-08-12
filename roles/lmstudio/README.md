---
namespace: odem
collection: development
role: lmstudio
---

# `odem.development.lmstudio`

Install LM Studio (CLI + AppImage) per user for Debian 13 (trixie)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `lmstudio_appimage_local_bin` | `.local/bin` | Home-relative per-user local bin directory |
| `lmstudio_appimage_path` | `.local/bin/lmstudio.AppImage` | Home-relative path where the LM Studio AppImage is stored |
| `lmstudio_appimage_url` | `https://installers.lmstudio.ai/linux/x64/{{ lmstudio_appimage_version }}/LM-Studio-{{ lmstudio_appimage_version }}-x64.AppImage` | Direct URL for the LM Studio AppImage |
| `lmstudio_appimage_version` | `0.4.12-1` | Version of the LM Studio desktop AppImage to install |
| `lmstudio_cli_bin` | `.lmstudio/bin/lms` | Home-relative path where the LM Studio CLI lands after install |
| `lmstudio_cli_installer_url` | `https://lmstudio.ai/install.sh` | URL of the LM Studio CLI installer script |
| `lmstudio_desktop_file` | `.local/share/applications/lmstudio.desktop` | Home-relative path where the .desktop launcher is written |

## Dependencies

- `odem.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - odem.development.lmstudio
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 81

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
