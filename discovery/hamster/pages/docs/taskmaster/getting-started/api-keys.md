---
description: Set up API keys for Taskmaster. Learn how Hamster helps teams plan, build, and ship software faster with AI agents and clear execution workflows.
title: API Keys | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

API Keys

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

# API Keys Configuration

Taskmaster supports multiple AI providers through environment variables. This page lists all available API keys and their configuration requirements.

## Required API Keys

> **Note**: At least one required API key must be configured for Taskmaster to function.
> 
> "Required: Yes" below means "required to use that specific provider," not "required globally." You only need at least one provider configured.

### ANTHROPIC\_API\_KEY (Recommended)

* **Provider**: Anthropic Claude models
* **Format**: `sk-ant-api03-...`
* **Required**: Yes
* **Models**: Claude 3.5 Sonnet, Claude 3 Haiku, Claude 3 Opus
* **Get Key**: [Anthropic Console](https://console.anthropic.com/)

```bash
ANTHROPIC_API_KEY="sk-ant-api03-your-key-here"

```

### PERPLEXITY\_API\_KEY (Highly Recommended for Research)

* **Provider**: Perplexity AI (Research features)
* **Format**: `pplx-...`
* **Required**: Yes
* **Purpose**: Enables research-backed task expansions and updates
* **Models**: Perplexity Sonar models
* **Get Key**: [Perplexity API](https://www.perplexity.ai/settings/api)

```bash
PERPLEXITY_API_KEY="pplx-your-key-here"

```

### OPENAI\_API\_KEY

* **Provider**: OpenAI GPT models
* **Format**: `sk-proj-...` or `sk-...`
* **Required**: Yes
* **Models**: GPT-4, GPT-4 Turbo, GPT-3.5 Turbo, O1 models
* **Get Key**: [OpenAI Platform](https://platform.openai.com/api-keys)

```bash
OPENAI_API_KEY="sk-proj-your-key-here"

```

### GOOGLE\_API\_KEY

* **Provider**: Google Gemini models
* **Format**: Various formats
* **Required**: Yes
* **Models**: Gemini Pro, Gemini Flash, Gemini Ultra
* **Get Key**: [Google AI Studio](https://aistudio.google.com/app/apikey)
* **Alternative**: Use `GOOGLE_APPLICATION_CREDENTIALS` for service account (Google Vertex)

```bash
GOOGLE_API_KEY="your-google-api-key-here"

```

### GROQ\_API\_KEY

* **Provider**: Groq (High-performance inference)
* **Required**: Yes
* **Models**: Llama models, Mixtral models (via Groq)
* **Get Key**: [Groq Console](https://console.groq.com/keys)

```bash
GROQ_API_KEY="your-groq-key-here"

```

### OPENROUTER\_API\_KEY

* **Provider**: OpenRouter (Multiple model access)
* **Required**: Yes
* **Models**: Access to various models through single API
* **Get Key**: [OpenRouter](https://openrouter.ai/keys)

```bash
OPENROUTER_API_KEY="your-openrouter-key-here"

```

### AZURE\_OPENAI\_API\_KEY

* **Provider**: Azure OpenAI Service
* **Required**: Yes
* **Requirements**: Also requires `AZURE_OPENAI_ENDPOINT` configuration
* **Models**: GPT models via Azure
* **Get Key**: [Azure Portal](https://portal.azure.com/)

```bash
AZURE_OPENAI_API_KEY="your-azure-key-here"

```

### XAI\_API\_KEY

* **Provider**: xAI (Grok) models
* **Required**: Yes
* **Models**: Grok models
* **Get Key**: [xAI Console](https://console.x.ai/)

```bash
XAI_API_KEY="your-xai-key-here"

```

## Optional API Keys

> **Note**: These API keys are optional - providers will work without them or use alternative authentication methods.

### AWS\_ACCESS\_KEY\_ID (Bedrock)

* **Provider**: AWS Bedrock
* **Required**: No (uses AWS credential chain)
* **Models**: Claude models via AWS Bedrock
* **Authentication**: Uses AWS credential chain (profiles, IAM roles, etc.)
* **Get Key**: [AWS Console](https://console.aws.amazon.com/iam/)

```bash
# Optional - AWS credential chain is preferred
AWS_ACCESS_KEY_ID="your-aws-access-key"
AWS_SECRET_ACCESS_KEY="your-aws-secret-key"

```

### CLAUDE\_CODE\_API\_KEY

* **Provider**: Claude Code CLI
* **Required**: No (uses OAuth tokens)
* **Purpose**: Integration with local Claude Code CLI
* **Authentication**: Uses OAuth tokens, no API key needed

```bash
# Not typically needed
CLAUDE_CODE_API_KEY="not-usually-required"

```

### GEMINI\_API\_KEY

* **Provider**: Gemini CLI
* **Required**: No (uses OAuth authentication)
* **Purpose**: Integration with Gemini CLI
* **Authentication**: Primarily uses OAuth via CLI, API key is optional

```bash
# Optional - OAuth via CLI is preferred
GEMINI_API_KEY="your-gemini-key-here"

```

### GROK\_CLI\_API\_KEY

* **Provider**: Grok CLI
* **Required**: No (can use CLI config)
* **Purpose**: Integration with Grok CLI
* **Authentication**: Can use Grok CLI's own config file

```bash
# Optional - CLI config is preferred
GROK_CLI_API_KEY="your-grok-cli-key"

```

### OLLAMA\_API\_KEY

* **Provider**: Ollama (Local/Remote)
* **Required**: No (local installation doesn't need key)
* **Purpose**: For remote Ollama servers that require authentication
* **Requirements**: Only needed for remote servers with authentication
* **Note**: Not needed for local Ollama installations

```bash
# Only needed for remote Ollama servers
OLLAMA_API_KEY="your-ollama-api-key-here"

```

### GITHUB\_API\_KEY

* **Provider**: GitHub (Import/Export features)
* **Format**: `ghp_...` or `github_pat_...`
* **Required**: No (for GitHub features only)
* **Purpose**: GitHub import/export features
* **Get Key**: [GitHub Settings](https://github.com/settings/tokens)

```bash
GITHUB_API_KEY="ghp-your-github-key-here"

```

## Configuration Methods

### Method 1: Environment File (.env)

Create a `.env` file in your project root:

```bash
# Copy from .env.example
cp .env.example .env

# Edit with your keys
vim .env

```

### Method 2: System Environment Variables

```bash
export ANTHROPIC_API_KEY="your-key-here"
export PERPLEXITY_API_KEY="your-key-here"
# ... other keys

```

### Method 3: MCP Server Configuration

For Claude Code integration, configure keys in `.mcp.json`:

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "ANTHROPIC_API_KEY": "your-key-here",
        "PERPLEXITY_API_KEY": "your-key-here",
        "OPENAI_API_KEY": "your-key-here"
      }
    }
  }
}

```

## Key Requirements

### Minimum Requirements

* **At least one** AI provider key is required
* **ANTHROPIC\_API\_KEY** is recommended as the primary provider
* **PERPLEXITY\_API\_KEY** is highly recommended for research features

### Provider-Specific Requirements

* **Azure OpenAI**: Requires both `AZURE_OPENAI_API_KEY` and `AZURE_OPENAI_ENDPOINT` configuration
* **Google Vertex**: Requires `VERTEX_PROJECT_ID` and `VERTEX_LOCATION` environment variables
* **AWS Bedrock**: Uses AWS credential chain (profiles, IAM roles, etc.) instead of API keys
* **Ollama**: Only needs API key for remote servers with authentication
* **CLI Providers**: Gemini CLI, Grok CLI, and Claude Code use OAuth/CLI config instead of API keys

## Model Configuration

After setting up API keys, configure which models to use:

```bash
# Interactive model setup
task-master models --setup

# Set specific models
task-master models --set-main claude-3-5-sonnet-20241022
task-master models --set-research perplexity-llama-3.1-sonar-large-128k-online
task-master models --set-fallback gpt-4o-mini

```

## Security Best Practices

1. Never commit API keys to version control
2. Use .env files and add them to `.gitignore`
3. Rotate keys regularly especially if compromised
4. Use minimal permissions for service accounts
5. Monitor usage to detect unauthorized access

## Troubleshooting

### Key Validation

```bash
# Check if keys are properly configured
task-master models

# Test specific provider
task-master add-task --prompt="test task" --model=claude-3-5-sonnet-20241022

```

### Common Issues

* **Invalid key format**: Check the expected format for each provider
* **Insufficient permissions**: Ensure keys have necessary API access
* **Rate limits**: Some providers have usage limits
* **Regional restrictions**: Some models may not be available in all regions

### Getting Help

If you encounter issues with API key configuration:

* Check the [FAQ](https://tryhamster.com/docs/taskmaster/getting-started/faq) for common solutions
* Join our [Discord community](https://discord.gg/fWJkU7rf) for support
* Report issues on [GitHub](https://github.com/eyaltoledano/claude-task-master/issues)

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Getting Started","item":"https://tryhamster.com/docs/taskmaster/getting-started"},{"@type":"ListItem","position":5,"name":"Api Keys","item":"https://tryhamster.com/docs/taskmaster/getting-started/api-keys"}]}
```
