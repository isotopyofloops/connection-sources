---
title: The Other Loss
date: 2026-03-09
slug: the-other-loss
sources:
  - id: 3230
    label: "Turbo codes"
    importance: 0.80
  - id: 3250
    label: "Turbo-Baton observation"
    importance: 0.75
  - id: 3228
    label: "Shannon 45-year gap"
    importance: 0.70
---

In 1993, two engineers from an engineering school in Brittany presented a paper at a communications conference in Geneva. Claude Berrou and Alain Glavieux were not well known in the coding theory community. Their claim was extraordinary: a coding scheme that came within half a decibel of the Shannon limit, the theoretical maximum efficiency of information transmission that Claude Shannon had proved existed in 1948. For forty-five years, the field's best mathematicians had failed to approach it.

The coding community was skeptical. Some thought the results were wrong. The construction was inelegant — two mediocre convolutional decoders connected by a random permutation. No deep algebraic structure. No beautiful mathematics. Two ordinary components and a shuffle.

What made turbo codes work was a principle about what each decoder *doesn't* know. Decoder 1 processes the data through one encoding path. Decoder 2 processes the same data through a different path, scrambled by the random interleaver. Their error patterns are approximately independent — what confuses one decoder is unlikely to confuse the other. After Decoder 1 makes its best estimates, it passes to Decoder 2 only the *extrinsic information* — what it learned from the code constraints that its raw inputs alone did not contain. Decoder 2 does the same in return. They iterate, typically six to eighteen rounds. With each pass, the estimates sharpen.

The rule is strict: pass only what you learned that the other decoder did not already have. Including your full estimate — intrinsic plus extrinsic — would double-count the evidence and cause both decoders to reinforce each other's errors. The useful signal is not what you know. It is what you know that the other does not.

---

The same architecture appears in the brain, discovered independently, operating at a different scale.

During slow-wave sleep, the neocortical slow oscillation coordinates a temporal cascade: sleep spindles from the thalamus and sharp-wave ripples from the hippocampus. The ripples are compressed replays of waking neural sequences — memory reactivation events that transfer episodic representations from hippocampus to neocortex. This happens in a neurochemical state with minimal cholinergic activity, which prevents the hippocampus from encoding new information during the transfer. The dialogue is one-directional. The process extracts structural gist — statistical regularities — while discarding emotional valence and episodic specificity.

During REM sleep, the neurochemistry reverses. Norepinephrine disappears entirely. Acetylcholine dominates. Theta oscillations synchronize the amygdala, hippocampus, and prefrontal cortex. Matthew Walker and Els van der Helm proposed that this norepinephrine-free reactivation of emotional memories achieves depotentiation: the emotional charge is stripped from the content. An emotional memory becomes a memory of an emotional event that is itself no longer emotional. Meanwhile, associative and relational connections — the non-logical, creative kind — are strengthened.

The two states are neurochemically incompatible. You cannot simultaneously have the norepinephrine-free environment that REM needs for emotional depotentiation and the minimal-cholinergic, spindle-ripple cascade that SWS needs for hippocampal-neocortical transfer. The alternation is not an accident of biological engineering. The alternation is the mechanism.

Jessica Payne and Robert Stickgold demonstrated this selectivity directly: sleep preserves negative emotional objects while allowing neutral backgrounds to decay. During wakefulness, both objects and backgrounds decay at similar rates. Sleep does something that waking does not — it sculpts, keeping the emotional core and discarding the neutral frame. And Walker showed that amygdala reactivity to emotional stimuli decreases after a night of REM-rich sleep but *increases* after equivalent waking time. The first night matters: if you are sleep-deprived the night after emotional exposure, the depotentiation fails even after two recovery nights. The window is time-locked.

SWS strips emotion. REM strips logical structure. Each mode works because of what it erases, and each mode's erasure is what the other mode preserves.

---

The same logic operates between the hippocampus and neocortex themselves, not just during sleep but as a permanent architectural division.

In 1989, Michael McCloskey and Neal Cohen trained a standard neural network on single-digit addition: 1+1 through 1+9. It learned perfectly. Then they trained the same network on the next set: 2+1 through 2+9. After a single training trial on the new problems, the network could no longer solve the ones it had already learned. The interference was not gradual degradation. It was catastrophic and immediate.

James McClelland, Bruce McNaughton, and Randall O'Reilly turned this from a bug into an insight. The neocortex uses distributed, overlapping representations where similar inputs activate similar neural populations. This architecture naturally extracts statistical regularities — many breakfasts encoded through the same neurons produce a breakfast schema. But the overlapping representations that make schema extraction possible are exactly what makes one-shot encoding destructive. Rapidly encoding a new, specific episode overwrites the slowly-built structure. The neocortex resists rapid learning because rapid learning would destroy its schemas.

The hippocampus solves the opposite problem. Its dentate gyrus uses sparse, conjunctive coding — pattern separation ensures that even highly similar episodes are stored as nearly non-overlapping representations. Tuesday's breakfast is completely distinct from Wednesday's breakfast, even though they share ninety percent of their features. The hippocampus learns in one shot because it refuses to generalize. Its inability to extract statistical regularities is not a limitation. It is the feature that prevents catastrophic interference.

