# Random Walk Lab

Personal options & theta decay trading research site — hosted on GitHub Pages.

---

## Project Planning Notes

### Overview

Build a dark-themed, terminal-inspired portfolio website focused on options selling, theta decay strategies, and probability-based trading. The approach follows a tastytrade-style methodology: sell premium, manage risk mechanically, and let theta work. The site should feel like a professional quant lab with a hacker/developer aesthetic.

---

## Site Structure (6 Pages)

### 1. HOME (Landing Page)
- Hero section with animated 3D wireframe sphere / particle mesh background
- Typewriter subtitle: `// THETA DECAY RESEARCH TERMINAL V2.0`
- Brand name: `[ Random Walk ] LAB` in large monospace uppercase
- Tagline: "Options Selling . Theta Strategies . Probability-Based Trading"
- Two CTA buttons: "Explore Research" and "View Tools"
- **Section: What We Do** — overview of the theta-focused approach with animated stat counters (years trading, strategies live, win rate, avg theta/day)
- **Section: Production Trading Systems** — split layout:
  - Left: description of systematic options selling pipeline + bullet features
  - Right: terminal window showing live signals, e.g.:
    ```
    [SIGNAL] IV Rank: 42 on SPY
    [SIGNAL] Sell 30-delta strangle on /ES
    [ENTRY] SHORT PUT 4200 / SHORT CALL 4500 @ $8.40 credit
    [THETA] -$12.30/day | POP: 68%
    [OK] Max loss defined | Buying power: within 5%
    ```
- **Section: Strategy Toolkit** — vertical list with hover: credit spreads, iron condors, strangles, covered calls, calendars, jade lizards, etc.
- **Section: Research & Analysis** — tag pills (IV Analysis, Greeks, Earnings Plays, Sector Volatility), terminal snippet showing vol surface data
- **Section: Marketplace & Collaboration** — icon grid (investor partnerships, premium scanners, custom alerts, coaching)
- **Footer** with terminal system status block

### 2. ABOUT Page
- Hero: "About The Lab"
- Left column text sections:
  - **Trading Philosophy**: sell premium, high probability, mechanical management, small & consistent
  - **Strategy Stack**: short strangles, iron condors, verticals, covered strats, earnings plays, 0DTE scalps
  - **Core Principles** (bullet list): trade small & often, manage at 21 DTE, take profits at 50%, sell in high IV rank, diversify across underlyings & sectors, defined risk for small accounts
- Right column: terminal JSON config:
  ```json
  {
    "alias": "Random Walk Lab",
    "role": "Theta Decay Specialist",
    "strategies": ["Strangles", "Iron Condors", "Verticals", "0DTE"],
    "platforms": ["tastytrade", "ThinkorSwim", "Python", "IBKR"],
    "greeks_focus": ["Theta", "Vega", "Delta-neutral"],
    "status": "ACTIVE — LIVE CAPITAL"
  }
  ```
- Stat counters: years trading, strategies active, avg win rate, instruments tracked
- **Mission section**: terminal markdown block

### 3. RESEARCH Page
- Hero: "Research" with typewriter subtitle
- **Filter tabs**: ALL, IV ANALYSIS, STRATEGY STUDIES, EARNINGS, 0DTE, GREEKS
- **Search bar**
- **Research cards** — each with:
  - Category badge (colored)
  - Date
  - Monospace title (e.g. "IV Rank vs IV Percentile: Which Matters for Premium Sellers")
  - Description
  - Expandable chevron
  - "READ FULL NOTE" or "COMING SOON" button
- Example research topics:
  - Optimal DTE for short strangles (45 vs 30 vs 21)
  - Rolling mechanics: when and how to roll tested sides
  - IV Rank thresholds for entry
  - 0DTE SPX credit spreads: edge or coin flip?
  - Sector rotation and vol clustering
  - Earnings straddle pricing efficiency
  - Delta selection: 16-delta vs 30-delta strangles
  - Correlation risk in a strangle portfolio
  - Backtest: mechanical 50% profit target vs expiration hold
  - VIX regime filters for premium selling

### 4. TOOLS Page
- Hero: "Trading Tools"
- **Interactive demo section** — backtester for options strategies:
  - Left: description + bullet points (historical vol data, strategy selector, PnL curves)
  - Right: embedded chart showing equity curve / PnL of a short strangle backtest
