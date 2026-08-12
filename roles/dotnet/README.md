---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: development
role: dotnet
---

# `mps.development.dotnet`

Install .NET SDK via the official dotnet-install.sh script

## Default variables

| Variable | Default | Description |
|---|---|---|
| `dotnet_install_args` | `--version latest` | Arguments passed to the dotnet-install.sh script |
| `dotnet_installer_path` | `/tmp/dotnet-install.sh` | Where to download the installer script (cleared after install) |
| `dotnet_installer_url` | `https://dot.net/v1/dotnet-install.sh` | URL of the official dotnet-install.sh script |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.development.dotnet
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 32
