# CC-Unleashed Agents

61 specialized subagents for Claude Code, designed as a companion plugin to [cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed).

**Version:** 1.0.0
**Agents:** 61
**License:** MIT

## Overview

This is a Claude Code **plugin** containing 61 specialized agents organized by category. Agents are auto-discovered and can be invoked:

- **Auto-Delegation**: Claude automatically picks the right expert via the Task tool
- **Plugin Namespacing**: Agents are namespaced as `cc-unleashed-agents:category:agent-name`
- **Tool Access**: Each agent inherits all MCP tools from the main thread

## Installation

### As Plugin (Recommended)

```bash
# Clone to your plugins directory
git clone https://github.com/RLGeeX/rlg-cc-subagents ~/path/to/plugins/cc-unleashed-agents

# Add to Claude Code
claude /plugin add ~/path/to/plugins/cc-unleashed-agents
```

Or add directly from GitHub:

```bash
claude /plugin add https://github.com/RLGeeX/rlg-cc-subagents
```

Verify with `/plugin list` to see `cc-unleashed-agents`.

## Usage

### Via Task Tool (Primary Method)

Claude uses the Task tool to delegate to agents based on your request:

```
Help me write a FastAPI endpoint with proper validation
Review my Terraform state management strategy
Check this API for security vulnerabilities
```

### With CC-Unleashed Plugin

Use agents in workflows via the cc-unleashed plugin:

```
/cc-unleashed:plan-new "Add authentication"  # Agents auto-assigned per task
/cc-unleashed:tdd                             # Uses appropriate specialist
/cc-unleashed:review                          # Uses code-reviewer
```

## Agent Categories

| Category | Count | Examples |
|----------|-------|----------|
| Core | 2 | tdd-enforcer, doc-assistant |
| Development | 18 | python-pro, react-specialist, fastapi-pro, backend-architect |
| Infrastructure | 13 | terraform-specialist, cloud-architect, devops-engineer, sre-engineer |
| Kubernetes | 4 | k8s-architect, helm-specialist, gitops-engineer, k8s-security |
| Quality | 11 | code-reviewer, test-automator, debugger, security-auditor |
| Product Management | 7 | product-manager, scrum-master, jira-specialist, story-writer |
| Creative | 3 | ghost-writer, copy-editor, content-reviewer |
| AI/ML | 2 | langgraph-specialist, vector-search-specialist |
| Business | 1 | financial-data-analyst |

See [agents-catalog.md](agents-catalog.md) for complete catalog with descriptions.

## Agent Format

Each agent follows the standalone format:

```markdown
---
name: python-pro
description: Expert Python developer specializing in modern async patterns...
category: development
model: sonnet
version: 1.0.0
---

# Python Pro

[Agent instructions...]
```

**Tool Access:** All agents inherit tools from the main thread (Read, Write, Edit, Bash, MCP tools, etc.).

## Directory Structure

```
rlg-cc-subagents/
├── .claude-plugin/
│   └── plugin.json           # Plugin manifest
├── README.md
├── AGENT-TEMPLATE.md         # Template for new agents
├── agents-catalog.md         # Full catalog with descriptions
└── agents/
    ├── ai-ml/                # 2 agents
    ├── business/             # 1 agent
    ├── core/                 # 2 agents
    ├── creative/             # 3 agents
    ├── development/          # 18 agents
    ├── infrastructure/       # 13 agents
    ├── kubernetes/           # 4 agents
    ├── product-management/   # 7 agents
    └── quality/              # 11 agents
```

## Agent Namespacing

Plugin agents with subdirectories are namespaced as `plugin:category:agent-name`:

- `cc-unleashed-agents:development:python-pro`
- `cc-unleashed-agents:infrastructure:terraform-specialist`
- `cc-unleashed-agents:quality:code-reviewer`

## Related

- [cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed) - Plugin with skills, commands, and planning

## License

MIT License

## Support

Issues: https://github.com/RLGeeX/rlg-cc-subagents/issues
