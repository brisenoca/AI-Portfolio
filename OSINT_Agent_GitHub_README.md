# OSINT Research Agent

An AI-powered open-source intelligence (OSINT) investigative research agent built on the Anthropic API. Given any topic or entity, the agent autonomously conducts multi-pass web searches, synthesizes findings, and returns a structured intelligence report.

---

## Overview

This project demonstrates an **agentic AI architecture** in which a language model is given tools (live web search) and autonomously decides how to use them to complete a research task — without user intervention between steps.

The agent produces structured reports covering:
- Executive summary
- Key findings
- Entity profile
- Recent activity
- Open questions / intelligence gaps
- Source assessment

---

## Architecture

```
User Query
    │
    ▼
Agent Loop (Claude claude-sonnet-4-20250514)
    ├── Tool: web_search (Anthropic built-in)
    ├── Multi-pass retrieval (surface / standard / deep)
    └── Synthesis + structured report generation
    │
    ▼
Intelligence Report
```

The agent uses Anthropic's **tool use API** with the `web_search_20250305` tool. Claude autonomously decides which queries to run, how many searches to perform, and how to weight conflicting sources — mimicking the reasoning process of a human analyst.

---

## Tech Stack

| Layer | Technology |
|---|---|
| LLM | Claude claude-sonnet-4-20250514 (Anthropic) |
| Tool | `web_search_20250305` (Anthropic native) |
| Frontend | React (embedded artifact) |
| API | Anthropic `/v1/messages` |

---

## Key Concepts Demonstrated

- **Agentic AI loop** — model drives its own tool use without hardcoded search queries
- **Prompt engineering** — system prompt structures output into a reproducible intelligence report format
- **Tool use / function calling** — real-time web search integrated into model inference
- **Depth scaling** — configurable investigation depth (surface / standard / deep) that adjusts agent behavior
- **Applied OSINT** — automated open-source intelligence gathering for entity research, threat awareness, and background investigation

---

## Usage

Enter any topic or entity into the search bar and select a depth level:

| Depth | Description |
|---|---|
| Surface | Single-pass scan, fast results |
| Standard | Broader search with synthesis |
| Deep | Multi-angle investigation, most thorough |

Example queries:
- `Palantir government contracts 2025`
- `CISA threat advisories recent`
- `[Organization name] leadership and funding`

---

## Background

This project was developed as part of a career transition into AI/ML engineering, combining a background in U.S. Marine Corps service, IT infrastructure, government/military systems, and a Master's in Artificial Intelligence (Penn State, in progress).

The OSINT use case was chosen deliberately — it bridges prior national security and IT security experience with applied AI, demonstrating that domain expertise accelerates the design of targeted AI tools.

---

## Future Development

- [ ] Multi-agent architecture (separate search agent, analysis agent, report agent)
- [ ] Persistent memory / session history
- [ ] RAG integration for document corpus search alongside web
- [ ] Entity relationship graph visualization
- [ ] Export to PDF / structured JSON

---

## Author

Christian A. Briseno  
M.S. Artificial Intelligence candidate, Penn State  
Former U.S. Marine | IT Infrastructure & Government Systems  
[LinkedIn](#) · [GitHub](#)
