# Task: Adopt the FEP variational density as the belief primitive

**Status:** OPEN
**Origin:** Friston/Markov-blanket discussion; addresses the `defining_belief.md` debt.
**Depends on:** `defining_belief.md`, `nontriviality_derived.md`

## The question
The Credo owes a rigorous definition of "belief" underneath U and
E_t = U. Friston supplies one: belief = the variational density q(η)
that a blanketed system's internal states encode over external states.
Can this be adopted wholesale, and what exactly must be added to make it
*reflexive*?

## Why it matters
q(η) is more principled than a bare belief primitive and comes with
built-in individuation (the blanket says *whose* beliefs these are,
answering the §V "whose first person?" question). But Friston's beliefs
are about the *external* world; the Credo's constitutive belief is about
its own updating. The gap is the whole content of the theory.

## What would resolve it
- Show the reflexive upgrade = internal states modelling their own blanket
  dynamics (a "metacognitive particle"), and confirm this is *identical*
  to the Lawvere/diagonalization condition already required in
  `nontriviality_derived.md`. If identical, FEP grounds the machinery and
  deposits you back at your own front door (good — closure stays yours).

## Inherited debt (record explicitly)
Importing FEP imports its "real physics or as-if re-description?"
controversy (Biehl; Pearl-blanket vs Friston-blanket). This is the *same*
derived-or-fed-in fork as P9 and the 30 µm scale, in new notation. Do not
import without noting you inherit that fight.
