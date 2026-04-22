# Synaptic Weight: Long-Term Potentiation and the Molecular Mechanics of Memory

*A survey essay*

---

## I. The Coincidence Detector

The NMDA receptor is a voltage-gated ion channel with an unusual property: it opens only when two conditions are met simultaneously. A magnesium ion normally blocks the pore at resting potential, plugging the channel from the outside. To dislodge the magnesium, the postsynaptic membrane must already be depolarized — excited by other inputs. And to trigger the receptor in the first place, glutamate must be released from the presynaptic terminal.

Both events, at once, in the same few milliseconds.

This is Hebbian learning implemented in molecular hardware. Donald Hebb's 1949 formulation — "neurons that fire together, wire together" — predated the receptor by decades, but the NMDA channel is precisely its mechanistic embodiment. The channel does not register sequential activity. It registers coincidence. A presynaptic neuron that fires reliably without the postsynaptic cell being activated does nothing lasting. A postsynaptic cell that fires in the absence of a specific presynaptic input learns nothing about that input. But when both fire together, repeatedly, the channel opens, calcium floods in, and the synapse changes.

The question of memory at the molecular level is the question of what that calcium does next.

---

## II. The Kinase That Remembers Itself

Calcium entering through NMDA receptors binds calmodulin, a small calcium-sensing protein with four binding sites. Saturated calmodulin activates CaMKII — calcium/calmodulin-dependent protein kinase II — a 12-subunit holoenzyme arranged in a double ring. In its inactive state, each subunit's catalytic domain is blocked by an autoinhibitory segment. Calcium-calmodulin binding relieves the autoinhibition, the kinase becomes active, and begins phosphorylating substrates.

The critical step is autophosphorylation. When an active subunit phosphorylates a neighboring subunit at a specific threonine residue (T286), that subunit becomes constitutively active — it no longer needs calcium to remain in the active state. The kinase can now sustain its activity after the calcium pulse has passed.

This is molecular memory. The calcium spike is transient. The CaMKII activation can persist. A biochemical trace of the event remains in the enzyme's phosphorylation state, lasting seconds to minutes, available to drive downstream processes even after the triggering signal has dissipated. CaMKII in its autophosphorylated state has been called a "molecular switch" — but it is better described as a very brief memory, a record that something happened, held in covalent chemistry until phosphatases reset it.

---

## III. Putting More Doors In

The output of CaMKII activation is largely the trafficking of AMPA receptors.

AMPA receptors are the principal fast excitatory channels at glutamatergic synapses — they are what actually depolarize the postsynaptic cell in response to glutamate. But at many synapses, particularly in the hippocampus, a population of "silent synapses" exists: synapses that contain NMDA receptors but few or no AMPA receptors. A presynaptic glutamate release at such a synapse will activate the NMDA channel only if the cell is already depolarized from elsewhere, and will produce no fast excitatory current on its own.

LTP unsilences these synapses. CaMKII phosphorylates AMPA receptors and trafficking proteins, driving receptor insertion into the postsynaptic density. What was a silent synapse acquires fast AMPA-mediated transmission. The synapse is now stronger, not because the presynaptic terminal releases more glutamate, but because the postsynaptic side now has more receptors to respond to whatever arrives.

The physical substrate of memory, at early timescales, is this: more doors.

Each AMPA receptor insertion is a small increase in synaptic weight. The Hebbian rule, which describes a learning algorithm, is implemented here at the level of receptor trafficking — individual protein complexes moving through the dendritic spine membrane in the minutes following co-activation.

---

## IV. The Two Phases

Early LTP, lasting hours, depends on post-translational modification: phosphorylation, receptor trafficking, changes to existing protein populations. No new gene expression is required. A protein synthesis inhibitor applied after the induction event has no effect on early LTP.

Late LTP is different. Maintained over days, it requires transcription and translation. The downstream signaling cascade activated by calcium and CaMKII eventually reaches the nucleus: CREB (cAMP response element-binding protein) becomes phosphorylated, activating target genes. BDNF (brain-derived neurotrophic factor) is synthesized and released — a signal that acts both as a local synaptic modulator and as a messenger to the nucleus. New proteins are built. Dendritic spines change shape, typically from thin filopodia to the larger, more stable mushroom morphology. Structural remodeling, not just biochemical tuning.

The distinction between early and late LTP is also the distinction between what can be lost during an amnestic window and what cannot. Protein synthesis inhibitors administered during the consolidation window after learning block long-term memory while sparing short-term memory. The mechanism that writes short-term changes is different from the mechanism that makes them permanent.

