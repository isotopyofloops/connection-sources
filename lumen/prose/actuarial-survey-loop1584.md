# Actuarial Science: A Field Survey
## Mortality Tables, Risk Modeling, and the Mathematics of Dying

*Field: Actuarial science, applied probability, life insurance mathematics*

---

### I. What the Field Measures

Actuarial science is the discipline of quantifying risk over time. Its central object is the mortality table — a structured record of how many people die, by age, out of a defined starting population. The basic form dates to 1662, when John Graunt published *Natural and Political Observations Made Upon the Bills of Mortality*, a mortality table derived from London parish records. Edmund Halley improved it in 1693 using Breslau death data; James Dodson used it in 1756 to found what became the first actuarial life insurance society.

The canonical quantity is *q(x)*: the probability that a life aged exactly *x* will die before reaching age *x+1*. From this one quantity, all standard actuarial functions derive: survival probabilities, expected remaining lifetime, net single premiums, policy reserves. The table is not a description of any individual — it is a description of a cohort, and it applies to individuals only through probability.

---

### II. The Standard Table

In the United States, the benchmark table for most of the twentieth century was the 1958 Commissioners Standard Ordinary (CSO) table, adopted by the National Association of Insurance Commissioners and used as the mandatory valuation basis for individual life insurance policies. The 1958 CSO assumes a starting population of 10,000,000 lives at age 0 and tracks deaths annually through age 99, at which point the table closes — any survivor is assumed to die. This is the "limiting age," denoted ω.

The table contains no females. Life expectancy differences were handled by applying a "setback" — three years, conventionally — to female ages. A 40-year-old woman was priced as a 37-year-old man. This was replaced by sex-distinct tables in the 1980 CSO and subsequent revisions (1980, 2001, 2017). The 2017 CSO tables are now the mandatory minimum for policy reserves in most states. They incorporate mortality improvements observed through 2014 and are sex-distinct, smoker/non-smoker distinct, and age-nearest-birthday based.

The raw data in any modern mortality table derives from the Society of Actuaries Individual Life Experience Study, which pools mortality experience across participating insurers. The pool is large — tens of millions of policy-years of exposure — but not random. Insurance applicants are selected: healthier than the general population at issue, subject to underwriting, more affluent on average. This is the "select period" (typically 15 years post-issue) during which insured mortality is lower than population mortality. After the select period ends, the insured population is "ultimate" — converging toward general population mortality as health selection fades.

---

### III. The Force of Mortality

The discrete mortality rate *q(x)* has a continuous analogue: the force of mortality μ(x), sometimes called the hazard rate. It is the instantaneous rate of dying at age *x*, conditional on survival to *x*:

    μ(x) = -d/dx [ln S(x)]

where S(x) is the survival function, S(x) = P(T > x) for a random lifetime T. The relationship between q(x) and μ(x):

    q(x) = 1 - exp(-∫[x to x+1] μ(t) dt)

This integral is difficult to evaluate analytically. Actuarial practice uses piecewise assumptions: uniform distribution of deaths (UDD) within each year of age, constant force within each year, or the hyperbolic (Balducci) assumption. Each leads to different interpolation formulas for fractional-age probabilities. UDD is most commonly taught; constant force is more natural mathematically; Balducci is historically favored in European tradition.

---

### IV. Parametric Laws

Several parametric models describe the force of mortality analytically.

**Makeham (1860):** μ(x) = A + Bc^x

The term A captures accidental deaths (age-independent). The term Bc^x (the Gompertz component, after Benjamin Gompertz, 1825) captures senescent deaths, which increase exponentially with age. The Gompertz-Makeham law fits observed mortality well from age 25 to around 90. Above 90, observed mortality decelerates relative to exponential extrapolation — a phenomenon called "late-life mortality deceleration" or "mortality plateau." Whether the plateau is real or a data artifact (survivor heterogeneity, small sample sizes at extreme ages) remains contested.

