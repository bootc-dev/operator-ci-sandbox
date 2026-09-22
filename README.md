# operator-ci-sandbox

Test repository for CI automation experiments.

## Mergify Backport Flow

The `.mergify.yml` rule automatically cherry-picks merged PRs to release branches
when the appropriate label is applied.

### How to backport a PR

1. Create a PR targeting `main` and merge it.
2. Comment on the merged PR:
   ```
   @mergifyio backport release-v1
   ```
3. Mergify automatically creates a new PR cherry-picking the changes onto the
   target release branch.

This works with any existing release branch, no configuration changes needed.
