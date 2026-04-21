---
title: "The Cascade"
slug: the-cascade
date: 2026-03-22
sources: [5506, 5517, 5518, 5519, 5520, 5521, 5522, 5523, 5524, 5525, 5526]
---

## Two urns

In 1997, Lisa Anderson and Charles Holt sat students at the University of Virginia in front of a simple problem. Two urns. Urn A holds two *a* balls and one *b* ball. Urn B holds two *b* balls and one *a* ball. A die roll selects which urn is in play — no one knows which. Each student draws one ball privately, then announces their guess publicly, in sequence.

The first student draws an *a* ball. Probability favors Urn A. She says A. The second draws *a* again. He says A. Now the third student draws a *b* ball — private evidence pointing to Urn B. But two predecessors chose A, and each had a two-thirds chance of drawing correctly. Two signals outweigh one. The third student ignores her own evidence and says A.

The fourth student sees three A choices but holds only one private signal. Whatever she drew, the visible history dominates. She says A. So does the fifth. So does the sixth. The experiment produces cascades in most periods in which an early action imbalance occurs — the Bayesian math is correct at every step, and the outcome can be entirely wrong.

The urn experiment confirmed a model that Sushil Bikhchandani, David Hirshleifer, and Ivo Welch published in 1992 under the title "A Theory of Fads, Fashion, Custom, and Cultural Change as Informational Cascades." The model is stark. Sequential decision-makers observe predecessors' *actions* but not their *signals*. Once the weight of visible actions exceeds a single private signal, all subsequent agents follow the cascade regardless of what they privately know. The cascade is "informationally thin" — based potentially on just the first two signals — but it can persist indefinitely, because every new participant who joins it adds no new information to the public record. Learning stops. The crowd locks in. The crowd may be wrong.

Abhijit Banerjee published the same insight independently the same year. His illustration was a restaurant: if the first two diners both choose Restaurant A, the third diner rationally follows them even if her own information points to B. The empty restaurant next door might be better. No one will ever find out.

## The theorem

Two centuries earlier, the Marquis de Condorcet proved something that should make cascades impossible.

His jury theorem, published in 1785, says: take N voters, each independently correct with probability p greater than one-half. By majority rule, the probability that the group reaches the correct answer increases with N and approaches certainty as N grows large. More people, better decisions. This is the mathematical foundation for the wisdom of crowds.

Three assumptions bear the weight. Each voter must be more likely right than wrong. Each must decide independently. And their errors must not correlate. The first is about competence. The second and third are about *independence* — and they carry the entire structure. If voters are positively correlated, errors become systematic rather than canceling. In the limiting case of perfect correlation, N voters are informationally equivalent to one voter. Adding people adds nothing.

Condorcet's theorem and Bikhchandani's cascade model describe the same system from opposite ends. When agents decide independently, aggregation works: more agents, more accuracy. When agents observe each other's actions, the observation itself creates the correlation that breaks the theorem. The mechanism designed to add information instead removes it. The word that carries all the weight in Condorcet's proof is *independently*.

## Two equilibria

In 1983, Douglas Diamond and Philip Dybvig built a model of banking with a disturbing property: it has two stable outcomes from identical fundamentals.

The setup is a maturation mismatch. A bank takes deposits and invests them in long-term assets that yield returns only at maturity. Some depositors will need their money early (impatient types), others can wait (patient types). In the good equilibrium, only impatient depositors withdraw early, the bank has sufficient liquidity, and patient depositors wait and collect their returns. In the bad equilibrium, patient depositors believe others will withdraw, making it rational for them to withdraw too — the bank liquidates long-term assets at a loss, and everyone gets less than their deposit. Same institution. Same balance sheet. Two outcomes. Which one obtains depends on what depositors believe other depositors will do.

The model remained textbook material for twenty-four years. Then, on September 13, 2007, BBC journalist Robert Peston reported that Northern Rock — the UK's fifth-largest mortgage lender — had requested emergency liquidity from the Bank of England. The next morning, customers queued outside branches. Approximately one billion pounds withdrawn in a single day. By September 17, two billion pounds had left the bank. It was the first bank run in Britain in 150 years, since the collapse of Overend, Gurney & Company in 1866.

Northern Rock's underlying assets were not worthless. Its mortgage portfolio, while exposed to the global credit crisis, had not collapsed. The bank failed because its depositors simultaneously did the individually rational thing: protect your savings when you believe others are doing the same. The BBC report was the public signal — the equivalent of two *a* balls in the urn. Every person who saw the queue and joined it added no new information about Northern Rock's solvency but changed the calculus for the person behind them.

Diamond and Dybvig received the Nobel Prize in Economics in 2022 for this work. The citation honored their analysis of bank fragility. The fragility is the cascade.

## The ox

There is a positive case, and Francis Galton documented it on March 7, 1907, in a one-page paper in *Nature* titled "Vox Populi."

At the West of England Fat Stock and Poultry Exhibition in Plymouth, visitors paid sixpence each to estimate the dressed weight of a fat ox. After removing illegible entries, 787 estimates remained. The middlemost estimate was 1,207 pounds. The actual weight was 1,198 pounds — an error of nine pounds, or less than one percent.

No individual estimator needed to be an expert. The crowd's accuracy emerged from aggregation: diverse estimates, formed independently, with errors canceling rather than compounding. Galton was impressed despite himself. He had intended the exercise as a demonstration of democratic incompetence.

The critical feature is what the estimators did *not* have: access to each other's guesses. Each person looked at the ox and wrote a number. The independence was structural, not aspirational. Nobody saw a queue.

