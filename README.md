# publish-docker-action
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
      - uses: dioptra-io/publish-docker-action@v1
        with:
          password: ${{ secrets.GITHUB_TOKEN }}
```

### Inputs

Name        | Default
------------|--------
`image`     | `${{ github.repository }}`
`registry`  | `ghcr.io`
`username`  | `${{ github.actor }}`
`password`  | None
`platforms` | `linux/amd64`
