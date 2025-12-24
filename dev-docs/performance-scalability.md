# Performance & Scalability

## Performance targets (adjust per project)

| Metric | Target | Tools |
|--------|--------|-------|
| Lighthouse Performance | ≥85 | Lighthouse CI |
| Lighthouse Accessibility | ≥90 | Lighthouse CI |
| First Contentful Paint (FCP) | <2s | Web Vitals |
| Cumulative Layout Shift (CLS) | <0.1 | Web Vitals |
| Time to Interactive (TTI) | <3.5s | Web Vitals |
| Bundle Size | <300KB (gzipped) | bundlesize/size-limit |
| API Response Time | <200ms (p95) | APM tools |
| Database Query Time | <100ms (p95) | Database profiling |

## Performance checklist

Before merging:
- [ ] No new large dependencies added without justification
- [ ] Images are optimized (Next.js Image component, WebP, responsive sizes)
- [ ] No N+1 queries (batch database operations)
- [ ] Expensive operations are cached or memoized
- [ ] Code splitting is in place (lazy load heavy routes)
- [ ] Bundle size is monitored and trending down

