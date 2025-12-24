# Accessibility & Inclusivity

## Accessibility standards

**Target:** WCAG 2.1 Level AA minimum (US ADA + EU compliance)

## Checklist

- [ ] **Color Contrast:** ≥4.5:1 for text, ≥3:1 for UI components
- [ ] **Keyboard Navigation:** All interactive elements accessible via Tab, Enter, Escape
- [ ] **ARIA Labels:** Buttons, form fields, landmarks have descriptive labels
- [ ] **Focus Indicator:** Clear focus visible on all interactive elements
- [ ] **Responsive Design:** Works on 320px–1920px viewports
- [ ] **Form Validation:** Clear error messages, accessible error handling
- [ ] **Image Alt Text:** All images have meaningful alt text (or `alt=""` if decorative)
- [ ] **Semantic HTML:** Use `<button>`, `<form>`, `<nav>`, `<header>`, etc., not `<div>` + ARIA
- [ ] **Screen Reader Testing:** Test with NVDA (Windows), JAWS, or VoiceOver (Mac)
- [ ] **Lighthouse Accessibility Score:** ≥95

## Tools

- **Axe DevTools** (browser extension) - automated accessibility scanning
- **Lighthouse** (Chrome DevTools) - accessibility audit
- **WAVE** (browser extension) - visual accessibility feedback
- **Screen Readers:** NVDA (free, Windows), JAWS (paid, Windows), VoiceOver (built-in, Mac)

