# Development Standards — Universal Guide for Software Projects

This document outlines comprehensive development standards applicable to any software project. It serves as a template for establishing consistent practices across teams and codebases.

---

## Table of Contents

1. [Philosophy & Principles](#philosophy--principles)
2. [Code Organization](#code-organization)
3. [Coding Style & Standards](#coding-style--standards)
4. [Testing & Quality](#testing--quality)
5. [Documentation](#documentation)
6. [Git & Version Control](#git--version-control)
7. [Pull Requests & Code Review](#pull-requests--code-review)
8. [Configuration & Secrets](#configuration--secrets)
9. [CI/CD & Build Pipeline](#cicd--build-pipeline)
10. [Performance & Scalability](#performance--scalability)
11. [Accessibility & Inclusivity](#accessibility--inclusivity)
12. [Security](#security)
13. [Architecture Decisions](#architecture-decisions)
14. [Onboarding & Knowledge Transfer](#onboarding--knowledge-transfer)
15. [Sync Instructions for .cursorrules, claude.md, AGENTS.md](#sync-instructions-for-cursorrules-claudemd-agentsmd)

---

## Philosophy & Principles

### Core Values

1. **Clarity > Cleverness**
   - Code should be readable first, optimized second
   - Prefer explicit over implicit
   - Comment the "why," not the "what"

2. **DRY (Don't Repeat Yourself)**
   - Extract shared logic into utilities/libraries
   - Avoid copy-paste; refactor instead
   - Single source of truth for business logic

3. **YAGNI (You Aren't Gonna Need It)**
   - Build for current requirements, not hypothetical futures
   - Avoid premature abstraction
   - Add features when they're needed, not before

4. **Fail Fast & Visibly**
   - Catch errors early (type checking, linting, tests)
   - Explicit error handling; no silent failures
   - Logs should be informative and actionable

5. **Documentation is Code**
   - Keep docs in version control alongside code
   - Treat docs with same rigor as code (review, test, update)
   - Outdated docs are worse than no docs

6. **Consistency Matters**
   - Follow team conventions (naming, file structure, patterns)
   - Automate style enforcement (formatters, linters)
   - New contributors should feel patterns, not guess them

---

## Code Organization

### Directory Structure Template

```
project-root/
├── src/                      # Application source code
│   ├── app/                  # Framework-specific (Next.js App Router, etc.)
│   │   ├── layout.tsx
│   │   ├── page.tsx
│   │   └── [segment]/
│   ├── lib/                  # Shared utilities & business logic
│   │   ├── utils/
│   │   ├── services/
│   │   ├── config/
│   │   └── types/
│   ├── components/           # Reusable UI components
│   │   ├── common/
│   │   ├── layout/
│   │   └── features/
│   ├── styles/               # Global stylesheets & design tokens
│   └── __tests__/            # Test files (colocated or separate)
├── tests/                    # Integration & E2E tests (optional)
├── docs/                     # Developer documentation
│   ├── planning/             # Phase plans, roadmaps, specs
│   ├── progress/             # Daily/weekly progress logs
│   └── QUICK-REFERENCE.md    # Developer cheat sheet
├── user-docs/                # User-facing guides
├── brand/                    # Design assets, logos, style guide
├── config/                   # Configuration files
├── .github/                  # GitHub Actions, PR templates
├── public/                   # Static assets
├── package.json
├── tsconfig.json
├── .env.example              # Template for env vars (checked in)
├── .env.local                # Local env vars (NOT checked in; in .gitignore)
├── .gitignore
├── .cursorrules              # AI assistant guidelines (sync with claude.md, AGENTS.md)
├── claude.md                 # Contributor guidelines (sync with .cursorrules, AGENTS.md)
├── AGENTS.md                 # Contributing process & standards (sync with .cursorrules, claude.md)
├── DEVELOPMENT-STANDARDS.md  # This file
├── README.md
└── CHANGELOG.md
```

### Module Organization Principles

- **Functional Cohesion:** Group related code together (by feature, not by type)
- **Clear Boundaries:** Each module has a single responsibility
- **Explicit Dependencies:** Import statements show data/function flow
- **Reusability:** Utilities/services are testable and independent
- **Configuration Isolation:** Config files are centralized; avoid magic values in code

---

## Coding Style & Standards

### Language-Specific Standards

#### TypeScript/JavaScript
- **Strict Mode:** Enable TypeScript strict mode (`"strict": true`)
- **Type Annotations:** Explicit types on function parameters and return values
- **Naming:**
  - `PascalCase` for classes, components, types
  - `camelCase` for functions, variables, props
  - `kebab-case` for filenames (utilities), `PascalCase` for components/routes
  - `SCREAMING_SNAKE_CASE` for constants only when truly constant (config values)
- **Formatting:**
  - 2-space indentation (configurable; pick one and enforce)
  - Use formatter (Prettier) to remove style debates
  - Linter (ESLint) for code quality
- **No Inline Disables:** Avoid `// @ts-ignore`, `// eslint-disable` unless documented

#### Example: Good TypeScript
```typescript
// ✅ Clear types, explicit return
export function parseUserInput(input: string): { name: string; email: string } {
  const [name, email] = input.split('|');
  return { name, email };
}

// ❌ Implicit types, unclear intent
export function parse(x: any): any {
  return x.split('|');
}
```

### Code Review Checklist

Before submitting code:
- [ ] Follows naming conventions
- [ ] No unused variables or imports
- [ ] Functions have clear purpose (name + types)
- [ ] No code duplication (DRY principle applied)
- [ ] No console.log() left in (use structured logging)
- [ ] Comments explain "why," not "what"
- [ ] Error handling is explicit (no swallowing errors)

---

## Testing & Quality

### Testing Strategy

**Pyramid Approach** (Many unit tests → Some integration → Few E2E):

1. **Unit Tests** (60–70% of test suite)
   - Test individual functions, modules, components
   - Isolated from external dependencies (mock APIs, databases)
   - Fast to run (<5ms per test)
   - Framework: Jest, Vitest, or equivalent

2. **Integration Tests** (20–30% of test suite)
   - Test how modules work together
   - Use realistic test fixtures
   - May hit real databases or file systems
   - Framework: Jest + Testing Library (for UI), or Supertest (for APIs)

3. **E2E Tests** (5–10% of test suite)
   - Test complete user workflows
   - Run in real browser/environment
   - Slow but high confidence
   - Framework: Playwright, Cypress, or equivalent

### Coverage Targets

- **Absolute Minimum:** 60% overall coverage (libraries/utilities should be ≥80%)
- **Safe Zone:** 70–80% coverage (most bugs caught, diminishing ROI beyond 80%)
- **Overkill:** >85% coverage (only for critical path modules where cost of failure is high)

### Testing Best Practices

```typescript
// ✅ Good: Descriptive test names, realistic fixtures, clear assertions
describe('parseMarkdown', () => {
  it('should extract YAML frontmatter and markdown body', () => {
    const input = '---\ntitle: Test\n---\n# Content';
    const result = parseMarkdown(input);
    expect(result.frontmatter.title).toBe('Test');
    expect(result.body).toContain('# Content');
  });

  it('should handle missing frontmatter gracefully', () => {
    const input = '# Content only';
    const result = parseMarkdown(input);
    expect(result.frontmatter).toEqual({});
    expect(result.body).toBe('# Content only');
  });
});

// ❌ Bad: Unclear test name, no fixtures, brittle assertions
describe('parsing', () => {
  it('works', () => {
    expect(parseMarkdown('---\ntitle: Test\n---\n# Content')).toBeTruthy();
  });
});
```

### Running Tests

```bash
npm test                      # Run all tests once
npm test -- --watch          # Watch mode (re-run on file change)
npm test -- --coverage       # Generate coverage report
npm run check                # Lint + typecheck + tests (full CI suite)
```

---

## Documentation

### Types of Documentation

| Type | Where | Audience | Updated |
|------|-------|----------|---------|
| **README.md** | Root | New users, overview | Every release |
| **DEVELOPMENT-STANDARDS.md** | Root | All developers | When standards change |
| **docs/** (developer) | `docs/` folder | Team members, contributors | Per PR/feature |
| **user-docs/** | `user-docs/` folder | End users, operators | Per release |
| **API Documentation** | Inline JSDoc + `docs/API.md` | Developers using the module | Per API change |
| **Architecture Decisions** | `docs/ARCHITECTURE-DECISIONS.md` | Long-term reference | When major decision made |
| **Progress Logs** | `docs/progress/YYYY_MM_DD.md` | Team sync, knowledge capture | Daily or per sprint |
| **Inline Comments** | In code | Future maintainers | When logic isn't obvious |

### Documentation Standards

1. **Keep Docs in Version Control**
   - Treat docs as code; review before merging
   - Outdated docs in repo > no docs
   - Use Markdown for readability and git diffs

2. **Link Related Docs**
   - Cross-reference related specs, APIs, decision logs
   - Update links when docs move

3. **API Documentation Template**
   ```typescript
   /**
    * Parses markdown content with YAML frontmatter.
    *
    * @param input Raw markdown string (e.g., "---\ntitle: ...\n---\n# Content")
    * @returns Object with `frontmatter` (YAML) and `body` (markdown content)
    *
    * @example
    * const { frontmatter, body } = parseMarkdown('---\ntitle: Test\n---\n# Title');
    * console.log(frontmatter.title); // "Test"
    *
    * @throws Error if frontmatter is malformed
    */
   export function parseMarkdown(input: string): { frontmatter: Record<string, any>; body: string } {
     // implementation
   }
   ```

4. **Progress Logs Template**
   ```markdown
   # Progress: YYYY-MM-DD

   ## Summary
   - ✅ Completed feature X
   - ✅ Fixed bug Y

   ## Work Done
   - Detailed breakdown of what was implemented

   ## Blockers/Open Questions
   - Any issues that need discussion

   ## Next Steps
   - What comes next
   ```

---

## Git & Version Control

### Commit Message Standards

**Format:** Conventional Commits (optional, but recommended)

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:** `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `style`, `perf`

**Examples:**
```bash
git commit -m "feat(search): add FlexSearch indexing for 1000+ documents"
git commit -m "fix(parser): handle missing YAML frontmatter gracefully"
git commit -m "docs: update DEVELOPMENT-STANDARDS with testing guidelines"
git commit -m "chore(deps): upgrade Next.js to 14.2.0"
```

### Branch Strategy

```
main (or master)
├── stable, always deployable
├── PR reviews required before merge

feature/feature-name
├── New features, small scope
├── Branch from: main
├── Example: feature/search-indexing

fix/bug-description
├── Bug fixes, urgent patches
├── Branch from: main
├── Example: fix/parser-crash-on-empty-frontmatter

chore/task-description
├── Documentation, dependencies, config
├── Branch from: main
├── Example: chore/update-eslint-config
```

### Tag Strategy (Semantic Versioning)

```bash
git tag -a v1.2.3 -m "Release v1.2.3: Add feature X, fix bug Y"
git tag -a v1.2.3-beta.1 -m "Beta 1 of v1.2.3"
git push origin --tags
```

---

## Pull Requests & Code Review

### PR Requirements

**All PRs must include:**

1. **Summary** (1–3 sentences)
   - What changed and why?
   - Link to related issue

2. **Testing Checklist**
   - `npm run lint` ✅
   - `npm run typecheck` ✅
   - `npm test` ✅
   - `npm run build` ✅
   - Manual testing in browser/CLI

3. **Documentation Updates**
   - Progress log created: `docs/progress/YYYY_MM_DD.md`
   - User-facing docs updated (if applicable)
   - Developer docs updated (if applicable)
   - CHANGELOG.md updated under `[Unreleased]` section

4. **Scope Check**
   - One feature/fix per PR (no unrelated changes)
   - Reviewers can understand the change in 15 minutes

### Code Review Checklist

Reviewers should verify:
- [ ] Code follows team standards (style, naming, patterns)
- [ ] Tests are present and meaningful
- [ ] No obvious bugs or security issues
- [ ] Documentation is clear and linked
- [ ] Commit messages are clear
- [ ] PR description is complete

---

## Configuration & Secrets

### Environment Variables

1. **Public Variables** (safe to expose, checked in)
   - Framework config: `NEXT_PUBLIC_API_URL`
   - Feature flags: `FEATURE_EXPERIMENTAL_SEARCH`
   - App metadata: `NEXT_PUBLIC_VERSION`

2. **Private Variables** (sensitive, NOT checked in)
   - API keys, database passwords
   - Service credentials
   - Private endpoints

### Setup

```bash
# 1. Create .env.example with public + placeholder vars (checked in)
NEXT_PUBLIC_SITE_NAME=MyApp
NEXT_PUBLIC_API_URL=https://api.example.com
DATABASE_PASSWORD=<change-me>
STRIPE_SECRET_KEY=<change-me>

# 2. Create .env.local with real values (add to .gitignore, NOT checked in)
NEXT_PUBLIC_SITE_NAME=MyApp
NEXT_PUBLIC_API_URL=https://api.example.com
DATABASE_PASSWORD=actual_secret_here
STRIPE_SECRET_KEY=sk_test_xxxx

# 3. In code, access via process.env
const apiUrl = process.env.NEXT_PUBLIC_API_URL; // public, OK in browser
const dbPass = process.env.DATABASE_PASSWORD;   // private, server-only
```

### Security Rules

- ✅ Commit `.env.example` (template only)
- ❌ Never commit `.env.local`, `.env.production`, or files with real secrets
- ✅ Use env vars for all secrets, never hardcode
- ✅ Rotate secrets regularly in production
- ✅ Use separate secrets for dev, staging, production

---

## CI/CD & Build Pipeline

### Standard Build Steps

```bash
npm install              # Install dependencies
npm run lint            # ESLint + Prettier
npm run typecheck       # TypeScript checks
npm run test            # Unit + integration tests
npm run build           # Production build
npm run build:verify    # Verify build output (optional smoke tests)
```

### GitHub Actions Template

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest
    strategy:
      matrix:
        node-version: [18.x, 20.x]

    steps:
      - uses: actions/checkout@v3
      - uses: actions/setup-node@v3
        with:
          node-version: ${{ matrix.node-version }}

      - name: Install dependencies
        run: npm install

      - name: Lint
        run: npm run lint

      - name: TypeScript
        run: npm run typecheck

      - name: Tests
        run: npm test -- --coverage

      - name: Build
        run: npm run build
```

### Deployment Strategy

1. **Development**: Deploy on every PR merge to `main`
2. **Staging**: Deploy on tagged pre-release (e.g., `v1.2.3-beta`)
3. **Production**: Deploy on stable release tag (e.g., `v1.2.3`)

---

## Performance & Scalability

### Performance Targets (adjust per project)

| Metric | Target | Tools |
|--------|--------|-------|
| Lighthouse Performance | ≥85 | Lighthouse CI |
| Lighthouse Accessibility | ≥90 | Lighthouse CI |
| First Contentful Paint (FCP) | <2s | Web Vitals |
| Cumulative Layout Shift (CLS) | <0.1 | Web Vitals |
| Time to Interactive (TTI) | <3.5s | Web Vitals |
| Bundle Size | <300KB (gzipped) | bundlesize/size-limit |
| API Response Time | <200ms (p95) | APM tools |
| Database Query Time | <100ms (p95) | Database profiling |

### Performance Checklist

Before merging:
- [ ] No new large dependencies added without justification
- [ ] Images are optimized (Next.js Image component, WebP, responsive sizes)
- [ ] No N+1 queries (batch database operations)
- [ ] Expensive operations are cached or memoized
- [ ] Code splitting is in place (lazy load heavy routes)
- [ ] Bundle size is monitored and trending down

---

## Accessibility & Inclusivity

### Accessibility Standards

**Target:** WCAG 2.1 Level AA minimum (US ADA + EU compliance)

### Checklist

- [ ] **Color Contrast:** ≥4.5:1 for text, ≥3:1 for UI components
- [ ] **Keyboard Navigation:** All interactive elements accessible via Tab, Enter, Escape
- [ ] **ARIA Labels:** Buttons, form fields, landmarks have descriptive labels
- [ ] **Focus Indicator:** Clear focus visible on all interactive elements
- [ ] **Responsive Design:** Works on 320px–1920px viewports
- [ ] **Form Validation:** Clear error messages, accessible error handling
- [ ] **Image Alt Text:** All images have meaningful alt text (or `alt=""` if decorative)
- [ ] **Semantic HTML:** Use `<button>`, `<form>`, `<nav>`, `<header>`, etc., not `<div>` + ARIA
- [ ] **Screen Reader Testing:** Test with NVDA (Windows), JAWS, or VoiceOver (Mac)
- [ ] **Lighthouse Accessibility Score:** ≥95

### Tools

- **Axe DevTools** (browser extension) — automated accessibility scanning
- **Lighthouse** (Chrome DevTools) — accessibility audit
- **WAVE** (browser extension) — visual accessibility feedback
- **Screen Readers:** NVDA (free, Windows), JAWS (paid, Windows), VoiceOver (built-in, Mac)

---

## Security

### Code Security Checklist

- [ ] **Input Validation:** All user input is validated, escaped, or parameterized
- [ ] **No SQL Injection:** Use parameterized queries, never string concatenation
- [ ] **No XSS:** Sanitize HTML, use templating engines, Content Security Policy (CSP)
- [ ] **Authentication:** Secure session management, no credentials in URLs
- [ ] **Authorization:** Check permissions server-side, never trust client-side checks
- [ ] **Secrets:** Never commit API keys, passwords, tokens (use .env.local + .gitignore)
- [ ] **Dependencies:** Keep packages up to date; audit with `npm audit`
- [ ] **HTTPS Only:** Enforce HTTPS in production
- [ ] **CORS:** Restrict CORS origins to trusted domains
- [ ] **Rate Limiting:** Implement rate limits on APIs to prevent abuse

### Dependency Management

```bash
npm audit                    # Find known vulnerabilities
npm audit fix                # Auto-fix where possible
npm update                   # Update to latest minor/patch versions
npm outdated                 # See what's outdated
```

### Regular Security Practices

- [ ] Rotate secrets monthly (or per-incident)
- [ ] Audit dependencies quarterly
- [ ] Security review of major features before release
- [ ] Incident response plan documented and practiced

---

## Architecture Decisions

### Why Architecture Decisions Matter

Major decisions (tech stack, database, versioning strategy, performance targets) impact cost, timeline, and flexibility. Documenting them prevents:
- **Repeated debates** ("Why did we pick Next.js?")
- **Bad refactors** (re-implementing features that were chosen for a reason)
- **Onboarding confusion** (new team members understand the "why")

### Architecture Decision Log (ADL) Pattern

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

---

## Onboarding & Knowledge Transfer

### New Developer Checklist

- [ ] Repository cloned and dependencies installed
- [ ] Local dev environment running (`npm run dev`)
- [ ] All tests passing locally (`npm test`)
- [ ] README.md read (project overview)
- [ ] DEVELOPMENT-STANDARDS.md skimmed (this file)
- [ ] docs/QUICK-REFERENCE.md studied (common commands, file structure)
- [ ] docs/ARCHITECTURE-DECISIONS.md reviewed (key decisions and rationale)
- [ ] First PR submitted (small fix, documentation update, or test)
- [ ] Code review process understood (checklist, CI requirements)
- [ ] Team communication channels joined (Slack, Discord, etc.)

### Creating a QUICK-REFERENCE.md

Template:
```markdown
# Quick Reference

## Setup & Installation
\`\`\`bash
npm install
cp .env.example .env.local
npm run dev
\`\`\`

## Common Commands
| Task | Command |
|------|---------|
| Run dev server | npm run dev |
| Run tests | npm test |
| Check code quality | npm run check |
| Format code | npm run format |

## Project Structure
- `src/app/` — Next.js routes and pages
- `src/lib/` — Shared utilities and business logic
- `src/components/` — Reusable React components
- `tests/` — Test files
- `docs/` — Developer documentation

## Writing Your First Component
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

---

## Sync Instructions for .cursorrules, claude.md, AGENTS.md

### Purpose of the Trio

These three files work together to establish team standards and contributor guidelines:

1. **.cursorrules** — Brief, concise rules for AI assistants (Claude, etc.)
2. **claude.md** — Detailed contributor guidelines for humans working with AI
3. **AGENTS.md** — Contributing process and standards (can also guide AI agents)

**CRITICAL:** Keep all three in sync. Changes to one should reflect in the others.

### Content to Keep in Sync

**Universal rules (same across all three files):**
- Code style (TypeScript strict, Prettier, ESLint)
- Naming conventions (PascalCase, camelCase, kebab-case)
- Project structure (where code lives, what's src/ vs. docs/)
- Commit message format (Conventional Commits)
- PR requirements (tests, docs, changelog)
- Testing standards (unit, integration, coverage targets)
- Documentation standards (where docs live, formats)
- Git workflow (branch strategy, tags)
- Security practices (secrets, dependencies, input validation)
- Accessibility standards (WCAG AA)
- Performance targets (Lighthouse scores, bundle size)

**Project-specific overrides (may differ per project):**
- Tech stack choices (Next.js, Flask, Django, etc.)
- Specific libraries (Tailwind vs. CSS-in-JS)
- Database technology (PostgreSQL, MongoDB, etc.)
- Deployment platform (Vercel, AWS, etc.)
- Organizational details (team structure, review processes)

### Sync Checklist (Before Every PR)

When updating standards:

- [ ] **DEVELOPMENT-STANDARDS.md** — Updated with new/changed standard
- [ ] **.cursorrules** — Updated with key rule in concise format
- [ ] **claude.md** — Updated with detailed explanation and examples
- [ ] **AGENTS.md** — Updated with process/checklist reflecting change
- [ ] **All three files reviewed for consistency** — Read through; verify tone/examples align

### Example: Adding a New Accessibility Standard

**1. Update DEVELOPMENT-STANDARDS.md (this file):**
```markdown
### New Accessibility Requirement
- [ ] **Voice Control:** Support voice commands for accessibility
```

**2. Update .cursorrules (concise):**
```
# Accessibility
- WCAG 2.1 Level AA minimum (4.5:1 color contrast, keyboard nav, ARIA labels, focus visible)
- Voice control support required for major actions (defer to Phase 02 if needed)
```

**3. Update claude.md (detailed):**
```markdown
## Accessibility Standards

Target WCAG 2.1 Level AA (US ADA + EU compliance).

### Checklist
- Color contrast ≥ 4.5:1
- Keyboard navigation (Tab, Shift+Tab, Enter, Escape)
- ARIA labels on buttons, forms, landmarks
- Clear focus indicator
- Voice control for major actions

### Voice Control Implementation
Voice commands should cover primary workflows:
- "Search documentation" → opens search palette
- "Dark mode" → toggles theme
- "Navigate to settings" → goes to settings

Defer advanced voice features to Phase 02.

### Testing
Use NVDA (Windows), VoiceOver (Mac), or Lighthouse accessibility audit.
```

**4. Update AGENTS.md (process):**
```markdown
## Accessibility Review

Before submitting PR:
1. Run Lighthouse accessibility audit (`npm run audit`)
2. Test keyboard navigation (Tab through all interactive elements)
3. Test with screen reader if UI changes
4. Check color contrast with Axe DevTools
5. Add voice control labels to major actions (if applicable)
6. Update ACCESSIBILITY.md with any changes
```

---

## Implementation for Your Project

### Step 1: Start with DEVELOPMENT-STANDARDS.md

You're reading it. Use this as your reference for team standards.

### Step 2: Create Project-Specific .cursorrules, claude.md, AGENTS.md

Each project should have its own trio, customized per Step 3 below.

### Step 3: Extract Universal Rules

From DEVELOPMENT-STANDARDS.md, extract the parts that apply to your project:

**Universal** (same in every project):
- TypeScript strict mode
- Prettier + ESLint
- Testing pyramid (unit/integration/E2E)
- WCAG AA accessibility
- Security checklist (input validation, secrets management, dependencies)
- Commit message format
- PR requirements (tests, docs, scope)

**Project-Specific Overrides:**
- Tech stack: "Use Next.js 14 App Router" (not "pick any framework")
- Styling: "Tailwind CSS + CSS Variables" (not generic CSS rules)
- Testing tool: "Jest for unit tests" (not "pick any test framework")
- Database: "PostgreSQL for primary data" (if applicable)
- Deployment: "Vercel for staging; AWS for production" (if applicable)

### Step 4: Keep the Trio Synchronized

Every time you update one file, update the others:
- Change to DEVELOPMENT-STANDARDS.md? → Update .cursorrules, claude.md, AGENTS.md
- Change to .cursorrules? → Update claude.md and AGENTS.md
- Change to claude.md? → Update .cursorrules and AGENTS.md

Use a checklist in your PR template to ensure this.

---

## Related Documents

- **README.md** — Project overview (what it does, quick start)
- **CHANGELOG.md** — Release notes (what changed, when)
- **docs/ARCHITECTURE-DECISIONS.md** — Major technical decisions and rationale
- **docs/QUICK-REFERENCE.md** — Developer cheat sheet (commands, structure, patterns)
- **docs/progress/YYYY_MM_DD.md** — Daily/weekly progress logs (team sync, blockers)
- **docs/planning/** — Phase plans, roadmaps, deliverables, success metrics
- **.github/PULL_REQUEST_TEMPLATE.md** — PR checklist and guidelines

---

## Version History

| Version | Date | Author | Changes |
|---------|------|--------|---------|
| 1.0 | 2025-12-23 | @contributor | Initial version; extracted from EmberDocs project standards |

---

## Contributing to These Standards

To propose changes to development standards:

1. Open an issue describing the problem or improvement
2. Create a PR with changes to DEVELOPMENT-STANDARDS.md
3. Include changes to .cursorrules, claude.md, AGENTS.md (keep in sync)
4. Get review from team leads or standards committee
5. Merge and announce to team

---

## Questions?

- **"What are universal standards?"** → Everything in this file (DEVELOPMENT-STANDARDS.md) applies across projects
- **"What's project-specific?"** → Tech stack choices, library selections, deployment platforms, organizational details
- **"How do I customize this?"** → Copy sections to .cursorrules/claude.md/AGENTS.md, override with your project's choices
- **"How often should I update?"** → When standards change (major new decision, team feedback, emerging best practices)
- **"Should I commit this file?"** → Yes! Keep DEVELOPMENT-STANDARDS.md in version control. It's documentation, not a template.
