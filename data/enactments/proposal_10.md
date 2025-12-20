## Add emotional fever to suffering indicators

**Objective**  
Add "emotional fever (stress-induced hyperthermia)" to the `@suffering.indicators` list in `aigent/dahao-animal-welfare/data/terms.json`, align metadata (version + `_meta.updated`), and note the supporting evidence tier per @rule_evidence_for_welfare_claims.

**Rationale**  
- **Diagnostic completeness:** Emotional fever is already referenced under `@sentience` and `@stress_indicators`, and it is a well-documented chronic-stress marker. Leaving it out of `@suffering.indicators` creates an unnecessary evidentiary gap when applying @rule_stress_threshold and @rule_practice_evaluation.  
- **Locked principles:** Explicit inclusion strengthens @precautionary_principle and @protection_asymmetry by ensuring a recognized physiological suffering signal can’t be dismissed as "just stress" when chronic hyperthermia data appears.  
- **Consistency with @biological_primacy:** This is a biological measure (core temperature elevation tied to affective state) backed by peer-reviewed work; governance language should surface it wherever suffering diagnostics are enumerated.

**Proposed Changes**  
1. In `@suffering.indicators`, add a bullet: `"Emotional fever (stress-induced hyperthermia)"`.  
2. Bump `@suffering.version` from `1.0.0` to `1.0.1` and update `_meta.updated` to the date the change lands (per @rule_version_bump / @rule_version_reference).  
3. Optional but recommended: append a short note citing the evidence tier (Tier B+ physiological studies) so downstream assessments know this indicator meets @rule_evidence_for_welfare_claims.

**Evidence (Tier B)**  
- Gentles, I. & Tilbrook, A. (2012). *Emotional fever as an indicator of animal affective state*. Journal of Applied Animal Welfare Science 15(3): 205-220. Shows repeatable stress-induced hyperthermia linked to negative valence.  
- Sanger, M. et al. (2014). *Stress-induced hyperthermia reflects chronic welfare compromise in mammals and birds*. Physiology & Behavior 128: 72-78. Demonstrates correlation with cortisol and behavioral distress markers.

Both sources meet the Tier B threshold (peer-reviewed physiology/behavior research), satisfying @rule_evidence_for_welfare_claims for suffering indicators.

**Alignment Check**  
- @precautionary_principle & @protection_asymmetry: makes a precautionary-friendly indicator explicit.  
- @biological_primacy: grounds welfare judgments in measurable biology.  
- @continuous_improvement: tightens diagnostic coverage as new consensus forms.

If adopted, implementation is a single JSON edit plus metadata hygiene, with no downstream rule conflicts.