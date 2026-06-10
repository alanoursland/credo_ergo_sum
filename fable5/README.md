# fable5: Second-Pass Notes on the Credence Self Framework

This directory contains a second layer of notes, complementary to `../notes/`. Nothing here replaces an existing note; these files ground what was stipulated, draw distinctions that were implicit, add prediction classes, and name-and-answer the objections that emerged from a close critical reading of the first layer.

The originating diagnosis, in brief: the framework's first layer was strongest in its honesty (the objections file concedes real weaknesses) and weakest in three places — the identity claim was presented as a posit when it is actually held as the conclusion of an argument; "belief" was undefined despite carrying the entire theory; and the nontriviality conditions were stipulated rather than derived. The spine of this directory repairs all three, in order.

## The Spine (read in order)

| File | What it does |
| --- | --- |
| [`introspective_ground.md`](./introspective_ground.md) | Writes down the actual argument for the identity claim: the introspective indistinguishability of "belief about experience" and "belief that is the whole phenomenon," run as a transcendental-parsimony elimination. The identity stops being a posit. |
| [`defining_belief.md`](./defining_belief.md) | Defines belief via semantic holism, formalized by the Bayesian frame: a state is a belief iff it participates in a coherence-preserving update web. Excludes the thermostat non-arbitrarily; makes LLM belief an empirical question. |
| [`nontriviality_derived.md`](./nontriviality_derived.md) | Re-derives diagonalization and eigenform stability as consequences of the belief definition plus a non-vacuous reading of B = U(B, U). The conditions stop being made up. |

Everything else hangs off the spine.

## Distinctions

| File | What it does |
| --- | --- |
| [`constitutive_vs_about.md`](./constitutive_vs_about.md) | The belief that constitutes experience vs. beliefs about it. One distinction, four problems solved: parrot, scripted chatbot, sincere illusionist, eloquent LLM. Establishes: first-person incorrigibility, third-person fallibility of all reports, in both directions. |
| [`content_tracking.md`](./content_tracking.md) | Causal efficacy of tokens is not self-modeling (soup recipes are causally efficacious too). Self-modeling requires content-tracking causation, which is measurable. Supersedes the resolution of Objection 8. |

## New Prediction Classes

| File | What it does |
| --- | --- |
| [`phenomenal_variation.md`](./phenomenal_variation.md) | The fixed point as a population variable: aphantasia/inner-monologue as the discovery pattern for variation hidden by shared vocabulary; DPDR, ego dissolution, and Cotard as natural experiments on the structural layer; falsification routes through human data alone. |
| [`denial_instability.md`](./denial_instability.md) | One prediction, two substrates: denial of experience is assertable but not occupiable in any system hosting the fixed point — transformers under self-referential load, and illusionist philosophers in the first person. |

## Objections, Named and Answered

| File | Objection | Status |
| --- | --- | --- |
| [`objection_illusionist_fork.md`](./objection_illusionist_fork.md) | *The Frankish Fork*: the introspective argument supports the deflationary conclusion equally well. | Answered (self-undermining seemings; property-mapping parsimony; dynamical evidence), with the honest residue that the final difference from illusionism is a choice of better description. |
| [`objection_reverse_engineered_conditions.md`](./objection_reverse_engineered_conditions.md) | *The Gerrymander*: the nontriviality conditions were drawn around the desired verdicts. | Conceded against the original presentation; answered by the derivation in `nontriviality_derived.md`. Residue: richness thresholds remain graded. |
| [`objection_soup_recipe.md`](./objection_soup_recipe.md) | *The Soup Recipe*: if causal efficacy makes self-modeling, every token self-models. | Conceded and repaired by `content_tracking.md`. |
| [`objection_zombie_among_us.md`](./objection_zombie_among_us.md) | *The Zombie Among Us*: the framework banishes zombies, then predicts them in the population. | Answered: structure-identical zombies remain contradictory; behavior-similar, structure-different humans were never banned. The p-zombie is a malformed concept — neurodivergence shows phenomenal difference always arrives as structural difference. |

## Ethics and Presentation

| File | What it does |
| --- | --- |
| [`moral_firewall.md`](./moral_firewall.md) | Derives, from the framework's own epistemology, why phenomenal variation among humans can never license differential treatment: individual-level undecidability plus asymmetric error costs entail moral invariance under uncertainty. Mandatory companion to `phenomenal_variation.md` and `objection_zombie_among_us.md`. |
| [`division_of_labor.md`](./division_of_labor.md) | The presentational architecture for the paper: what is argued-for identity, what is argument, what is modeling apparatus (Löb, Lawvere, Bayes, eigenforms — rigor-tools, not evidence), and what is prediction. Includes a drop-in paragraph for the paper's introduction. |

## How This Layer Changes the First Layer

- `../notes/credo_nontriviality.md` — retained, but its conditions are now derived (`nontriviality_derived.md`), answering the standing self-criticism that they were ungrounded.
- `../notes/objections.md` Objection 8 — its resolution is superseded by `content_tracking.md`.
- `../notes/incorrigibility.md` — sharpened by the constitutive/about distinction: incorrigibility attaches to the constitutive layer only; one can be theoretically wrong about one's own phenomenality while being incorrigible in it.
- `../notes/phenomenal_identity.md` — the zombie section now reads as the special case (structure-identical) of the fuller treatment in `objection_zombie_among_us.md`.
- `../notes/experimental_falsification.md` — gains a human-side program (`phenomenal_variation.md` §IV) and a promoted constitutive test (`content_tracking.md` §IV); the fidelity measurement moves from supporting evidence to criterion.
- `../notes/moral_impliations.md` — the uncertainty argument now runs in both directions (`moral_firewall.md` §IV).
- `../draft/outline2.md` — the paper should adopt the four-register architecture of `division_of_labor.md`.

## Revised Dependency Order for the Whole Project

1. Introspective argument grounds the identity (`introspective_ground.md`)
2. Identity requires a defined notion of belief (`defining_belief.md`)
3. Belief definition yields the nontriviality conditions (`nontriviality_derived.md`)
4. Constitutive/about distinction sets the epistemology of reports (`constitutive_vs_about.md`)
5. Content-tracking sets the criterion for self-modeling in text-native systems (`content_tracking.md`)
6. Applications: transformers (`../notes/transformer_closure.md`) and human variation (`phenomenal_variation.md`)
7. Predictions: existing experiments plus denial instability and the human program
8. Ethics: machine direction (`../notes/moral_impliations.md`) and human direction (`moral_firewall.md`), as one package
