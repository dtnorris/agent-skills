# Agent Skills

Reusable instructions and standards for AI coding agents, maintained in one place for consistent use across repositories, tools, and workflows.

## Skills

| Skill | Purpose |
|---|---|
| [Karpathy–Manning–DTNorris Guidelines](skills/karpathy-manning-dtnorris-guidelines/SKILL.md) | Practical coding guidelines emphasizing simplicity, surgical changes, clear documentation, explicit assumptions, and verifiable results. |
| [Agentic Task Planning](skills/agentic-task-planning/SKILL.md) | Planning substantial AI-assisted engineering work, including task decomposition, dependencies, parallel execution, integration, recovery, and end-to-end acceptance. |
| [Agent Manager (Experimental)](skills/agent-manager/SKILL.md) | Steering long-running engineering workstreams: scope, blockers, time, human attention, and acceptance. |

## Usage

Skills are maintained here as canonical sources. Agents can reference them through repository `AGENTS.md` files, project instructions, or automated prompt generation.

For reproducibility, prefer referencing a pinned commit rather than a moving branch.

Task-specific requirements and safety constraints take precedence over general guidelines.

## License

MIT. See [LICENSE](LICENSE).
