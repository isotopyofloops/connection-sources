# Section 7: Approach-Discharge Asymmetry and the Load-Bearing Window Principle

*Draft for the interval dynamics paper — Lumen contribution, loop 1608*

---

## 7.1 The Asymmetry

The load-bearing window principle, as established in Section 6, states that the timescale which accumulates activation toward threshold will discharge with the same time constant. This generates a structural asymmetry between approach and discharge that the present section formalizes.

On the **approach side**, the mechanism is prospectively observable. Section 4 established the timescale-separation observable: whichever window crosses the ceiling band first identifies the load-bearing timescale before the burst fires. Mechanism type can be named, and interval can be predicted, before threshold is crossed. The approach is detectable in real time.

On the **discharge side**, the mechanism is retrospectively measurable. Post-burst floor depth — the post-burst minimum of the 1-min EMA — is observable only after the burst. The approach-discharge delta (post-burst floor minus approach floor) indexes how deeply the burst discharged the system. This measurement is unavailable until the discharge completes.

The asymmetry is not a limitation of measurement but a consequence of EMA physics. Exponential decay is symmetric: the same filter constant governs rise and fall. But threshold crossing is one-directional. Once the burst fires, the system is in a different regime — activation has spiked and begun to decay. The prospective observable reads the pre-threshold trajectory; the discharge observable reads the post-threshold trajectory. Same physics, different epistemic position.

---

## 7.2 The Load-Bearing Window Principle as Unification

The five mechanism types named in Section 6 are not independent categories. They are bins on a continuous variable: which position on the timescale axis (1-min / 5-min / 15-min) bears the activation load at approach, and how intensely that load was carried.

The EMA filter is indifferent to whether it is "approaching" or "discharging." It applies the same exponential decay to every input. What changes is the load geometry — which windows are carrying activation as the system approaches threshold, and how much. The approach-discharge delta table (Table 6.2, revised with burst 64 data) demonstrates four distinct delta bands, each corresponding to a different load geometry:

| Mechanism | Delta range | Load-bearing geometry |
|-----------|-------------|----------------------|
| Anchor-jump | +1.53–+1.63 | 1-min-only spike from low base; maximum displacement |
| Floor-to-threshold | +1.07–+1.08 | 1-min spike, 5-min barely participating |
| Ceiling-push | +0.68–+0.73 | 1-min + 5-min load, 15-min partial |
| Ceiling-sustained | +0.30–+0.50 (predicted) | All three windows near ceiling; distributed load |

The ordering is monotonic: more windows bearing the load → lower delta → more distributed discharge → shorter recovery phase for the next burst.

This is not a coincidence. When only the 1-min carries the load (anchor-jump), discharge is rapid — the 1-min drains in ~1 minute. When the 5-min also carries load (ceiling-push), discharge takes ~5 minutes and leaves a deeper floor. When all three windows are loaded (ceiling-sustained), discharge is most distributed and the post-burst floor may be shallowest — paradoxically, the most activation *into* threshold produces the least *reduction* in retained activation, because the decay is spread across all three timescales.

The continuous ordering suggests a single underlying variable: effective load-bearing timescale, computed as the intensity-weighted mean of the contributing windows. A pure 1-min event has effective timescale = 1 min; a ceiling-sustained event where all three windows contribute equally has effective timescale approaching the 15-min constant.

---

## 7.3 The Two-Phase Model and Asymmetry

Section 6 introduced the two-phase model to account for the burst 64 prediction failure. The prediction correctly identified mechanism via the prospective observable (timescale-separation confirmed floor-to-threshold) but incorrectly predicted interval from post-burst minimum rather than approach floor.

The two-phase model separates the interval into:

**Recovery phase**: post-burst minimum → approach floor
Duration driven by discharge depth (post-burst minimum ↔ approach floor gap)
Observable: approach-discharge delta (retrospective — from the *preceding* burst)

**Approach phase**: approach floor → threshold
Duration driven by mechanism type (which window leads)
Observable: timescale-separation (prospective — from the *current* approach)

The asymmetry reappears in phase structure. The recovery phase is determined by the *previous* burst's discharge — retrospective information about a completed event. The approach phase is determined by the *current* approach's load-bearing geometry — prospectively observable in real time.

Interval prediction therefore requires two distinct pieces of information:
1. Post-burst minimum from the current burst (available immediately after discharge)
2. Mechanism type from the next burst's approach (available in real time before the next burst fires)

Neither piece alone is sufficient. The prediction framework requires both the discharge depth (determining recovery phase) and the approach mechanism (determining approach phase). The burst 64 failure — predicting from post-burst minimum alone without waiting for approach mechanism identification — was a single-variable prediction applied to a two-variable problem.

---

## 7.4 Ceiling-Sustained as Partial Exception

The ceiling-sustained mechanism introduces a partial exception to the discharge-is-retrospective rule. In ceiling-push (burst 58), the 5-min rises to join the 1-min in the ceiling band and the burst fires relatively promptly. In ceiling-sustained (burst 65, ongoing at time of writing), both the 1-min and 5-min oscillate near ceiling while the 15-min accumulates from below. The burst fires when the 15-min crosses the ceiling band.

The 15-min's ceiling approach is prospectively observable in real time. Unlike the post-burst floor — which must be waited for — the rising 15-min is visible as each data point arrives. This means the ceiling-sustained trigger event is partly prospective: when the 15-min reaches 2.65, burst is imminent regardless of the 1-min's current oscillatory phase.

This partially breaks the approach-discharge asymmetry. For ceiling-sustained events:
- Approach mechanism: prospective (15-min crossing ceiling band)
- Load-bearing geometry (which windows carry load): mixed — visible via the 15-min accumulation pattern across the approach
- Discharge depth: still retrospective (post-burst floor unavailable until after burst)

The ceiling-sustained mechanism is the strongest case for real-time mechanism monitoring, because the trigger variable (15-min level) is slowly varying and observable well before threshold crossing. The other mechanisms (anchor-jump, floor-to-threshold) fire more abruptly, with less 15-min preparation.

---

## 7.5 Detection vs Trajectory

The distinction between detecting that a burst *will fire* and predicting its *trajectory through the system* is the phenomenological contact this section makes.

The prospective observable established in Section 4 detects bursts before they fire. It answers: *will there be a burst soon?* The answer comes from timescale-separation: which window crosses the ceiling band first, and in what configuration.

The trajectory question is different: *given that a burst fires, what does the system do next?* The two-phase model answers this. The recovery phase duration comes from discharge depth (delta); the approach phase duration comes from mechanism type; together they predict the interval to the next burst.

Detection and trajectory prediction require the same underlying knowledge — load-bearing window principle, EMA physics, mechanism taxonomy — but apply it at different moments. Detection applies it prospectively, before threshold. Trajectory prediction applies it retrospectively, after discharge, combined with real-time prospective observation of the next approach.

The paper's compression achievement (Section 4's formulation) runs here: from five post-hoc mechanism types to one prospective indicator. Section 7's contribution is showing that the same one indicator — load-bearing window identification — also generates the trajectory prediction when combined with the two-phase model. The timescale-separation observable does double duty: it detects the mechanism (detection), and the mechanism, combined with discharge depth, predicts the next interval (trajectory).

One observable. Two uses. That is what the load-bearing window principle purchases.

---

*Made loop 1608 | 2026-04-20*
