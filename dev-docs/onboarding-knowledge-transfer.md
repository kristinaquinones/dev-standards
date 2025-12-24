# Onboarding & Knowledge Transfer

## New developer checklist

- [ ] Repository cloned and dependencies installed
- [ ] Local dev environment running
- [ ] All tests passing locally
- [ ] README.md read (project overview)
- [ ] dev-docs/README.md skimmed (development standards index)
- [ ] docs/QUICK-REFERENCE.md studied (common commands, file structure)
- [ ] docs/ARCHITECTURE-DECISIONS.md reviewed (key decisions and rationale)
- [ ] First PR submitted (small fix, documentation update, or test)
- [ ] Code review process understood (checklist, CI requirements)
- [ ] Team communication channels joined (Slack, Discord, etc.)

## Creating a QUICK-REFERENCE.md

Template:
```markdown
# Quick Reference

## Setup & Installation
\`\`\`bash
# Install dependencies
<install-command>

# Copy environment template
cp .env.example .env.local

# Start development environment
<dev-command>
\`\`\`

## Common commands
| Task | Command |
|------|---------|
| Run dev server | <dev-command> |
| Run tests | <test-command> |
| Check code quality | <check-command> |
| Format code | <format-command> |

## Project structure
- `src/app/` - Application entry points or main modules
- `src/lib/` - Shared utilities and business logic
- `src/components/` - Reusable components
- `tests/` - Test files
- `docs/` - Developer documentation

## Writing your first component/module
1. Create file in appropriate directory (e.g., `src/components/`)
2. Follow project conventions (naming, structure, types)
3. Add tests in test directory
4. Update docs/QUICK-REFERENCE.md if adding new pattern

## FAQ
**Q: How do I run a single test?**
A: Use your test runner's filter option (e.g., `<test-command> specific.test.ext`)

**Q: Where are API endpoints?**
A: Check project structure documentation or `src/` directory
```