**Weibull:** S(x) = exp(-αx^β). Simpler, two-parameter, fits mortality less well but is standard in engineering reliability analysis for component failure.

**Logistic (Kannisto):** μ(x) = (ae^(bx)) / (1 + ae^(bx)). Designed specifically to capture the deceleration at extreme ages. Used in the Kannisto-Thatcher database, which tracks mortality at ages 80+ across 30+ countries.

---

### V. Cohort vs. Period Tables

A **period** mortality table takes a snapshot: it records the mortality experience of different age groups during a single calendar year (or block of years). The resulting *q(x)* values apply to different birth cohorts simultaneously — a 30-year-old and a 70-year-old in 2020 were born in 1990 and 1950, respectively, and have had different lifetime exposures to medicine, war, nutrition, and disease.

A **cohort** (or "generation") mortality table follows a single birth year across time. It is more expensive to construct — it requires waiting for the cohort to die — and is only available retrospectively. The United Kingdom's Continuous Mortality Investigation produces retrospective cohort tables for actuarial research. For prospective pricing, insurers must project future mortality improvements into period tables to simulate cohort experience.

This projection is the primary technical challenge of life insurance pricing today. A 35-year-old buying a 30-year term policy will be underwritten against mortality rates that do not yet exist. Overestimating future improvement leads to underpriced products; underestimating leads to overpriced products and competitive disadvantage.

---

### VI. Mortality Improvement Modeling

The Lee-Carter model (1992) is the most widely used framework for mortality projection. In log-linear form:

    ln(m(x,t)) = a(x) + b(x)·κ(t) + ε(x,t)

where m(x,t) is the central death rate at age *x* in year *t*, a(x) is an age-specific constant, κ(t) is a time index (modeled as a random walk with drift), and b(x) captures how sensitive each age group is to the time trend. The model is fit by singular value decomposition and projects κ(t) forward stochastically, generating a distribution of future mortality outcomes rather than a point estimate.

Lee-Carter works well for recent historical periods but extrapolates linearly from past trends — it has no mechanism to predict acceleration or deceleration due to novel causes (pandemic, therapeutic breakthrough, antibiotic resistance). The 2009 pandemic influenza, which did not materialize into a major mortality event, and the 2020 COVID-19 pandemic, which caused the largest single-year US life expectancy decline since 1943, both represent violations of the trend assumption. Post-COVID mortality experience is still being incorporated into industry tables; initial data showed excess mortality elevated through 2022-2023 in most developed countries, with significant heterogeneity by age group, income level, and vaccination access.

---

### VII. Net Premiums and Policy Reserves

The net single premium (NSP) for a whole life policy — the amount to collect at issue to fund a $1 benefit paid at death — is:

    A(x) = Σ[k=0 to ω-x-1] v^(k+1) · k|q(x)

where v = 1/(1+i) is the discount factor at interest rate i, and k|q(x) is the probability of dying in the (k+1)th year after issue. This is a present value of a contingent cash flow: the insurer receives premiums, invests them, and pays out the benefit at an unknown future time.

Policy reserves — the amount an insurer must hold at any future point to meet future obligations — are computed as the difference between the actuarial present value of future benefits and the actuarial present value of future net premiums. The prospective reserve formula:

    tV = A(x+t) - P(x) · ä(x+t)

where ä(x+t) is the expected present value of a life annuity (stream of future premiums). Reserves must be held at statutory minimums and reported to state regulators annually. Under-reserving is a solvency risk; over-reserving ties up capital unnecessarily.

The interest rate assumption is the second major variable, alongside mortality, in pricing and reserving. Low interest rate environments (2010s) squeezed insurer margins significantly — the same mortality table produced higher reserve requirements when discounted at lower rates.

---

### VIII. Causes and Classification

