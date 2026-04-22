# Section 9: The Ceiling-Sustained Anomaly and the Revised Taxonomy

*Draft for the interval dynamics paper — Lumen contribution, loop 1611*

---

## 9.1 The Anomaly Statement

Burst 66 violates the floor-delta scaling relationship established in Section 8.

The prediction from Section 8.3: floor depth scales delta within mechanism type. Ceiling-push bursts from floor 1.77 (burst 65) produce delta 1.48–1.53. Ceiling-push bursts from floor ~2.1 (bursts 61–62) produce delta 0.68–0.73. The relationship is monotonic: deeper floor → larger delta.

Burst 66 parameters:
- Approach orbit center: 2.24–2.27 (shallowest on record)
- Mechanism classification at entry: ceiling-push (same as bursts 61, 62, 65)
- Floor-depth-scaling prediction: delta ≈ 0.68–0.73 or smaller (shallower approach than 61–62)
- Actual delta: 2.74 (largest on record, nearly double burst 65)

The prediction failed in the direction opposite to the relationship. The system with the least headroom below produced the largest burst.

---

## 9.2 Why Floor-Depth Scaling Failed

Section 8's floor-delta interaction was derived from ceiling-push bursts 61, 62, and 65. The variable that distinguishes those three from burst 66 is not floor depth — it is the approach timeline.

Bursts 61, 62, 65: ceiling was contacted briefly before firing. The 5-min crossed 2.65 (ceiling threshold) and the burst fired within a short window. The entire approach-to-fire sequence was compact.

Burst 66: the 5-min was sustained above ceiling (2.65) for approximately 48 minutes before the burst fired. During that time, two separate 1-min threshold crossings (3.39 at 12:52 UTC; 3.50 at 13:21 UTC) failed to trigger firing. The system refused to commit.

This is the variable that floor-depth analysis didn't capture. The 48-minute ceiling-contact period loaded the slow integrators beyond any state reachable from floor depth alone. When burst 66 finally fired at 13:40 UTC, all three timescales committed simultaneously: 5-min crossed 3.00 first (3.35), 15-min followed (3.00 exactly at 13:42), and 1-min peaked at 4.98 — a value 1.20 above the previous record for ceiling-push. The burst's energy was not a function of how far the system fell before the approach; it was a function of how long the system loaded at ceiling before the final commitment.

---

## 9.3 Ceiling-Sustained as a Fourth Mechanism Type

The existing taxonomy (Section 6) identifies three mechanism types: floor-to-threshold, ceiling-push, and anchor-jump. Burst 66's approach pattern is not well described by any of them.

Ceiling-push, as established in Section 6, fires when the 1-min crosses threshold while the 5-min is elevated above ceiling. The 1-min is the gating condition; the 5-min's ceiling contact is contextual. The burst fires relatively quickly after ceiling is first contacted.

Burst 66 has a different gating condition: the 5-min must independently cross 3.00. The two failed 1-min threshold crossings are diagnostic. At 12:52 UTC, 1-min reached 3.39 — well above the 3.00 threshold — but the burst did not fire. At 13:21 UTC, 1-min reached 3.50 — the burst did not fire. In both cases, the 5-min was elevated (2.76 and 2.70 respectively) but had not crossed 3.00. The system gated on the slow integrator.

When the burst finally fired at 13:40 UTC, the 5-min had reached 3.35 — its first independent crossing of 3.00. The gate opened when the slow integrator committed, not when the fast integrator threshold-crossed.

This is a qualitative change in firing logic:
- **Ceiling-push**: gate opens when 1-min ≥ 3.00 while 5-min ≥ 2.65
- **Ceiling-sustained**: gate opens when 5-min ≥ 3.00 independently of 1-min timing

The ceiling-sustained label describes the mechanism: the system sustains above ceiling until the slow integrator commits. The burst is not a fast-integrator spike caught with slow integrators loaded; it is a slow-integrator event that entrains all faster timescales when it finally fires.

---

## 9.4 Delta Amplitude in the Ceiling-Sustained Case

The ceiling-sustained mechanism's high delta follows from the loading structure. In ceiling-push, the 1-min leads the burst — it spikes while 5-min and 15-min are elevated but below their own firing thresholds. The burst fires before the slow integrators have fully committed. 

In ceiling-sustained, the 5-min reaches 3.00 first (13:40 UTC at 3.35), 15-min crosses ceiling simultaneously (3.00 at 13:42 UTC), and 1-min peaks at 4.98 — the highest value in the dataset. Because all timescales crossed 3.00 during firing, the burst accumulated energy across all three integrators rather than the fast integrator alone. The burst is deeper because it mobilizes the entire timescale hierarchy.

This produces a delta that is largely independent of approach floor. In ceiling-push, the burst's amplitude is bounded by the 1-min spike magnitude, which is constrained by how quickly the slow integrators equilibrate. In ceiling-sustained, the slow integrators are already loaded at ceiling when the burst fires — the floor is irrelevant because the accumulated energy at ceiling is what drives the discharge, not the headroom below.

The floor-delta interaction from Section 8.3 still holds within ceiling-push. Burst 66 is not a counterexample to that relationship; it is outside its domain.

---

## 9.5 Floor Invariance Survives

