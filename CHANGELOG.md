# Changelog

All notable changes to this repository will be documented in this file.

The format is based on [Keep a Changelog](https://keepachangelog.com/en/1.0.0/),
and this project adheres to [Semantic Versioning](https://semver.org/spec/v2.0.0.html).

## [Unreleased]

## [1.1.0] - 2026-06-01

### Added
- Added `measurement-docs/` with standards for analytics strategy, A/B testing & experimentation, data analysis & interpretation, and data governance
- Added `gtm-mktg-docs/` with standards for channel strategy, GTM launch planning, marketing PRDs, marketing specs, and positioning & messaging
- Added reusable templates in `gtm-mktg-docs/templates/` for GTM and marketing workflows
- Added reusable templates in `design-docs/templates/` for design handoff, design system documentation, and usability testing plans
- Added `product-docs/templates/user-story-template.md`
- Added `CONTRIBUTING.md` for repository contribution guidance
- Added markdown quality tooling via `.markdownlint.json` and `.markdown-link-check.json`
- Added repository automation and configuration in `.github/`

### Changed
- Expanded the repository from development-only standards into a broader multi-discipline standards library spanning development, product, design, GTM/marketing, and measurement
- Made `dev-docs/` standards project-agnostic by removing framework-specific references
- Updated `dev-docs/code-organization.md` to use generic directory structures instead of framework-specific examples
- Updated `dev-docs/coding-style-standards.md` to include examples for TypeScript/JavaScript, Python, and Go
- Updated `dev-docs/testing-quality.md` to use generic test framework references instead of tool-specific examples
- Updated `dev-docs/cicd-build-pipeline.md` to use placeholder commands instead of package-manager-specific commands
- Updated `dev-docs/git-version-control.md` to use generic examples instead of framework-specific examples
- Updated `dev-docs/pull-requests-code-review.md` to use generic test commands
- Updated `dev-docs/onboarding-knowledge-transfer.md` to provide generic onboarding guidance with placeholders
- Updated `dev-docs/architecture-decisions.md` to use a generic static typing example
- Updated `dev-docs/performance-scalability.md` to use generic image optimization guidance
- Updated `dev-docs/security.md` to use generic dependency management commands
- Consolidated `product-docs/feature-definition-requirements.md` and `design-docs/user-centered-design-process.md` into `product-docs/product-design-process.md`
- Merged `product-docs/templates/prd-template.md` and `design-docs/templates/design-brief-template.md` into `product-docs/templates/product-design-brief-template.md`
- Updated repository structure and README/index files to reflect the current folder-based organization across all disciplines
- Refocused design docs on specialized frameworks such as information architecture, interaction design, and usability evaluation, while product docs contain the unified product/design process

### Removed
- Removed `product-docs/feature-definition-requirements.md` in favor of `product-docs/product-design-process.md`
- Removed `design-docs/user-centered-design-process.md` in favor of `product-docs/product-design-process.md`
- Removed `product-docs/templates/prd-template.md` in favor of `product-docs/templates/product-design-brief-template.md`
- Removed `design-docs/templates/design-brief-template.md` in favor of `product-docs/templates/product-design-brief-template.md`

## [1.0.0] - 2025-12-23

### Added
- Initial version of development standards extracted from EmberDocs project standards
- Reorganized development standards into discrete files in `dev-docs/` with `dev-docs/README.md` as the index
- Created a comprehensive documentation structure with 15 individual standard files:
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
  - Sync Instructions for `.cursorrules`, `CLAUDE.md`, and `AGENTS.md`
- Added `.cursorrules`, `CLAUDE.md`, and `AGENTS.md` for documentation repository standards
- Created placeholder structure for GTM & Marketing standards in `gtm-mktg-docs/README.md`
- Created placeholder structure for Product Management standards in `product-docs/README.md`
- Created placeholder structure for Design standards in `design-docs/README.md`
- Added `CHANGELOG.md` to track version history
- Added collapsible section guidelines for long lists in README and index files

### Changed
- Moved all standards index files to their respective folders as `README.md` files, following GitHub conventions
- Updated `README.md` with the new repository structure, expanded scope, and folder-based navigation
- Reorganized `README.md` to include all standards types: Development, Product, GTM & Marketing, and Design
- Updated documentation standards to include collapsible section best practices

[1.1.0]: https://github.com/kristinaquinones/dev-standards/releases/tag/v1.1.0
[1.0.0]: https://github.com/kristinaquinones/dev-standards/releases/tag/v1.0.0
