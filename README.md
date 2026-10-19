# ReleaseCheck Documentation

![Core CI](https://github.com/ReleaseCheck/releasecheck/actions/workflows/ci.yml/badge.svg?branch=main) ![Action CI](https://github.com/ReleaseCheck/releasecheck-action/actions/workflows/ci.yml/badge.svg?branch=main) ![Apache-2.0](https://img.shields.io/badge/license-Apache--2.0-blue)

Guides for using [ReleaseCheck](https://github.com/ReleaseCheck/releasecheck), a tool that compares published npm and PyPI packages with their claimed source releases.

[Core and implementation](https://github.com/ReleaseCheck/releasecheck) · [GitHub Action](https://github.com/ReleaseCheck/releasecheck-action) · [Documentation issues](https://github.com/ReleaseCheck/releasecheck-docs/issues)

## Choose a path

| If you want to... | Start here |
| --- | --- |
| Understand the evidence ReleaseCheck collects | [What is ReleaseCheck?](docs/what-is-releasecheck.md) |
| Build it and verify a package | [Quickstart](docs/quickstart.md) |
| Select commands and output formats | [CLI usage](docs/cli-usage.md) |
| Interpret a verdict or file difference | [Understanding results](docs/results.md) |
| Add checks to continuous integration | [CI usage](docs/ci.md) |
| Use the official GitHub Action | [GitHub Action](docs/github-action.md) |
| Understand what the tool cannot establish | [Limitations](docs/limitations.md) |
| Troubleshoot or find the right issue tracker | [FAQ](docs/faq.md) |

## How the repositories fit together

```mermaid
flowchart LR
    Core[Core CLI and verification engine] --> Action[GitHub Action integration]
    Core --> Guides[User documentation]
    Action --> Guides
```

The core repository owns implementation, tests, fixtures, architecture, security decisions, roadmap, and release status. The Action invokes a released core binary. This repository explains user workflows and links to the technical source of truth. Start with the [quickstart](docs/quickstart.md) if you want to run a check, or [What is ReleaseCheck?](docs/what-is-releasecheck.md) if you want the evidence model first.

## Current status

ReleaseCheck `v0.1.2` is publicly released, and the official Action has completed a live end-to-end run against that release. The guides describe supported behavior and limitations without claiming that provenance or package safety is fully verified. For the precise overlap boundary with registry, provenance, reproducibility, and security tools, see the [core positioning document](https://github.com/ReleaseCheck/releasecheck/blob/main/docs/POSITIONING.md).

## Contributing

See [CONTRIBUTING.md](CONTRIBUTING.md). Documentation issues belong here; core verifier issues belong in the [core repository](https://github.com/ReleaseCheck/releasecheck/issues), and Action issues belong in the [Action repository](https://github.com/ReleaseCheck/releasecheck-action/issues).
