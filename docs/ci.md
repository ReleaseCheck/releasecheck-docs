# CI usage

ReleaseCheck is suitable for CI when a workflow needs deterministic evidence about a published npm or PyPI release. Use the JSON or SARIF output for automation and choose a policy for `MATCH`, `REVIEW`, `INCOMPLETE`, and operational failures that matches the repository's risk tolerance.

The core CLI must be installed from a pinned release or built from a reviewed revision. Do not download an unpinned binary in a security-sensitive workflow. The official [GitHub Action](https://github.com/ReleaseCheck/releasecheck-action) provides checksum-verified acquisition of a released core binary for Ubuntu runners.

ReleaseCheck does not install the package under inspection and does not execute package lifecycle scripts or build backends.

## Example

```yaml
- name: Verify published release
  uses: ReleaseCheck/releasecheck-action@main
  with:
    ecosystem: npm
    package: example-package
    releasecheck-version: 0.1.0
    format: sarif
    output: releasecheck.sarif
```

Pin the Action to a reviewed commit or release tag in production, and keep the core version explicit.

