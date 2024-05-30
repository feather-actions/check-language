# Check Unacceptable Language

This GitHub Action runs a script to check for unacceptable language in your repository.

## Usage

Include the action in your workflow.

```yaml
- uses: feather-actions/check-language@0.0.1
```
Full example:

```yaml
on: [push]

jobs:
  check-language:
    runs-on: macos-latest

    steps:
      - name: Checkout
        uses: actions/checkout@v4
        with:
          fetch-depth: 1
  
      - name: Check Unacceptable Language
        uses: feather-actions/check-language@0.0.1
```

