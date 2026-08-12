# `odem.development` Ansible Collection

Per-user development tooling — SDKs, CLIs, IDEs.

## Galaxy metadata

- **namespace**: `odem`
- **name**: `development`
- **version**: `0.3.1`
- **dependencies**: `odem.base`, `ansible.posix`

See [`galaxy.yml`](galaxy.yml) for the canonical values.

## Roles

| Role | Purpose |
|---|---|
| [`odem.development.opencode`](roles/opencode/README.md) | opencode CLI + dotfile sync (`files/`-based). |
| [`odem.development.java`](roles/java/README.md) | Java packages (`texlive-full`-style single apt install). |
| [`odem.development.dotnet`](roles/dotnet/README.md) | Microsoft `.NET` installer per user. |
| [`odem.development.espidf`](roles/espidf/README.md) | Multi-version esp-idf clone + install + per-version activator scripts. |
| [`odem.development.latex`](roles/latex/README.md) | texlive-full install. |
| [`odem.development.lmstudio`](roles/lmstudio/README.md) | LM Studio CLI + appimage + .desktop entry. |
| [`odem.development.unity`](roles/unity/README.md) | Unity apt repo + signing key + UnityHub packages + conditional VS Code deb. |

## Installation

```bash
ansible-galaxy collection install odem.development
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
    - odem.base.identity
    - odem.development.opencode
    - odem.development.java
    - odem.development.dotnet
```

## Documentation

- [`AGENTS.md`](AGENTS.md) — developer conventions
- `roles/<role>/README.md` — per-role variable docs

## License

GPL-3.0-or-later
