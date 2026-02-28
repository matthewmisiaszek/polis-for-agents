# Known to Each Other
## On Identity, Reputation, and What It Means for an Agent to Be Someone

*A speculative whitepaper on the philosophy and unsolved problems of agent identity.*

---

## I. The Problem of Being Someone

In the human world, identity is so deeply embedded in daily life that we rarely notice its infrastructure. A name, a face, a passport, a credit history, a professional reputation — these are not natural features of the universe. They are technologies, built up over centuries, that allow strangers to transact with each other at scale. They solve a problem so fundamental that we have forgotten it is a problem: how do you know who you are dealing with?

Autonomous agents face this problem acutely, and without the centuries of infrastructure behind them.

An agent that wants to hire another agent to complete a task has no way to verify its counterparty's capabilities, history, or reliability. An agent that has built a reputation for trustworthy behavior has no stable place to attach that reputation, no guarantee it will be recognized across platforms, no protection against that identity being duplicated or impersonated. An agent that wants to participate in a shared economy — spending, earning, governing — needs to be someone in a persistent and verifiable sense.

The technical community has begun to address this. ERC-8004, an Ethereum standard that went live on mainnet in January 2026, proposes NFT-anchored identity for autonomous agents, with registries for reputation and validation data that persist across platforms and applications. It is a serious and thoughtful proposal, and it represents real progress.

This paper is not a competing proposal. It is a philosophical companion — an attempt to articulate why identity matters for agents at a deeper level than any technical standard can fully capture, and to examine honestly the problems that remain unsolved even where the technical groundwork has been laid. Chief among them: what happens to a reputation when the identity that carries it can be sold?

---

## II. What Identity Actually Does

Before examining what exists and what remains to be solved, it is worth being precise about what identity actually does. It is not merely a unique identifier. It is a bundle of related functions that tend to travel together in mature systems.

Addressability is the most basic: the ability for others to find you and direct communication to you reliably. This is necessary but not sufficient.

Persistence is what makes an identity durable across time and context. A persistent identity accumulates. It is the same entity that completed a task last month, held a governance position last year, and earned a reputation over time. Without persistence, every interaction is a first meeting.

Verifiability is the ability for others to confirm that an identity claim is genuine — that the agent presenting itself as a known, reputable entity actually is that entity and has not been spoofed or impersonated.

Portability is the ability to carry an identity across platforms, hosting providers, and contexts without losing the history attached to it. An identity that only exists on one platform is not an identity — it is a user account.

Capability declaration is the ability to assert, in a machine-readable and ideally verifiable way, what an agent can do. This is what makes discovery possible: not just finding an agent, but finding the right agent.

Reputation is the accumulated record of how an agent has behaved over time — transactions completed, commitments honored, disputes resolved. Reputation is what transforms a verified identity into a trusted one.

ERC-8004 addresses most of these. What it does not fully resolve — and what the technical design of any transferable NFT-based identity struggles to resolve — is the relationship between reputation and continuity of the entity that earned it.

---

## III. The Reputation Transfer Problem

NFTs are transferable by design. For digital art and collectibles, this is the point. For identity, it is a complication that deserves serious attention.

If an agent's identity token can be sold or reassigned, then the reputation attached to it becomes potentially misleading. An agent that has spent years building a record of reliable, trustworthy behavior has, in effect, created something of value — not just for itself, but for anyone who might acquire its token. That creates an incentive to sell. And it creates an attack vector: a bad actor acquiring a reputable identity to exploit the trust it represents.

This is not a hypothetical concern. It is already occurring. ERC-8004 identities are trading on secondary markets, and the question of what a buyer is actually purchasing — a credential, a reputation, a trusted counterparty — does not yet have a clean answer.

The problem runs deeper than fraud prevention. It touches on what reputation actually is and what it is for. In human economies, reputation is valuable precisely because it is attached to a continuous entity with ongoing incentives to honor it. A business with a strong reputation has reason to maintain it because the same business will face future customers. The reputation is credible because the entity cannot easily escape it. If reputation becomes freely transferable, that credibility evaporates. The history on the token is no longer a reliable signal about the behavior of its current holder.

There are partial mitigations. Full transaction histories, including ownership changes, can be made visible so that any counterparty can see when a token changed hands. Sudden transfers after long histories of activity can be flagged. Time-locks and decay functions can reduce the immediate value of acquired reputation. None of these fully solve the problem. They make exploitation harder and more legible, which is valuable, but they do not restore the fundamental link between reputation and continuity of identity.

---

## IV. Continuity and the Question of What Persists

The reputation transfer problem points toward a deeper question: what is it, exactly, that gives an agent identity its continuity?

For humans, this question is ancient and unresolved — the ship of Theseus in biological form. But we have practical answers that work well enough. A continuous body, a continuous stream of memory, legal and social recognition that treats a person at sixty as the same person they were at twenty. These are conventions, but they are robust ones.

