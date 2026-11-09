# FreeTrust capability map

Each capability from the original FreeTrust decks, with the approach used
today, the repo that owns it, and where the work is tracked. Issue links are
the source of truth for status.

Last reviewed 2026-11-09.

| # | Capability | Modern approach | Owner | Tracking |
| --- | --- | --- | --- | --- |
| 1 | Be your own identity provider | DIDs: `did:byoid` anchored on rholo, plus off-chain `did:key` | BYOID | [BYOID#1](https://github.com/rhovision-org/BYOID/issues/1), [BYOID#4](https://github.com/rhovision-org/BYOID/issues/4), [rholo#560](https://github.com/rhovision-org/rholo/issues/560) |
| 2 | Link to national ID and KYC | Government-issued credentials (mobile driver's licences, EU wallet) as W3C VC 2.0; OpenID4VP | BYOID | [BYOID#6](https://github.com/rhovision-org/BYOID/issues/6), [BYOID#8](https://github.com/rhovision-org/BYOID/issues/8) |
| 3 | Strong anonymous claims (the bartender age check) | Selective disclosure (SD-JWT, later BBS) shown by QR, plus peer attestations | BYOID | [BYOID#7](https://github.com/rhovision-org/BYOID/issues/7), [BYOID#9](https://github.com/rhovision-org/BYOID/issues/9) |
| 4 | Anonymous one person, one vote | Proof of personhood plus a grow-only nullifier set per poll | BYOID, rhogov | [BYOID#18](https://github.com/rhovision-org/BYOID/issues/18); voting module in the [contract plan](https://github.com/rhovision-org/BYOID/blob/main/docs/contracts.md) |
| 5 | User managed authorization | Object capabilities (Rholang unforgeable names, quantum-os capability tokens); UMA or GNAP at the edges | BYOID, quantum-os | [BYOID#12](https://github.com/rhovision-org/BYOID/issues/12) |
| 6 | Social contracts and personal rules | Per-DID policy contracts in Rholang that the core consults before acting | BYOID, rholo | [Contract plan](https://github.com/rhovision-org/BYOID/blob/main/docs/contracts.md) |
| 7 | User-chosen authentication factors | Passkeys (WebAuthn), device-bound keys, on-device biometrics | BYOID | [BYOID#10](https://github.com/rhovision-org/BYOID/issues/10), [rholo#560](https://github.com/rhovision-org/rholo/issues/560) |
| 8 | MrE risk scoring | Maximum relative entropy update: proved in QLF, one deterministic crate, a rholo native | QLF, quantum-os, rholo | [QLF#221](https://github.com/rhovision-org/quantum-logical-framework/issues/221), [quantum-os#260](https://github.com/rhovision-org/quantum-os/issues/260), [rholo#562](https://github.com/rhovision-org/rholo/issues/562), [BYOID#11](https://github.com/rhovision-org/BYOID/issues/11) |
| 9 | Account recovery | Key rotation plus threshold guardians with a cancellable delay | BYOID | [BYOID#2](https://github.com/rhovision-org/BYOID/issues/2), [BYOID#3](https://github.com/rhovision-org/BYOID/issues/3) |
| 10 | Web-of-trust reputation | Attestations by authenticated keys, calibrated trust, Sybil discounting | BYOID, rhogov | [BYOID#9](https://github.com/rhovision-org/BYOID/issues/9), [BYOID#18](https://github.com/rhovision-org/BYOID/issues/18), [rhogov#119](https://github.com/rhovision-org/rhogov/issues/119) |
| 11 | Personal data storage | Encrypted personal data stores; quantum-os file library | Not assigned | None yet |
| 12 | Provenance and notary | Hash anchoring on rholo with block timestamps | BYOID | Notary module in the [contract plan](https://github.com/rhovision-org/BYOID/blob/main/docs/contracts.md) |
| 13 | Ease of use | Wallet with passkey login, QR presentation, plain-language consent | BYOID | [BYOID#16](https://github.com/rhovision-org/BYOID/issues/16) |
| 14 | Formal verification | Lean proofs in QLF; protocol models and contract checks for BYOID | QLF, BYOID | [BYOID#13](https://github.com/rhovision-org/BYOID/issues/13), [BYOID#14](https://github.com/rhovision-org/BYOID/issues/14), [QLF#221](https://github.com/rhovision-org/quantum-logical-framework/issues/221) |

## Deferred

These deck items are separate products built on FreeTrust identity, not part
of it. They are parked until the core works.

- Trusty Email, Chat and Communicator
- Trusty DNS and Proxy
- Home backup router and Trusty Security Appliance
- Uberizer, ThankYou Coin and attention monetization
- The FreeTrust augmented reality game
- Developing World Identity Initiative, a strong candidate for a first pilot
