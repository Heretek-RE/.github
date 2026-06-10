# Heretek-RE

Public-release tooling for offensive reverse-engineering research.

This org hosts scrubbed, vendor-neutral public versions of the Heretek reverse-engineering toolchain. Client names, engagement identifiers, per-target binary fingerprints, and host-path information are removed. Vendor names at the protection-family level (Denuvo, EAC, VMProtect, Themida, Arxan, StarForce, BattlEye, EOS, Steam CEG, etc.) are kept because they are the subjects the tools analyze, not the subjects of any specific engagement.

## Repos

| Repo | Purpose |
|---|---|
| [RE-Library](https://github.com/Heretek-RE/RE-Library) | Curated knowledge base for reverse engineering. Astro site + MCP server. Includes engines/, storefronts/, and protection/ catalogs. |
| [Android-RE](https://github.com/Heretek-RE/Android-RE) | APK triage, Frida hooking, MASVS-aligned reporting. 4 Python MCP servers + 1 TypeScript bridge. |
| [RE-AI](https://github.com/Heretek-RE/RE-AI) | The agent-space monorepo that orchestrates the per-MCP repos. |
| [RE-BREAKER](https://github.com/Heretek-RE/RE-BREAKER) | Bypass primitives and entitlement-emulation toolset. AGPL-3.0 + Offensive-Research-Use Clause. |
| `re-<name>` (30 repos) | Per-MCP-server repos, split out of the RE-AI monorepo for independent versioning. |

## License posture

- **Analytical tooling** (RE-Library, Android-RE, RE-AI agent-space, all 31 `re-*` MCP repos): MIT.
- **Bypass tooling** (RE-BREAKER): AGPL-3.0 + Offensive-Research-Use Clause. The `--license-acknowledge` CLI flag must be set before bypass primitives will execute.

## Contributing

See [CONTRIBUTING.md](https://github.com/Heretek-RE/.github/blob/main/CONTRIBUTING.md).

## Code of conduct

See [CODE_OF_CONDUCT.md](https://github.com/Heretek-RE/.github/blob/main/CODE_OF_CONDUCT.md). Contributor Covenant v2.1.

## Reporting security issues

See [SECURITY.md](https://github.com/Heretek-RE/.github/blob/main/SECURITY.md). Private disclosure via GitHub Security Advisories.

## Out-of-scope use

This is research tooling. The bypass-adjacent tools require you to affirm — under penalty of perjury — that you have the legal right to reverse-engineer the target binary. Piracy, unauthorized access, and surveillance of non-consenting individuals are out of scope. The CLI will refuse to run without an explicit `--license-acknowledge` flag.
