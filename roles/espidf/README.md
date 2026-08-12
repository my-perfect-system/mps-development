---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: development
role: espidf
---

# `mps.development.espidf`

Install Espressif IoT Development Framework (multi-version, per-user)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `espidf_apt_packages` | `[14 items]` | Apt packages required by ESP-IDF |
| `espidf_local_bin` | `.local/bin` | Home-relative per-user bin directory for activation scripts |
| `espidf_src_base` | `esp/sources` | Home-relative base directory for ESP-IDF source clones |
| `espidf_tools_base` | `esp/tools` | Home-relative base directory for ESP-IDF toolchains (per version) |
| `espidf_versions` | `- v5.3` | ESP-IDF versions to install (one isolated install per version) |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.development.espidf
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 109

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
