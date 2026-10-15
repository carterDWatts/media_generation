# Character video production

Status: foundation installed; generation stages are not implemented yet.

Compute direction: the home server coordinates jobs and stores results. Its GPU is reserved for another AI project. Prefer hosted generation and external rendering; providers are still to be selected.

The project lives at `/home/carter/media_project` on `carter@100.115.73.59`.

## Working agreement

Build one reviewable stage at a time. Start with a small batch of theme and plot candidates; Carter reviews before we develop script generation. Keep genre and personality open. See [creative framework](docs/character-framework.md) and [pipeline graph](docs/production-pipeline.mmd).

Use AI for creative work and judgment. Use code for validation, caching, file management, timing, assembly, rendering, and notifications. Avoid automatic critique loops and repeated calls for unchanged inputs. Model choices, budgets, and notification delivery remain open.

## Tools

All newly installed tools live under `/home/carter/.local/share/media-project-tools`. No system packages or shell startup files were changed.

- Node.js 24.22.0 (official Linux x64 release; SHA-256 verified)
- npm bundled with Node
- Codex CLI 0.162.1 (version pinned in its user-local npm installation)
- Existing system Python 3.12.3 is available; no Python dependencies installed yet.

From an SSH session:

```bash
cd /home/carter/media_project
source scripts/env.sh
codex --version
codex login --device-auth
codex login status
```

Complete the device login in your own browser. If disabled, enable device code login in ChatGPT security settings. Do not put credentials in this repository. Official instructions: https://learn.chatgpt.com/docs/auth

Subscription sign-in is supported for Codex. Access and billing for each future text/image/audio/video integration must be verified separately before wiring it into the pipeline. No server-side generation calls have been made during foundation setup.

## Next review

Agree on the input brief and output format for theme/plot experiments before implementing that stage. Proposed output: a few concise concepts showing personality, audience relationship, visual action, recurring appeal, and one sample episode. Later stages should retain their inputs and outputs so revisions can rerun only affected work.
