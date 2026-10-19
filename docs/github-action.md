# GitHub Action

The [official Action repository](https://github.com/ReleaseCheck/releasecheck-action) is a thin integration layer. It downloads a selected ReleaseCheck core release, verifies the published SHA-256 checksum, executes the binary with the requested arguments, and propagates its exit status.

It does not contain a second verification engine. This keeps registry behavior, archive handling, comparison semantics, and report contracts in the [core repository](https://github.com/ReleaseCheck/releasecheck).

The Action currently targets Ubuntu runners and supports the core's `npm` and `pypi` paths. The public `v0.1.2` core release has passed the tag-driven release workflow, and the Action E2E workflow has passed against that exact released binary. The Action repository contains a manual E2E workflow that consumes an explicit released version; future changes must preserve checksum verification and exit-status propagation.
