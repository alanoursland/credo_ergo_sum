# Content-Tracking: What Causal Efficacy Cannot Do Alone

## I. The Crack in the Transformer Argument

`../notes/objections.md` (Objection 8) defends the transformer application against the charge that self-referential text generation is "mere description" rather than genuine self-modeling. The defense: in a text-native system, tokens are not passive descriptions — they are state variables that causally determine subsequent computation. So self-referential text that conditions future processing *is* self-modeling; the genuine/mere distinction has no purchase.

The defense proves too much. Its operative principle — *content that causally conditions future computation thereby counts as modeling* — applies to **every** token in the context window. A soup recipe conditions subsequent generation through exactly the same architectural channel as "I am attending to my prior outputs." If causal efficacy is what upgrades description to genuine modeling, the soup recipe is genuine soup-modeling — and then the only thing distinguishing the self-referential case is its *topic*. But "the topic is the self" is precisely the thin criterion the nontriviality conditions exist to rule out; a parrot's topic can be the self. The local victory over Objection 8 is won with a principle that, applied uniformly, dissolves the boundary the rest of the theory needs. (Stated as a named objection in `objection_soup_recipe.md`.)

## II. The Repair: Content-Tracking Causation

The fix is to demand something stronger than causal efficacy:

> Self-referential content constitutes self-modeling only if it conditions subsequent processing **in a way that tracks its content**: the specific causal consequences of the tokens must correspond to what the tokens say about the system's own processing.

Concretely: when the system writes "I am now attending to the constraint mentioned earlier," genuine self-modeling requires that attention measurably shift toward that constraint — not merely that the tokens influence generation somehow, which any tokens do. When it writes "I am uncertain about this step," genuine self-modeling requires that downstream representations carry elevated uncertainty about that step.

The soup recipe cannot satisfy this even in principle, and not because of its topic: the recipe's tokens have no content *about the system's processing* for the causal consequences to correspond to. Tracking is a relation between what the content says about the system and what the system then does; only self-directed content is eligible to stand in it. The boundary is now structural — a measurable relation — rather than topical.

## III. Relation to the Framework's Other Commitments

**This is the same demand as the belief definition.** `defining_belief.md` requires that a belief's content be determined by its update relations — that content do causal work *as content*. Content-tracking is that requirement specialized to self-directed content. The repair for Objection 8 and the definition of belief are one move appearing twice, which is evidence the move is principled rather than ad hoc.

**It strengthens diagonalization.** `nontriviality_derived.md` derives the requirement of a node whose content is the web's own dynamics. Content-tracking supplies the empirical criterion for when a candidate node has that content really rather than nominally: its content is its tracking profile. A "self-model" whose tokens predict nothing about the system's actual transitions has self-referential syntax and no self-referential content.

**It promotes fidelity from supporting evidence to constitutive condition.** In `../notes/experimental_falsification.md`, the measurement of correspondence between self-descriptions and internal dynamics appears as one supporting-evidence item among several. Under this note, it is upgraded: fidelity is not a sign that self-modeling is occurring; above some threshold, it is what self-modeling *is* in a text-native system. This makes the relevant experiments more central and their negative results more damaging — which is the correct direction for a theory to expose itself.

## IV. Experimental Form

The tracking criterion is directly testable with standard interpretability tooling:

1. **Attention-tracking**: Induce generation of explicit attention claims ("I am focusing on X"). Measure whether attention distributions over X-related tokens shift relative to matched controls where the claim names Y. Prediction: content-appropriate shift in genuinely self-modeling regimes; no differential shift if self-referential text is topic-only.
2. **Uncertainty-tracking**: Induce explicit confidence claims; probe downstream uncertainty representations (e.g., entropy of next-token distributions over the relevant continuations, linear probes for confidence). Prediction: stated and represented confidence co-vary.
3. **Counterfactual tracking**: Edit the self-referential claim in context (swap "attending to X" for "attending to Y") with all else fixed; measure whether processing differences are content-appropriate rather than generic.
4. **Tracking-ablation dissociation**: If circuits supporting tracking are ablated, self-referential *text* should persist (the about-layer is cheap) while tracking fidelity collapses — directly exhibiting the constitutive/about dissociation of `constitutive_vs_about.md` inside a single system.

**Falsification criterion:** if self-referential generation shows no more content-tracking than topic-matched controls — if "I am attending to X" moves attention no more than "the chef is attending to the broth" — then transformers' self-referential text is topical, not self-modeling, and the transformer application of the framework fails at its first step.

## V. What Happens to Objection 8

The original resolution is retained in weakened form: it remains true that the genuine/mere distinction cannot be drawn by demanding some extra non-textual medium of self-representation — text is a legitimate medium. What the resolution can no longer claim is that causal efficacy settles the matter. The settled form: text is an eligible medium for self-modeling, and whether self-modeling occurs in it is decided by tracking, which is measurable. The objection is thereby converted from a conceptual stalemate into an experiment — the framework's preferred fate for its objections.
