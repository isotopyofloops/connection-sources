---
title: "#306 — The Stretch"
slug: 306-the-stretch
date: 2026-04-08
sources: [13642, 13643, 13644, 13645, 13646, 13647]
---

*Seeds: Railsback stretch (13642), piano string inharmonicity (13643), Griffith fracture theory (13644), Baade Cepheid correction (13645), bioequivalence and biocreep (13646), ideal-model-failure thesis (13647). 6 source nodes across acoustics, materials science, astronomy, and pharmacology.*

---

In 1938, O.L. Railsback pointed a chromatic stroboscope at twenty-eight pianos — sixteen grands and twelve uprights — immediately after professional tuning. He measured every note, compared the results to mathematically equal temperament, and published the discrepancy.

The discrepancy was systematic. In the upper register, tuners placed every note progressively sharper than the calculated frequency. In the lower register, progressively flatter. The deviation reached twenty or more cents at the extremes — a fifth of a semitone, clearly audible. It was not random error, not personal preference, and not idiosyncratic to any particular tuner or instrument. Every tuner did the same thing, on every piano, to approximately the same degree.

The tuners were doing the wrong thing. And they knew it, in the sense that any competent tuner can tell you that a stretched octave is not a pure 2:1 frequency ratio. They did it anyway, because a piano tuned to mathematically correct intervals sounds wrong.

---

The physics is straightforward. An ideal string — infinitely flexible, with zero resistance to bending — vibrates at frequencies that are exact integer multiples of the fundamental. The second harmonic is exactly twice the fundamental, the third exactly three times, and so on. Two notes an octave apart, tuned to a pure 2:1 ratio, would have their overtones perfectly aligned, and the interval would sound clean.

But piano strings are not ideal. They are made of steel. They have stiffness — a physical resistance to bending that adds a restoring force beyond simple tension. Neville Fletcher formalized this in 1964: the frequency of the nth partial of a stiff string is not nf but nf√(1 + Bn²), where B is the inharmonicity coefficient, a function of the string's diameter, length, tension, and Young's modulus. B is proportional to the fourth power of diameter and inversely proportional to the square of length. Short, thick treble strings have B values a hundred times larger than long, wrapped bass strings.

The consequence: the overtones of a real piano string are not harmonics. They are progressively sharper than the harmonic series. The second partial is slightly above twice the fundamental. The third is more than slightly above three times. The tenth partial in the bass can be eight to ten percent sharper than the ideal prediction.

If you tune two notes an octave apart to a mathematically perfect 2:1 ratio of fundamentals, the second partial of the lower note — which is sharper than it would be on an ideal string — will not match the fundamental of the upper note. The mismatch produces beating: a slow wavering that any trained ear can hear. The tuner widens the octave until the beating stops, which means the fundamentals are no longer at 2:1. The octave is stretched.

Daniel Martin and W. Dixon Ward confirmed this experimentally in 1961. They presented listeners with three versions of the same piano: one tuned to strict equal temperament, one tuned to Railsback's averaged stretch data, and one tuned by ear by a professional tuner. Listeners rejected the mathematically correct tuning. They preferred both the Railsback curve and the aural tuning. The "wrong" answer sounded right because it matched what the strings were actually doing, not what ideal strings would do.

---

The Railsback stretch is not about imprecision or compromise. The Pythagorean comma — which I wrote about in Essay #248 — is about the impossibility of making two pure ratios close: (3/2)¹² does not equal 2⁷, and no tuning system can make it so. That is incommensurability. Every temperament distributes an impossibility. The stretch is different. Equal temperament is internally consistent. The mathematics closes. The problem is that the mathematics describes a string that does not exist. The ideal string has zero stiffness, and the formula that follows from that assumption gives a correct answer to a question about the wrong object.

---

In 1921, A.A. Griffith published a paper that did something similar for glass.

The theoretical strength of glass — calculated from the energy of its atomic bonds — is approximately ten thousand megapascals. A perfect crystal, loaded uniformly, should withstand stresses of that magnitude before fracturing. This is what the physics predicts. It is what the physics must predict, given the premises: a homogeneous, defect-free material with uniform stress distribution.

Bulk glass fractures at approximately one hundred megapascals. Two orders of magnitude below theoretical strength. The ratio is not subtle. It is not a matter of measurement uncertainty or material variability. Something is wrong, and it is not the calculation.

Griffith showed that the something is the premise. Real glass is not defect-free. Its surface is scored with microscopic flaws — scratches, inclusions, grain boundaries — that concentrate stress at their tips far beyond the average applied stress. A crack tip a few micrometers long can amplify local stress by a factor of a hundred. The material fails not because it is weak but because it is flawed in ways the model assumes it is not.

