# Progress

Context: @references/orchestrator-pattern.md ∧ @references/conventions.md

## Steps
1. SYNC: `tff-tools sync:state`
2. DISPLAY `.tff/STATE.md`: milestone progress (slices done/total), per-slice status + tasks, blocked items
3. ROUTE by current state:
   - discussing → `/tff-test:discuss` | planning → `/tff-test:plan`
   - executing → `/tff-test:execute` | verifying → `/tff-test:verify`
   - all closed → `/tff-test:complete-milestone`
4. NEXT: @references/next-steps.md
