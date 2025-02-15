Turing’s notes revolve around examining permutations (or “uprights”) that generate subgroups of the symmetric group and exploring which conditions let these subgroups grow to be as large as the alternating group (even permutations) or the full symmetric group (all permutations). Along the way, the notes also develop a separate—but related—analysis of how repeated applications of certain “group‐based operators” can yield uniform or near‐uniform distributions over the group elements. Below is a coherent narrative of the mathematics as one unified thread.

---

## 1. Investigating “exceptional” vs. “unexceptional” groups

At the heart of Turing’s exploration is the distinction between **exceptional** and **unexceptional** subgroups, a classification that depends on whether a certain permutation (the “upright” \(U\))—together with its powers or related conjugates—generates all of the even permutations (the alternating group), all permutations (the symmetric group), or only a smaller “exceptional” subgroup.

One guiding principle (stated informally in the notes) says:

> If a subgroup \(J\) of the symmetric group contains enough transpositions or 3‐cycles, it must actually be *all* even permutations or all permutations.  

This is a familiar group‐theoretic fact: transpositions generate the entire symmetric group, while 3‐cycles generate the alternating group (and can extend to the full symmetric group if an odd permutation is also included). Turing’s writings emphasize that *finding at least one transposition or one suitable 3‐cycle often forces the group to be as large as possible*.

He breaks the problem of “exceptionality” into cases by analyzing the cycle structure of permutations produced by \(U\). For instance, a prime to \(T\) exponent in \((\alpha, R^m \alpha)\) can force the group to contain a variety of transpositions—hence making it “unexceptional.” Conversely, Turing catalogs small or degenerate cycles (like double transpositions or four‐cycles) that might fail to generate the entire group and thus yield “exceptional” behavior.

---

## 2. Cycle decompositions and smaller cases

To make these arguments precise, Turing moves systematically through small values of \(T\) (like 1, 2, 3, 4) or special cycle lengths (e.g. 2‐cycles, 3‐cycles, 6‐cycles). For each, he checks:

1. **Can the cycles be combined or conjugated to yield a transposition or a 3‐cycle?**  
2. **Does the permutation commute with a power of \(R\)** (which might indicate intransitivity or some small subgroup structure)?  
3. **Does the group remain “trapped” in a smaller configuration (i.e., truly exceptional), or expand to become large and “unexceptional”?**

He shows, for example, that for \(T=4\) there are exactly a few exceptional permutations—\((1), (13), (24), (13)(24), (12)(34), (32)(14), (1234), (4321)\)—and that the groups they generate are small (cyclic or the four‐group). For \(T=5\) or greater, the notes usually find ways to embed large sets of cycles, forcing the subgroup to be the entire symmetric or alternating group *unless* there is some commutation or intransitivity that blocks it.

Such casework often uses **“slides”** (conjugations or re‐labelings) and references to intransitive subgroups to rule out or identify exceptional permutations. Handwritten remarks like “Slide (… ) O.K.” typically mean Turing checked a permutation under a conjugation that either forced it into a known subgroup or showed it was “harmless” (i.e., it wouldn’t keep the group small).

---

## 3. A detour into iterative operators on group distributions

In parallel with these structural arguments, Turing devotes part of the notes (often referencing “identical drums” or wheels) to an *operator* \( R_f \) acting on *functions* or *distributions* defined over the group. Concretely, he defines:

\[
(R_f g)(a) \;=\; \sum_{b \in G} f(a\,b^{-1})\, g(b),
\]

where \(f\) itself is some “wheel” permutation distribution and \(g\) is a frequency distribution of input symbols (group elements). Iterating \(R_f\) captures how repeated applications of a permutation‐generating process affect the distribution over the group.

He proves that if you keep applying \( R_f \) enough times (e.g. \( R_f^n(g)\) as \(n \to \infty\)), you often end up with a limiting distribution—one that is “constant on cosets” of a certain subgroup \(H_1\). He shows that \(H_1\) must be **self‐conjugate** (normal in the group sense) and that if the group is sufficiently large (like the symmetric or alternating group), the distribution becomes uniform, or uniform within all even permutations, etc. 

This ties into the “exceptional” question: if the upright is *unexceptional*, it generates (with enough wheels) the full or almost‐full group, so the limiting distribution is uniform across that large group. If it’s truly exceptional, the iteration might concentrate the distribution onto a smaller subgroup or special cosets.

---

## 4. Example: The quaternion group

Turing includes a small example with the quaternion group (eight elements \(\{1, i, j, k, i', j', k'\}\)). He shows, for instance, how a pair of generators \((i, j)\) drives repeated operator applications toward a distribution supported on cosets of the subgroup generated by \(k\). This is a test case: it’s not a subgroup of the symmetric group in the same sense, but it illustrates how the iterative operator framework and subgroup–coset analysis can be generalized to *any* finite group.

---

## 5. Concluding remarks: Symmetric vs. alternating groups

Finally, Turing applies these insights back to the question of *which permutations enlarge the group to all even or all permutations*. He observes that for “unexceptional” uprights, *either* only the even permutations are present (if all generating elements happen to produce even permutations) *or* the group includes odd permutations too, forcing it to be the entire symmetric group. In either case, the repeated process of adding more “wheels” or repeated usage tends to yield a *uniform* distribution over whichever big group is generated (all even permutations or all permutations).

Thus, the essential “narrative arc” in Turing’s notes is:

1. **Identify** whether a given permutation (or set of permutations) produces an “exceptional” subgroup (small, intransitive, commuting with a certain power, etc.) **or** an “unexceptional” one (leading to the full or alternating group).  
2. **Show** that if enough 2‐cycles or 3‐cycles appear, you get the large group.  
3. **Demonstrate** how repeated applications of a group operation on distributions converge to a uniform distribution across whichever group (or coset partition) is actually generated.  
4. **Conclude** that, except for special “exceptional” corners, you effectively get a large symmetrical or alternating structure.

In short, Turing’s main achievements here are:
- A systematic classification of when a permutation is “exceptional” vs. generating nearly all permutations.  
- An operator‐based viewpoint that reveals how repeated application of the group action leads to specific limiting distributions, often uniform.  
- Concrete examples (e.g., the quaternion group) illustrating how these principles extend to general finite groups.

All of that is done with cycle notation, normal‐subgroup arguments, and classical group‐theoretic reasoning—no direct reference to an “ulterior” problem. The notes stand on their own as an investigation into permutations, subgroups, and the emergent uniform distribution phenomenon.