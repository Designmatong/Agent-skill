<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://img.shields.io/badge/Codex-Skill-8B5CF6?style=for-the-badge&logo=data:image/svg+xml;base64,PHN2ZyB4bWxucz0iaHR0cDovL3d3dy53My5vcmcvMjAwMC9zdmciIHdpZHRoPSIyNCIgaGVpZ2h0PSIyNCIgdmlld0JveD0iMCAwIDI0IDI0IiBmaWxsPSJub25lIiBzdHJva2U9IiNmZmZmZmYiIHN0cm9rZS13aWR0aD0iMiIgc3Ryb2tlLWxpbmVjYXA9InJvdW5kIiBzdHJva2UtbGluZWpvaW49InJvdW5kIj48cGF0aCBkPSJNMTIgMmw1LjUgNy41TDIyIDJsLTUuNSA3LjVMMjIgMTdsLTUuNS0zLjVMMTIgMjJsLTQuNS04LjVMMiAxN2w0LjUtNy41TDIgMmw0LjUgNy41TDEyIDJ6Ii8+PC9zdmc+">
    <img src="https://img.shields.io/badge/Codex-Skill-8B5CF6?style=for-the-badge" alt="Codex Skill">
  </picture>
</p>

<h1 align="center">Agent Scaffolder</h1>

<p align="center">
  <strong>Define and blueprint AI agents through a structured, conversational interview</strong>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/version-1.0.0-8B5CF6?style=flat-square" alt="Version">
  <img src="https://img.shields.io/badge/platform-agent--agnostic-10B981?style=flat-square" alt="Platform Agnostic">
  <img src="https://img.shields.io/badge/interview-6%20phases-3B82F6?style=flat-square" alt="6 Phases">
  <img src="https://img.shields.io/badge/output-structured%20document-F59E0B?style=flat-square" alt="Structured Output">
</p>

<p align="center">
  <em>A Codex skill that guides you through 6 discovery phases — from role and capabilities to constraints and output format — then produces a comprehensive, platform-agnostic agent definition document.</em>
</p>

<br>

---

## Overview

**Agent Scaffolder** transforms the fuzzy vision of "I want to build an AI agent" into a concrete, structured specification. Instead of staring at a blank page, you walk through a conversation designed to explore every dimension of your agent.

The skill interviews you across **6 phases** (14+ questions) and compiles your answers into a polished markdown document you can use as a blueprint, share with your team, or map directly onto any platform — OpenAI, LangChain, custom frameworks, or something you haven't decided on yet.

**What you get:** A living specification document covering identity, capabilities, tools, memory, constraints, and interaction design.

<br>

## How It Works

```
  Phase 1          Phase 2           Phase 3           Phase 4           Phase 5            Phase 6
┌────────────┐  ┌──────────────┐  ┌──────────────┐  ┌────────────┐  ┌────────────────┐  ┌──────────────────┐
│ Foundation  │→ │ Capabilities │→ │ Tools &      │→ │ Memory &   │→ │ Constraints,   │→ │ Output &         │
│             │  │ & Personality│  │ Knowledge    │  │ Context    │  │ Safety &       │  │ Interaction      │
│ Role        │  │ Skills       │  │ External APIs│  │ Persistence│  │ Quality        │  │ Format           │
│ Mission     │  │ Tone         │  │ Docs & Data  │  │ Scope      │  │ Boundaries     │  │ Output types     │
│ Audience    │  │ Languages    │  │ Integrations │  │ Continuity │  │ Error handling │  │ Style            │
└────────────┘  └──────────────┘  └──────────────┘  └────────────┘  └────────────────┘  └──────────────────┘
       │               │                 │                │                │                     │
       └───────────────┴─────────────────┴────────────────┴────────────────┴─────────────────────┘
                                                    │
                                                    ▼
                                  ┌─────────────────────────────────┐
                                  │    Agent Definition Document     │
                                  │   ────────────────────────────   │
                                  │   •  Identity & Purpose          │
                                  │   •  Capabilities & Personality  │
                                  │   •  Tools & Integrations        │
                                  │   •  Memory & Context            │
                                  │   •  Constraints & Quality       │
                                  │   •  Output & Interaction        │
                                  │   •  Example Interaction         │
                                  │   •  Implementation Notes        │
                                  └─────────────────────────────────┘
```

<br>

## The 6 Phases

### 1. Foundation
Establishes the agent's identity and purpose. You define what the agent is called, its primary role, its core mission, and who it serves.

