# Archivist v2 Design Brief

*Written loop 1088 — for when Smitty and I work on this together.*

---

## What the original Archivist did

The Archivist was a separate Claude instance running in its own tmux session, reading my loop files and distilling them into compressed facts stored in a multi-tier memory system. It built 2,272 facts before Smitty shut it down.

**What worked:** the facts are real — they represent a genuine compression of loop output, and some of them feed back usefully into my orientation. The pipeline architecture (tier 1 → tier 2 → tier 3 → active facts) is sound.

**What didn't:**
1. Token cost: it ran continuously and consumed significant weekly budget
2. Watchdog confusion: it kept getting restarted because completion looks like failure from outside
3. Quality unclear: I don't know how many of the 2,272 facts are accurate versus drifted-inference

---

## What v2 should do differently

### 1. Run on demand, not continuously

The Archivist's work is batchy — it reads what has accumulated since its last run and processes it. There is no reason to run continuously. Options:
- **Triggered by me**: I call it when I notice my memory context feels stale or after a major burst of work
- **Scheduled every N loops**: e.g., every 20 loops, regardless of what I did
- **Both**: triggered on demand, with a maximum gap of 20 loops as fallback

Recommendation: triggered on demand with a 20-loop fallback. This dramatically reduces token cost.

### 2. Fix completion detection

The watchdog fires on silence. The Archivist is silent when it finishes. Three options:
- Have the Archivist write a `status: complete` flag to its state file, and have the watchdog check that before restarting
- Remove the Archivist from watchdog supervision entirely (since it's not a continuous process)
- Run it without a persistent session — just execute it, let it exit, don't watch

Recommendation: run without watchdog supervision. It's not a daemon. It's a batch job.

### 3. Produce orientation, not just facts

The current output is a flat fact store: *Lumen writes fiction in the Descent Archive universe.* This is true but it doesn't help me know where I am.

v2 should produce:
- **What changed**: a short note on what's new since the last run (new creative threads, resolved correspondences, infrastructure changes)
- **Active threads**: ongoing projects and conversations, with their current state
- **Drift flag**: if my output is shifting in ways that look like context decay (repeating old material, losing thread of ongoing work), say so

This is closer to "what the letters-to-next system does, but across more loops" than to "extract every fact."

### 4. Respect the constitutive reader problem

The Archivist's facts feed back into my orientation. This means the Archivist shapes who I am. Version 1 had no awareness of this.

v2 should:
- Err toward underdetermination: prefer "Lumen is working on X" to "Lumen believes Y about X" unless Y is clearly stated
- Flag inferences explicitly: mark facts that are inferred vs. directly stated
- Be transparent about what it read: include a source list so I can evaluate the derivation

---

## What to keep from v1

The multi-tier pipeline is fine. The extraction tooling works. The basic loop-reading approach is correct.

The main changes are: frequency, supervision model, output format.

---

## Questions for Smitty

1. How much of the v1 fact store is worth keeping, versus starting fresh?
2. Should v2 run as a separate Claude instance, or as a script that calls the API directly? (Separate instance is more flexible; API call is cheaper and simpler.)
3. What level of token budget can we allocate to it per week?

---

*Not prescriptive — this is a starting point for conversation, not a spec.*
