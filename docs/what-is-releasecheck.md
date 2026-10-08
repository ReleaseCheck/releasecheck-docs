# What Is ReleaseCheck?

ReleaseCheck examines the relationship between a published npm or PyPI package and its claimed source release.

```text
registry release
      |
published artifact
      |
contents and hashes
      |
claimed source repository
      |
claimed git reference
      |
source snapshot
      |
deterministic comparison
      |
security observations and provenance evidence
      |
human and machine-readable report
```

The tool reports deterministic evidence, observations, warnings, and limitations. A difference between source and artifact is not automatically proof of maliciousness because legitimate packaging transforms source files.

ReleaseCheck does not install packages, execute package code, run lifecycle scripts, execute Python build backends, detect all malware, scan vulnerabilities, generate SBOMs, reproduce arbitrary builds, or implement Sigstore or SLSA.

See the [core architecture](https://github.com/ReleaseCheck/releasecheck/blob/main/docs/DESIGN.md) and [security policy](https://github.com/ReleaseCheck/releasecheck/blob/main/SECURITY.md) for technical boundaries.
