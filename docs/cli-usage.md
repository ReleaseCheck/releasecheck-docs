# CLI Usage

The core CLI uses the Go standard flag parser, so options appear before positional package arguments.

## npm

```text
releasecheck verify npm PACKAGE
releasecheck verify npm PACKAGE VERSION
releasecheck verify npm --json --output report.json PACKAGE VERSION
```

## PyPI

```text
releasecheck verify pypi PACKAGE
releasecheck verify pypi PACKAGE VERSION
releasecheck verify pypi --artifact PACKAGE-VERSION-py3-none-any.whl PACKAGE VERSION
```

## Output options

- Human-readable output is the default.
- `--json` emits JSON schema `1.0`.
- `--sarif` emits SARIF `2.1.0`.
- `--output PATH` writes the report with restrictive local permissions.
- `--timeout DURATION` bounds registry and source operations.
- `--artifact FILENAME` selects a PyPI release file.

`--json` and `--sarif` cannot be used together. Exit code `0` means `MATCH`; `1` means `REVIEW` or `INCOMPLETE`; `2` means usage error; and `3` means operational or rendering error.
