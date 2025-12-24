# Pull Requests & Code Review

## PR Requirements

**All PRs must include:**

1. **Summary** (1–3 sentences)
   - What changed and why?
   - Link to related issue

2. **Testing Checklist**
   - Linting passes ✅
   - Type checking passes (if applicable) ✅
   - All tests pass ✅
   - Build succeeds ✅
   - Manual testing completed (if applicable)

3. **Documentation Updates**
   - Progress log created: `docs/progress/YYYY_MM_DD.md`
   - User-facing docs updated (if applicable)
   - Developer docs updated (if applicable)
   - CHANGELOG.md updated under `[Unreleased]` section

4. **Scope Check**
   - One feature/fix per PR (no unrelated changes)
   - Reviewers can understand the change in 15 minutes

## Code review checklist

Reviewers should verify:
- [ ] Code follows team standards (style, naming, patterns)
- [ ] Tests are present and meaningful
- [ ] No obvious bugs or security issues
- [ ] Documentation is clear and linked
- [ ] Commit messages are clear
- [ ] PR description is complete

