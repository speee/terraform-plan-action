# speee/terraform-plan-action

The `speee/terraform-plan-action` action is a CI action that runs `terraform plan` beside your pull requests and gives result summaries.

## Usage

```yaml
- uses: speee/terraform-plan-action@v1
  with:
    working-directory: terraform/dir/
```

## Inputs

### `working-directory`

**Required.**
The action supports the following inputs:

### `enable-lock`

Optional.
Relative path from repository root to your terraform root module. Default is `.`.

## Outputs

### `plan-stdout`

stdout of plan execution. Logs during plan are omitted.

### `plan-stderr`

stderr of plan execution.

### `replace-resources`

JSON strings of resources to be replaced.

An example output format is like below.

```
["aws_iam_user.foo","aws_iam_user.bar"]
```

### `create-resources`

JSON strings of resources to be created.
An example output format is same as `replace-resources`.

### `delete-resources`

JSON strings of resources to be deleted.
An example output format is same as `replace-resources`.

### `update-resources`

JSON strings of resources to be updated.
An example output format is same as `replace-resources`.

### `plan-has-changes`

A flat indicates that the plan command has changes.
