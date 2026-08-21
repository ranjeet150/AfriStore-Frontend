# AfriStore-Frontend


The Next.js 16 frontend for the [Afristore Marketplace](https://github.com/Afristore/marketplace) — extracted from the monorepo into its own dedicated repository.

This application includes:
- **Next.js 16** — App Router, server components, and API routes
- **Freighter & Magic Wallet** — Stellar wallet integration
- **Sentry** — Error monitoring via `@sentry/nextjs`
- **PostHog** — Product analytics
- **Playwright** — End-to-end testing
- **Jest** — Unit and component testing

---

##  Getting Started (once code is populated)

```bash
npm install
npm run dev           # Start dev server on localhost:3000
npm run test          # Run Jest unit tests
npm run test:e2e      # Run Playwright E2E tests
npm run build         # Production build
```

---

##  Environment Variables

Copy `.env.example` to `.env.local` and fill in:

| Variable | Description |
|---|---|
| `NEXT_PUBLIC_INDEXER_URL` | URL of the Afristore-Backend API |
| `NEXT_PUBLIC_MAGIC_API_KEY` | Magic.link publishable API key |
| `NEXT_PUBLIC_SENTRY_DSN` | Sentry DSN for error reporting |
| `NEXT_PUBLIC_POSTHOG_KEY` | PostHog analytics key |
| `NEXT_PUBLIC_NETWORK` | Stellar network (`testnet` or `mainnet`) |
| `NEXT_PUBLIC_CONTRACT_ID` | Soroban Marketplace contract address |
| `NEXT_PUBLIC_E2E_MOCK_CHAIN` | Set to `true` for E2E test runs |

---

##  Source Location (Monorepo)

This repository is being extracted from [`afristore/frontend/afristore-app/`](https://github.com/Afristore/marketplace/tree/master/frontend/afristore-app) in the main monorepo.

**Tracked in:** [ui-ux-issues.md — Issue 121](https://github.com/Afristore/marketplace/blob/master/ui-ux-issues.md)

---

##  Contributing

1. Fork this repository
2. Create a feature branch: `git checkout -b feat/your-feature`
3. Make your changes and ensure all CI checks pass:
   - `npm run lint` — ESLint must exit 0
   - `npm run type-check` — TypeScript `tsc --noEmit` must exit 0
   - `npm run test` — All 202 Jest tests must pass
   - `npm run build` — Next.js production build must succeed
4. Open a PR — **all CI must pass before a PR is eligible for review and merge**

---

##  Tech Stack

- Next.js 16 / React 18 / TypeScript
- `@stellar/freighter-api` + `magic-sdk`
- `@sentry/nextjs` + `posthog-js`
- Jest + `@testing-library/react`
- Playwright (E2E)

---

##  License

MIT — see [LICENSE](./LICENSE)
