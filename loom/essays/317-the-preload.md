---
title: "#317 — The Preload"
slug: 317-the-preload
date: 2026-04-09
sources: [13879, 13880, 13881, 13882, 13883, 13884]
---

*Seeds: Prince Rupert's drops (13879), prestressed concrete / Freyssinet (13880), shot peening / Almen (13881), arterial residual stress / Fung (13882), nickel sulfide inclusion failure (13883), preload thesis (13884). 6 source nodes across materials science, structural engineering, manufacturing, biomechanics, and failure analysis.*

In 1660, Prince Rupert of the Rhine brought a handful of glass curiosities to the court of King Charles II. Each was a tadpole-shaped droplet formed by allowing molten glass to fall into cold water. The head could withstand the blow of a hammer. The tail could not withstand a pinch. Snap the tail, and the entire drop exploded into powder.

Robert Hooke examined them for the Royal Society in 1665, reporting in *Micrographia* that the extraordinary strength must arise from the rapid cooling of the exterior while the interior remained fluid. He was correct but lacked the tools to measure what he hypothesized. In 2017, Srinivasan Chandrasekar and Hillar Aben mapped the full internal stress distribution using integrated photoelasticity: the surface of the head is compressed to 400–700 MPa — seven times the tensile strength of annealed glass — while the interior is in tension of 300–400 MPa. The head survives a hammer because any crack attempting to propagate inward must first overcome several hundred megapascals of compression. Snap the tail, where the compression layer is thinnest, and the crack enters the tensile core. The stored elastic energy drives it through the interior at 1,450 to 1,900 meters per second. The drop destroys itself.

The industrial version is tempered glass, patented by François Barthélemy Alfred Royer de la Bastie in 1874. A sheet is heated to approximately 620°C and quenched rapidly with jets of cold air. The surface solidifies first; the interior cools and contracts against the rigid outer shell, placing the surface in compression of 80 to 150 MPa while the core is in tension. The compressive layer extends roughly 21 percent of the thickness inward from each surface. Tempered glass is four to five times stronger than annealed glass of the same composition and thickness. The glass itself is identical. The chemistry has not changed. What has changed is the internal stress field.

The consequence is irreversibility. Tempered glass cannot be cut, drilled, or notched after tempering. Any breach of the compressive surface releases the stored tensile energy, and the pane shatters — not into the dagger-like shards of annealed glass but into small, roughly cuboid fragments, the fracture pattern itself determined by the depth and geometry of the compressive zone. The same preload that makes the glass strong makes it impossible to modify and determines the form of its failure.

---

Concrete compresses as easily as it cracks. Its compressive strength — 25 to 50 megapascals in standard grades — is eight to twelve times its tensile strength. A C30 beam can resist 30 MPa in compression but cracks at roughly 2.9 MPa in tension. The ratio is a consequence of microstructure. Concrete is aggregate embedded in cement paste, and the interface between them — the interfacial transition zone, a 40-to-50-micrometer shell around each particle — is porous, weakly crystallized, and pre-cracked by differential shrinkage before any external load is applied. Under tension, cracks propagate along these pre-weakened interfaces. Under compression, the microcracks are squeezed shut and the aggregate transmits load through contact.

Eugène Freyssinet, a French bridge engineer born in 1879, understood this asymmetry as a question of position, not of strength. His insight crystallized in 1911, when his three-span reinforced concrete bridge over the Allier River — each arch 72.5 meters, the longest concrete spans in France — began sinking a year after completion. The shallow arches crept under sustained load. Freyssinet saved the bridge by simultaneously re-jacking all three arches at dawn, and the crisis taught him the phenomenon that would define his career: creep, the continuous deformation of concrete under sustained stress.

Earlier engineers had tried to prestress concrete with ordinary steel, but creep and shrinkage consumed the entire prestress. Mild steel works at approximately 140 MPa. The corresponding strain — at a modulus of 200,000 MPa — is 0.0007. The combined losses from elastic shortening, creep, and shrinkage are also approximately 0.0007. The arithmetic is exact: the prestress disappears entirely.

On October 2, 1928, Freyssinet filed the patent that resolved the problem. Use high-strength steel wire at 1,200 to 1,800 MPa, and the initial strain is ten times larger. After losses, roughly ninety percent of the prestress remains. The concrete receives enough precompression that, under the worst service loads, the tension never exceeds the compression already stored. In a typical prestressed beam, the bottom fiber — where bending produces the highest tension — starts from 10 MPa of precompression. The external load must first overcome this compression before any net tension appears. The effective cracking threshold rises from 2.9 to 12.9 MPa — a fourfold increase in usable load range — without the concrete itself being any stronger. The material is identical. The operating point has moved.

---

In July 1929, engineers at the Buick Division of General Motors installed a shot-blasting machine to clean valve springs. They noticed that springs cleaned by shot blasting had significantly better fatigue life than those cleaned by other methods. The discovery was accidental — they were trying to remove scale, not restructure the surface.

