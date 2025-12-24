# Contributing to dev-standards

This repository contains project-agnostic standards across multiple disciplines (development, product, GTM/marketing, design, measurement) organized as Markdown files. Each discipline has its own directory with a README.md index file.

## Contributing process

### Before making changes

1. **Review existing content**
   - Read relevant files in the appropriate `*-docs/` directory
   - Understand the structure and formatting patterns
   - Check the section README.md index for related content

2. **Plan your changes**
   - Determine which file(s) need updates
   - Identify if new files are needed
   - Consider impact on related files and links

3. **Create a branch**
   - Use descriptive branch name: `feature/add-new-standard`, `fix/typo-in-security`, `chore/update-links`
   - Branch from `main`

### Making changes

**For new content:**
1. Create new file in appropriate `*-docs/` directory with kebab-case filename
2. Follow existing file structure (title, sections, formatting)
3. Add entry to the section's README.md index
4. Link to related standards where appropriate
5. Verify all links work

**For updates:**
1. Edit the relevant file(s) in the appropriate `*-docs/` directory
2. Maintain consistent formatting
3. Update links if structure changes
4. Update index if adding/removing files
5. Update `.cursorrules`, `claude.md`, and `AGENTS.md` if standards change

**For fixes:**
1. Fix the issue (typo, broken link, formatting)
2. Verify related content is still accurate
3. Check for similar issues in other files

### Pull request requirements

**All PRs must include:**

1. **Summary** (1-3 sentences)
   - What changed and why
   - Which files were modified
   - Link to related issue (if applicable)

2. **Documentation checklist**
   - [ ] All links verified
   - [ ] Formatting consistent
   - [ ] Index updated (if structure changed)
   - [ ] Related files updated (if standards changed)
   - [ ] Spelling/grammar checked

3. **Scope check**
   - One topic per PR
   - Changes are focused and related
   - Reviewers can understand changes quickly

### Review process

**Reviewers should verify:**
- [ ] Content is accurate and clear
- [ ] Formatting follows standards
- [ ] All links work correctly
- [ ] Structure is consistent
- [ ] Related files are updated
- [ ] Commit messages are clear
- [ ] PR description is complete

## Questions?

### General questions

- **"What are universal standards?"** → Everything in the `*-docs/` directories applies across projects
- **"What's project-specific?"** → Tech stack choices, library selections, deployment platforms, organizational details, brand identity, industry-specific requirements
- **"How do I customize this?"** → Copy sections and adapt for your organization's needs. For project-specific standards, copy to `.cursorrules`, `claude.md`, or `AGENTS.md` and override with your project's choices
- **"How often should I update?"** → When standards change (major new decision, team feedback, emerging best practices, new frameworks, updated best practices)
- **"Should I commit these files?"** → Yes! Keep all standards files in version control. They're documentation, not templates.

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

- **[.cursorrules](.cursorrules)** - Brief rules for AI assistants
- **[claude.md](claude.md)** - Detailed contributor guidelines
- **[AGENTS.md](AGENTS.md)** - Contributing process and standards