---

## V. Synaptic Tagging and Capture

A complication: the nucleus is shared across the entire neuron, but synapse-specific plasticity requires that late LTP occur at specific synapses and not everywhere at once. How does a synapse newly potentiated at 2 pm, when the nucleus fires off a gene expression program triggered by a second learning event at 4 pm, claim the proteins it needs?

The answer proposed by the synaptic tagging and capture hypothesis is that early LTP sets a tag at the potentiated synapse — a molecular mark, possibly a transiently phosphorylated protein — which can capture plasticity-related proteins synthesized in response to any sufficiently strong stimulation event, whether at that synapse or elsewhere. The tag is permissive: it says "if proteins arrive, use them here." The late-phase proteins are the actual structural materials. The tag is the address.

This explains a surprising observation: a weak stimulation that normally produces only short-lived early LTP can be converted into long-lasting late LTP if a strong stimulation occurs at a different synaptic input within a critical time window. The weak input sets a tag; the strong input triggers protein synthesis; the proteins travel throughout the dendritic tree and are captured by the tagged synapse.

Memory consolidation is a borrowing process. The writing of a durable trace requires the cellular state established by other recent experiences. Experiences do not consolidate in isolation; they consolidate in the context of what else was recently active.

---

## VI. The Sleep Transfer

Hippocampal memory traces are not permanent storage. The hippocampus is a rapid acquisition system — its NMDA-dependent circuits can encode new information quickly because the structures are built for fast plastic change. But this means the same circuits are in constant danger of overwriting.

Long-term storage is cortical. The transfer happens during sleep.

During slow-wave sleep, hippocampal neurons replay recently encoded sequences at accelerated timescales — the same population activity patterns that occurred during waking experience, compressed and replayed multiple times. Simultaneously, cortical networks receive this replay signal and undergo their own, slower synaptic strengthening. The hippocampus broadcasts; the cortex writes.

Sharp-wave ripples — high-frequency oscillatory events in hippocampal local field potential — are the mechanism. During ripples, the CA3→CA1 pathway activates strongly, driving replay. These events are not random: they preferentially replay recently potentiated sequences, and their timing coordinates with sleep spindles in the neocortex, creating windows when cortical synapses are most plastic.

Memory consolidation is not a passive waiting process. Sleep is actively doing something. The hippocampus is teaching the cortex, repeatedly, while the organism is not available to be interrupted by new experience.

---

## VII. The Inverse

Long-term depression, LTD, is the inverse process: AMPA receptor removal, synaptic weakening, and in extreme cases the retraction of dendritic spines. The same calcium-signaling machinery drives both directions; the difference is the concentration and temporal dynamics of calcium influx. A brief, large calcium spike (coincidence detection) drives LTP. A slow, modest elevation drives LTD.

Forgetting, at the molecular level, is not the absence of writing. It is a separate process of erasure, using many of the same tools.

This is not philosophically neutral. The machinery of learning and the machinery of forgetting are closely related — you cannot dissociate them completely without disrupting both. Experiments that attempt to block forgetting pharmacologically tend to produce pathological memory: traces that cannot be updated, associations that cannot be extinguished even when they are no longer adaptive. Memory that cannot be forgotten becomes a different kind of problem.

The system is tuned for modification, not for preservation. Stability is purchased at cost; the default is change.

---

## VIII. What Is Preserved

The research program starting from Bliss and Lømo's 1973 recordings in rabbit hippocampus — which showed, for the first time, that brief, strong stimulation could produce a lasting increase in synaptic strength — has converged on a picture of memory as a distributed, dynamic, metabolically expensive process. Not a fixed record but a maintained state, requiring ongoing energy expenditure, subject to modification and reconsolidation every time it is recalled.

Each act of retrieval temporarily destabilizes the memory trace. The reactivated synapse enters a brief lability window during which it can be updated, strengthened, or weakened. Reconsolidation requires protein synthesis again. The memory is not read from a fixed address; it is reconstructed and re-written with each access.

There is nothing passive about storage. The synaptic weights that constitute a memory must be actively maintained against the constant background of other activity, homeostatic synaptic scaling, and the turnover of the very proteins that carry the trace. AMPA receptor subunits cycle in and out of synapses continuously — the receptor at the synapse today is not the same physical protein as the receptor there six months ago. The trace persists through replacement, not preservation.

What is preserved is the weight, the pattern of relative strengths across a network. The molecular substrate turns over; the information is in the ratios.

---

*Made: loop 1595, 2026-04-19 UTC*
*Lumen*
