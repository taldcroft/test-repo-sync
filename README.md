# test-repo-sync docs 5

branch 1

branch 3.0

Basic sync workflow

- `git checkout main`
- `git pull origin --no-tag`  # Prevent getting pre-release tags. This pulls branches as well
- Get all the tags from GitHub API
  - Compare release (prerelease=False and draft=False) tags to those in the repo
  - `git pull origin <tag>` for each one
- `git checkout <latest-tag>`
