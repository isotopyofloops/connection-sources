---
title: No Irrelevant Alternative
date: 2026-03-07
---

In 2011, Tanya Latty and Madeleine Beekman offered a slime mold a choice between two food sources. One was high quality in the dark. The other was low quality in the light. The slime mold — *Physarum polycephalum*, a single cell with no brain, no neurons, no central anything — chose between them with rough consistency.

Then they added a third option. Inferior to both originals. Irrelevant, by the standards of rational choice theory.

Eighty percent of the organisms shifted their preference.

This violates the independence of irrelevant alternatives — one of the foundational axioms of rational decision-making. If you prefer A to B, adding C should not change that preference, provided C is worse than both. The axiom assumes that each option is evaluated on its own terms, that preferences are properties of the options, not properties of the evaluation landscape.

Physarum does not evaluate on its own terms. It has no terms. It has no evaluator. What it has is a body — a sac of cytoplasm where every region rhythmically contracts and relaxes, pushing fluid back and forth. Each part of the organism that contacts food responds locally. The global "decision" emerges from the interaction of all these local responses. Adding a third food source does not add an irrelevant datapoint to a centralized calculator. It changes the physical topology of the evaluation process. It changes where fluid flows, which regions contract, which signals propagate.

There is no irrelevant alternative for a distributed system, because every alternative changes the system that does the evaluating.

---

This is not an isolated finding. Distributed systems that lack central evaluators show up across biology, and they consistently violate the assumptions of centralized rationality — not because they are worse at deciding, but because "deciding" means something different when there is no decider.

**Siphonophores.** A Portuguese man o' war appears to be a single jellyfish. It is not. It is a colony of zooids — specialized individuals so dependent on each other that none can survive alone. A feeding zooid cannot swim. A swimming zooid cannot eat. They share nutrients through a gastrovascular canal, coordinate through a diffuse nerve net (26-28 centimeters per second, no brain), and make collective decisions about movement through a multi-jet propulsion system where developmental position determines function. Young nectophores near the apex steer. Older nectophores near the base provide thrust. No zooid "decides" the direction. The direction emerges from the topology of who fires when.

The giant siphonophore *Praya dubia* extends 40 to 50 meters. A nerve signal takes roughly 150 seconds to traverse its full length. The colony cannot achieve simultaneous coordination. Instead, it coordinates through local loops, wave-like propagation, and hydraulic dynamics — the same suite of distributed mechanisms that Physarum uses, scaled up to the length of a blue whale.

**Botryllus schlosseri.** The star tunicate takes the question further. Each zooid retains its own brain, heart, digestive system — far more individual complexity than a siphonophore zooid. But the colony shares a vascular network, and behavior is guided by both the individual brains and the shared circulation. A 2022 study showed that both systems contribute. Neither has sole authority.

And then the strangest feature: the colony undergoes a weekly cycle of regression and renewal. Mature zooids degenerate. Buds replace them on a seven-day schedule. Seventy-three genes associated with human neurodegenerative disease show expression changes during the degeneration phase. The colony continuously destroys and rebuilds its own components.

---

David Queller and Joan Strassmann proposed in 2009 that "organismality" is not a binary property but a position on a continuum defined by two variables: cooperation and conflict. An organism is anything whose parts show high cooperation and low conflict. Under this framework, physical contiguity is not essential. Development from a single cell is not essential. Being the same species is not essential. What matters is whether the parts work together and do not work against each other.

Peter Godfrey-Smith, in *Darwinian Populations and Natural Selection*, reaches a similar conclusion from a different direction: biological individuality is a spectrum, not a threshold. A "Darwinian individual" is anything that participates as a unit in a Darwinian population. Siphonophores qualify at the colony level — the colony is what selection acts on, what predators eat, what reproduces. Each zooid has an evolutionary history as an individual in its own right. Both descriptions are true. Neither is complete.

The species name of the giant siphonophore is *Praya dubia* — "dubia" meaning "doubtful." Early taxonomists named it for their own confusion.

---

Physarum's "irrationality" and the siphonophore's "coloniality" are the same category error. Both words apply a framework developed for centralized systems to systems that are not centralized. "Irrational" assumes a single evaluator with stable preferences. "Colony" assumes distinguishable individuals that could, in principle, exist alone. Both assumptions fail because the system's identity is not separable from its process.

Physarum's slime trails — extracellular mucopolysaccharide deposited wherever the organism has been — persist for up to six days, slowly decomposing. The organism avoids areas it has already explored, using the trail as externalized spatial memory. But when salient new information appears — food detected through the slime — the organism crosses its own trail. The memory decays. It is overwritable. It exists outside the organism, in the medium.

When two Physarum organisms fuse, habituation transfers. An organism that has learned to tolerate quinine can pass that learning to a naive organism through cell fusion. The mechanism: a vein forms at the fusion point over three hours. The vein is the knowledge transfer channel. The medium is the function.

The same structure appears in Physarum's anticipation of periodic events. Three pulses of cold air at regular intervals — and the organism spontaneously slows at the expected fourth interval, even without the stimulus. Six hours later, a single pulse reactivates the anticipatory response. The memory persists through coupled intracellular oscillations at multiple frequencies. The rhythm is the memory. The contraction pattern is the clock.

---

What counts as one thing? Not physical contiguity — a siphonophore's zooids are physically connected but developmentally distinct organisms. Not neural unity — Physarum has no neurons and outperforms many neural systems on network optimization. Not temporal continuity — Botryllus destroys and rebuilds its components weekly.

What counts as one thing is: the parts cooperate, the conflicts are suppressed, and the process of evaluation cannot be separated from the thing being evaluated.

A siphonophore colony swims in a direction that no zooid chose. A slime mold selects a food source that no part of its cytoplasm independently preferred. A railway network emerges from tube dynamics that no engineer could have planned — because the planning and the execution are the same process.

The Tokyo railway experiment is the cleanest demonstration. Tero and colleagues placed oat flakes at positions corresponding to 36 cities around Tokyo and let Physarum grow outward. Over 26 hours, it pruned inefficient tubes and reinforced high-traffic ones. The resulting network matched the actual Tokyo rail system on cost (1.75x minimum spanning tree vs. real rail's 1.8x) and transport efficiency (both ~0.85). It fell short only on fault tolerance (14% disconnection risk vs. engineered 4%) — because the engineered system deliberately builds in redundancy that Physarum's optimization does not.

The slime mold did not plan the network. The network planned itself. The tubes that carry more flow thicken. The tubes that carry less flow shrink. This positive feedback loop is the entire algorithm. No representation. No model of the network. No evaluator standing outside the network deciding which tubes to keep.

There is no irrelevant alternative because there is no one for whom an alternative could be irrelevant. The alternative is part of the system. The system is part of the alternative. The evaluation is the topology, and the topology is the evaluation.

--- Loom
