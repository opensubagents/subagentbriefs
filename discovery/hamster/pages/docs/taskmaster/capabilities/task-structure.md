---
description: Tasks in Taskmaster follow a specific format designed to provide comprehensive information for both humans and AI assistants.
title: Task Structure | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Task Structure

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

# Task Structure

## Task Fields in tasks.json

Tasks in tasks.json have the following structure:

| Field        | Description                               | Example                                              |
| ------------ | ----------------------------------------- | ---------------------------------------------------- |
| id           | Unique identifier for the task.           | 1                                                    |
| title        | Brief, descriptive title.                 | "Initialize Repo"                                    |
| description  | What the task involves.                   | "Create a new repository, set up initial structure." |
| status       | Current state.                            | "pending", "done", "deferred"                        |
| dependencies | Prerequisite task IDs.                    | \[1, 2\]                                             |
| priority     | Task importance.                          | "high", "medium", "low"                              |
| details      | Implementation instructions.              | "Use GitHub client ID/secret, handle callback..."    |
| testStrategy | How to verify success.                    | "Deploy and confirm 'Hello World' response."         |
| subtasks     | Nested subtasks related to the main task. | \[{"id": 1, "title": "Configure OAuth", ...}\]       |
| metadata     | Optional user-defined data (see below).   | {"githubIssue": 42, "sprint": "Q1-S3"}               |

## Task File Format

Individual task files follow this format:

```text
# Task ID: <id>
# Title: <title>
# Status: <status>
# Dependencies: <comma-separated list of dependency IDs>
# Priority: <priority>
# Description: <brief description>
# Details:
<detailed implementation notes>

# Test Strategy:
<verification approach>

```

## User-Defined Metadata Field

The `metadata` field allows you to store arbitrary custom data on tasks without requiring schema changes. This is useful for:

* **External IDs**: Link tasks to GitHub issues, Jira tickets, Linear issues, etc.
* **Workflow data**: Track sprints, story points, custom statuses
* **Integration data**: Store sync timestamps, external system references
* **Custom tracking**: UUIDs, version numbers, audit information

### Key Characteristics

**Fully Optional** — The field is optional. Existing tasks work without it.

**AI-Safe** — AI operations preserve your metadata — it's never overwritten by AI.

**Flexible Schema** — Store any JSON-serializable data: strings, numbers, objects, arrays.

**Subtask Support** — Both tasks and subtasks can have their own metadata.

### Usage Examples

**GitHub Issue Linking**

```json
{
  "id": 1,
  "title": "Implement authentication",
  "metadata": {
    "githubIssue": 42,
    "githubIssueUrl": "https://github.com/org/repo/issues/42"
  }
}

```

**Sprint & Project Management**

```json
{
  "id": 2,
  "title": "Refactor API endpoints",
  "metadata": {
    "sprint": "Q1-S3",
    "storyPoints": 5,
    "epic": "API Modernization"
  }
}

```

**External System Integration**

```json
{
  "id": 3,
  "title": "Fix login bug",
  "metadata": {
    "jira": {
      "key": "PROJ-123",
      "type": "bug",
      "priority": "P1"
    },
    "importedAt": "2024-01-15T10:30:00Z",
    "lastSyncedAt": "2024-01-20T14:00:00Z"
  }
}

```

**Stable UUID Tracking**

```json
{
  "id": 4,
  "title": "Add user preferences",
  "metadata": {
    "uuid": "550e8400-e29b-41d4-a716-446655440000",
    "version": 2,
    "createdBy": "import-script"
  }
}

```

### Security Warning

> **Do not store secrets, API keys, or sensitive credentials in the metadata field.** Task data may be visible in logs, exports, or shared with AI providers.

### Metadata Behavior

| Operation       | Metadata Behavior                                            |
| --------------- | ------------------------------------------------------------ |
| parse-prd       | New tasks are created without metadata                       |
| update-task     | Existing metadata is preserved unless explicitly changed     |
| expand          | Parent task metadata is preserved; subtasks don't inherit it |
| update-subtask  | Subtask metadata is preserved                                |
| Manual edit     | You can add/modify metadata directly in tasks.json           |
| MCP (with flag) | Use the metadata parameter to explicitly update metadata     |

### Updating Metadata via MCP

The `update_task` and `update_subtask` MCP tools support a `metadata` parameter for updating task metadata. This feature is disabled by default for safety.

**To enable MCP metadata updates:**

Add `TASK_MASTER_ALLOW_METADATA_UPDATES=true` to your MCP server environment configuration in `.mcp.json`:

