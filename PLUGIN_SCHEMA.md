# Plugin Schema Documentation

This document describes the schema for creating plugins in this marketplace.

## Marketplace Manifest

The `.claude-plugin/marketplace.json` file defines the marketplace metadata and lists all available plugins.

```json
{
  "name": "marketplace-name",
  "metadata": {
    "description": "Marketplace description",
    "version": "0.1.0"
  },
  "owner": {
    "name": "owner-name",
    "url": "https://github.com/owner"
  },
  "homepage": "https://github.com/owner/repo",
  "plugins": [
    {
      "name": "plugin-name",
      "source": "./plugins/plugin-name",
      "description": "Plugin description",
      "category": "category-name"
    }
  ]
}
```

### Marketplace Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| name | string | Yes | Unique marketplace identifier |
| metadata.description | string | No | Marketplace description |
| metadata.version | string | No | Marketplace version |
| owner.name | string | Yes | Owner name |
| owner.url | string | No | Owner URL |
| homepage | string | No | Marketplace homepage URL |
| plugins | array | Yes | List of plugin entries |

### Plugin Entry Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| name | string | Yes | Plugin name |
| source | string | Yes | Path to plugin directory |
| description | string | No | Plugin description |
| category | string | No | Plugin category |
| tags | array | No | Plugin tags |
| strict | boolean | No | When `true` (default), marketplace fields supplement plugin.json. When `false`, marketplace entry serves as complete manifest if no plugin.json exists |

## Plugin Manifest

Each plugin has its own `.claude-plugin/plugin.json` file.

```json
{
  "name": "plugin-name",
  "description": "Plugin description",
  "version": "1.0.0",
  "author": {
    "name": "Author Name",
    "url": "https://github.com/author"
  },
  "homepage": "https://plugin-homepage.com",
  "keywords": ["keyword1", "keyword2"],
  "commands": "./commands/",
  "agents": "./agents/",
  "skills": "./skills/",
  "hooks": "./hooks/"
}
```

### Plugin Fields

| Field | Type | Required | Description |
|-------|------|----------|-------------|
| name | string | Yes | Plugin name (must match directory name) |
| description | string | No | Plugin description |
| version | string | No | Plugin version (semver) |
| author.name | string | No | Author name |
| author.email | string | No | Author email |
| author.url | string | No | Author URL |
| homepage | string | No | Plugin homepage |
| repository | string | No | Repository URL |
| license | string | No | License identifier |
| keywords | array | No | Search keywords |
| commands | string | No | Path to commands directory |
| agents | string | No | Path to agents directory |
| skills | string | No | Path to skills directory |
| hooks | string | No | Path to hooks directory |

## Command Files

Commands are defined as Markdown files in the `commands/` directory.

### Command Frontmatter

```yaml
---
name: command-name
description: Command description
allowed_tools:
  - Bash(git diff:*)
  - Bash(git log:*)
---
```

### Command Body

The body of the command file contains instructions for Claude when the command is invoked.

## Agent Files

Agents are defined as Markdown files in the `agents/` directory.

### Agent Frontmatter

```yaml
---
name: agent-name
description: Agent description
---
```

## Skill Files

Skills are defined as Markdown files in the `skills/` directory.

### Skill Frontmatter

```yaml
---
name: skill-name
description: Skill description
---
```

## Directory Structure Example

```
plugins/
└── my-plugin/
    ├── .claude-plugin/
    │   └── plugin.json
    ├── commands/
    │   ├── review.md
    │   └── test.md
    ├── agents/
    │   └── developer.md
    ├── skills/
    │   └── debugging.md
    └── hooks/
        └── pre-commit.md
```

## Environment Variables

Use `${CLAUDE_PLUGIN_ROOT}` to reference the plugin root directory in paths within your configuration.
