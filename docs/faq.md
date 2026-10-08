# FAQ and troubleshooting

## Does ReleaseCheck install the package?

No. The verification boundary excludes package installation, lifecycle scripts, build backends, setup code, and arbitrary package execution.

## Does a difference mean the package is malicious?

No. Build, bundling, compilation, ignored files, generated files, and packaging rules can create legitimate differences. ReleaseCheck reports observations and warnings; it does not turn a diff into a malware verdict.

## Why is a result incomplete?

Typical causes are missing repository metadata, an unavailable or ambiguous source reference, a failed download, a package format that cannot be compared directly, or unavailable provenance evidence. Inspect the JSON report for the exact evidence and limitation.

## Which ecosystems are supported?

The v0.1 scope is npm and PyPI. Other ecosystems are future discovery-gated work and are not implied by the current documentation.

## Where should I report an issue?

Report verifier, architecture, and security issues in the [core repository](https://github.com/ReleaseCheck/releasecheck/issues). Report Action behavior in the [Action repository](https://github.com/ReleaseCheck/releasecheck-action/issues). Report documentation defects here.

