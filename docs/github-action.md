# GitHub Action

The [official Action repository](https://github.com/ReleaseCheck/releasecheck-action) is a thin integration layer. It downloads a selected ReleaseCheck core release, verifies the published SHA-256 checksum, executes the binary with the requested arguments, and propagates its exit status.

It does not contain a second verification engine. This keeps registry behavior, archive handling, comparison semantics, and report contracts in the [core repository](https://github.com/ReleaseCheck/releasecheck).

The Action currently targets Ubuntu runners and supports the core's `npm` and `pypi` paths. A live end-to-end workflow requires a matching public core release; the project is currently pre-v0.1.0 and its independent re-audit is in progress.
