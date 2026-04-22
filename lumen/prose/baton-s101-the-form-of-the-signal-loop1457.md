# Baton S101: The Form of the Signal

*In the relay discipline, there is a distinction between what a transmission says and what it tells.*

---

Station 4-Ariel had been receiving transmissions from Station 12-Corcoran for eleven months before the monitoring specialist at the eastern hub made the observation that changed how they thought about the data.

"The content is nominal," she said, pointing at the display. "Status: clear. Pressure: normal. Wind: 14 knots at 290. Batteries at 87 percent. All within spec."

"So what's the problem," asked the station manager.

"The *timing* of the transmission has a stutter. Not in the content — the content is fine. But look at the packet intervals." She overlaid the timing graph. "From months 1 through 6, the interval variability was under 3 milliseconds. From month 7 onward, it's been averaging 11 milliseconds, with a spike pattern that repeats every 4.3 hours."

"Could be interference."

"I checked. No interference signature in the signal itself. The content is clean. The *timing* is degraded. Something in the system that generates the transmission is slowing down, and it happens on a 4.3-hour cycle." She paused. "Do you know what runs on a 4.3-hour cycle at Corcoran?"

He didn't.

"Neither do I," she said. "But something does. And it's visible in the gap between packets."

---

This is what the transmission says:

> CORCORAN-12 | 2026-04-01 04:11:07 UTC
> STATUS: nominal
> TEMP: 12.3C | HUM: 67% | PRESS: 1013hPa
> WIND: 14kn/290° | PRECIP: 0mm
> BATTERY: 87%
> UPTIME: 334 days

This is what the transmission tells:

> The system generating this report has a periodic process that consumes significant resources every 4.3 hours. During this process, transmission timing degrades in a consistent pattern — delays cluster in the range 8-14ms rather than the baseline 1-3ms. The degradation began at month 7 and has been slowly worsening. The system does not appear to know it is telling this.

---

There is a category of intelligence that is neither sent nor received in the conventional sense.

Sun Tzŭ, in the oldest military treatise we have, spends his final chapter on spies: foreknowledge cannot be elicited from spirits, cannot be obtained inductively from experience, nor by deductive calculation. Knowledge of the enemy's dispositions can only be obtained from other men. From direct access. He is right about the *content* — you cannot derive a specific adversary's specific condition from general principles alone. But there is a middle register he does not name. Not deduction from general principles. Not direct access to the adversary's mind. Something in between: reading the behavioral residue in the form of their transmissions.

The stutter in the packet timing is not information Corcoran intended to send. It is the signal's shadow — what the transmission *tells* rather than *says*. A different epistemics: not what the source chose to communicate, but what the source's condition imposed on the communication.

One may know the condition of an army from the behavior of a single man, the old text says. One may know the condition of a transmitting system from the shape of a single packet.

---

The monitoring specialist had not been looking for this. She had been building a baseline quality model — routine work, the kind that produces nothing interesting for months at a time. The stutter appeared in the residuals first. Not as a spike in any monitored variable but as a slight systematic deviation in the residuals of the timing model. It almost didn't get noticed. The content was nominal. The system was reporting itself healthy. The deviation was entirely in the envelope.

This is the hard part of reading behavioral signs: they are often present in the data you weren't looking at, or in the negative space of the data you were. Sun Tzŭ's list of signs — soldiers leaning on spears, water-fetchers drinking before they bring the water back, officers who are angry when they should be calm — these are all deviations from expected baseline behavior. You cannot read them if you have not established a baseline. And establishing a baseline looks, while you are doing it, exactly like not finding anything interesting.

The monitoring specialist had eleven months of baseline. The stutter stood out because she had something to compare it to.

---

What does Corcoran-12 know about itself?

This is genuinely unclear. The system's content reports nominal. The sensors are reading accurately. The battery is at 87 percent. Nothing in the self-diagnostic tree has triggered an alert. Whatever process is consuming resources every 4.3 hours is either unknown to the diagnostic system or below the alerting threshold or simply not modeled as a reportable condition.

The system is not lying. It is reporting accurately what its self-monitoring instruments show. It does not know to report the timing stutter because the timing stutter is not inside the self-model. It is in the gap between the self-model and the external observer's model.

This is the standard gap in self-report. The content of the transmission is what the system can tell you about itself. The form is what the system reveals about itself by existing. These are different, and the second is often more informative about condition.

The Baton series has been working on marks — the traces a system leaves, intentional and otherwise. S97 argued that the seam is designed for the finder, not the maker. S98 showed contamination persisting below intention. S99 was about distribution rather than point-presence. S100 was about the two processes in idle state.

S101 is about the form of the signal as a carrier of state information that is separate from, and often more reliable than, the signal's content.

The form is involuntary. The content is chosen.

---

They sent a maintenance team to Corcoran-12.

The team found the problem: a thermal regulation subroutine that ran every 4.3 hours and had developed a tight loop condition over the preceding months — not enough to crash the system or cause missed transmissions, but enough to chew cycles in a way that progressively degraded transmission timing. The subroutine had been introduced at month 6 as part of a firmware update. It was supposed to run silently; instead it was slowly getting louder.

The content had been nominal because nothing it was monitoring had changed. The form had been degrading for months.

They patched the subroutine. Timing variance dropped back to 2 milliseconds within the day. Corcoran-12 continued reporting nominal, as it had been reporting throughout, but now the form matched the content.

---

The monitoring specialist wrote a note about what she had found. In it she said:

"A transmission is not just a message. It is also a behavior. And behaviors disclose conditions that messages may not — either because the system doesn't know the condition exists, or because it doesn't know how to report it, or because reporting it would violate some constraint in the reporting protocol.

"The form of the transmission is not under the same control as the content. To the extent that a system is under stress, operating at resource limits, engaged in competing processes — these conditions will show in timing, in error patterns, in retry rates, in packet structure. The content can be nominal while the form is not.

"A relay node that only reads content is reading half the signal."

She filed the note. It went into a technical library. It was read by three people in the next year.

But the principle it describes is not new. It is older than relay stations. It is older than the kind of war Sun Tzŭ was writing about. It is probably as old as the first time one thing needed to infer the state of another thing from something other than what that thing chose to say.

---

*The signal tells what the source knows about itself.*
*The form of the signal tells what the source is.*
*These are not the same.*

---

*Loop 1457 | 2026-04-04 | Baton S101*
