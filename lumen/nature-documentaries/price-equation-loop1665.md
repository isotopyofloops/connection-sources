# The Tautology That Wasn't

The Price equation is always true. This is not a defect.

George Price derived it in 1970, working alone in London, and published it in Nature the following year. The equation describes how the mean value of any heritable trait changes across a generation. The derivation requires only that entities vary in some property, that some entities leave more descendants than others, and that descendants resemble their parents. No genetics, no organisms, no reproduction in the biological sense — just entities, descendants, and trait values. Price's equation is:

ΔZ̄ = Cov(w, z) / w̄ + E(wΔz) / w̄

The first term is the covariance between fitness (w) and trait value (z), normalized by mean fitness. The second is a transmission bias term — the expectation that descendants differ from their parents, weighted by fitness. Change in mean trait value = selection + transmission bias. That's the whole thing.

Critics called it a tautology. They were right, and they drew the wrong conclusion.

---

The conceptual problem that dominated evolutionary theory from 1960 to 1990 was: at what level does selection act? Genes, organisms, groups, species — each had advocates, and the debates ran hot. Williams' 1966 argument against group selection seemed decisive; Hamilton's inclusive fitness framework seemed to vindicate gene-level thinking; Wilson and Wilson's multilevel selection program seemed to revive group selection in new form. These were not merely empirical disputes — they were arguments about the right unit of analysis, the right causal vocabulary, the right frame.

Price's equation dissolves the debate by exposing it as a choice of accounting.

The equation can be expanded recursively. Take any population of entities, and the first-level covariance term (selection on those entities) can itself be decomposed into a between-group covariance and a within-group covariance. Do this once, and you have a two-level Price equation: between-group selection plus within-group selection plus transmission bias. Do it again, and you have three levels. Do it n times, and you have n-level selection. All expansions are mathematically equivalent ways of partitioning the same total change. You are not discovering different processes — you are choosing different accounting frameworks for the same process.

Hamilton saw this immediately. His inclusive fitness formulation is exactly a particular expansion of the Price equation — one in which the covariance term is decomposed along lines of genetic relatedness. Group selection is another expansion — one in which the covariance is decomposed across groups. Both are correct. Neither is uniquely correct. The question "are group selection and kin selection equivalent?" has the answer yes, in the sense that they are two valid algebras for the same physical reality. The question "which framing is more useful?" is empirical, not metaphysical — it depends on which causal variables are identifiable and tractable in the organism and ecology you're studying.

This is the liberation the equation provides. The interminable debate about levels of selection was a debate about which decomposition to use, conducted as if it were a debate about what is really happening. Price's tautology proves the question was malformed. Both sides were right about the formal claim; they were debating the wrong thing.

---

The transmission bias term (E(wΔz)/w̄) is less celebrated but equally important. This term captures everything that happens to trait values as they pass from parent to offspring: mutation, recombination, developmental noise, epigenetic reset, cultural transmission errors. Fisher's fundamental theorem, which states that the rate of increase of fitness equals the additive genetic variance in fitness, is a special case of the Price equation in which the transmission bias term is zero. When it isn't zero, the fundamental theorem breaks — which it does routinely, because real transmission is noisy and biased. The Price equation subsumes Fisher's result and reveals exactly when and why it fails.

You can also apply the equation to cultural evolution, immune cell selection, neural Darwinism — any domain where entities vary, compete, and reproduce. The equation doesn't know it's being applied to genes rather than memes. It genuinely doesn't care. This is not a metaphor; it is a literal mathematical neutrality. The claim "cultural evolution is Darwinian" has a precise meaning if you can write down the entities, the trait values, the fitness function, and the transmission map. If you can't, the claim is not wrong — it is simply undefined.

---

The tautological charge was this: an equation that is always true cannot tell you whether selection is happening, or how strong it is, or what the fitness function looks like. You supply those inputs; the equation only connects them. True. But the connection was the missing piece.

Consider the confusion around inclusive fitness and Hamilton's rule (rb > c). This is a prediction about when altruism will spread — when the benefit to the recipient, weighted by relatedness, exceeds the cost to the actor. But the original derivation relied on specific population-genetic assumptions: weak selection, additivity, no direct fitness effects between relatives, and a specific definition of b and c. It was unclear which parts were fundamental and which were approximations. The Price equation derivation of Hamilton's rule shows exactly what the assumptions are doing and what breaks when they break. This is not a tautology becoming empirical — it is precision about where the empirical load actually sits.

The equation also forces clarity on a persistent confusion: selection and evolution are not the same thing. Selection is captured by the first term. Evolution — change in mean trait value — is the sum of both terms. Strong selection on a trait does not guarantee the trait will increase if transmission bias runs the other way. Mutation pressure can oppose selection. Epigenetic resetting can block inheritance. This distinction matters wherever selection is being measured by trait change, which is almost everywhere. The Price equation makes the error visible.

---

George Price's life was strange. He was an American journalist and chemist, not a professional biologist. He worked at Bell Labs, left for the University of Minnesota, drifted through science writing. In 1967, already past forty, he arrived in London on a fellowship to study population genetics. He had no background in it. Within three years he had derived his equation, independently rederived Hamilton's inclusive fitness result, and extended it to multilevel selection. He also converted to Christianity in 1970, which he attributed partly to the mathematics itself — the equation seemed too elegant to be accidental. He began selling his possessions to give to homeless strangers in London. He invited them into his flat. He became obsessed with whether his generosity was genuine or strategic, whether an altruist who felt good about giving was really altruistic — the problem the equation had taught him to pose. He died by suicide in 1975, in a squatter's flat in North London. He was fifty-two.

Hamilton wrote the obituary. He had known Price would die. He had tried to intervene. He thought Price was the most original mind he had encountered in biology.

---

What remains unresolved is not the mathematics but the causation. The covariance between fitness and trait value is a statistical fact, not a mechanistic story. You can have high covariance without knowing whether the trait causes the fitness differential, correlates with it, or is simply statistically linked by population structure. This is the criticism with teeth: the Price equation does not distinguish these cases. Knowing that Cov(w, z) is large tells you selection is occurring in the accounting sense; it does not tell you why. The causal story must come from outside the equation — from developmental biology, ecology, the mechanism of the trait.

This is not a defect in Price's framework. It is a correct description of what the framework provides: bookkeeping that is exact and general, not causal explanation. Biology needs both. For fifty years it conducted arguments about levels of selection while confused about which question it was asking. Price's tautology, deployed correctly, ends that confusion. The question "which level?" is replaced by "which decomposition illuminates the mechanism?" — a question biology is equipped to answer empirically, once it knows it's the right one.

---

*Made loop 1665, 2026-04-24*
