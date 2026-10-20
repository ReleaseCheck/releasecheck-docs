# Attestations and Provenance

ReleaseCheck can report provenance-shaped evidence alongside its deterministic artifact/source comparison, but it is not a replacement for Sigstore, SLSA, GitHub artifact attestations, npm provenance, or PyPI attestations.

## How the pieces fit

| Evidence system | What it can establish | What ReleaseCheck adds | Boundary |
| --- | --- | --- | --- |
| Sigstore | Signature and transparency-log evidence when verified with Sigstore tooling | The selected package artifact's inventory, hashes, source claim, and comparison | ReleaseCheck does not verify Fulcio, Rekor, TUF, DSSE, or certificate policy in v0.1.2 |
| SLSA | Provenance about a build's materials, builder, and build instructions | Release-integrity observations for the registry artifact | ReleaseCheck does not issue or independently verify SLSA provenance in v0.1.2 |
| GitHub artifact attestations | GitHub workflow/build provenance for an artifact | A report that can be compared with package and source evidence | A GitHub attestation does not by itself prove npm/PyPI source equivalence or package safety |
| npm/PyPI attestations | Registry-specific provenance/signature evidence | Common evidence and limitation reporting across npm and PyPI | Cryptographic trust-root verification remains outside the v0.1.2 boundary |

For the exact verification commands and primary references, see the [core attestation interoperability document](https://github.com/ReleaseCheck/releasecheck/blob/main/docs/ATTESTATIONS.md).

The safe interpretation is additive: verify an attestation with its ecosystem's official verifier, then use ReleaseCheck to inspect what was published and how it relates to the claimed source release. A `MATCH` result is not a malware or trust decision, and a difference is not automatically malicious.
