# Testing & Quality

## Testing strategy

**Pyramid Approach** (Many unit tests → Some integration → Few E2E):

1. **Unit Tests** (60–70% of test suite)
   - Test individual functions, modules, components
   - Isolated from external dependencies (mock APIs, databases)
   - Fast to run (<5ms per test)
   - Use appropriate testing framework for your language/ecosystem

2. **Integration Tests** (20–30% of test suite)
   - Test how modules work together
   - Use realistic test fixtures
   - May hit real databases or file systems
   - Use appropriate testing framework for your language/ecosystem

3. **E2E Tests** (5–10% of test suite)
   - Test complete user workflows
   - Run in real browser/environment (for web apps) or production-like environments
   - Slow but high confidence
   - Use appropriate E2E testing tools for your platform

## Coverage targets

- **Absolute Minimum:** 60% overall coverage (libraries/utilities should be ≥80%)
- **Safe Zone:** 70–80% coverage (most bugs caught, diminishing ROI beyond 80%)
- **Overkill:** >85% coverage (only for critical path modules where cost of failure is high)

## Testing best practices

### General Principles

Write tests that are:
- **Descriptive**: Test names clearly state what they're testing
- **Realistic**: Use realistic test fixtures and data
- **Clear**: Assertions are explicit and meaningful
- **Isolated**: Tests don't depend on each other

### JavaScript/TypeScript Example

```javascript
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

### Python Example

```python
# ✅ Good: Descriptive test names, realistic fixtures, clear assertions
def test_parse_markdown_extracts_frontmatter_and_body():
    input_text = '---\ntitle: Test\n---\n# Content'
    result = parse_markdown(input_text)
    assert result['frontmatter']['title'] == 'Test'
    assert '# Content' in result['body']

def test_parse_markdown_handles_missing_frontmatter():
    input_text = '# Content only'
    result = parse_markdown(input_text)
    assert result['frontmatter'] == {}
    assert result['body'] == '# Content only'

# ❌ Bad: Unclear test name, no fixtures, brittle assertions
def test_parsing():
    assert parse_markdown('---\ntitle: Test\n---\n# Content')
```

## Running tests

Adapt these commands to your project's testing setup:

```bash
# Run all tests once
<test-command>                  # e.g., npm test, pytest, go test, cargo test

# Watch mode (re-run on file change)
<test-command> --watch          # e.g., npm test -- --watch, pytest-watch

# Generate coverage report
<test-command> --coverage       # e.g., npm test -- --coverage, pytest --cov

# Full CI suite (lint + typecheck + tests)
<check-command>                 # e.g., npm run check, make test, cargo test
```

