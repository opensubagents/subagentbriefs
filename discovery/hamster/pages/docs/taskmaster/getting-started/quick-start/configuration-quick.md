---
description: Set up Taskmaster configuration by adding the required API keys and defaults so your first task planning and execution workflow runs smoothly.
title: Configuration | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Configuration

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started  
   * [Overview](https://tryhamster.com/docs/taskmaster/getting-started "Overview")  
   * [Quick Start](https://tryhamster.com/docs/taskmaster/getting-started/quick-start/quick-start "Quick Start")  
   * [API Keys](https://tryhamster.com/docs/taskmaster/getting-started/api-keys "API Keys")  
   * [FAQ](https://tryhamster.com/docs/taskmaster/getting-started/faq "FAQ")  
   * [Contribute](https://tryhamster.com/docs/taskmaster/getting-started/contribute "Contribute")

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities

# Configuration

Before getting started with Taskmaster, you'll need to set up your API keys. There are a couple of ways to do this depending on whether you're using the CLI or working inside MCP. It's also a good time to start getting familiar with the other configuration options available — even if you don't need to adjust them yet, knowing what's possible will help down the line.

## API Key Setup

Taskmaster uses environment variables to securely store provider API keys and optional endpoint URLs.

### MCP Usage: mcp.json file

For MCP/Cursor usage: Configure keys in the env section of your .cursor/mcp.json file.

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "ANTHROPIC_API_KEY": "ANTHROPIC_API_KEY_HERE",
        "PERPLEXITY_API_KEY": "PERPLEXITY_API_KEY_HERE",
        "OPENAI_API_KEY": "OPENAI_API_KEY_HERE",
        "GOOGLE_API_KEY": "GOOGLE_API_KEY_HERE",
        "XAI_API_KEY": "XAI_API_KEY_HERE",
        "OPENROUTER_API_KEY": "OPENROUTER_API_KEY_HERE",
        "MISTRAL_API_KEY": "MISTRAL_API_KEY_HERE",
        "AZURE_OPENAI_API_KEY": "AZURE_OPENAI_API_KEY_HERE",
        "OLLAMA_API_KEY": "OLLAMA_API_KEY_HERE",
        "GITHUB_API_KEY": "GITHUB_API_KEY_HERE"
      }
    }
  }
}

```

> **Tip: Optimize Context Usage**: You can control which Task Master MCP tools are loaded using the `TASK_MASTER_TOOLS` environment variable. This helps reduce LLM context usage by only loading the tools you need.
> 
> Options:
> 
> * `core` or `lean` (default) — 7 essential tools
> * `standard` — 15 commonly used tools
> * `all` — All 36 tools
> 
> Example:
> 
> ```json
> "env": {
>  "TASK_MASTER_TOOLS": "standard",
>  "ANTHROPIC_API_KEY": "your_key_here"
> }
> 
> ```
> 
> See the [MCP Tools documentation](https://tryhamster.com/docs/taskmaster/capabilities/mcp) for details.

### CLI Usage: `.env` File

Create a `.env` file in your project root and include the keys for the providers you plan to use:

```bash
# Required API keys for providers configured in .taskmaster/config.json
ANTHROPIC_API_KEY=sk-ant-api03-your-key-here
PERPLEXITY_API_KEY=pplx-your-key-here
# OPENAI_API_KEY=sk-your-key-here
# GOOGLE_API_KEY=AIzaSy...
# AZURE_OPENAI_API_KEY=your-azure-openai-api-key-here
# etc.

# Optional Endpoint Overrides
# Use a specific provider's base URL, e.g., for an OpenAI-compatible API
# OPENAI_BASE_URL=https://api.third-party.com/v1
#
# Azure OpenAI Configuration
# AZURE_OPENAI_ENDPOINT=https://your-resource-name.openai.azure.com/ or https://your-endpoint-name.cognitiveservices.azure.com/openai/deployments
# OLLAMA_BASE_URL=http://custom-ollama-host:11434/api

# Google Vertex AI Configuration (Required if using 'vertex' provider)
# VERTEX_PROJECT_ID=your-gcp-project-id

```

## What Else Can Be Configured?

The main configuration file (`.taskmaster/config.json`) allows you to control nearly every aspect of Taskmaster’s behavior. Here’s a high-level look at what you can customize:

> **You don't need to configure everything up front. Most settings can be left as defaults or updated later as your workflow evolves.**

## View Configuration Options

### Models and Providers

* Role-based model setup: `main`, `research`, `fallback`
* Provider selection (Anthropic, OpenAI, Perplexity, etc.)
* Model IDs per role
* Temperature, max tokens, and other generation settings
* Custom base URLs for OpenAI-compatible APIs

### Global Settings

* `logLevel`: Logging verbosity
* `debug`: Enable/disable debug mode
* `projectName`: Optional name for your project
* `defaultTag`: Default tag for task grouping
* `defaultSubtasks`: Number of subtasks to auto-generate
* `defaultPriority`: Priority level for new tasks

### API Endpoint Overrides

* `ollamaBaseURL`: Custom Ollama server URL
* `azureBaseURL`: Global Azure endpoint
* `vertexProjectId`: Google Vertex AI project ID
* `vertexLocation`: Region for Vertex AI models

### Tag and Git Integration

* Default tag context per project
* Support for task isolation by tag
* Manual tag creation from Git branches

### State Management

* Active tag tracking
* Migration state
* Last tag switch timestamp

> **For advanced configuration options and detailed customization, see our [Advanced Configuration Guide](https://tryhamster.com/docs/taskmaster/best-practices/configuration-advanced) page.**

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Configuration Quick","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/configuration-quick"}]}
```
