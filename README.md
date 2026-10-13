# Organization-wide community health defaults

This **public** repository hosts Dirigo Strategic Advisors' organization-wide GitHub
defaults. GitHub uses these files as the default for any repository in the
`Dirigo-Strategic-Advisors` organization that does not define its own.

## Contents

| File | Purpose |
|------|---------|
| `SECURITY.md` | Vulnerability disclosure policy (default) |
| `CONTRIBUTING.md` | Contribution defaults (default) |
| `CODE_OF_CONDUCT.md` | Community code of conduct (default) |
| `SUPPORT.md` | Where to get help (default) |
| `ISSUE_TEMPLATE/` | Default issue forms |
| `PULL_REQUEST_TEMPLATE.md` | Default pull request template |
| `.github/workflows/` | **Reusable** CI/CD workflows callable by every repository |

## Important: this repository is public

Only **non-confidential** content belongs here. **The engineering handbook, ADRs,
architecture, and any proprietary documentation live in the private
`engineering-standards` repository**, not here.

## Using the reusable workflows

Any repository in the organization can call these:

```yaml
# .github/workflows/ci.yml
name: CI
on:
  pull_request:
  push:
    branches: [main]
permissions:
  contents: read
jobs:
  dotnet:
    uses: Dirigo-Strategic-Advisors/.github/.github/workflows/dotnet-ci.yml@main
    with:
      dotnet-version: "9.0.x"
  angular:
    uses: Dirigo-Strategic-Advisors/.github/.github/workflows/angular-ci.yml@main
    with:
      node-version: "22.x"
```

Available reusable workflows:

- `dotnet-ci.yml` — restore/build/test .NET with coverage
- `angular-ci.yml` — install/lint/test/build Angular (+ optional Playwright e2e)
- `deploy-environment.yml` — environment-gated deployment foundation
- `dependency-review.yml` — fail PRs that add vulnerable dependencies
  (**public repos or repos with GitHub Advanced Security only** — it fails on private
  repos without GHAS)
