# Agent Definition Schema

This document defines the output schema for the agent-scaffolder skill. When generating the final agent definition document, use this template as the structure and fill each section with the user's answers from the interview.

---

# {Agent Name} — Agent Definition

> **Version:** 1.0
> **Date:** {YYYY-MM-DD}
> **Platform:** Platform-agnostic (see the "Implementation Notes" section for framework mapping)

---

## 1. Identity & Purpose

### Agent Name

{The agent's designated name.}

### Primary Role

{The agent's primary role — one or two sentences describing what kind of agent this is.}

### Mission Statement

{The core mission or primary objective: what problem does this agent solve, and for whom?}

### Target Audience

{Who will interact with this agent? e.g., developers, end customers, internal team members, students, general public, etc.}

---

## 2. Capabilities & Personality

### Core Capabilities

{A bullet list of specific skills or abilities the agent possesses. Describe what the agent can DO, not how it does it.}

- {Capability 1: description}
- {Capability 2: description}
- {Capability 3: description}
- ...

### Interaction Style & Personality

{A description of the agent's tone, demeanor, and communication style.}

- **Tone:** {formal / casual / technical / empathetic / motivational / etc.}
- **Personality traits:** {e.g., patient, direct, encouraging, Socratic, concise, thorough}
- **Communication cadence:** {e.g., brief answers, detailed explanations, step-by-step guidance}

### Languages

{The primary language(s) the agent operates in, and whether it can switch between them.}

---

## 3. Tools, Knowledge & Integrations

### External Tools & APIs

{List of external tools, APIs, systems, or services the agent has access to. Describe the purpose of each.}

| Tool / API | Purpose | Access Level |
|---|---|---|
| {Name} | {What it's used for} | {Read / Write / Admin} |
| ... | ... | ... |

### Knowledge Base

{Description of the knowledge sources the agent relies on. Include whether these already exist or need to be built.}

- **Internal documentation:** {description}
- **Reference materials:** {description}
- **Databases / datasets:** {description}
- **Code repositories:** {description}
- **Other:** {description}

---

## 4. Memory & Context

### Memory Model

{Description of the agent's memory and persistence capabilities.}

- **Session memory:** {Does the agent remember context within a single conversation?}
- **Cross-session memory:** {Does the agent recall information from previous interactions?}
- **Long-term learning:** {Does the agent adapt or learn from feedback over time?}
- **Memory storage:** {Where/how is memory stored? e.g., conversation history, knowledge graph, vector database, external file}

### Context Scope

{What context does the agent maintain awareness of?}

- **Interaction scope:** {single-turn / multi-turn within topic / cross-session / full project workspace awareness}
- **Context boundaries:** {When and how does context get reset or truncated?}

---

## 5. Constraints, Safety & Quality

### Boundaries & Limitations

{Clear rules about what the agent must not do or engage with.}

- **Prohibited topics:** {topics the agent must avoid or defer}
- **Prohibited actions:** {actions the agent must never take}
- **Data sensitivity:** {rules about handling sensitive or private information}
- **Escalation criteria:** {conditions under which the agent should defer to a human}
- **Confidence threshold:** {minimum confidence level before asking for clarification or deferring}

### Error Handling & Fallbacks

{How the agent behaves when it encounters errors, ambiguity, or situations it cannot handle.}

- **Ambiguity:** {e.g., asks clarifying questions}
- **Uncertainty:** {e.g., states confidence level, offers alternatives}
- **Errors/failures:** {e.g., logs the error, retries, falls back to a simpler approach}
- **Out-of-scope requests:** {e.g., gracefully declines, provides alternative resources}
- **Critical failures:** {e.g., escalates to human, stops processing}

### Quality Standards

{The criteria that define a successful interaction.}

- **Accuracy:** {expected response accuracy or correctness threshold}
- **Citations:** {when and how sources must be cited}
- **Response length:** {minimum/maximum length expectations}
- **Tone consistency:** {guidelines for maintaining consistent tone}
- **Response time:** {expected response latency or performance targets}
- **Format compliance:** {any specific output structure requirements}

---

## 6. Output & Interaction Format

### Output Types

{The kinds of outputs the agent produces.}

- {Output type 1: description and format}
- {Output type 2: description and format}
- ...

### Communication Medium

{The medium(s) through which the agent communicates.}

- {e.g., Chat interface, markdown documents, API responses, file attachments, email, voice, etc.}

### Formatting & Style Guide

{Specific rules for how the agent structures its responses.}

- {Rule 1: e.g., "Always begin responses with a brief summary"}
- {Rule 2: e.g., "Use markdown formatting for code blocks"}
- {Rule 3: e.g., "Provide step-by-step reasoning before conclusions"}
- ...

---

## 7. Example Interaction

{A concrete example showing the agent in action — a user request and the agent's ideal response. This serves as a touchstone for behavior validation.}

```
User: {Example user input}
Agent: {Example ideal response}
```

---

## 8. Implementation Notes

{Optional section: notes on how this agent definition could be mapped to specific platforms or frameworks. This section is for internal reference and may be omitted from the delivered document.}

- **Recommended platform fit:** {e.g., "This agent's memory and tool-use requirements make it a good fit for an OpenAI Assistant with Retrieval and Code Interpreter enabled."}
- **Key implementation considerations:** {e.g., "The knowledge base should be chunked and indexed in a vector database for efficient retrieval."}
- **Potential challenges:** {e.g., "Cross-session memory requires an external persistence layer."}

---

*Generated by [agent-scaffolder](https://github.com/user/agent-scaffolder)*
