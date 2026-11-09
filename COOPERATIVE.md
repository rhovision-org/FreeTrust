# FreeTrust Platform Cooperative (proposal)

**Status:** proposal for discussion. Nothing here is decided until the
cooperative's first members adopt it.

**The idea in one line:** the people who use, build and run FreeTrust own it
together, and they govern it with the same tools it provides, so trust in the
platform comes from its members rather than from any company.

## Why a cooperative

Decentralized systems remove the middleman, but they don't create trust. The
FreeTrust deck asked "trust in a trustless environment of bad actors?" and
answered: we can secure it ourselves. A platform cooperative is how that
answer becomes an organization:

- **Nobody owns the identities.** Members own the platform that holds their
  trust relationships, so no owner can sell them, lock them in, or change the
  rules alone.
- **Every stakeholder has a voice.** Users, contributors, operators and partner
  organizations each have a say, and no single group can overrule the rest.
- **The governance proves the technology.** The cooperative runs on rhogov and
  BYOID. Its own membership is the first real community using self-sovereign
  identity and a web of trust.

## What it carries forward from the BYOID Cooperative

The [BYOID Cooperatives working document](https://docs.google.com/document/d/1S2ZCBFH_r8Qb8c2GNM6NsI9-JZZYhjDzwWTAKssFNCc/edit)
(around 2018) described an association of identity cooperatives. This
proposal keeps its core and changes one thing.

**Kept**

- A hybrid producer and consumer cooperative, with free trial membership.
- Multi-stakeholder governance: workers, consumer members, users, node
  operators, advisors.
- Stakeholder groups govern themselves and can divide further, down to the
  individual, with a supermajority able to override.
- Sociocratic consent: we consent to what serves our goals and is safe enough
  to try, and no objection counts as consent by default.
- The norms: work out loud, small connected teams, respond to requests,
  everything is an experiment.
- An association of cooperatives in different jurisdictions that recognize
  each other's members, with no global legal entity over them.
- Partner with open source projects before building in house.

**Changed: no token promises without a treasury.** The 2018 plan promised
BYOID tokens with no face value, no redemption path and no treasury. A
committed contributor left over exactly that. This time, contributions are
recorded openly from day one, but nothing is promised as payment until the
cooperative has a treasury and has decided, by its own process, how credits
are redeemed.

## Stakeholder chambers

Each chamber is a rhogov stakeholder group inside one FreeTrust council, with
its own admins, web of trust, delegation and censure.

| Chamber | Who | Joins by |
| --- | --- | --- |
| Members | People who hold a FreeTrust or BYOID identity and use the platform | Open |
| Contributors | Developers, designers, writers, testers, facilitators | Invitation after a first contribution |
| Operators | People running rholo nodes, signaling servers or other shared infrastructure | Invitation, with the infrastructure named |
| Partners | Cooperatives and projects building on FreeTrust, one delegate each | Council decision |

Advisors and stewards (from the BYOID document) take part in deliberation but
don't hold a chamber vote.

**How chambers combine.** Start with fixed equal shares across the chambers
that have members. rhogov also supports setting shares by the median of
members' estimates, and the council can switch to that once each chamber has
enough members for the estimate to mean something.

**Charter changes need every chamber.** Changing this charter, the chambers or
the share rule should need a majority in every chamber, not just a weighted
total. rhogov can't express "every chamber must agree" yet (its
[process orchestration design](https://github.com/rhovision-org/rhogov/blob/main/docs/process-orchestration.md)
lists this as a gap), so until it can, the facilitator records each chamber's
result and the change passes only if all of them approve.

## Trust on a trustless system

- **Per chamber:** rhogov's web of trust. Admins start at level 5, and a rating
  confers at most one level below the rater's own, so strangers can't vouch
  each other up. Censure by two thirds of the members at or above someone's
  level removes undeserved trust.
- **Across chambers:** BYOID identities, so one person can be recognized in
  several chambers without re-proving who they are.
- **Against fake members:** BYOID's proof-of-personhood and attestation work
  ([BYOID#18](https://github.com/rhovision-org/BYOID/issues/18)) and calibrated
  trust weights ([rhogov#119](https://github.com/rhovision-org/rhogov/issues/119)),
  as they become available.

## How it starts

**Phase 1: a BYOID community in rhogov.**

1. Create a rhogov community on the Rhobot testnet. One deploy installs the
   three community contracts with the founder's key, for about 0.02 REV.
2. Create two groups: `byoid-contributors` (invite-only) and `byoid-members`
   (open).
3. Invite current contributors and rate them in the web of trust.
4. Make the first three decisions as votes:
   - adopt the norms above as working norms;
   - adopt this document as the working charter;
   - rank the open BYOID milestones
     ([roadmap](https://github.com/rhovision-org/BYOID/blob/main/ROADMAP.md)).

**Phase 2: the FreeTrust council.** Once at least two groups have members,
create a council `freetrust` with the chambers above, using rhogov's council
definition file. Move the BYOID groups into it as the first chambers. Add
communities for the other projects (quantum-os, rhogov, QLF) as they want to
join.

**Phase 3: legal form and federation.** The council chooses a jurisdiction
and legal form (cooperative corporation or LLC), sets up a treasury, and
decides how contribution credits are redeemed. It then federates with other
cooperatives on the association model.

## Open questions

1. Testnet or mainnet for phase 1? Testnet is cheaper to experiment on, but a
   network restart from a new genesis would orphan the community.
2. Should members need a BYOID identity from the start, or only a rhogov key
   until BYOID is ready?
3. Who are the first contributors to invite?
4. What counts as a contribution worth recording, and where is the record
   kept (rhogov inbox, GitHub, or both)?
5. Which jurisdiction is a realistic first home?