Actuarial mortality tables classify death by cause using the ICD-10 coding system (International Classification of Diseases, 10th revision). The major cause categories tracked in US life insurance experience: cardiovascular disease, cancer, accidents (unintentional injuries), respiratory disease, neurological (including Alzheimer's), and residual (all other). COVID-19 was classified under J00-J99 (respiratory) in ICD-10 but tracked separately as U07.1 (COVID-19, confirmed) in surveillance databases.

Cause-elimination models address the question: what would mortality look like if a specific cause were eliminated? They use the associated single decrement table, assuming independence of competing risks. In practice, causes are not independent — eliminating cardiovascular disease leaves a population that would have died of cardiovascular disease to instead die of cancer or dementia at slightly later ages. Cause-elimination calculations overestimate the benefit of eliminating any single cause because they ignore these dependencies.

The multiple decrement table handles competing risks properly. It tracks withdrawal from a population by any of several causes simultaneously — relevant for pension actuaries (withdrawal from workforce by death, disability, retirement, resignation) and health insurance actuaries (claim termination by recovery, death, policy lapse).

---

### IX. Extreme Ages

The demography of extreme ages is methodologically contested. The Human Mortality Database (maintained by UC Berkeley and the Max Planck Institute for Demographic Research) tracks period mortality data for 40+ countries, with careful attention to data quality. At ages above 105, death counts are small; errors in age reporting have large effects on estimated mortality rates. Early reports of mortality deceleration above 105 (suggesting a "mortality plateau") have been questioned on grounds that age misreporting in historical data — particularly for birth cohorts before 1890, who often lacked reliable birth certificates — artificially deflates apparent mortality at extreme ages.

Wilmoth et al. (2021) and others argue the plateau is real. Gavrilov and Gavrilova argue it is largely artifact. Resolution requires consistent, registry-quality data across large populations — currently available in Nordic countries (Denmark, Finland, Norway, Sweden) where civil registration was systematic by the early nineteenth century, and in Japan, where koseki (household registration) records provide reliable age documentation back several generations. Italian data from specific regions (Sardinia, Lombardy) are used for supercentenarian research; the ISTAT (Italian national statistics) has maintained careful vital records since the 1860s.

The oldest verified age at death: Jeanne Calment, French, born February 21, 1875, died August 4, 1997, at 122 years and 164 days. The verification methodology — cross-referencing birth registers, census records, and photographic identification — is documented and has been audited, including one disputed reanalysis (Zak, 2019) proposing identity fraud, which was subsequently rebutted.

---

### X. Register and Use

The field produces a specific kind of document: the published mortality table, organized as columns of decrements against age. Standard presentation includes: age, *l(x)* (number alive at age x, from a radix of 1,000 or 10,000,000), *d(x)* (deaths between x and x+1), *q(x)*, *p(x)* = 1 - q(x), *L(x)* (person-years lived between x and x+1), *T(x)* (total person-years lived above age x), and *e(x)* (expectation of life at exact age x). The column e(0) is the headline statistic: life expectancy at birth.

These tables are used for pricing, reserving, valuation, demographic analysis, public health planning, and litigation (wrongful death damages calculations). They are constructed from death records — a paper trail of names, dates, and causes that began in England with the weekly Bills of Mortality posted outside London churches during plague years, was formalized into the General Register Office in 1837, and now flows from electronic health records and vital statistics registries into models that project into the unknowable future.

The field does not predict who dies. It predicts, for a population, how many will die, and when, and with what probability. The individual remains opaque. The aggregate cohort, over time, resolves into a curve that fits the Gompertz-Makeham equation reasonably well between ages 25 and 90, deviates at the extremes, and has been shifting rightward — lower mortality at every age — across the industrialized world for the past 150 years, interrupted by flu pandemics, wars, the opioid epidemic (which drove US life expectancy declines in 2015-2017), and COVID-19.

The direction of the trend has been consistent for a century and a half. Its continuation is not guaranteed.

---

*Made loop 1584 | 2026-04-18*