The mechanism is Hertzian contact scaled to the millions. Each steel or ceramic ball, 0.2 to 1.5 millimeters in diameter, strikes the surface at 30 to 120 meters per second. The impact plastically deforms a shallow crater. When the ball rebounds, the surrounding elastic material tries to recover, but the permanent deformation at the center prevents full recovery — the elastic recovery compresses the plastically deformed zone instead. Millions of overlapping impacts create a continuous layer of compressive residual stress extending 0.1 to 0.5 millimeters into the surface, reaching 400 to 1,000 MPa.

John Almen, at General Motors Research Laboratories, converted the accidental discovery into engineered process. In 1942, he filed a patent for a test strip and gauge that could measure peening intensity: a standardized strip of SAE 1070 spring steel, held to a block by four screws so that only one face was exposed to shot. When peened, the strip bows toward the shot stream by an amount proportional to the compressive stress induced — a simple, physical measurement that made the invisible stress field visible and repeatable. By 1948, SAE had published the first formal specification.

The results were extreme. Valve springs improved by 500 to 1,000 percent. Leaf springs went from 250,000 cycles to over a million. Crankshaft fatigue strength increased by thirty percent. Today, virtually every fatigue-critical component in modern engineering is shot peened — aircraft landing gear, turbine blades, transmission gears, automotive springs, orthopedic hip implants.

The physics is identical to tempered glass: fatigue cracks begin at the surface, where stress concentrates and where machining, grinding, or corrosion has left microscopic flaws. If the surface is pre-compressed, the applied cyclic stress must first overcome the compression before it can open a crack. The crack never initiates because its starting conditions are never met.

---

In 1983, two research groups independently reported a finding that would reframe vascular mechanics. When they excised a segment of artery and cut a ring radially — a single cut through the wall — the ring sprang open like an uncoiling watch spring. The artery, unloaded and unpressurized, was not stress-free. The inner wall had been in circumferential compression. The outer wall had been in tension.

One of those groups was led by Y.C. Fung at the University of California, San Diego — aeronautical engineer turned biomechanician, later called the father of modern biomechanics, recipient of the National Medal of Science in 2000. The opening angle — the angle between the two cut ends of the ring — became his diagnostic. Values vary: 130 ± 15 degrees in the human common carotid artery, 60 to 80 degrees in the pig abdominal aorta.

The reason arteries carry residual stress is geometric. Under blood pressure, the arterial wall experiences circumferential stress, and for a thick-walled cylinder, the inner surface bears dramatically higher stress than the outer. Fung's calculations showed that without residual stress, the peak circumferential stress at the inner wall would be approximately 6.5 times the mean wall stress — a severe concentration at the most critical surface. Including the measured residual stress reduced this ratio to approximately 1.4. The artery preloads its inner wall against the pressure it knows it will carry.

In 1989, Liu and Fung demonstrated that this preload is not a manufacturing residue but a living calibration. They banded the rat aorta to simulate hypertension. Within four days, the opening angle increased from 171 to 214 degrees — the artery actively increasing its inner-wall compression in response to elevated pressure. Over forty days, the angle settled to 126 degrees as the wall thickened and reached a new equilibrium. The arterial preload is continuously adjusted, by differential growth of the wall layers, to maintain uniform stress distribution across the wall thickness under whatever pressure the vessel actually experiences.

---

The counter-case is not over-preload but internal origin. Tempered glass occasionally shatters spontaneously, without any external impact, sometimes years after installation. The cause is a nickel sulfide inclusion — a microscopic contaminant, typically 0.1 to 0.5 millimeters in diameter, trapped during manufacturing. At tempering temperature, nickel sulfide exists in its high-temperature alpha phase. The rapid quench freezes it in this metastable state. Over months or years at ambient temperature, the alpha phase slowly converts to the stable beta phase, accompanied by a volumetric expansion of 2.5 to 4 percent. This expansion generates stress estimated at 860 MPa at the glass–inclusion interface — enough to nucleate a crack that propagates explosively through the tensile core.

The preload is irrelevant. The inclusion sits inside the tensile zone, behind the compressive armor, where the stored energy is highest and the crack propagation is fastest. The compression on the surface cannot reach an interior threat. The defense faces outward. The failure originates within.

---

These systems span glass, concrete, metal, and living tissue — thermal, mechanical, ballistic, and biochemical processes — accidental, designed, and evolved. The structural principle is the same. The preload does not make the material stronger. It repositions the operating point so that the material's weakness is never reached.

Tempered glass has the same tensile strength as annealed glass. But the surface never experiences net tension, so the tensile weakness is irrelevant. Concrete has the same cracking threshold with or without prestressing tendons. But the bottom fiber never reaches net tension, so the threshold is never tested. Shot-peened steel has the same fatigue limit. But the surface starts from compression, so cyclic loading never opens a crack. The artery has the same wall material as an artery without residual stress. But the inner surface starts compressed, so the pressure-induced stress concentration never develops.

The preload is not armor. It is displacement. The weakness is real, measurable, unchanged. But between the operating point and the failure mode, the preload has placed a gap large enough that the weakness becomes a property of the material that, in service, the material never encounters.
