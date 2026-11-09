# sift

A local code review desk for agent-written changes. Agents explain their work with a small CLI:
notes pinned to the exact lines, files ranked by importance, and a numbered walkthrough. You read
it in a fast browser UI and send line comments straight back to the agent.

**Site and docs: https://sift.lakebed.app**

This repository hosts release binaries only.

## Install

```bash
curl -fsSL https://sift.lakebed.app/install.sh | sh
```

The installer picks the build for your OS and CPU, checks its SHA-256, installs
`~/.local/bin/sift`, and adds the Claude Code skill if `~/.claude` exists.

Or download a tarball from [Releases](https://github.com/kubilayjg/sift/releases), unpack it, and
put `sift` on your PATH. On macOS, if you downloaded it in a browser, run
`xattr -d com.apple.quarantine ~/.local/bin/sift` (the binary is not notarized).

| Platform | File |
| --- | --- |
| macOS, Apple Silicon | `sift-macos-arm64.tar.gz` |
| macOS, Intel | `sift-macos-x86_64.tar.gz` |
| Linux x86_64 (static) | `sift-linux-x86_64.tar.gz` |
| Linux arm64 (static) | `sift-linux-arm64.tar.gz` |

sift needs `git` at runtime and nothing else. On Windows, use the Linux build inside WSL.
