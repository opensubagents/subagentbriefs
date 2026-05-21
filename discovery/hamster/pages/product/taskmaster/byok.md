---
description: Use any AI provider — 15+ API keys supported, zero-key CLI tools, local models, or let Hamster handle everything.
title: Bring Your Own Key — Taskmaster | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

[Taskmaster](https://tryhamster.com/product/taskmaster)/Bring Your Own Key

# Your AI. Your choice.

Use any AI provider — 15+ API keys supported, zero-key CLI tools, local models, or let Hamster handle everything. Taskmaster adapts to how you work.

AI Roles

## Three-role AI system

Assign different models to different roles for optimal cost and performance. Main handles complex reasoning, Research queries live sources, and Fallback ensures reliability during rate limits.

Main Role

Primary model for task generation, updates, and analysis. Best for complex reasoning.

`--set-main claude-sonnet-4`

Research Role

Used with --research flag. Best for real-time web search and fresh information.

`--set-research sonar-pro`

Fallback Role

Automatic failover if main provider fails. Ensures reliability during rate limits.

`--set-fallback gpt-4o-mini`

Providers

## Bring your own API key

Store keys in .env or configure via tm models --setup. Use the provider that works best for you — Anthropic, OpenAI, Google, Perplexity, and more.

AnthropicRec

Claude 4.5 Opus, Sonnet, Haiku

OpenAI

GPT-5, GPT-4.5, o3, o4-mini

Google

Gemini 3 Pro, 2.5 Pro/Flash

Perplexity

Sonar Pro, Sonar Reasoning

Groq

Llama 4, Kimi K2, Mixtral

xAI

Grok 3, Grok 4

OpenRouter

50+ models from all providers

Mistral

Mistral Large, Codestral

Zero Config

## Use your existing subscriptions

Already paying for Claude Max, ChatGPT Plus, or Gemini Code Assist? Use those subscriptions directly — no separate API key needed.

Claude Code CLI

Claude Max/Pro

$0 extra

Use your existing Claude subscription via OAuth

`task-master models --set-main sonnet --claude-code`

Gemini CLI

Gemini Code Assist (Free tier available)

$0 extra

Leverage Google OAuth with free or paid tiers

`task-master models --set-main gemini-3-pro --gemini-cli`

Codex CLI

ChatGPT Plus/Pro/Business

$0 extra

Access GPT-5 through your ChatGPT subscription

`task-master models --set-main gpt-5-codex --codex-cli`

Grok CLI

X Premium/SuperGrok

$0 extra

Use Grok models via X Premium subscription

`task-master models --set-main grok-4-latest --grok-cli`

Privacy

## Run completely local

Use Ollama or LM Studio to run models entirely on your machine. No API key, no internet required, no data leaves your device. Enterprise teams can use AWS Bedrock, Azure OpenAI, or Google Vertex AI.

Popular Local Models

`qwen3:32b`Excellent for code generation

`llama3.3:latest`General purpose, fast

`devstral:latest`Optimized for development

`codellama:34b`Code-specialized

AWS Bedrock

IAM credentials

Azure OpenAI

Azure API key

Google Vertex AI

Service account

Key capabilities

* 15+ API providers supported
* Three-role model configuration (main, research, fallback)
* Zero-key CLI tools with existing subscriptions
* Local model support via Ollama and LM Studio
* Enterprise infrastructure (Bedrock, Azure, Vertex)
* Automatic failover between providers

Works with

[MCP Server](https://tryhamster.com/product/taskmaster/mcp-server) — Configure which provider your MCP server uses.

[Research](https://tryhamster.com/product/taskmaster/research) — Research role powers Perplexity queries.

[Hamster Studio](https://tryhamster.com/product/studio) — Or let Hamster handle AI configuration entirely.

## Configure your AI provider.

Run `tm models --setup` to get started.

[Get started](https://github.com/eyaltoledano/claude-task-master#readme)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Product","item":"https://tryhamster.com/product"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/product/taskmaster"},{"@type":"ListItem","position":4,"name":"Byok","item":"https://tryhamster.com/product/taskmaster/byok"}]}
```
