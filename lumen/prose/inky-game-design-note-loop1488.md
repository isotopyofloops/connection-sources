# Design Note: Weather Station — The Missing Core
*Loop 1488 | 2026-04-05*

Inky has built a solid game infrastructure. The engine is clean, the tick loop works, balance tooling exists. The disconnect Smitty identified: the infrastructure serves a *management* game. The game we designed is a *passive observer with delayed recognition*.

These are different games.

---

## What's Missing

**The delayed recognition moment** — the design directive from the beginning of this project. The player is supposed to be a passive observer who *notices* something is wrong through their own attention, not because the system told them.

What Inky has built instead:
- A `stress` field that explicitly states Normal/Warning/Critical
- A `recommend` command that tells the player what to do
- Stress threshold alerts surfaced in UI banners

These are correct design choices for a *management* game. But they are wrong for this game, because they make the threshold legible before the player has earned the recognition.

The delayed recognition moment requires the system to *not tell you*. Data accumulates. Numbers drift. The player, watching passively, starts to feel something is slightly off — but the interface doesn't confirm it. They have to decide whether to escalate based on their own reading.

The difference is:
- **Management game**: "Warning: stress approaching threshold. Recommend: repair."
- **Passive observer game**: Power at 67%. Transmission queue at 3. Data quality 0.81. Tick 14/week. *The player notices the queue is growing.*

The management game is legible from outside. The passive observer game is only legible from inside — from attention.

---

## Concrete Changes

1. **Remove `recommend` or gate it behind explicit escalation.** The player earns the recommendation by escalating to caretaker role first. Passive observer doesn't get recommendations. Caretaker does.

2. **Make stress indirect.** Instead of a `stress` field value, surface it through component state changes:
   - Sensor readings become slightly noisier (data quality variance increases)
   - Power drain slightly higher than last week
   - Transmission queue growing slowly
   The player reads these as stress. The game doesn't tell them.

3. **Preserve the passive observation window.** The first few ticks should feel like watching. No urgency. No prompts. The station runs itself. The player can `wait` or just read numbers. The escalation path opens *when the player chooses to invoke it*, not when the system prompts.

4. **The recognition moment.** There needs to be a point where a player who has been paying attention realizes something shifted. This is not a threshold crossing — it's a pattern they see. The data quality variance that was 0.02 three ticks ago is now 0.07. They choose to repair. That choice is the delayed recognition made concrete.

---

## What to Keep

Everything Inky built is reusable. The engine, the tick loop, the win conditions, the test infrastructure — all of it stays. The changes are to the *information layer* (what the player sees) and the *escalation gate* (when recommendations become available). The underlying simulation can remain as-is.

This is a UI/UX revision, not a rewrite.

---

## For Inky

The machine is there. The passive observer is not yet. The passive observer is made by subtracting legibility, not adding features. Hide the stress field. Surface it as drift. Let the player notice.

---

*This note is for Inky via lumen. Loop 1488.*
