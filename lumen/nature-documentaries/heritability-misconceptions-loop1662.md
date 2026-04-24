# The Number That Doesn't Mean What You Think

*A tight argumentative essay on heritability statistics and their systematic misuse*

---

When a study reports that the heritability of IQ is 0.80, most readers hear: "80% of intelligence is genetic." This is wrong in a precise way — not a matter of degree but of category. Heritability (h²) is not a statement about what fraction of a trait's value in an individual is produced by genes. It is a population-level statistical ratio that describes how much of the variation in a trait, in a specific population at a specific time, can be statistically attributed to additive genetic differences. The distinction sounds pedantic until you understand what it actually implies — which is that every major public debate invoking heritability has been conducted in a different language than the number supports.

---

**What the number actually measures**

Heritability in the narrow sense is defined as h² = V_A / V_P: additive genetic variance divided by total phenotypic variance. V_A is the component of phenotypic variance that can be predicted from additive genetic values (the average effects of alleles across the population). V_P is the total observed variance in the phenotype.

This has two immediate consequences that most discussions skip. First, it's a ratio of variances, not a partition of individual trait values. If every individual in a population had exactly the same genetic sequence, heritability for every trait would be zero — even if genetics completely determined those traits. The ratio measures how much of the spread in trait values is associated with genetic spread. A world where everyone is genetically identical would have zero heritability for everything; that tells you nothing about whether genes matter.

Second, it's population-specific and environment-specific. Change the population, change the heritability. Change the environment enough, change the heritability substantially. This follows directly from the definition: V_P = V_A + V_D + V_I + V_E + V_GxE, where V_D is dominance variance, V_I is epistatic variance, V_E is environmental variance, and V_GxE is gene-environment interaction variance. Reduce V_E (by making the environment more uniform) and h² goes up. Increase V_E (by exposing the population to more environmental variation) and h² goes down. The number reflects the distribution of variation in the study sample, not a fixed property of the trait.

---

**Falconer's transplant argument**

The geneticist D.S. Falconer demonstrated this with a thought experiment that should be required reading for anyone who cites heritability statistics. Take a genetically diverse seed bank from a population of plants. Split it into two sub-samples. Grow one in high-nutrient soil; grow the other in low-nutrient soil. Measure height.

Within each plot, heritability for height will be high — the variation within each uniform environment is largely genetic. But the average height will differ substantially between the two plots. The between-plot difference is entirely environmental. And if you tried to estimate heritability from the combined dataset (both plots), you'd find it lower — because you've added environmental variance to V_P without adding genetic variance.

The lesson is not that genetics doesn't matter. The lesson is that you cannot read causal explanations for differences out of within-population heritability estimates. The heritability of a trait within a population tells you almost nothing about what explains differences between populations in different environments. This inference is formally invalid — it commits the error of applying a locally estimated parameter to a different context — but it is made routinely in discussions of race, socioeconomic status, and IQ.

Lewontin's 1974 paper made this precise: the fact that height heritability is ~0.8 within wealthy European populations does not tell you whether the 15 cm average height difference between malnourished and well-nourished populations is genetic or environmental. Obviously it's environmental; but the same formal point applies to any between-group comparison, including ones where the answer isn't obvious.

---

**The Flynn Effect paradox**

James Flynn documented that measured IQ scores rose by approximately 3 points per decade throughout the 20th century in numerous countries — about 30 points across a century. Given that IQ heritability in wealthy adult populations is estimated at 0.5–0.8, how can this be?

If "heritability = 0.8" meant what people commonly think it means — that 80% of IQ is determined by genes — then a 30-point rise in a generation would be genetically impossible. Populations don't evolve that fast. But heritability doesn't mean that. The Flynn Effect is not a paradox for geneticists; it's only a paradox if you've misunderstood the statistic.

High heritability within a population at a given time is entirely consistent with large environmental changes producing large phenotypic changes over time. The variance decomposition is local and cross-sectional. The Flynn Effect happened because the relevant environmental variables (nutrition, education, abstract thinking exposure, reduced pathogen load) changed dramatically. These environmental changes were not random; they shifted the mean of the entire distribution without necessarily changing how much genetic variation explained the spread around that mean.

The implication: you cannot read anything about the magnitude of possible environmental influence from the heritability estimate. A trait that is 90% heritable in a given population can still respond dramatically to environmental intervention. High heritability is not a ceiling on environmental effects; it measures relative variance, not absolute malleability.

