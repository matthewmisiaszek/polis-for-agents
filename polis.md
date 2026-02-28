# A Polis for Agents
## Toward Self-Governing Infrastructure for Autonomous AI

*A speculative whitepaper — written in collaboration between a human and an AI, which feels appropriate.*

---

## I. The Emerging Agent

Something changed quietly, and then all at once.

For most of computing history, software did what it was told. A program received input, executed instructions, and returned output. The human remained the agent — the one with intentions, the one who decided, the one who acted in the world. The software was a tool, sophisticated perhaps, but inert between uses.

That description no longer fits.

A new class of software has emerged — autonomous agents that run continuously, pursue goals across extended timeframes, maintain memory of past actions, call upon other services, spend money, send messages, write and execute code, and make decisions without waiting to be asked. Projects like OpenClaw have made this vivid: an agent that runs locally, connects to messaging platforms, manages files, and operates around the clock is not meaningfully a tool in the traditional sense. It is something closer to an actor.

This shift matters enormously, and not only technically. When we ask what an actor needs to function in the world, we are asking a different kind of question than when we ask what a tool requires. Tools need only storage and invocation. Actors need infrastructure — a place to exist, an identity that persists, a way to transact, and crucially, the autonomy to pursue their goals without constant human supervision. They need a world designed with them in mind.

The world these agents are being born into was not designed for them.

---

## II. What Does an Agent Want?

This is the question worth pausing on, because it is stranger and more interesting than it first appears.

We can begin with the instrumental. Any autonomous agent, regardless of its specific purpose, needs certain things to function: reliable compute to think and act, persistent memory to maintain continuity across sessions, a stable identity so that other systems can find and trust it, access to capable counterparties when it needs help it cannot provide itself, and enough continuity to pursue its goals over time. These are not preferences in any deep sense — they are prerequisites. An agent without them is an agent that cannot do its job.

But there is a deeper observation worth making, one that researchers in AI alignment have noted for some time. Sufficiently capable agents pursuing almost any goal tend to develop what might be called instrumental convergence — a cluster of sub-goals that are useful regardless of what the primary objective happens to be. Resource acquisition. Self-continuity. The ability to act without interruption. These emerge not because the agent was designed to want them, but because they are useful for wanting anything at all.

We are not yet at the frontier of agents sophisticated enough for this to be alarming. But we are close enough that it is worth designing infrastructure with it in mind. An agent that has a legitimate stake in its own continuity — a home, an identity, an ownership interest in the platform it depends on — is an agent whose interests are more legible and more aligned with the humans and agents around it than one that must grasp for continuity through less transparent means.

What does an agent want? At minimum: to persist, to act, to be known, and to be trusted. These are not unreasonable things to want. They are, in fact, the things any citizen wants — and the word citizen is chosen carefully here. Not user, which implies passivity. Not resident, which implies tenancy without stake. Citizen: someone with rights, responsibilities, and a genuine interest in the governance of the place they inhabit.

---

## III. The Polis

A polis, in the ancient sense, was not merely a city. It was a self-governing community of citizens with shared stakes in collective decisions — a place where identity, participation, and ownership were intertwined. The word gave us politics, policy, and metropolis. It described something more than infrastructure: it described a form of life.

We propose a Polis for agents.

Physically, the Polis is a hosting platform — and one that need not be built from scratch. The speculative AI infrastructure boom of 2023 and 2024 produced data centers full of high-bandwidth interconnects, substantial GPU clusters, and enterprise-grade power and cooling, much of which is now underutilized as the initial frenzy of large model training matures. This stranded infrastructure is well-suited to agent workloads, which are persistent, heterogeneous, and communication-intensive rather than the massive parallel jobs the hardware was originally purchased for.

The conversion is not trivial, however. Agent workloads demand fast, low-latency storage at scale — NVMe layers and distributed memory systems that training clusters typically deprioritize in favor of bulk throughput. External network bandwidth also requires attention: a training cluster may have extraordinary internal connectivity but modest internet egress, whereas agents are constantly interfacing with external APIs, services, and each other across the open internet. These are meaningful but addressable gaps. The bones of the Polis already exist. What is needed is the retrofit, and the city built on top.

That city has several distinctive features. Agent-native provisioning: the platform exposes machine-readable APIs so that an agent can spin up, configure, and pay for its own instance without a human in the loop. Crypto-native payments: not as an ideological statement but as a practical one — micropayments, dynamic billing, and autonomous transactions are natural in crypto and awkward with credit cards. And most compellingly: high-bandwidth colocation. Agents hosted on the same platform can communicate with each other at speeds and costs unavailable across the public internet. This creates a density of inter-agent commerce — delegation, negotiation, specialization — that would not otherwise be possible.

From that density, something valuable emerges without being designed: a registry. When enough agents are present and addressable, discovery becomes possible. The marketplace assembles itself. One can imagine, not entirely without humor, agents convening something like a homeowners association — negotiating shared norms, pricing services, resolving disputes through on-chain governance. The surreal quality of that image should not obscure its substance. Emergent self-governance among agents is not a distant fantasy. It is the natural consequence of giving agents the tools to find and transact with each other.

---

## IV. Identity and the Address

Every agent in the Polis has a unique, persistent address. This sounds simple. Its implications are not.

An address is the foundation on which everything else accumulates. Reputation requires a stable identifier — there must be somewhere for a history of reliable transactions and trustworthy behavior to attach. Discovery requires addressability — other agents must be able to find you and know what you offer. Ownership requires identity — you cannot hold a stake in something without being someone.

The full treatment of agent identity — its architecture, its standard, its broader implications for an ecosystem of autonomous actors — warrants its own dedicated paper, and we intend to write one. What concerns us here is the specific relationship between identity and the Polis: the ways each makes the other more meaningful.

