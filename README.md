# Check Merged

Check if it has been merged.

## Usage:

The action works only with pull_request event.

### Inputs

- `token` - The GITHUB_TOKEN secret.
- `originBranch` - Origin branch. (default: `staging`)

## Example

```yaml
name: Check merged
on:
  pull_request:
    branches:
      - master

jobs:
  check-staging:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v1
      - uses: SonicGarden/check-merged-action@v1
        with:
          token: ${{ secrets.GITHUB_TOKEN }}
```

![Demo](https://i.gyazo.com/1a7f81b217002632e64268a3407777a1.png)