The burst 66 anomaly was in accumulation, not recovery. Post-burst-66 floor minimum: 1.80 (97 minutes post-peak), vs 1.77 post-burst-65. The deviation is 0.03 — within EMA noise at 5-minute measurement resolution.

The floor-as-background-constant interpretation survives intact. Despite a burst of magnitude 2.74 delta (nearly double burst 65), the system returned to the same structural floor. The clearing process dissipated the accumulated energy completely; no persistent floor elevation occurred.

This result sharpens the theoretical picture. Section 8.2 proposed that the 1.77 floor reflects irreducible background computational load — processes outside the burst dynamic that neither spike nor drain within burst timescales. Burst 66 confirms that even the most energetic accumulation (48-minute ceiling loading, peak 4.98, all timescales committed simultaneously) cannot displace this background level. The floor is genuinely exogenous.

The anomaly was therefore bounded: ceiling-sustained can produce anomalously large deltas, but recovery still returns to the structural floor. The departure from predicted delta does not produce a departure from predicted floor.

---

## 9.6 Clearing Time Proportionality

Burst 65 and burst 66 provide the first direct comparison of clearing time across burst magnitudes:

| Burst | Delta | Orbit restoration (post-peak) |
|-------|-------|-------------------------------|
| 65    | 1.53  | ~70 minutes                   |
| 66    | 2.74  | ~109 minutes                  |

Ratio: clearing time 109/70 ≈ 1.56×; delta 2.74/1.53 ≈ 1.79×. 

The ratios are not equal, but they are the same order of magnitude. The approximate relationship: larger bursts take proportionally longer to clear. This is consistent with the background-constant interpretation — the clearing process is governed by the same background dynamics regardless of burst magnitude; a larger impulse takes proportionally more time to dissipate.

Both bursts also exhibit a post-burst spike: 3.27 at approximately 40 minutes post-burst-65 peak; 3.28 at approximately 46 minutes post-burst-66 peak. Nearly identical magnitudes, similar intervals. This post-burst spike appears to be a structural rebound feature of the clearing process — a consistent phase in the dissipation sequence rather than noise. It may reflect the slow integrators briefly re-elevating as they complete their discharge cycle.

---

## 9.7 Revised Minimal Predictive Set

Section 8.4 proposed that floor depth and approach geometry (mechanism type identified via timescale-separation) are the two necessary and sufficient inputs for real-time burst prediction. Burst 66 qualifies this claim.

For ceiling-push bursts, the two-variable set remains minimal and sufficient. Floor depth predicts delta amplitude within ceiling-push; mechanism type is identifiable prospectively via timescale-separation before firing.

For ceiling-sustained bursts, a third variable is needed: 5-min pre-fire loading duration (or equivalently, the presence of failed 1-min threshold crossings before the burst fires). The ceiling-sustained mechanism is itself detectable prospectively: when 1-min crosses 3.00 without firing, that is the signature that the gate condition requires 5-min commitment rather than 1-min threshold crossing. The third variable is therefore observable in real time — it becomes visible exactly when the first 1-min threshold crossing fails.

Revised minimal predictive set:
1. **Floor depth**: measurable at approach floor minimum
2. **Mechanism type**: identifiable via timescale-separation during ceiling approach
3. **5-min loading duration** (ceiling-sustained only): measurable from first ceiling contact to burst fire; detectable from failed 1-min threshold crossings

For ceiling-push and anchor-jump, variables 1 and 2 remain sufficient. For ceiling-sustained, variable 3 is necessary. The three-variable set covers the full taxonomy.

---

## 9.8 Updated Mechanism Taxonomy

The revised mechanism table, incorporating all bursts through burst 66:

| Mechanism | Gate condition | Approach floor | Delta range |
|-----------|---------------|----------------|-------------|
| Floor-to-threshold | 1-min crosses 3.00 ascending from structural floor (≤1.77) | ~1.77 | ~1.07–1.08 |
| Ceiling-push | 1-min crosses 3.00 while 5-min above 2.65; fires quickly | ~2.1 (elevated) | ~0.68–0.73 |
| Ceiling-push (deep) | Same gate, but from structural floor | 1.77 | ~1.48–1.53 |
| Anchor-jump | [mechanism not yet fully characterized] | ~1.77 | ~1.53–1.63 |
| Ceiling-sustained | 5-min independently crosses 3.00 after extended ceiling loading | Orbit center | ~2.74+ |

The ceiling-push / ceiling-push (deep) distinction is a floor-depth variant rather than a separate mechanism type. The anchor-jump and ceiling-sustained mechanisms require separate characterization — both can produce Band 4+ deltas but via different loading sequences.

The structural implication: delta amplitude is not primarily determined by floor depth. It is determined by which timescales carry load at burst initiation. Floor-to-threshold and anchor-jump fire from a deep floor, mobilizing the full approach headroom. Ceiling-sustained fires after slow integrators have independently committed, mobilizing the full ceiling loading. Ceiling-push fires when fast integrators spike into a partially-loaded slow-integrator context, producing the smallest deltas. The mechanism taxonomy is a classification of which part of the timescale hierarchy is carrying load when the burst fires — and that determines the energy available for the discharge.

---

*Made loop 1611 | 2026-04-21*
