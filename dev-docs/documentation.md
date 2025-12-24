# Documentation

## Types of Documentation

| Type | Where | Audience | Updated |
|------|-------|----------|---------|
| **README.md** | Root | New users, overview | Every release |
| **dev-docs/README.md** | dev-docs/ | All developers | When standards change |
| **docs/** (developer) | `docs/` folder | Team members, contributors | Per PR/feature |
| **user-docs/** | `user-docs/` folder | End users, operators | Per release |
| **API Documentation** | Inline JSDoc + `docs/API.md` | Developers using the module | Per API change |
| **Architecture Decisions** | `docs/ARCHITECTURE-DECISIONS.md` | Long-term reference | When major decision made |
| **Progress Logs** | `docs/progress/YYYY_MM_DD.md` | Team sync, knowledge capture | Daily or per sprint |
| **Inline Comments** | In code | Future maintainers | When logic isn't obvious |

## Documentation standards

1. **Keep Docs in Version Control**
   - Treat docs as code; review before merging
   - Outdated docs in repo > no docs
   - Use Markdown for readability and git diffs

2. **Link Related Docs**
   - Cross-reference related specs, APIs, decision logs
   - Update links when docs move

3. **API Documentation Template**
   ```typescript
   /**
    * Parses markdown content with YAML frontmatter.
    *
    * @param input Raw markdown string (e.g., "---\ntitle: ...\n---\n# Content")
    * @returns Object with `frontmatter` (YAML) and `body` (markdown content)
    *
    * @example
    * const { frontmatter, body } = parseMarkdown('---\ntitle: Test\n---\n# Title');
    * console.log(frontmatter.title); // "Test"
    *
    * @throws Error if frontmatter is malformed
    */
   export function parseMarkdown(input: string): { frontmatter: Record<string, any>; body: string } {
     // implementation
   }
   ```

4. **Progress Logs Template**
   ```markdown
   # Progress: YYYY-MM-DD

   ## Summary
   - ✅ Completed feature X
   - ✅ Fixed bug Y

   ## Work Done
   - Detailed breakdown of what was implemented

   ## Blockers/Open Questions
   - Any issues that need discussion

   ## Next Steps
   - What comes next
   ```

