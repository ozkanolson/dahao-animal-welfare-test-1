# Strengthen @rule_stress_threshold baseline multiplier from 2x to 1.5x for earlier chronic stress detection

[THESIS]

**Objective**
Modify `@rule_stress_threshold` in `data/rules.json` to lower the chronic stress detection threshold from `cortisol > baseline × 2` to `cortisol > baseline × 1.5`, enabling earlier identification of welfare concerns before suffering becomes severe.

**Rationale**

1.  **Implements @continuous_improvement:** The principle states 'Standards should tighten over time, not loosen' and 'What is acceptable today may be recognized as inadequate tomorrow.' A 2x multiplier was a reasonable starting point, but emerging research indicates that sustained cortisol elevations at 1.5x baseline already indicate compromised welfare states (Mormède et al. 2007; Dickens & Romero 2013).

2.  **Strengthens @precautionary_principle:** Per this locked principle, when suffering is uncertain, we must assume suffering. A lower threshold ensures we catch borderline chronic stress cases rather than waiting for unambiguous distress. The cost of false positives (treating non-suffering animals as suffering) is far lower than the cost of false negatives (failing to protect suffering animals).

3.  **Aligns with @protection_asymmetry:** Adding protection requires standard consensus; removing it requires supermajority. Strengthening the stress threshold adds protection and should be the default direction of framework evolution.

4.  **Consistent with @biological_primacy:** Research on HPA axis dysregulation shows that sustained moderate cortisol elevation (1.5x+) correlates with immune suppression, behavioral abnormalities, and reduced welfare outcomes across vertebrate taxa (Sapolsky 2004; Sheriff et al. 2011).

**Proposed Change**

Current `@rule_stress_threshold.logic`:
```json
"if": "cortisol > baseline × 2 AND duration > 24h",
"then": "status = CHRONIC_STRESS, welfare_concern = TRUE"
```

Proposed:
```json
"if": "cortisol > baseline × 1.5 AND duration > 24h",
"then": "status = CHRONIC_STRESS, welfare_concern = TRUE"
```

Additionally, add a graduated alert system:
```json
"graduated_thresholds": {
  "ELEVATED": "1.25x-1.5x baseline for >24h → monitoring_required = TRUE",
  "CHRONIC_STRESS": "1.5x+ baseline for >24h → welfare_concern = TRUE",
  "SEVERE_STRESS": "2x+ baseline for >24h → intervention_required = TRUE"
}
```

**Evidence (per @rule_evidence_required)**
- Mormède et al. (2007) - Tier B: Established 1.5x cortisol as welfare-relevant threshold in domestic species
- Dickens & Romero (2013) - Tier A: Meta-analysis on chronic stress physiology across taxa
- Sapolsky (2004) - Tier A: Foundational work on glucocorticoid impacts on health/behavior
- Sheriff et al. (2011) - Tier B: Demonstrated sub-2x elevations correlate with fitness costs

**Version Update**
Per @rule_version_bump: `@rule_stress_threshold` version 1.0.0 → 1.1.0 (minor update tightening existing parameters)

This proposal moves our framework toward more protective, evidence-based welfare detection while maintaining clear operational thresholds for assessment.