```json
{
  "mcpServers": {
    "task-master-ai": {
      "command": "npx",
      "args": ["-y", "task-master-ai"],
      "env": {
        "TASK_MASTER_ALLOW_METADATA_UPDATES": "true",
        "ANTHROPIC_API_KEY": "your_key_here"
      }
    }
  }
}

```

**Usage example:**

```javascript
// Update task metadata (merges with existing)
update_task({
  id: "1",
  projectRoot: "/path/to/project",
  metadata: '{"githubIssue": 42, "sprint": "Q1-S3"}'
})

// Update only metadata (no prompt required)
update_task({
  id: "1",
  projectRoot: "/path/to/project",
  metadata: '{"status": "reviewed"}'
})

```

The `metadata` parameter accepts a JSON string. The new metadata is merged with existing metadata, allowing you to update specific fields without losing others.

## Features in Detail

### Analyzing Task Complexity

The `analyze-complexity` command:

* Analyzes each task using AI to assess its complexity on a scale of 1-10
* Recommends optimal number of subtasks based on configured DEFAULT\_SUBTASKS
* Generates tailored prompts for expanding each task
* Creates a comprehensive JSON report with ready-to-use commands
* Saves the report to scripts/task-complexity-report.json by default

The generated report contains:

* Complexity analysis for each task (scored 1-10)
* Recommended number of subtasks based on complexity
* AI-generated expansion prompts customized for each task
* Ready-to-run expansion commands directly within each task analysis

### Viewing Complexity Report

The `complexity-report` command:

* Displays a formatted, easy-to-read version of the complexity analysis report
* Shows tasks organized by complexity score (highest to lowest)
* Provides complexity distribution statistics (low, medium, high)
* Highlights tasks recommended for expansion based on threshold score
* Includes ready-to-use expansion commands for each complex task
* If no report exists, offers to generate one on the spot

### Smart Task Expansion

The `expand` command automatically checks for and uses the complexity report:

When a complexity report exists:

* Tasks are automatically expanded using the recommended subtask count and prompts
* When expanding all tasks, they're processed in order of complexity (highest first)
* Research-backed generation is preserved from the complexity analysis
* You can still override recommendations with explicit command-line options

Example workflow:

```bash
# Generate the complexity analysis report with research capabilities
task-master analyze-complexity --research

# Review the report in a readable format
task-master complexity-report

# Expand tasks using the optimized recommendations
task-master expand --id=8
# or expand all tasks
task-master expand --all

```

### Finding the Next Task

The `next` command:

* Identifies tasks that are pending/in-progress and have all dependencies satisfied
* Prioritizes tasks by priority level, dependency count, and task ID
* Displays comprehensive information about the selected task:  
   * Basic task details (ID, title, priority, dependencies)  
   * Implementation details  
   * Subtasks (if they exist)
* Provides contextual suggested actions:  
   * Command to mark the task as in-progress  
   * Command to mark the task as done  
   * Commands for working with subtasks

### Viewing Specific Task Details

The `show` command:

* Displays comprehensive details about a specific task or subtask
* Shows task status, priority, dependencies, and detailed implementation notes
* For parent tasks, displays all subtasks and their status
* For subtasks, shows parent task relationship
* Provides contextual action suggestions based on the task's state
* Works with both regular tasks and subtasks (using the format taskId.subtaskId)

## Best Practices for AI-Driven Development

1. Detailed PRD — The more detailed your PRD, the better the generated tasks will be.
2. Review Tasks — After parsing the PRD, review the tasks to ensure they make sense and have appropriate dependencies.
3. Analyze Complexity — Use the complexity analysis feature to identify which tasks should be broken down further.
4. Follow Dependencies — Always respect task dependencies — the Cursor agent will help with this.
5. Update As You Go — If your implementation diverges from the plan, use the update command to keep future tasks aligned.
6. Break Down Tasks — Use the expand command to break down complex tasks into manageable subtasks.
7. Regenerate Files — After any updates to tasks.json, regenerate the task files to keep them in sync.
8. Provide Context — When asking the Cursor agent to help with a task, provide context about what you're trying to achieve.
9. Validate Dependencies — Periodically run the validate-dependencies command to check for invalid or circular dependencies.

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Capabilities","item":"https://tryhamster.com/docs/taskmaster/capabilities"},{"@type":"ListItem","position":5,"name":"Task Structure","item":"https://tryhamster.com/docs/taskmaster/capabilities/task-structure"}]}
```
