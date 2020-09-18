# speee/terraform-plan-action

The `speee/terraform-plan-action` action is a CI action that runs `terraform plan` beside your pull requests and gives result summaries.

## Usage

```yaml
- uses: speee/terraform-plan-action@v1
  with:
      terraform_version: 0.12.29
```

## Inputs

The action supports the following inputs:

- `working-directory` - (optional) Relative path from repository root to your terraform root module (default `.`).

- `aws-access-key-id` - (optional) Used when performing `terraform plan` to your AWS environment.

- `aws-secret-access-key` - (optional)

- `terraform-version` - (optional) The version of Terraform CLI to install. Defaults to `latest`.

- `github-token` - Used when writing comments on your pull request.
