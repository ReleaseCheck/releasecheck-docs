# Limitations

ReleaseCheck reports deterministic release-integrity evidence. It does not prove that a package is safe, non-malicious, or free of vulnerabilities.

Important limitations in the current pre-v0.1.0 audit-required state include:

- source-to-commit binding is not yet a complete cryptographic trust decision;
- provenance may be detected or parsed without being sufficient to establish a stronger conclusion;
- source and artifact differences can be legitimate build transformations;
- wheels and other compiled artifacts are not expected to equal a source tree byte-for-byte;
- missing metadata, unavailable tags, and network failures produce incomplete evidence;
- a registry or repository may change after evidence is collected;
- the current Action integration is prepared for a release but cannot complete a live workflow before the first public core release;
- ReleaseCheck does not replace vulnerability scanners, SBOM tooling, Sigstore, SLSA, or registry infrastructure.

Read the core repository's `FINAL_AUDIT.md` and `docs/DESIGN.md` for the current detailed boundaries. Limitations are release-blocking information, not footnotes to hide from a report.

