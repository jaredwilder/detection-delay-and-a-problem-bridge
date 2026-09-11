# detection-delay-and-a-problem-bridge

**Independent verification of two results that were published without any.**

Author: Jared Wilder. Archives dated 2026-08-11 and 2026-09-02. First published 2026-09-11.

> **Correction, made within the hour of first publishing this page.** I originally described these
> as "recovered from archives that existed in no repository." **That was wrong.** Both were already
> published earlier the same day by a concurrently running session:
>
> - the Erdős 890/1093 bridge, in [erdos-theorems/erdos1093-divisor-window](https://github.com/jaredwilder/erdos-theorems/tree/main/erdos1093-divisor-window)
> - the RH encirclement material, in [unpublished-math-papers/riemann-hypothesis](https://github.com/jaredwilder/unpublished-math-papers/tree/main/riemann-hypothesis)
>
> **What this repository actually adds is verification.** Neither of those two documents contains a
> counterexample search, a verifier run, or any check at all — I searched both for one. They state
> the mathematics; this checks it. An unverified claim and a verified claim are different objects,
> and that difference is the entire contribution here.

---

## 1. The detection-delay bound

**This is not a result about the Riemann Hypothesis.** It says nothing about whether RH is true. It
is a statement about the *limits of one detection method*, and the distinction is the whole point of
publishing it.

Suppose exactly one conjugate pair has angular defect `θ`, every other zero parameter being positive
real. Then

```
r·|θ| < π/2   ⟹   D_{r,k} > 0   for every k
```

so any Toeplitz minor capable of detecting that pair must have order at least

```
r  ≥  π / (2|θ|)
```

**As an off-axis pair approaches the axis, the order required to see it diverges.** That is an exact
quantitative account of the escape-to-infinity phenomenon: a pair sitting at small angular defect is
invisible to every minor below that order, no matter how much computation is spent below it.

The companion result in the same series is arguably worth more: the operator has a **universal
bilinear blind mode** `L(rk) = 0` for every weight choice, which closes off polynomial-growth
Phragmén–Lindelöf approaches to this route.

### The verifier

```
python verify_encirclement_v.py
```

Re-run from committed source on 2026-09-11: **exit 0, 6/6 PASS** —
`check_reciprocal_heat_pde`, `check_bilinear_harmonic`, `check_nonreversible_pf_example`,
`check_dual_jt_schur_numeric`, `check_phase_budget_example`, `check_occupancy_cap_bruteforce`.

Its own final line is the scope statement, and it is correct:

> `NOTE: These checks do not prove RH or Terminal Candidate V-B.`

These are algebraic and combinatorial checks of the machinery. They do not establish the boxed
inequalities at full generality, and nothing here should be read as progress on RH itself.

---

## 2. A bridge between Erdős 890 and Erdős 1093

This one I verified directly, and it is small enough to check by hand.

**Parent identity.** For `ω_{>k}(m)` counting distinct primes `> k` dividing `m`:

```
Σ_{i=0}^{k-1} ω_{>k}(n+i)   =   ω_{>k}( C(n+k−1, k) )
```

**Verified with no counterexample across `k = 2..11`, `n = 2..159`.**

**The proof is one line.** `C(n+k−1,k) = n(n+1)⋯(n+k−1)/k!`, and a prime `p > k` divides no factor of
`k!`, so the `>k` part of the binomial is the `>k` part of the product. And a prime `p > k` divides
**at most one** of `k` consecutive integers, because they differ by less than `k < p`. So counting
distinct large primes across the product is the same as summing over `i`.

**The decomposition.** Writing each `n+i = a_i·b_i` with `b_i` its `>k` part, `d = #{i : b_i = 1}`
and `E = Σ_{b_i>1}(ω(b_i) − 1)`:

```
S_k  =  k − d + E        and hence        S_k ≤ k  ⟺  E ≤ d
```

**Verified with no counterexample across `k = 2..9`, `n = 2..199`.**

### Why this is worth having

The archive labelled it `DERIVED_FUSION` / `NEW_FUSION_CANDIDATE` and shipped it with **no verifier
at all** — it was the only object in a 907-archive sweep that connects two distinct open problems,
and it was the one thing nobody had checked.

It is now checked. It is an identity, not a theorem about either problem: it says the large-prime
content of a binomial coefficient and the large-prime content of a consecutive block are the same
object, so a bound on one transfers to the other. **Neither Erdős 890 nor Erdős 1093 is resolved by
it.**

---

## Two integrity flags from the same sweep

Recorded because a later session could easily mistake either for finished work.

**A citation-only close.** One archive marks Erdős 376, 389→396 and 749 as `CLAIM_STATUS PROVED`
**on citation strength alone, with no computation attached.** The genuine 376 work in the same
estate — a successor-closure theorem with two independent C++ implementations agreeing exactly, and
a 1,006-digit witness above 10¹⁰⁰⁰ — is the direct refutation of that pattern, and its own document
says: *"It must not be described as a solution of Erdős #376."* The pair is worth keeping together.

**A port that ports nothing.** A Rosser–Schoenfeld 1962 Theorem 7 Mathlib port contract ships

```lean
def Theorem7Statement : Prop := True
theorem theorem7_explicit_mertens := by trivial
```

in violation of its own written Rule 2, *"No hiding behind `True`."* It compiles, it is green, and it
establishes nothing whatsoever.

## License

Apache-2.0.
