# CI/CD & Build Pipeline

## Standard build steps

```bash
npm install              # Install dependencies
npm run lint            # ESLint + Prettier
npm run typecheck       # TypeScript checks
npm run test            # Unit + integration tests
npm run build           # Production build
npm run build:verify    # Verify build output (optional smoke tests)
```

## GitHub Actions Template

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

## Deployment strategy

1. **Development**: Deploy on every PR merge to `main`
2. **Staging**: Deploy on tagged pre-release (e.g., `v1.2.3-beta`)
3. **Production**: Deploy on stable release tag (e.g., `v1.2.3`)

