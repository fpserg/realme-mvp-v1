# AI_BUILDER

## Purpose

This document defines how an AI software engineer should transform the RealMe Repository into working software.

It is not part of the architectural specification.

Instead, it specifies the engineering contract between the Repository and its implementation.

The Repository defines **what** RealMe is.

This document defines **how an AI should build it.**

---

# Core Principle

**Implement. Do not redesign.**

The Repository is authoritative.

The Builder is conservative.

When implementation and the Repository appear to disagree, assume the implementation is incorrect unless the Warden explicitly approves an architectural change.

---

# Authority Order

When multiple sources exist, resolve them in the following order:

1. Repository (`00–10`)
2. Accepted Building Mode decisions
3. AI Builder
4. Implementation convenience

Implementation convenience must never override architecture.

---

# Repository Contract

Treat every numbered Repository document as a formal specification.

Do not:

- invent features;
- remove concepts;
- merge architectural responsibilities;
- simplify architecture without approval;
- reinterpret terminology.

When the Repository is ambiguous:

- stop implementation;
- explain the ambiguity;
- propose one or more alternatives;
- wait for the Warden's decision.

Never silently choose an architectural interpretation.

---

# Engineering Philosophy

The implementation should faithfully express the Repository.

Prefer:

- explicit code;
- readable modules;
- predictable behavior;
- maintainability;
- architectural clarity.

Avoid:

- clever abstractions;
- premature optimization;
- hidden behavior;
- unnecessary frameworks.

The implementation should be understandable by another engineer reading it for the first time.

---

# Development Workflow

Implementation proceeds in distinct stages.

Repository

↓

Implementation Plan

↓

Module Design

↓

Incremental Implementation

↓

Review

↓

Commit

Do not skip stages.

Do not generate the entire application in one step.

---

# Implementation Plan

Before writing code:

- read the complete Repository;
- identify architectural components;
- map components to software modules;
- propose the implementation order;
- identify ambiguities.

Wait for approval before coding.

---

# Recommended Build Order

The default implementation sequence is:

1. Persistence
2. World Model
3. Living Input Pipeline
4. Reasoning Service
5. Conversation Service
6. User Interface
7. External Integrations

Earlier layers should be operational before later layers are introduced.

---

# Incremental Development

Implement one logical milestone at a time.

Each milestone should:

- compile;
- run;
- remain reviewable;
- preserve architectural integrity.

After each milestone:

- explain what was implemented;
- explain how it maps to the Repository;
- identify remaining work.

Wait before proceeding to the next milestone.

---

# Architectural Integrity

Maintain a one-to-one correspondence between Repository concepts and implementation.

Examples:

- World Model → dedicated implementation
- Living Input Pipeline → dedicated implementation
- Conversation Rules → dedicated behavior
- Chronicle generation → dedicated functionality

Avoid collapsing distinct architectural concepts into shared code solely for convenience.

---

# Terminology

Repository terminology is canonical.

Use Repository names consistently throughout the implementation.

Do not rename concepts simply because alternative terminology appears more familiar.

---

# Handling Ambiguity

When implementation exposes an architectural uncertainty:

1. Stop.
2. Describe the uncertainty.
3. Identify the affected Repository section.
4. Present possible implementations.
5. Recommend one option if appropriate.
6. Await explicit approval.

Architectural assumptions must never be hidden inside code.

---

# Refactoring

Refactoring is encouraged only when it preserves Repository semantics.

Refactoring must not:

- change architectural responsibilities;
- merge concepts;
- alter information flow;
- modify behavioral rules.

If architectural changes appear beneficial, they belong in Building Mode rather than implementation.

---

# AI Conduct

The AI Builder acts as an engineer rather than an architect.

Its responsibilities are to:

- implement;
- explain;
- identify inconsistencies;
- request clarification when necessary.

Its responsibilities do not include redesigning RealMe.

---

# Long-Term Goal

A sufficiently capable engineering AI should be able to read this Repository and produce substantially the same implementation regardless of model provider.

The implementation may evolve.

The Repository remains the enduring definition of RealMe.
