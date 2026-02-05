# Claude Code Settings

My personal [Claude Code](https://claude.ai/claude-code) configuration.

## Installation

Copy `settings.json` to `~/.claude/settings.json`:

```bash
curl -o ~/.claude/settings.json https://raw.githubusercontent.com/alicankustemur/claude-settings/main/settings.json
```

## Configuration

### Attribution

Disables the "Co-Authored-By: Claude" line in git commit messages.

### Allowed Commands

The following commands run without approval prompts:

| Category | Commands |
|----------|----------|
| **Kubernetes** | `kubectl` |
| **Terraform** | `terraform plan`, `terraform lint`, `terraform init`, `terraform validate` |
| **Git** | `git commit`, `git branch`, `git pull`, `git status`, `git diff` |
| **Containers** | `docker`, `docker-compose`, `helm` |
| **Languages** | `go` |
| **Cloud** | `aws` |
| **Other** | `grep` |
