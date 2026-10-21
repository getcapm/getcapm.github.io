# Getting Started

## Running a package

The `run` command runs a package inside the current directory. 

For example, to show the help screen for JSHint (a linter for JavaScript):

```shell
capm run jshint --help
```

Only the first time a package is used, CAPM will build the Docker image.

To run JSHint on the `src` directory:

```shell
capm run jshint src
```

Specific package configuration files are not managed by CAPM and can be stored
in the codebase as usual.

## Package configuration

A file called `.capm.yml` can be used to configure multiple packages, for
example:

```yaml
packages:
  - mypy
  - ruff
```

New packages can be added using the `capm add` command. Packages can be removed
using the `capm remove` command. Packages can be listed using the `capm list`
command`

## Finding packages

A list of packages can be found on the [Packages](/packages/) page.

## Running in GitHub Actions

There's a GitHub Action available
([capm-action](https://github.com/getcapm/capm-action)) that you can add to
your CI workflow. This action will run all configured CAPM packages.

An example of a GitHub Actions workflow using the CAPM action:

```yaml
name: code-analysis

on:
  push:
    branches:
      - main
  pull_request:
    branches:
      - main

jobs:
  code_analysis:
    runs-on: ubuntu-latest
    steps:
      - name: Checkout sources
        uses: actions/checkout@v7

      - name: Run CAPM
        uses: getcapm/capm-action@v1
```
