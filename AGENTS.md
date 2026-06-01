# Contributing Process & Standards

This document outlines the contributing process and standards for this documentation repository, designed to guide both human contributors and AI agents.

## Repository purpose

This repository contains project-agnostic development standards organized as Markdown documentation across multiple discipline-specific directories (`dev-docs/`, `product-docs/`, `gtm-mktg-docs/`, `design-docs/`, `measurement-docs/`), each with its own `README.md` serving as the index.

## Contributing process

### Before Making Changes

1. **Review existing content**
   - Read relevant files in the appropriate `*-docs/` directory
   - Understand the structure and formatting patterns
   - Check the section's `README.md` index for related content

2. **Plan your changes**
   - Determine which file(s) need updates
   - Identify if new files are needed
   - Consider impact on related files and links

3. **Create a branch**
   - Use descriptive branch name: `feature/add-new-standard`, `fix/typo-in-security`, `chore/update-links`
   - Branch from `main`

### Making Changes

**For New Content:**
1. Create new file in the appropriate `*-docs/` directory with kebab-case filename
2. Follow existing file structure (title, sections, formatting)
3. Add entry to the section's `README.md` index
4. Link to related standards where appropriate
5. Verify all links work

**For Updates:**
1. Edit the relevant file(s) in the appropriate `*-docs/` directory
2. Maintain consistent formatting
3. Update links if structure changes
4. Update index if adding/removing files
5. Update `.cursorrules`, `CLAUDE.md`, and `AGENTS.md` if standards change

**For Fixes:**
1. Fix the issue (typo, broken link, formatting)
2. Verify related content is still accurate
3. Check for similar issues in other files

### Documentation Review Checklist

Before submitting a PR, verify:

**Content Quality:**
- [ ] Spelling and grammar are correct
- [ ] Language is clear and concise
- [ ] Examples are accurate and helpful
- [ ] Content follows DRY principle (no duplication)
- [ ] Avoids "business" terminology; uses "product goals", "objectives", "outcomes", "strategic goals" instead
- [ ] SMART goals framework used as primary goal-setting framework where applicable
- [ ] Incrementality emphasized for experiments: well-designed experiments that measure incrementality are the only way to understand actual impact
- [ ] Cross-references reviewed: All related topics linked across all standards directories
- [ ] DRY conflicts checked: No duplicate content, conflicts resolved, consolidation considered
- [ ] Style guide followed: Sentence casing for headings and labels, minimal to no em dashes

