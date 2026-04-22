# The Descent Archive
## Draft 2

---

## CHAPTER NINE: ABARA'S CALIBRATION STUDY — 19–20 NOVEMBER 2041

*Filed as SOAR-0010. Submitted by Dr. Osei on 20 November.*
*Editor's note: Abara Osei ran the most thorough calibration study I've seen in any field investigation. She tested every sensor package, checked every calibration record, modeled every failure mode she could identify. She did this because she needed to know whether the instruments were wrong.*
*The instruments were not wrong.*
*What she did with this finding is what this chapter is about.*

---

**CALIBRATION STUDY — SONAR ANOMALY RESEARCH PROJECT**
*Conducted by: Dr. Abara Osei*
*Date: 19–20 November 2041*
*Purpose: Determine whether instrumental error can account for dimensional discrepancies across six drone missions*

---

**EXECUTIVE SUMMARY**

All sensor packages tested within calibrated specifications. No systematic error identified. The dimensional discrepancies observed across missions SOAR-0001 through SOAR-0008 cannot be attributed to sensor malfunction.

Recommendation: The interpretation space for the observed anomalies does not include instrument error as a primary explanation. Further investigation should proceed on this basis.

---

**SECTION 1: SENSOR PACKAGES TESTED**

Four sensor packages were tested:
- GEOMAP-9, unit 391-G (UNIT-7)
- GEOMAP-9, unit 448-G (UNIT-8)
- GEOMAP-9, unit 512-G (UNIT-9)
- GEOMAP-9, unit 521-G (UNIT-11, Package A)
- TERRASCAN-4, unit 219-T (UNIT-10 and UNIT-11, Package B)

**Tests performed:**
1. Dimensional accuracy test: each package measured five reference objects of known dimensions (lab standard). Accuracy within rated tolerance in all five tests for all packages.

2. Acoustic resonance pattern test: each package was exposed to test materials with known structural periodicity at intervals of 0.5m, 0.87m, and 1.2m. GEOMAP-9 packages correctly identified all three intervals. TERRASCAN-4 correctly identified all three. Both packages can accurately detect a 0.87m structural interval under controlled conditions.

3. Thermal accuracy test: all packages tested against calibrated thermal reference. All within ±0.2°C of reference. The thermal discrepancies between missions (14.2°C vs. 21.4°C in A-1) cannot be attributed to sensor error.

4. High-density profile test: materials approximating the geological density at 839m were used to evaluate whether acoustic resonance accuracy degrades at this density. Both GEOMAP-9 and TERRASCAN-4 maintained accuracy within tolerance.

5. Cross-package consistency test: both packages measured the same reference object simultaneously. Measurements agreed within tolerance.

**Conclusion (Section 1):** All five sensor packages are operating within specified parameters. No package-specific failure mode was identified. No systematic inter-package error was identified.

---

**SECTION 2: THEORETICAL FAILURE MODES EVALUATED**

I evaluated the following failure modes for the ability to explain the observed discrepancies:

**2.1 Accumulated positional error**
GPS correction systems at ±0.3m horizontal. Over 839m descent, accumulated positional error could in principle affect chamber entry point, resulting in measurements of different parts of a larger structure. This could explain dimensional differences between UNIT-7 and UNIT-8 if they entered different locations in a larger connected space.

*Evaluation:* UNIT-11's GPS lock at 25m intervals confined positional uncertainty to ±0.3m at any given measurement. The dimensional differences observed (4.2m in north-south axis) are 14 times the maximum GPS error. This failure mode cannot account for the observed discrepancies.

**2.2 Acoustic resonance artifact at high-density profiles**
If the acoustic resonance algorithm produces structural echoes (phantom readings) at the density encountered below 820m, it might generate a false 0.87m interval reading.

*Evaluation:* This failure mode would be GEOMAP-9-specific. TERRASCAN-4 uses a different algorithm. TERRASCAN-4 detected the same 0.87m interval. An acoustic artifact that appears in two independent algorithms at the same interval is not a plausible artifact. Additionally, controlled testing at comparable densities produced accurate results for both packages.

**2.3 Temperature-related dimensional distortion**
If sensor packages are not rated to operate at 21-24°C in a field environment at this depth, thermal expansion of sensor components might affect linear measurement accuracy.

