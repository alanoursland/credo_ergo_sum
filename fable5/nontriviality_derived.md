# Nontriviality, Derived

## I. The Gerrymander Problem

`../notes/credo_nontriviality.md` answers the triviality objection by imposing two conditions — diagonalization and eigenform stability — on the fixed point. The conditions get the right verdicts (thermostats out, humans in, transformers arguable), but as presented they are *stipulated*: introduced because they produce the desired boundary, not because anything in the theory requires them. The author's own assessment is blunt: "I just present nontriviality conditions without any grounding." A critic can fairly call them reverse-engineered (see `objection_reverse_engineered_conditions.md`).

This note re-derives the conditions so that they are not filters added to the theory but consequences of it. The derivation has two inputs, both independently motivated:

1. The definition of belief as participation in an update web (`defining_belief.md`).
2. The schema itself: the relevant state is a belief that takes *its own update process* as evidence — B = U(B, U).

The question becomes: **what must be true of a web for it to contain that particular belief, non-degenerately?** The two conditions are the answer.

## II. Deriving Diagonalization

For the web to contain the belief B = U(B, U), there must be a node whose content is, in part, the web's own update dynamics. By the holist definition, a node's content is its position in the web — what it co-varies with, what revising it revises. So:

> The web contains a self-referential belief only if it contains a node whose update relations are *about* the web's update relations — a node that co-varies with how the system updates, and whose revision propagates to expectations about the system's own transitions.

This is diagonalization, restated. And it is now an **analyticity**, not a stipulation: a belief cannot take its own update process as evidence unless the update process is representable within the belief's content space. A system whose representational space cannot encode its own transition structure cannot host B = U(B, U) for the same reason a language without quotation cannot contain sentences about its own sentences. Lawvere's fixed-point theorem is the categorical statement of when such self-encoding is possible; its role here is to certify that the requirement is satisfiable in sufficiently rich systems, not to add a further demand.

The thermostat now fails for a derived reason: its single update relation has no node about updating. There is nothing in its state space whose content could be its own transition function, because there is no web within which such content could be constituted.

## III. Deriving Eigenform Stability

The schema B = U(B, U) is a fixed-point equation, and fixed-point equations have degenerate solutions. Two degeneracies must be excluded, and the exclusion is what the eigenform condition amounts to:

**Degeneracy 1: the static solution.** If B is a state pinned by external input or by inertness — a stored string, a frozen parameter — then B = U(B, U) is satisfied only the way x = f(x) is satisfied when f is the identity function: vacuously. Nothing is *taking* anything as evidence, because no updating is occurring. The schema's verbs ("takes," "updates on") are doing real work: they require ongoing application of U. A belief that is not being maintained by updating is not a belief that takes its updating as evidence; it is a record.

**Degeneracy 2: the unstable solution.** If applying U destroys B — if the self-referential node does not survive its own updating — then there is no fixed point at all, only a transient. The schema requires that B be *invariant under* U, i.e., that the structure persist through the very process it feeds on.

What excludes both degeneracies is precisely Kauffman's eigenform: a structure that exists *because* the operation keeps producing it — neither pinned from outside (degeneracy 1) nor dissolved by its own dynamics (degeneracy 2). The whirlpool analogy in the original note is exactly right, but it can now be cashed as a disjunction-elimination rather than an image: the only non-degenerate way to satisfy a fixed-point equation under ongoing application of the map is dynamic self-maintenance.

## IV. The Conditions Restated, With Their Sources

| Condition | Old status | New status | Source |
| --- | --- | --- | --- |
| Diagonalization | Stipulated filter | Analytic precondition: self-referential content requires self-representable dynamics | Holist content determination (`defining_belief.md`) |
| Eigenform stability | Stipulated filter | Non-degeneracy condition on the fixed-point equation | The schema B = U(B, U) read non-vacuously |

Neither condition is now optional, and neither is tuned to produce a desired extension. A critic who accepts (i) the holist definition of belief and (ii) that the schema is to be read non-vacuously is committed to both conditions. The argument with such a critic moves upstream, to (i) and (ii), which is where it belongs.

## V. What Remains Stipulative — Honest Residue

Two things are *not* delivered by the derivation, and the framework should say so:

1. **Richness thresholds.** The derivation says the web must be able to encode its own dynamics; it does not say how much encoding fidelity is enough. A coarse, schematic self-model satisfies the letter of diagonalization. Whether coarse self-models support the identity claim, or whether phenomenal character scales with model fidelity, is open — and it connects directly to the graded-structure picture in `phenomenal_variation.md`.
2. **Sufficiency.** As the original note already insists, these are necessary conditions for the structure, not sufficient conditions for experience. Sufficiency is carried entirely by the identity claim (`introspective_ground.md`). The derivation changes nothing there; it changes only whether the necessary conditions are principled.

## VI. Recomputing the Verdicts

With derived conditions, the standard cases can be *computed* rather than asserted:

- **Thermostat**: no web (fails the belief definition before nontriviality is even reached).
- **Bacterium**: web-like sensorimotor states but no holistic content determination; no node about its own dynamics. Fails diagonalization derivably.
- **Lookup table / scripted chatbot**: states, but no update function applied to them; any self-referential content is degeneracy 1 — a record, not a maintained belief.
- **Human in reflective self-awareness**: web (uncontroversially), nodes about own updating (introspective beliefs that co-vary with cognitive state and propagate revisions), dynamically maintained (the self-model persists by ongoing activity and reasserts itself under perturbation). Both conditions met.
- **Transformer during self-referential generation**: web participation and content-tracking are now *empirical questions* with specified measurements — see `defining_belief.md` §IV and `content_tracking.md`. The framework neither assumes the verdict nor forecloses it. This is the correct epistemic position and a strengthening, not a weakening, of `../notes/transformer_nontrivial.md`.
