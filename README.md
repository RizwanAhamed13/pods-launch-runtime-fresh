# PODS user compute

This public repository supplies the runtime environment for PODS launches in your own GitHub Codespaces account. It contains no application source or credentials.

PODS builds supported applications on its server before launch. After you authorize GitHub, PODS creates or resumes your Codespace, delivers a verified launch artifact over authenticated SSH, and opens the application on port 8080. No application build or dependency installation runs in the Codespace.

The runtime uses the official Node.js 24 Bookworm development image pinned by digest and the official SSH server feature required by GitHub CLI. Codespaces installs that runtime feature during initial environment setup; cold provisioning is controlled by GitHub and is not guaranteed to finish in 20 seconds.

Only the generic runtime is public. Application artifacts arrive separately from PODS. The forwarded port remains private to your GitHub account. Your account owns the Codespace and its quota and costs; PODS requests a 15-minute idle timeout and a one-day stopped-environment retention period.

Configuration sources: [Node image](https://github.com/devcontainers/images/tree/main/src/javascript-node), [SSH requirement](https://cli.github.com/manual/gh_codespace_ssh).
