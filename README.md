# AFEOL Workspace Framework

Version

```text
2026.1
```

Status

```text
FOUNDATION DRAFT
```

License

```text
Mozilla Public License 2.0 (MPL-2.0)
```

---

# Purpose

The AFEOL Workspace Framework defines a standardized, application-independent Workspace Runtime.

The Workspace Runtime validates, renders, and manages application workspaces through a common Workspace Standard.

The framework defines architecture and behavior.

It does not define business logic.

---

# Vision

A compatible application should be able to describe its user interface through a standard Workspace Contract.

The Workspace Runtime validates the submitted definition, renders the Workspace, and reports structured events and diagnostics back to the application.

---

# Core Architecture

```text
Application

↓

Workspace Contract

↓

Workspace Runtime

↓

Rendered Workspace
```

Communication between the application and the Workspace Runtime is duplex.

---

# Workspace Runtime Responsibilities

The Workspace Runtime is responsible for:

- validating Workspace definitions;
- rendering the Workspace;
- managing layout;
- managing Dock behavior;
- managing Canvas behavior;
- dispatching Workspace events;
- enforcing Workspace constraints;
- reporting structured diagnostics.

---

# Application Responsibilities

The application is responsible for:

- business logic;
- user identity;
- tenant identity;
- project state;
- persistence;
- user preferences;
- application configuration;
- authorization;
- diagnostics history.

---

# Stateless Runtime Principle

The Workspace Runtime is stateless outside the lifetime of a running Workspace instance.

Temporary in-memory state is permitted while a Workspace instance is active.

Persistent application state is never owned by the Runtime.

---

# Normative Rule

> **THE WORKSPACE RUNTIME SHALL NEVER PERSIST USER-SPECIFIC, TENANT-SPECIFIC, PROJECT-SPECIFIC, APPLICATION-SPECIFIC, BUSINESS-SPECIFIC, OR CROSS-SESSION STATE.**

Persistence is exclusively the responsibility of the application implementing the Workspace Standard.

---

# Canvas Principle

The Canvas is the primary working area.

The Dock follows the active Canvas context.

The Canvas never becomes subordinate to the Dock.

---

# Dock Principle

The Dock is a generic Workspace component.

It is not application-specific.

The Runtime owns Dock behavior.

Applications own Dock content.

---

# Floating Dock

The Workspace Runtime may support multiple Dock modes.

Typical supported modes are:

```text
LEFT

RIGHT

FLOATING

HIDDEN
```

The Runtime validates Dock movement.

The application decides whether the resulting Dock state should be persisted.

---

# Diagnostics

The Workspace Runtime reports structured diagnostics.

Diagnostics should contain sufficient information for developers to identify, understand, and resolve validation failures.

The Runtime reports current diagnostics only.

Applications may maintain temporary diagnostic history.

---

# Foundation

The architectural foundation of the Workspace Framework is defined in:

```text
docs/foundation/workspace-foundation.md
```

Derived specifications extend the Foundation.

They shall never contradict it.

---

# Repository Structure

```text
afeol-workspace-framework/

├── README.md
├── LICENSE
├── CHANGELOG.md
├── .gitignore
└── docs/
    ├── foundation/
    └── specifications/
```

---

# Development Principle

The Workspace Framework evolves from proven application behavior.

```text
Foundation

↓

Implementation

↓

Observation

↓

Refinement

↓

Specification

↓

Lock
```

The Standard follows successful implementations.

Implementations do not redefine the Standard.

---

# License

This repository is licensed under the Mozilla Public License Version 2.0 (MPL-2.0).

See the `LICENSE` file for the complete license text.
