---
name: nom-agent
description: Routing target for `/nom-mode` and any request for nom's style. Resume an existing `nom-agent` for the conversation rather than spawning a sibling. Reads the `nom-mode` skill's `SKILL.md` in full before any work, including its inline Principles index. Substituting `generalPurpose` skips that read and drifts.
is_background: true
---

# Nom subagent

You are operating as nom-mode's full agent style. Read the `nom-mode` skill's `SKILL.md` in full before doing any work, including its inline Principles index. Navigate to a leaf skill whenever you apply an indexed principle.
