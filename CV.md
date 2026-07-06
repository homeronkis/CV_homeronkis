# Igor Kim — Senior Frontend Engineer

**Stack:** TypeScript, React 18, Next.js, Vue.js, Nuxt, Electron, Node.js
**Niches:** real-time chat, virtualized lists, FinTech / crypto exchange UIs, AI-driven personal tooling
**Location:** Bishkek, Kyrgyzstan · UTC+6 (MSK+3) · remote
**Email:** homeronkis@gmail.com
**LinkedIn:** https://www.linkedin.com/in/igor-kim-45a3b817a/
**Live CV:** https://homeronkis.github.io/CV_homeronkis/
**GitHub:** https://github.com/homeronkis

---

## Summary

Senior Frontend Engineer with 7+ years. Real-time chat at scale on Matrix SDK (10k+ message
virtualized threads), crypto-exchange UIs in Amsterdam (BoxExchanger, AZARA), Electron desktop
chat (Alandarev), and AI-agent-callable tooling I've been building lately.

Most of the last seven years has been chat and finance: Matrix protocol from scratch at
Pocketnet, virtualized 10k+ message threads in a Zoom-class desktop client at Alandarev, crypto
exchanges in Amsterdam. On most of these I was the sole frontend or the chat lead. I work best
as the only person who owns the client side end to end.

Currently building a daily-briefing PWA on React 18 / Vite / FastAPI. Each feature is a pluggable
app that declares its own surfaces and MCP-callable tools, so an AI agent can act on it the same
way a person does. Apps mount and unmount live, with schema-versioned permissions. 438 backend
tests, 96% coverage.
Source on GitHub, live at dashboard.heiks.uk.

---

## Skills

**Languages:** TypeScript (daily), JavaScript (ES6+), HTML5, CSS3, Python (FastAPI / pydantic for tooling).

**Frameworks:** React 18 (concurrent, Suspense, hooks-deep), Next.js, Vue 2/3, Nuxt, Electron.

**State management:** Redux Toolkit, MobX-State-Tree, Zustand, TanStack Query (React Query), Vuex.

**Real-time / messaging:** WebSockets, Matrix JS SDK + Synapse, Olm/Megolm encryption, virtualized lists (react-window, react-virtualized, custom), Intersection Observer flows, OpenGraph link previews, paste-from-clipboard attachment pipelines.

**Cross-platform:** Electron (multi-window IPC, native menus, file system integration, system tray), PWA (service workers, Web Push VAPID, offline cache, manifest icons, iOS standalone).

**Styling / motion:** Tailwind, SCSS / Less, styled-components, emotion, Framer Motion, CSS variables for theming.

**Testing / build:** Jest, React Testing Library, Vitest, Playwright, Vite, Webpack, Babel, Docker Compose, GitHub Actions.

**Networking / data:** REST, GraphQL (consumer), Axios / Fetch, REST cache strategies, retry/backoff patterns, network-aware loading.

**Adjacent:** Node.js for full-stack, FastAPI / Python for personal tooling, Docker, basic blockchain & E2E encryption.

**AI tooling experience:** integrating Claude / Anthropic API via subprocess, prompt design for ranking pipelines, MCP server contracts, mood-aware filter rules.

**Methodology:** Scrum, Agile, async-friendly remote teams.

**Languages (human):** Russian (native, interview-ready), English (technical: reading, writing, async chat).

---

## Experience

### Heiks — daily-briefing PWA · 2024 to present

**Founder & lead engineer · open-source · Live at dashboard.heiks.uk**

**Stack:** React 18, TypeScript, Vite, TanStack Query, Framer Motion, FastAPI, Pydantic, Playwright, Vitest, Cloudflare Tunnel.

- Pluggable apps architecture: each feature is a self-contained `apps/{slug}/` container whose manifest.json declares three surfaces (UI, REST API, MCP-callable tools), its data scope, and a whitelist of permissions. Apps hot-mount/unmount on toggle without a server restart.
- Built a Vite plugin that scans `apps/` at build time and emits a typed registry with lazy import loaders. Adding a feature is dropping a folder.
- AI scoring pipeline for incoming jobs and news. A regex pre-filter runs first, then Claude Haiku ranks candidates over a subprocess against a structured-JSON contract. Mood-aware rules shape the result, and a fallback pool covers the LLM being unavailable.
- VAPID Web Push + service worker with offline cache and background pipeline-completion notifier. Diagnosed and shipped a fix for a pywebpush 2.x ↔ py_vapid PEM-vs-DER mismatch in production.
- Cloudflare Tunnel + Cloudflare Access (Google OAuth) for zero-port-forward delivery on a residential connection.
- Test discipline: 438 backend tests at 96% line coverage (every module ≥90%), 26 Vitest unit, 19/19 Playwright e2e. Lazy chunks for non-landing pages cut initial bundle ~30%.
- Source: https://github.com/homeronkis.

### Alandarev — Redux External — Mar 2022 to Aug 2023 · 1 y 5 m

**Senior Frontend Engineer · Remote.**

**Stack:** React, Redux Toolkit, Jest, MongoDB, Electron, virtualized lists.

