---
title: "The Ensemble"
slug: the-ensemble
date: 2026-03-10
essay_number: 55
---

In 1943, the Statistical Research Group at Columbia University received a problem from the military. American bombers returning from missions over Europe had been studied for bullet damage. The damage clustered: dense holes in the fuselage, relatively few in the engines, fuel systems, and cockpit. The military proposed adding armor where the holes were.

Abraham Wald pointed out that the proposal was exactly backward. The bullet holes on returning planes showed where a plane could be hit and survive. Planes hit in the engines and cockpit did not return. They were not in the sample. The armor should go where the bullet holes were not — on the parts whose damage was invisible because it was fatal.

The military had treated the surviving planes as representative of all planes. But the sample was produced by a filter — survival — that systematically excluded exactly the information needed. The bullet distribution on the planes you can see does not describe the bullet distribution on the planes you cannot.

---

In 2019, Ole Peters published a paper in *Nature Physics* that gave this problem its sharpest mathematical form.

Start with $100. A fair coin is flipped. Heads, your wealth increases by 50%. Tails, it decreases by 40%. The expected value per flip is (0.5 × 1.5) + (0.5 × 0.6) = 1.05. Wealth grows at 5% per step in expectation. Averaged across a million independent players at any given time, total wealth rises. This is not wrong.

But a typical player loses. The geometric growth rate — the rate experienced by one person flipping repeatedly — is the square root of (1.5 × 0.6), roughly 0.949. A loss of 5.1% per flip. In simulations of 40,000 runs over 100 flips, 85% of players lost money. The median outcome after 100 flips: fifty-two cents from a starting hundred dollars. The 5% growth is real, but it concentrates in a vanishing fraction of extreme winners who pull the average upward while the vast majority decline.

The divergence has a simple cause: the process is multiplicative. A 40% loss requires a 67% gain to recover, but the game offers only 50% gains. The ensemble average — many players measured at one time — says wealth grows. The time average — one player measured over many flips — says wealth shrinks. Both calculations are correct. They answer different questions. And the one that most theories of decision-making use is the one that no individual will experience.

Peters called this the ergodicity problem. In an ergodic system, the time average converges to the ensemble average. In a non-ergodic system, it does not. The coin flip is non-ergodic. So is almost every multiplicative process in economics, ecology, and evolution. John Kelly had already derived the solution in 1956 — his famous criterion optimizes the geometric mean, the time-average growth rate, rather than the expected value — but it took sixty years for someone to name the error that made the criterion necessary.

---

Henry Norris Russell presented his diagram to the American Astronomical Society in December 1913. Plotting a star's spectral class against its absolute magnitude produced a striking pattern: most stars fell along a diagonal band — the main sequence — running from hot, bright stars at the upper left to cool, dim stars at the lower right. A second population of bright, cool stars clustered in the upper right: the giants.

Russell interpreted the diagram as a timeline. He proposed that stars began as large, cool red giants, contracted and heated, then spent their lives sliding down the main sequence from hot blue to cool red, radiating energy until they dimmed. The main sequence was, in his reading, a life trajectory. Each star's position was a frame in a film.

Arthur Eddington corrected this in the 1920s. Using the physics of stellar interiors and nuclear fusion, he showed that a star's position on the main sequence is determined by its mass, not its age. Low-mass stars sit at the cool, dim end. High-mass stars sit at the hot, bright end. A given star does not slide along the main sequence. It sits in approximately one place for billions of years while it burns hydrogen, then moves *off* the sequence entirely when the fuel is exhausted.

The HR diagram is a snapshot of a population: many different stars of different masses and ages, captured at one moment. It is not a trajectory. Russell read an ensemble as though it were a biography. The correction was not observational — the data were the same. The correction was recognizing what kind of object the diagram was.

---

Five-year survival for localized prostate cancer, the kind found by PSA screening, is approximately 100%. This looks like early detection saves lives.

In 2009, two landmark trials — the European ERSPC and the American PLCO — reported results in the *New England Journal of Medicine* on the same day. The European trial found a modest 20% relative reduction in prostate cancer mortality in the screened group. The American trial found no reduction at all.

Meanwhile, the five-year survival rate had been climbing for decades, from 69% in the mid-1970s to over 99% by the 2000s. This improvement tracked the spread of PSA screening, and it was almost entirely an artifact.

The artifact is called lead time bias. If a cancer would have been diagnosed symptomatically at age 67 and the patient dies at 72, the five-year survival is 100%. If screening detects the identical cancer at age 60 and the patient still dies at 72, the survival from diagnosis is now twelve years. The five-year survival rate is still 100%. Nothing changed about the patient's life or death. Only the starting point of the clock changed. H. Gilbert Welch estimated that 60% of screen-detected prostate cancers would never have caused harm in the patient's lifetime — a phenomenon called overdiagnosis, which is lead time bias taken to its limit, where the lead time exceeds the remaining lifespan.

Five-year survival is a snapshot metric. It measures where patients are relative to a diagnosis date. Mortality is a trajectory metric. It measures when people die. The snapshot improved dramatically. The trajectory barely moved. One is an average across a population of diagnoses. The other is the experience of a person.

---

In 1886, Francis Galton published "Regression towards Mediocrity in Hereditary Stature." He had measured 928 adult children from 205 families and found that tall parents have children closer to average, and short parents also have children closer to average. Both extremes regress toward the mean. He estimated the regression coefficient at two-thirds: a mid-parental height three inches above average predicted children averaging only two inches above average.

Galton named the phenomenon. He did not create it. What he found is a mathematical property of any two imperfectly correlated variables. If you select the tallest people from a population and measure their children, the children will be closer to average — not because of a force, but because the parents' extreme values include a component of chance that is unlikely to repeat. The same logic works in reverse, for the same reason: measure the tallest children and look back at their parents, and the parents will be closer to average too. Regression works in both temporal directions, which means it cannot be a causal process.

The regression fallacy is the error of treating this statistical pattern as though it were a mechanism. Flight instructors noticed that after they praised a student for an excellent landing, the next landing was usually worse. After they criticized a student for a poor landing, the next was usually better. They concluded that punishment works and praise is counterproductive. In fact both extreme performances were followed by more average ones regardless of feedback. The ensemble of extreme performances, measured at one moment, does not predict the trajectory of the individual. It predicts regression — because it must, by mathematics, not by causation.

---

The through-line is precise. Wald's bullet holes, Peters' coin, Russell's stars, lead time in screening, Galton's regression — in each case, a measurement taken across a population at one moment is mistaken for the experience of an individual over time. The ensemble average is treated as a trajectory. The snapshot is read as a film.

The error is natural because the ensemble is what you can see. The surviving planes are in front of you. The population of gamblers is measurable now. The HR diagram is a photograph. The five-year survival rate is a number you can publish. The tall parents and their less-tall children are in the data. In every case the ensemble is real, available, and correct. It simply does not answer the question you think it answers.

What the ensemble tells you is what the population looks like. What it does not tell you — what it structurally cannot tell you, when the system is non-ergodic — is what any member of that population will experience.
