# nom

<img width="1200" height="1600" alt="nom" src="https://github.com/user-attachments/assets/aace5cf6-13c9-4476-85a0-9ca5a890007b" />

A Cursor plugin for principle-driven engineering. `/nom-mode` classifies the task, loads a playbook, and runs it under standing rules.

It is not an agent harness. Cursor owns the loop. Nom encodes how the work should be done.

## Install

After it is listed on the Cursor Marketplace:

```
/add-plugin nom
```

Or Customize → Plugins → search **nom**.

Until then, load it as a local plugin:

```bash
rsync -a --delete --exclude .git --exclude .cursor ./ ~/.cursor/plugins/local/nom/
```

Then **Developer: Reload Window**.

## Use

Start rigorous work with [`/nom-mode`](./skills/nom-mode/SKILL.md). It picks a playbook from the deliverable:

| Playbook | Use when |
| --- | --- |
| [Investigation](./skills/nom-mode/playbooks/investigation.md) | A read-only explanation, diagnosis, or recommendation |
| [Bug fix](./skills/nom-mode/playbooks/bug-fix.md) | A defect to reproduce, isolate, fix, and verify |
| [Feature](./skills/nom-mode/playbooks/feature.md) | New or changed product behavior |
| [Refactoring](./skills/nom-mode/playbooks/refactoring.md) | A behavior-preserving structural change |
| [Performance](./skills/nom-mode/playbooks/performance.md) | A measured latency, throughput, or resource problem |
| [Prototype](./skills/nom-mode/playbooks/prototype.md) | A throwaway artifact to settle an empirical decision |

No match stays under standing rules. If the pattern will recur, add a playbook instead of repeating a bespoke plan.

Subagents inside a playbook use `subagent_type: "nom-agent"`.

## Cloud

Cloud agents do not see `~/.cursor/skills` or `~/.cursor/plugins/local`. They see the cloned repo and marketplace or team plugins.

Install nom from the marketplace (or a team marketplace set to Required / Default On). In the consumer repo, commit:

```json
{
  "plugins": {
    "nom": { "enabled": true }
  }
}
```

Put that in `.cursor/settings.json`. Cloud kickoffs still have to enter nom-mode. Name it in the prompt. `/nom-mode` is explicit on purpose.

## What it contains

- **[`/nom-mode`](./skills/nom-mode/SKILL.md)** entry point and playbooks
- **Nine principle leaves** under `skills/principle-*`, read in full when applied
- **[`unslop`](./skills/unslop/SKILL.md)** for every prose surface, including the reply
- **[`nom-agent`](./agents/nom-agent.md)** wrapper for playbook subagents

## License

MIT. `unslop` comes from pstack (Lauren Tan).
