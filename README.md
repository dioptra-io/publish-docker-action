# publish-docker-action
Composite action to build and push a Docker image to a registry.

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
