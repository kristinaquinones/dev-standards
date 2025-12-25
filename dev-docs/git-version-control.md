# Git & Version Control

## Commit message standards

**Format:** Conventional Commits (optional, but recommended)

```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:** `feat`, `fix`, `refactor`, `docs`, `test`, `chore`, `style`, `perf`

**Examples:**
```bash
git commit -m "feat(search): add full-text search indexing for 1000+ documents"
git commit -m "fix(parser): handle missing YAML frontmatter gracefully"
git commit -m "docs: update development standards with testing guidelines"
git commit -m "chore(deps): upgrade framework to latest stable version"
```

## Branch strategy

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

## Tag strategy (semantic versioning)

```bash
git tag -a v1.2.3 -m "Release v1.2.3: Add feature X, fix bug Y"
git tag -a v1.2.3-beta.1 -m "Beta 1 of v1.2.3"
git push origin --tags
```

