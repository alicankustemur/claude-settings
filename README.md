# Claude Code Settings

My personal [Claude Code](https://claude.ai/claude-code) configuration.

## Installation

### Settings
Copy `settings.json` to `~/.claude/settings.json`:

```bash
curl -o ~/.claude/settings.json https://raw.githubusercontent.com/alicankustemur/claude-settings/main/settings.json
```

### MCP Servers
Run these commands to install the MCP servers:

```bash
# Kubernetes - manage clusters, pods, deployments
claude mcp add -s user kubernetes -- npx -y mcp-server-kubernetes

# Terraform - infrastructure as code
claude mcp add -s user terraform -- npx -y @anthropic/terraform-mcp-server

# GitHub - PRs, issues, repos (replace YOUR_TOKEN)
claude mcp add -s user github -e GITHUB_PERSONAL_ACCESS_TOKEN=YOUR_TOKEN -- npx -y @modelcontextprotocol/server-github

# AWS Documentation - search AWS docs
claude mcp add -s user aws-docs -- uvx awslabs.aws-documentation-mcp-server

# AWS API - interact with AWS services
claude mcp add -s user aws-api -- uvx awslabs.aws-api-mcp-server

# MySQL - database queries
claude mcp add -s user mysql -- npx -y @benborla29/mcp-server-mysql
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
| **System** | `echo`, `env`, `export`, `source`, `which`, `whoami`, `date`, `df`, `du`, `ps`, `top`, `htop`, `history`, `xargs`, `tee` |

### MCP Servers

| Server | Purpose |
|--------|---------|
| **kubernetes** | Manage K8s clusters, pods, deployments, services |
| **terraform** | Terraform Registry, providers, modules lookup |
| **github** | PRs, issues, repos, code search |
| **aws-docs** | Search AWS documentation |
| **aws-api** | Interact with AWS services directly |
| **mysql** | Query MySQL databases |