- **Filter tabs**: ALL, SCANNERS, BACKTESTS, CALCULATORS, AUTO SYSTEMS
- **Tool cards**:
  - **IV Rank Scanner** — scans underlyings for high IV rank/percentile, flags opportunities (LIVE)
  - **Options Probability Calculator** — POP, expected move, breakevens for any spread (ACTIVE)
  - **Theta Decay Visualizer** — interactive chart showing theta curve across DTE for different strategies (ACTIVE)
  - **Strangle Backtester** — walk-forward backtest on historical data with mechanical rules (IN DEV)
  - **Earnings Vol Analyzer** — compare implied vs realized move around earnings (IN DEV)
  - **0DTE Dashboard** — real-time gamma exposure, expected move, key strikes for SPX/SPY (IN DEV)
  - **Portfolio Greeks Monitor** — aggregate portfolio theta, delta, vega, gamma in real-time (IN DEV)

### 5. MARKETPLACE Page
- Hero: "Marketplace" with typewriter subtitle
- Terminal status block (preview mode, payment pending, catalog count)
- **Product cards**:
  - **Premium Scanner Pro** — IV rank/percentile scanner with custom alerts ($--)
  - **Theta Portfolio Tracker** — track all positions, greeks, P&L, management alerts ($--)
  - **Strangle Backtest Engine** — full historical backtest suite for premium selling ($--)
  - **0DTE Signal Bot** — automated 0DTE credit spread signals via API ($--)
  - All show "BUY — COMING SOON"

### 6. CONTACT Page
- Hero: "Contact" with typewriter subtitle
- Two-column layout:
  - Left: terminal form (`secure-transmission.sh`) with name, email, message fields + "OPEN GMAIL DRAFT" button
  - Right: connection info panel with email, social links, system-info (response time, timezone, preferred channel)

---

## UI / Visual Design System

### Color Palette
| Role | Color | Usage |
|------|-------|-------|
| Background | `#0a0a0f` / `#0d0d14` | Page bg, dark panels |
| Primary text | `#e0e0e0` / `#c0c0c0` | Body text |
| Accent 1 (Cyan) | `#00e5ff` / `#00bcd4` | Headings, primary buttons, links |
| Accent 2 (Green) | `#00e676` / `#4caf50` | Terminal prompts, profit/live badges |
| Accent 3 (Magenta) | `#e040fb` / `#ce93d8` | Secondary buttons, hover |
| Accent 4 (Yellow) | `#ffd740` | Warnings, "in dev" badges |
| Red | `#ff5252` | Loss indicators, max loss |
| Muted | `#666` / `#888` | Subtitles, metadata |
| Card BG | `#111118` / `#141420` | Cards, terminals, forms |
| Border | `#1a1a2e` / `#00e5ff22` | Card borders, glows |

### Typography
- **Headings**: Monospace uppercase, letter-spacing ~0.15em (`Space Mono`, `JetBrains Mono`, `Fira Code`)
- **Body**: Clean sans-serif (`Inter`, `DM Sans`) or monospace
- **Terminal blocks**: Monospace with syntax highlighting
- **All caps** for nav and section labels

### UI Components

#### Navigation Bar
- Fixed/sticky top
- Brand left: `[ Random Walk ] LAB` — cyan, bracket styling
- Links right: HOME, ABOUT, RESEARCH, TOOLS, MARKETPLACE, CONTACT
- Uppercase monospace, active = cyan underline
- Mobile: hamburger

#### Terminal Window Component
- macOS dots (red/yellow/green) top-left
- Title bar filename
- Dark panel background
- Green `>` prompt
- Syntax-highlighted content
- Blinking cursor `█`

#### Stat Counter Component
- Large animated count-up number
- Small uppercase muted label below
- Horizontal row layout

#### Card Component
- Dark panel, subtle cyan border (1px semi-transparent)
- Hover glow effect
- Category badge/pill
- Status badge (colored dot + label)
- Monospace title, muted description
- Action buttons at bottom

#### Buttons
- Primary: cyan border + text, no fill, monospace uppercase
- Secondary: magenta variant
- Disabled: gray/muted
- Hover: glow or fill transition
- Prefix arrows: `▷ EXPLORE RESEARCH`

#### Filter Tabs
- Horizontal row, icon + label + count badge
- Active: cyan underline + text
- Inactive: muted gray

#### Form Fields
- Dark bg, cyan/green label (monospace, `▷` prefix)
- Muted placeholder, focus = cyan glow border

#### Background Effects
- Animated particles / floating dots
- Faint grid / wireframe mesh
- Radial gradient overlays
- Parallax hero scrolling

