# Check Unacceptable Language

This GitHub Action runs a script to check for unacceptable language in your repository.

## Usage

Include the action in your workflow. Add an [unacceptable-language.txt](https://github.com/feather-actions/check-language/blob/main/unacceptable-language.txt) file to your repository to specify which unacceptable language patterns to use during the search. If no file added, then the default is used.

```yaml
- uses: feather-actions/check-language@0.0.3
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
        uses: feather-actions/check-language@0.0.3
```