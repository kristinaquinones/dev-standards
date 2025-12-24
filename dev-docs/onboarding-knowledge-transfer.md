# Onboarding & Knowledge Transfer

## New developer checklist

- [ ] Repository cloned and dependencies installed
- [ ] Local dev environment running (`npm run dev`)
- [ ] All tests passing locally (`npm test`)
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
npm install
cp .env.example .env.local
npm run dev
\`\`\`

## Common commands
| Task | Command |
|------|---------|
| Run dev server | npm run dev |
| Run tests | npm test |
| Check code quality | npm run check |
| Format code | npm run format |

## Project structure
- `src/app/` - Next.js routes and pages
- `src/lib/` - Shared utilities and business logic
- `src/components/` - Reusable React components
- `tests/` - Test files
- `docs/` - Developer documentation

## Writing your first component
1. Create file in `src/components/`
2. Use TypeScript + named export
3. Add unit tests in `src/__tests__/`
4. Update docs/QUICK-REFERENCE.md if adding new pattern

## FAQ
**Q: How do I run a single test?**
A: \`npm test -- specific.test.ts --verbose\`

**Q: Where are API endpoints?**
A: \`src/app/api/\` (Next.js API Routes)
```

