# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2026-06-01

### Added
- Added `measurement-docs/` with standards for analytics strategy, A/B testing & experimentation, data analysis & interpretation, and data governance
- Added `gtm-mktg-docs/` standards covering channel strategy, GTM launch planning, marketing PRDs, marketing specs, and positioning & messaging
- Added reusable templates for GTM & marketing workflows in `gtm-mktg-docs/templates/`
- Added reusable design templates in `design-docs/templates/` for design handoff, design system documentation, and usability testing plans
- Added `user-story-template.md` to `product-docs/templates/`
- Added `CONTRIBUTING.md` to document contribution expectations and repository workflow
- Added repository markdown tooling configuration via `.markdownlint.json` and `.markdown-link-check.json`
- Added GitHub-specific repository automation/configuration in `.github/`

### Changed
- Expanded the repository from development-only standards into a broader multi-discipline standards library spanning development, product, design, GTM/marketing, and measurement
- Made `dev-docs/` standards project-agnostic by removing framework-specific references (Next.js, React, npm, etc.)
- Updated `code-organization.md` to use generic directory structures instead of framework-specific examples
- Updated `coding-style-standards.md` to include examples for TypeScript/JavaScript, Python, and Go instead of only TypeScript
- Updated `testing-quality.md` to use generic test framework references instead of Jest/Vitest/Playwright/Cypress
- Updated `cicd-build-pipeline.md` to use placeholder commands instead of npm-specific commands
- Updated `git-version-control.md` to use generic framework examples instead of Next.js-specific examples
- Updated `pull-requests-code-review.md` to use generic test commands instead of npm-specific commands
- Updated `onboarding-knowledge-transfer.md` to provide generic onboarding guidance with placeholders
- Updated `architecture-decisions.md` to use a generic static typing example instead of a TypeScript-specific example
- Updated `performance-scalability.md` to use generic image optimization guidance instead of the Next.js Image component
- Updated `security.md` to use generic dependency management commands instead of npm-specific commands
- Consolidated `feature-definition-requirements.md` and `user-centered-design-process.md` into unified `product-design-process.md` in `product-docs/`
- Merged `prd-template.md` and `design-brief-template.md` into unified `product-design-brief-template.md` in `product-docs/templates/`
- Updated repository structure and README/index files to reflect the current folder-based organization across all disciplines
- Design docs now focus on specialized frameworks such as information architecture, interaction design, and usability evaluation, while product docs contain the unified product/design process

### Removed
- Removed `product-docs/feature-definition-requirements.md` in favor of `product-design-process.md`
- Removed `design-docs/user-centered-design-process.md` in favor of `product-design-process.md`
- Removed `product-docs/templates/prd-template.md` in favor of `product-design-brief-template.md`
- Removed `design-docs/templates/design-brief-template.md` in favor of `product-design-brief-template.md`

## [1.0.0] - 2025-12-23

### Added
- Initial version of development standards extracted from EmberDocs project standards
- Reorganized development standards into discrete files in `dev-docs/` directory with `dev-docs/README.md` as index
- Created comprehensive documentation structure with 15 individual standard files:
  - Philosophy & Principles
  - Code Organization
  - Coding Style & Standards
  - Testing & Quality
  - Documentation
  - Git & Version Control
  - Pull Requests & Code Review
  - Configuration & Secrets
  - CI/CD & Build Pipeline
  - Performance & Scalability
  - Accessibility & Inclusivity
  - Security
  - Architecture Decisions
  - Onboarding & Knowledge Transfer
  - Sync Instructions for .cursorrules, CLAUDE.md, AGENTS.md
- Added `.cursorrules`, `CLAUDE.md`, and `AGENTS.md` for documentation repository standards
- Created placeholder structure for GTM & Marketing standards (`gtm-mktg-docs/README.md`)
- Created placeholder structure for Product Management standards (`product-docs/README.md`)
- Created placeholder structure for Design standards (`design-docs/README.md`)
- Added `CHANGELOG.md` to track version history
- Added collapsible section guidelines for long lists in README and index files

### Changed
- Moved all standards index files to their respective folders as README.md files (following GitHub conventions)
- Updated README.md with new repository structure, expanded scope including all standards sections, and folder-based navigation
- Reorganized README.md structure to include all standards types (Development, Product, GTM & Marketing, Design)
- Updated documentation standards to include collapsible section best practices

[1.0.0]: https://github.com/kristinaquinones/dev-standards/releases/tag/v1.0.0
