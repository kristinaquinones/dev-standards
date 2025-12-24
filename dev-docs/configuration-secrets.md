# Configuration & Secrets

## Environment variables

1. **Public Variables** (safe to expose, checked in)
   - Framework config: `NEXT_PUBLIC_API_URL`
   - Feature flags: `FEATURE_EXPERIMENTAL_SEARCH`
   - App metadata: `NEXT_PUBLIC_VERSION`

2. **Private Variables** (sensitive, NOT checked in)
   - API keys, database passwords
   - Service credentials
   - Private endpoints

## Setup

```bash
# 1. Create .env.example with public + placeholder vars (checked in)
NEXT_PUBLIC_SITE_NAME=MyApp
NEXT_PUBLIC_API_URL=https://api.example.com
DATABASE_PASSWORD=<change-me>
STRIPE_SECRET_KEY=<change-me>

# 2. Create .env.local with real values (add to .gitignore, NOT checked in)
NEXT_PUBLIC_SITE_NAME=MyApp
NEXT_PUBLIC_API_URL=https://api.example.com
DATABASE_PASSWORD=actual_secret_here
STRIPE_SECRET_KEY=sk_test_xxxx

# 3. In code, access via process.env
const apiUrl = process.env.NEXT_PUBLIC_API_URL; // public, OK in browser
const dbPass = process.env.DATABASE_PASSWORD;   // private, server-only
```

## Security rules

- ✅ Commit `.env.example` (template only)
- ❌ Never commit `.env.local`, `.env.production`, or files with real secrets
- ✅ Use env vars for all secrets, never hardcode
- ✅ Rotate secrets regularly in production
- ✅ Use separate secrets for dev, staging, production

