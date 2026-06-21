# Contributing to dev-standards

This repository contains project-agnostic standards across multiple disciplines (development, product, GTM/marketing, design, measurement) organized as Markdown files. Each discipline has its own directory with a `README.md` index file.

This document describes the contributing **process**. For the documentation **standards** themselves (formatting, file organization, content rules, style guide, and changelog policy), see [CLAUDE.md](CLAUDE.md), which is the single source of truth.

## Contributing process

### Before making changes

1. **Review existing content**
   - Read relevant files in the appropriate `*-docs/` directory
   - Understand the structure and formatting patterns (see [CLAUDE.md](CLAUDE.md))
   - Check the section's `README.md` index for related content

2. **Plan your changes**
   - Determine which file(s) need updates
   - Identify if new files are needed
   - Consider impact on related files and links
   - Determine whether the change should be recorded in `CHANGELOG.md`

3. **Create a branch**
   - Use a descriptive branch name: `feature/add-new-standard`, `fix/typo-in-security`, `chore/update-links`
   - Branch from `main`

### Making changes

**For new content:**
1. Create a new file in the appropriate `*-docs/` directory with a kebab-case filename
2. Follow the existing file structure (title, sections, formatting) per [CLAUDE.md](CLAUDE.md)
3. Add an entry to the section's `README.md` index
4. Link to related standards where appropriate
5. Verify all links work
6. Update `CHANGELOG.md` if the addition materially changes repository content, structure, or contributor workflow

**For updates:**
1. Edit the relevant file(s) in the appropriate `*-docs/` directory
2. Maintain consistent formatting
3. Update links if structure changes
4. Update the index if adding or removing files
5. Update `CLAUDE.md` if the documentation standards themselves change (it is the source of truth; `AGENTS.md` and `.cursorrules` are stubs that point to it and need no content updates)
6. Update `CHANGELOG.md` when the change is significant enough to matter to future contributors or users

**For fixes:**
1. Fix the issue (typo, broken link, formatting)
2. Verify related content is still accurate
3. Check for similar issues in other files
4. Update `CHANGELOG.md` only if the fix is notable beyond a minor editorial correction

### Git workflow

