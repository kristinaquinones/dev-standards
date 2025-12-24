# Coding Style & Standards

## Language-Specific Standards

### TypeScript/JavaScript
- **Strict Mode:** Enable TypeScript strict mode (`"strict": true`)
- **Type Annotations:** Explicit types on function parameters and return values
- **Naming:**
  - `PascalCase` for classes, components, types
  - `camelCase` for functions, variables, props
  - `kebab-case` for filenames (utilities), `PascalCase` for components/routes
  - `SCREAMING_SNAKE_CASE` for constants only when truly constant (config values)
- **Formatting:**
  - 2-space indentation (configurable; pick one and enforce)
  - Use formatter (Prettier) to remove style debates
  - Linter (ESLint) for code quality
- **No Inline Disables:** Avoid `// @ts-ignore`, `// eslint-disable` unless documented

### Example: Good TypeScript
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

## Code review checklist

Before submitting code:
- [ ] Follows naming conventions
- [ ] No unused variables or imports
- [ ] Functions have clear purpose (name + types)
- [ ] No code duplication (DRY principle applied)
- [ ] No console.log() left in (use structured logging)
- [ ] Comments explain "why," not "what"
- [ ] Error handling is explicit (no swallowing errors)

