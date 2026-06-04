# UI Guidelines - TODO App

## Purpose

This document defines UI and UX guidelines for the TODO application and serves as the source of truth for interface consistency.

## Scope

These guidelines cover component system usage, visual style, responsiveness, messaging, and copy tone.

## Core UI Guidelines

### UI-001: Material Components

The application must use Material components as the primary UI component system.

Acceptance criteria:
- New UI features use Material-based components for controls, layout primitives, and form elements.
- Custom components should align visually and behaviorally with Material patterns.
- Component usage remains consistent across screens.

### UI-002: Pastel Color Palette

The application must follow a pastel color palette.

Acceptance criteria:
- Primary, secondary, background, and state colors use pastel tones.
- Color choices preserve readability and contrast for text and interactive elements.
- Status colors (success, warning, error, info) remain visually distinct while fitting the pastel palette.

### UI-003: Rounded Corners

Buttons and UI components should use rounded corners.

Acceptance criteria:
- Buttons use rounded corners by default.
- Surfaces and interactive components (for example cards, inputs, dialogs, chips) use a consistent rounded corner style.
- Corner radius values are consistent across the app unless a specific component requires an exception.

### UI-004: Responsive Experience

The application must always feel responsive.

Acceptance criteria:
- Layout and components adapt to common mobile, tablet, and desktop viewports.
- Interactive elements provide immediate visual feedback to user actions.
- Loading and asynchronous states are clearly communicated to users.

### UI-005: User-Facing Error Messages

Errors must always be presented to the user with a clear message.

Acceptance criteria:
- Any failed user action or system error surfaces an understandable message.
- Error messages explain what happened in simple language and, when appropriate, suggest a next step.
- Error feedback is shown in context (inline, toast, dialog, or banner) where users can notice it.

### UI-006: Short and Effective Wording

Application wording must be short and effective.

Acceptance criteria:
- Labels, button text, helper text, and messages are concise and direct.
- Avoid long or ambiguous wording when a shorter alternative communicates the same meaning.
- Microcopy uses plain language and action-oriented phrasing.

## Implementation Notes

- These guidelines apply to all new UI work and to refactors of existing UI.
- If a guideline conflicts with accessibility requirements, accessibility takes priority.
- If a guideline conflicts with a functional requirement, align implementation with functional behavior while preserving these UI principles as much as possible.