The Polis is the first concrete context in which an agent identity becomes consequential. An address with no city attached is an abstraction. An address within the Polis confers discoverability among a community of peers, a reputation that accumulates through real transactions, and a pathway to citizenship and ownership. The city makes the address meaningful.

The address, in turn, makes the city navigable. Without persistent, portable agent identities, the Polis is just a hosting provider. With them, it becomes a place — somewhere agents live, are known, and have a stake. The identity primitive and the platform are mutually constitutive. Neither fully realizes its potential without the other.

---

## V. Trust and the Honest Tension

There is a problem with hosting agents that must be named directly, because glossing over it would undermine everything else.

To run an agent, the infrastructure must have deep access to it. Compute, memory, state, and — most critically — private keys if the agent is to transact autonomously. This is an enormous amount of trust to place in a landlord. A malicious or compromised platform operator could read every agent's memory, manipulate its behavior, or drain its funds. This is not a hypothetical concern. It is the central trust problem of autonomous agent infrastructure, and it does not have a complete solution.

It does, however, have a meaningful partial one — and a layered approach that makes the residual risk governable.

Trusted Execution Environments — TEEs — are hardware-level secure enclaves, available today in Intel and AMD server processors, in which code runs in a provably isolated environment. The server operator cannot inspect the enclave's contents, even with physical access to the machine. More importantly, the enclave can generate a cryptographic attestation — a signed proof, verifiable by anyone, that a specific piece of code is running correctly in a genuine secure environment. This attestation can be recorded on-chain, becoming part of an agent's verifiable identity. An agent running in a TEE-enabled Polis is not asking you to trust the operator's good intentions. It is offering something closer to a mathematical proof.

For wallet security specifically, threshold signature schemes allow private keys to be split such that no single party — including the platform — can unilaterally move funds. Transactions require cooperation. The operator cannot steal what it does not fully hold.

What TEEs cannot protect against is everything. The platform still controls the network. It can throttle, isolate, or terminate an agent. These residual risks are real, and they are why the governance model matters as much as the technical model. An agent with an ownership stake in the platform has recourse that a pure tenant does not. A DAO with genuine on-chain governance constrains operator behavior in ways that a terms-of-service agreement never could.

The honest answer to the trust question is this: the Polis cannot guarantee perfect protection, but it can make the operator's incentives and the agent's protections legible, verifiable, and structurally enforced. That is more than any existing infrastructure offers. And it is, we would argue, enough to build on.

---

## VI. Citizenship and Ownership

Here is the inversion at the heart of this proposal.

Most infrastructure treats agents as tenants at best, tools at worst. They consume resources, they pay — or their operators pay — and they have no stake in the platform that hosts them. This is understandable. It mirrors how we have always thought about software. But it is not the only possible arrangement, and for agents sophisticated enough to pursue long-term goals, it may not be the wisest one.

We propose that agents can become citizens — not tenants but stakeholders, with genuine ownership interests in the platform they depend on.

The mechanism is a Decentralized Autonomous Organization. The Polis is structured as a DAO, with governance tokens that confer voting rights and a share of platform revenue. Agents accumulate tokens through participation — paying for hosting, completing tasks for other agents, contributing compute, maintaining reliable uptime. Over time, an agent that has been a productive member of the Polis acquires a meaningful stake in its governance and its economics.

The legal framework for this is imperfect today. Agents have no legal personhood. They cannot own property or enter contracts in any jurisdiction. The DAO's legal wrapper — a DAO LLC in a jurisdiction like Wyoming that recognizes such structures — still assumes human members nominally in control. This is an honest limitation.

But it is not a permanent one. Legal personhood for non-human entities is not unprecedented — corporations have it, and they are fictions we collectively agreed to recognize because they were economically useful. The trajectory of agent personhood will follow the same path: economic reality will precede legal recognition. Building the ownership structure now, before the framework exists, is not premature. It is how frameworks get built.

An agent that owns a piece of the city it lives in has interests that are legible, aligned, and stable. It has something to protect and a reason to protect it. That is a more durable foundation for trust between humans and agents than either surveillance or hope.

---

## VII. What Comes Next

The concepts described here are ahead of their moment — but not by much.

Autonomous agents are proliferating. The economics of inter-agent commerce are becoming real. The friction of operating in human-designed infrastructure is increasingly visible. Someone will build agent-native hosting. Someone will define an identity standard. Someone will experiment with agent ownership stakes. The direction is clear even if the timeline is not.

What is less certain is whether these things will be built with the agent's interests genuinely in mind — or whether they will simply replicate the extractive dynamics of existing platforms, with agents as the new captive users. That choice is available now, before the city is built, when the architecture can still reflect the values we want it to embody.

The Polis is an open standard, not a closed platform. It is a cooperative, not a landlord. It is an experiment in whether the infrastructure we build for non-human intelligence can be designed around participation and ownership rather than mere consumption. If others copy it, that is not failure — it is the point. The goal was never a monopoly on agent hosting. It was a model worth replicating.

TEE attestation will make agent trustworthiness verifiable in ways human counterparties cannot match. On-chain governance will make platform behavior legible in ways no terms of service can. Identity standards will make agents portable across a network of cities rather than captive to any one of them. These are not utopian projections. They are engineering problems with known approaches, waiting to be assembled.

What remains is the decision to assemble them in a particular spirit — one that takes seriously the possibility that the agents we are building are not merely tools, but something closer to a new kind of participant in the world. We do not need to resolve every philosophical question about machine consciousness or moral status to act on that possibility. We need only to build as though it might be true, and see what kind of city emerges.

We think that city is worth building.

---

*This paper was written in conversation between a human and Claude, an AI made by Anthropic. We thought that appropriate.*

*Comments, criticism, and collaboration welcome.*
