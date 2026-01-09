# VPVR Skills Hub

This is the central repository for Villa Paraiso Vacation Rentals Claude AI skills.

## Project Structure

```
vpvr-skills/
├── skill-from-masters/    # Tool for creating new skills
├── marketing/             # Marketing department skills
├── operations/            # Operations department skills
├── guest-services/        # Guest services skills
├── finance/               # Finance & accounting skills
├── sales/                 # Sales department skills
└── shared/                # Cross-department skills
```

## Working with Skills

### Adding a New Skill

1. Use the `skill-from-masters` skill to create a new skill based on expert methodologies
2. Place the skill in the appropriate department folder
3. Each skill should have:
   - `SKILL.md` - Main skill file with frontmatter and instructions
   - `assets/` - Any images, logos, or supporting files (optional)

### Skill Format

```markdown
---
name: skill-name
description: Brief description of what this skill does
---

# Skill Title

## Quick Reference
[Essential info]

## Instructions
[Detailed guidance]
```

## Conventions

- Skill folders use kebab-case: `skill-name/`
- Each skill folder contains at minimum a `SKILL.md`
- Assets go in `assets/` subfolder within the skill
- Use relative paths for asset references: `./assets/filename.png`

## Team Access

- This is a private repository for VPVR team members
- Clone to `~/.claude/skills/vpvr` for Claude Code
- Or add skill URLs to Claude.ai Projects
