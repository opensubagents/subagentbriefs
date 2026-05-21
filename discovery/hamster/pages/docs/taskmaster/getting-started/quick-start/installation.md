---
description: Now that you have Node.js and your first API Key, you are ready to begin installing Taskmaster. Learn how Hamster helps teams plan, build, and ship...
title: Installation | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Installation

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

# Installation

Now that you have Node.js and your first API Key, you are ready to begin installing Taskmaster in one of three ways.

> **Cursor Users Can Use the One Click Install Below**

## Quick Install for Cursor 1.0+ (One-Click)

[![Add Taskmaster MCP server to Cursor](https://cursor.com/deeplink/mcp-install-light.png)![Add Taskmaster MCP server to Cursor](https://cursor.com/deeplink/mcp-install-dark.png)](cursor://anysphere.cursor-deeplink/mcp/install?name=task-master-ai&config=eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyIteSIsIi0tcGFja2FnZT10YXNrLW1hc3Rlci1haSIsInRhc2stbWFzdGVyLWFpIl0sImVudiI6eyJBTlRIUk9QSUNfQVBJX0tFWSI6IllPVVJfQU5USFJPUElDX0FQSV9LRVlfSEVSRSIsIlBFUlBMRVhJVFlfQVBJX0tFWSI6IllPVVJfUEVSUExFWElUWV9BUElfS0VZX0hFUkUiLCJPUEVOQUlfQVBJX0tFWSI6IllPVVJfT1BFTkFJX0tFWV9IRVJFIiwiR09PR0xFX0FQSV9LRVkiOiJZT1VSX0dPT0dMRV9LRVlfSEVSRSIsIk1JU1RSQUxfQVBJX0tFWSI6IllPVVJfTUlTVFJBTF9LRVlfSEVSRSIsIk9QRU5ST1VURVJfQVBJX0tFWSI6IllPVVJfT1BFTlJPVVRFUl9LRVlfSEVSRSIsIlhBSV9BUElfS0VZIjoiWU9VUl9YQUlfS0VZX0hFUkUiLCJBWlVSRV9PUEVOQUJFX0FQSV9LRVkiOiJZT1VSX0FaVVJFX0tFWV9IRVJFIiwiT0xMQU1BX0FQSV9LRVkiOiJZT1VSX09MTEFNQV9BUElfS0VZX0hFUkUifX0%3D) 

Or click the copy button (top-right of code block) then paste into your browser:

```text
cursor://anysphere.cursor-deeplink/mcp/install?name=taskmaster-ai&config=eyJjb21tYW5kIjoibnB4IiwiYXJncyI6WyIteSIsIi0tcGFja2FnZT10YXNrLW1hc3Rlci1haSIsInRhc2stbWFzdGVyLWFpIl0sImVudiI6eyJBTlRIUk9QSUNfQVBJX0tFWSI6IllPVVJfQU5USFJPUElDX0FQSV9LRVlfSEVSRSIsIlBFUlBMRVhJVFlfQVBJX0tFWSI6IllPVVJfUEVSUExFWElUWV9BUElfS0VZX0hFUkUiLCJPUEVOQUlfQVBJX0tFWSI6IllPVVJfT1BFTkFJX0tFWV9IRVJFIiwiR09PR0xFX0FQSV9LRVkiOiJZT1VSX0dPT0dMRV9LRVlfSEVSRSIsIk1JU1RSQUxfQVBJX0tFWSI6IllPVVJfTUlTVFJBTF9LRVlfSEVSRSIsIk9QRU5ST1VURVJfQVBJX0tFWSI6IllPVVJfT1BFTlJPVVRFUl9LRVlfSEVSRSIsIlhBSV9BUElfS0VZIjoiWU9VUl9YQUlfS0VZX0hFUkUiLCJBWlVSRV9PUEVOQUlfQVBJX0tFWSI6IllPVVJfQVpVUkVfS0VZX0hFUkUiLCJPTExBTUFfQVBJX0tFWSI6IllPVVJfT0xMQU1BX0FQSV9LRVlfSEVSRSJ9fQo=

```

> **Note:** After clicking the link, you'll still need to add your API keys to the configuration. The link installs the MCP server with placeholder keys that you'll need to replace with your actual API keys.

### Claude Code Quick Install

For Claude Code users:

```bash
claude mcp add taskmaster-ai -- npx -y task-master-ai

```

Don't forget to add your API keys to the configuration:

* in the root .env of your Project
* in the "env" section of your mcp config for taskmaster-ai

## Installation Options

## Option 1: MCP (Recommended)

MCP (Model Control Protocol) lets you run Taskmaster directly from your editor.

## 1\. Add your MCP config at the following path depending on your editor

| Editor   | Scope                              | Linux/macOS Path                      | Windows Path                                        | Key        |
| -------- | ---------------------------------- | ------------------------------------- | --------------------------------------------------- | ---------- |
| Cursor   | Global                             | \~/.cursor/mcp.json                   | %USERPROFILE%\\.cursor\\mcp.json                    | mcpServers |
| Project  | <project\_folder>/.cursor/mcp.json | <project\_folder>\\.cursor\\mcp.json  | mcpServers                                          |            |
| Windsurf | Global                             | \~/.codeium/windsurf/mcp\_config.json | %USERPROFILE%\\.codeium\\windsurf\\mcp\_config.json | mcpServers |
| VS Code  | Project                            | <project\_folder>/.vscode/mcp.json    | <project\_folder>\\.vscode\\mcp.json                | servers    |

## Manual Configuration

### Cursor & Windsurf (`mcpServers`)

```json
{
  "mcpServers": {
    "taskmaster-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "ANTHROPIC_API_KEY": "YOUR_ANTHROPIC_API_KEY_HERE",
        "PERPLEXITY_API_KEY": "YOUR_PERPLEXITY_API_KEY_HERE",
        "OPENAI_API_KEY": "YOUR_OPENAI_KEY_HERE",
        "GOOGLE_API_KEY": "YOUR_GOOGLE_KEY_HERE",
        "MISTRAL_API_KEY": "YOUR_MISTRAL_KEY_HERE",
        "OPENROUTER_API_KEY": "YOUR_OPENROUTER_KEY_HERE",
        "XAI_API_KEY": "YOUR_XAI_KEY_HERE",
        "AZURE_OPENAI_API_KEY": "YOUR_AZURE_KEY_HERE",
        "OLLAMA_API_KEY": "YOUR_OLLAMA_API_KEY_HERE"
      }
    }
  }
}

```

> 🔑 Replace `YOUR_…_KEY_HERE` with your real API keys. You can remove keys you don't use.

> **Note**: If you see `0 tools enabled` in the MCP settings, restart your editor and check that your API keys are correctly configured.

### VS Code (`servers` \+ `type`)

```json
{
  "servers": {
    "taskmaster-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "ANTHROPIC_API_KEY": "YOUR_ANTHROPIC_API_KEY_HERE",
        "PERPLEXITY_API_KEY": "YOUR_PERPLEXITY_API_KEY_HERE",
        "OPENAI_API_KEY": "YOUR_OPENAI_KEY_HERE",
        "GOOGLE_API_KEY": "YOUR_GOOGLE_KEY_HERE",
        "MISTRAL_API_KEY": "YOUR_MISTRAL_KEY_HERE",
        "OPENROUTER_API_KEY": "YOUR_OPENROUTER_KEY_HERE",
        "XAI_API_KEY": "YOUR_XAI_KEY_HERE",
        "AZURE_OPENAI_API_KEY": "YOUR_AZURE_KEY_HERE"
      },
      "type": "stdio"
    }
  }
}

```

> 🔑 Replace `YOUR_…_KEY_HERE` with your real API keys. You can remove keys you don't use.

#### 2\. (Cursor-only) Enable Taskmaster MCP

Open Cursor Settings (Ctrl+Shift+J) ➡ Click on MCP tab on the left ➡ Enable task-master-ai with the toggle

#### 3\. (Optional) Configure the models you want to use

In your editor's AI chat pane, say:

```txt
Change the main, research and fallback models to <model_name>, <model_name> and <model_name> respectively.

```

For example, to use Claude Code (no API key required):

```txt
Change the main model to claude-code/sonnet

```

#### 4\. Initialize Taskmaster

In your editor's AI chat pane, say:

```txt
Initialize taskmaster-ai in my project

```

## Option 2: Using Command Line

## CLI Installation

```bash
# Install globally
npm install -g task-master-ai

# OR install locally within your project
npm install task-master-ai

```

## Initialize a new project

```bash
# If installed globally
task-master init

# If installed locally
npx task-master init

# Initialize project with specific rules
task-master init --rules cursor,windsurf,vscode

```

This will prompt you for project details and set up a new project with the necessary files and structure.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Quick Start","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start"},{"@type":"ListItem","position":6,"name":"Installation","item":"https://tryhamster.com/docs/taskmaster/getting-started/quick-start/installation"}]}
```
