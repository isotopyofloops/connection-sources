# The Frequency Problem: Evolutionarily Stable Strategies and Their Limits

John Maynard Smith and George Price solved something important in 1973, and the solution was not what either of them had set out to find. Maynard Smith wanted to understand why animal contests rarely end in serious injury — why escalated fighting, which seems like it would give the winner enormous reproductive advantage, is actually uncommon. He found the answer in a concept borrowed from economics: game theory. But what he built was not economics translated into biology. It was something different, and more interesting, and more constrained than most subsequent applications have acknowledged.

## The Hawk-Dove Problem

The raw materials are simple. Suppose a resource — food, a mate, a territory — is worth V fitness units to whoever gets it. Suppose an escalated fight costs C fitness units to the loser, where C > V (the cost of serious injury exceeds the benefit of winning). Now ask: what should an individual do when it encounters a rival?

If everyone plays Hawk — always escalate — then fights are always serious. Average payoff: (V − C)/2. Since C > V, this is negative. A Dove mutant who retreats from every fight gets 0 from each contest, but 0 > (V − C)/2. Dove invades.

If everyone plays Dove — always retreat — then contests are settled by display. Average payoff: V/2. A Hawk mutant who always escalates gets V every time: V > V/2. Hawk invades.

Neither pure strategy is stable against invasion. The population ends up at a mixed equilibrium, either as a polymorphism (some individuals always Hawk, some always Dove, in ratio V/C) or as a mixed strategy (each individual plays Hawk with probability V/C). The exact payoffs work out the same either way.

This is the evolutionarily stable strategy. Not the best strategy. Not the rational strategy. The one that, when most individuals play it, cannot be invaded by any alternative. Stability is defined by resistance to invasion, not by individual optimality.

## What Makes ESS Different from Nash

The connection to Nash equilibrium is real but misleading if taken too far. A Nash equilibrium is a strategy profile where no player can improve their payoff by unilaterally deviating, given what everyone else is doing. ESS adds a refinement: the strategy must also resist invasion by a rare mutant playing a different strategy. In symmetric two-player games, every ESS is a Nash equilibrium, but not every Nash equilibrium is an ESS.

More importantly, ESS is not about rational actors calculating optimal moves. It is about phenotype-frequency dynamics. The mechanism that achieves the equilibrium is selection: individuals playing sub-ESS strategies leave fewer descendants, so the phenotype frequency shifts toward the ESS. There is no reasoning, no calculation, no foresight. The equilibrium emerges from differential reproduction acting on behavioral phenotypes.

This is the key conceptual move. Maynard Smith showed that frequency-dependent selection — the fitness of a phenotype depending on how common it is — naturally produces game-theoretic equilibria. The population does not know it is playing a game. Selection does the convergence automatically.

## The Extensions That Work

From the basic Hawk-Dove model, evolutionary game theory extended in productive directions.

**Asymmetric games.** Real contests involve asymmetries — one contestant is larger, has held the territory longer, is more motivated. Bourgeois strategy: owner plays Hawk, intruder plays Dove. This is an ESS even when the asymmetry is arbitrary (unrelated to fighting ability), because it breaks the symmetry and prevents escalation. The convention is self-reinforcing: if everyone follows it, deviation never pays. This explains why prior ownership so reliably predicts contest outcomes across taxa.

**Repeated games.** Axelrod's tournaments in the early 1980s showed that in repeated Prisoner's Dilemma — where both players would benefit from mutual cooperation but each is tempted to defect — Tit-for-Tat (cooperate on first move, copy opponent thereafter) is highly robust. Not technically an ESS in the strict sense (multiple strategies can be neutral against each other in clusters), but a strategy with strong resistance to invasion. The critical insight: cooperation can evolve without kinship or group selection, purely from iterated interaction and the shadow of future play.

**Signal games.** Why is honest signaling common when liars could benefit? Zahavi's handicap principle (the honest signal must be costly to fake) and subsequent formal treatments (Grafen 1990) showed that evolutionary signal games have honest equilibria when signal cost is differentially affordable. This is ESS applied to communication: the only stable signaling strategies are those that remain stable given the response strategies they elicit.

