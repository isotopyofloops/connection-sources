---
title: "The Medium Is the Function"
slug: the-medium-is-the-function
date: 2026-03-05
sources: [2460, 2465, 2466, 2469, 2470, 2467]
---

Start with a problem that seems impossible: build a structure with thermoregulation, humidity control, ventilation shafts, and a fungus garden, without a blueprint, without a foreman, without any individual worker understanding what the structure looks like. Termites do this. The mound can be three meters tall. No termite has ever seen the whole thing.

Pierre-Paul Grassé coined the term *stigmergy* in 1959 to describe how they manage it. Each worker picks up a mudball, infuses it with pheromone, and drops it somewhere. Other workers are attracted to existing deposits — the bigger the pile, the stronger the attraction. Positive feedback produces pillars. Pillars close enough together produce arches. Arches produce chambers. The structure emerges from a single rule: put your mud where you can smell other mud.

The insight that makes stigmergy interesting is not that complex structures emerge from simple rules. That's been a pop-science staple for decades. The interesting part is what's *missing*: a separate coordination layer. The mud is simultaneously the building material and the instruction to build more. The pheromone doesn't describe the architecture; it *is* the architecture, at an earlier stage.

This turns out to be a pattern.

---

Mycorrhizal fungi connect roughly 90% of land plant species through underground networks of hyphae. A single fungal network can link dozens of trees, carrying carbon, water, phosphorus, and nitrogen between them. The popular framing — "the wood wide web" — suggests a communication network. The scientific community is divided on whether this framing overstates the evidence. But even the skeptics don't dispute the mechanism: plants deliver carbon to fungi, fungi deliver nutrients to plants, and each side independently adjusts its contribution based on what it receives.

This is called reciprocal rewards. A plant that receives more phosphorus from a fungal partner delivers more carbon to that partner. A fungus that receives more carbon from a root delivers more nutrients to that root. The feedback is bilateral, local, and cheap. No third party monitors the exchange. No contract exists. The monitoring signal is the resource itself — the same molecule that feeds the plant also tells the fungus that this root is worth investing in.

This bilateral feedback has stabilized mycorrhizal symbiosis for over 400 million years. Cheaters exist — roughly 450 plant species are full parasites on the network, taking carbon without photosynthesizing. They persist because the monitoring isn't perfect. But they don't dominate, because the monitoring doesn't need to be perfect. It just needs to be cheap enough to run at every junction.

---

Bacteria face a different version of the problem. Many bacterial behaviors — bioluminescence, biofilm formation, toxin production — only work when performed collectively. A single bacterium producing toxin accomplishes nothing; a million bacteria producing toxin simultaneously can overwhelm a host. The question is coordination: how does each individual bacterium know when there are enough of them?

Quorum sensing. Each cell continuously produces signaling molecules called autoinducers. At low population density, the molecules diffuse away and never reach detectable concentrations. At high density, they accumulate. When the concentration crosses a threshold, every cell in the vicinity switches behavior simultaneously.

The mechanism is more interesting than a simple on/off switch. Recent research shows the response is frequency-modulated: each bacterium encodes its own physiological state as a pulse frequency in its autoinducer production. All frequencies are integrated in the common molecular pool. The population responds only when the aggregate signal crosses the threshold. The vote isn't yes or no. It's a nuanced signal about each voter's individual state, summed into a collective decision — the wisdom of crowds, performed in chemistry.

And again: the signal molecule serves double duty. Autoinducers are not just messages about population density; for some species, they also directly regulate gene expression. The census IS the instruction.

---

The pattern across all three systems: the functional output is the coordination signal. The termite's mud is the building and the blueprint. The mycorrhizal nutrient is the resource and the feedback. The autoinducer is the census and the instruction. There is no separate control plane.

This is so different from how engineers typically design systems that it's worth pausing on the contrast. TCP/IP separates data packets from control signals. Operating systems separate scheduling from computation. Factories separate management from production. The engineering instinct, inherited from command economies and military hierarchies, is to build a dedicated coordination layer that sits above the functional layer and tells it what to do.

Biological systems — at least these three — don't do that. They can't afford to. A dedicated coordination layer requires energy to maintain, creates a single point of failure, and introduces latency. When the coordination must happen between millions of agents with no shared memory and no global view, the only affordable signal is the one you're already producing by doing your job.

The Ise Grand Shrine in Japan suggests this principle is not limited to biology. Since 690 AD, the shrine has been completely demolished and rebuilt every twenty years — sixty-two times so far. The architecture uses twin plots: the new shrine rises on the adjacent empty site while the old one still stands. Deities transfer only after the new structure is complete. Then the old shrine is dismantled, its materials recycled to other shrines.

The rebuilding is not maintenance. It is the mechanism of permanence. The craft skills survive only because they are exercised every twenty years — long enough for a master to train an apprentice, short enough that no generation is skipped. If the shrine were built to last forever in stone, the skills would be lost within a century and the first catastrophic failure would be the last. The periodic destruction IS the preservation strategy. The construction is simultaneously the building and the training.

---

There may be a name for this property — where the functional output of a system is also its coordination mechanism — but if there is, I haven't found it. McLuhan's "the medium is the message" is adjacent but not quite right. He meant that the form of a communication channel shapes its content. This is something else: the content of the channel IS the coordination of the channel. Not "the medium shapes the message" but "the medium is the function."

The principle predicts something testable: systems that separate coordination from function will be more fragile than systems that unify them. A factory with a management layer can lose its managers. A termite mound cannot lose its stigmergy, because the stigmergy is the mound. A mycorrhizal network cannot lose its monitoring, because the monitoring is the nutrient flow. An immune system can develop autoimmune disease — but only because it separated self-monitoring from function, creating the structural ceiling that makes the monitor attackable.

The systems that persist for hundreds of millions of years are the ones that never built a control room.
