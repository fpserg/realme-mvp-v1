# RealMe MVP Repository

RealMe is a personal cognitive operating system designed to reduce cognitive load while preserving human agency.

This repository contains the architectural specification for the RealMe MVP.

---

## Repository Structure

The numbered documents (`00`–`10`) constitute the authoritative specification of the system.

They define:

- principles;
- architecture;
- persistent knowledge;
- information flow;
- conversational conduct;
- implementation boundaries;
- future evolution.

When documents appear to conflict, lower-numbered documents take precedence unless explicitly superseded.

---

## Companion Documents

The repository also contains several unnumbered documents.

These are **not** part of the architectural specification itself.

Instead, they describe how the specification is developed or implemented.

Examples include:

- `AI_BUILDER.md` — instructions for AI software engineers implementing the Repository;
- `BUILDING_MODE.md` — protocol for collaboratively evolving the Repository.

---

## Source of Truth

The numbered Repository documents are the canonical definition of RealMe.

Implementations should conform to the Repository.

When implementation and Repository disagree, the Repository is considered authoritative until intentionally revised.

---

## Repository Philosophy

The Repository should remain:

- small;
- explicit;
- technology-independent;
- maintainable;
- understandable by both humans and AI.

It is intended to outlive any specific implementation, framework or language.
