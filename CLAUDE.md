# Contributor Guidelines for dev-standards

This document is the single source of truth for the documentation standards in this repository (formatting, file organization, content, style, and changelog policy), especially when working with AI assistants like Claude.

For the contributing process (branching, commit messages, pull requests, and review), see [CONTRIBUTING.md](CONTRIBUTING.md). `AGENTS.md` and `.cursorrules` are short stubs that point back to this file, so the standards below live here only.

## Repository overview

This repository contains project-agnostic standards across multiple disciplines (development, product, GTM/marketing, design, measurement) organized as Markdown files. Each discipline has its own directory and README index for navigation.

## Documentation standards

### Markdown formatting

**Headers:**
- Use `#` for the main title (matches filename)
- Use `##` for major sections
- Use `###` for subsections
- Use `####` sparingly for nested subsections

**Code blocks:**
- Always include language tags: ` ```typescript`, ` ```bash`, ` ```markdown`, etc.
- For inline code, use backticks: `` `code` ``
- Preserve indentation in code examples

**Lists:**
- Use `-` for unordered lists
- Use numbered lists (`1.`, `2.`, etc.) for ordered sequences
- Indent nested lists with 2 spaces
- Use `- [ ]` for checklists

**Collapsible sections:**
GitHub supports collapsible sections using HTML `<details>` and `<summary>` tags. Use these for long lists to improve readability:
- **When to use:** Lists with 5+ items in README files, index files, or overview documents
- **When NOT to use:** Short lists (fewer than 5 items), lists in detailed documentation files, essential content that should always be visible
- **Format:**
  ```markdown
  <details>
  <summary>View all topics</summary>

  - Item 1
  - Item 2
  - Item 3
  ...

  </details>
  ```
- **Best practices:**
  - Use descriptive summary text (for example, "View all topics", "See full list")
  - Keep summary text concise
  - Ensure the summary clearly indicates what's inside
  - Use for topic lists, file listings, or other reference material that doesn't need to be immediately visible

**Links:**
- Use relative paths for internal links: `[text](dev-docs/file.md)`
- Use anchors for section links: `[text](dev-docs/file.md#section-name)`
- External links should be descriptive: `[TypeScript Handbook](https://www.typescriptlang.org/docs/)`

**Tables:**
- Use pipe syntax with alignment: `| Left | Center | Right |`
- Keep tables readable; break long content into multiple rows if needed

### File organization

**Naming convention:**
- All filenames use kebab-case: `philosophy-principles.md`
- Filenames should match the main heading (lowercase, hyphenated)
- Keep filenames descriptive and clear

**Directory structure:**
```
dev-standards/
├── README.md                    # Repository overview
├── CHANGELOG.md                 # Version history
├── LICENSE                      # License file
├── CONTRIBUTING.md              # Contributing process
├── CLAUDE.md                    # This file (source of truth for standards)
├── AGENTS.md                    # Stub pointing to CLAUDE.md
├── .cursorrules                 # Stub pointing to CLAUDE.md
├── dev-docs/                    # Development standards
│   └── README.md                # Development standards index
├── product-docs/                # Product standards
│   └── README.md                # Product standards index
├── gtm-mktg-docs/               # GTM & Marketing standards
│   └── README.md                # GTM & Marketing standards index
├── design-docs/                 # Design standards
│   └── README.md                # Design standards index
└── measurement-docs/            # Measurement & Analytics standards
    └── README.md                # Measurement standards index
```

**File structure:**
Each standard file should:
1. Start with a `#` title matching the filename
2. Include clear section headers (`##`)
3. Use consistent formatting throughout
4. Link to related standards when appropriate
5. Include examples where helpful

### Content guidelines

**Clarity & readability:**
- Write for humans first; assume the reader is familiar with software development but may be new to these specific standards
- Use clear, concise language
- Prefer active voice over passive
- Break long paragraphs into shorter ones
- Use bullet points for lists of items

**DRY principle:**
- Do not duplicate content across files
- Link to related standards instead of repeating information
- If content appears in multiple places, consider consolidating it

**Consistency:**
- Follow existing patterns in the repository
- Use consistent terminology (for example, "development standards" not "dev standards")
- Avoid "business" terminology; use "product goals", "objectives", "outcomes", "strategic goals" instead to be inclusive of indie makers, creators, and developers
- **SMART goals framework**: The primary goal-setting framework recommended throughout these standards (Specific, Measurable, Achievable, Relevant, Time-bound)
- **Incrementality in experiments**: Well-designed experiments that measure incrementality are the only way to understand the actual impact of a change or intervention; observed data over time alone is not enough
- Maintain consistent formatting style
- Keep tone professional but approachable

**Style guide:**
- **Headings and labels**: Use sentence casing (capitalize first word and proper nouns only)
- **Em dashes**: Minimal to no use of em dashes; prefer commas, periods, or parentheses instead

**Cross-referencing:**
- Link to related standards using relative paths
- Update links when files are moved or renamed
- Use descriptive link text (not "click here")
- Verify all links work before committing

### Git workflow

The commit message format, branch strategy, and pull request process live in [CONTRIBUTING.md](CONTRIBUTING.md). Follow that document for anything related to the contributing process; this file covers the documentation standards only.

### Working with AI assistants

**When asking AI to help:**
- Be specific about which file(s) to modify
- Reference existing patterns: "Follow the same format as philosophy-principles.md"
- Ask for link verification: "Check all links in the file"
- Request consistency checks: "Ensure formatting matches other files"
- Call out whether the task should also update `CHANGELOG.md`

**AI should:**
- Maintain existing formatting patterns
- Use relative paths for links
- Follow the file naming conventions
- Update related files when making changes
- Verify links before suggesting changes
- Review whether `CHANGELOG.md` should be updated for notable changes
- Update `CLAUDE.md` when the documentation standards themselves change (it is the source of truth); update `CONTRIBUTING.md` for process changes, and `README.md` for contributor-facing repository guidance. `AGENTS.md` and `.cursorrules` are stubs and need no content updates.

**AI should NOT:**
- Create new files without updating the index
- Break existing links
- Change formatting style arbitrarily
- Duplicate content that should be linked instead
- Add changelog entries for trivial typo-only or purely editorial changes unless they materially change guidance

### Link maintenance

**Internal links:**
- Always use relative paths: `[text](dev-docs/file.md)`
- For section links: `[text](dev-docs/file.md#section-name)`
- Verify links work after moving/renaming files
- Update links in all affected files when structure changes

**Link verification:**
Before committing:
1. Check all internal links resolve correctly
2. Verify external links are still valid
3. Ensure anchor links point to correct sections
4. Update broken or moved links

### Cross-reference review

**Reviewing for cross-references:**
- Identify related topics across all standards directories
- Link between related sections (for example, product-docs → dev-docs, product-docs → measurement-docs)
- Check for missed connections between disciplines
- Ensure cross-discipline topics are properly linked

**DRY conflict checking:**
- Identify duplicate content across files
- Resolve conflicts by consolidating or linking
- Check for content that appears in multiple places
- Consider if duplicate content should be consolidated into a shared file
- Ensure all standards directories are reviewed for conflicts

### Documentation review checklist

The full pre-PR review checklist lives in [CONTRIBUTING.md](CONTRIBUTING.md#documentation-review-checklist). Use it before submitting any change.

### Governance files and source of truth

This repository keeps standards and process in one place each, so there is nothing to keep in content sync:

- **`CLAUDE.md`** (this file) is the single source of truth for the documentation standards.
- **`CONTRIBUTING.md`** owns the contributing process (branching, commits, pull requests, review).
- **`AGENTS.md`** and **`.cursorrules`** are short stubs that point to `CLAUDE.md`. They intentionally hold no standards of their own, so they do not need updating when standards change. Update them only if the pointer itself changes.

**When updating standards:**
1. Update the relevant file in the appropriate `*-docs/` directory
2. Update the relevant `*-docs/README.md` index if structure changes
3. Review for cross-referencing opportunities across all standards directories
4. Check for DRY conflicts and resolve or consolidate as needed
5. Update `CLAUDE.md` if the standards themselves change (it is the source of truth)
6. Update `README.md` if contributor-facing repository guidance changes
7. Update `CHANGELOG.md` if the change is notable

### Version history

**Location:**
- Version history is maintained in `CHANGELOG.md` at the repository root
- Do **NOT** add version history sections to individual documentation files or section README files
- This ensures a single source of truth for change tracking and follows DRY principles

**Format:**
- Follow [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format
- Group changes under `Added`, `Changed`, `Removed`, `Fixed` headings
- Keep in-progress work in `## [Unreleased]`
- Move `Unreleased` content into a dated release section when preparing a release
- Add release links at the bottom for tagged versions when applicable

**When to update `CHANGELOG.md`:**
- Additions of new standards, templates, directories, or contributor-facing files
- Significant updates to existing standards that affect repository usage
- Structural reorganizations, file moves, consolidations, or removals
- Changes to contributor workflow, review process, or repository-wide tooling/configuration
- Do **not** add minor typo fixes or small editorial tweaks unless they materially change guidance

## Questions?

- **"Where should new content go?"** → Create a new file in the appropriate `*-docs/` directory and update that directory's `README.md` index
- **"How do I link to another standard?"** → Use relative path: `[text](dev-docs/file.md)` or `[text](../product-docs/file.md)` for cross-directory links
- **"Should I duplicate content?"** → No, link to it instead. Review all standards directories for duplicate content and consolidate when appropriate
- **"What if I'm unsure about formatting?"** → Follow existing patterns in similar files
- **"How do I handle cross-discipline topics?"** → Link between relevant standards directories, avoid duplicating content
- **"Should I update the changelog?"** → Yes for notable repository, workflow, structure, or standards changes; no for minor editorial-only fixes
