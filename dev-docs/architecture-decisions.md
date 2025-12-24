# Architecture Decisions

## Why architecture decisions matter

Major decisions (tech stack, database, versioning strategy, performance targets) impact cost, timeline, and flexibility. Documenting them prevents:
- **Repeated debates** ("Why did we pick Next.js?")
- **Bad refactors** (re-implementing features that were chosen for a reason)
- **Onboarding confusion** (new team members understand the "why")

## Architecture decision log (ADL) pattern

Create `docs/ARCHITECTURE-DECISIONS.md`:

```markdown
# Architecture Decisions

## ADL-001: Choose TypeScript + Strict Mode for Type Safety

**Date:** 2025-01-15
**Status:** Accepted
**Decision Makers:** @user1, @user2

### Context
Project needs to prevent common bugs (undefined access, type mismatches).
Team has TypeScript experience.

### Decision
Use TypeScript with `"strict": true` for all projects.

### Alternatives Considered
- JavaScript (fastest to write; higher runtime errors)
- Flow (learning curve; weaker ecosystem)

### Consequences
- ✅ Catch bugs at compile time
- ✅ Better IDE support, autocomplete
- ❌ Slower initial development (5–10% slower)
- ❌ Requires build step

### Related Decisions
- ADL-002: ESLint + Prettier for code style
- ADL-003: Jest for testing

### Links
- [TypeScript Handbook](https://www.typescriptlang.org/docs/)
- [Strict Mode Guide](https://www.typescriptlang.org/tsconfig#strict)
```

**For each ADL entry:**
- Clear decision statement
- Context and alternatives
- Consequences (pros/cons)
- Links to related docs and decisions