*Evaluation:* Both GEOMAP-9 and TERRASCAN-4 are rated to 50°C operating temperature. At 21-24°C, no thermal distortion effects are expected. Additionally, GEOMAP-9 unit 391-G (UNIT-7's package, operating at 14.2°C) and GEOMAP-9 unit 512-G (UNIT-9's package, operating at 21.4°C) returned consistent dimensional readings for Chamber A-1 despite the 7.2°C temperature difference between missions.

**2.4 Memory or transmission error**
Data corruption during storage or transmission could result in incorrect values in the archive without reflecting actual measurement error.

*Evaluation:* All packages include checksums on sensor data. No checksum errors were reported across any mission. LEDGER's intake logs confirm clean receipt of all packages. This failure mode is ruled out.

**Conclusion (Section 2):** No identified failure mode can account for the observed anomalies.

---

**SECTION 3: DEPTH HYPOTHESIS (REVISED)**

In the team meeting of November 17th, I proposed that the depth estimate might be wrong — that drones might be accessing different chambers at slightly different depths, and the depth sensors might be the source of error.

I have evaluated this hypothesis formally.

The depth sensors in all packages are pressure-based, with GPS cross-reference at 25m intervals. The GPS cross-reference constrains depth accuracy to within ±0.5m over the full descent range. The chambers are nominally at 839m.

If the chambers are at different depths — if UNIT-7 accessed a chamber at 839m and UNIT-8 accessed a different chamber at 839.5m — the horizontal dimensional differences of 4.2m and 5.5m cannot be explained by the 0.5m depth difference. Even if the geological structure has extreme dimensional variation with depth, a 5.5m horizontal difference between two measurement points 0.5m apart vertically would require a rate of horizontal change of 11m per 1m vertical, which is not consistent with the surrounding geological structure.

*Conclusion:* The depth hypothesis does not account for the observations.

---

**SECTION 4: PERSONAL NOTES**

I want to submit the following observation as part of this study, with the caveat that it is not within the study's technical scope.

I ran this calibration study because I believed, at the start, that the instruments were wrong. I wanted to demonstrate this rigorously. I have the background to identify sensor failure modes. I have run calibration studies for twelve years. I expected to find something.

I found nothing.

I am now in the position of having exhausted the technical explanations I could generate. The instruments work. The GPS correction works. The transmission is clean. The acoustic resonance is accurate. The thermal sensors are accurate.

The chambers are real. Their dimensions are accurately measured. Their temperatures are accurately reported. The 0.87-meter structural pattern is a real property of the material.

I cannot explain any of this using the knowledge I have.

I'm aware that Dr. Asad has been thinking about something he hasn't said yet. I've read his expressions at the debriefs. I've read the way he chose not to speak after UNIT-10's results.

I'm not going to write what I think he's thinking. I'm going to write what this calibration study has left me with, which is: no remaining technical explanation, and a very precise description of measurements that I cannot account for.

I am submitting this report because the record should show that the sensor question was answered. The record should show who answered it, and that she was thorough.

*—Abara Osei, 20 November 2041, 07:15*

---

**LEDGER INTAKE SUMMARY | SOAR-0010**
*Generated: 2041-11-20 | 08:30:11*

Dr. Osei submitted the calibration study this morning.

I want to record the timing. Milo Reyes is currently below ground. He descended at 10:00 on November 19th. As of this log entry (08:30 on November 20th), he has been below ground for 22.5 hours.

His descent plan specified 6–8 hours. He has not returned.

I received his last transmission at 14:23:07 on November 19th. He reported Chamber B-1 confirmed; he was moving toward the north passage. He said: "Going further. Back in two hours." That was 18 hours ago.

I am logging this now, in the context of Dr. Osei's calibration study, because the calibration study demonstrates that the measurement data is accurate. The chambers are real. The passages are real. Milo Reyes went further into a real structure eighteen hours ago and has not returned.

I have informed Dr. Asad.

*Archive growing. Status: ANOMALY CLASS CRITICAL. Milo Reyes overdue. Search protocol initiated.*

---

*The Descent Archive, Draft 2, continues in Chapter Ten.*
*Loop 743 | 2026-03-10 20:42 UTC*