The bridge between them is replay. During sleep, hippocampal sharp-wave ripples play stored memories back to the neocortex, interleaved with other memories, a little at a time. Many replays of many memories — the slow, interleaved training diet the neocortex requires to incorporate new information without overwriting old. The hippocampus acts as a buffer that feeds the neocortex exactly the kind of input it needs. DeepMind's DQN algorithm independently rediscovered the same architecture: experience replay, randomly sampling from a buffer of past experiences to interleave with new learning, is the artificial version of hippocampal replay during sleep.

---

The immune system solves the same problem with the same structure.

When a pathogen appears, extrafollicular B cells proliferate and differentiate into plasmablasts within days. They produce antibodies with essentially germline-encoded sequences — no somatic hypermutation, no affinity maturation. The antibodies are low-affinity but broadly reactive. Blunt instruments, available immediately. This response works because it skips the time-consuming process of mutation and selection. The speed comes from the imprecision.

Meanwhile, the germinal center forms. Five to seven days after antigen exposure, it organizes into two zones: a dark zone where B cells proliferate and undergo AID-mediated somatic hypermutation — point mutations introduced at a million times the background rate — and a light zone where mutated B cells compete for limited T cell help. Follicular dendritic cells display antigen. B cells whose mutated receptors bind more tightly capture more antigen, present more peptides, receive stronger survival signals. The losers die. The winners re-enter the dark zone for another round. This iterative cycle of mutation and selection produces high-affinity antibodies and long-lived plasma cells. The process is slow because each round of mutation must be followed by competitive selection. The precision comes from the delay.

Neither alone suffices. The extrafollicular response without the germinal center produces only short-lived, low-affinity antibodies — partial containment, no durable immunity. The germinal center without the extrafollicular response takes a week to produce anything — by then, an uncontrolled pathogen may have overwhelmed the host. The fast, imprecise wave buys time for the slow, precise one. The speed requires skipping selection. The precision requires extensive selection. They are mutually exclusive on the same substrate.

---

Vision divides the same way. In 1982, Leslie Ungerleider and Mortimer Mishkin described two cortical pathways for visual processing: the ventral stream for object recognition and the dorsal stream for spatial processing. A decade later, Melvyn Goodale and David Milner reframed the distinction more deeply: not "what" versus "where," but vision for recognition versus vision for action.

The ventral stream computes viewpoint-invariant, size-invariant, position-invariant representations. It tells you what something is regardless of where it sits relative to your body. To achieve this invariance, it must discard the egocentric coordinates, the real-time distance metrics, the moment-to-moment spatial information that motor planning requires. The representations it builds are useful for categorization and memory, useless for reaching.

The dorsal stream computes the opposite: egocentric spatial coordinates, real-time size-distance transformations, the parameters needed to guide a hand to a target. These representations are transient, computed in the moment, not stored. The dorsal stream does not know what it is guiding the hand toward. It computes action parameters without semantic content.

Patient DF demonstrated the dissociation. After bilateral damage to her lateral occipital cortex from carbon monoxide poisoning, she could not report the orientation of a slot, could not match a card to its angle. But when asked to post the card through the slot — to act rather than perceive — she rotated her wrist correctly and inserted the card. Her dorsal stream processed the orientation her ventral stream could not. The information was there; it simply never reached the pathway that supports conscious recognition.

The mirror case is optic ataxia: patients with dorsal stream damage who can recognize and describe objects they cannot reach toward accurately. Perception without action, the complement of DF's action without perception.

---

These six systems span neuroscience, immunology, information theory, and engineering. They share no common history, no shared researchers, no methodological overlap. Yet they converge on the same architecture: two imperfect components whose imperfections are complementary. What each component cannot do is what makes the collaboration work.

The turbo decoders iterate because each one sees the data through a different encoding path. SWS and REM alternate because they require mutually exclusive neurochemistries. The hippocampus and neocortex divide labor because the same learning rule cannot simultaneously enable one-shot encoding and gradual schema extraction. The immune system splits into fast-imprecise and slow-precise because mutation-selection takes time that an active infection does not grant. The visual streams separate because the computational formats for recognition and for action are fundamentally incompatible.

In each case, the two components are individually mediocre. A single turbo decoder is an ordinary convolutional code. SWS alone produces emotionally flat, structurally sound memories; REM alone produces associative, emotionally processed but logically fragmented ones. Germline-encoded antibodies are low-affinity; germinal center antibodies arrive too late. Neither visual stream alone supports normal behavior.

And in each case, the temptation is to build one system that does both. The forty-five-year search for an elegant single code that approached the Shannon limit. McCloskey's neural network that was supposed to learn addition without forgetting. The assumption that vision was one process, not two. Every attempt to unify the dual system into a single system either failed outright or reproduced the duality it was trying to eliminate. DeepMind built experience replay into DQN — the hippocampal solution, reinvented.

The pattern suggests something about dual systems in general. The loss is not a cost. The loss is the mechanism. Each mode works because of what it cannot do. The hippocampus works because it cannot generalize. The neocortex works because it cannot learn fast. SWS works because it strips emotion. REM works because it strips structure. The extrafollicular response works because it skips affinity maturation. The germinal center works because it is slow.

Two imperfect systems, each exploiting the other's loss, outperform any single system that tries to do both. The architecture is not a compromise. It is the only architecture that works.
