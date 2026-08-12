# AGENTS.md — odem-development

Per-user development tooling — SDKs, CLIs, IDEs. All roles are
single-file `tasks/main.yml` (flattened in this refactor pass).

## Galaxy

- **namespace**: `odem`
- **name**: `development`
- **version**: `0.3.1`
- **dependencies**: `odem.base >=0.1.0`, `ansible.posix >=1.0.0`

## Roles

| Role | Description | Complexity |
|---|---|---|
| `odem.development.opencode` | opencode CLI install (stat-gated), 2× `synchronize` to deploy `.opencode/` and `.claude/` config from role `files/`. | 2 |
| `odem.development.java` | Single `apt` install of `java_packages`. Per-user loop gated by `development_java` flag. | 1 |
| `odem.development.dotnet` | Microsoft installer download + run per user, `.dotnet/` directory ownership fixup. | 1 |
| `odem.development.espidf` | apt deps, per-version clone + install (multi-version loop), per-version activator script deployment. | 2 |
| `odem.development.latex` | Single `apt` install of `texlive-full`. Per-user loop. | 1 |
| `odem.development.lmstudio` | Stat-gated CLI + appimage download, .desktop entry generated inline. | 2 |
| `odem.development.unity` | Keyring dearmor, `apt_repository` with `signed-by=`, unity packages, conditional VS Code deb install. | 2 |

## Conventions

- All per-user loops use `block:` wrappers with `loop: "{{ identity_users_resolved | odem_filter_users('development_<x>') }}"`.
- Multi-version loops (espidf) nest inside the per-user block: block iterates per user, inner task iterates over `espidf_versions`.
- Stat-gated installs (`opencode`, `lmstudio`) skip the download step if the binary already exists.
