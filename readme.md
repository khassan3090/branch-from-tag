
# Create Branch From TAG GitHub Action

This action creates a new branch from a specific tag.

## Inputs

### `branch`

**Optional** The name of the branch to create. Default `"release-candidate"`.

### `from`

**Required** 
The name of the tag from which new branch will be created.

tag should be prefix with tags/your-tag.

branch you can provide directly.

## Example usage

create branch from tag
```
- name: creating rc branch
  uses: khassan3090/create-branch@1.0.0
  env:
   GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
   branch: release
   tag: tags/v0.0.7
```

create branch from specific ref (branch)
```
- name: creating rc branch
  uses: khassan3090/create-branch@1.0.0
  env:
   GITHUB_TOKEN: ${{ secrets.GITHUB_TOKEN }}
  with:
   branch: release
   tag: test
```
