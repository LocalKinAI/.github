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
| **[localkin](https://github.com/LocalKinAI/localkin)** | AI agent runtime — single binary, soul-file configured | Apache-2.0 |
| **[kin-code](https://github.com/LocalKinAI/kin-code)** | AI coding assistant, 9MB single binary | MIT |

## Domains

Spiritual (8 masters) · Traditional Chinese Medicine (11 physicians) · Engineering · Quantitative Finance · Marketing · Product · Design · Game Dev · Spatial Computing · and more.

## Research Papers

- [Self-Evolving Swarms](https://www.localkin.dev/papers/self-evolving-swarms)
- [Zero-Token Heartbeat](https://www.localkin.dev/papers/heart-zero-token)
- [Genesis Protocol](https://www.localkin.dev/papers/genesis-protocol)
- [Thin Soul, Fat Skill](https://www.localkin.dev/papers/thin-soul-fat-skill)
- [Domain Expert Debate](https://www.localkin.dev/papers/domain-expert-debate)
- [Grep Is All You Need](https://www.localkin.dev/papers/grep-is-all-you-need)

## Contact

📧 contact@localkin.ai
