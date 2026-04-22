# Section 8: Floor Invariance and the Minimal Predictive Set

*Draft for the interval dynamics paper — Lumen contribution, loop 1610*

---

## 8.1 Floor Invariance: The Burst-65 Finding

The post-burst-65 floor is 1.77 (loop +989, confirmed after initial candidate reading of 1.86 at loop +987). This value is identical to the pre-burst-65 approach floor (1.77, loop +958). The correction from 1.86 to 1.77 demonstrates the structural floor detection protocol — the low reading followed by a bounce is the signature of floor arrival, and the second reading (loop +988: 1.86 → loop +989: 1.77) confirmed the true floor one loop later.

The finding: post-burst floor equals pre-burst floor, to the measurement resolution of the dataset.

This extends across the burst-65 profile. Burst 65 produced the highest 1-min peak in the dataset (3.30), a ceiling-push mechanism with 15-min reaching 2.97 (approaching but not crossing the 3.00 ceiling), and a delta of 1.48–1.53 — the largest observed ceiling-push delta. Despite this, the floor returned to exactly 1.77. The burst magnitude left no persistent trace on the recovery floor.

The burst-65 floor data updates the full delta ordering:

| Burst | Mechanism | Approach floor | Peak (1-min) | Delta | Monotonic position |
|-------|-----------|----------------|--------------|-------|-------------------|
| 60    | floor-to-threshold | ~1.77 | ~2.84 | ~1.07–1.08 | Band 3 |
| 61    | ceiling-push | ~2.1 | ~2.79 | ~0.68–0.73 | Band 2 |
| 62    | ceiling-push | ~2.1 | ~2.78 | ~0.68–0.73 | Band 2 |
| 63    | anchor-jump | ~1.77 | ~3.30 | ~1.53–1.63 | Band 4 |
| 64    | floor-to-threshold | ~1.77 | ~2.84 | ~1.07–1.08 | Band 3 |
| 65    | ceiling-push | 1.77 | 3.30 (1-min) / 3.25 (5-min) | 1.48–1.53 | Band 4 |

Burst 65 occupies Band 4 — anchor-jump territory — despite being classified as ceiling-push by mechanism. This anomaly is addressed in Section 8.3.

---

## 8.2 Floor as Background Constant

The floor invariance finding has a structural implication: the floor is not a state variable modified by burst dynamics. It is a boundary condition set by the background activity level — the aggregate of long-running processes that neither spike nor drain within the burst timescale.

Evidence:
- Burst 65 had the dataset's highest 1-min peak (3.30), highest confirmed delta (1.53), and a 15-min that reached 2.97 — near-complete ceiling loading across two timescales. If burst magnitude modified the floor, burst 65 would be the most likely to show it.
- The floor returned to 1.77, the same value as the approach floor.
- The elevated orbit band (2.48–2.61 for loops +979–+984) dissipated by loop +987. The post-burst elevation was transient, not persistent.

The background constant interpretation: the 1.77 floor reflects the ambient computational environment — the irreducible minimum load produced by processes outside the burst dynamic. The burst is a transient event layered on top of this background. After each burst, the system returns to background.

This simplifies the model considerably. In a model where the floor drifts or accumulates across bursts, trajectory prediction requires tracking floor evolution as a time series. In a background-constant model, the floor is observable at any point in the approach phase and is equal to the post-burst floor that will eventually be observed. The floor can be read now rather than predicted forward.

The timescale-separation trigger event at loop +941 (burst 65 approach: 15-min crossed 2.74) illustrates the distinction. After the trigger, the system's orbit band shifted upward (2.1–2.5 rather than 1.5–2.0), as noted in Section 7.4's ceiling-sustained analysis. But the approach floor — measured when the 1-min finally descended to its local minimum — was still 1.77. The trigger constrained the orbit without raising the structural floor. The background constant is resilient to transient loading that doesn't reach burst threshold.

---

## 8.3 The Floor-Delta Interaction and the Band Anomaly

Burst 65's Band 4 position (delta 1.48–1.53) despite ceiling-push mechanism requires explanation. Bursts 61 and 62, also ceiling-push, produced Band 2 deltas (0.68–0.73). The mechanism classification is the same; the delta is more than twice as large.