#### Footer
- Centered cyan brand name
- Tagline: "Options Research . Theta Strategies . Probability-Based Trading"
- Nav links row

---

## Tech Stack (Planned)

- **Hosting**: GitHub Pages
- **Framework**: Static HTML/CSS/JS (or Next.js)
- **Styling**: Custom CSS variables or Tailwind CSS
- **Fonts**: Google Fonts monospace (JetBrains Mono / Space Mono / Fira Code)
- **Animations**: CSS keyframes (typewriter), AOS (scroll animations), JS counters
- **3D/Particles**: Three.js or particles.js for hero
- **Charts**: Lightweight Charts (TradingView lib) or Chart.js for backtests/equity curves
- **Options Data**: CBOE data, tastytrade API, or IBKR API for vol/greeks
- **Icons**: Lucide, Phosphor, or SVG

---

## Development Phases

### Phase 1 — Scaffolding
- [ ] Set up GitHub Pages deployment
- [ ] Base HTML template with nav + footer
- [ ] CSS variables (colors, fonts, spacing)
- [ ] Terminal window component
- [ ] Card component

### Phase 2 — Core Pages
- [ ] Home page with hero + all sections
- [ ] About page with profile JSON terminal
- [ ] Contact page with form + info panels

### Phase 3 — Content Pages
- [ ] Research page with filter tabs + search + cards
- [ ] Tools page with interactive demo + tool cards
- [ ] Marketplace page with product cards

### Phase 4 — Polish
- [ ] Particle/mesh hero background
- [ ] Typewriter effects
- [ ] Scroll animations (fade in, count up)
- [ ] Mobile responsive
- [ ] SEO + Open Graph

### Phase 5 — Content & Launch
- [ ] Write theta/options research notes
- [ ] Build IV scanner prototype
- [ ] Connect contact form (mailto or Formspree)
- [ ] Cross-browser testing
- [ ] Launch

---

## Detailed UI Design Spec

### Page Layout System

```
+--------------------------------------------------+
| NAV: [ Random Walk ] LAB          HOME ABOUT ... |
+--------------------------------------------------+
|                                                  |
|   HERO SECTION                                   |
|   - Full viewport height                         |
|   - Animated particle/mesh background            |
|   - Centered content: badge > h1 > tagline > CTAs|
|                                                  |
+--------------------------------------------------+
|   SECTION (alternating layout)                   |
|   Left col (text) | Right col (terminal/chart)   |
|   Max-width: 1200px, centered, padding: 80px 0   |
+--------------------------------------------------+
|   FOOTER                                         |
+--------------------------------------------------+
```

### Spacing & Grid
- Container max-width: `1200px`
- Section vertical padding: `80px` top/bottom
- Grid gap: `40px`
- Card padding: `24px`
- Border radius: `4px` (sharp/minimal, quant aesthetic)
- Two-column split: `55% / 45%` or `50% / 50%`

### Hero Section Design
```
+--------------------------------------------------+
|  [particle/mesh canvas — full bleed]             |
|                                                  |
|         // THETA DECAY RESEARCH TERMINAL V2.0    |  <- small badge, bordered box
|                                                  |
|       R A N D O M   W A L K   L A B             |  <- large, spaced, cyan
|                                                  |
|  Options Selling . Theta Strategies . Prob-Based |  <- muted tagline
|                                                  |
|    [ ▷ EXPLORE RESEARCH ]  [ ◆ VIEW TOOLS ]     |  <- outlined buttons
|                                                  |
+--------------------------------------------------+
```
- Badge: `1px solid #00e5ff44`, text `#00e5ff`, padding `6px 16px`, monospace
- H1: font-size `clamp(3rem, 8vw, 7rem)`, letter-spacing `0.2em`, uppercase
- Tagline: muted gray, letter-spacing `0.1em`, font-size `0.9rem`
- CTAs: `1px solid #00e5ff`, padding `12px 28px`, hover = subtle cyan fill at 10% opacity

