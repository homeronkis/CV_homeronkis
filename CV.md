# Igor Kim — Senior Frontend Engineer

**Stack:** TypeScript, React 18, Next.js, Vue.js, Nuxt, Electron, Node.js
**Niches:** real-time chat, virtualized lists, FinTech / crypto exchange UIs, AI-driven personal tooling
**Location:** Bishkek, Kyrgyzstan · UTC+6 · remote, ±3 h MSK
**Email:** homeronkis@gmail.com
**LinkedIn:** https://www.linkedin.com/in/igor-kim-45a3b817a/
**Live CV:** https://homeronkis.github.io/CV_homeronkis/
**GitHub:** https://github.com/homeronkis

---

## Summary

Senior Frontend Engineer with 7+ years building real-time, performance-critical interfaces:
chat at scale (Matrix SDK, virtualized lists for 10k+ messages), crypto-exchange UIs, FinTech
dashboards, Electron desktop apps. React / TypeScript today; deep history in Vue / Nuxt.

Currently building a daily-briefing PWA on React 18 / Vite / FastAPI with a pluggable apps
architecture (manifest-declared surfaces, MCP-callable tools, hot mount/unmount, schema-versioned
permissions). Source on GitHub, live at dashboard.heiks.uk.

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

**Languages (human):** Russian (native, interview-ready), English (technical reading & writing fluent, conversational ok).

---

## Experience

### Personal projects · AI-driven tooling — 2024 to present

Building / shipping / iterating.

**Stack:** React 18, TypeScript, Vite, TanStack Query, Framer Motion, FastAPI, Pydantic, Playwright, Vitest, Cloudflare Tunnel.

- Built a daily-briefing PWA from scratch — React 18 / Vite / FastAPI backend, deployed live at dashboard.heiks.uk via Cloudflare Tunnel + Cloudflare Access (Google OAuth gate, no port-forward).
- Designed a pluggable apps architecture: each feature is a self-contained `apps/{slug}/` container (manifest.json + frontend + backend + data scope + permissions). Hot mount/unmount without server restart. Manifest-declared surfaces (UI, REST API, MCP-callable tools) so any app can expose itself to AI agents.
- Wrote a Vite plugin that scans `apps/` at build time and generates the registry + lazy import loaders. New app = drop a folder, push, done.
- AI scoring pipeline for jobs and news: regex pre-filter → Claude Haiku via subprocess for ranking, mood-aware filter rules, emergency fallback pool when LLM is unavailable.
- VAPID Web Push + service worker with offline cache + background pipeline-completion notifier. Debugged a real-world pywebpush 2.x ↔ py_vapid PEM-vs-DER mismatch and shipped the migration in production.
- Test discipline: 438 backend tests at 96% line coverage (every module ≥90%), 26 frontend Vitest unit tests, 19/19 Playwright e2e smoke. Lazy-loaded non-default pages reduce initial bundle ~30%.
- Source: https://github.com/homeronkis. Used daily on iPhone PWA.

### Alandarev — Redux External — Mar 2022 to Aug 2023 · 1 y 5 m

**Senior Frontend Engineer · Remote.**

**Stack:** React, Redux Toolkit, Jest, MongoDB, Electron, virtualized lists.

- Owned the chat module of a Zoom-class corporate communications client.
- Virtualized message lists handle 10k+ messages per thread — instant scroll-to-bottom open, no jank on low-end machines via react-window + intersection observer.
- Detached chat windows via Electron IPC — open any thread in a separate window, drag across monitors, keep state in sync across all windows.
- Attachment pipeline: upload with progress, paste-from-clipboard, image preview, exponential-backoff retry on flaky network.
- Read-receipt batching via Intersection Observer — messages mark as read only when actually visible, batched to one server call per second instead of one per message.
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

- Crypto exchange front-end with real-time order book via WebSocket — order forms, order history with multi-axis filters, exchange-history accordions, live price ticks.
- Owned the client side end-to-end across three surfaces — public landing, transactional demo, internal admin UI.

### BoxExchanger — Mar 2019 to Aug 2020 · 1 y 5 m

**Senior Frontend Engineer · Amsterdam · Remote.**

**Stack:** Vue.js, Nuxt, SCSS.

- Sole frontend for the whole product surface — three apps from scratch:
  marketing site (https://www.boxexchanger.net/en), trading demo, admin panel.
- Crypto-exchange forms with multi-step validation, auth and registration flows, partners directory, search and filter UIs across thousands of items.
- Translated complex finance flows (rate calculations, fee disclosure, AML / KYC steps) into UIs that don't drop users mid-transaction — conversion was the team's primary KPI.

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
- Implemented core product flows for Bazaar — refactored legacy code, removed unused libs, modernised dependencies.
- Browser extension that generated PGP keys for the user's wallet after auth.
- Container backup and snapshot UIs (docker-style snapshots, rendered client-side from raw API data).
- Heavy data-table work — sortable, filterable, resizable, with custom cell renderers.
- 3D globe visualisation via Three.js for the network topology view.

---

## What I do best (signature niches)

- **Real-time chat and messaging.** Matrix SDK, WebSockets, custom virtualization for 10k+ message threads, encryption pipelines (Olm / Megolm), image / file attachments with preview, typing indicators, read-receipt batching.
- **Crypto and FinTech UIs.** Exchange forms, order histories, partner pages with auth, wallet integrations, USDT payments, multi-step KYC flows that don't lose users mid-transaction.
- **Performance work.** Profiling React renders, bundle splitting, virtualized lists (react-window / react-virtualized), intersection-observer-driven lazy loading, network-aware caching.
- **State at scale.** Redux Toolkit, MobX-State-Tree, Zustand, TanStack Query. Picking the right tool for the shape of the data, not the framework of the year.
- **Cross-platform clients.** Electron desktop apps with multi-window IPC, native menus, system tray, file-system integration.

---

## Contact

**Email:** homeronkis@gmail.com
**LinkedIn:** https://www.linkedin.com/in/igor-kim-45a3b817a/
**Live CV (rendered):** https://homeronkis.github.io/CV_homeronkis/
**GitHub:** https://github.com/homeronkis
**Location:** Bishkek, Kyrgyzstan (UTC+6)

Available: remote, full-time, ±3 h MSK timezone. Available now.
