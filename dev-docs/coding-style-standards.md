# Coding Style & Standards

## General Principles

### Naming Conventions

Choose naming conventions appropriate for your language and ecosystem:

- **Classes/Types:** Use language conventions (e.g., `PascalCase` in many languages, `snake_case` in Python/Ruby)
- **Functions/Variables:** Use language conventions (e.g., `camelCase` in JavaScript/Java, `snake_case` in Python/Ruby)
- **Constants:** Use language conventions (e.g., `SCREAMING_SNAKE_CASE` for true constants)
- **Files:** Follow ecosystem conventions (e.g., `kebab-case` for web projects, `snake_case` for Python, `PascalCase` for C# classes)

### Formatting Standards

- **Indentation:** Choose consistent indentation (2 or 4 spaces, or tabs) and enforce it across the project
- **Line Length:** Set a maximum line length (80-120 characters) and enforce it
- **Automated Formatting:** Use language-appropriate formatters to remove style debates (e.g., Prettier for JavaScript, Black for Python, gofmt for Go, rustfmt for Rust)
- **Linting:** Use language-appropriate linters for code quality (e.g., ESLint for JavaScript, pylint for Python, clippy for Rust)

### Type Safety

Where applicable, use type systems to catch errors early:

- Enable strict mode or equivalent in typed languages
- Add explicit type annotations on function parameters and return values
- Avoid disabling type checks or linting rules without documentation

## Language-Specific Examples

### TypeScript/JavaScript

```typescript
// ✅ Clear types, explicit return
export function parseUserInput(input: string): { name: string; email: string } {
  const [name, email] = input.split('|');
  return { name, email };
}

// ❌ Implicit types, unclear intent
export function parse(x: any): any {
  return x.split('|');
}
```

### Python

```python
# ✅ Clear types, explicit return
def parse_user_input(input: str) -> dict[str, str]:
    name, email = input.split('|')
    return {'name': name, 'email': email}

# ❌ No types, unclear intent
def parse(x):
    return x.split('|')
```

### Go

```go
// ✅ Clear function signature, explicit return
func ParseUserInput(input string) (name string, email string, err error) {
    parts := strings.Split(input, "|")
    if len(parts) != 2 {
        return "", "", errors.New("invalid input format")
    }
    return parts[0], parts[1], nil
}

// ❌ Unclear intent, no error handling
func Parse(x string) []string {
    return strings.Split(x, "|")
}
```

## Code review checklist

Before submitting code:
- [ ] Follows naming conventions
- [ ] No unused variables or imports
- [ ] Functions have clear purpose (name + types)
- [ ] No code duplication (DRY principle applied)
- [ ] No console.log() left in (use structured logging)
- [ ] Comments explain "why," not "what"
- [ ] Error handling is explicit (no swallowing errors)

