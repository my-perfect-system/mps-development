# `mps.development` Ansible Collection

Per-user development tooling — SDKs, CLIs, IDEs.

## Galaxy metadata

- **namespace**: `mps`
- **name**: `development`
- **version**: `0.3.1`
- **dependencies**: `mps.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

| Role | Purpose |
|---|---|
| `mps.development.opencode` | opencode CLI + dotfile sync (`files/`-based). |
| `mps.development.java` | Java packages (`texlive-full`-style single apt install). |
| `mps.development.dotnet` | Microsoft `.NET` installer per user. |
| `mps.development.espidf` | Multi-version esp-idf clone + install + per-version activator scripts. |
| `mps.development.latex` | texlive-full install. |
| `mps.development.lmstudio` | LM Studio CLI + appimage + .desktop entry. |
| `mps.development.unity` | Unity apt repo + signing key + UnityHub packages + conditional VS Code deb. |

## Installation

```bash
ansible-galaxy collection install mps.development
```

## Usage

```yaml
- hosts: all
  become: true
  vars:
    users_catalog:
      dev01:
        user_roles:
          development_opencode: true
          development_java: true
          development_dotnet: true
  roles:
    - mps.base.identity
    - mps.development.opencode
    - mps.development.java
    - mps.development.dotnet
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
