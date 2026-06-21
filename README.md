# Narrative Architect Skill

**English** | [简体中文](README.zh-CN.md)

Turn abstract, technical, or sensitive material into clear, audience-specific communication.

Most drafts fail in the same quiet way: the facts are correct, but nobody feels why they matter. Narrative Architect Skill helps you find the pressure, conflict, and turn inside complex material — then shape it for the person you actually need to reach. It will not make everyone like your message. It helps the right listener understand why it matters.

The skill preserves source meaning and claim boundaries while improving narrative structure, emotional force, audience fit, and surface naturalness.

It is inspired by story-principle methods, including Robert McKee-style narrative thinking, but it is not affiliated with Robert McKee or any third-party writing program.

## What It Does

- **Finds the narrative kernel** — what is at stake, what old assumption is breaking
- **Reads the audience** — what they know, what they fear, where to start
- **Controls rhythm** — when to ground the reader, when to surprise them
- **Keeps factual claims inside the boundary of what is known**

For source-grounded work, factual claims stay tied to known material. If the source has gaps, the output names them instead of filling them with speculation.

## Common Tasks

Use this skill when the user asks to:

- rewrite an email, message, post, proposal, README, article, speech, or pitch
- turn technical material into a non-technical explanation
- create founder, investor, customer, partner, or executive communication
- improve a draft that sounds too generic, too AI-written, too formal, too salesy, or too abstract
- adapt one idea for different audiences, such as developers, investors, customers, executives, or general readers
- preserve factual claims while making the communication sharper, more natural, and more persuasive

## Example Prompts

- "Rewrite this founder update so it sounds sharper and less generic."
- "Turn this technical concept into a clear explanation for non-technical executives."
- "Help me write a launch post for this open-source project."
- "Rewrite this README introduction so developers understand the value faster."
- "Turn this product explanation into an investor pitch narrative."
- "Make this message warmer, more direct, and less AI-written."
- "Convert this abstract idea into a story people can remember."

## Who It's For

Writers, founders, developers, marketers, operators, and product teams use this skill to draft and rewrite high-stakes communication: emails, pitches, launch posts, speeches, README introductions, proposals, personal messages, executive summaries, and technical-to-nontechnical explanations.

The skill is useful when the source material is abstract, technical, sensitive, strategic, or too generic. It improves narrative structure, audience fit, claim fidelity, emotional force, and naturalness while avoiding over-selling or unsupported claims.

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
