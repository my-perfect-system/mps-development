---
namespace: odem
collection: development
role: latex
---

# `odem.development.latex`

Install texlive-full for Debian 13 (trixie)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `latex_packages` | `- texlive-full` | Apt packages required for the LaTeX toolchain |

## Dependencies

- `odem.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - odem.development.latex
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: GPL-3.0-or-later
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 14

## Related files

- [`meta/main.yml`](meta/main.yml) — galaxy_info + role dependencies
- [`meta/argument_specs.yml`](meta/argument_specs.yml) — variable spec (the source of the variable table above)
- [`defaults/main.yml`](defaults/main.yml) — variable defaults (the source of the default values above)
