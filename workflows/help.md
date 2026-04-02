# Help

Context: @references/orchestrator-pattern.md ∧ @references/conventions.md

Display tff command reference:

### Project Lifecycle
| Command | Description |
|---|---|
| `/tff-test:new` | Initialize new tff project |
| `/tff-test:new-milestone` | Start new milestone |
| `/tff-test:progress` | Show status dashboard |

### Slice Lifecycle
| Command | Description |
|---|---|
| `/tff-test:discuss` | Brainstorm and scope a slice |
| `/tff-test:research [slice-id]` | Research phase |
| `/tff-test:plan [slice-id]` | Plan and create tasks |
| `/tff-test:execute [slice-id]` | Execute with wave parallelism |
| `/tff-test:verify [slice-id]` | Verify acceptance criteria |
| `/tff-test:ship [slice-id]` | PR review and create slice PR |

### Milestone Lifecycle
| Command | Description |
|---|---|
| `/tff-test:audit-milestone` | Audit against original intent |
| `/tff-test:complete-milestone` | PR review and create milestone PR |

### Management
| Command | Description |
|---|---|
| `/tff-test:add-slice` | Add slice to milestone |
| `/tff-test:insert-slice` | Insert between slices |
| `/tff-test:remove-slice` | Remove future slice |
| `/tff-test:rollback [slice-id]` | Revert slice commits |
| `/tff-test:pause` | Save checkpoint |
| `/tff-test:resume` | Restore from checkpoint |
| `/tff-test:sync` | Regenerate STATE.md from SQLite |
| `/tff-test:health` | Diagnose state consistency |
| `/tff-test:settings` | Configure model profiles |
| `/tff-test:detect-patterns` | Extract and rank tool-use patterns |
| `/tff-test:suggest-skills` | Show pattern candidates with summaries |
| `/tff-test:create-skill` | Draft a skill from a pattern |
| `/tff-test:learn` | Propose refinements to existing skills |
| `/tff-test:compose` | Propose skill bundles or agents |
