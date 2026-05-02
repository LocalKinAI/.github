<div align="center">
  <h1>LocalKin — Private AI Agent Swarm on Your Machine</h1>
  <p>75+ specialized AI agents running on a single Mac Mini. Self-evolving. Zero cloud dependency.</p>
  <p>
    <a href="https://www.localkin.dev">Website</a> · 
    <a href="https://www.localkin.dev/papers">Research Papers</a> · 
    <a href="https://youtube.com/@localkinai">YouTube</a> · 
    <a href="https://discord.gg/w8KGyBpc">Discord</a> · 
    <a href="https://x.com/LocalKinAI">𝕏 @LocalKinAI</a>
  </p>
</div>

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
| **[ollamadiffuser](https://github.com/LocalKinAI/ollamadiffuser)** | Local AI image generation, zero cloud dependency | 20K+ downloads |
| **[localkin-service-audio](https://github.com/LocalKinAI/localkin-service-audio)** | High-performance local STT & TTS services | 10K+ downloads |
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

Spiritual (8 masters) · Traditional Chinese Medicine (11 physicians) · Engineering · Quantitative Finance · Marketing · Product · Design · Game Dev · Spatial Computing · and more.

## Research Papers

- [Self-Evolving Swarms](https://www.localkin.dev/papers/self-evolving-swarms)
- [Zero-Token Heartbeat](https://www.localkin.dev/papers/heart-zero-token)
- [Genesis Protocol](https://www.localkin.dev/papers/genesis-protocol)
- [Thin Soul, Fat Skill](https://www.localkin.dev/papers/thin-soul-fat-skill)
- [Domain Expert Debate](https://www.localkin.dev/papers/domain-expert-debate)
- [Grep Is All You Need](https://www.localkin.dev/papers/grep-is-all-you-need)
- [Knowledge Compile](https://www.localkin.dev/papers/knowledge-compile)
- [Autonomous Swarm Genesis](https://www.localkin.dev/papers/autonomous-swarm-genesis)
- [Embedded Dylib](https://www.localkin.dev/papers/embedded-dylib)

## Contact

📧 contact@localkin.ai
