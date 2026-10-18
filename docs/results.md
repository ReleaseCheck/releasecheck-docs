# Understanding Results

ReleaseCheck produces evidence, not a universal safe/unsafe label.

## Verdicts

- `MATCH`: available comparison evidence is identical and no warning or limitation prevents that result.
- `REVIEW`: differences, warnings, invalid evidence, or insufficient provenance require review.
- `INCOMPLETE`: important source, git, comparison, or other evidence was unavailable.
- `ERROR`: an operational or rendering failure occurred.

`MATCH` does not prove that code is safe. `REVIEW` does not prove maliciousness.

Machine-readable reports also include a stable `reason_code`, `explanation`, `evidence_missing`, `evidence_conflicts`, and `recommended_action`. These fields explain the evidence state and next review step; they do not turn ReleaseCheck into a malware detector or trust authority.

## Comparison categories

Reports can identify identical files, source-only files, artifact-only files, modified files, type changes, and unverifiable files. Wheels, compiled extensions, bundled files, generated files, and documentation can legitimately differ from source.

## Evidence categories

Reports distinguish known facts, unavailable evidence, invalid metadata, security observations, limitations, and parsed provenance. Provenance may be structurally bound to an artifact while still being marked insufficient because ReleaseCheck has not verified the full signature and trust chain.
