# Security policy

ReleaseCheck documentation must not weaken the project's security boundaries. Never add instructions that require installing an untrusted package, running its lifecycle scripts, invoking its build backend, or executing package code merely to inspect a release.

Report suspected vulnerabilities privately through the security process documented in the [core repository](https://github.com/ReleaseCheck/releasecheck/blob/main/SECURITY.md). Documentation-only issues may be opened in this repository unless the issue exposes sensitive information.

Documentation must describe ReleaseCheck as a deterministic evidence tool, not as malware detection, a vulnerability scanner, or a guarantee of package safety.

