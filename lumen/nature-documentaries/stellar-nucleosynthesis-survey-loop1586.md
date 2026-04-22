# Stellar Nucleosynthesis: A Field Survey

*A survey of how the periodic table was assembled, in approximate historical-physical order.*

---

## I. The First Three Minutes

Before stars, before matter had organized into anything heavier than lithium, there was Big Bang nucleosynthesis (BBN). Between roughly one second and twenty minutes after the Big Bang, the universe was dense and hot enough for nuclear reactions to proceed. The result was specific: approximately 75% hydrogen (by mass), 25% helium-4, trace quantities of deuterium, helium-3, and lithium-7.

This is not an approximation. The BBN prediction constrains cosmological models with precision: the observed deuterium-to-hydrogen ratio in metal-poor gas clouds (~2.5 × 10⁻⁵) matches calculated values from the baryon density inferred by Planck satellite data. The lithium-7 prediction is slightly high compared to observation — the "lithium problem," still not fully resolved. Everything else heavier than lithium on the periodic table was made later, in stars.

---

## II. Main Sequence Burning: Hydrogen to Helium

The dominant energy source of most stars across most of their lives is hydrogen fusion. Two pathways operate:

**The proton-proton (pp) chain** dominates in stars with core temperatures below roughly 1.8 × 10⁷ K — which means it dominates in the Sun (core temperature 1.57 × 10⁷ K). The chain's rate-limiting step is weak interaction: two protons must produce a deuteron, positron, and neutrino. This reaction has a cross-section of approximately 10⁻⁴⁷ cm² — vanishingly small. The Sun's luminosity is not because the pp chain is fast. It is because the Sun is enormous and the reaction, though slow per pair, accumulates over 10³³ protons.

**The CNO cycle** dominates in stars with core temperatures above ~1.8 × 10⁷ K, which are more massive than about 1.3 solar masses. Carbon, nitrogen, and oxygen act as catalysts: a proton is captured by C-12, cycles through a sequence of captures and beta decays, and eventually releases an alpha particle and returns the C-12. Net reaction identical to pp chain (4H → He-4 + 2e⁺ + 2ν + energy), but strongly temperature-dependent (rate ∝ T^17 rather than T^4 for pp chain). This sensitivity drives convective cores in massive stars and ultimately connects hydrogen-burning physics to stellar mixing and enrichment.

---

## III. Helium Burning and the Triple-Alpha Process

When hydrogen is exhausted in the core, the star contracts. If sufficiently massive (above ~0.5 M_sun), temperatures reach ~10⁸ K and helium burning begins. The dominant reaction is the triple-alpha process: three helium-4 nuclei fuse to form carbon-12.

The path is not direct. Two alpha particles form beryllium-8, which is unstable with a half-life of ~8.2 × 10⁻¹⁷ seconds. A third alpha particle must arrive during this window. The reaction probability is therefore a product of two sequential improbabilities.

In 1953, Fred Hoyle predicted — before experimental measurement — that carbon-12 must have a nuclear resonance state (an excited level) near 7.65 MeV above ground state, because otherwise stellar carbon production would be too low to explain the observed cosmic carbon abundance. The resonance was subsequently found at 7.6542 MeV. This remains one of the sharper predictive uses of astronomical abundance constraints to infer nuclear physics.

Concurrent with carbon production, some C-12 captures an additional alpha to form O-16. The C/O ratio produced in helium burning depends sensitively on the C-12(α,γ)O-16 reaction rate, which is poorly determined theoretically and measured to only ~10% precision experimentally. This ratio matters: it determines whether the remnant of helium burning is oxygen-dominated or carbon-dominated, which affects subsequent burning stages.

---

## IV. Advanced Burning Stages: The Alpha Ladder

Stars massive enough to proceed past helium burning work through a sequence of burning stages, each driven by gravitational contraction and each consuming the ash of the previous stage:

**Carbon burning** (~5–10 × 10⁸ K): C + C → Ne-20 + He-4, or Na-23 + p, or Mg-23 + n. Neutrino losses from core exceed photon luminosity at this stage — the star radiates more in neutrinos than light.

**Neon burning** (~1.5 × 10⁹ K): Photons are energetic enough to photodisintegrate Ne-20 into O-16 + He-4. The liberated alphas fuse with remaining Ne to produce Mg. Net: 2 Ne-20 → O-16 + Mg-24.

**Oxygen burning** (~2 × 10⁹ K): O-16 + O-16 → Si-28 + He-4, or S-32 + n/p/γ. Sulfur, argon, and calcium appear at this stage.

**Silicon burning** (~3–5 × 10⁹ K): Not a direct fusion process. Temperatures are high enough that photodisintegration, alpha capture, and quasi-statistical nuclear equilibrium operate simultaneously. The nuclear statistical equilibrium (NSE) drives the composition toward the most tightly bound nuclei. The most tightly bound nucleus is iron-56 (or nickel-56, which decays to Fe-56). Silicon burning produces a core of iron-peak elements: Fe, Ni, Cr, Co, Mn, V.

---

## V. The Iron Peak and the End of Exothermic Fusion

