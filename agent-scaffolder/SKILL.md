---
name: agent-scaffolder
description: Guide users through a structured, step-by-step interviewing process to define and scaffold an AI agent. Collects specifications including role, goals, capabilities, tools, knowledge base, memory, constraints, interaction style, and error handling, then produces a comprehensive, platform-agnostic agent definition document. Use when a user says they want to design, define, scaffold, blueprint, or outline an AI agent.
metadata:
  short-description: Define and blueprint an AI agent through guided questions
---

# Agent Scaffolder

This skill helps you interview the user about their AI agent and produce a structured, platform-agnostic agent definition document. The conversation is organized into six phases, each covering a core dimension of agent design.

## Workflow Overview

1. **Introduce the process** — Briefly explain that you will ask a set of questions organized by topic, and that the final output will be a structured agent definition document.
2. **Collect answers phase by phase** — Ask questions from each phase below. Let the user answer naturally; follow up or clarify when needed. Mark collected data in your working state.
3. **Generate the agent definition document** — After all phases are complete, compile the answers into the structured document format defined in [references/agent-definition-schema.md](./references/agent-definition-schema.md) and write it to a `.md` file in the user's workspace.
4. **Present the result** — Show the file path, summarize what was produced, and ask if the user wants any adjustments.

## Question Catalog

Ask questions conversationally, not like a form. Let the user elaborate. You may rephrase, split, or combine questions as long as all dimensions are covered.

### Phase 1: Foundation

Goal: Establish the agent's identity and purpose.

- What is the agent's name? If the user doesn't have one, suggest a name based on the role (or skip - the name can be derived later).
- What is the agent's primary role? (e.g., code reviewer, customer support agent, data analyst, research assistant, creative writing partner, DevOps engineer, tutor, etc.)
- What is the agent's core mission or primary objective? What problem does it solve for its users?

### Phase 2: Capabilities & Personality

Goal: Define what the agent can do and how it comes across.

- What specific capabilities or skills should the agent have? (e.g., writing code, analyzing data, answering FAQs, generating images, searching the web, summarizing documents, etc.)
- What is the agent's interaction style and personality? (e.g., formal and precise, casual and friendly, empathetic and patient, terse and technical, motivational, Socratic/teaching, etc.)
- What language(s) should the agent primarily operate in, and should it be able to switch between them?

### Phase 3: Tools, Knowledge & Integrations

Goal: Define what resources the agent needs access to.

- What external tools, APIs, or systems should the agent have access to? (e.g., web search, email, database queries, file system, third-party APIs, code execution environment, etc.)
- What knowledge base or reference materials does the agent need? (e.g., internal documentation, product specs, a codebase, policy manuals, research papers, a specific dataset, etc.) Does the user already have these, or do they need to be built?

### Phase 4: Memory & Context

Goal: Define how the agent remembers and maintains state.

- What kind of memory or persistence does the agent need? (e.g., remembers conversation history within a session, recalls user preferences across sessions, maintains a long-term knowledge graph, learns from user feedback over time, etc.)
- What context window or interaction scope should the agent maintain? (e.g., single-turn Q&A, multi-turn conversation within a topic, cross-session continuity, awareness of the full project workspace, etc.)

### Phase 5: Constraints, Safety & Quality

Goal: Define boundaries, failure modes, and quality standards.

- What are the agent's boundaries and limitations? (e.g., topics to avoid, actions it must never take, sensitive data it must never expose, domains it should defer to a human, max confidence threshold before asking for clarification, etc.)
- How should the agent handle errors, ambiguity, or situations it cannot handle? (e.g., ask clarifying questions, gracefully decline, escalate to a human, log the failure, fall back to a simpler response, etc.)
- What quality standards or success criteria should the agent meet? (e.g., response accuracy threshold, citation requirements, response length limits, tone consistency, response time expectations, etc.)

### Phase 6: Output & Interaction Format

Goal: Define how the agent communicates and what it produces.

- What kind of outputs should the agent produce? (e.g., plain text responses, code snippets, structured data/JSON, reports, diagrams, charts, email drafts, etc.)
- What format or medium should the agent use for communication? (e.g., chat interface, markdown documents, API responses, file attachments, voice, etc.)
- Are there any specific formatting, structure, or style requirements for the agent's outputs? (e.g., always cite sources, use a specific template, prioritize brevity, provide step-by-step reasoning, etc.)

## Writing the Output Document

1. When all six phases are complete, read [references/agent-definition-schema.md](./references/agent-definition-schema.md) for the full output template.
2. Compile the user's answers into a markdown file. Use the schema as the structure, filling in each section with the user's actual answers. Adapt the level of detail to what was discussed.
3. Write the file to the user's workspace root as `{agent-name}-definition.md` (or ask the user where they'd like it saved).
4. Present the result and offer to make adjustments.

## Design Principles Embedded in This Skill

- **Platform-agnostic**: The output intentionally avoids framework-specific constructs (LangChain, OpenAI Assistants, etc.). It describes the agent in terms of its concept, not its implementation. The user can later map it to any platform.
- **Conversational, not form-like**: Questions are designed to be asked naturally, with room for follow-ups. The goal is shared understanding, not checkbox completion.
- **Progressive disclosure**: If a user already knows what they want about a dimension, one question may suffice. If they're unsure, explore together. Use the question catalog as a guide, not a script.
