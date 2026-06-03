# Functional Requirements - TODO App

## Purpose

This document defines the core functional requirements for the TODO application and serves as the source of truth for expected behavior.

## Scope

These requirements cover task creation, task editing, due dates, task status management, importance levels, and sorting behavior.

## Definitions

- Task: A single TODO item created by the user.
- Status: The current progress state of a task. Allowed values are `To Do`, `In Progress`, and `Completed`.
- Importance: The priority level of a task. Allowed values are `Low`, `Medium`, `Top`, and `Critical`.
- Sorting direction:
  - Up: Ascending order.
  - Down: Descending order.

## Core Functional Requirements

### FR-001: Create Task

The system must allow the user to create a new task.

Acceptance criteria:
- The user can enter task content/title.
- A task is persisted after creation.
- A newly created task defaults to status `To Do` unless the user explicitly sets a different valid status during creation.
- A newly created task defaults to importance `Low` unless the user explicitly sets a different valid importance during creation.

### FR-002: Assign Due Date

The system must allow the user to set a due date for a task.

Acceptance criteria:
- The user can assign a due date when creating a task.
- The user can add or update a due date after task creation.
- The due date is stored and displayed with the task.
- A task may exist without a due date.

### FR-003: Edit Task After Creation

The system must allow the user to edit an existing task after it has been created.

Acceptance criteria:
- The user can edit task content/title.
- The user can edit due date.
- The user can edit importance.
- The user can edit status.
- Edits are persisted and visible immediately after save/confirm.

### FR-004: Manage Task Status

The system must allow users to set and update task status.

Acceptance criteria:
- The user can set a task to `To Do`.
- The user can set a task to `In Progress`.
- The user can set a task to `Completed`.
- Status changes are persisted.

### FR-005: Importance Levels

The system must support the following importance levels for each task:
- `Low`
- `Medium`
- `Top`
- `Critical`

Acceptance criteria:
- Every task has exactly one importance level.
- Importance value must be one of the four allowed values.
- Importance changes are persisted.

### FR-006: Sort Tasks Alphabetically (Up)

The system must allow sorting tasks alphabetically in ascending order.

Acceptance criteria:
- Sorting by task title/content in ascending A-Z order is available.
- Sorting is applied to the currently visible task list.

### FR-007: Sort Tasks Alphabetically (Down)

The system must allow sorting tasks alphabetically in descending order.

Acceptance criteria:
- Sorting by task title/content in descending Z-A order is available.
- Sorting is applied to the currently visible task list.

### FR-008: Sort Tasks by Due Date (Up)

The system must allow sorting tasks by due date in ascending order.

Acceptance criteria:
- Sorting by due date from earliest to latest is available.
- Tasks without a due date are placed at the end of the list.
- Sorting is applied to the currently visible task list.

### FR-009: Sort Tasks by Due Date (Down)

The system must allow sorting tasks by due date in descending order.

Acceptance criteria:
- Sorting by due date from latest to earliest is available.
- Tasks without a due date are placed at the end of the list.
- Sorting is applied to the currently visible task list.

### FR-010: Sort Tasks by Importance

The system must allow sorting tasks by importance in both directions.

Acceptance criteria:
- Importance sorting supports `Up` and `Down`.
- The defined importance rank from lowest to highest is: `Low` < `Medium` < `Top` < `Critical`.
- `Up` sorts using lowest-to-highest rank.
- `Down` sorts using highest-to-lowest rank.
- Sorting is applied to the currently visible task list.

### FR-011: Sort Tasks by Completion

The system must allow sorting tasks by completion/status in both directions.

Acceptance criteria:
- Completion sorting supports `Up` and `Down`.
- Status rank for `Up` is: `To Do` < `In Progress` < `Completed`.
- Status rank for `Down` is the reverse of `Up`.
- Sorting is applied to the currently visible task list.

## Common Sorting Rules

The following rules apply to every sorting mode:
- Only one active primary sort mode is applied at a time.
- Sorting operation must not modify task data; it only changes display order.
- Sorting results are deterministic for equal values by using task creation timestamp ascending as a tie-breaker.

## Non-Goals (Out of Scope for This Document)

The following are intentionally not defined here:
- Authentication or user account management.
- Sharing/collaboration between users.
- Notifications/reminders.
- Recurring tasks.
- Subtasks.
