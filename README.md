# publish-docker-action

[![Tests](https://github.com/dioptra-io/publish-docker-action/actions/workflows/tests.yml/badge.svg)](https://github.com/dioptra-io/publish-docker-action/actions/workflows/tests.yml)

Composite action to build and push a Docker image to a registry.

## Usage

```yaml
name: Docker
on: [push]
jobs:
  build:
    runs-on: ubuntu-latest
    steps:
      - uses: actions/checkout@v2
      - uses: dioptra-io/publish-docker-action@v2
        with:
          password: ${{ secrets.GITHUB_TOKEN }}
```

### Inputs

Name        | Default
------------|--------
`context`   | `.`
`image`     | `${{ github.repository }}`
`registry`  | `ghcr.io`
`username`  | `${{ github.actor }}`
`password`  | None
`platforms` | `linux/amd64`
`push`      | `true`
