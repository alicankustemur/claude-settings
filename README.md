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
| **Kubernetes** | `kubectl`, `eksctl`, `helm` |
| **Terraform** | `terraform plan`, `terraform lint`, `terraform init`, `terraform validate` |
| **Git** | `git commit`, `git branch`, `git pull`, `git push`, `git status`, `git diff`, `git add`, `git checkout`, `git stash`, `git log` |
| **Containers** | `docker`, `docker-compose` |
| **Languages** | `go`, `python`, `python3`, `node`, `npm` |
| **Package Managers** | `pip`, `pip3` |
| **Cloud** | `aws` |
| **Network** | `ssh`, `curl`, `wget`, `nc` |
| **Data Processing** | `jq`, `yq`, `grep`, `sed`, `awk`, `tr`, `cut`, `paste`, `column`, `sort`, `uniq`, `wc` |
| **Build** | `make` |
| **File Operations** | `ls`, `cp`, `mv`, `mkdir`, `rmdir`, `touch`, `cat`, `head`, `tail`, `less`, `more`, `find`, `diff`, `file`, `stat`, `tree` |
| **Navigation** | `cd`, `pwd`, `basename`, `dirname`, `realpath` |
| **Permissions** | `chmod`, `chown` |
| **Compression** | `tar`, `zip`, `unzip`, `gzip`, `gunzip` |
| **System** | `echo`, `env`, `export`, `source`, `which`, `whoami`, `date`, `df`, `du`, `ps`, `top`, `htop`, `kill`, `history`, `xargs`, `tee` |
