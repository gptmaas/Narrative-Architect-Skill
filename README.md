# Narrative Architect Skill

**English** | [简体中文](README.zh-CN.md)

Turn complex ideas into story-driven communication.

Most drafts fail in the same quiet way: the facts are correct, but nobody feels why they matter.

Narrative Architect Skill helps you find the pressure, conflict, and turn inside complex material — then shape it for the person you actually need to reach. It will not make everyone like your message. It helps the right listener understand why it matters.

## What It Is

This skill builds communication the way stories are built: from stakes and turning points, not bullet points and buzzwords.

It does a few things well:

- **Finds the narrative kernel** — what is at stake, what old assumption is breaking
- **Reads the audience** — what they know, what they fear, where to start
- **Controls rhythm** — when to ground the reader, when to surprise them
- **Keeps factual claims inside the boundary of what is known**

For source-grounded work, factual claims stay tied to known material. If the source has gaps, the output names them instead of filling them with speculation.

## Who It's For

For people who know what they mean, but keep watching others misunderstand it.

Useful for founders preparing a pitch, engineers explaining architecture, BD leads writing outreach that does not sound templated, and writers who want structure without losing their voice.

## Try It

- "Write an article about why disconnected data is more dangerous than missing data."
- "Help me message an expert through a friend's intro. I want to explore collaboration."
- "Explain this technical architecture to someone with no engineering background."
- "Give me a short follow-up after tomorrow's pitch meeting."
- "Not cold outreach. This is through a friend."

## What It Helps You Do

| Task | Example |
| --- | --- |
| Public narrative | Turn a product launch into a story with tension, stakes, and a memorable close |
| One-on-one strategy | Prepare a message to an investor, expert, or partner that moves the relationship forward |
| Expert translation | Explain a technical concept to a different audience without dumbing it down |
| Quick messages | Draft a warm intro, follow-up, or meeting confirmation in a few sentences |
| Personal communication | Draft a personal, romantic, or emotionally sensitive message that stays natural |
| Rewrite recovery | Diagnose why a draft did not land, then reroute instead of surface-polishing |

## How It Works

The skill picks the lightest mode that handles your task. A short message never inflates into a proposal. A correction never gets a surface polish.

| Mode | When to use it |
| --- | --- |
| Quick Message | Short note, WeChat, follow-up |
| One-on-One Strategy | Reaching a person, team, investor, expert, or partner |
| Public Narrative | Article, speech, brand story, social post |
| Expert Translation | Explaining a concept to a different audience |
| Rewrite Recovery | Fixing a draft that did not land |
| Personal Communication | Personal, romantic, friendship, or emotionally sensitive messages |
| Full Narrative | Major pitch, manifesto, keynote, long-form piece |

## Principles

**Story, not selling.**
The goal is not universal appeal. It is strong resonance with the right listener.

**Controlled surprise.**
Good communication moves between "I understand this" and "I did not see it that way before." Predictable is boring. Chaotic is unreadable. This skill manages that rhythm.

**Audience-first, authority-preserved.**
The audience determines entry point and pace. Your central judgment does not change.

**Claim boundary.**
For source-grounded work, factual claims stay tied to known material. If the source has gaps, the output names them instead of filling them with speculation.

## Installation

Clone the repository:

```bash
git clone https://github.com/gptmaas/Narrative-Architect-Skill.git
```

A typical local setup is to place the skill directory under `skills/` in your OpenClaw workspace:

```
skills/narrative_architect_skill/
```

Requirements depend on your OpenClaw runtime and model provider configuration.

## Project Structure

A simplified layout of the repository:

```
Narrative-Architect-Skill/
├── LICENSE
└── narrative_architect_skill/
    ├── skill.md              # Rules and principles
    ├── runtime_chain.md      # Runtime chain and modes
    ├── mappers/              # Story structure, audience, entropy
    ├── principles/           # Core storytelling principles
    ├── selectors/            # Runtime mode and entry point selection
    ├── renderers/            # Renderer and style wrappers
    ├── harness/              # Quality and validation checks
    ├── contracts/            # Output format contracts
    ├── policies/             # Behavioral policies
    └── cases/                # Regression tests
```

## Status

Prototype.

Core architecture is implemented. Field testing and tuning are ongoing.

## Contributing

Narrative Architect Skill improves with more audience profiles, output contracts, language patterns, style wrappers, and regression cases.

To contribute:

1. Fork the repository
2. Add or improve a mapper, harness, contract, policy, renderer, or case
3. Open a pull request with a short note explaining what gap it fills

## License

Apache License 2.0.
See the [LICENSE](LICENSE) file for details.

---

Designed for OpenClaw-compatible skill runtimes.