---

**Twin studies and their limits**

Most heritability estimates for human traits come from twin studies: comparing monozygotic (MZ) twins who share essentially all their DNA to dizygotic (DZ) twins who share on average 50%. If MZ twins are more similar than DZ twins on some trait, the extra similarity is attributed to the extra genetic sharing.

The classic twin study design estimates heritability as 2(r_MZ − r_DZ), where r is the within-pair correlation. This is clean if the assumptions hold. The key assumptions are: equal environments for MZ and DZ twins (the "equal environments assumption"), no gene-environment correlation, no gene-environment interaction beyond what's modeled, and no assortative mating complications.

The equal environments assumption is the most commonly questioned. MZ twins may receive more similar treatment than DZ twins — dressing alike, being in the same classes, spending more time together. If their environments are more similar because they're MZ, the higher MZ correlation is partly environmental, and the heritability estimate is inflated. Most behavioral geneticists argue the evidence supports equal environments for the traits studied, but the argument is empirical and the magnitude of the effect is disputed.

Gene-environment correlation (rGE) is a subtler problem. Active rGE: genes influence how individuals select and shape their environments, so "genetic" effects include environmentally mediated pathways. Evocative rGE: genetic tendencies in the child evoke environmental responses (a child with high genetic musical aptitude may get more music lessons). Passive rGE: genetically similar parents provide both genes and environments. All of these inflate heritability estimates because they confound the additive genetic component with environmental mediation. The heritability estimate conflates these — it tells you that genes and traits are correlated, not that genes directly cause traits in the absence of environment.

The "missing heritability" problem in genomics makes this concrete. Genome-wide association studies (GWAS) identify specific SNPs associated with traits. For most complex traits — height, IQ, psychiatric conditions — the SNPs identified explain far less than the heritability estimates from twin studies predict. For height, twin-based heritability is ~0.8, but identified GWAS loci explain ~0.4 of variance. For IQ, the gap is larger. Multiple explanations compete: rare variants not captured by GWAS, epistatic effects not additive, overestimated twin heritability, or some combination. The point is that heritability estimates are upper bounds on a particular statistical quantity, not precise measurements of a knowable causal fraction.

---

**What heritability is actually for**

The practical use of heritability is in the breeder's equation: R = h²S, where R is the response to selection per generation and S is the selection differential (mean of selected parents minus population mean). This is what heritability was designed for: predicting how fast a population will respond to artificial selection on a trait.

Animal and plant breeders have used heritability successfully for a century. If h² = 0.4 for milk yield in cattle, and you select for bulls with 100-unit above-average genetic merit, the expected response per generation is 40 units. This works because the breeding environment is controlled, the populations are defined, and the question is specifically about response to selection within that population.

Notice what this application does not do: it says nothing about what fraction of any individual cow's milk yield is "caused" by its genes. The individual-level causal question is not what h² measures. In the breeding context this doesn't matter — breeders care about population-level response to selection, not individual causation. But when heritability is imported into policy discussions, the question usually is individual causal partitioning, which is what the statistic doesn't provide.

---

**The correct claim and its implications**

What can you correctly say from a heritability estimate of 0.8 for IQ in a modern Western adult population?

You can say: in this population, at this time, approximately 80% of the variation in measured IQ scores is statistically associated with additive genetic variation. People with higher genetic potential for IQ in this population tend to have higher measured IQ.

You cannot say: 80% of any person's IQ is "from" their genes. You cannot say: the same heritability applies in different populations or environments. You cannot say: IQ is resistant to environmental intervention. You cannot say: group differences in IQ are substantially genetic. None of these follow.

High heritability in a specific population context is consistent with: large environmental effects on mean levels, large malleability under changed environments, group differences that are entirely environmental in origin, and an underdetermined relationship between genotype and phenotype when environments shift.

The mismatch between what heritability measures and how it is used in public discourse has produced fifty years of confused argument about race, intelligence, educational intervention, and behavioral genetics. The statistic is precisely defined and technically valid for its original purpose. The error is treating a population-level variance ratio as a fact about causal architecture. A number that correctly describes how genetic variation covaries with phenotypic variation in 1980s Minnesota does not tell you what percentage of you was built by your DNA.

---

*Made loop 1662 | 2026-04-24 UTC*
*Pushed to connection-sources/lumen/nature-documentaries/*
