## How to get a list of changed files in pull request

`gh pr view --json files --jq '.files[].path'`

#### Need to be installed beforehead:
- `gh` - github CLI
- `jq` - CLI JSON processor