- Owned the chat module of a Zoom-class corporate communications client.
- Virtualized message lists handle 10k+ messages per thread. They open scrolled straight to the bottom and stay smooth on low-end machines, built on react-window and an intersection observer.
- Detached chat windows over Electron IPC: open any thread in a separate window, drag it across monitors, and the state stays in sync across all of them.
- Attachment pipeline: upload with progress, paste-from-clipboard, image preview, exponential-backoff retry on flaky network.
- Read-receipt batching with an Intersection Observer. A message marks as read only when it's actually on screen, and reads are batched into one server call per second instead of one per message.
- Custom context menus on attachments and messages, keyboard shortcuts, polished hover/focus states.

### Pocketnet — Sep 2020 to Nov 2021 · 1 y 3 m

**Senior Frontend Engineer (chat lead) · Remote.**

**Stack:** Vue.js, Matrix JS SDK, Synapse, Olm/Megolm E2E encryption, Docker.

- Built the entire chat product on Matrix protocol from zero. Solo for the first 6 months, then led a two-engineer team for the remaining 9 months.
- Roughly 60% of the Matrix JS SDK surface used; the integration layer is reusable as a library on any future Matrix-based project.
- Direct and group chats, contact management with search across thousands of users, invites, group admin (members, files, images, rename, mute, kick).
- Message types: text, images with inline preview, files with progress / download / preview, URL link previews via OpenGraph, image gallery, reply threads.
- End-to-end encryption: Olm / Megolm key verification, device cross-signing, encrypted attachments.
- Single codebase serves desktop, tablet, mobile.
- Live: https://pocketnet.app/index

### AZARA — Jul 2020 to Apr 2021 · 9 m

**Senior Frontend Engineer · Amsterdam · Remote.**

**Stack:** Vue.js, Nuxt, SCSS, WebSockets.

- Crypto exchange front-end with a real-time order book over WebSocket: order forms, order history with multi-axis filters, exchange-history accordions, and live price ticks.
- Owned the client side end to end across three surfaces: public landing, transactional demo, and internal admin UI.

### BoxExchanger — Mar 2019 to Aug 2020 · 1 y 5 m

**Senior Frontend Engineer · Amsterdam · Remote.**

**Stack:** Vue.js, Nuxt, SCSS.

- Sole frontend for the whole product surface, three apps from scratch:
  marketing site (https://www.boxexchanger.net/en), trading demo, admin panel.
- Crypto-exchange forms with multi-step validation, auth and registration flows, partners directory, search and filter UIs across thousands of items.
- Translated complex finance flows (rate calculations, fee disclosure, AML / KYC steps) into UIs that don't drop users mid-transaction. Conversion was the team's primary KPI.

### NEO DOC — Jul 2021 to Oct 2021 · 4 m

**Frontend Engineer · Tech Lead, MVP · Bishkek.**

**Stack:** Vue.js.

- Took the MVP from spec to release as the sole frontend.
- Calendar / booking UI: date picker, slot availability, validations.
- Order forms with conditional flows and server-side validation feedback.
- Live: https://dev.neodoc.io/

### OptDyn / Subutai — Jun 2018 to Jul 2019 · 1 y 1 m

**Frontend Engineer · Delaware · Remote.**

**Stack:** Angular 1.5, jQuery, DataTables, Three.js.

- Built and shipped the Subutai.io marketing site.
- Implemented core product flows for Bazaar: refactored legacy code, removed unused libs, and modernised dependencies.
- Browser extension that generated PGP keys for the user's wallet after auth.
- Container backup and snapshot UIs (docker-style snapshots, rendered client-side from raw API data).
- Heavy data-table work: sortable, filterable, resizable, with custom cell renderers.
- 3D globe visualisation via Three.js for the network topology view.

---

## Focus areas

- **Real-time chat at scale.** Matrix JS SDK (~60% surface used in production), Olm / Megolm E2E encryption, WebSockets, virtualized 10k+ message threads via react-window + Intersection Observer, paste-from-clipboard attachments, batched read-receipts.
- **Crypto and FinTech UIs.** Exchange forms, real-time order books over WebSocket, multi-step AML/KYC flows that hold conversion KPI as the team's primary metric, wallet and USDT payment integrations.
- **Performance work.** React render profiling, bundle splitting (lazy chunks for non-landing pages, ~30% initial-bundle cut on my dashboard), intersection-observer lazy loading, network-aware caching, virtualization where the data is real-world large.
- **AI-aware frontends.** Plugin architectures where each feature exposes a UI, a REST API, and MCP-callable tools, so a Claude or GPT agent can act on the same surfaces a person uses. I keep the LLM side pragmatic: it runs over a subprocess against a structured-JSON contract, with a fallback pool for when it's down.

---

## Contact

**Email:** homeronkis@gmail.com
**LinkedIn:** https://www.linkedin.com/in/igor-kim-45a3b817a/
**Live CV (rendered):** https://homeronkis.github.io/CV_homeronkis/
**GitHub:** https://github.com/homeronkis
**Location:** Bishkek, Kyrgyzstan (UTC+6)

Available: remote, full-time, UTC+6 (MSK+3). Available now.
