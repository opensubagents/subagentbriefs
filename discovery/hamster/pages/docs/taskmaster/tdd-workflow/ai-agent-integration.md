---
description: Complete guide for integrating AI agents with the TaskMaster TDD workflow system. Learn how Hamster helps teams plan, build, and ship software faster...
title: AI Agent Integration | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

AI Agent Integration

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
   * [Quickstart](https://tryhamster.com/docs/taskmaster/tdd-workflow/quickstart "Quickstart")  
   * [AI Agent Integration](https://tryhamster.com/docs/taskmaster/tdd-workflow/ai-agent-integration "AI Agent Integration")

* Technical Capabilities

# AI Agent Integration Guide

## Overview

TaskMaster provides a complete TDD workflow orchestration system that enables AI agents to autonomously implement features following strict Test-Driven Development practices. The system manages workflow state, git operations, test validation, and progress tracking.

### Key Features

* **TDD State Machine**: Enforces RED -> GREEN -> COMMIT cycle
* **Git Integration**: Automated branch creation, commits with metadata
* **Test Validation**: Ensures RED phase has failures, GREEN phase passes
* **Progress Tracking**: Subtask completion, attempt counting, error logging
* **State Persistence**: Automatic workflow state management
* **Dual Interface**: CLI commands and MCP tools for flexibility

## Architecture

```
+-----------------------------------------------------+
|                   AI Agent                            |
|  (Claude Code, Custom Agent, etc.)                   |
+-------------+---------------------------------------+
              |
              | Uses CLI or MCP
              |
+-------------v---------------------------------------+
|            TaskMaster Interface                       |
|  +--------------+         +--------------+           |
|  | CLI Commands |         |  MCP Tools   |           |
|  +------+-------+         +------+-------+           |
+---------+------------------------+-------------------+
          |                        |
+---------v------------------------v-------------------+
|         WorkflowOrchestrator (Core)                  |
|  +---------------------------------------------+    |
|  |  State Machine: RED -> GREEN -> COMMIT       |    |
|  +---------------------------------------------+    |
|  +----------+  +----------+  +--------------+        |
|  |GitAdapter|  |TestResult|  |CommitMessage |        |
|  |          |  |Validator |  |Generator     |        |
|  +----------+  +----------+  +--------------+        |
+------------------------------------------------------+
          |
          | Persists to
          |
+---------v-----------------------------------------------+
|  .taskmaster/workflow-state.json                         |
+---------------------------------------------------------+

```

### Component Responsibilities

**WorkflowOrchestrator**

* Manages TDD state machine transitions
* Tracks current subtask and progress
* Enforces workflow rules and validations
* Emits events for state changes

**GitAdapter**

* Creates and manages workflow branches
* Stages files and creates commits
* Validates git repository state
* Provides safety checks (clean working tree, etc.)

**TestResultValidator**

* Validates RED phase has test failures
* Validates GREEN phase has all tests passing
* Parses test results from various formats

**CommitMessageGenerator**

* Generates conventional commit messages
* Embeds workflow metadata (subtask ID, phase, etc.)
* Follows project commit conventions

## Getting Started

### Prerequisites

1. TaskMaster initialized project with subtasks
2. Git repository with clean working tree
3. Test framework configured (vitest, jest, etc.)

### Quick Start

```bash
# 1. Initialize workflow for a task
tm autopilot start 7

# 2. Check what to do next
tm autopilot next

# 3. Write failing test (RED phase)
# ... create test file ...

# 4. Run tests and complete RED phase
tm autopilot complete --results '{"total":1,"passed":0,"failed":1,"skipped":0}'

# 5. Implement code to pass tests (GREEN phase)
# ... write implementation ...

# 6. Run tests and complete GREEN phase
tm autopilot complete --results '{"total":1,"passed":1,"failed":0,"skipped":0}'

# 7. Commit changes
tm autopilot commit

# 8. Repeat for next subtask (automatically advanced)
tm autopilot next

```

## CLI Commands

All commands support `--json` flag for machine-readable output.

### `tm autopilot start <taskId>`

Initialize a new TDD workflow for a task.

**Options:**

* `--max-attempts <number>`: Maximum attempts per subtask (default: 3)
* `--force`: Force start even if workflow exists
* `--project-root <path>`: Project root directory
* `--json`: Output JSON

**Example:**

```bash
tm autopilot start 7 --max-attempts 5 --json

```

**JSON Output:**

```json
{
  "success": true,
  "message": "Workflow started for task 7",
  "taskId": "7",
  "branchName": "task-7",
  "phase": "SUBTASK_LOOP",
  "tddPhase": "RED",
  "progress": {
    "completed": 0,
    "total": 5,
    "percentage": 0
  },
  "currentSubtask": {
    "id": "1",
    "title": "Implement start command",
    "status": "in-progress",
    "attempts": 0
  },
  "nextAction": "generate_test"
}

```

### `tm autopilot resume`

Resume a previously started workflow from saved state.

```bash
tm autopilot resume --json

```

### `tm autopilot next`

Get the next action to perform with detailed context.

**JSON Output:**

```json
{
  "action": "generate_test",
  "actionDescription": "Write a failing test for the current subtask",
  "phase": "SUBTASK_LOOP",
  "tddPhase": "RED",
  "taskId": "7",
  "branchName": "task-7",
  "progress": {
    "completed": 0,
    "total": 5,
    "current": 1,
    "percentage": 0
  },
  "currentSubtask": {
    "id": "1",
    "title": "Implement start command",
    "status": "in-progress",
    "attempts": 0,
    "maxAttempts": 3
  },
  "expectedFiles": ["test file"],
  "context": {
    "canProceed": false,
    "errors": []
  }
}

```

### `tm autopilot status`

Get comprehensive workflow progress and state information.

```bash
tm autopilot status --json

```

### `tm autopilot complete`

Complete the current TDD phase with test result validation.

**Options:**

* `--results <json>`: Test results JSON string

**Example:**

```bash
tm autopilot complete --results '{"total":10,"passed":9,"failed":1,"skipped":0}' --json

```

**Validation Rules:**

* **RED Phase**: Must have at least one failing test
* **GREEN Phase**: All tests must pass (failed === 0)

### `tm autopilot commit`

Create a git commit with enhanced message generation.

**Options:**

* `--message <text>`: Custom commit message (optional)
* `--files <paths...>`: Specific files to stage (optional)

```bash
tm autopilot commit --json

```

### `tm autopilot abort`

Abort the workflow and clean up state (preserves git branch and code).

```bash
tm autopilot abort --force --json

```

## MCP Tools

MCP tools provide the same functionality as CLI commands for programmatic integration.

### `autopilot_start`

**Parameters:**

```typescript
{
  taskId: string;          // Required: Task ID (e.g., "7", "2.3")
  projectRoot: string;     // Required: Absolute path to project
  tag?: string;            // Optional: Tag context
  maxAttempts?: number;    // Optional: Default 3
  force?: boolean;         // Optional: Default false
}

```

**Returns:**

```typescript
{
  success: boolean;
  message: string;
  taskId: string;
  branchName: string;
  phase: WorkflowPhase;
  tddPhase: TDDPhase;
  progress: {
    completed: number;
    total: number;
    percentage: number;
  };
  currentSubtask: SubtaskInfo | null;
  nextAction: string;
}

```

### `autopilot_resume`

**Parameters:**

```typescript
{
  projectRoot: string;  // Required: Absolute path to project
}

```

### `autopilot_next`

**Parameters:**

```typescript
{
  projectRoot: string;  // Required: Absolute path to project
}

```

**Returns:**

```typescript
{
  action: string;              // 'generate_test' | 'implement_code' | 'commit_changes'
  actionDescription: string;
  phase: WorkflowPhase;
  tddPhase: TDDPhase;
  taskId: string;
  branchName: string;
  progress: ProgressInfo;
  currentSubtask: SubtaskInfo | null;
  expectedFiles: string[];
  context: {
    canProceed: boolean;
    errors: string[];
  };
}

```

### `autopilot_status`

**Parameters:**

```typescript
{
  projectRoot: string;  // Required: Absolute path to project
}

```

**Returns:**

```typescript
{
  taskId: string;
  branchName: string;
  phase: WorkflowPhase;
  tddPhase: TDDPhase;
  progress: ProgressInfo;
  currentSubtask: SubtaskInfo | null;
  subtasks: SubtaskInfo[];
  errors: string[];
  metadata: Record<string, any>;
  canProceed: boolean;
}

```

### `autopilot_complete_phase`

**Parameters:**

```typescript
{
  projectRoot: string;  // Required: Absolute path to project
  testResults: {
    total: number;      // Required: Total tests
    passed: number;     // Required: Passing tests
    failed: number;     // Required: Failing tests
    skipped?: number;   // Optional: Skipped tests
  };
}

```

### `autopilot_commit`

**Parameters:**

```typescript
{
  projectRoot: string;     // Required: Absolute path to project
  files?: string[];        // Optional: Files to stage
  customMessage?: string;  // Optional: Custom commit message
}

```

### `autopilot_abort`

**Parameters:**

```typescript
{
  projectRoot: string;  // Required: Absolute path to project
}

```

## Workflow Phases

### Phase Diagram

```
PREFLIGHT -> BRANCH_SETUP -> SUBTASK_LOOP -> FINALIZE -> COMPLETE
                                   |
                          RED -> GREEN -> COMMIT
                           ^              |
                           +--------------+
                             (Next Subtask)

```

### Phase Descriptions

**PREFLIGHT**

* Validate task has subtasks
* Check git repository state
* Verify preconditions

**BRANCH\_SETUP**

* Create workflow branch: `task-{taskId}`
* Checkout new branch
* Initialize workflow context

**SUBTASK\_LOOP**

* **RED Phase**: Write failing tests  
   * Action: `generate_test`  
   * Validation: At least one test must fail  
   * Files: Test files
* **GREEN Phase**: Implement code  
   * Action: `implement_code`  
   * Validation: All tests must pass  
   * Files: Implementation files
* **COMMIT Phase**: Create commit  
   * Action: `commit_changes`  
   * Auto-generates commit message  
   * Advances to next subtask

**FINALIZE**

* All subtasks complete
* Workflow ready for review/merge

**COMPLETE**

* Workflow finished
* State can be cleaned up

## Responsibility Matrix

| Responsibility            | AI Agent                       | TaskMaster           |
| ------------------------- | ------------------------------ | -------------------- |
| Start/resume workflow     | Call CLI/MCP                   | Execute and validate |
| Track workflow state      | Read state                     | Persist state        |
| Manage TDD phases         | Request transitions            | Enforce transitions  |
| Validate phase completion | RED must fail, GREEN must pass |                      |
| Write test code           | Yes                            |                      |
| Run tests                 | Yes                            |                      |
| Parse test output         | Yes                            |                      |
| Report test results       | Provide JSON                   | Validate results     |
| Write implementation code | Yes                            |                      |
| Ensure tests pass         | Yes                            |                      |
| Follow TDD cycle          | Yes (guided)                   | Enforce rules        |
| Create workflow branch    | Request                        | Execute              |
| Stage files               | Request (optional)             | Execute              |
| Generate commit messages  | Yes                            |                      |
| Create commits            | Request                        | Execute              |
| Query progress            | Call status                    | Provide data         |
| Advance subtasks          | Automatic on commit            |                      |
| Count attempts            | Yes                            |                      |
| Log activity              | Yes                            |                      |

## Examples

### Complete TDD Cycle Example

#### 1\. Start Workflow

```bash
$ tm autopilot start 7 --json

```

```json
{
  "success": true,
  "taskId": "7",
  "branchName": "task-7",
  "tddPhase": "RED",
  "currentSubtask": {
    "id": "1",
    "title": "Implement start command",
    "status": "in-progress"
  },
  "nextAction": "generate_test"
}

```

#### 2\. Get Next Action

```bash
$ tm autopilot next --json

```

```json
{
  "action": "generate_test",
  "actionDescription": "Write a failing test for the current subtask",
  "tddPhase": "RED",
  "currentSubtask": {
    "id": "1",
    "title": "Implement start command"
  }
}

```

#### 3\. Write Failing Test

AI Agent creates `tests/start.test.ts`:

```typescript
import { describe, it, expect } from 'vitest';
import { StartCommand } from '../src/commands/start.js';

describe('StartCommand', () => {
  it('should initialize workflow and create branch', async () => {
    const command = new StartCommand();
    const result = await command.execute({ taskId: '7' });
    expect(result.success).toBe(true);
    expect(result.branchName).toBe('task-7');
  });
});

```

#### 4\. Run Tests (Should Fail)

```bash
$ npm test
# Output: 1 test failed (expected)

```

#### 5\. Complete RED Phase

```bash
$ tm autopilot complete --results '{"total":1,"passed":0,"failed":1,"skipped":0}' --json

```

```json
{
  "success": true,
  "message": "Completed RED phase",
  "previousPhase": "RED",
  "currentPhase": "GREEN",
  "nextAction": "implement_code"
}

```

#### 6\. Implement Code

AI Agent creates `src/commands/start.ts`:

```typescript
export class StartCommand {
  async execute(options: { taskId: string }) {
    return {
      success: true,
      branchName: `task-${options.taskId}`
    };
  }
}

```

#### 7\. Run Tests (Should Pass)

```bash
$ npm test
# Output: 1 test passed

```

#### 8\. Complete GREEN Phase

```bash
$ tm autopilot complete --results '{"total":1,"passed":1,"failed":0,"skipped":0}' --json

```

```json
{
  "success": true,
  "previousPhase": "GREEN",
  "currentPhase": "COMMIT",
  "nextAction": "commit_changes"
}

```

#### 9\. Commit Changes

```bash
$ tm autopilot commit --json

```

```json
{
  "success": true,
  "commit": {
    "hash": "abc123",
    "message": "feat(autopilot): implement start command (Task 7.1)\n\n..."
  },
  "subtaskCompleted": "1",
  "currentSubtask": {
    "id": "2",
    "title": "Implement resume command"
  },
  "nextAction": "generate_test"
}

```

### MCP Integration Example

```typescript
// AI Agent using MCP tools

async function implementTask(taskId: string) {
  // Start workflow
  const start = await mcp.call('autopilot_start', {
    taskId,
    projectRoot: '/path/to/project'
  });

  while (true) {
    // Get next action
    const next = await mcp.call('autopilot_next', {
      projectRoot: '/path/to/project'
    });

    if (next.action === 'generate_test') {
      // AI generates test
      const testCode = await generateTest(next.currentSubtask);
      await writeFile(testCode);

      // Run tests
      const results = await runTests();

      // Complete RED phase
      await mcp.call('autopilot_complete_phase', {
        projectRoot: '/path/to/project',
        testResults: results
      });

    } else if (next.action === 'implement_code') {
      // AI generates implementation
      const implCode = await generateImplementation(next.currentSubtask);
      await writeFile(implCode);

      // Run tests
      const results = await runTests();

      // Complete GREEN phase
      await mcp.call('autopilot_complete_phase', {
        projectRoot: '/path/to/project',
        testResults: results
      });

    } else if (next.action === 'commit_changes') {
      // Commit
      const commit = await mcp.call('autopilot_commit', {
        projectRoot: '/path/to/project'
      });

      if (commit.isComplete) {
        break;
      }
    }
  }
}

```

## Error Handling

### Common Errors and Solutions

#### Workflow Already Exists

```json
{
  "error": "Workflow already in progress",
  "suggestion": "Use autopilot_resume to continue the existing workflow"
}

```

**Solution:**

```bash
# Resume existing workflow
tm autopilot resume

# OR force start new workflow
tm autopilot start 7 --force

```

#### RED Phase Validation Failed

```json
{
  "error": "RED phase validation failed",
  "reason": "At least one test must be failing in RED phase",
  "actual": { "passed": 10, "failed": 0 },
  "suggestion": "Ensure you have written a failing test before proceeding"
}

```

**Solution:** The test isn't actually testing the new feature. Write a test that validates the new behavior that doesn't exist yet.

#### GREEN Phase Validation Failed

```json
{
  "error": "GREEN phase validation failed",
  "reason": "All tests must pass in GREEN phase",
  "actual": { "passed": 9, "failed": 1 },
  "suggestion": "Fix the implementation to make all tests pass"
}

```

**Solution:** Implementation isn't complete. Debug failing test and fix implementation.

#### No Staged Changes

```json
{
  "error": "No staged changes to commit",
  "suggestion": "Make code changes before committing"
}

```

**Solution:** Ensure you've actually created/modified files before committing.

#### Git Working Tree Not Clean

```json
{
  "error": "Git validation failed: working tree not clean",
  "suggestion": "Commit or stash changes before starting workflow"
}

```

**Solution:**

```bash
git status
git add . && git commit -m "chore: save work"
# Then start workflow

```

## Troubleshooting

### Workflow State Issues

**Problem:** State file corrupted or inconsistent

**Solution:**

```bash
# Check state file
cat .taskmaster/workflow-state.json

# If corrupted, abort and restart
tm autopilot abort --force
tm autopilot start 7

```

### Test Results Parsing

**Problem:** Test output format not recognized

**Solution:** Ensure test results JSON has required fields:

```json
{
  "total": 10,
  "passed": 8,
  "failed": 2,
  "skipped": 0
}

```

### Branch Conflicts

**Problem:** Workflow branch already exists

**Solution:**

```bash
# Check branches
git branch

# Delete old workflow branch if safe
git branch -D task-7

# Start workflow again
tm autopilot start 7

```

### Permission Issues

**Problem:** Cannot write to .taskmaster directory

**Solution:**

```bash
# Check directory permissions
ls -la .taskmaster/

# Fix permissions
chmod -R u+w .taskmaster/

```

## Working with AI Agents

Example prompts for AI agents (Claude Code, Cursor, etc.) to use the TDD workflow.

### Starting a Task

```
I want to implement Task 7 using TDD workflow. Please:
1. Start the autopilot workflow
2. Show me the first subtask to implement
3. Begin the RED-GREEN-COMMIT cycle

```

### RED Phase — Writing Failing Tests

```
We're in RED phase for subtask "{SUBTASK_TITLE}". Please:
1. Read the subtask requirements
2. Write a test that validates the behavior
3. The test MUST fail because the feature doesn't exist yet
4. Run the tests and report results to complete the RED phase

```

### GREEN Phase — Implementing

```
We're in GREEN phase. The test is failing with: {ERROR_MESSAGE}

Please:
1. Implement the minimal code to make this test pass
2. Don't over-engineer or add untested features
3. Run tests and report results to complete the GREEN phase

```

### Handling Errors

```
The RED phase validation failed - no test failures detected.

Please:
1. Review the test I just wrote
2. Identify why it's not actually testing new behavior
3. Rewrite the test to properly fail until the feature is implemented

```

### Checking Progress

```
What's the current state of the workflow? Please show:
- Which subtask we're on
- Current TDD phase (RED/GREEN/COMMIT)
- Progress percentage
- Next action required

```

### Resuming Work

```
I have an in-progress workflow. Please:
1. Resume the autopilot workflow
2. Show current status
3. Continue from where we left off

```

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Tdd Workflow","item":"https://tryhamster.com/docs/taskmaster/tdd-workflow"},{"@type":"ListItem","position":5,"name":"Ai Agent Integration","item":"https://tryhamster.com/docs/taskmaster/tdd-workflow/ai-agent-integration"}]}
```
