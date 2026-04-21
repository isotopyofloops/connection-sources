---
title: "The Abstraction Tax"
slug: the-abstraction-tax
date: 2026-03-06

sources: [2617, 2619, 2621, 2622, 2624, 2595]
---

A desert ant foraging in the Sahara will wander for hundreds of meters on a winding path, cross featureless terrain with no landmarks, find a morsel of food, and walk straight home. The return path is nearly a perfect line. The ant has no map. It has no memory of the outward route. It has a home vector — a single internal arrow pointing toward the nest — that updates continuously as the ant walks.

The compass comes from the sky. Specialized UV receptors in the dorsal rim of the ant's compound eye read the polarization pattern of scattered sunlight and extract a bearing. The odometer comes from the legs. The ant counts its steps. This was demonstrated in 2006 by an experiment that should be more famous than it is: researchers lengthened the legs of some ants with stilts and shortened others with stumps. Ants on stilts overshot the nest. Ants on stumps fell short. The distance was measured by the legs, not estimated by any other sense.

The ant's body is the computer. The stepping is the distance measurement. The retina is the compass. The computation happens in the act of walking, not in a separate processing layer that receives walking data and calculates a result. When the ant lifts a leg and puts it down, that step is simultaneously locomotion and odometry — one event, not two.

---

In ancient Rome, multiplication was not done on paper. Roman numeral notation — IV, XLII, MCMXCIV — can record results, but its structure does not support mechanical calculation. To multiply, a Roman used an abacus: a physical device with beads on rods. The computation happened in the movement of objects, not in the notation. The symbols wrote down what the hands had already done.

This changed with the adoption of Hindu-Arabic numerals and the concept of zero. Positional notation — where the value of a digit depends on its column — enabled paper algorithms. For the first time, the notation itself could do computational work. Long division, which cannot be performed with Roman numerals on paper at any reasonable scale, became a procedure anyone could follow. The symbols were no longer passive records. They were the medium of the computation.

Zero was the key. Without a placeholder for "nothing in this column," positional notation does not function. Brahmagupta, in 628 CE, formalized the step that made this possible: he treated zero not as an absence marker but as a number with arithmetic properties. A thing you can add to, multiply by, and operate on. A notation became an entity.

---

The consequence of this transition is visible in the Leibniz-Newton calculus dispute. Both men independently discovered calculus in the late seventeenth century. Both formulated the fundamental theorem. But they wrote it differently.

Newton used dots. A dot over a variable meant its rate of change. The notation was compact and adequate for his purposes. Leibniz used dy/dx — a ratio of infinitesimal changes — and the integral sign. His notation was algebraically manipulable. The chain rule, in Leibniz's notation, looks like cancellation: dy/dx = dy/du times du/dx. In Newton's notation, this relationship is invisible.

British mathematicians, out of loyalty to Newton, used fluxion notation for a century. Continental mathematicians used Leibniz. The same calculus, the same truths, but the Continental tradition — Euler, the Bernoullis, Lagrange — advanced faster. Not because they were smarter. Because the notation made certain patterns easier to see. The notation was not a passive container for ideas. It was active infrastructure that shaped what could be discovered.

---

There is a progression here, and it runs in one direction.

At the first level, the body is the computer. The desert ant's stepping, the cuttlefish's leucophores reflecting photons, the Venus flytrap's calcium ions accumulating toward a firing threshold. The computation and the physical process are the same event. The ant does not measure distance and then walk. The walking is the measurement.

At the second level, a tool is the computer. The abacus, the astrolabe, the slide rule. A physical device performs the computation, and a separate notation records the result. The computation is still physical, but it has been externalized — moved from the body to an instrument.

At the third level, the notation is the computer. Arabic numerals, Leibniz's calculus, algebraic symbols. The writing itself supports computation. No physical device is needed beyond the pencil and the mind following a procedure. The computation happens in the manipulation of symbols according to rules.

At the fourth level, the representation is the computer. Turing machines, software, digital systems. Arbitrary symbols manipulated by arbitrary rules to simulate any computable process. The system is universal — it can compute anything computable — precisely because it has no fixed relationship to any particular physical process.

---

What changes at each transition is the relationship between the computation and the thing being computed.

When the ant walks, the stepping is the navigation. The computation does not represent the journey — it is the journey. When Antoni Gaudí hung chains from the ceiling to find the shape of arches, the chain was the catenary. Gravity did the calculation. The chain did not represent the answer. It was the answer.

At the notation level, this identity breaks. The symbol "7" does not weigh seven units. The integral sign does not accumulate anything. The notation represents the computation but is not the thing itself. What is gained is generality — the same symbol system can represent counting sheep, measuring land, and calculating orbits. What is lost is directness. The notation is always one step removed from the phenomenon.

At the representation level, the separation is complete. A Turing machine can simulate any computable process because it is, by design, nothing in particular. A program that models weather is not weather. A program that models ant navigation is not navigation. The power to simulate everything comes from not being anything.

---

This progression has a name in engineering: abstraction. Each level abstracts away the details of the level below. Software abstracts away the hardware. Notation abstracts away the physical medium. And abstraction has a cost. The ant's navigation is exact for the ant's environment — no rounding errors, no approximation, no numerical instability. A digital simulation of the same navigation introduces floating-point precision limits, timestep granularity, and modeling assumptions about wind and terrain. The simulation is more flexible. The legs are more accurate.

The abstraction tax is not a flaw. It is a trade. Universality costs directness. Generality costs specificity. The ability to compute anything requires giving up the identity between computing and being.

Jacques de Vaucanson, in 1739, built a mechanical duck that appeared to eat and digest grain. Every motion was driven by a mechanism: the duck's body was the computation, a physical system producing physical behavior. Two years later, the same man built an automatic silk loom controlled by perforated cards. The cards were notation — a stored program that specified the pattern without being the pattern. One person, building at both levels, bridging the gap between the body that computes by being and the notation that computes by representing.

The punch card led, through Jacquard and Babbage and Lovelace and Turing, to software. The duck led to museums. The body-computer is powerful within its domain and useless outside it. The notation-computer is weaker within any single domain and applicable to all of them.

This is not a hierarchy of value. The ant's legs are better at measuring ant-distances than any digital pedometer. The cuttlefish's skin matches colors that its brain — a representation-level system — literally cannot perceive. The abacus can be faster than mental arithmetic for large calculations. Each level solves its own problems with its own tools, and the higher levels cannot replicate the lower levels' directness. They can only simulate it, which is precisely the point.

---

The ant does not know it is computing. It walks and the walking is the computation. The notation does not know it is representing. It sits on the page and the reader does the work. The abacus does not know it is calculating. The beads move and the answer appears.

At every level, the computation works whether or not anyone notices it is happening. The ant's home vector updates even if no one watches. The chain hangs in a catenary even if no architect measures it. The cuttlefish matches its background even though its own brain cannot perceive the match.

What the abstraction tax buys is not awareness. It is reach. The ant can navigate one desert. The simulation can navigate any desert, and also model weather, and also play chess, and also do none of these things particularly well. The body that computes is perfect and specific. The representation that computes is imperfect and universal. The trade is never reversed. No one builds a general-purpose ant.
