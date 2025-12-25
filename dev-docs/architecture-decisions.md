# Architecture Decisions

## Why architecture decisions matter

Major decisions (tech stack, database, versioning strategy, performance targets) impact cost, timeline, and flexibility. Documenting them prevents:
- **Repeated debates** ("Why did we choose this framework?")
- **Bad refactors** (re-implementing features that were chosen for a reason)
- **Onboarding confusion** (new team members understand the "why")

## Architecture decision log (ADL) pattern

Create `docs/ARCHITECTURE-DECISIONS.md`:

```markdown
# Architecture Decisions

## ADL-001: Choose Static Typing for Type Safety

**Date:** 2025-01-15
**Status:** Accepted
**Decision Makers:** @user1, @user2

### Context
Project needs to prevent common bugs (undefined access, type mismatches).
Team has experience with statically typed languages.

### Decision
Use a statically typed language with strict type checking enabled.

### Alternatives Considered
- Dynamic typing (fastest to write; higher runtime errors)
- Gradual typing (flexible; can lead to inconsistency)

### Consequences
- ✅ Catch bugs at compile time
- ✅ Better IDE support, autocomplete
- ❌ Slower initial development (5–10% slower)
- ❌ May require build step

### Related Decisions
- ADL-002: Linting and formatting standards
- ADL-003: Testing framework selection

### Links
- Language documentation
- Type system guide
```

**For each ADL entry:**
- Clear decision statement
- Context and alternatives
- Consequences (pros/cons)
- Links to related docs and decisions

