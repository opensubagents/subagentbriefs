---
description: This document provides an overview of the MCP (Machine-to-Machine Communication Protocol) interface for the Taskmaster application.
title: MCP Tools | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

MCP Tools

* Welcome  
   * [Introduction](https://tryhamster.com/docs/taskmaster "Introduction")

* Getting Started

* Task Workflow

* Automation

* AI Providers

* IDE & Editor Setup

* Team Collaboration

* Best Practices

* TDD Workflow

* Technical Capabilities  
   * [MCP Tools](https://tryhamster.com/docs/taskmaster/capabilities/mcp "MCP Tools")  
   * [CLI Commands](https://tryhamster.com/docs/taskmaster/capabilities/cli-root-commands "CLI Commands")  
   * [Task Structure](https://tryhamster.com/docs/taskmaster/capabilities/task-structure "Task Structure")  
   * [Clusters](https://tryhamster.com/docs/taskmaster/capabilities/clusters "Clusters")

# MCP Tools

This document provides an overview of the MCP (Machine-to-Machine Communication Protocol) interface for the Task Master application. The MCP interface is defined in the `mcp-server/` directory and exposes the application's core functionalities as a set of tools that can be called remotely.

## Configurable Tool Loading

To optimize LLM context usage, you can control which Task Master MCP tools are loaded using the `TASK_MASTER_TOOLS` environment variable. This is particularly useful when working with LLMs that have context limits or when you only need a subset of tools.

### Configuration Modes

#### Core Tools (Default, Lean Mode)

Loads only 7 essential tools for daily development. Ideal for minimal context usage.

**Core tools included:**

* `get_tasks` — List all tasks
* `next_task` — Find the next task to work on
* `get_task` — Get detailed task information
* `set_task_status` — Update task status
* `update_subtask` — Add implementation notes
* `parse_prd` — Generate tasks from PRD
* `expand_task` — Break down tasks into subtasks

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "TASK_MASTER_TOOLS": "core",
        "ANTHROPIC_API_KEY": "your_key_here"
      }
    }
  }
}

```

You can also use `"lean"` as an alias for `"core"`. If `TASK_MASTER_TOOLS` is not set, core tools are loaded by default.

#### Standard Tools

Loads 15 commonly used tools. Balances functionality with context efficiency.

**Standard tools include all core tools plus:**

* `initialize_project` — Set up new projects
* `analyze_project_complexity` — Analyze task complexity
* `expand_all` — Expand all eligible tasks
* `add_subtask` — Add subtasks manually
* `remove_task` — Remove tasks
* `generate` — Generate task markdown files
* `add_task` — Create new tasks
* `complexity_report` — View complexity analysis

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "TASK_MASTER_TOOLS": "standard",
        "ANTHROPIC_API_KEY": "your_key_here"
      }
    }
  }
}

```

#### All Tools

Loads all 36 available tools. Use when you need full Task Master functionality.

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "TASK_MASTER_TOOLS": "all",
        "ANTHROPIC_API_KEY": "your_key_here"
      }
    }
  }
}

```

#### Custom Tool Selection

Specify exactly which tools to load using a comma-separated list. Tool names are case-insensitive and support both underscores and hyphens.

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "TASK_MASTER_TOOLS": "get_tasks,next_task,set_task_status,update_subtask",
        "ANTHROPIC_API_KEY": "your_key_here"
      }
    }
  }
}

```

### Choosing the Right Configuration

* **Use `core`/`lean`**: Default setting, ideal for basic task management workflows or when context limits are strict
* **Use `standard`**: For most development workflows that include task creation and analysis
* **Use `all`**: When you need full functionality including tag management, dependencies, and advanced features
* **Use custom list**: When you have specific tool requirements or want to experiment with minimal sets

### Verification

When the MCP server starts, it logs which tools were loaded:

```
Task Master MCP Server starting...
Tool mode configuration: standard
Loading standard tools
Registering 15 MCP tools (mode: standard)
Successfully registered 15/15 tools

```

## Core Concepts

The MCP interface is built on top of the `fastmcp` library and registers a set of tools that correspond to the core functionalities of the Taskmaster application. These tools are defined in the `mcp-server/src/tools/` directory and are registered with the MCP server in `mcp-server/src/tools/index.js`.

Each tool is defined with a name, a description, and a set of parameters that are validated using the `zod` library. The `execute` function of each tool calls the corresponding core logic function from `scripts/modules/task-manager.js`.

## Tool Categories

The MCP tools can be categorized in the same way as the core functionalities:

### 1\. Task and Subtask Management

* **`add_task`**: Creates a new task.
* **`add_subtask`**: Adds a subtask to a parent task.
* **`remove_task`**: Removes one or more tasks or subtasks.
* **`remove_subtask`**: Removes a subtask from its parent.
* **`update_task`**: Updates a single task.
* **`update_subtask`**: Appends information to a subtask.
* **`update`**: Updates multiple tasks.
* **`move_task`**: Moves a task or subtask.
* **`clear_subtasks`**: Clears all subtasks from one or more tasks.

### 2\. Task Information and Status

* **`get_tasks`**: Lists all tasks.
* **`get_task`**: Shows the details of a specific task.
* **`next_task`**: Shows the next task to work on.
* **`set_task_status`**: Sets the status of a task or subtask.

### 3\. Task Analysis and Expansion

* **`parse_prd`**: Parses a PRD to generate tasks.
* **`expand_task`**: Expands a task into subtasks.
* **`expand_all`**: Expands all eligible tasks.
* **`analyze_project_complexity`**: Analyzes task complexity.
* **`complexity_report`**: Displays the complexity analysis report.

### 4\. Dependency Management

* **`add_dependency`**: Adds a dependency to a task.
* **`remove_dependency`**: Removes a dependency from a task.
* **`validate_dependencies`**: Validates the dependencies of all tasks.
* **`fix_dependencies`**: Fixes any invalid dependencies.

### 5\. Project and Configuration

* **`initialize_project`**: Initializes a new project.
* **`generate`**: Generates individual task files.
* **`models`**: Manages AI model configurations.
* **`research`**: Performs AI-powered research.

### 6\. Tag Management

* **`add_tag`**: Creates a new tag.
* **`delete_tag`**: Deletes a tag.
* **`list_tags`**: Lists all tags.
* **`use_tag`**: Switches to a different tag.
* **`rename_tag`**: Renames a tag.
* **`copy_tag`**: Copies a tag.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Capabilities","item":"https://tryhamster.com/docs/taskmaster/capabilities"},{"@type":"ListItem","position":5,"name":"Mcp","item":"https://tryhamster.com/docs/taskmaster/capabilities/mcp"}]}
```
