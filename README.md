# action-pdk-test-unit

This action runs `pdk test unit` on your codebase and fails the step if there are test failures.

## Usage

To use the action add the following step to your workflow file (e.g. `.github/workflows/pdk-test-unit.yml`)

```yaml
name: Run pdk test unit

on:
  - push
  - pull_request

jobs:
  build:
    runs-on: ubuntu-latest
    steps:
    - name: Clone repository
      uses: actions/checkout@v2

    - name: Run unit tests
      uses: puppets-epic-show-theatre/action-pdk-test-unit@v1
      with:
        puppet-version: ""
        # [optional]
        # A string indicating the Puppet version to validate against, such as "5.4.2" or "5.5".
        pe-version: ""
        # [optional]
        # A string indicating the PE version to validate against, such as "2017.3.5" or "2018.1".
```
