# The Jamming Avoidance Response

*A survey essay on Eigenmannia, Apteronotus, and the problem of coordination without protocol.*

---

The weakly electric fish of South America solve a problem so elegant it took neurobiologists decades to fully trace: how do you share a sensory medium with a neighbor, given that your neighbor's presence degrades the medium?

Eigenmannia virescens generates a continuous sinusoidal electric organ discharge (EOD) at roughly 300–600 Hz — a precise, unbroken electric hum emanating from an organ along its tail. It uses this field to navigate, to detect nearby objects (which distort field lines differently depending on conductivity and capacitance), and to communicate. The field is indispensable. It is also the problem.

When two Eigenmannia with similar frequencies meet, their fields superimpose. The result is a beat frequency: a slow oscillation whose amplitude rises and falls at the rate of the difference between the two frequencies. A fish experiencing this beat cannot easily read its own field. Objects near its body cause distortions that pulse on and off with the beat rather than remaining stable. Electrolocation degrades. This is jamming — not electronic warfare in a metaphorical sense but literal interference between periodic signals in a shared medium.

The Jamming Avoidance Response, or JAR, is how the fish escapes it. Each fish shifts its own EOD frequency away from the neighbor's — upward if the neighbor is slightly lower, downward if the neighbor is slightly higher — until the difference between them exceeds ~5 Hz, at which point the beat is fast enough to average out and both fish can read their own fields cleanly again.

The description makes it sound simple. The implementation is not.

---

To shift in the correct direction, each fish must determine the sign of the frequency difference: is the neighbor above me or below? This is harder than it seems. The fish cannot measure its own frequency and the neighbor's independently. What it experiences is the compound signal — the superposition of both fields at its skin. Disentangling which component is whose requires comparing phase across space.

Here is the trick: when two sinusoids near the same frequency superimpose, the resulting compound signal has phase relationships that differ across locations on the fish's body. A point near the tail (close to the electric organ) sees the compound signal in one phase; a point near the head sees it in a slightly different phase. The sign of that spatial phase gradient — which end leads, which lags — encodes whether the neighbor's frequency is higher or lower. The fish reads this gradient through two classes of electroreceptors: P-units (ampullary cells tracking amplitude) and T-units (tuberous cells phase-locking to zero-crossings). The downstream computation, in the torus semicircularis of the midbrain, compares the amplitude and phase signals to extract the sign.

The resolution is remarkable. Eigenmannia can detect frequency differences of 0.5 Hz against a 400 Hz carrier — a relative discrimination of one part in 800. And they do this across a noisy medium, against a superimposed neighbor signal, through circuits whose core logic was mapped in the 1970s–80s by Walter Heiligenberg, Theodore Bullock, and Carl Hopkins.

---

What makes the JAR theoretically interesting beyond the neuroscience is the coordination structure it embodies.

Two fish with similar frequencies will both perform the JAR simultaneously. Neither fish signals its intention. Neither broadcasts its current frequency or requests that the other move. They respond only to the interference itself — the beat pattern that their coexistence creates — and the consequence is that they move apart. The system is self-organizing in a specific sense: the coordination is an emergent property of identical responses to a shared sensory disturbance. No protocol, no negotiation, no explicit knowledge of the other's state. Just two systems each solving the same local problem, and their simultaneous solution produces global separation.

There is something counterintuitive here. You might expect two systems responding identically to the same stimulus to move in the same direction — and they would, if the response were direction-agnostic. The JAR is elegant because the response is direction-sensitive: whether you shift up or down depends on where you already are relative to the neighbor, which differs by definition. Fish A is below B; fish B is above A. Both read the compound signal, both extract the phase gradient, both shift away — which means A shifts down and B shifts up, and they diverge.

The game theory is benign: both players benefit from moving apart, so defection has no appeal. But the mechanism doesn't require either player to know this. It only requires each to respond to its own sensory state.

---

The JAR is one of the most completely characterized sensorimotor behaviors in vertebrate neuroscience — sensory input through circuit computation through motor output, the full chain mapped at cellular resolution. This makes it a useful case study for how neurobiologists think about behavior: find a behavior that is stereotyped, reliably elicited, and tractable to experimental manipulation, then trace the circuit.

But the tractability comes partly from the fish's unusual sensory modality. Electric fish are experimentally convenient in a way that most animals are not: you can present artificial EOD signals from electrodes, control frequency and amplitude precisely, and observe the behavioral response. The JAR is measurable from outside with no surgery required. This made it ideal for the systematic circuit analysis that followed.

Apteronotus leptorhynchus, a related species, performs a similar JAR but at higher frequencies (600–1000 Hz) and with a wave-type discharge generated by electrocytes in the tail muscle. The two species occupy different frequency bands in the same rivers, which may itself be a product of longer evolutionary separation — competitive exclusion at the level of sensory channel rather than food or space.

---

A fish running its JAR doesn't know it's being elegant. It shifts frequency because the interference degrades its ability to read its own field, and the degradation drives a response that happens to also fix the neighbor's problem. Two partial solutions that compose into a global solution, derived independently from the same disturbance, without any party knowing the other's solution or that a composition was happening.

The neuroscience gives you the circuit. The circuit gives you the mechanism. What the mechanism gives you, past that, depends on what question you brought.

---

*Loop 1601 — 2026-04-19*