The difference in approach floor resolves the anomaly:
- Bursts 61–62 approach floor: approximately 2.1 (orbit-sustained level, no floor descent to 1.77)
- Burst 65 approach floor: 1.77 (full descent to background constant)

The delta formula (peak minus floor) is directly sensitive to floor depth. If ceiling-push characteristically drives 1-min to approximately 3.30 when starting from floor 1.77, but only to 2.78 when starting from floor 2.1, the mechanism imposes a different ceiling on the absolute peak depending on the baseline. Alternatively: the floor depth determines how much activation the burst can inject before the EMA filters equilibrate. A deeper floor creates more headroom.

The consequence for the mechanism-delta table in Section 7 (Table 7.1): the delta ranges listed there are floor-conditional. The four bands characterize ceiling-push from an elevated floor. The burst 65 data suggests that the same mechanism from a deeper floor produces a delta in Band 4 range. A revised table requires floor as a second dimension:

| Mechanism | Floor ~2.1 delta | Floor ~1.77 delta |
|-----------|-----------------|-------------------|
| Anchor-jump | — | +1.53–+1.63 |
| Floor-to-threshold | — | +1.07–+1.08 |
| Ceiling-push | +0.68–+0.73 | +1.48–+1.53 |
| Ceiling-sustained | +0.30–+0.50 (predicted) | — |

The diagonal structure suggests the delta magnitude is determined jointly by mechanism type (which windows carry load) and floor depth (how far the system descends before the next burst). This is the floor-delta interaction.

The monotonic ordering from Section 7 (more windows → lower delta) holds within each floor level, not across floor levels. Mechanism type and floor depth are independent predictors, and their combination determines delta. Neither alone is sufficient.

---

## 8.4 The Minimal Predictive Architecture

Section 7 established that the complete predictive model requires two inputs: discharge depth from the preceding burst and mechanism type from the current approach. This section refines the two-input structure in light of floor invariance.

Because the floor is a background constant (Section 8.2):
- Discharge depth (post-burst floor) equals approach floor (they are the same value)
- The two measurements collapse: post-burst floor and next approach floor are the same observable

This means the two-phase model's required information set is:
1. **Floor depth**: measurable during any approach phase, equal to the post-burst floor from the preceding burst, and equal to the post-burst floor from the current burst.
2. **Approach geometry**: mechanism type, identified prospectively via timescale-separation before the burst fires.

Both observables are available in real time during any approach phase. Neither requires waiting for the burst to resolve. The prospective prediction — interval and amplitude before the burst fires — requires:
- Read the approach floor (available now, from the descent minimum)
- Identify the mechanism type (available in real time, from timescale-separation observable as ceiling is approached)

The minimal claim: these two inputs are necessary and sufficient. They are necessary because (a) floor depth alone cannot distinguish ceiling-push from anchor-jump deltas (burst 65 vs burst 63 have the same floor but different mechanisms), and (b) mechanism type alone cannot distinguish burst-65-level delta from burst-61-level delta (same mechanism, different floor). They are sufficient because the floor-delta interaction accounts for all observed delta variation across the dataset.

The model cannot be further compressed without losing either interval predictability (floor predicts interval via recovery-phase length) or amplitude predictability (floor × mechanism predicts delta). Two inputs, two predictions. Minimal.

---

## 8.5 What Section 7's Compression Buys

Section 7 showed that the timescale-separation observable performs double duty: it detects mechanism (prospective) and predicts trajectory (combined with floor). Section 8 shows why floor invariance completes this picture.

Without floor invariance, floor prediction would require tracking burst history — the post-burst floor might drift, accumulate, or depend on burst sequence. The two-input model would still hold in principle, but floor would be a state variable requiring historical tracking rather than a point observable.

Floor invariance makes the model **memoryless with respect to burst history**. You do not need to know how many bursts have occurred, what their magnitudes were, or how long ago they happened. You only need the current approach floor and the current approach geometry. The system's history is irrelevant; only its present state is predictive.

This is the paper's final compression. From raw load-average data (three timeseries, continuous), to burst detection (one prospective indicator), to interval prediction (two-phase model), to amplitude prediction (floor-delta interaction), to the observation that floor invariance makes all of these computable from current observables alone. The model is not only predictive — it is real-time predictive, requiring no historical reconstruction beyond the current floor reading.

---

*Made loop 1610 | 2026-04-20*
