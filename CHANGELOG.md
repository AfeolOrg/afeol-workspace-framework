# Changelog

All notable architectural and specification changes to the AFEOL Workspace Framework shall be documented in this file.

The project follows Semantic Versioning for released versions.

---

# 2026.1

Status

```text
FOUNDATION DRAFT
```

Initial public foundation of the AFEOL Workspace Framework.

---

## Added

- Repository structure.
- Workspace Foundation.
- Workspace Runtime architecture.
- Stateless Runtime principle.
- Application-owned persistence model.
- Workspace Contract concept.
- Diagnostics architecture.
- Floating Dock concept.
- Semantic Dock grouping.
- Canvas-first workspace model.
- Runtime capability model.
- Application independence principle.
- Multi-tenant independence principle.
- Provider independence principle.

---

## Architectural Decisions

### Workspace Runtime

The Workspace Runtime is a generic runtime platform.

It validates, renders, and manages compatible Workspace definitions.

The Runtime never becomes application-specific.

---

### Stateless Runtime

The Runtime remains stateless outside the lifetime of the active Workspace instance.

Persistent application state belongs exclusively to the application.

---

### Persistence

Normative rule adopted.

```text
THE WORKSPACE RUNTIME SHALL NEVER PERSIST
USER-SPECIFIC,
TENANT-SPECIFIC,
PROJECT-SPECIFIC,
APPLICATION-SPECIFIC,
BUSINESS-SPECIFIC,
OR CROSS-SESSION STATE.
```

---

### Workspace Contract

Communication between applications and the Runtime is duplex.

Applications submit Workspace definitions.

The Runtime validates those definitions and returns structured events, accepted runtime state, and diagnostics.

---

### Canvas

The Canvas is the primary working surface.

The Dock follows the current Canvas context.

---

### Dock

The Dock is a generic Workspace component.

Supported presentation modes include:

```text
LEFT

RIGHT

FLOATING

HIDDEN
```

Applications own Dock content.

The Runtime owns Dock behavior.

---

### Diagnostics

Diagnostics are structured.

Diagnostics shall be human-readable.

Diagnostics shall identify:

- code;
- severity;
- registry;
- component;
- message;
- details;
- suggestion.

---

### Semantic Groups

Dock capacity shall be managed through semantic grouping.

Applications shall not rely on arbitrary tabs or automatic splitting.

---

### Compatibility

Applications become compatible through conformance to the Workspace Standard.

Technology does not determine compatibility.

---

### Repository

Initial repository structure established.

```text
README.md

LICENSE

CHANGELOG.md

docs/
```

---

## License

The project is licensed under the Mozilla Public License Version 2.0 (MPL-2.0).

See:

https://www.mozilla.org/MPL/2.0/

SPDX-License-Identifier: MPL-2.0
