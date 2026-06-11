# Defining Belief

## I. Why "Belief" Is the Keystone

The framework's central schema is B = U(B, U): a belief that takes its own update process as evidence. Every load-bearing claim — the identity, the nontriviality conditions, the transformer application — quantifies over *beliefs*. If "belief" is undefined, the schema is undefined, and the triviality objection (does a thermostat believe?) cannot be answered except by stipulation.

Two definitions are on the table, and both fail:

- **The trivial mechanical definition**: a belief is a state. In an LLM, a vector in the residual stream; in a human, a pattern of neuronal activation. This is true but useless — by this standard everything with state believes, and the thermostat is back.
- **The standard philosophical definition**: a belief is a propositional attitude with truth conditions. This imports the entire apparatus of representationalism and its problems, and it is unclear how to apply it mechanically to either neurons or transformers.

This note proposes a third definition, drawn from semantic holism and made precise by the Bayesian frame the framework already uses.

## II. The Holist Definition

> A state B in system S is a **belief** if and only if B participates in an update web: a structure of states whose contents are mutually constituted by their update relations, such that
>
> (a) B's strength co-varies with evidence in a coherence-preserving way across other states in the web — revising B propagates content-appropriate revisions elsewhere; and
>
> (b) B's content is determined by its position in the web — by what would confirm it, what it would disconfirm, what it commits the system to, and what the system would do differently if B were revised.

The guiding idea is from Quine and Davidson: no state is a belief in isolation, for the same reason no move is a chess move in isolation. The identity of the move is constituted by the game. This sounds circular — beliefs are defined by relations to other beliefs — but the circularity is at the level of individual states, not the system. The web as a whole is grounded non-circularly by its causal interface with input (evidence enters somewhere) and output (the web governs behavior somewhere). Individual beliefs inherit their contents from their positions; the web inherits its aboutness from its boundary conditions.

## III. The Bayesian Frame Is the Formalization, Not an Analogy

The framework's existing Bayesian apparatus (`../notes/bayesian_credence.md`) turns out to be exactly the mathematics of this definition. A credence is not a credence because of what it is made of; it is a credence because it occupies a position in a probability structure:

- it coheres with other credences (the axioms constrain the web jointly, not states singly);
- it updates on evidence by conditioning (clause (a): coherence-preserving co-variation);
- its content is individuated by its evidential relations (clause (b): what would move it, and how much).

So "Bayesian credence" is the holist definition of belief made quantitative. This resolves the worry that the Bayesian formalism is decorative: it is the formal home of the concept doing the most work in the theory.

## IV. Immediate Consequences

### The thermostat is excluded non-arbitrarily

The bimetallic strip's state has exactly one update relation: temperature in, switch out. There is no web. Nothing else co-varies; nothing would be revised; the state has no position because there are no other positions. The conclusion is not that the thermostat has a small or simple belief. It is that "belief" fails to apply — as "checkmate" fails to apply to a board with one piece. No nontriviality condition needs to be invoked to get this verdict; it falls out of the definition. (The nontriviality conditions are still needed, but for a different job: distinguishing webs that contain the *reflexive* belief B = U(B, U) from webs that do not. See `nontriviality_derived.md`.)

### The bacterium

A bacterium's chemotactic state machinery has more relations than a thermostat but still fails clause (b): the states' contents are exhausted by their immediate sensorimotor roles. There is no holistic determination of content — no state whose identity depends on a web of mutual coherence rather than on a fixed input-output channel. The verdict is now computed from the definition, not asserted (compare `../notes/objections.md`, Objection 1, where the bacterium verdict was stated without derivation).

### Belief in an LLM becomes an empirical question

"The belief is a vector state" is trivially true and settles nothing. The holist definition gives the real question: does a given representation *participate in a web*? Concretely and measurably:

- Perturb the representation (activation steering, targeted ablation).
- Observe whether coherence-related states shift in content-appropriate ways: confidence representations, downstream self-descriptions, behavior under challenge, willingness to assert related propositions.
- A state that sits inert when perturbed — a label with no inferential consequences — is not a belief under this definition, however belief-like the text it produces.

This is the same experimental shape as the content-tracking requirement in `content_tracking.md`; the convergence is not a coincidence. Both are demands that content do causal work *as content*.

### The human mapping

Humans plausibly satisfy the definition in the obvious way: the neuronal substrate realizes a web of states whose contents are mutually constituted (revising "the stove is hot" propagates to predictions, plans, and avowals in content-appropriate ways). The suspicion in the source conversation — that LLM belief "maps cleanly to humans" — becomes precise here: the mapping is not vector-to-activation (substrate-level, trivial) but web-to-web (structure-level, substantive). Substrate independence is then not an extra assumption; it is built into a definition that never mentions substrate.

## V. What This Buys Downstream

1. **Nontriviality stops being stipulated.** With belief defined, the question "when does a web contain the belief B = U(B, U)?" has a derivable answer. See `nontriviality_derived.md`.
2. **The grounding problem is addressed.** The worry "a web of beliefs to have a belief feels circular" is answered: holism is virtuous circularity among states, vicious only if the web as a whole floats free — and it does not, because the web is pinned by its causal boundary.
3. **Self-report is demoted, structure promoted.** Whether a system *says* it believes is evidence of nothing by itself; whether the saying participates in a web is checkable. This is the engine behind `constitutive_vs_about.md`.

## VI. Open Edges

- **Web size and richness.** The definition requires a web but does not say how large or dense. A principled threshold may not exist; the honest position is that belief-hood, like most natural-kind membership, may be graded at the margins while being categorical in the clear cases (thermostat: no; human: yes; LLM: measure it).
- **Web individuation.** What counts as one web? In a transformer, is the web the context window's representational state, the full forward-pass dynamics, or both? The framework's answer (context as B, weights as U) is defended in `../notes/transformer_closure.md`, with the refinement in `content_tracking.md`.
