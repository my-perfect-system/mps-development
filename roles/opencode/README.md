---
# Reference doc — auto-generated, do not edit by hand.
# Regenerate via: python3 manage/gen_role_readmes.py
namespace: mps
collection: development
role: opencode
---

# `mps.development.opencode`

Install OpenCode CLI + per-user dotfiles (~/.config/opencode, ~/.claude)

## Default variables

| Variable | Default | Description |
|---|---|---|
| `opencode_claude_dst` | `.claude` | Home-relative destination for the Claude Code dotfiles |
| `opencode_claude_src` | `{{ opencode_dotfiles_root }}/.claude/` | Source path for the Claude Code dotfiles tree |
| `opencode_cli_bin` | `.opencode/bin/opencode` | Home-relative path where the OpenCode CLI lands after install |
| `opencode_config_dst` | `.config` | Home-relative destination for the opencode config dotfiles |
| `opencode_config_src` | `{{ opencode_dotfiles_root }}/.config/opencode/` | Source path for the opencode config dotfiles |
| `opencode_dotfiles_root` | `{{ role_path }}/files/dotfiles` | Role-relative path to the dotfiles root |
| `opencode_installer_path` | `/tmp/opencode-install.sh` | Where the installer script is staged |
| `opencode_installer_url` | `https://opencode.ai/install` | URL of the OpenCode installer script |

## Dependencies

- `mps.base.identity`

## Example usage

```yaml
- hosts: all
  roles:
    - mps.development.opencode
```

## Role metadata

- **Min Ansible version**: `2.16.0`
- **License**: G, P, L, -, 3, ., 0, -, o, r, -, l, a, t, e, r
- **Platforms**: Debian (trixie)
- **Tasks file lines**: 82
