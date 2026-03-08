# amped-research-kit
ARK is an open source Claude skills kit for UX and market researchers. Plug in ready-made research workflows, tune them to your team, and contribute back what you build. Built by researchers for researchers (and PwDR).

## Structure

```
amped-research-kit/
├── skills/       # Research workflow skills
├── docs/         # Documentation
└── examples/     # Example configurations
```

## Skills

| Skill | What it does | Status |
|---|---|---|
| usability-test-plan-builder | Generates a structured usability test plan from a brief you provide | available |
<!-- Add new skill rows here as they are contributed -->

## Who This Is For

- **UX researchers** who want ready-made workflows for common research tasks
- **Market researchers** looking for structured templates and guides they can adapt
- **Research ops** teams who want a shareable, version-controlled skill library
- **PwDR (people with disabilities who do research)** for whom plain, structured workflows reduce friction and cognitive load

## Quick Start

**1. Install a skill**

Copy the skill folder into your Claude skills directory. You can install it globally or per project.

Global install (available in any project):
```
~/.claude/skills/
```

Project-level install (only available in that project):
```
your-project/.claude/skills/
```

For example, to install `usability-test-plan-builder`:
```
cp -r skills/usability-test-plan-builder ~/.claude/skills/
```

**2. Invoke a skill in Claude Code**

Once the skill folder is in place, call it by name inside Claude Code using a slash command:

```
/usability-test-plan-builder
```

Claude will prompt you for any inputs the skill needs and then run the workflow.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md) for guidelines. Contributions of new research workflow skills, improvements to existing ones, and documentation fixes are all welcome.