**Formatting:**
- [ ] Markdown syntax is correct
- [ ] Headers follow hierarchy (#, ##, ###)
- [ ] Code blocks have language tags
- [ ] Lists are properly formatted
- [ ] Long lists (5+ items) in README/index files use collapsible sections
- [ ] Tables are readable and aligned
- [ ] Formatting matches existing files

**Links:**
- [ ] All internal links use relative paths
- [ ] All links resolve correctly
- [ ] Link text is descriptive (not "click here")
- [ ] External links are still valid
- [ ] Section anchors work correctly

**Structure:**
- [ ] Filename matches main heading (kebab-case)
- [ ] File structure follows conventions
- [ ] Index file is updated if needed (in the appropriate `*-docs/` directory)
- [ ] Related files are updated if standards change (across all standards directories)

**Git:**
- [ ] Commit message follows Conventional Commits format
- [ ] Branch name is descriptive
- [ ] PR description is clear and complete
- [ ] One topic per PR (focused scope)

### PR Requirements

**All PRs must include:**

1. **Summary** (1-3 sentences)
   - What changed and why
   - Which files were modified
   - Link to related issue (if applicable)

2. **Documentation Checklist**
   - [ ] All links verified
   - [ ] Formatting consistent
   - [ ] Index updated (if structure changed)
   - [ ] Related files updated (if standards changed)
   - [ ] Spelling/grammar checked

3. **Scope Check**
   - One topic per PR
   - Changes are focused and related
   - Reviewers can understand changes quickly

### Review Process

**Reviewers should verify:**
- [ ] Content is accurate and clear
- [ ] Formatting follows standards
- [ ] Long lists use collapsible sections where appropriate
- [ ] All links work correctly
- [ ] Structure is consistent
- [ ] Related files are updated
- [ ] Commit messages are clear
- [ ] PR description is complete

**Common Issues to Check:**
- Broken internal links
- Inconsistent formatting
- Long lists that should be collapsible (5+ items in README/index files)
- Duplicated content (should be linked instead)
- Missing cross-references between standards directories
- DRY conflicts (duplicate content across files)
- Missing index updates
- Unclear or incomplete descriptions

### Keeping Files in Sync

**The Trio Files:**
- `.cursorrules` - Brief rules for AI assistants
- `CLAUDE.md` - Detailed contributor guidelines
- `AGENTS.md` - This file (contributing process)

**Sync Checklist:**
When updating standards that affect the trio:
- [ ] `.cursorrules` updated with key rule
- [ ] `CLAUDE.md` updated with detailed explanation
- [ ] `AGENTS.md` updated with process/checklist
- [ ] All three files reviewed for consistency

**When to Update the Trio:**
- Adding new documentation standards
- Changing formatting requirements
- Updating git workflow
- Modifying review process
- Changing file organization

### Version History

**Location:**
- Version history is maintained in `CHANGELOG.md` at the repository root
- Do **NOT** add version history sections to individual documentation files or section README files
- This ensures a single source of truth for change tracking

**Format:**
- Follow [Keep a Changelog](https://keepachangelog.com/en/1.0.0/) format
- Group changes under `Added`, `Changed`, `Removed`, `Fixed` headings
- Update `CHANGELOG.md` when making significant changes

### File Organization Standards

**Directory Structure:**
```
dev-standards/
├── README.md                    # Repository overview
├── CHANGELOG.md                 # Version history
├── LICENSE                      # License file
├── .cursorrules                 # AI assistant rules
├── CLAUDE.md                    # Contributor guidelines
├── AGENTS.md                    # This file
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

**Naming Conventions:**
- Filenames: kebab-case (e.g., `philosophy-principles.md`)
- Headers: Sentence case for all headings (capitalize first word and proper nouns only)
- Links: Use relative paths, descriptive text

**File Structure:**
Each standard file should:
1. Start with `#` title matching filename
2. Use `##` for major sections
3. Use `###` for subsections
4. Include examples where helpful
5. Link to related standards

### Git Workflow

**Commit Message Format:**
```
<type>(<scope>): <subject>

<body>

<footer>
```

**Types:**
- `docs:` - Documentation changes
- `fix:` - Corrections, typos, broken links
- `feat:` - New content or standards
- `refactor:` - Reorganization, restructuring
- `chore:` - Maintenance tasks

**Examples:**
```bash
git commit -m "docs: add new section on code organization"
git commit -m "fix: correct typo in security.md"
git commit -m "feat: add accessibility standards"
git commit -m "refactor: reorganize documentation structure"
```

**Branch Strategy:**
- `feature/description` - New content or major updates
- `fix/description` - Corrections and fixes
- `chore/description` - Maintenance and cleanup
- Always branch from `main`

### Common Tasks

**Adding a New Standard:**
1. Create the new file in the appropriate `*-docs/` directory (e.g., `dev-docs/new-standard.md`)
2. Follow existing file structure
3. Add to the section's `README.md` index
4. Link from related standards
5. Verify all links work

**Fixing a Broken Link:**
1. Find the broken link
2. Determine correct path
3. Update the link
4. Verify it works
5. Check for similar issues

**Updating Related Content:**
1. Identify all affected files
2. Update each file consistently
3. Verify links still work
4. Update index if structure changes
5. Update trio files if standards change

**Reorganizing Structure:**
1. Plan the new structure
2. Move/rename files
3. Update all internal links
4. Update index file
5. Verify all links work
6. Update trio files if needed

## Questions?

- **"Where do I add new content?"** → Create file in the appropriate `*-docs/` directory and update that section's `README.md` index
- **"How do I link to another standard?"** → Use `[text](dev-docs/file.md)` or `[text](../product-docs/file.md)` for cross-directory links
- **"What if I break a link?"** → Fix it immediately, check for others
- **"Should I update the trio files?"** → Yes, if standards or process change

