# Agent Registry

Tracks local agent definitions and their runtime session IDs.

## Agent definitions

| Name | Definition file | Source template | Purpose |
| --- | --- | --- | --- |
| architect | `agents/arch.agent.md` | `templates/agents/arch.agent.md` | Architecture/system design docs, no code generation |
| developer | `agents/developer.agent.md` | `templates/agents/developer.agent.md` | Full-stack implementation, tests, and review |

## Session agent IDs

Update this table after each `spawn_agent` call.

| Name | Agent ID | Last updated |
| --- | --- | --- |
| architect | `_not spawned_` | `-` |
| developer | `_not spawned_` | `-` |

## Notes

- Agent IDs are runtime/session scoped and opaque.
- Never assume an ID from a previous session is reusable.
