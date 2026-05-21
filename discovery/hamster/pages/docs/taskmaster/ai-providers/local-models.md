---
description: Run Taskmaster with fully offline models using Ollama, LM Studio, or CLI-based providers. Learn how Hamster helps teams plan, build, and ship software...
title: Local Models | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Local Models

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers  
   * [Provider Overview](https://tryhamster.com/docs/taskmaster/ai-providers/overview "Provider Overview")  
   * [Local Models](https://tryhamster.com/docs/taskmaster/ai-providers/local-models "Local Models")

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Local & Offline Models

Taskmaster can run entirely offline using local AI models. This is useful for air-gapped environments, cost-sensitive workflows, or when you prefer to keep data on your machine.

## Ollama

[Ollama](https://ollama.com) runs open-source models locally with a simple CLI.

**Setup:**

```bash
# Install Ollama
curl -fsSL https://ollama.com/install.sh | sh

# Pull a model
ollama pull llama3

# Configure Taskmaster to use it
tm models --set-main ollama/llama3

```

No API key is needed for local Ollama. If you're connecting to a remote Ollama server, set `OLLAMA_API_KEY` in your environment.

## LM Studio

[LM Studio](https://lmstudio.ai) provides a desktop app for downloading and running models locally with zero configuration.

**Setup:**

1. Download and install LM Studio
2. Browse and download a model from the built-in model hub
3. Start the local server in LM Studio
4. Configure Taskmaster:

```bash
tm models --set-main lmstudio/your-model-name

```

## Claude Code CLI

If you have Claude Code installed, Taskmaster can use it directly — no separate API key needed.

```bash
tm models --set-main claude-code/sonnet

```

Claude Code respects your existing configuration (`~/.claude/`, `.claude/`, `CLAUDE.md`) and provides codebase-aware results by analyzing your project structure.

## Gemini CLI

Google's Gemini CLI works with a free Google account.

```bash
tm models --set-main gemini-cli/gemini-2.0-flash

```

Gemini CLI provides structured output support and codebase analysis. A Google Cloud Application (GCA) subscription removes rate limits.

## OpenAI-Compatible Endpoints

Connect any service that implements the OpenAI API format:

```bash
# Set custom endpoint
tm models --set-main openai-compatible/your-model

# Configure the base URL in .env
OPENAI_COMPATIBLE_BASE_URL="http://localhost:8080/v1"

```

This works with vLLM, text-generation-webui, LocalAI, and other OpenAI-compatible servers.

## Choosing a Local Model

| Use case                  | Recommended                |
| ------------------------- | -------------------------- |
| Best quality, no internet | Ollama with a large model  |
| Easy setup, desktop app   | LM Studio                  |
| Already use Claude Code   | Claude Code CLI            |
| Free, Google account      | Gemini CLI                 |
| Custom infrastructure     | OpenAI-compatible endpoint |

## Limitations

Local models may produce lower quality results compared to cloud providers, especially for complex task generation and expansion. Consider using a cloud provider for the main model and a local model as the fallback:

```bash
tm models --set-main claude-sonnet-4-20250514
tm models --set-fallback ollama/llama3

```

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Ai Providers","item":"https://tryhamster.com/docs/taskmaster/ai-providers"},{"@type":"ListItem","position":5,"name":"Local Models","item":"https://tryhamster.com/docs/taskmaster/ai-providers/local-models"}]}
```
