# [Project Name] Agent Playbook

## Before Starting
1. Ensure PROGRESS.md is up to date
2. Verify previous WP's tests still pass
3. Start a fresh agent session for each WP

## Common Mistakes
- Starting the next WP without being asked → prevented by "out of scope"
- Skipping tests → prevented by done criteria
- Inventing table names → prevented by ERD
- Wrong API shapes → prevented by API contracts

## Tips
- Use /review on complex WPs
- If agent runs out of tokens, say "continue WP-XX"
- If something breaks, use /fix before moving on
