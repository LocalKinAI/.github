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
│        │  kinclaw-mac v0.4.1  (SwiftUI)   │                  │
│        │  Chat ┊ Cowork ┊ Code            │                  │
│        └────────┬───────────┬─────────────┘                  │
└─────────────────┼───────────┼────────────────────────────────┘
                  │           │
        ┌─────────▼──┐  ┌─────▼──────┐
        │ :5001      │  │ :5002      │
        │ kinclaw    │  │ kincode    │   LAYER 2 — kernels
        │ v1.15.0    │  │ v0.10.0    │   (Apache-2.0 / MIT)
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
| **[kinclaw](https://github.com/LocalKinAI/kinclaw)** | macOS computer-use agent — 5 claws + floating chat UI + voice. Agent operates your real Mac. **67.3% on macbench v0.1** (first reference run, 2026-05-08). | Apache-2.0 · v1.15.0 |
| **[kinclaw-mac](https://github.com/LocalKinAI/kinclaw-mac)** | Native macOS Spotlight shell for the kernel family. ⌘⌥K → Chat (98 cloud agents) · Cowork (kinclaw 5 claws) · Code (kincode + repo). | Apache-2.0 · v0.4.1 |
| **[kincode](https://github.com/LocalKinAI/kincode)** | AI coding assistant, 10MB single binary. HTTP+SSE server mode for desktop shells. | MIT · v0.10.0 |
| **[macbench](https://github.com/LocalKinAI/macbench)** | **First publicly published macOS-native computer-use benchmark.** 369 task slots, 15 categories, agent-agnostic Go runner. Inspired by OSWorld; adapted for the macOS app surface OSWorld can't reach. | MIT · v0.1.0 |

### KinKit — pure-Go macOS bindings (zero cgo, embedded dylib, `go install`-able)

The libraries that power 4 of KinClaw's 5 claws. Each is independently usable in any Go project that needs to drive macOS at the framework level — no Xcode, no cgo, no Swift bridge.

| Library | Description | |
|---------|-------------|-|
| **[sckit-go](https://github.com/LocalKinAI/sckit-go)** | ScreenCaptureKit bindings · sub-20ms streams · powers `screen` claw | MIT |
| **[kinax-go](https://github.com/LocalKinAI/kinax-go)** | Accessibility API bindings · navigate UI trees via AXUIElement · powers `ui` claw | MIT |
| **[input-go](https://github.com/LocalKinAI/input-go)** | CGEvent mouse + keyboard synthesis · `target_pid` background mode · powers `input` claw | MIT |
| **[kinrec](https://github.com/LocalKinAI/kinrec)** | Screen + audio recorder · built on sckit-go · powers `record` claw | MIT |

See the [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib) paper for the distribution pattern these all share.

### The 5th claw — `web` (3-tier, cost-aware)

The other 4 claws are macOS-bound. The web claw is **cross-platform** and arguably the most-used in real flows, because most modern productivity lives in browser tabs — Gmail, Linear, Notion, GitHub, Booking, Airbnb, Google Flights, the LocalKin family's own apps (`localkin.ai`, `faith.localkin.ai`, `heal.localkin.ai`, `api.localkin.dev`).

KinClaw's web claw is **3 tiers, picked by Pilot based on what the task actually needs** — cheap-and-fast first, expensive-and-flexible only when nothing else works:

#### Tier 0 · URL-first (~50ms, no startup cost)

The most important operational doctrine in `pilot.soul.md` — go straight to result URLs, skip GUI clicking entirely. Covers ~80% of real flows.

| Capability | What it does |
|---|---|
| **`shell open <URL>`** | macOS URL-handler routing — `maps://`, `mailto:`, `music://`, `https://` — land at destination state without any clicking |
| **`web_fetch <URL>`** | Server-side fetch + HTML strip → clean text, no Chromium, no JS render |
| **`web_search`** | DuckDuckGo (default) or [Tavily](https://tavily.com) (when `TAVILY_API_KEY` set) |
| **14 baked-in URL templates** | Google Flights · Kayak · Skyscanner · Booking · Airbnb · Zillow · Maps · Amazon · YouTube · GitHub search · ArXiv · 12306 · Reddit · etc. — canonical patterns in the soul prompt so Pilot knows the deep-link grammar of every popular site |

Why this beats GUI puppeteering for an LLM agent: calendar pickers (clicking "previous month" 30 times to land on July is doomed; `?checkin=2025-07-08` lands instantly), faceted filters (URL params take 4 dimensions atomically), cookie banners + modals (skipped entirely), SPA accessibility gaps (React tree without AX labels — URL bypasses the DOM).

#### Tier 1 · `web` skill (~3s cold start, single-step Playwright)

When URL-first can't reach (page needs JS to render, content lives behind a click, you need a screenshot of the rendered DOM), Pilot drops to the `web` skill — a Playwright-driven single-shot.

```
web url=X
web url=X click=".btn" type_text="hello"
web url=X js="document.body.innerText"
web url=X screenshot=true
```

One call = one Playwright session, ~3s cold start, returns immediately. For 99% of one-off web tasks: scrape a page, run a snippet of JS, fill+submit a form, grab a screenshot.

#### Tier 2 · `browser_session` super-skill (~10-20s warmup, multi-step)

For genuinely complex flows — login + navigate + extract, fill + submit + verify, search + sort + dig three pages deep — KinClaw wraps [**browser-use**](https://github.com/browser-use/browser-use) (the 91K★ OSS that is the de-facto LLM-driven browser agent library) as a single-argument super-skill:

```
browser_session task="登录 GitHub 找我未读 PR"
browser_session task="去 weather.com 输 zip code 95014 拿一周预报表"
browser_session task="open my Linear, find tickets assigned to me this week, summarize"
```

What you get under the hood:
- **Persistent session** — login state, cookies, localStorage all survive across steps
- **DOM element numbering** — browser-use auto-numbers every interactive element so the LLM can refer to "click element 17" instead of fragile CSS selectors
- **Visual reasoning** — screenshot + numbered elements fed back to the planning LLM each step
- **Cross-page flows** — natural to chain login → navigate → extract; the inner LLM plans steps, you just give it the goal

**Trigger rule** (from `pilot.soul.md`): the task description has 2+ interaction verbs (login + navigate + extract / fill + submit + verify / search + sort + dig).

| Task | Tier picked |
|---|---|
| "查 hacker news 头条" | `web_fetch` (Tier 0) |
| "抓 example.com 的 H1" | `web` (Tier 1) |
| "登录 github 找我未读 PR" | `browser_session` (Tier 2 — login is the multi-step signal) |
| "去 weather.com 输 zip code 拿一周预报" | `browser_session` (Tier 2 — multi-step interaction) |

**Cost-aware**: `browser_session` burns LLM tokens per planning step (~$0.05–0.15 Claude per 5-step task). Pilot's soul says explicitly: **don't reach for `browser_session` when `web` would do**. The tier system isn't just capability — it's economics.

#### Strategic angle

Most LocalKin's own products **are** web — Selah, Heal, Morning Manna, the 98-agent chat hub. When Pilot drives a LocalKin user flow, the web claw is doing the lift. All three tiers are **cross-platform** (shell + Node.js, no macOS framework dependencies) — future [`kinclaw-pal`](https://github.com/LocalKinAI/kinclaw-mac/blob/main/CHANGELOG.md) (Linux/Windows shell) inherits the whole web stack with zero rewrite. Only the 4 macOS-bound claws need platform-specific rebinding. **The web tier is what makes the Linux/Win story viable.**

## Public benchmarks

### [macbench](https://github.com/LocalKinAI/macbench) — first publicly published macOS-native computer-use benchmark

```
First reference run (2026-05-08):
  kinclaw v1.15.0 + Kimi-K2.5(cloud) on macbench v0.1
    IMPLEMENTED:  101 / 150  =  67.3%
    STRICT:       101 / 369  =  27.4%   (stubs count as fail)
```

For context, [Anthropic Computer Use](https://www.anthropic.com/news/3-5-models-and-computer-use) scores **~38%** on [OSWorld](https://os-world.github.io) (Linux desktop). macbench measures a different surface (macOS native), so the numbers aren't directly comparable, but the methodology + scoring discipline are the same.

[`xlang-ai/OSWorld`](https://github.com/xlang-ai/OSWorld) (NeurIPS 2024) became the de-facto standard for desktop computer-use agents — but it benchmarks inside an Ubuntu/Windows VM. Nobody had published a comparable benchmark for macOS native apps. macbench fills that gap with **369 task slots** across 15 macOS app categories (Finder · Safari · Mail · Notes · Calendar · Reminders · Settings · Terminal · Pages · Numbers · Keynote · Music · Photos · Maps · multi-app), an **agent-agnostic Go runner** (any binary that takes a prompt + drives macOS plugs in via `-agent` + `-agent-args` template), and **per-task PID-snapshot isolation** that preserves any pre-existing user app state.

v0.1 ships 150 implemented + 219 stubs (real prompts, no setup/eval scripts yet); fill rate over v0.2 → v1.0 is roughly 30-50 stubs/month. License MIT.

## Domains

**75+ specialized agents** across expert traditions, each grounded in real source texts:

- **Spiritual** · 44 masters spanning 19 centuries → [faith.localkin.ai](https://faith.localkin.ai) (Augustine, John Chrysostom, Brother Lawrence, Spurgeon, 倪柝声, 钟马田 …)
- **Traditional Chinese Medicine** · 39 masters spanning 4,500 years → [heal.localkin.ai](https://heal.localkin.ai) (黄帝 → 当代国医大师, 498 books / 159 MB corpus)
- More domains in active development — engineering, quant finance, education, language tutoring, design, game dev, spatial computing, and growing.

## Research Papers

All 10 papers are on Zenodo with permanent DOIs (CC-BY-4.0) and
mirrored bilingually (EN+中文) at [localkin.dev/papers](https://www.localkin.dev/papers).

| # | Title | DOI |
|---|---|---|
| 1 | [Self-Evolving Swarms](https://www.localkin.dev/papers/self-evolving-swarms) | [10.5281/zenodo.20094224](https://doi.org/10.5281/zenodo.20094224) |
| 2 | [Zero-Token Heartbeat](https://www.localkin.dev/papers/heart-zero-token) | [10.5281/zenodo.20094226](https://doi.org/10.5281/zenodo.20094226) |
| 3 | [Genesis Protocol](https://www.localkin.dev/papers/genesis-protocol) | [10.5281/zenodo.20094231](https://doi.org/10.5281/zenodo.20094231) |
| 4 | [Grep Is All You Need](https://www.localkin.dev/papers/grep-is-all-you-need) · [code](https://github.com/LocalKinAI/grep-is-all-you-need) | [10.5281/zenodo.19777260](https://doi.org/10.5281/zenodo.19777260) |
| 5 | [Thin Soul, Fat Skill](https://www.localkin.dev/papers/thin-soul-fat-skill) | [10.5281/zenodo.20094233](https://doi.org/10.5281/zenodo.20094233) |
| 6 | [Domain Expert Debate](https://www.localkin.dev/papers/domain-expert-debate) | [10.5281/zenodo.20094237](https://doi.org/10.5281/zenodo.20094237) |
| 7 | [Knowledge Compile](https://www.localkin.dev/papers/knowledge-compile) | [10.5281/zenodo.20094239](https://doi.org/10.5281/zenodo.20094239) |
| 8 | [Autonomous Swarm Genesis](https://www.localkin.dev/papers/autonomous-swarm-genesis) | [10.5281/zenodo.20094241](https://doi.org/10.5281/zenodo.20094241) |
| 9 | [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib) · [code](https://github.com/LocalKinAI/sckit-go) | [10.5281/zenodo.20094243](https://doi.org/10.5281/zenodo.20094243) |
| 10 | [macbench](https://www.localkin.dev/papers/macbench) · [code](https://github.com/LocalKinAI/macbench) | [10.5281/zenodo.20094245](https://doi.org/10.5281/zenodo.20094245) |

## Contact

📧 contact@localkin.ai