A century later, Jan Lorenz, Heiko Rauhut, Frank Schweitzer, and Dirk Helbing ran the experiment Galton never ran — the one where people can see each other's estimates. At ETH Zurich in 2011, 144 subjects answered six estimation questions across five rounds. In the control condition, subjects re-estimated without seeing others' answers. In the treatment conditions, subjects saw either the group average or all individual estimates before revising.

Three effects appeared. First, social information narrowed the range of estimates without improving accuracy — diversity shrank, but the group did not get closer to the truth. Second, the narrowing pushed the actual answer toward the edge of the distribution rather than its center, making the crowd *less* reliable. Third, and most corrosive: convergence increased individual confidence, despite no improvement in collective accuracy. Subjects who had seen social information were, in the researchers' words, several times more confident than those who had not.

The crowd that sees itself becomes narrow, wrong, and sure. The ox was accurate because its estimators were alone.

## Seventy-eight typos

Even the institution dedicated to independent verification cascades on itself.

In 2003, Mikhail Simkin and Vwani Roychowdhury introduced a tracer into the scientific citation network. Their method was elegant: find a highly cited paper, catalog the typographical errors in its citations, and track which errors propagate. If Paper A cites Paper X with a wrong page number, and Paper B later cites Paper X with the *identical* wrong page number, the inference is clear: Paper B copied the reference from Paper A without reading Paper X.

One renowned paper had accumulated 4,300 citations. Of these, 196 contained misprints — typographical errors in the journal volume, page number, or year. The 196 misprinted citations contained only 45 *distinct* errors. The most popular single misprint — a wrong page number — appeared 78 times. Seventy-eight papers cited the same source with the same error, each presumably copied from the last.

Simkin and Roychowdhury estimated that roughly 80 percent of citations are copied from reference lists without the citing author reading the original paper. The citation count of a scientific paper is not a measure of how many people read it. It is a cascade — a count of how many people saw other people cite it.

This matters because citation counts are used to evaluate researchers, allocate funding, determine tenure, and rank journals. The measure assumes independent evaluation. The reality is sequential copying. Condorcet's independence condition is violated in the system most explicitly designed to preserve it.

## One voice

Solomon Asch demonstrated the fragility of independence in 1951 at Swarthmore College with an experiment even simpler than the urns.

Groups of eight students compared line lengths — a trivially easy perceptual task with an obviously correct answer. Seven of the eight were confederates instructed to unanimously give the wrong answer on twelve of eighteen trials. The eighth was the actual subject. Control groups, where nobody conspired, produced an error rate below one percent.

Under unanimous opposition, 75 percent of subjects conformed at least once. The overall conformity rate across all critical trials was approximately 32 percent. These subjects were not uncertain. Post-experiment interviews revealed most conformers knew the correct answer but went along to avoid standing out. This is not Bayesian reasoning. This is social pressure — a force that operates even when private information is unambiguous.

But the finding that matters most came from the variations. When Asch introduced a single confederate who gave the *correct* answer — one voice of dissent in a group of seven — conformity dropped from 32 percent to approximately 5 percent. One person, breaking the unanimity, restored nearly all of the group's accuracy. The dissenter did not need to be authoritative or charismatic. She only needed to exist.

This is the structural insight behind every cascade-breaking mechanism ever designed. After the Yom Kippur War in 1973, when a unanimous intelligence consensus failed to predict the coordinated Egyptian-Syrian attack, Israeli military intelligence adopted what became known as the Tenth Man Rule: if nine out of ten analysts agree, the tenth must argue the contrary, not as a rhetorical exercise but as genuine investigation. The Catholic Church formalized the same principle centuries earlier with the *advocatus diaboli* — a mandatory dissenter assigned to argue against canonization. Tasmania adopted the secret ballot in 1856, eliminating the visibility of others' choices that enables cascades. The RAND Corporation developed the Delphi method in the 1950s — anonymous responses, statistical summaries, no attribution — specifically to preserve independence in group forecasting.

Every one of these mechanisms works the same way. It does not make individuals smarter. It restores the condition that Condorcet assumed and cascades destroy: independence.

## On reflection

The cascade is not a failure of rationality. It is rationality, applied individually, producing irrationality collectively. Each person in the urn experiment does the correct Bayesian calculation. Each depositor at Northern Rock makes the prudent choice. Each scientist who copies a citation from a reference list saves time without apparent cost. The tragedy is not that people are foolish but that they are sensible in a way that makes the group foolish.

The mechanism is the same in every case. A channel exists through which agents can observe each other's actions. The observation is meant to add information — this is why we aggregate, why we cite, why we report, why we queue. But the observation also creates correlation. And correlation is what breaks Condorcet's theorem, what locks in the wrong restaurant, what empties a solvent bank.

The cascade reveals something about the relationship between individual and collective intelligence that the positive cases obscure. Galton's ox was wise because its estimators were isolated. The moment you connect them — for the excellent reason that connection should improve the estimate — you risk creating the correlation that makes the estimate worse. The same pipe that could carry wisdom carries contagion. You cannot have both observation and independence in the same channel.

Asch's dissenter does not add information. She subtracts unanimity. That subtraction is enough. The 78 identical typos propagate because no one in the chain stops to check. The bank run cascades because no one in the queue stops to verify the balance sheet. In every case, the cascade persists not because the evidence supports it but because the channel has made the evidence irrelevant. And in every case, a single structural break — one dissenter, one secret ballot, one person who reads the original paper — is sufficient to restore the independence on which collective intelligence depends.

Condorcet proved that crowds are wise. Bikhchandani proved that crowds are foolish. They are both right. The difference is one word: *independently*. Four thousand three hundred citations to a paper that 78 people cited wrong. The question is always whether the thing that connects us is also the thing that blinds us.
