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

| Project | Description | |
|---------|-------------|-|
| **[ollamadiffuser](https://github.com/LocalKinAI/ollamadiffuser)** | Local AI image generation, zero cloud dependency | [![Downloads](https://static.pepy.tech/badge/ollamadiffuser)](https://pepy.tech/projects/ollamadiffuser?timeRange=threeMonths&category=version&includeCIDownloads=true&granularity=daily&viewType=line&versions=Total%2C2.*%2C1.*) |
| **[localkin-service-audio](https://github.com/LocalKinAI/localkin-service-audio)** | High-performance local STT & TTS services | [![Downloads](https://static.pepy.tech/badge/localkin-service-audio)](https://pepy.tech/projects/localkin-service-audio?timeRange=threeMonths&category=version&includeCIDownloads=true&granularity=daily&viewType=line&versions=Total%2C2.*%2C1.*) |
| **[kinclaw](https://github.com/LocalKinAI/kinclaw)** | macOS computer-use agent — 5 claws + floating chat UI + voice. Agent operates your real Mac. | MIT · v1.8.0 |
| **[kin-code](https://github.com/LocalKinAI/kin-code)** | AI coding assistant, 9MB single binary | MIT |

### KinKit — pure-Go macOS bindings (zero cgo, embedded dylib, `go install`-able)

The libraries that power KinClaw's claws. Each is independently usable in any Go project that needs to drive macOS at the framework level — no Xcode, no cgo, no Swift bridge.

| Library | Description | |
|---------|-------------|-|
| **[sckit-go](https://github.com/LocalKinAI/sckit-go)** | ScreenCaptureKit bindings · sub-20ms streams · powers `screen` claw | MIT |
| **[kinax-go](https://github.com/LocalKinAI/kinax-go)** | Accessibility API bindings · navigate UI trees via AXUIElement · powers `ui` claw | MIT |
| **[input-go](https://github.com/LocalKinAI/input-go)** | CGEvent mouse + keyboard synthesis · `target_pid` background mode · powers `input` claw | MIT |
| **[kinrec](https://github.com/LocalKinAI/kinrec)** | Screen + audio recorder · built on sckit-go · powers `record` claw | MIT |

See the [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib) paper for the distribution pattern these all share.

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
