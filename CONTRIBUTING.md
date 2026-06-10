# Contributing to Heretek-RE

Thanks for your interest in contributing to the Heretek reverse-engineering toolchain. This is a public-release org; the rules of engagement are different from a private research repo.

## Scope of contributions

**In scope:**
- Bug fixes, performance improvements, and documentation updates to the analytical tooling (RE-Library, Android-RE, the analytical `re-*` MCP repos, the RE-AI agent-space orchestration).
- New analytical MCP servers that wrap open-source RE tools (Ghidra plugins, Frida gadgets, pwntools, etc.).
- New knowledge-base entries for RE-Library (techniques, anti-analysis bypass, packer writeups).
- Improvements to the agent-space orchestration in Heretek-RE/RE-AI.

**Out of scope:**
- New bypass primitives or per-vendor entitlement emulators. The bypass-adjacent tooling is frozen at its current level; we do not add new vendor bypass code to the public org.
- Any reference to specific game titles, publisher names in per-engagement context, or engagement identifiers in source code, comments, or docs. The CI blacklist enforces this; PRs with such references will be auto-failed.

## Process

1. **Fork the repo** you want to contribute to.
2. **Create a feature branch** from `main`.
3. **Make your change.** Follow the existing code style. Add tests where applicable.
4. **Verify locally:**
   - `redact.sh --audit .` from the repo root must return exit 0. (For repos that ship the scrub tool; otherwise CI will run it.)
   - The CI workflow must pass (Astro build, Python tests, etc.).
5. **Open a PR.** The PR template will prompt for the standard checklist.
6. **A maintainer reviews** the PR. The CI blacklist check must pass before merge.
7. **Squash-merge** to `main` with a Conventional Commits-style message.

## Commit message conventions

Use Conventional Commits:

- `feat:` for new features
- `fix:` for bug fixes
- `docs:` for documentation only
- `refactor:` for code changes that don't add features or fix bugs
- `test:` for adding or updating tests
- `chore:` for maintenance / tooling changes

## The "no engagement references" rule

This org's public repos are scrubbed of:
- Specific game titles (007 First Light, Crimson Desert, Football Manager 26, etc.)
- Publisher names in per-engagement context (Sunblink, Sports Interactive, Pearl Abyss, IO Interactive, etc.)
- Engagement identifiers (SOW codes, MRTEA references, "live-fire" phrasing, specific engagement dates)
- Host-fingerprint information (specific IPs, ssh key references, host paths)
- Per-engagement output paths

If your PR contains any of these — in code, comments, docstrings, tests, or documentation — the blacklist check will fail. The reviewer will ask you to remove them before merge.

Vendor names at the **protection-family level** (Denuvo, EAC, VMProtect, Themida, Arxan, StarForce, BattlEye, EOS, Steam CEG) are fine — they are the subjects the tools analyze, not engagement identifiers.

## Bypass-adjacent repos

If you're contributing to one of the bypass-adjacent repos (`re-game-ac-bypass`, `re-eos-bypass`, `re-origin-stub-drop`, `re-steam-stub-unwrap`, `re-encrypted-vm-tamper`, `re-drm-fingerprint`, `re-hypervisor-detect`, or `RE-BREAKER` itself):

- The `--license-acknowledge` CLI gate is part of the contract. PRs that remove or weaken it will not be merged.
- The `LICENSE-OFFENSIVE.md` terms are non-negotiable. The license is AGPL-3.0 + Offensive-Research-Use Clause, not MIT.
- Out-of-scope uses (piracy, unauthorized access, surveillance of non-consenting individuals) are explicitly forbidden by the license and the Contributor Covenant.

## Code of conduct

See [CODE_OF_CONDUCT.md](./CODE_OF_CONDUCT.md). Contributor Covenant v2.1.

## Security disclosures

See [SECURITY.md](./SECURITY.md). Private disclosure via GitHub Security Advisories.
