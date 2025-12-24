# Security

## Code security checklist

- [ ] **Input Validation:** All user input is validated, escaped, or parameterized
- [ ] **No SQL Injection:** Use parameterized queries, never string concatenation
- [ ] **No XSS:** Sanitize HTML, use templating engines, Content Security Policy (CSP)
- [ ] **Authentication:** Secure session management, no credentials in URLs
- [ ] **Authorization:** Check permissions server-side, never trust client-side checks
- [ ] **Secrets:** Never commit API keys, passwords, tokens (use .env.local + .gitignore)
- [ ] **Dependencies:** Keep packages up to date; audit with `npm audit`
- [ ] **HTTPS Only:** Enforce HTTPS in production
- [ ] **CORS:** Restrict CORS origins to trusted domains
- [ ] **Rate Limiting:** Implement rate limits on APIs to prevent abuse

## Dependency management

```bash
npm audit                    # Find known vulnerabilities
npm audit fix                # Auto-fix where possible
npm update                   # Update to latest minor/patch versions
npm outdated                 # See what's outdated
```

## Regular security practices

- [ ] Rotate secrets monthly (or per-incident)
- [ ] Audit dependencies quarterly
- [ ] Security review of major features before release
- [ ] Incident response plan documented and practiced

