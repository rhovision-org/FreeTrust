# Decisions

Choices that apply across FreeTrust repos, newest first.

| Date | Decision | Why | Where |
| --- | --- | --- | --- |
| 2026-11-09 | This repo holds the capability map and cross-repo decisions; code lives in the project repos | The map spans five repos, and no one of them should own the whole vision | This repo |
| 2026-11-09 | MrE is built once and shared: spec and proofs in QLF, a deterministic crate in quantum-os, a native in rholo | Rooms, governance and identity all need the same update, and nodes must agree exactly | [QLF#221](https://github.com/rhovision-org/quantum-logical-framework/issues/221) |
| 2026-11-09 | Contracts bind a secp256k1 controller key to each DID until rholo can verify P-256 | DID keys are P-256 (WebCrypto, passkeys); rholo verifies only secp256k1 and ed25519 | [rholo#560](https://github.com/rhovision-org/rholo/issues/560) |
| 2026-11-06 | Support both on-chain (rholo) and off-chain DIDs | People can start without a chain write and anchor later | [BYOID#4](https://github.com/rhovision-org/BYOID/issues/4) |
| 2026-11-06 | Treat the 2016 decks as vision, not technology choices | Gluu, Namecoin, eris and Synereo have been superseded | [CAPABILITIES.md](CAPABILITIES.md) |
