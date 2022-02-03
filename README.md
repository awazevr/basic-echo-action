# basic-action-action
This is a GitHub Action meant to be used as a [composite action](https://docs.github.com/en/actions/creating-actions/creating-a-composite-action) within an existing workflow. This action encapsulates setting for outputting an input to workflow build log. 


## Inputs

### `your_name`

**Required** Name to be output to build log

## Usage
You can use this composite Action in your own workflow by adding:

```yml
name: Test (Echo Action)

on:
  workflow_dispatch:
  schedule:
    - cron: "0 9,18 * * 1-5"

jobs:
  echo-action-test:
    name: Output unput to build log
    runs-on: ubuntu-latest
    steps:
       - name: echo action test
          uses: awazevr/basic-echo-action@v1.0.1
          with:
            your_name: "Hello Mum"
```

