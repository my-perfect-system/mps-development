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
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 109
