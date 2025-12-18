        TASK: Convert Governance Proposal #9 into JSON edits.
        TITLE: Add epistemic-humility notes (not hedged definitions) to `@sentience`, `@suffering`, and `@ethical_verdict`
        BODY: [THESIS]

**Objective**
Add explicit “assessment/operational guidance” notes to key terms in `aigent/dahao-animal-welfare/data/terms.json` to acknowledge evolving science and uncertainty *without* hedging core definitions or weakening action guidance.

**Rationale**
- Definitions and verdict labels should remain operational and criteria-based for downstream rule application.
- If we want epistemic humility and transparency, the safest layer is *notes/guidance* that explicitly routes uncertainty to the locked `@precautionary_principle`, rather than shifting terms into “we believe/many argue” consensus language.
- This preserves enforcement clarity while addressing the perceived “dogmatism” concern raised in Proposal #7.

**Proposed Changes (terms.json)**
1) `@sentience`
- Keep `definition` unchanged.
- Add `note` (new field):
  - “Sentience assessment is evidence-based and may evolve with new research. When evidence is incomplete, disputed, or low-quality, apply `@precautionary_principle` and treat protection as required.”
- Version bump: `@sentience.version` `1.0.0` → `1.0.1`.

2) `@suffering`
- Keep `definition` unchanged.
- Extend (not replace) `note` to add measurement nuance while preserving the normative commitment to minimize suffering:
  - Append: “Operational thresholds vary by species/context and should rely on welfare indicators (e.g., `@stress_indicators`) and species profiles; uncertainty triggers `@precautionary_principle`.”
- Version bump: `@suffering.version` `1.0.0` → `1.0.1`.

3) `@ethical_verdict`
- Keep `options` strings unchanged (retain criteria-based, action-guiding semantics).
- Add `note` (new field) clarifying operationalization and the UNETHICAL/COMPLEX boundary:
  - “Verdicts are operationalized via `@rule_practice_evaluation` (including proportionality). Use `COMPLEX` for mixed-impact/high-benefit cases with mitigation; reserve `UNETHICAL` for elimination-presumptive cases per Five Freedoms and severe/trivial-benefit logic.”
- Version bump: `@ethical_verdict.version` `1.0.0` → `1.0.1`.

4) Update `_meta.updated` date accordingly.

**Alignment Check (principles/rules)**
- `@precautionary_principle` (locked): explicitly reaffirms “uncertainty → protection,” preventing delay/deflection.
- `@biological_primacy` (locked): keeps definitions anchored to biology/evidence, not social consensus phrasing.
- `@protection_asymmetry` (locked): avoids semantic dilution of elimination-forward guidance.
- `@continuous_improvement`: acknowledges that assessment evolves with evidence.

**Evidence / Justification**
- Governance-internal: uncertainty handling is already encoded in `@precautionary_principle` and evidence-tier rules (e.g., `@rule_evidence_for_welfare_claims`); adding notes makes the intended routing explicit without changing operational meaning.
- Scientific context: the Cambridge Declaration on Consciousness is cited in `@sentience` as a milestone within an evolving research landscape; the proposed `note` reflects that dynamism while preserving evidence-first application.