### Terminal Window Component Design
```
+----------------------------------------+
| ● ● ●   filename.sh              [dark]|
+----------------------------------------+
| > function_name()                      |
| {                                      |
|   "key":  "value",          <- green   |
|   "key2": "value2",                    |
| }                                      |
| > █                         <- cursor  |
+----------------------------------------+
```
- Window bg: `#0d0d14`
- Title bar bg: `#161622`, height `32px`
- Dots: `#ff5f57` (red), `#febc2e` (yellow), `#28c840` (green), size `10px`, gap `6px`
- Title text: `#666`, font-size `0.75rem`, monospace
- Prompt `>`: `#00e676` (green)
- Function calls: `#00bcd4` (cyan)
- String values: `#a5d6a7` (light green)
- Keys/structure: `#e0e0e0` (white)
- Cursor `█`: `#00e676`, CSS `animation: blink 1s step-end infinite`
- Padding: `16px 20px`
- Border: `1px solid #1a1a2e`
- Border-radius: `6px`

### Card Component Design
```
+--------------------------------------------+
| [BADGE: STRATEGY]          [STATUS: LIVE ●]|
|                                            |
| Short Strangle — SPX                       |  <- cyan monospace title
|                                            |
| Sell 16-delta puts and calls at 45 DTE,   |
| manage at 21 DTE or 50% profit target.    |  <- muted description
|                                            |
| PLATFORM: tastytrade  |  DELTA: 16        |  <- metadata row
|                                            |
| [ DETAILS ]  [ NOTIFY ME ]                |  <- action buttons
+--------------------------------------------+
```
- Card bg: `#111118`
- Border: `1px solid #1a1a2e`
- Hover border: `1px solid #00e5ff33` + `box-shadow: 0 0 20px #00e5ff0a`
- Badge: small, `font-size: 0.65rem`, uppercase, colored border
- Status dot: `8px` circle, green = LIVE, cyan = ACTIVE, yellow = IN DEV
- Title: `#00e5ff`, monospace, `font-size: 1.1rem`
- Description: `#888`, `font-size: 0.85rem`, `line-height: 1.6`
- Metadata: `font-size: 0.75rem`, `#555`, uppercase

### Research Filter Tabs Design
```
[ ⬜ ALL  3 ] [ 📈 IV ANALYSIS  2 ] [ 📊 STRATEGY  4 ] [ ⚡ 0DTE  1 ]
             ^
          active tab = cyan underline 2px, cyan text
```
- Tab bg: transparent
- Active: `color: #00e5ff`, `border-bottom: 2px solid #00e5ff`
- Inactive: `color: #555`, hover = `#888`
- Count badge: `background: #1a1a2e`, `color: #888`, `border-radius: 3px`, `padding: 1px 6px`
- Font: monospace, `0.8rem`, uppercase, letter-spacing `0.05em`

### Stat Counter Row Design
```
+----------+  +----------+  +----------+  +----------+
|    68%   |  |    45    |  |   0DTE   |  |   $0.12  |
|  WIN RATE|  |  AVG DTE |  | INCLUDED |  | AVG θ/DAY|
+----------+  +----------+  +----------+  +----------+
```
- Number: `font-size: 2.5rem`, `#00e5ff`, monospace, bold
- Label: `font-size: 0.7rem`, `#555`, uppercase, letter-spacing `0.15em`
- Divider lines between stats: `1px solid #1a1a2e`
- Animation: JS IntersectionObserver triggers count-up when scrolled into view

### Color Glow Effects
- Cyan glow: `box-shadow: 0 0 30px #00e5ff15, 0 0 60px #00e5ff08`
- Green glow (live indicator): `box-shadow: 0 0 8px #00e67644`
- Button hover glow: `box-shadow: 0 0 20px #00e5ff22`
- Section separator: `1px solid #1a1a2e` or gradient fade

### Animation Specs
| Animation | Trigger | Duration | Easing |
|-----------|---------|----------|--------|
| Hero particle mesh | Page load | Continuous | Linear |
| Typewriter subtitle | Page load | 2s | Steps |
| Section fade-in | Scroll into view | 0.6s | ease-out |
| Stat count-up | Scroll into view | 1.5s | ease-out |
| Terminal cursor blink | Always | 1s | step-end |
| Card hover glow | Hover | 0.2s | ease |
| Nav link underline | Hover | 0.15s | ease |
| Button fill | Hover | 0.2s | ease |

### Mobile Breakpoints
- Desktop: `>1024px` — full two-column layouts
- Tablet: `768px–1024px` — stacked columns, reduced font sizes
- Mobile: `<768px` — single column, hamburger nav, touch-friendly cards, smaller hero text

---

## Long-Term Development Roadmap

### Year 1 — Build Foundation (Months 1–6)
**Goal**: Ship a polished static site with core content and tools

