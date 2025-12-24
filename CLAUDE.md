# Contributor Guidelines for dev-standards

This document provides detailed guidelines for contributing to this documentation repository, especially when working with AI assistants like Claude.

## Repository overview

This repository contains project-agnostic standards across multiple disciplines (development, product, GTM/marketing, design, measurement) organized as Markdown files. Each discipline has its own directory with a README.md index file.

## Documentation standards

### Markdown Formatting

**Headers:**
- Use `#` for the main title (matches filename)
- Use `##` for major sections
- Use `###` for subsections
- Use `####` sparingly for nested subsections

**Code Blocks:**
- Always include language tags: ` ```typescript`, ` ```bash`, ` ```markdown`, etc.
- For inline code, use backticks: `` `code` ``
- Preserve indentation in code examples

**Lists:**
- Use `-` for unordered lists
- Use numbered lists (`1.`, `2.`, etc.) for ordered sequences
- Indent nested lists with 2 spaces
- Use `- [ ]` for checklists

**Collapsible Sections:**
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
  - Use descriptive summary text (e.g., "View all topics", "See full list")
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

### File Organization

**Naming Convention:**
- All filenames use kebab-case: `philosophy-principles.md`
- Filenames should match the main heading (lowercase, hyphenated)
- Keep filenames descriptive and clear

**Directory Structure:**
```
dev-standards/
├── README.md                    # Repository overview
├── CHANGELOG.md                 # Version history
├── LICENSE                      # License file
├── .cursorrules                 # AI assistant rules
├── claude.md                    # This file
├── AGENTS.md                    # Contributing process
├── dev-docs/                    # Development standards
│   └── README.md                # Development standards index
├── product-docs/                # Product management standards
│   └── README.md                # Product standards index
├── gtm-mktg-docs/              # GTM & Marketing standards
│   └── README.md                # GTM & Marketing standards index
├── design-docs/                 # Design standards
│   └── README.md                # Design standards index
└── measurement-docs/            # Measurement & Analytics standards
    └── README.md                # Measurement standards index
```

**File Structure:**
Each standard file should:
1. Start with a `#` title matching the filename
2. Include clear section headers (`##`)
3. Use consistent formatting throughout
4. Link to related standards when appropriate
5. Include examples where helpful

### Content Guidelines

**Clarity & Readability:**
- Write for humans first; assume the reader is familiar with software development but may be new to these specific standards
- Use clear, concise language
- Prefer active voice over passive
- Break long paragraphs into shorter ones
- Use bullet points for lists of items

**DRY Principle:**
- Don't duplicate content across files
- Link to related standards instead of repeating information
- If content appears in multiple places, consider consolidating it

**Consistency:**
- Follow existing patterns in the repository
- Use consistent terminology (e.g., "development standards" not "dev standards")
- Avoid "business" terminology; use "product goals", "objectives", "outcomes", "strategic goals" instead to be inclusive of indie makers, creators, and developers
- **SMART goals framework**: The primary goal-setting framework recommended throughout these standards (Specific, Measurable, Achievable, Relevant, Time-bound)
- **Incrementality in experiments**: Well-designed experiments that measure incrementality are the only way to understand the actual impact of a change or intervention; observed data over time alone is insufficient
- Maintain consistent formatting style
- Keep tone professional but approachable

**Style Guide:**
- **Headings and labels**: Use sentence casing (capitalize first word and proper nouns only)
- **Em dashes**: Minimal to no use of em dashes; prefer commas, periods, or parentheses instead

**Cross-Referencing:**
- Link to related standards using relative paths
- Update links when files are moved or renamed
- Use descriptive link text (not "click here")
- Verify all links work before committing

### Git Workflow

**Commit Messages:**
Use Conventional Commits format:
- `docs: add new section on code organization`
- `fix: correct typo in security.md`
- `feat: add new accessibility standards`
- `refactor: reorganize documentation structure`