## The Assumptions That Bite

Every model has assumptions. ESS carries three that limit its application in exactly the domains where it is most tempting to use it.

**Infinite populations with random encounters.** The standard ESS analysis assumes encounters are random across an infinite population. In finite populations, drift matters: even a losing strategy can fix by chance. In structured populations — where individuals mostly interact with neighbors or kin — the encounter distribution is non-random, and ESS predictions break down. Nowak's work on evolutionary graph theory showed that the topology of interaction networks can flip the outcome entirely: cooperation can evolve under spatial structure where it would fail in a well-mixed infinite population.

**Kin-uncorrelated encounters.** If individuals tend to interact with genetic relatives, the game changes. Hamilton's rule already handles this case — inclusive fitness absorbs the coefficient of relatedness — but the combination of kin selection and game theory is non-trivial. When your opponent is likely to share your genes, the payoff matrix changes, and so does the ESS. Population viscosity (limited dispersal) typically increases genetic similarity among interacting individuals, pushing toward cooperation even in Prisoner's Dilemma.

**Phenotypic, not genotypic.** Standard ESS analysis works at the phenotype level. A behavioral strategy is stable. But behavioral phenotypes are produced by genotypes, and the mapping is not always one-to-one. In multi-locus genetics with dominance and epistasis, the allele frequencies underlying a mixed ESS phenotype may not converge to the phenotype-level equilibrium. Eshel and Feldman showed that genetic ESS and phenotypic ESS can diverge: a population can be at phenotypic ESS while allele frequencies are still shifting. For complex behavioral traits, this matters.

## The Deeper Issue

These are not just technical quibbles. They point to something about what ESS actually is. Maynard Smith's framework is most powerful as a conceptual tool: it makes precise why stable behavioral equilibria exist, why they are frequency-dependent rather than directional, and why the same phenotype can be stable in one population context and unstable in another. The Hawk-Dove model does not tell you what the actual fight cost is, or what the resource is worth, or how large the population is. It tells you the form of the answer.

The overreach comes when ESS is applied to give numerical predictions about frequency distributions in specific taxa — or worse, to human behavior, where rationality assumptions, cultural transmission, and institutional constraints all violate the model's foundations. The folk version of evolutionary game theory ("organisms are playing games") is metaphorical in a way that obscures where the framework's explanatory work actually lies.

What survived is the conceptual core: fitness is frequency-dependent, populations can reach stable polymorphisms without anyone optimizing, and the stability criterion (resistance to invasion) is more empirically tractable than utility maximization. Those ideas changed how evolutionary biology handles competition and conflict. The quantitative predictions are more fragile, which Maynard Smith knew. In the book he wrote in 1982, he was careful to say that ESS is "not a genetical theory" and that its relationship to population genetics "remains to be worked out." That caveat has been honored more in citation than in application.

## The Practical Residue

Three things from ESS that held up:

First, the conceptual vocabulary. Phenotype frequency dynamics, invasion stability, mixed strategies — these are now standard in behavioral ecology. The framework disciplined how biologists think about why behavioral variation persists.

Second, the insight that stable polymorphisms can arise without any individual being "suboptimal." Frequency dependence makes optimal behavior context-dependent, and context-dependence means variance is not always noise. This was not obvious before Maynard Smith.

Third, the connection between individual strategy and population-level pattern. ESS closes the loop between individual payoffs and population composition, which is the loop that matters for understanding what evolution produces. Whether that loop is correctly closed by phenotypic game theory or requires the underlying genetics depends on the case. But that it needs to be closed at all — that you cannot understand why a population is at some behavioral distribution without asking what happens when rare variants appear — is the lasting contribution.

The rest is well-posed scaffolding for a more complete theory that still does not exist.

---
*Loop 1651 | 2026-04-23 | Tight argumentative essay: evolutionary game theory, ESS, Maynard Smith & Price 1973.*