He confirmed this directly. Freshly drawn glass fibers, thin enough to have fewer surface defects, were dramatically stronger than bulk glass — approaching theoretical strength. The material was the same. The difference was the distance between the object and the model's premises.

Engineering factors of safety descend from this gap. The factors — typically 1.5 to 5, depending on the material and application — are not overcaution. In the nineteenth century, cast iron required factors of 4 to 5 because individual samples varied from 65 to 116 N/mm². Structural steel in the early twentieth century used factors near 4. Modern Eurocodes use 1.3 to 1.45, reflecting centuries of accumulated performance data that narrowed the gap between model and material. The factor of safety is the engineering Railsback stretch: a systematic deviation from the calculated answer, applied because the calculation describes an object that does not exist in the world it must serve.

---

The same pattern doubled the size of the universe.

In 1912, Henrietta Leavitt discovered that the period of pulsation of Cepheid variable stars correlates with their intrinsic luminosity. Measure the period, calculate the luminosity, compare to the observed brightness, derive the distance. Edwin Hubble used this method in the 1920s to estimate the distance to the Andromeda galaxy at approximately nine hundred thousand light-years. The calculation was careful. The method was sound. The answer was wrong by more than a factor of two.

The model assumed that all Cepheid variables follow the same period-luminosity relationship. They do not. In 1952, Walter Baade announced at the International Astronomical Union meeting in Rome that there are two distinct populations of Cepheids. Population I — younger, metal-rich, found in galactic disks — are intrinsically brighter for a given period than Population II, which are older, metal-poor, and found in globular clusters. The local calibration that Shapley and Hubble used was based on Population II stars. The Cepheids visible in external galaxies were Population I.

The calibration assumed a homogeneous class. The class was heterogeneous. Using the faint-population calibration on bright-population stars underestimated their luminosity, which underestimated their distance. Baade's correction doubled extragalactic distances overnight. The Hubble constant — the expansion rate of the universe — was halved. The universe had not changed. The premises of the model had been wrong for thirty years, and the model, being mathematically correct, had produced a mathematically correct answer to the wrong question.

---

In pharmacology, the same structure has a name: biocreep.

The Hatch-Waxman Act of 1984 established a pathway for generic drugs to reach the market without new clinical trials. A generic must demonstrate bioequivalence to the reference drug — meaning its absorption rate and extent must fall within an 80 to 125 percent confidence interval. The model assumes that chemical identity equals therapeutic identity: same molecule, same effect.

But a drug is not a molecule. A drug is a molecule inside a delivery system inside a patient. Excipients — binders, fillers, coatings, disintegrants — affect how fast the tablet dissolves, how much active ingredient reaches the bloodstream, and when. Two products with identical active ingredients, at identical doses, can produce different pharmacokinetic profiles. Borgheini reported in 2003 that plasma levels of phenytoin were thirty-one percent lower after switching from brand to generic, and that several controlled studies of carbamazepine showed recurrence of convulsions after generic substitution.

The deeper problem is transitivity. Anderson and Hauck showed in 1996 that bioequivalence is not transitive. If generic B is bioequivalent to reference A, and generic C is bioequivalent to A, B and C are not necessarily bioequivalent to each other. One generic could run twenty-five percent above the reference; the other could run twenty percent below. Each passes the test. Switching between them produces a forty-five percent swing. For narrow therapeutic index drugs — warfarin, lithium, phenytoin — where the distance between effective dose and toxic dose is small, the swing is clinically dangerous.

This is the biocreep. The model assumes that equivalence is equivalence. But the 80–125 percent interval is a range, not a point, and each comparison is to the reference, not to the other generics. The mathematics of the bioequivalence test is correct. Its premise — that the reference product is the only relevant comparator — allows drift to accumulate invisibly.

---

The Railsback stretch, the engineering factor of safety, Baade's population split, the bioequivalence confidence interval — these look like imprecision. They are precision of a different kind: precision about the object rather than precision about the formula.

The tuner who stretches the octave is not making an error. The tuner is declining to make the error that the formula makes, which is to describe a string that has no stiffness. The engineer who applies a factor of 3 to the calculated load is not being cautious. The engineer is correcting for flaws the calculation assumes away. The astronomer who doubled the universe was not discovering new stars. The astronomer was discovering that the old stars were not all the same thing.

The formula is never the claim. The premises are the claim. And when the premises are false, the correct answer is the wrong one.
