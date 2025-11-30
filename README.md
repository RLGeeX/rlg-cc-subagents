# CC-Unleashed Agents

Standalone specialized agents for [cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed) Claude Code plugin.

[![Version](https://img.shields.io/badge/version-2.5.0-blue.svg)](https://github.com/RLGeeX/rlg-cc-subagents/releases)
[![License](https://img.shields.io/badge/license-MIT-green.svg)](LICENSE)
[![Agents](https://img.shields.io/badge/agents-59-orange.svg)](agents-catalog.md)

---

## Overview

This repository contains **59 specialized agents** for Claude Code, covering development, infrastructure, quality, and product management. Each agent is an expert in specific technologies, frameworks, or workflows, designed to help you build better software faster.

### What are Standalone Agents?

Standalone agents are markdown files with YAML frontmatter that Claude Code can automatically discover and use. They enable:

- **Auto-Delegation**: Claude automatically picks the right expert for your task
- **Explicit Invocation**: Call specific agents with `@agent-name` syntax
- **Tool Access**: Each agent has specific capabilities and tool access
- **Independent Installation**: Use agents without installing the full plugin

---

## Quick Start

### Installation

**Option 1: Standalone (Agents Only)**
```bash
# Clone the repository
git clone https://github.com/RLGeeX/rlg-cc-subagents.git ~/rlg-cc-subagents

# Create the agents directory if it doesn't exist
mkdir -p ~/.claude/agents

# Symlink to activate agents
ln -sf ~/rlg-cc-subagents/agents ~/.claude/agents/cc-unleashed

# Verify installation
ls -la ~/.claude/agents/cc-unleashed  # Should show all agent files
```

**Option 2: With Plugin (Recommended)**
```bash
# Clone both repositories
git clone https://github.com/RLGeeX/rlg-cc-unleashed.git ~/rlg-cc-unleashed
git clone https://github.com/RLGeeX/rlg-cc-subagents.git ~/rlg-cc-subagents

# Install the plugin first
/plugin install ~/rlg-cc-unleashed

# Create the agents directory if it doesn't exist
mkdir -p ~/.claude/agents

# Symlink to activate agents
ln -sf ~/rlg-cc-subagents/agents ~/.claude/agents/cc-unleashed
```

**Option 3: Monorepo Setup (Development)**
```bash
# If you have the monorepo already cloned
cd /path/to/rlg-cc

# Install plugin from monorepo
/plugin install rlg-cc-unleashed

# Create the agents directory if it doesn't exist
mkdir -p ~/.claude/agents

# Symlink agents from monorepo
ln -sf $(pwd)/rlg-cc-subagents/agents ~/.claude/agents/cc-unleashed
```

### Verify Installation

```bash
# Check symlink is correct
ls -la ~/.claude/agents/cc-unleashed
# Should point to: /path/to/rlg-cc-subagents/agents

# Verify agents are accessible
ls ~/.claude/agents/cc-unleashed/development/
# Should show: python-pro.md, react-specialist.md, etc.

# In Claude Code, agents should be auto-discoverable:
# - Type "@" to see available agents
# - Use agent names in commands: @python-pro, @code-reviewer, etc.
```

---

## Usage

### Explicit Invocation

Call specific agents directly:

```bash
# Python development
claude "Use @python-pro to explain async/await patterns"

# Infrastructure
claude "Use @terraform-specialist to review this module"

# Code review
claude "Use @code-reviewer to review my implementation"

# Kubernetes
claude "Use @k8s-architect to design my deployment"
```

### Auto-Delegation

Let Claude pick the right agent automatically:

```bash
# Claude selects python-pro automatically
claude "Help me optimize this Python script for async processing"

# Claude selects terraform-specialist automatically
claude "Review my Terraform state management strategy"

# Claude selects code-reviewer automatically
claude "Review this completed feature against the plan"
```

### With Plugin Skills

Use agents in workflows via the cc-unleashed plugin:

```bash
# Create a plan (agent auto-selected per task)
/cc-unleashed:plan-new "Add authentication system"

# Execute the plan (uses specified agents)
/cc-unleashed:plan-next

# TDD workflow (uses python-pro or similar)
/cc-unleashed:tdd

# Code review (uses code-reviewer)
/cc-unleashed:review
```

---

## Agent Categories

### Core (3 agents)

Foundational agents for code quality and documentation:

- **tdd-enforcer** - Enforces test-driven development practices
- **doc-assistant** - Maintains documentation quality
- **orchestrator** - Coordinates complex multi-agent workflows

### Development (13 agents)

Software development specialists:

- **python-pro** - Python/FastAPI/async expert
- **react-specialist** - React/component development
- **backend-architect** - Backend architecture & API design
- **frontend-developer** - Modern frontend development
- **fullstack-developer** - End-to-end application development
- **fastapi-developer** - FastAPI async APIs
- **microservices-architect** - Distributed systems design
- **postgres-pro** - PostgreSQL database specialist
- **api-designer** - REST/GraphQL API design
- **api-documenter** - API documentation
- **dotnet-core-expert** - .NET Core development
- **csharp-developer** - C# programming
- **ui-designer** - Visual UI/UX design

### Infrastructure (8 agents)

DevOps and cloud specialists:

- **terraform-specialist** - Terraform/OpenTofu IaC expert
- **cloud-architect** - Multi-cloud architecture (AWS/Azure/GCP)
- **devops-engineer** - CI/CD and automation
- **deployment-engineer** - Deployment automation & GitOps
- **sre-engineer** - Site reliability engineering
- **incident-responder** - Production incident response
- **database-administrator** - Database management
- **security-engineer** - Infrastructure security & DevSecOps

### Kubernetes (4 agents)

Container orchestration specialists:

- **k8s-architect** - Kubernetes architecture & platform engineering
- **helm-specialist** - Helm charts & package management
- **gitops-engineer** - ArgoCD/Flux & progressive delivery
- **k8s-security** - Kubernetes security & compliance

### Product Management (7 agents)

PM, documentation, and team facilitation:

- **product-manager** - Product strategy & roadmaps
- **scrum-master** - Agile ceremonies & sprint planning
- **business-analyst** - Requirements & business intelligence
- **technical-writer** - Technical documentation
- **documentation-engineer** - Documentation systems
- **jira-specialist** - JIRA workflows & project management
- **story-writer** - User stories & requirements

### Quality (10 agents)

Testing, review, and security:

- **code-reviewer** - Code review & quality standards
- **architect-reviewer** - Architecture review & validation
- **test-automator** - Test automation strategies
- **qa-expert** - QA processes & quality assurance
- **debugger** - Debugging & troubleshooting
- **security-auditor** - Security audits & penetration testing
- **build-engineer** - Build optimization & compilation
- **git-workflow-manager** - Git workflows & branching
- **dependency-manager** - Dependency management & security
- **chaos-engineer** - Chaos engineering & resilience

See [agents/INDEX.md](agents/INDEX.md) for complete catalog with descriptions.

---

## Agent Format

Each agent follows the standalone format with YAML frontmatter:

```markdown
---
name: python-pro
description: Expert Python developer specializing in modern async patterns, FastAPI, and type-safe code. Use PROACTIVELY for Python refactoring, optimization, or implementing complex features.
category: development
model: sonnet
version: 1.0.0
---

# Python Pro

[Agent instructions and capabilities...]
```

### Fields

- **name**: Simple agent identifier (no prefixes)
- **description**: Detailed description for auto-delegation
- **category**: One of: core, development, infrastructure, kubernetes, product-management, quality, ai-ml, business
- **model**: Claude model (sonnet, haiku, opus)
- **version**: Semantic version

### Tool Access

**All agents inherit tools from the main thread**, including:
- **Core Tools:** Read, Write, Edit, Bash, Glob, Grep, Task, etc.
- **All MCP Tools:** Jira, Context7, Tavily, Playwright, and any future MCP servers

Agents no longer specify a `tools:` field in their YAML frontmatter. This ensures:
- ✅ Automatic access to new MCP tools as they're installed
- ✅ Consistent tool availability across all agents
- ✅ Reduced maintenance overhead
- ✅ Future-proof configuration

Agents use only the tools they need from the inherited set.

---

## Examples

### Python Development

```bash
# Get help with async patterns
claude "Use @python-pro to explain the difference between asyncio.gather and asyncio.wait"

# Optimize code
claude "Use @python-pro to optimize this data processing pipeline for async execution"

# Auto-delegation
claude "Help me write a FastAPI endpoint with proper error handling and validation"
```

### Infrastructure Automation

```bash
# Terraform review
claude "Use @terraform-specialist to review my state locking strategy"

# Cloud architecture
claude "Use @cloud-architect to design a multi-region failover solution on AWS"

# Auto-delegation
claude "How should I structure my Terraform modules for a multi-environment setup?"
```

### Code Quality

```bash
# Code review
claude "Use @code-reviewer to review this authentication implementation against the plan"

# Security audit
claude "Use @security-auditor to check this API for vulnerabilities"

# Auto-delegation
claude "Review this completed feature for security issues and performance problems"
```

### Kubernetes

```bash
# K8s architecture
claude "Use @k8s-architect to design a platform for multi-tenant applications"

# Helm charts
claude "Use @helm-specialist to create a reusable chart for my microservices"

# Auto-delegation
claude "How should I configure HPA and resource limits for this deployment?"
```

---

## Integration with cc-unleashed Plugin

These agents integrate seamlessly with the [cc-unleashed plugin](https://github.com/RLGeeX/rlg-cc-unleashed):

### Planning System

The plugin's planning system automatically selects appropriate agents:

```bash
/cc-unleashed:plan-new "Add payment processing"
# Creates micro-chunked plan with agent assignments:
# - Task 1: **Agent:** python-pro (API implementation)
# - Task 2: **Agent:** postgres-pro (Database schema)
# - Task 3: **Agent:** security-auditor (Security review)
# - Task 4: **Agent:** test-automator (Integration tests)
```

### Workflow Skills

Agents power workflow skills (requires cc-unleashed plugin):

- `/cc-unleashed:tdd` - Uses python-pro/react-specialist for TDD
- `/cc-unleashed:review` - Uses code-reviewer for reviews
- `/cc-unleashed:debug` - Uses debugger for troubleshooting
- `/cc-unleashed:brainstorm` - Uses appropriate specialist for ideation

### Dynamic Execution

```bash
/cc-unleashed:plan-next
# Executes next task with its assigned agent
# Agent automatically loaded based on plan
```

---

## Directory Structure

```
rlg-cc-subagents/
├── README.md                      # This file
├── LICENSE                        # MIT License
├── agents/
│   ├── INDEX.md                   # Complete agent catalog
│   ├── core/                      # Core agents (3)
│   │   ├── tdd-enforcer.md
│   │   ├── doc-assistant.md
│   │   └── orchestrator.md
│   ├── development/               # Development agents (13)
│   │   ├── python-pro.md
│   │   ├── react-specialist.md
│   │   └── ...
│   ├── infrastructure/            # Infrastructure agents (8)
│   │   ├── terraform-specialist.md
│   │   ├── cloud-architect.md
│   │   └── ...
│   ├── kubernetes/                # Kubernetes agents (4)
│   │   ├── k8s-architect.md
│   │   └── ...
│   ├── product-management/        # PM agents (7)
│   │   ├── product-manager.md
│   │   └── ...
│   └── quality/                   # Quality agents (10)
│       ├── code-reviewer.md
│       └── ...
└── .gitignore
```

---

## Contributing

We welcome contributions! Here's how to add or improve agents:

### Adding a New Agent

1. Create markdown file in appropriate category directory
2. Add YAML frontmatter with required fields
3. Write clear, detailed agent instructions
4. Test with explicit invocation and auto-delegation
5. Submit pull request

### Agent Guidelines

- **Clear descriptions**: Enable effective auto-delegation
- **Specific expertise**: Focus on particular technologies/patterns
- **Tool access**: Only include necessary tools
- **Model selection**: Use sonnet for most, haiku for simple tasks
- **Examples**: Include usage examples in the agent content

### Pull Request Process

1. Fork the repository
2. Create feature branch (`git checkout -b feature/new-agent`)
3. Add/modify agent file
4. Update INDEX.md if adding new agent
5. Test agent functionality
6. Commit with clear message (`feat: add rust-developer agent`)
7. Push and create pull request

---

## Versioning

We use [Semantic Versioning](https://semver.org/):

- **MAJOR**: Breaking changes to agent format or structure
- **MINOR**: New agents added or significant improvements
- **PATCH**: Bug fixes, description improvements, minor updates

Current version: **2.1.0**

---

## License

This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.

---

## Related Projects

- **[rlg-cc-unleashed](https://github.com/RLGeeX/rlg-cc-unleashed)** - Claude Code plugin with skills, commands, and planning
- **[rlg-cc](https://github.com/RLGeeX/rlg-cc)** - Monorepo workspace containing both plugin and agents

---

## Support

- **Issues**: [GitHub Issues](https://github.com/RLGeeX/rlg-cc-subagents/issues)
- **Discussions**: [GitHub Discussions](https://github.com/RLGeeX/rlg-cc-subagents/discussions)
- **Documentation**: See [agents/INDEX.md](agents/INDEX.md) for agent catalog

---

## Changelog

### [2.1.0] - 2025-11-14

#### Added
- Initial release of standalone agents repository
- 45 specialized agents across 6 categories
- YAML frontmatter format for Claude Code auto-delegation
- Complete agent catalog with INDEX.md
- Integration with cc-unleashed plugin v2.1.0
- Three installation options: standalone, with plugin, or monorepo

#### Changed
- Migrated from rlg-cc-unleashed plugin to separate repository
- Simplified agent names (removed `cc-unleashed:category:` prefixes)
- Converted all agents to standalone format with YAML frontmatter
- Agents now installed via symlink to `~/.claude/agents/cc-unleashed/`

#### Fixed
- Corrected product-manager agent name in documentation
- Updated installation instructions with symlink activation steps

---

**Made with ❤️ for the Claude Code community**
