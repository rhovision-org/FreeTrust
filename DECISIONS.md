# Decisions

FreeTrust spans several repos, and each one records its own decisions in its
own way. This file indexes those records and keeps the decisions that span
more than one repo.

## Where each repo records decisions

| Repo | Decision record | What it covers |
| --- | --- | --- |
| BYOID | [DECISIONS.md](https://github.com/rhovision-org/BYOID/pull/20) (proposed) | Identity design choices: DID method, keys, contracts, credentials |
| rholo | [AGENTS.md](https://github.com/rhovision-org/rholo/blob/dev/AGENTS.md) and the [findings register](https://github.com/rhovision-org/rholo/blob/dev/spec/AUDIT.md) | Binding intent and formal specification for the node; audit findings and their resolution |
| quantum-logical-framework | [Philosophy.md](https://github.com/rhovision-org/quantum-logical-framework/blob/main/Philosophy.md) and [ScientificApproach.md](https://github.com/rhovision-org/quantum-logical-framework/blob/main/ScientificApproach.md) | Founding commitments, and the rules for promoting or rejecting claims |
| quantum-os | [Manifesto.md](https://github.com/rhovision-org/quantum-os/blob/main/Manifesto.md) and [SECURITY.md](https://github.com/rhovision-org/quantum-os/blob/main/SECURITY.md) | Why rooms are off-chain by default and capability-based; the security model |
| rhogov | [README principles](https://github.com/rhovision-org/rhogov#readme) and [process-orchestration.md](https://github.com/rhovision-org/rhogov/blob/main/docs/process-orchestration.md) | State in contracts, computation in natives, no policy in contracts; how councils decide |

A decision that affects only one repo goes in that repo's record. A decision
that changes how two or more repos fit together goes below, with links to
the issues in each repo that carry it out.

## Cross-repo decisions

Newest first.

| Date | Decision | Why | Where |
| --- | --- | --- | --- |
| 2026-11-09 | This repo holds the capability map and cross-repo decisions; code lives in the project repos | The map spans five repos, and no one of them should own the whole vision | This repo |
| 2026-11-09 | MrE is built once and shared: spec and proofs in QLF, a deterministic crate in quantum-os, a native in rholo | Rooms, governance and identity all need the same update, and nodes must agree exactly | [QLF#221](https://github.com/rhovision-org/quantum-logical-framework/issues/221) |
| 2026-11-09 | Contracts bind a secp256k1 controller key to each DID until rholo can verify P-256 | DID keys are P-256 (WebCrypto, passkeys); rholo verifies only secp256k1 and ed25519 | [rholo#560](https://github.com/rhovision-org/rholo/issues/560) |
| 2026-11-06 | Treat the 2016 decks as vision, not technology choices | Gluu, Namecoin, eris and Synereo have been superseded | [CAPABILITIES.md](CAPABILITIES.md) |
