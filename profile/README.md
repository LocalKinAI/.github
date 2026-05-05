<div align="center">
  <h1>LocalKin — Private AI Agent Swarm on Your Machine</h1>
  <p>75+ specialized AI agents running on a single Mac Mini. Self-evolving. Zero cloud dependency.</p>
  <p>
    <a href="https://www.localkin.ai"><b>localkin.ai</b> · apps</a> · 
    <a href="https://api.localkin.dev"><b>api.localkin.dev</b> · chat</a> · 
    <a href="https://www.localkin.dev"><b>localkin.dev</b> · for developers</a>
  </p>
  <p>
    <a href="https://www.localkin.dev/papers">papers</a> · 
    <a href="https://youtube.com/@localkinai">YouTube</a> · 
    <a href="https://discord.gg/w8KGyBpc">Discord</a> · 
    <a href="https://x.com/LocalKinAI">𝕏 @LocalKinAI</a>
  </p>
</div>

---

## Surfaces

### [localkin.ai](https://www.localkin.ai) — knowledge-grounded apps

Direct chat with AI distilled from real human writings. Every answer grounded in actual source texts under enforced retrieval — zero hallucination. Three standalone properties:

- **[清晨甘露 · Morning Manna](https://www.localkin.ai)** — daily devotional reading + audio. Offline + background playback, lock-screen control, resumable across episodes.
- **[细拉 · Selah](https://faith.localkin.ai)** — converse with **44 spiritual masters** spanning 19 centuries (Augustine, John Chrysostom, Brother Lawrence, Spurgeon, 倪柝声, 钟马田 …). Every reply cites the source work + page.
- **[岐黄 · Yellow Emperor's Way](https://heal.localkin.ai)** — converse with **39 TCM masters** spanning 4,500 years (黄帝 → 当代国医大师). 498 books, 159 MB corpus, enforced citation.

### [api.localkin.dev](https://api.localkin.dev) — multi-agent chat hub

Specialist conversational agents — language tutoring, citizenship prep, spiritual companion, TCM diagnosis. 7-day free trial, [Pro upgrade](https://localkin.dev/pricing) for continued use.

- 🕊️ **Madame Guyon** — spiritual companion & inner way guide
- 🎓 **English Tutor** — 100 real-life scenarios + pronunciation coach
- 🏥 **TCM Master** — classical diagnosis across 12 master physicians
- 🇺🇸 **Citizenship Coach** — 128 USCIS questions, bilingual
- 🇨🇳 **Chinese Tutor** — ABC kids edition · 25 scenarios + quiz
- 🇪🇸 **Spanish Tutor** — fun bilingual Spanish for kids

### [localkin.dev](https://www.localkin.dev) — open source for developers

The agent runtime that powers everything above, plus the open-source ecosystem and research papers documenting how it all works. Single 23 MB binary, zero cloud dependency, soul-file configured. See **Core Innovations** + **Ecosystem** below for the technical surface.

---

## What is LocalKin

LocalKin is a Go-based AI agent runtime that orchestrates 75+ domain-expert agents through structured multi-round debates, autonomous scheduling, and self-improvement cycles — all from a single 23MB binary.

## Core Innovations

**Thin Soul + Fat Skill** — Agent identity in 30-line YAML soul files. Skill logic runs as subprocesses, never sent to the LLM. Token-efficient and injection-resistant.

**Zero-Token Heartbeat** — Tri-chamber autonomous scheduling (pulse / schedule / idle) coordinates 75+ agents via MQTT without burning tokens. Agents wake on schedule, catch up after restarts, and roll back silent wakeups with zero memory pollution.

**Conductor-Driven Swarm Debates** — Domain experts debate independently, then update positions after seeing others' arguments. Consensus inertia detection prevents false agreement. Cascade amplification guards catch herding behavior.

**Self-Evolving Architecture** — SAGE four-step improvement loop (Challenger → Planner → Solver → Critic) with experiential reflective learning. 29+ autonomous improvement cycles, 68+ auto-fixes.

**Genesis Protocol** — Bare binary + soul file self-bootstraps: hardware probing → skill forging → self-testing → checkpoint resume.

## Ecosystem

The KinClaw family fits in 4 layers — apps on top, raw macOS bindings at the bottom, kernels in the middle, and a single Mac shell binding it all together. **Same SSE event protocol + same `.soul.md` format across every kernel** — one client codebase drives the whole stack, future Linux/Windows shells reuse it without changes.

```
┌───────────────────────────────────────────────────────────────┐
│  LAYER 4 — apps + chat hub                                     │
│  localkin.ai (Selah · Heal · Manna)   api.localkin.dev (98)   │
└──────────────────────────┬────────────────────────────────────┘
                           │
┌──────────────────────────▼────────────────────────────────────┐
│  LAYER 3 — desktop shell  (Apache-2.0)                         │
│                                                               │
│   ⌘⌥K  ┌──────────────────────────────────┐                  │
│        │  kinclaw-mac v0.2.0  (SwiftUI)   │                  │
│        │  Chat ┊ Cowork ┊ Code            │                  │
│        └────────┬───────────┬─────────────┘                  │
└─────────────────┼───────────┼────────────────────────────────┘
                  │           │
        ┌─────────▼──┐  ┌─────▼──────┐
        │ :5001      │  │ :5002      │
        │ kinclaw    │  │ kincode    │   LAYER 2 — kernels
        │ v1.11.0    │  │ v0.7.1     │   (Apache-2.0 / MIT)
        │ 5 claws    │  │ 10 tools   │
        └────────┬───┘  └────────────┘
                 │
┌────────────────▼──────────────────────────────────────────────┐
│  LAYER 1 — Pure-Go macOS bindings  (KinKit, MIT)               │
│  sckit-go · kinax-go · input-go · kinrec                      │
└───────────────────────────────────────────────────────────────┘
```

**Repos:**

| Project | Description | |
|---------|-------------|-|
| **[ollamadiffuser](https://github.com/LocalKinAI/ollamadiffuser)** | Local AI image generation, zero cloud dependency | [![Downloads](https://static.pepy.tech/badge/ollamadiffuser)](https://pepy.tech/projects/ollamadiffuser?timeRange=threeMonths&category=version&includeCIDownloads=true&granularity=daily&viewType=line&versions=Total%2C2.*%2C1.*) |
| **[localkin-service-audio](https://github.com/LocalKinAI/localkin-service-audio)** | High-performance local STT & TTS services | [![Downloads](https://static.pepy.tech/badge/localkin-service-audio)](https://pepy.tech/projects/localkin-service-audio?timeRange=threeMonths&category=version&includeCIDownloads=true&granularity=daily&viewType=line&versions=Total%2C2.*%2C1.*) |
| **[kinclaw](https://github.com/LocalKinAI/kinclaw)** | macOS computer-use agent — 5 claws + floating chat UI + voice. Agent operates your real Mac. | Apache-2.0 · v1.11.0 |
| **[kinclaw-mac](https://github.com/LocalKinAI/kinclaw-mac)** | Native macOS Spotlight shell for the kernel family. ⌘⌥K → Chat (98 cloud agents) · Cowork (kinclaw 5 claws) · Code (kincode + repo). | Apache-2.0 · v0.2.0 |
| **[kincode](https://github.com/LocalKinAI/kincode)** | AI coding assistant, 10MB single binary. HTTP+SSE server mode for desktop shells. | MIT · v0.7.1 |

### KinKit — pure-Go macOS bindings (zero cgo, embedded dylib, `go install`-able)

The libraries that power 4 of KinClaw's 5 claws. Each is independently usable in any Go project that needs to drive macOS at the framework level — no Xcode, no cgo, no Swift bridge.

| Library | Description | |
|---------|-------------|-|
| **[sckit-go](https://github.com/LocalKinAI/sckit-go)** | ScreenCaptureKit bindings · sub-20ms streams · powers `screen` claw | MIT |
| **[kinax-go](https://github.com/LocalKinAI/kinax-go)** | Accessibility API bindings · navigate UI trees via AXUIElement · powers `ui` claw | MIT |
| **[input-go](https://github.com/LocalKinAI/input-go)** | CGEvent mouse + keyboard synthesis · `target_pid` background mode · powers `input` claw | MIT |
| **[kinrec](https://github.com/LocalKinAI/kinrec)** | Screen + audio recorder · built on sckit-go · powers `record` claw | MIT |

See the [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib) paper for the distribution pattern these all share.

### The 5th claw — `web` (URL-first + Playwright fallback)

The other 4 claws are macOS-bound. The web claw is **cross-platform** and arguably the most-used in real flows, because most modern productivity lives in browser tabs — Gmail, Linear, Notion, GitHub, Booking, Airbnb, Google Flights, the LocalKin family's own apps (`localkin.ai`, `faith.localkin.ai`, `heal.localkin.ai`, `api.localkin.dev`).

KinClaw's web claw runs in **two tiers**, picked by the agent based on what the task actually needs.

#### Tier 1 · URL-first (default, ~80% of flows)

Pilot's `pilot.soul.md` ships this as **the most important operational doctrine**:

> Tasks like "open X to state Y" — **think URL first**. One shell line or one web fetch beats clicking through a calendar picker / cookie banner / React SPA.

| Capability | What it does |
|---|---|
| **`shell open <URL>`** | macOS URL-handler routing — `maps://`, `mailto:`, `music://`, `https://` — land at destination state without UI clicking |
| **`web_fetch <URL>`** | Server-side fetch + HTML strip → clean text. No Chromium, no JS render, ~50ms |
| **`web_search`** | DuckDuckGo (default) or [Tavily](https://tavily.com) (when `TAVILY_API_KEY` set) |
| **14 baked-in URL templates** | Google Flights · Kayak · Skyscanner · Booking · Airbnb · Zillow · Maps · Amazon · YouTube · GitHub search · ArXiv · 12306 · Reddit · etc. — canonical patterns hardcoded into the soul prompt |

Why URL-first beats GUI puppeteering for an LLM agent:

- **Calendar pickers** — clicking "previous month" 30 times to land on July is doomed. `?checkin=2025-07-08` lands instantly.
- **Faceted filters** — Google Flights has roundtrip / cabin / passengers / time-of-day. URL params take all 4 atomically.
- **Cookie banners + modals** — URL → result page skips them entirely.
- **Modern SPA accessibility gaps** — React trees often have no AX labels. URL params bypass the whole DOM.

#### Tier 2 · `web_browser` skill — Playwright when URL-first isn't enough

For the ~20% of flows that genuinely need a real browser (auth-walled pages, JS-rendered content with no URL params, screenshot-of-rendered-DOM, "wait for X to appear"), KinClaw forges a [Playwright](https://playwright.dev) skill on demand and parks it under `~/.localkin/skills/web_browser/`. Invoked via the `spawn` skill or by Pilot directly.

```
web_browser <url> [--screenshot] [--wait N] [--selector CSS] [--text]
```

What it ships:

- **Headless Chromium** (Playwright launches its own, not your system browser — no profile / cookie cross-contamination)
- **Full-page screenshot** to disk → kinclaw's `/file` endpoint → renderable in any UI
- **CSS selector extraction** — `--selector "h1.title" --text` returns clean innerText
- **Page-text extraction** — script/style stripped, `<body>.innerText` saved to disk for follow-up reads
- **Redirect tracking** — final URL reported so the agent knows it landed where it asked

This is also a clean example of the **Genesis / forge pattern**: kinclaw's binary stays small (17 MB, no embedded Chromium), heavy capabilities are forged at runtime as `~/.localkin/skills/<name>/` directories with their own `package.json` + dependencies. Update Playwright? `npm install` in the skill's dir, no kernel rebuild.

#### Strategic angle

Most LocalKin's own products **are** web — Selah, Heal, Morning Manna, the 98-agent chat hub. When Pilot drives a LocalKin user flow, the web claw is doing the lift. Future [`kinclaw-pal`](https://github.com/LocalKinAI/kinclaw-mac/blob/main/CHANGELOG.md) (Linux/Windows shell) inherits **both tiers** with zero rewrite — only the 4 macOS claws need platform-specific rebinding. URL-first is shell-only (cross-platform); Playwright is Node.js (cross-platform). The web tier is what makes the Linux/Win story viable.

## Domains

**75+ specialized agents** across expert traditions, each grounded in real source texts:

- **Spiritual** · 44 masters spanning 19 centuries → [faith.localkin.ai](https://faith.localkin.ai) (Augustine, John Chrysostom, Brother Lawrence, Spurgeon, 倪柝声, 钟马田 …)
- **Traditional Chinese Medicine** · 39 masters spanning 4,500 years → [heal.localkin.ai](https://heal.localkin.ai) (黄帝 → 当代国医大师, 498 books / 159 MB corpus)
- More domains in active development — engineering, quant finance, education, language tutoring, design, game dev, spatial computing, and growing.

## Research Papers

- [Self-Evolving Swarms](https://www.localkin.dev/papers/self-evolving-swarms)
- [Zero-Token Heartbeat](https://www.localkin.dev/papers/heart-zero-token)
- [Genesis Protocol](https://www.localkin.dev/papers/genesis-protocol)
- [Thin Soul, Fat Skill](https://www.localkin.dev/papers/thin-soul-fat-skill)
- [Domain Expert Debate](https://www.localkin.dev/papers/domain-expert-debate)
- [Grep Is All You Need](https://www.localkin.dev/papers/grep-is-all-you-need) · [code](https://github.com/LocalKinAI/grep-is-all-you-need)
- [Knowledge Compile](https://www.localkin.dev/papers/knowledge-compile)
- [Autonomous Swarm Genesis](https://www.localkin.dev/papers/autonomous-swarm-genesis)
- [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib)

## Contact

📧 contact@localkin.ai
