---
description: Get started with the autonomous TDD workflow using tm autopilot commands. Learn how Hamster helps teams plan, build, and ship software faster with AI...
title: TDD Workflow Quick Start | Hamster
image: https://tryhamster.com/opengraph-image
---

[Sign In](https://tryhamster.com/auth/sign-in)[Get started free](https://tryhamster.com/auth/sign-up)

[Sign In](https://tryhamster.com/auth/sign-in)[Get Started](https://tryhamster.com/auth/sign-up)

Quickstart

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

# TDD Workflow Quick Start

## Prerequisites

* TaskMaster initialized project (`tm init`)
* Tasks with subtasks created (`tm parse-prd` or `tm expand`)
* Git repository with clean working tree
* Test framework installed (vitest, jest, mocha, etc.)

## 1\. Start a Workflow

```bash
tm autopilot start <taskId>

```

Example:

```bash
$ tm autopilot start 7

✓ Workflow started for task 7
✓ Created branch: task-7
✓ Current phase: RED
✓ Subtask 1/5: Implement start command
→ Next action: Write a failing test

```

## 2\. The TDD Cycle

### RED Phase: Write Failing Test

```bash
# Check what to do next
$ tm autopilot next --json
{
  "action": "generate_test",
  "currentSubtask": {
    "id": "1",
    "title": "Implement start command"
  }
}

```

Write a test that fails:

```typescript
// tests/start.test.ts
import { describe, it, expect } from 'vitest';
import { StartCommand } from '../src/commands/start';

describe('StartCommand', () => {
  it('should initialize workflow', async () => {
    const command = new StartCommand();
    const result = await command.execute({ taskId: '7' });
    expect(result.success).toBe(true);
  });
});

```

Run tests:

```bash
$ npm test
# ✗ 1 test failed

```

Complete RED phase:

```bash
$ tm autopilot complete --results '{"total":1,"passed":0,"failed":1,"skipped":0}'

✓ RED phase complete
✓ Current phase: GREEN
→ Next action: Implement code to pass tests

```

### GREEN Phase: Implement Feature

Write minimal code to pass:

```typescript
// src/commands/start.ts
export class StartCommand {
  async execute(options: { taskId: string }) {
    return { success: true };
  }
}

```

Run tests:

```bash
$ npm test
# ✓ 1 test passed

```

Complete GREEN phase:

```bash
$ tm autopilot complete --results '{"total":1,"passed":1,"failed":0,"skipped":0}'

✓ GREEN phase complete
✓ Current phase: COMMIT
→ Next action: Commit changes

```

### COMMIT Phase: Save Progress

```bash
$ tm autopilot commit

✓ Created commit: abc123
✓ Message: feat(autopilot): implement start command (Task 7.1)
✓ Advanced to subtask 2/5
✓ Current phase: RED
→ Next action: Write a failing test

```

## 3\. Continue for All Subtasks

Repeat the RED-GREEN-COMMIT cycle for each subtask until complete.

```bash
# Check progress anytime
$ tm autopilot status --json
{
  "taskId": "7",
  "progress": {
    "completed": 1,
    "total": 5,
    "percentage": 20
  },
  "currentSubtask": {
    "id": "2",
    "title": "Implement resume command"
  }
}

```

## 4\. Complete the Workflow

When all subtasks are done:

```bash
$ tm autopilot status --json
{
  "phase": "COMPLETE",
  "progress": {
    "completed": 5,
    "total": 5,
    "percentage": 100
  }
}

```

Your branch `task-7` is ready for review/merge.

## Common Patterns

### Parse Test Output

Your test runner outputs human-readable format — convert to JSON:

**Vitest:**

```
Tests  2 failed | 8 passed | 10 total

```

\-> `{"total":10,"passed":8,"failed":2,"skipped":0}`

**Jest:**

```
Tests:  2 failed, 8 passed, 10 total

```

\-> `{"total":10,"passed":8,"failed":2,"skipped":0}`

### Handle Errors

**Problem:** RED phase won't complete — "no test failures"

**Solution:** Your test isn't testing new behavior. Make sure it fails:

```typescript
// Bad - test passes immediately
it('should exist', () => {
  expect(StartCommand).toBeDefined(); // Always passes
});

// Good - test fails until feature exists
it('should initialize workflow', async () => {
  const result = await new StartCommand().execute({ taskId: '7' });
  expect(result.success).toBe(true); // Fails until execute() is implemented
});

```

**Problem:** GREEN phase won't complete — "tests still failing"

**Solution:** Fix your implementation until all tests pass:

```bash
# Run tests to see what's failing
$ npm test

# Fix the issue
$ vim src/commands/start.ts

# Verify tests pass
$ npm test

# Try again
$ tm autopilot complete --results '{"total":1,"passed":1,"failed":0,"skipped":0}'

```

### Resume Interrupted Work

```bash
# If you interrupted the workflow
$ tm autopilot resume

✓ Workflow resumed
✓ Task 7 - subtask 3/5
✓ Current phase: GREEN
→ Continue from where you left off

```

## JSON Output Mode

All commands support `--json` for programmatic use:

```bash
$ tm autopilot start 7 --json | jq .
{
  "success": true,
  "taskId": "7",
  "branchName": "task-7",
  "phase": "SUBTASK_LOOP",
  "tddPhase": "RED",
  "progress": { ... },
  "currentSubtask": { ... },
  "nextAction": "generate_test"
}

```

Perfect for:

* CI/CD integration
* Custom tooling
* Automated workflows
* Progress monitoring

## MCP Integration

For AI agents (Claude Code, etc.), use MCP tools:

```typescript
// Start workflow
await mcp.call('autopilot_start', {
  taskId: '7',
  projectRoot: '/path/to/project'
});

// Get next action
const next = await mcp.call('autopilot_next', {
  projectRoot: '/path/to/project'
});

// Complete phase
await mcp.call('autopilot_complete_phase', {
  projectRoot: '/path/to/project',
  testResults: { total: 1, passed: 0, failed: 1, skipped: 0 }
});

// Commit
await mcp.call('autopilot_commit', {
  projectRoot: '/path/to/project'
});

```

See [AI Agent Integration Guide](https://tryhamster.com/docs/taskmaster/tdd-workflow/ai-agent-integration) for details.

## Cheat Sheet

```bash
# Start
tm autopilot start <taskId>         # Initialize workflow

# Workflow Control
tm autopilot next                    # What's next?
tm autopilot status                  # Current state
tm autopilot resume                  # Continue interrupted work
tm autopilot abort                   # Cancel and cleanup

# TDD Cycle
tm autopilot complete --results '{...}'   # Advance phase
tm autopilot commit                       # Save progress

# Options
--json                              # Machine-readable output
--project-root <path>               # Specify project location
--force                             # Override safety checks

```

## Tips

1. Always let tests fail first — That's the RED phase
2. Write minimal code — Just enough to pass
3. Commit frequently — After each subtask
4. Use --json — Better for programmatic use
5. Check status often — Know where you are
6. Trust the workflow — It enforces TDD rules

```json
[{"@context":"https://schema.org","@type":"Organization","name":"Hamster","url":"https://tryhamster.com","logo":"https://tryhamster.com/images/og-image.png","description":"Hamster is an AI-powered development platform that helps teams plan, collaborate, and ship software faster.","sameAs":["https://github.com/eyaltoledano/claude-task-master","https://x.com/usehamster","https://www.linkedin.com/company/tryhamster"],"foundingDate":"2024","knowsAbout":["Project management software","Product management software","AI project management","AI product management","AI workspace","AI agents","Agentic workflows","Context engineering","Context Graph","Product engineering","AI-native software development lifecycle"]},{"@context":"https://schema.org","@type":"WebSite","name":"Hamster","url":"https://tryhamster.com","description":"Hamster is an AI-native product planning workspace where humans and AI teammates share context, align on briefs, and ship together."}]
{"@context":"https://schema.org","@type":"BreadcrumbList","itemListElement":[{"@type":"ListItem","position":1,"name":"Home","item":"https://tryhamster.com"},{"@type":"ListItem","position":2,"name":"Docs","item":"https://tryhamster.com/docs"},{"@type":"ListItem","position":3,"name":"Taskmaster","item":"https://tryhamster.com/docs/taskmaster"},{"@type":"ListItem","position":4,"name":"Tdd Workflow","item":"https://tryhamster.com/docs/taskmaster/tdd-workflow"},{"@type":"ListItem","position":5,"name":"Quickstart","item":"https://tryhamster.com/docs/taskmaster/tdd-workflow/quickstart"}]}
```
