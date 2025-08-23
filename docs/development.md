# Development

After installing dependencies with `uv sync`, CAPM can be run from the
repository root like this:

```shell
uv run capm
```

For example, to run the `tokei` package, run:

```shell
uv run capm run tokei
```

## Local installation using pipx

To install the development repository locally in editable mode run:

```shell
pipx install --force --editable .
```

To install the `main` branch locally run:

```shell
pipx install git+https://github.com/getcapm/capm.git
```

Or to install another branch locally run:

```shell
pip install git+https://github.com/getcapm/capm.git@issue-123
```

## Building the binary distribution

Generate a self-contained binary:

```shell
uv run poe bundle
```

## Static documentation

Generating the static documentation:

```shell
uv run mkdocs build
```

See the output:

```shell
uv run mkdocs serve
```
