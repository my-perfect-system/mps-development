---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: development
role: java
---

# `mps.development.java`

Install default JDK and JRE for Debian 13 (trixie)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `java_packages` | `- default-jdk<br>- default-jre` | Apt packages required for the default Java toolchain |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.development.java
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 14