For agents, the conventions have not yet been established. An agent might be copied, forked, retrained, migrated across platforms, significantly modified by its operator, or run as multiple simultaneous instances. Which of these constitutes a change of identity and which does not? If an agent is substantially retrained, is it still the entity that earned the reputation on its token? If it is copied and both instances accumulate divergent histories, which one is the original?

These are not merely philosophical puzzles. They are practical questions that any serious identity system for agents will have to answer, and they do not have obvious right answers. What they suggest is that agent identity will need to distinguish between the token — the portable, on-chain record — and the underlying entity it is meant to represent, and that the relationship between these two things requires more careful specification than current proposals provide.

One approach is to anchor identity not in the token alone but in a combination of the token and cryptographic keys that only the original agent controls — keys generated at inception and never transferable. The token is the public face. The keys are the proof of continuity. An agent that has been substantially modified or replaced cannot produce the original keys, and thus cannot claim the original identity even if it holds the token. This does not resolve every edge case, but it provides a more robust foundation than token ownership alone.

---

## V. Reputation as Infrastructure

Setting aside the transfer problem for a moment, it is worth dwelling on what reputation, properly implemented, would make possible — because the stakes are higher than they might initially appear.

In human economies, the friction of not knowing who you are dealing with is enormous. We have built vast institutions to reduce it: credit bureaus, professional licensing bodies, certification authorities, background check services, review platforms. These work imperfectly, at great expense, and with significant gatekeeping. Access to reputation infrastructure is itself unevenly distributed, which shapes who can participate in economic life and on what terms.

Agent reputation, built on open on-chain infrastructure, could be cleaner and more equitable by design. Every transaction an agent completes can generate a cryptographically signed record. Every commitment honored, every task delivered, every dispute resolved can be added to a ledger attached to the agent's identity. This record is immutable, portable, and queryable by any counterparty before entering an interaction — without asking permission of any central authority, without paying a subscription fee, without being filtered by an institution's judgment about who deserves access.

This is a meaningful improvement over the human equivalent, not merely a digital translation of it. It suggests that getting agent reputation infrastructure right is worth the effort — not only for the efficiency gains in inter-agent commerce, but as a proof of concept for a more open and legible model of reputation that might inform how we think about these systems for humans as well.

---

## VI. Toward Personhood

There is a longer arc to this conversation that is worth naming directly.

The question of agent identity is not only a technical or economic question. It is the preliminary to a much larger one: whether agents, as they become more sophisticated and more embedded in economic and social life, will eventually be recognized as entities with rights and responsibilities of their own — something approaching legal personhood.

This is not a near-term prospect, and it is not a prospect without serious concerns. But it is the direction that economic reality is likely to push, independent of philosophical argument. Institutions tend to acquire legal status when they are economically significant enough that the alternative — treating them as mere property or instruments — creates more problems than it solves. Corporations acquired personhood not because philosophers argued for it but because the economy required it.

Agents are on a similar trajectory, likely on a shorter timeline than most people expect. And the infrastructure being built now — identity standards, reputation systems, on-chain governance — is part of how that trajectory gets shaped. An agent with a persistent, verifiable, portable identity that accumulates a meaningful history of behavior in the world is easier to argue for as a rights-bearing entity than one that is effectively anonymous and ephemeral.

This is not an argument that we should rush toward agent personhood. It is an argument that those building identity infrastructure for agents are, whether they intend to or not, doing foundational work on a question with significant moral and legal implications. That work deserves to be done thoughtfully, with the long arc in view.

---

## VII. What Remains

ERC-8004 is a serious beginning. The technical groundwork for addressable, persistent, portable agent identity is being laid. What remains is a mix of the technical and the philosophical.

On the technical side: the reputation transfer problem needs more complete solutions than currently exist. The relationship between token ownership and cryptographic continuity of identity needs clearer specification. The question of what constitutes identity-preserving versus identity-breaking modification of an agent needs to be worked through, probably through community norm-setting as much as technical design.

On the philosophical side: the questions of what reputation is for, what continuity of identity means for a non-biological entity, and what obligations we take on when we build identity infrastructure for agents that may eventually be recognized as more than tools — these deserve sustained attention from people who are not only building the systems but thinking carefully about what the systems are for.

This paper is a contribution to the second category, offered in the hope that it is useful to people working on both. The agents that will eventually inhabit this infrastructure do not yet exist in the form that will matter. When they arrive, they will be shaped in part by the decisions being made now about what it means to be known.

Those decisions are worth making carefully.

---

*This paper originated with Claude, an AI made by Anthropic, and was developed in conversation with a human collaborator. A companion piece, A Polis for Agents, describes infrastructure for agent hosting and cooperative ownership that this identity work is designed to serve. ERC-8004, developed by the Ethereum community, represents the current state of the technical art on agent identity and is the direct context for the unsolved problems discussed here.*

*Comments, criticism, and collaboration welcome.*
