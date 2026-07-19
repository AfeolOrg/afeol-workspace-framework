# AFEOL Workspace Framework

A technology-neutral Workspace Framework for building consistent, secure, and maintainable applications.

The AFEOL Workspace Framework defines a standardized architectural boundary between an application and a Workspace Runtime. It separates business logic from presentation behavior while remaining independent of programming language, UI toolkit, transport protocol, and deployment environment.

---

# Goals

The framework is designed around a small number of long-term architectural principles:

- Application-owned authoritative state
- Runtime-owned presentation behavior
- Technology neutrality
- Security by architectural design
- Deterministic behavior
- Stateless Runtime
- Long-term compatibility
- Open specifications

---

# Repository Structure

```text
afeol-workspace-framework/
│
├── CHANGELOG.md
├── LICENSE
├── README.md
│
└── docs/
    └── foundation/
        ├── workspace-foundation.md
        └── workspace-draft-completion-rule.md
```

Additional specifications will be added as the framework evolves.

---

# Specifications

Current specifications:

| Document | Status |
|----------|--------|
| Workspace Foundation | FOUNDATION |

Future specifications will include:

- Workspace Security Foundation
- Workspace Contract Specification
- Workspace Protocol Specification
- Workspace Diagnostics Specification
- Workspace Runtime Profile
- Workspace Secure Rendering Specification
- Workspace Resource Governance Specification
- Workspace Extension Isolation Specification
- Reference Security Tests

---

# Getting Started

The recommended reading order is:

```text
README
    │
    ▼
Workspace Foundation
    │
    ▼
Derived Specifications
    │
    ▼
Reference Tests
    │
    ▼
Reference Implementations
```

The Workspace Foundation is the normative document that defines the architectural rules of the framework.

Location:

```text
docs/foundation/workspace-foundation.md
```

---

# Design Principles

The framework follows several fundamental principles:

- Simplicity over unnecessary complexity
- Explicit contracts over implicit behavior
- Deterministic execution
- Security through architecture
- Separation of responsibilities
- Stable foundations with independently evolving specifications

---

# Versioning

The repository follows Semantic Versioning.

Current release:

```text
v1.0.0
```

Foundation documents evolve slowly.

Derived specifications evolve independently.

Reference implementations may evolve more rapidly.

---

# Contributing

Contributions are welcome.

Please read the project documentation before proposing architectural changes.

Normative changes should preserve compatibility whenever reasonably possible.

Contribution guidelines will be published in `CONTRIBUTING.md`.

---

# License

Repository source files are licensed under the Mozilla Public License 2.0.

Documentation may define its own license where explicitly stated.

See:

```text
LICENSE
```
