# SECURE URL
# 

This action is to scan the url that you input

## Inputs

### `who-to-greet`

**Required** The URL that need to scan `"URL"`.

## Outputs

### `time`

The time that the scan URL finish scanning

## Example usage

```yaml
on:
  workflow_dispatch:
    inputs:
      url:
        description: 'URL to check'
        required: true
        type: string

jobs:
  call-external-workflow:
    uses: Accenture-CIO-ApplicationCodeSecurity/PreventSecureURL_181564/.github/workflows/CheckHeader.yml@main
    with:
      url: ${{ github.event.inputs.url }}

```
