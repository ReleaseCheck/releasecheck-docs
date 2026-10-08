# ReleaseCheck Documentation

This repository contains the curated public documentation for [ReleaseCheck](https://github.com/ReleaseCheck/releasecheck), a deterministic release-integrity analysis tool for npm and PyPI.

## Start here

- [What is ReleaseCheck?](docs/what-is-releasecheck.md)
- [Quickstart](docs/quickstart.md)
- [CLI usage](docs/cli-usage.md)
- [Understanding results](docs/results.md)
- [CI usage](docs/ci.md)
- [GitHub Action](docs/github-action.md)
- [Limitations](docs/limitations.md)
- [FAQ and troubleshooting](docs/faq.md)

The core repository remains the source of truth for implementation, architecture, security decisions, roadmap, and contributor engineering guidance. The [GitHub Action repository](https://github.com/ReleaseCheck/releasecheck-action) provides CI integration without duplicating the verification engine.

## Current status

ReleaseCheck is post-Phase-14 audit, `AUDIT REQUIRED`, and pre-v0.1.0. The documentation describes the current implementation honestly; it does not claim that v0.1.0 has been released or that provenance and package safety are fully verified.

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Documentation issues belong here; core verifier issues belong in the [core repository](https://github.com/ReleaseCheck/releasecheck/issues), and Action issues belong in the [Action repository](https://github.com/ReleaseCheck/releasecheck-action/issues).
