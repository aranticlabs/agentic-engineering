<div align="center">
    <picture>
        <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/aranticlabs/arantic-docs/main/static/img/brand/arantic-logo-dark.svg" />
        <img src="https://raw.githubusercontent.com/aranticlabs/arantic-docs/main/static/img/brand/arantic-logo-light.svg" width="400" alt="Arantic Skills" />
    </picture><br /><br />
    <p>A library of Claude Code skills from Arantic Labs.<br />
    Reusable, ready-to-install skills for planning, specs, reviews, and AI-assisted development workflows.</p>
</div>

# Arantic Skills

A curated collection of [Claude Code](https://docs.claude.com/en/docs/claude-code) skills built and maintained by Arantic Labs. Each skill is a self-contained directory with a `SKILL.md` file that Claude Code can load to extend its capabilities with domain-specific workflows.

## What's inside

Skills will be added here over time. Each skill lives in its own directory at the root of this repo.

---

## Installing a skill

Skills can be installed at the **user level** (available in every project) or at the **project level** (scoped to a single repo).

### User-level (global)

```bash
git clone https://github.com/aranticlabs/skills.git
cp -r skills/<skill-name> ~/.claude/skills/
```

The skill is now available in every Claude Code session as `/<skill-name>`.

### Project-level

```bash
mkdir -p .claude/skills
cp -r /path/to/skills/<skill-name> .claude/skills/
```

The skill is available only inside this project, and can be committed alongside your code.

### Verify

Inside Claude Code, type `/` and you should see the skill listed.

---

## Using a skill

In a Claude Code session, invoke a skill by name:

```
/<skill-name>
```

Or simply describe the task in natural language — Claude Code will trigger the relevant skill based on its `description` frontmatter.

---

## Skill format

Each skill is a directory containing a `SKILL.md` file with YAML frontmatter:

```markdown
---
name: skill-name
description: When to invoke this skill and what it does.
model: opus
---

# Skill Name

Instructions for Claude to follow when this skill is invoked...
```

The `description` field is what Claude uses to decide when to load the skill, so it should clearly state the trigger conditions.

For a full guide to authoring skills, see the [Skills section of Arantic Docs](https://github.com/aranticlabs/arantic-docs).

---

Built and maintained by [Arantic Digital](https://arantic.com).
