# Hey, I'm Pradeep 👋

**Product Specialist · Frontend Developer · Based in Sydney 🇦🇺**

I build production-ready tools that solve real problems — spec first, then build lean and ship. My background is frontend development; I now work at the intersection of product thinking and engineering, which means I know how to design the right thing *and* direct it being built with precision.

---

## 🧠 How I Work

Every project starts with a detailed spec — data models, UX flows, edge cases, and acceptance criteria — before a single line of code is written. That document is what makes builds fast and outputs reliable. I test with real data, diagnose bugs at root cause, and ship tools I actually use.

---

## 🚀 Projects

### 📈 Alpha Market Engine (AME)
`Python · yfinance · Cloudflare KV · launchd · Claude Code`

A fully automated, private investment intelligence system for ASX + NASDAQ swing trading and long-term investing.

**What it does:**
- **Data pipeline** — fetches live portfolio + technicals (EMA 9/21/50/200, RSI, volume, phase) every morning, evening, and intraday via launchd scheduling
- **Automated email reports** — daily morning signals briefing (pre-market) and EOD report (ASX close), both privacy-safe (public signals only)
- **3-pool ASX market scanner** — RSI Reset, Panic Sell, and Smart Volume pools; HIGH CONVICTION badge when a stock appears in 2+ pools simultaneously
- **Sector-aware overnight context** — maps each holding to its actual US indicator (ITA for defence stocks, GDX for gold miners, URA for uranium, not just generic NASDAQ)
- **AME Dashboard** — live tab in the finance app showing Full Tank net worth, buy signals, market scan, and phase alerts; pushed via Cloudflare KV, auto-refreshes every 5 min
- **Claude Code skills** — `/iw` (investing wizard), `/scan` (morning scan), `/phc` (portfolio health check) — each loads unified pipeline output + strategy framework automatically

**Investment framework:** 4 Market Phases · 7-Rule Entry Checklist · O'Neil Sell Signals · Buffett principles for core positions · Position taxonomy (CORE / TACTICAL / LOTTERY TICKET)

---

### 💰 Personal Finance Tracker
`React 19 · Vite · Tailwind CSS v4 · Recharts · localStorage`  
**[▶ Live Demo](https://personal-finance-tracker-b8a.pages.dev)**

A browser-based financial dashboard built from a 35-page product specification. Fully offline — no backend, no subscriptions, no data leaving your device.

**Five modules:** Net worth dashboard · Income tracking · Investment portfolio · Expense management · Settings

**Notable engineering decisions:**
- **Tranche-based portfolio model** — every purchase is a separate lot with its own cost basis, enabling accurate P&L on partial sells and multiple buy-ins
- **Dual-exchange live pricing** — ASX (.AX suffix, AUD) via Twelve Data + US tickers via Finnhub, with exchange detection and a USD badge when pricing crosses over. CORS-verified with `curl` before writing any code — Alpha Vantage and Yahoo Finance were both disqualified this way
- **Bank statement CSV import** — sign-convention auto-detection (ANZ Amex exports purchases as positive, opposite to standard). 17-category Australian merchant ruleset covering Woolworths, Coles, Chemist Warehouse, Telstra, Netflix, and more. 80%+ auto-categorisation rate on real ANZ data
- **AME Dashboard tab** — live investment intelligence view integrated with the Alpha Market Engine pipeline

---

### 🍽️ Café POS — WINGHOUSE Point of Sale
`Vue 3 · Pinia · Firebase Firestore · Dexie.js · Vite · Cloudflare Pages`  
**[▶ Live App](https://wh-pos.pages.dev)**

A fully functional, cloud-synced POS built for a real restaurant. Multi-device live sync — counter tablet, kitchen monitor, and manager's iPad all stay in sync via Firestore `onSnapshot()`. No server to manage. No monthly SaaS fee.

**Key capabilities:**
- **QR self-ordering** — customers scan a table-specific QR code and order from their phone; "Order More" appends to the same Firestore order, triggering a 🔔 badge on the kitchen dashboard
- **Multi-cart (3 slots)** — independent cart slots with item-count badges; auto-switches to the next active cart after an order is placed
- **KOT + bill printing** — opens native browser print dialog, works with USB/Bluetooth receipt printers; addendum print shows only newly added items
- **Live dashboard** — elapsed time indicators (white / orange / red blinking), inline order editing, hot sellers panel with last-30-day rankings
- **Admin module** — menu management, sales reports with CSV export, expense tracker, per-item revenue breakdown, monthly analytics, employee register, backup/restore
- **Data split by purpose** — orders and settings in Firestore (cross-device, real-time); expenses, employees, and image cache in IndexedDB/Dexie (device-local, fast)

---

## 🛠️ Tech Stack

| Layer | Technologies |
|---|---|
| **Frontend** | Vue 3 (Composition API), React 19, Tailwind CSS v4 |
| **State** | Pinia, React hooks + localStorage |
| **Cloud / Realtime** | Firebase Firestore, Cloudflare Pages, Cloudflare KV |
| **Data & Charts** | ApexCharts, Recharts, yfinance |
| **Build & DevOps** | Vite, GitHub Actions, launchd (macOS) |
| **Backend / Scripting** | Python (data pipelines, email automation) |
| **Local Storage** | Dexie.js / IndexedDB |

---

## 📊 GitHub Stats

![GitHub Stats](https://github-readme-stats.vercel.app/api?username=pradeepn556&show_icons=true&theme=dark&hide_border=true)
![Top Languages](https://github-readme-stats.vercel.app/api/top-langs/?username=pradeepn556&layout=compact&theme=dark&hide_border=true)