**Branch Strategy:**
- `feature/description` for new content or major updates
- `fix/description` for corrections
- `chore/description` for maintenance tasks
- Always branch from `main`

**Pull Requests:**
- One topic per PR (keep scope focused)
- Include clear description of changes
- Verify all links work
- Update index file if adding/removing files
- Update related files if changing standards

### Working with AI Assistants

**When asking AI to help:**
- Be specific about which file(s) to modify
- Reference existing patterns: "Follow the same format as philosophy-principles.md"
- Ask for link verification: "Check all links in the file"
- Request consistency checks: "Ensure formatting matches other files"

**AI should:**
- Maintain existing formatting patterns
- Use relative paths for links
- Follow the file naming conventions
- Update related files when making changes
- Verify links before suggesting changes

**AI should NOT:**
- Create new files without updating the index
- Break existing links
- Change formatting style arbitrarily
- Duplicate content that should be linked instead

### Link Maintenance

**Internal Links:**
- Always use relative paths: `[text](dev-docs/file.md)`
- For section links: `[text](dev-docs/file.md#section-name)`
- Verify links work after moving/renaming files
- Update links in all affected files when structure changes

**Link Verification:**
Before committing:
1. Check all internal links resolve correctly
2. Verify external links are still valid
3. Ensure anchor links point to correct sections
4. Update broken or moved links

### Cross-Reference Review

**Reviewing for Cross-References:**
- Identify related topics across all standards directories
- Link between related sections (e.g., product-docs → dev-docs, product-docs → measurement-docs)
- Check for missed connections between disciplines
- Ensure cross-discipline topics are properly linked

**DRY Conflict Checking:**
- Identify duplicate content across files
- Resolve conflicts by consolidating or linking
- Check for content that appears in multiple places
- Consider if duplicate content should be consolidated into a shared file
- Ensure all standards directories are reviewed for conflicts

### Documentation Review Checklist

Before submitting a PR:
- [ ] Spelling and grammar checked
- [ ] All links verified (internal and external)
- [ ] Formatting consistent with existing files
- [ ] File structure follows conventions
- [ ] Related files updated (especially index files and trio files)
- [ ] Cross-references reviewed: All related topics linked across all standards directories
- [ ] DRY conflicts checked: No duplicate content, conflicts resolved
- [ ] Commit message follows Conventional Commits format
- [ ] PR description is clear and complete

### Keeping Files in Sync

**The Trio:**
- `.cursorrules` - Brief rules for AI assistants
- `claude.md` - This file (detailed guidelines)
- `AGENTS.md` - Contributing process

**When updating standards:**
1. Update the relevant file in the appropriate `*-docs/` directory
2. Update the relevant `*-docs/README.md` index if structure changes
3. Review for cross-referencing opportunities across all standards directories
4. Check for DRY conflicts and resolve or consolidate as needed
5. Update `.cursorrules`, `claude.md`, and `AGENTS.md` if standards change
6. Keep all three files consistent with each other

### Version History

**Location:**
- Version history is maintained **ONLY** in the root `README.md` file
- Do **NOT** add version history sections to individual documentation files or section README files
- This ensures a single source of truth for change tracking and follows DRY principles

**Format:**
- Use a table with columns: Version | Date | Contributor | Changes
- Contributor should be in GitHub username format: `@username`
- Include meaningful descriptions of what changed in each version

## Questions?

- **"Where should new content go?"** → Create a new file in the appropriate `*-docs/` directory and update that directory's README.md index
- **"How do I link to another standard?"** → Use relative path: `[text](dev-docs/file.md)` or `[text](../product-docs/file.md)` for cross-directory links
- **"Should I duplicate content?"** → No, link to it instead. Review all standards directories for duplicate content and consolidate when appropriate
- **"What if I'm unsure about formatting?"** → Follow existing patterns in similar files
- **"How do I handle cross-discipline topics?"** → Link between relevant standards directories, avoid duplicating content

