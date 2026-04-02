# Next Step Suggestions

Every tff command MUST end with a next-step suggestion based on the current state.

## State → Suggestion Map

After each command completes, check the slice/milestone state and suggest:

| Current State | Suggested Command | Message |
|---|---|---|
| Project just created | `/tff-test:new-milestone` | "Project initialized. Create your first milestone with `/tff-test:new-milestone`." |
| Milestone created, no slices | `/tff-test:discuss` | "Milestone ready. Start scoping the first slice with `/tff-test:discuss`." |
| Slice in `discussing` | `/tff-test:discuss` | "Continue discussing, or if scope is locked, it will auto-advance to research." |
| Slice in `researching` | `/tff-test:research` | "Research phase. Run `/tff-test:research` to investigate the technical approach." |
| Slice in `planning` | `/tff-test:plan` | "Ready to plan. Run `/tff-test:plan` to create tasks and review via plannotator." |
| Slice in `executing` | `/tff-test:execute` | "Execution phase. Run `/tff-test:execute` to start wave-based task execution." |
| Slice in `verifying` | `/tff-test:verify` | "Verification phase. Run `/tff-test:verify` to check acceptance criteria." |
| Slice in `reviewing` | `/tff-test:ship` | "Ready for review. Run `/tff-test:ship` to create the slice PR and run reviews." |
| Slice in `completing` | (auto) | "Slice is being finalized. It will close automatically after merge." |
| Slice `closed`, more slices open | `/tff-test:discuss` or `/tff-test:progress` | "Slice shipped! Run `/tff-test:progress` to see overall status, or `/tff-test:discuss` for the next slice." |
| All slices `closed` | `/tff-test:audit-milestone` | "All slices complete. Run `/tff-test:audit-milestone` to verify milestone readiness." |
| Milestone audited | `/tff-test:complete-milestone` | "Audit passed. Run `/tff-test:complete-milestone` to create the milestone PR." |
| Milestone `closed` | `/tff-test:new-milestone` | "Milestone shipped! Start the next one with `/tff-test:new-milestone`." |

## How to Use

At the end of every workflow, add:

```
### Next Step
Read the current state and suggest the appropriate next command from @references/next-steps.md.
```

## Paused/Resumed States

| State | Suggested Command |
|---|---|
| Checkpoint exists | `/tff-test:resume` | "Found a saved checkpoint. Run `/tff-test:resume` to continue from where you left off." |
| Verification failed | `/tff-test:execute` | "Verification found issues. Run `/tff-test:execute` to fix and re-run failed tasks." |
| PR changes requested | `/tff-test:ship` | "Review requested changes. Run `/tff-test:ship` to apply fixes and re-review." |
