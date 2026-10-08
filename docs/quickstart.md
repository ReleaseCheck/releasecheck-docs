# Quickstart

ReleaseCheck is currently built from the core repository or installed from a future versioned release. No public `v0.1.0` release exists yet.

## Build from source

With Go 1.25 or newer:

```text
git clone https://github.com/ReleaseCheck/releasecheck.git
cd releasecheck
go build -trimpath -o releasecheck ./cmd/releasecheck
```

## Verify a package

```text
releasecheck verify npm NAME
releasecheck verify npm NAME VERSION
releasecheck verify pypi NAME
releasecheck verify pypi NAME VERSION
```

Useful options:

```text
--json
--sarif
--output PATH
--artifact FILENAME
--timeout DURATION
```

The command downloads metadata and artifacts for inspection. It does not install or execute the package.