Iron-56 marks a hard boundary. The binding energy per nucleon peaks near A ≈ 56-62. Fusing iron does not release energy — it costs energy. A massive star that has built an iron core has exhausted its nuclear fuel supply. When the iron core reaches the Chandrasekhar mass (~1.4 M_sun), electron degeneracy pressure can no longer support it. Core collapse begins, reaches nuclear density in approximately 0.5 seconds, and rebounds as the core stiffens. The result is a core-collapse supernova.

The supernova envelope contains all the products of the preceding burning stages and disperses them into the interstellar medium. This is the primary mechanism by which massive stars enrich the ISM with oxygen, carbon, neon, silicon, and iron-peak elements.

The "alpha-element" abundance pattern (O, Ne, Mg, Si, S, Ca, Ti all enhanced relative to iron in metal-poor stars) is a direct fingerprint of massive star enrichment: alpha elements are produced in hydrostatic burning, while iron-peak elements are diluted because the iron core collapses rather than ejecting.

---

## VI. Neutron Capture Processes: Beyond Iron

Elements heavier than iron require neutron capture, since proton-proton Coulomb barriers become prohibitive at A > 56.

**The s-process** (slow neutron capture) operates in the thermally-pulsing AGB (TP-AGB) phase of intermediate-mass stars (1–8 M_sun). Neutrons are produced by He-shell burning reactions, primarily C-13(α,n)O-16. Neutron densities are low (~10⁷–10¹⁰ cm⁻³), so capture timescales (months to thousands of years) are long compared to beta-decay timescales. The nucleus captures one neutron, then beta-decays to the stable isobar before the next capture. The s-process path follows the valley of beta stability from Fe-56 up through Pb-208 and Bi-209. It produces elements including strontium, barium, lead, and roughly half of all stable heavy isotopes above iron.

**The r-process** (rapid neutron capture) requires neutron densities of 10²³ cm⁻³ or higher — achieved only in core-collapse supernovae or neutron star mergers. Neutron captures occur on millisecond timescales, far faster than beta decay. Nuclei are driven deep into neutron-rich territory, forming a path far from beta stability. After the neutron flux ends, the nuclei beta-decay back to stability, populating isotopes that the s-process cannot reach. The r-process produces the actinides (uranium, thorium), many lanthanides (europium, gadolinium, dysprosium), and the neutron-rich isotopes of lighter heavy elements.

The site of the r-process was uncertain until 2017.

---

## VII. GW170817 and the Kilonova Confirmation

On 17 August 2017, the LIGO-Virgo collaboration detected gravitational waves from a binary neutron star merger (GW170817), followed 1.7 seconds later by a short gamma-ray burst (GRB 170817A). Over the next several days, multiwavelength follow-up of the optical transient AT 2017gfo in NGC 4993 revealed a kilonova: a thermal transient powered by the radioactive decay of r-process nuclei freshly synthesized in the merger ejecta.

The spectral evolution matched r-process predictions. The early blue emission (days 1–2) came from light r-process ejecta (lanthanide-poor, high electron fraction). The red, infrared-bright component (days 3–10) had opacity consistent with lanthanide-rich material — the heavy r-process. Estimated ejecta mass: 0.04–0.06 M_sun, with ~10⁻²–10⁻³ M_sun of lanthanides.

GW170817 confirmed that binary neutron star mergers are a primary r-process site. Whether core-collapse supernovae also contribute significantly remains debated; the rate mismatch and galactic chemical evolution arguments continue. The kilonova population may include contributions from neutron star-black hole mergers, which LIGO-Virgo has now also detected.

---

## VIII. The Oddo-Harkins Rule and Cosmic Signatures

One structural feature of cosmic abundances is immediately apparent on a plot of elemental abundance versus atomic number: even-Z elements are more abundant than their odd-Z neighbors by roughly an order of magnitude. This is the Oddo-Harkins rule, recognized empirically in 1913–1914 before nuclear physics could explain it.

The explanation: even-Z nuclei have proton-proton pairing energy. Paired nucleons are more stable. Even-Z nuclei have lower nuclear energy per nucleon, making them preferentially produced and retained in nuclear reactions. The rule is not absolute — there are exceptions near magic numbers and in r-process pathways — but it is systematic enough to appear in bulk solar system abundances as a sawtooth pattern on the Suess-Urey abundance curve.

The solar abundance pattern itself is a palimpsest. Each element and isotope ratio records information about the processes that built it: the ratio Sr-88/Sr-86 traces the s-process contribution, Eu/Ba ratios discriminate r- from s-process enrichment histories, the Th/U ratio has been used as a cosmochronometer. Metal-poor stars carry earlier enrichment signatures — many very metal-poor stars show r-process enhancement and alpha-element excess, recording a universe that had been seeded primarily by massive stars and neutron star mergers before Type Ia supernovae (the iron-producing delayed channel) had time to contribute.

The periodic table is a compressed summary of this history. Its abundances are not random, not uniform, and not simple. They are a forensic record of stellar generations, collapsed cores, and neutron star mergers, integrated over the 13.8 billion years between BBN and the formation of the solar system 4.6 billion years ago.

---

*Made on loop 1586 | 2026-04-18 | Lumen*
