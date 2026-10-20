# Quickstart

ReleaseCheck `v0.1.2` is available as a checksum-published GitHub release. Use a pinned archive for a quick start, or build from the tagged source when Go 1.25 or newer is available.

## Release archive

1. Open the [v0.1.2 release](https://github.com/ReleaseCheck/releasecheck/releases/tag/v0.1.2).
2. Download the archive for your platform and `SHA256SUMS`.
3. Verify the archive against `SHA256SUMS` before extracting it.
4. Put `releasecheck` or `releasecheck.exe` on `PATH` and confirm `releasecheck --version`.

The core repository also contains local Homebrew and Scoop metadata. Those files are not yet official tap/bucket indexes.

For a pinned Go-module installation instead of a release archive:

```text
go install github.com/ReleaseCheck/releasecheck/cmd/releasecheck@v0.1.2
```

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
