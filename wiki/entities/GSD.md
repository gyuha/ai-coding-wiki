# GSD

## Summary

[[GSD]] (Get Shit Done) is described in the current source base as an open-source workflow layer for AI coding agents. Rather than replacing tools like Claude Code or Codex, it is presented as a context-engineering harness that adds planning, execution structure, persistent project memory, and verification on top of those runtimes.

## Core idea

The central claim is that agent quality degrades through [[Context Rot]] as sessions grow longer and less focused. GSD's answer is to decompose work into explicit phases and persist important context in project files so each implementation step can run with a smaller, fresher working set.

## Workflow shape in the current source

According to [[2026-03-26 GSD Context Engineering for Coding Agents]], GSD is organized around:

- codebase mapping before changes
- project and requirements initialization
- phase discussion before planning
- small, atomic plan creation
- dependency-aware execution, including parallel waves for independent work
- verification against user-visible outcomes
- explicit guidance on the next workflow step

## Claimed strengths

- makes implicit product and implementation decisions explicit before coding
- stores project memory outside a single chat session
- supports bounded execution units instead of one giant prompt
- treats verification as a separate discipline rather than assuming tests are enough

## Limits and cautions

- The source says the workflow is likely too heavy for small one-off edits.
- The workflow is terminal-centric, so it may be a poor fit for GUI-first preferences.
- The current evidence is from a secondary article, so operational details should be revalidated against upstream docs before use.

## Sources

- [[2026-03-26 GSD Context Engineering for Coding Agents]]
