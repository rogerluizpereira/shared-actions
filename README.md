## Shared GitHub Actions

This repository contains reusable GitHub Actions.

### Available Actions
- `Deploy Action`: Deploys the application to a server.

### Usage

```yaml
name: Deploy Workflow
on: push
jobs:
  deploy:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout Code
        uses: actions/checkout@v3

      - name: Deploy
        uses: USERNAME/shared-actions/.github/actions/deploy@v1
        with:
          environment: production