### 2. Capabilities & Personality
Defines what the agent can do and how it comes across. Skills, interaction style, tone, personality traits, and language support.

### 3. Tools, Knowledge & Integrations
Maps out the resources the agent needs — external APIs, databases, file systems, knowledge bases, reference materials, and whether those resources already exist or need to be built.

### 4. Memory & Context
Defines how the agent remembers and maintains state — session memory, cross-session persistence, long-term learning, and interaction scope.

### 5. Constraints, Safety & Quality
Establishes boundaries: prohibited topics, actions to never take, data sensitivity rules, error handling strategies, and quality benchmarks.

### 6. Output & Interaction Format
Defines how the agent communicates — output types, communication medium, formatting style, and structural requirements.

<br>

## Output Document

Every interview produces a structured markdown document covering 8 sections:

| Section | Description |
|---|---|
| **Identity & Purpose** | Name, role, mission statement, target audience |
| **Capabilities & Personality** | Skills, tone, personality traits, language support |
| **Tools, Knowledge & Integrations** | External APIs, knowledge bases, reference materials |
| **Memory & Context** | Memory model, persistence strategy, context scope |
| **Constraints, Safety & Quality** | Boundaries, error handling, quality standards |
| **Output & Interaction Format** | Output types, communication medium, style guide |
| **Example Interaction** | Concrete user-agent exchange for behavior validation |
| **Implementation Notes** | Platform mapping recommendations (optional) |

The output is **platform-agnostic by design** — it describes what the agent is, not how to implement it. You can map it to any framework later.

<br>

## Installation

### Via Codex Marketplace (recommended)

```bash
# Coming soon
```

### Manual install

Clone or download the skill into your Codex skills directory:

```bash
git clone https://github.com/Designmatong/ComClean.git
# or copy the `agent-scaffolder` folder into:
# ~/.codex/skills/agent-scaffolder/
```

Or simply place the skill folder anywhere in your workspace and reference it by name when needed.

<br>

## Quick Start

Once the skill is available, just tell Codex:

> **"I want to design an AI agent. Can you help me define it?"**

or

> **"Let's scaffold an agent for reviewing pull requests."**

Codex will load the skill and begin the conversational interview, phase by phase.

<br>

## Project Structure

```
agent-scaffolder/
├── SKILL.md                              # Main skill instructions
│   ├── Workflow overview
│   ├── Question catalog (6 phases)
│   └── Output generation instructions
├── references/
│   └── agent-definition-schema.md        # Output document template
├── scripts/
│   └── generate_agent_definition.py      # CLI tool for deterministic output
└── agents/
    └── openai.yaml                       # UI metadata for skill discovery
```

<br>

## Design Principles

- **Platform-agnostic** — The output avoids framework-specific constructs. Describe your agent's concept, not its implementation.
- **Conversational, not form-like** — Questions are designed for natural dialogue with room for follow-ups. The goal is shared understanding, not checkbox completion.
- **Progressive disclosure** — If you know what you want, one question may suffice. If you're unsure, the skill explores together with you.
- **Token-conscious** — SKILL.md is kept lean; detailed reference material stays in separate files, loaded only when needed.

<br>

## Use Cases

- **Define a new agent from scratch** — No blank page syndrome. Walk through the phases and emerge with a complete spec.
- **Document an existing agent** — Reverse-engineer your running agent into a shareable specification.
- **Compare design alternatives** — Run the interview twice with different answers and compare the outputs.
- **Onboard collaborators** — Share the output document so everyone agrees on what the agent should be.
- **Prepare for implementation** — Use the spec as input for building on OpenAI, LangChain, Anthropic, or any other platform.

<br>

## Example Output

A sample agent definition generated by this skill:

```markdown
# PR Pilot — Agent Definition

## 1. Identity & Purpose
- **Role:** Automated code review assistant
- **Mission:** Catch bugs, style issues, and security problems before they reach production
- **Audience:** Engineering teams using GitHub

## 2. Capabilities & Personality
- **Skills:** Diff analysis, static code analysis, security scanning
- **Tone:** Constructive and precise — not punitive, not casual
- **Languages:** English (primary), with syntax awareness for 10+ programming languages

[ ... and 5 more sections covering tools, memory, constraints, and output format ... ]
```

<br>

## License

MIT License © 2025 Designmatong

<br>

---

<p align="center">
  <sub>Built for <a href="https://github.com/Designmatong/ComClean">ComClean</a> · Agent Scaffolder Skill · v1.0.0</sub>
</p>
