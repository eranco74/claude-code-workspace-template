# Claude Code Workspace Template

A ready-to-go project workspace template for AI-assisted software development using [Claude Code](https://docs.anthropic.com/en/docs/claude-code) with the [GSD (Get Stuff Done)](https://github.com/cyanheads/gsd) workflow system.

## What This Is

This template provides the scaffolding for managing a software project with Claude Code as your AI pair-programmer. It includes:

- **CLAUDE.md** -- Project instructions that Claude Code reads automatically
- **`.claude/settings.json`** -- Permission presets for common commands
- **`.planning/`** -- GSD workflow directory structure (planning, tracking, state)
- **`.gitignore`** -- Sensible defaults for AI-assisted development

## Quick Start

```bash
# Option 1: Clone this template
git clone <this-repo-url> my-project
cd my-project
rm -rf .git && git init

# Option 2: Copy into an existing project
cp -r claude-code-workspace-template/.  my-project/
```

Then customize:

1. **Edit `CLAUDE.md`** -- Replace placeholder sections with your project's context, commands, and conventions
2. **Edit `.planning/config.json`** -- Adjust GSD workflow settings
3. **Start working** -- Run `claude` in your project directory

## What's Included

```
.
├── CLAUDE.md                    # Project instructions for Claude Code
├── .claude/
│   └── settings.json            # Pre-approved shell commands
├── .planning/
│   └── config.json              # GSD workflow configuration
├── .gitignore                   # Ignores credentials, editor files, planning artifacts
└── README.md                    # This file
```

## GSD Workflow

The GSD system structures your work into milestones, phases, and plans:

```
/gsd:new-project     # Initialize project with requirements gathering
/gsd:plan-phase      # Plan the next phase of work
/gsd:execute-phase   # Execute a planned phase
/gsd:progress        # Check current project status
/gsd:next            # Advance to the next logical step
```

GSD creates and manages files under `.planning/` automatically. The `config.json` seeds its behavior.

## CLAUDE.md Guide

The `CLAUDE.md` file is the most important file in this template. It tells Claude Code:

- **What your project is** -- so it understands context
- **How to build and test** -- so it can run the right commands
- **What conventions to follow** -- so its code matches your style
- **What to avoid** -- so it doesn't make common mistakes

The template includes commented sections for each of these. Fill them in as your project evolves.

## Customizing Permissions

`.claude/settings.json` pre-approves safe, read-only commands (git status, ls, cat, etc.). Add your own:

```json
{
  "permissions": {
    "allow": [
      "Bash(make:*)",
      "Bash(npm test:*)",
      "Bash(go build:*)"
    ]
  }
}
```

See [Claude Code docs](https://docs.anthropic.com/en/docs/claude-code/settings) for the full permissions reference.

## Tips

- **Start small** -- Let CLAUDE.md grow organically as you discover what Claude needs to know
- **Use GSD for multi-step work** -- Single-step tasks don't need the full workflow
- **Commit CLAUDE.md** -- It's project documentation that benefits the whole team
- **Keep `.planning/` gitignored** -- It's your personal workspace state (the default `.gitignore` does this)
