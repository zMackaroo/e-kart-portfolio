# E-Kart — Product Brief

**Portfolio:** [Home](index.html) · [Promo](ekart-promo.html) · [Case Study](ekart-case-study.html) · [Mockups](ekart-mockups.html) · [System Design](ekart-system-design.html) · [App Flow](ekart-app-flow.html)

---

**App title:** E-Kart

**App description:** E-Kart is an iOS/Android app for Filipino grocery shopping — create budget-aware checklists, capture items in the cart, compare prices across stores, and learn from a community forum. Phase 2 adds a NestJS backend (`e-kart-service`) with MongoDB so checklists, forum, profile, analytics, and AI generation persist per user.

## Screens

- Onboarding (3 slides)
- Login & register
- **Home** — shopping analytics, active checklist, quick actions, store promos (API-backed when online)
- **Checklist** — master lists, items, camera capture, budget, share by email
- **Catalog** — multi-store price search *(mock data; backend TBD)*
- **Forum** — Reddit-style feed, votes, comments, subforums, media
- **Profile** — alias, activity, forum history, account forms
- **Settings** — language (EN / FIL), theme (light / dark / system)

## Features

- JWT auth with session restore (register, login, logout)
- Checklist CRUD, share by email, presigned image upload
- AI generate checklist (mock / OpenAI / Anthropic providers on backend)
- Forum posts, comments, votes, join/leave subforums
- Home analytics & promos from API
- Camera OCR for price capture *(mock on client; real OCR TBD)*
- Alias-based forum identity
- Bilingual UI and theme persistence synced to API

## Tech stack

### Frontend (`e-kart-app`)

- Expo SDK 54 · React Native · TypeScript
- Expo Router · Gluestack UI · Zustand
- MVVM — `app/` views, `viewmodels/`, `stores/`, `services/api/`

### Backend (`e-kart-service`)

- NestJS 11 · MongoDB (Mongoose)
- JWT authentication · Passport
- OpenAPI / Swagger at `/api/docs`
- Modules: auth, users, preferences, checklists, generate (AI), forum, analytics, promos, health
- 30+ e2e API tests

### Integration

- `EXPO_PUBLIC_NESTJS_API_URL` enables all `USE_API.*` flags in `constants/config.ts`
- API clients: auth, user, checklist, forum, analytics, promo
- Catalog and OCR remain mock-only by design (spec 20)

## Architecture

- MVVM on the client; modular NestJS on the server
- Spec-driven development (20 specs: 01–11 frontend, 13–20 backend + integration)
- No over-engineering — mock services swap to API clients per domain via feature flags

## Project status

| Phase | Scope | Status |
| ----- | ----- | ------ |
| Phase 1 | Expo frontend, mock services | Complete (specs 01–11) |
| Phase 2 | NestJS API + app integration | Complete (specs 13–20) |
| Future | Production deploy, real OCR, catalog backend | Planned |
