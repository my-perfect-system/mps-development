---
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
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 32

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