Commit messages follow the [Conventional Commits](https://www.conventionalcommits.org/) format:

- `docs:` documentation changes
- `fix:` corrections, typos, broken links
- `feat:` new content or standards
- `refactor:` reorganization, restructuring
- `chore:` maintenance tasks

Examples:

```bash
git commit -m "docs: add new section on code organization"
git commit -m "fix: correct typo in security.md"
git commit -m "feat: add accessibility standards"
git commit -m "refactor: reorganize documentation structure"
```

**Branch strategy:**

- `feature/description` for new content or major updates
- `fix/description` for corrections and fixes
- `chore/description` for maintenance and cleanup
- Always branch from `main`

### Pull request requirements

**All PRs must include:**

1. **Summary** (1-3 sentences)
   - What changed and why
   - Which files were modified
   - Link to related issue (if applicable)

2. **Documentation checklist** (see the full checklist below)

3. **Scope check**
   - One topic per PR
   - Changes are focused and related
   - Reviewers can understand the changes quickly

### Documentation review checklist

Before submitting a PR, verify:

**Content quality:**
- [ ] Spelling and grammar checked
- [ ] Language is clear and concise
- [ ] Examples are accurate and helpful
- [ ] Content follows the DRY principle (no duplication, link instead)
- [ ] Avoids "business" terminology; uses "product goals", "objectives", "outcomes", "strategic goals"
- [ ] SMART goals used as the primary goal-setting framework where applicable
- [ ] Incrementality emphasized for experiments: well-designed experiments that measure incrementality are the only way to understand actual impact
- [ ] Style guide followed: sentence casing for headings and labels, minimal to no em dashes

**Formatting:**
- [ ] Markdown syntax is correct
- [ ] Headers follow hierarchy (`#`, `##`, `###`)
- [ ] Code blocks have language tags
- [ ] Lists are properly formatted
- [ ] Long lists (5+ items) in README/index files use collapsible sections
- [ ] Tables are readable and aligned

**Links:**
- [ ] All internal links use relative paths
- [ ] All links resolve correctly (internal, external, and section anchors)
- [ ] Link text is descriptive (not "click here")

**Structure:**
- [ ] Filename matches the main heading (kebab-case)
- [ ] File structure follows conventions
- [ ] Index file updated if files were added or removed
- [ ] Related files updated across standards directories if standards changed
- [ ] `CLAUDE.md` updated if the documentation standards themselves changed

**Changelog:**
- [ ] `CHANGELOG.md` reviewed for impact
- [ ] Notable additions, removals, restructuring, or contributor workflow changes recorded under `Unreleased`
- [ ] Minor editorial-only updates excluded unless they materially affect repository usage

**Git:**
- [ ] Commit message follows Conventional Commits format
- [ ] Branch name is descriptive
- [ ] One topic per PR (focused scope)
- [ ] PR description is clear and complete

### Review process

**Reviewers should verify:**
- [ ] Content is accurate and clear
- [ ] Formatting follows the standards in [CLAUDE.md](CLAUDE.md)
- [ ] Long lists use collapsible sections where appropriate
- [ ] All links work correctly
- [ ] Structure is consistent
- [ ] Related files are updated
- [ ] `CHANGELOG.md` reflects notable changes when applicable
- [ ] Commit messages are clear and the PR description is complete

**Common issues to check:**
- Broken internal links
- Inconsistent formatting
- Long lists that should be collapsible (5+ items in README/index files)
- Duplicated content (should be linked instead)
- Missing cross-references between standards directories
- Missing index updates
- Missing changelog updates for notable changes
- Unclear or incomplete descriptions

### Common tasks

**Adding a new standard:**
1. Create the file in the appropriate `*-docs/` directory
2. Follow the existing file structure
3. Add it to the section's `README.md` index
4. Link from related standards
5. Verify all links work
6. Add a changelog entry if it changes repository scope or guidance

**Fixing a broken link:**
1. Find the broken link
2. Determine the correct path
3. Update the link and verify it works
4. Check for similar issues elsewhere

**Reorganizing structure:**
1. Plan the new structure
2. Move or rename files
3. Update all internal links and the index
4. Verify all links work
5. Record the reorganization in `CHANGELOG.md`

## Keeping governance files in sync

- **[CLAUDE.md](CLAUDE.md)** is the single source of truth for the documentation standards.
- **[CONTRIBUTING.md](CONTRIBUTING.md)** (this file) owns the contributing process.
- **[AGENTS.md](AGENTS.md)** and **[.cursorrules](.cursorrules)** are short stubs that point to `CLAUDE.md`. They intentionally contain no standards of their own, so there is nothing to keep in content sync when standards change. Update them only if the pointer itself needs to change.
- Update `README.md` if contributor-facing repository guidance changes.
- Update `CHANGELOG.md` if changelog policy or contributor workflow changes materially.

## Version history

- Version history is maintained in `CHANGELOG.md` at the repository root, following [Keep a Changelog](https://keepachangelog.com/en/1.0.0/).
- Do **not** add version history sections to individual documentation files or section README files; this keeps a single source of truth for change tracking.
- Keep in-progress work under `## [Unreleased]`, and promote it into a dated release section when preparing a release.
- For the full changelog policy (what counts as notable, formatting, headings), see [CLAUDE.md](CLAUDE.md#version-history).

## Questions?

### General questions

- **"What are universal standards?"** → Everything in the `*-docs/` directories applies across projects
- **"What's project-specific?"** → Tech stack choices, library selections, deployment platforms, organizational details, brand identity, industry-specific requirements
- **"How do I customize this?"** → Copy sections and adapt for your organization's needs. For project-specific standards, keep your own `CLAUDE.md` (and optionally `.cursorrules` or `AGENTS.md`) in your project and override with your project's choices
- **"How often should I update?"** → When standards change (major new decision, team feedback, emerging best practices, new frameworks)
- **"Should I commit these files?"** → Yes! Keep all standards files in version control. They're documentation, not throwaway templates.

### Section-specific questions

**Development standards:**
- **"What's project-specific?"** → Tech stack choices, library selections, deployment platforms, organizational details

**Product standards:**
- **"What's project-specific?"** → Industry-specific requirements, organizational processes, tool choices

**Measurement standards:**
- **"What's project-specific?"** → Industry-specific metrics, tool choices, organizational processes

**Design standards:**
- **"What's project-specific?"** → Brand identity, visual style, component implementations, tool choices

**GTM & Marketing standards:**
- **"What's project-specific?"** → Industry-specific tactics, brand voice, channel mix, organizational details

## Related files

- **[CLAUDE.md](CLAUDE.md)** - Source of truth for the documentation standards and guidelines
- **[AGENTS.md](AGENTS.md)** - Stub pointing to `CLAUDE.md`
- **[.cursorrules](.cursorrules)** - Stub pointing to `CLAUDE.md`
