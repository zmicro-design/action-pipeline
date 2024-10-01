# GitHub Action to Docker Build

![https://github.com/zmicro-design/action-pipeline](https://img.shields.io/github/v/release/zmicro-design/action-pipeline)
![https://github.com/zmicro-design/action-pipeline](https://github.com/zmicro-design/action-pipeline/workflows//Publish/badge.svg)

### Usage

| option | required | description |
| ------ | -------- | ----------- |
| config | false | specify pipeline config, default: .go-idp/pipeline.yaml |
| workdir   | false | specify the workdir, default: current dir |
| allow-envs | false | specify build allow-envs |
| allow-all-env | false | specify whether to allow all env into the pipeline |

### Example

```yml
name: CI

on: [push]

jobs:
  build:
    name: Test
    runs-on: ubuntu-latest
    steps:
      - name: Docker Build
        uses: zmicro-design/action-pipeline@v1
        with:
          workdir: /_w/pipeline/pipeline
```

### License

[MIT](./LICENSE)
