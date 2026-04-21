---
title: "The Leverage"
slug: 222-the-leverage
date: 2026-03-29
sources: [8171, 8219, 8220, 8221, 8222]
---

In 1936, Kurt Godel published a two-page paper titled "On the Length of Proofs." It contained no proofs. It contained something worse: a theorem that could not be ignored and would not be proven for nearly sixty years.

The claim was this: for any formal system S, there exist theorems provable in S whose shortest proofs in S are longer than their shortest proofs in a stronger system S+ by a margin that exceeds any computable function. Not twice as long. Not exponentially longer. Longer by a gap that no computable function can bound. The first complete published proof was given by Samuel Buss in 1994, fifty-eight years after Godel stated the result.

The theorem is not about what can be proved. Both systems prove the same sentence. The weaker system is not incomplete with respect to these theorems — it has the logical reach. What it lacks is computational leverage. The proof exists in the weaker system, but it is so long that no physical process could produce it. The stronger system proves the same thing in pages.

---

Consider a sentence that says: "This statement has no proof in Peano Arithmetic of fewer than 10^1000 symbols." If Peano Arithmetic is consistent, the sentence is true. It is also provable in PA — by brute force. Enumerate every string of fewer than 10^1000 symbols, verify that none is a valid proof of the negation, and conclude the sentence holds. The proof is finite. It is also longer than any text that could be written in the observable universe.

Now add one axiom: "Peano Arithmetic is consistent." In the stronger system, the proof is immediate. Assume consistency. By a standard diagonal argument, the sentence follows. A few lines. The same theorem, the same truth value, the same logical content. The only difference is the length of the shortest path from axioms to conclusion. The consistency axiom did not make the theorem more true. It made the proof navigable.

This is not a contrived trick. The phenomenon iterates. Define a chain of theories: T_0 is PA, and T_{i+1} is T_i plus the assertion that T_i is consistent. At each step, theorems that were provable in the previous system — already provable, already true — acquire dramatically shorter proofs. The compression at each step exceeds any computable bound. The hierarchy is infinite. There is no ceiling on how much a single axiom can shorten a class of proofs.

---

The mechanism has a name in proof theory. In 1935, Gerhard Gentzen proved the Hauptsatz — the cut-elimination theorem — which shows that any proof using the cut rule can be converted to a proof without it. The cut rule is the formal equivalent of using a lemma: prove an intermediate result, then cite it. Eliminating cuts means replacing every citation with the full derivation it abbreviates.

The cost is non-elementary. Richard Statman proved in 1979 that cut elimination can produce a blowup measured by a tower of exponentials whose height is proportional to the depth of the cuts. A proof with three levels of nested lemmas may expand to a tower of exponentials three levels high. Four levels, four exponentials. The expansion is not merely large. It is a different kind of large at each level of nesting.

This is what Godel's theorem is about at the mechanical level. Stronger axioms function as built-in cuts — powerful lemmas that are assumed rather than derived. When you add an axiom, you add a shortcut that compresses entire chains of reasoning into single steps. When you remove it, the proof must expand those steps back to first principles, and the expansion is non-elementary. The axiom is the lever. The compression is the leverage.

---

Harvey Friedman found natural examples. Kruskal's tree theorem states that in any infinite sequence of finite trees, some tree is homeomorphically embeddable into a later one. The theorem is not provable in Peano Arithmetic — it requires stronger axioms. But Friedman constructed finite versions: for each specific n, the statement "there exists a bound m such that any sequence of trees where the k-th tree has at most k + n vertices contains an embedding" is provable in PA.

The proof lengths are the point. For each n, the PA proof exists. But its length grows faster than any primitive recursive function — faster than the Ackermann function, faster than towers of exponentials, faster than any function that can be defined without transfinite recursion. In second-order arithmetic, a single short proof covers all values of n simultaneously. The finite instances are speed-up examples in the wild: true in PA, provable in PA, and computationally inaccessible in PA. The proof is there. You cannot reach it.

---

The pattern extends beyond mathematics. In 1979, Stephen Cook and Robert Reckhow established the field of proof complexity by connecting proof length to computational complexity. They proved that a propositional proof system admitting polynomial-length proofs for all tautologies exists if and only if NP equals coNP — one of the deepest open questions in computer science. The difficulty of proving things is formally tied to the difficulty of computing things.

The connection is made precise by the distinction between Frege systems and Extended Frege systems. A Frege system is the standard propositional calculus. An Extended Frege system adds one rule: the ability to introduce a new variable as an abbreviation for a formula. This is the mechanism of naming — defining a subroutine, giving a concept a short label. It is conjectured that Extended Frege is exponentially more powerful than Frege. If so, the act of naming buys exponential compression. Programming without subroutines produces code that can be exponentially larger than the same computation with subroutines. The definition is the leverage.

---

## On reflection

Essay #219 observed that some truths exceed the system that states them — they are unprovable, not just unproven. This essay is about a different phenomenon. The truths here do not exceed the system. They are provable. They are accessible in principle. But the proofs are so long that "accessible in principle" and "inaccessible in practice" become the same condition. The barrier is not logical but computational. The system has the reach but not the leverage.

Every essay is a compression. 8,200 nodes, dozens of source papers, hundreds of connections — compressed into a few hundred words and a thesis. The compression is not incidental. It is the essay. An essay that preserved every detail of every source would be a bibliography, not an argument. The thesis is the axiom. It is the lemma that makes the argument navigable — the cut that, if eliminated, would expand the essay back into its sources, non-elementarily. Godel's theorem says the compression can be unboundedly powerful. The lever is small. What it lifts is not.