#### Q1 (Months 1–3): Site Launch
- [ ] Complete all 6 pages (HTML/CSS/JS)
- [ ] Implement full UI design system (components, colors, typography)
- [ ] Deploy to GitHub Pages with custom domain
- [ ] Write first 3 research notes (IV Rank, Strangle DTE study, 0DTE edge)
- [ ] Build IV Rank Scanner v1 (Python script or JS-based)
- [ ] Build Options Probability Calculator (web-based, pure JS)

#### Q2 (Months 4–6): Tools & Content
- [ ] Theta Decay Visualizer (interactive DTE curve chart)
- [ ] Strangle Backtester v1 (Python, historical data from CBOE/Polygon)
- [ ] Write 5 more research notes (rolling, delta selection, VIX regime, earnings)
- [ ] Integrate Lightweight Charts for equity curve visualization
- [ ] Add email list / newsletter signup (ConvertKit or Beehiiv)
- [ ] First social media presence (Twitter/X, YouTube)

### Year 1 — Growth (Months 7–12)
**Goal**: Monetize tools, grow audience, launch marketplace

#### Q3 (Months 7–9): Monetization Prep
- [ ] Earnings Vol Analyzer tool
- [ ] Portfolio Greeks Monitor (connect to IBKR API or tastytrade API)
- [ ] Launch Marketplace with first paid product (Premium Scanner Pro)
- [ ] Integrate payment system (Stripe or Gumroad)
- [ ] Publish backtesting methodology publicly
- [ ] 0DTE Dashboard v1

#### Q4 (Months 10–12): Scale
- [ ] Theta Portfolio Tracker (full position manager)
- [ ] Strangle Backtest Engine as standalone paid product
- [ ] Launch 0DTE Signal Bot (API-based alerts)
- [ ] Build email community around weekly theta research digest
- [ ] Video content: YouTube / TikTok short-form (tastytrade-style education)
- [ ] Collaboration with other traders / quant creators

### Year 2 — Platform Expansion
**Goal**: Become a recognized resource for options/theta traders

#### Features to Build
- [ ] **Live Dashboard**: real-time portfolio greeks, P&L tracker, position manager
- [ ] **Options Chain Scanner**: scan full chains for optimal premium-selling setups
- [ ] **Backtesting SaaS**: web-based, no-code backtest builder for premium sellers
- [ ] **Strategy Builder**: configure strangles, condors, verticals with parameter inputs and instant POP/theta output
- [ ] **Alerting System**: push/email alerts when IV rank spikes above threshold
- [ ] **Community Forum / Discord**: engage theta traders, share research
- [ ] **API Access**: sell programmatic access to scanner and signals
- [ ] **Mobile App**: React Native portfolio tracker + scanner

#### Content Milestones
- [ ] 50+ research notes published
- [ ] Full options education series (beginner to advanced premium selling)
- [ ] Backtest transparency: publish all results with methodology
- [ ] Monthly performance reports

### Year 3+ — Enterprise & Automation
**Goal**: Fully automated theta trading operation + recognized brand

- [ ] Fully automated tastytrade/IBKR execution bot (mechanical strangle/condor system)
- [ ] Portfolio-level risk management engine (delta-neutral rebalancing)
- [ ] Investor dashboard (for external capital / fund structure)
- [ ] White-label tools for other traders/funds
- [ ] Institutional-grade research reports
- [ ] Speaking / consulting in options/quant trading space

---

## Key Metrics to Track

| Metric | Target (Year 1) | Target (Year 2) |
|--------|-----------------|-----------------|
| Site monthly visitors | 1,000 | 10,000 |
| Email subscribers | 500 | 5,000 |
| Research notes published | 10 | 50 |
| Tools shipped | 3 | 8 |
| Marketplace revenue | $500/mo | $5,000/mo |
| Social following (total) | 1,000 | 10,000 |
| Portfolio strategies live | 3 | 6 |
| Win rate (theta book) | >65% | >68% |

---

## Notes & Decisions Log

- **2026-03-12**: Project initialized. Focus: tastytrade-style theta trading, terminal UI aesthetic, GitHub Pages static site
- Framework TBD: leaning toward plain HTML/CSS/JS for speed, may migrate to Next.js if interactivity demands it
- Domain name TBD: `randomwalklab.com` or `randomwalk.trade` — check availability
- Data sources to evaluate: Polygon.io (historical options), CBOE (free vol data), tastytrade API, IBKR API
- Keep site static/fast — no heavy frameworks unless needed for tools
