<div align="center">

# LangChain Agentic AI

**A hands-on crash course for building AI agents with LangChain — from basics to middleware, tools, structured output, and human-in-the-loop workflows.**

[![Python](https://img.shields.io/badge/Python-3.13+-3776AB?style=for-the-badge&logo=python&logoColor=white)](https://python.org)
[![LangChain](https://img.shields.io/badge/LangChain-1.3+-1C3C3C?style=for-the-badge&logo=langchain&logoColor=white)](https://langchain.com)
[![Groq](https://img.shields.io/badge/Groq-LLM_Inference-F55B38?style=for-the-badge)](https://groq.com)
[![Google AI](https://img.shields.io/badge/Google_Gemini-AI-4285F4?style=for-the-badge&logo=google&logoColor=white)](https://ai.google.dev)
[![License](https://img.shields.io/badge/License-MIT-green?style=for-the-badge)](LICENSE)

<br/>

<!-- Replace with actual screenshot/video later -->
<!-- ![Demo](assets/demo.gif) -->

</div>

---

## Table of Contents

- [Overview](#overview)
- [Topics Covered](#topics-covered)
- [Project Structure](#project-structure)
- [Setup](#setup)
- [Environment Variables](#environment-variables)
- [Notebooks](#notebooks)
- [Tech Stack](#tech-stack)
- [Media](#media)
- [License](#license)

---

## Overview

This repository is a **structured learning path** for LangChain's agentic AI capabilities. Each notebook walks through a core concept with runnable examples — from sending your first message to building agents with human-in-the-loop safeguards.

Whether you're new to LangChain or looking to understand middleware, tools, and structured outputs, this repo gives you **copy-paste-ready code** with explanations.

---

## Topics Covered

| Topic | Description |
|-------|-------------|
| **Model Integration** | Connect to Groq, Google Gemini, and other LLM providers |
| **Messages** | System, Human, and AI message types and conversation flow |
| **Tools** | Define and bind custom tools for agent function calling |
| **Structured Output** | Get typed, schema-validated responses from LLMs |
| **Middleware** | Summarization, token management, and execution control |
| **Human in the Loop** | Pause agent execution for human approval, editing, or rejection |

---

## Project Structure

```
langchain-agentic-ai/
├── main.py
├── pyproject.toml
├── requirements.txt
├── README.md
└── updatedlangchain/
    ├── langchainintro.ipynb        # LangChain basics
    ├── messages.ipynb              # Message types & roles
    ├── modelIntegration.ipynb      # LLM provider setup
    ├── structuredoutput.ipynb      # Schema-validated outputs
    ├── tools.ipynb                 # Tool binding & calling
    ├── middleware.ipynb             # Summarization middleware
    ├── api-integration-guide.md    # API setup reference
    ├── structured-output-notes.md  # Structured output cheat sheet
    ├── tools-notes.md              # Tools cheat sheet
    └── human-in-the-loop-notes.md  # HITL explanation
```

---

## Setup

```bash
# Clone the repo
git clone https://github.com/<your-username>/langchain-agentic-ai.git
cd langchain-agentic-ai

# Install dependencies
uv sync

# Add new dependencies
uv add <package-name>
```

---

## Environment Variables

Create a `.env` file in the project root:

```env
GROQ_API_KEY=your_groq_api_key_here
GOOGLE_API_KEY=your_google_api_key_here
```

> **Note:** Use underscores (`_`) in env variable names — Python's `os.getenv()` can't read hyphens.

---

## Notebooks

### 1. LangChain Intro
Getting started with LangChain — model invocation, prompts, and chains.

### 2. Messages
Understanding `SystemMessage`, `HumanMessage`, and `AIMessage` — how conversation context flows through the agent.

### 3. Model Integration
Setting up LLM providers:
- **Groq** — `groq:llama-3.3-70b-versatile`, `groq:qwen/qwen3-32b`
- **Google Gemini** — `google_genai:gemini-2.0-flash`

> Always use the provider prefix (e.g., `groq:`, `google_genai:`). Auto-detection fails for non-OpenAI models.

### 4. Tools
Define custom functions with `@tool` decorator and bind them to agents for function calling.

### 5. Structured Output
Get typed Pydantic models back from LLMs instead of raw text.

### 6. Middleware — Summarization
Automatically compress long conversation histories to reduce token usage:
- **Message-based trigger** — summarize after N messages
- **Token-based trigger** — summarize after N tokens
- **Fraction-based trigger** — summarize after X% of context window

### 7. Middleware — Human in the Loop
Pause agent execution before sensitive operations:
- **Approve** — let the agent proceed
- **Reject** — block the action
- **Edit** — modify arguments before execution

---

## Tech Stack

| Component | Technology |
|-----------|-----------|
| Framework | LangChain 1.3+ |
| LLM Providers | Groq, Google Gemini |
| Agent Runtime | LangGraph |
| Language | Python 3.13+ |
| Package Manager | uv |

---

## Media

<!-- Replace with actual screenshots/videos -->

### Screenshots

> _Coming soon_

### Demo Video

> _Coming soon_

---

## License

This project is licensed under the MIT License.

---

<div align="center">

**Built with LangChain**

</div>
