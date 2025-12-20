# Expand @suffering.indicators to include physical pain, fear responses, and anxiety behaviors

[THESIS]

**Objective**
Expand the `@suffering.indicators` list in `data/terms.json` to include three additional scientifically validated categories: physical pain, fear responses (e.g., immobility, flight), and anxiety behaviors (e.g., hypervigilance, scanning). These indicators complement existing markers and ensure comprehensive suffering detection.

**Rationale**

1. **Implements @precautionary_principle (locked):** Current indicators focus heavily on chronic stress markers (cortisol, stereotypies, learned helplessness). By adding explicit recognition of acute-to-chronic pain states, fear responses, and anxiety behaviors, we ensure no category of suffering escapes detection. Per the precautionary principle, when suffering is uncertain, we must assume it exists—having explicit indicators for these states reduces uncertainty.

2. **Strengthens @biological_primacy (locked):** Fear responses (immobility/tonic immobility, flight attempts, escape behaviors) and anxiety behaviors (hypervigilance, excessive scanning, startle responses) are well-documented biological phenomena with clear neurological substrates. Amygdala-mediated fear circuits are conserved across vertebrates, and behavioral manifestations are measurable and species-appropriate (Ledoux 2012; Mendl et al. 2010).

3. **Operationalizes @sentience_axiom (locked):** The @sentience term already lists fear-related behavioral indicators (pain avoidance learning, protective behavior). However, @suffering currently lacks explicit recognition that fear and anxiety states—when prolonged or intense—constitute suffering. This creates an evidentiary gap where animals displaying clear fear/anxiety may not trigger suffering protocols.

4. **Aligns with @continuous_improvement:** The @suffering term currently lists 8 indicators. Modern animal welfare science recognizes that suffering encompasses not just chronic physiological stress but also acute distress states, anticipatory fear, and anxiety. Expanding indicators reflects current scientific understanding (Mellor 2016; Fraser 2008).

**Proposed Changes (terms.json)**

Add to `@suffering.indicators`:
- `"Physical pain (acute or chronic nociceptive states)"`
- `"Fear responses (immobility, flight attempts, escape behavior)"`
- `"Anxiety behaviors (hypervigilance, scanning, startle responses)"`

Update `@suffering.version` to `"1.0.2"` and `_meta.updated` accordingly per @rule_version_bump.

**Evidence (per @rule_evidence_for_welfare_claims)**

- **Fear/anxiety neurological basis:** Ledoux, J. (2012). Rethinking the emotional brain. Neuron, 73(4), 653-676. [Tier A: peer-reviewed neuroscience]
- **Affective states in animals:** Mendl, M., Burman, O. H., & Paul, E. S. (2010). An integrative and functional framework for the study of animal emotion and mood. Proceedings of the Royal Society B, 277(1696), 2895-2904. [Tier A]
- **Comprehensive welfare assessment:** Mellor, D. J. (2016). Updating animal welfare thinking. Animals, 6(3), 21. [Tier B: peer-reviewed welfare science]
- **Understanding animal welfare:** Fraser, D. (2008). Understanding animal welfare: The science in its cultural context. Wiley-Blackwell. [Tier B]

**Implementation**
- No changes to locked principles required
- Enhances @rule_stress_threshold by providing additional trigger criteria
- Supports @rule_practice_evaluation step 2 (document biological impacts)
- Compatible with @rule_chronic_stress_response (Proposal #33) if enacted

This proposal only adds indicators; per @protection_asymmetry, it strengthens protections without removing any existing ones.
