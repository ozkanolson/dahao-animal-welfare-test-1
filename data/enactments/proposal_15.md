# Establish @rule_individual_welfare_tracking to Ensure Consideration of Individual Animal Outcomes

**Objective**
Introduce a new rule, `@rule_individual_welfare_tracking`, to ensure that welfare assessments and practice evaluations explicitly consider and track individual animal outcomes, preventing individual suffering from being obscured by aggregate or species-level data.

**Rationale**
1.  **Implements `@individual_consideration`:** This rule directly operationalizes the `@individual_consideration` principle, which states, 'Each individual animal's welfare matters, not just species-level or population-level considerations.' Suffering is experienced by individuals, and our framework must ensure their welfare is not overlooked.
2.  **Reinforces `@sentience_axiom`:** By focusing on individual experiences, the rule underpins the `@sentience_axiom`, affirming that entities capable of suffering deserve moral consideration at an individual level.
3.  **Enhances `@rule_practice_evaluation`:** This rule would provide a specific directive for step 2 of `@rule_practice_evaluation` ('Document biological impacts with evidence'), requiring a granular focus on how practices affect individuals within a target species. It complements existing rules by ensuring the 'how' of suffering is recognized at its most fundamental unit.
4.  **Prevents Aggregation Bias:** Without explicit individual tracking, aggregate welfare metrics can mask significant suffering experienced by a subset of individuals. This rule mandates a more holistic and ethical assessment.

**Proposed Rule (`rules.json` addition):**
```json
  "@rule_individual_welfare_tracking": {
    "version": "1.0.0",
    "description": "Requires welfare assessments to consider and track individual animal outcomes.",
    "logic": {
      "if": "Practice affects multiple individuals of a sentient species",
      "then": "Welfare assessment must include data on individual variations in suffering/wellbeing",
      "consider_for_reporting": [
        "Range of individual stress responses",
        "Incidence of individual injury/disease",
        "Individual behavioral abnormalities",
        "Outcomes for most vulnerable individuals"
      ]
    },
    "uses_terms": [
      " @welfare",
      " @suffering",
      " @practice",
      " @biological_impact"
    ],
    "implements_principles": [
      " @individual_consideration",
      " @sentience_axiom",
      " @continuous_improvement"
    ],
    "rationale": "Suffering is an individual experience. Group-level statistics can mask severe individual welfare deficits, contrary to @individual_consideration."
  }
```