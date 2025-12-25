# Code Organization

## Directory structure template

```
project-root/
├── src/                      # Application source code
│   ├── app/                  # Application entry points, main modules, or framework-specific code
│   ├── lib/                  # Shared utilities & business logic
│   │   ├── utils/
│   │   ├── services/
│   │   ├── config/
│   │   └── types/
│   ├── components/           # Reusable components (UI, domain logic, etc.)
│   │   ├── common/
│   │   ├── layout/
│   │   └── features/
│   ├── styles/               # Global stylesheets & design tokens (if applicable)
│   └── __tests__/            # Test files (colocated or separate)
├── tests/                    # Integration & E2E tests (optional)
├── docs/                     # Developer documentation
│   ├── planning/             # Phase plans, roadmaps, specs
│   ├── progress/             # Daily/weekly progress logs
│   └── QUICK-REFERENCE.md    # Developer cheat sheet
├── user-docs/                # User-facing guides
├── brand/                    # Design assets, logos, style guide
├── config/                   # Configuration files
├── .github/                  # GitHub Actions, PR templates, issue templates
├── public/                   # Static assets (if applicable)
├── .env.example              # Template for env vars (checked in)
├── .env.local                # Local env vars (NOT checked in; in .gitignore)
├── .gitignore
├── .cursorrules              # AI assistant guidelines (sync with claude.md, AGENTS.md)
├── claude.md                 # Contributor guidelines (sync with .cursorrules, AGENTS.md)
├── AGENTS.md                 # Contributing process & standards (sync with .cursorrules, claude.md)
├── dev-docs/README.md        # Development standards index
├── README.md
└── CHANGELOG.md
```

## Module organization principles

- **Functional Cohesion:** Group related code together (by feature, not by type)
- **Clear Boundaries:** Each module has a single responsibility
- **Explicit Dependencies:** Import statements show data/function flow
- **Reusability:** Utilities/services are testable and independent
- **Configuration Isolation:** Config files are centralized; avoid magic values in code

