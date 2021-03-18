# Update File Action

This Action lets you Create/Update/Delete a file in a repository other than the one running the Action.

## Inputs

### `github-token`

**Required** GitHub Token to use to access the target repository.

### `owner`

**Required** Owner of the target repository.

### `repository`

**Required** Target repository name.

### `target-file-path`

**Required** Path of file in the repository to create/update/delete.

### `commit-message`

**Required** The commit message to use. Default `"Automated workflow commit."`.

### `content`

**Required** If creating/updating, the content for the file. Default `""`.

### `delete`

**Required** If the file should be deleted, instead of created/updated. Default `"false"`.

## Example usage

```yaml
uses: spacelift-io/update-file-action@v1.0.0
with:
  github-token: ${{ secrets.GH_TOKEN }}
  owner: spacelift-io
  repository: update-file-action
  target-file-path: 'test/main2.md'
  content: |
    Amazing
    Great
    Content
```
