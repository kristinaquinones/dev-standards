# CI/CD & Build Pipeline

## Standard build steps

```bash
# Install dependencies
<install-command>           # e.g., npm install, pip install -r requirements.txt, go mod download

# Lint code
<lint-command>              # e.g., npm run lint, pylint src/, cargo clippy

# Type checking (if applicable)
<typecheck-command>         # e.g., npm run typecheck, mypy src/, tsc --noEmit

# Run tests
<test-command>              # e.g., npm test, pytest, go test ./..., cargo test

# Build production artifacts
<build-command>             # e.g., npm run build, python setup.py build, go build, cargo build --release

# Verify build (optional)
<verify-command>            # e.g., smoke tests, build artifact validation
```

## GitHub Actions Template

```yaml
name: CI

on: [push, pull_request]

jobs:
  build:
    runs-on: ubuntu-latest

    steps:
      - uses: actions/checkout@v4
      
      # Setup environment (adapt to your language/stack)
      # - uses: actions/setup-node@v4    # for Node.js
      # - uses: actions/setup-python@v4  # for Python
      # - uses: actions/setup-go@v4      # for Go

      - name: Install dependencies
        run: <install-command>

      - name: Lint
        run: <lint-command>

      - name: Type check
        run: <typecheck-command>

      - name: Tests
        run: <test-command>   # include coverage flag per tool: jest --coverage, pytest --cov, go test -cover

      - name: Build
        run: <build-command>
```

## Deployment strategy

1. **Development**: Deploy on every PR merge to `main`
2. **Staging**: Deploy on tagged pre-release (e.g., `v1.2.3-beta`)
3. **Production**: Deploy on stable release tag (e.g., `v1.2.3`)

