# Context Rot

## Summary

[[Context Rot]] is the term used in the current source base for the degradation in an AI coding agent's performance as a session accumulates more context, stale decisions, and incidental detail. The source describes it as a practical failure mode of long-running agent sessions rather than a purely theoretical limitation.

## Symptoms described in the current source

According to [[2026-03-26 GSD Context Engineering for Coding Agents]], context rot can show up as:

- shorter or less useful responses over time
- forgotten earlier decisions
- unrelated or random code changes
- increasing user effort spent supervising the agent instead of delegating to it

## Mitigation patterns

The source argues that context rot can be reduced by:

- splitting work into bounded phases instead of one long session
- persisting project memory in files rather than only in chat
- planning atomic tasks before execution
- re-verifying outputs at each step

[[GSD]] is presented as one workflow system built around those mitigation patterns.

## Sources

- [[2026-03-26 GSD Context Engineering for Coding Agents]]
