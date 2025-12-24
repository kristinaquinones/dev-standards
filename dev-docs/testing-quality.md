# Testing & Quality

## Testing strategy

**Pyramid Approach** (Many unit tests → Some integration → Few E2E):

1. **Unit Tests** (60–70% of test suite)
   - Test individual functions, modules, components
   - Isolated from external dependencies (mock APIs, databases)
   - Fast to run (<5ms per test)
   - Framework: Jest, Vitest, or equivalent

2. **Integration Tests** (20–30% of test suite)
   - Test how modules work together
   - Use realistic test fixtures
   - May hit real databases or file systems
   - Framework: Jest + Testing Library (for UI), or Supertest (for APIs)

3. **E2E Tests** (5–10% of test suite)
   - Test complete user workflows
   - Run in real browser/environment
   - Slow but high confidence
   - Framework: Playwright, Cypress, or equivalent

## Coverage targets

- **Absolute Minimum:** 60% overall coverage (libraries/utilities should be ≥80%)
- **Safe Zone:** 70–80% coverage (most bugs caught, diminishing ROI beyond 80%)
- **Overkill:** >85% coverage (only for critical path modules where cost of failure is high)

## Testing best practices

```typescript
// ✅ Good: Descriptive test names, realistic fixtures, clear assertions
describe('parseMarkdown', () => {
  it('should extract YAML frontmatter and markdown body', () => {
    const input = '---\ntitle: Test\n---\n# Content';
    const result = parseMarkdown(input);
    expect(result.frontmatter.title).toBe('Test');
    expect(result.body).toContain('# Content');
  });

  it('should handle missing frontmatter gracefully', () => {
    const input = '# Content only';
    const result = parseMarkdown(input);
    expect(result.frontmatter).toEqual({});
    expect(result.body).toBe('# Content only');
  });
});

// ❌ Bad: Unclear test name, no fixtures, brittle assertions
describe('parsing', () => {
  it('works', () => {
    expect(parseMarkdown('---\ntitle: Test\n---\n# Content')).toBeTruthy();
  });
});
```

## Running tests

```bash
npm test                      # Run all tests once
npm test -- --watch          # Watch mode (re-run on file change)
npm test -- --coverage       # Generate coverage report
npm run check                # Lint + typecheck + tests (full CI suite)
```

