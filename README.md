# Claude Code Settings

My personal [Claude Code](https://claude.ai/claude-code) configuration.

## Installation

### Settings
```bash
curl -o ~/.claude/settings.json https://raw.githubusercontent.com/alicankustemur/claude-settings/main/settings.json
```

### MCP Servers
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

### Skills/Plugins
```bash
# Terraform skill by Anton Babenko
git clone https://github.com/antonbabenko/terraform-skill ~/.claude/skills/terraform-skill
```

## Configuration

### Attribution
Disables the "Co-Authored-By: Claude" line in git commit messages.

### Allowed Commands

| Category | Commands |
|----------|----------|
| **Kubernetes** | `kubectl`, `eksctl`, `helm` |
| **Terraform** | `terraform plan/lint/init/validate` |
| **Git** | All git commands, `gh` CLI |
| **Containers** | `docker`, `docker-compose` |
| **Languages** | `go`, `python`, `python3`, `node`, `ruby`, `swift`, `java`, `rustc` |
| **Package Managers** | `npm`, `npx`, `yarn`, `pnpm`, `pip`, `pip3`, `brew`, `cargo`, `gem`, `bundle`, `pod`, `uvx`, `uv` |
| **Build Tools** | `make`, `mvn`, `gradle`, `xcodebuild` |
| **Cloud** | `aws` |
| **Network** | `ssh`, `scp`, `rsync`, `curl`, `wget`, `nc`, `ping`, `traceroute`, `dig`, `nslookup`, `telnet`, `nmap`, `netstat`, `ss`, `ifconfig` |
| **Data Processing** | `jq`, `yq`, `grep`, `sed`, `awk`, `tr`, `cut`, `paste`, `column`, `sort`, `uniq`, `wc`, `bc`, `expr` |
| **File Operations** | `ls`, `cp`, `mv`, `mkdir`, `rmdir`, `touch`, `cat`, `head`, `tail`, `less`, `more`, `find`, `diff`, `file`, `stat`, `tree`, `ln`, `readlink` |
| **Compression** | `tar`, `zip`, `unzip`, `gzip`, `gunzip` |
| **Crypto** | `openssl`, `base64`, `md5`, `shasum` |
| **System** | `ps`, `top`, `htop`, `df`, `du`, `lsof`, `uname`, `hostname`, `uptime`, `vmstat`, `iostat`, `id`, `groups` |
| **Terminal** | `tmux`, `screen`, `nohup`, `time`, `timeout`, `watch`, `sleep`, `wait` |
| **Claude** | `claude` CLI |

### MCP Servers

| Server | Purpose |
|--------|---------|
| **kubernetes** | Manage K8s clusters, pods, deployments, services |
| **terraform** | Terraform Registry, providers, modules lookup |
| **github** | PRs, issues, repos, code search |
| **aws-docs** | Search AWS documentation |
| **aws-api** | Interact with AWS services directly |
| **mysql** | Query MySQL databases |

### Skills/Plugins

| Skill | Purpose |
|-------|---------|
| **terraform-skill** | Terraform best practices, module generation, code review |
