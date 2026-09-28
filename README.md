# RVR — Research, Validate, Report

A Claude Code skill that answers "will this actually work?" for a specific architectural, schema, pipeline, or technical design proposal. It researches the real constraints, stress-tests the idea with a Sandboxer and a Skeptic, then reports a strict verdict:

- **Feasibility Score** — Highly Feasible / Feasible with Trade-offs / Will Break
- **The Why**
- **The Gotchas**
- **The Pivot** (when it isn't Highly Feasible)

## Install

In Claude Code:

```
/plugin marketplace add ambareeshav/rvr
/plugin install rvr@ambareeshav
```

## Use

Describe the design decision and end your message with `rvr`, e.g.

> Instead of having the LLM read the whole document with get_document, get_document(code) returns a skeleton and it uses section-ids from the skeleton to read just the needed sections with get_document(code, section_ids=[…]) rvr

The bundled hook forces the skill to run when a message ends with `rvr`. It also triggers on its own when you ask whether a specific design will hold up.

## Manual install (skill only, no hook)

```
claude plugin marketplace add ambareeshav/rvr
claude plugin install rvr@ambareeshav
```
