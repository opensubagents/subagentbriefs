---
description: Taskmaster supports 15+ AI providers including cloud, local, and CLI-based models. Learn how Hamster helps teams plan, build, and ship software faster...
title: AI Providers | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Provider Overview

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

# AI Providers

Taskmaster works with 15+ AI providers. You can mix and match — use Anthropic for task generation, Perplexity for research, and a local model for fallback. Bring your own keys and switch models anytime.

## Three Model Roles

Taskmaster uses three independent model roles, each configurable with its own provider and model:

| Role     | Purpose                                               | Default                 |
| -------- | ----------------------------------------------------- | ----------------------- |
| Main     | Task generation, expansion, updates, and analysis     | Anthropic Claude Sonnet |
| Research | Live web search for current information and citations | Perplexity Sonar        |
| Fallback | Used when the main model fails or is unavailable      | Anthropic Claude Sonnet |

## Configuring Models

```bash
# Interactive setup — walks through all three roles
tm models --setup

# Set models directly
tm models --set-main claude-sonnet-4-20250514
tm models --set-research sonar
tm models --set-fallback gpt-4o-mini

# View current configuration
tm models

```

## Supported Cloud Providers

| Provider       | Models                     | Best for                              |
| -------------- | -------------------------- | ------------------------------------- |
| Anthropic      | Claude Opus, Sonnet, Haiku | General-purpose (recommended default) |
| OpenAI         | GPT-4o, o3, o3-mini        | Reasoning-heavy tasks                 |
| Google         | Gemini Pro, Gemini Flash   | Fast generation, large context        |
| Perplexity     | Sonar, Sonar Deep Research | Research with live web access         |
| xAI            | Grok 4, Grok 3, Grok 2     | Large codebase context                |
| Groq           | Various models             | Fast inference                        |
| OpenRouter     | 100+ models                | Access any model through one API      |
| Mistral        | Mistral models             | European AI provider                  |
| Azure OpenAI   | GPT models via Azure       | Enterprise deployments                |
| Amazon Bedrock | Claude via AWS             | AWS-native deployments                |
| Google Vertex  | Gemini via GCP             | Google Cloud deployments              |

## Local & CLI Providers

Run Taskmaster without sending data to external APIs:

| Provider          | Setup                        | Cost                               |
| ----------------- | ---------------------------- | ---------------------------------- |
| Ollama            | Install Ollama, pull a model | Free, fully offline                |
| LM Studio         | Download models locally      | Free, fully offline                |
| Claude Code       | Install Claude Code CLI      | Uses your Claude Code subscription |
| Gemini CLI        | Google account               | Free tier available                |
| OpenAI-compatible | Any compatible endpoint      | Varies                             |

For details on local model setup, see [Local Models](https://tryhamster.com/docs/taskmaster/ai-providers/local-models).

## Switching Providers

You can change providers at any time without affecting your tasks:

```bash
# Switch main model to OpenAI
tm models --set-main gpt-4o

# Switch to a local model
tm models --set-main ollama/llama3

# Use Claude Code (no API key needed)
tm models --set-main claude-code/sonnet

```

## API Key Setup

Each provider requires its own API key. See [API Keys](https://tryhamster.com/docs/taskmaster/getting-started/api-keys) for the complete setup guide.

Keys can be configured via:

* **`.env` file** in your project root
* **Environment variables** in your shell
* **MCP server config** in `.mcp.json` or editor settings

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Ai Providers","item":"https://tryhamster.com/docs/taskmaster/ai-providers"},{"@type":"ListItem","position":5,"name":"Overview","item":"https://tryhamster.com/docs/taskmaster/ai-providers/overview"}]}
```
