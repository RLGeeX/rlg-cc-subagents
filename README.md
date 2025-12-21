# CC-Unleashed Agents

61 specialized agents for Claude Code, designed to work with [cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed) plugin.

**Version:** 1.1.1
**Agents:** 61
**License:** MIT

## Overview

Standalone agents are markdown files with YAML frontmatter that Claude Code can automatically discover and use:

- **Auto-Delegation**: Claude automatically picks the right expert for your task
- **Explicit Invocation**: Call specific agents with `@agent-name` syntax
- **Tool Access**: Each agent inherits all MCP tools from the main thread

## Installation

```bash
git clone https://github.com/RLGeeX/rlg-cc-subagents ~/.claude/agents/cc-unleashed
```

Verify with `@` autocomplete in Claude Code to see available agents.

## Usage

### Explicit Invocation

```
@python-pro help me optimize this async code
@terraform-specialist review my module structure
@code-reviewer review this implementation
```

### Auto-Delegation

Just describe your task - Claude selects the right agent:

```
Help me write a FastAPI endpoint with proper validation
Review my Terraform state management strategy
Check this API for security vulnerabilities
```

### With Plugin

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
├── README.md
├── agents-catalog.md
└── agents/
    ├── core/                 # 2 agents
    ├── development/          # 18 agents
    ├── infrastructure/       # 13 agents
    ├── kubernetes/           # 4 agents
    ├── product-management/   # 7 agents
    ├── quality/              # 11 agents
    ├── creative/             # 3 agents
    ├── ai-ml/                # 2 agents
    └── business/             # 1 agent
```

## Related

- [cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed) - Plugin with skills, commands, and planning

## License

MIT License

## Support

Issues: https://github.com/RLGeeX/rlg-cc-subagents/issues
