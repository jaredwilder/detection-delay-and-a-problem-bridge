# RIEMANN HYPOTHESIS — ENCIRCLEMENT V
## Ten faithful internal rounds + terminal encirclement

**Date:** 2026-08-11  
**Status:** `MajorReduction / StrictFrontier`  
**Riemann Hypothesis proved:** **NO**

This campaign starts from Encirclement IV and does not revive its killed routes.

---

# Terminal verdict

The exact harmonic-velocity program does **not** by itself close the escape-to-infinity problem.

Two decisive facts were established:

1. the adaptive harmonic operator has a universal bilinear blind mode
   \[
   rk,
   \]
   so a naive polynomial-growth Phragmén–Lindelöf theorem is false;

2. in the real-zero/PF-infinity phase, every consecutive Toeplitz minor is a
   rectangular Schur polynomial, and a single zero parameter can contribute at most
   \(1/k\) of the normalized logarithmic sensitivity.

The second fact produces a rigorous *dilution mechanism* for high-index zero motion.

The surviving obstruction is now sharply identified:

> Near a de Bruijn–Newman collision, a very small angular departure of one or a few
> zero pairs can remain invisible to every bounded determinant order, while a
> determinant order diverging like the reciprocal angle can eventually detect it.

Thus the terminal unresolved object is no longer generic harmonic growth.  It is the
**collision-angle / determinant-order coupling at infinity**.

---

# Round 1 — Kill generic reversibility

Encirclement IV gave the exact adaptive harmonic equation
\[
R_{r,k}\Delta_k^2 V_{r,k}
+
A_{r,k}\Delta_r^2 V_{r,k}
=0,
\qquad
R+A=1.
\]

Interpreting this as a nearest-neighbor random walk is exact.

A tempting next step is to seek a reversible measure \(\pi\) and use Dirichlet energy.

For reversibility one would need
\[
\pi_{r,k}R_{r,k}
=
\pi_{r,k+1}R_{r,k+1},
\]
and
\[
\pi_{r,k}A_{r,k}
=
\pi_{r+1,k}A_{r+1,k}.
\]

The corresponding plaquette compatibility condition fails for a generic positive
Toeplitz determinant array, even for finite PF-infinity sequences.

**Kill:** the adaptive walk is not generically reversible.

The factorial orbit is exceptional: for
\[
R=\frac{k}{k+r},\qquad A=\frac{r}{k+r},
\]
one may take
\[
\pi_{r,k}=\frac{r+k}{rk}.
\]

---

# Round 2 — Exact reciprocal heat equation

Let
\[
G_t(z)=\sum_{n\ge0}a_n(t)z^n
\]
satisfy
\[
\partial_tG_t=4zG_t''+2G_t'.
\]

Define
\[
H_t(z)=G_t(-z),
\qquad
E_t(z)=\frac1{H_t(z)}.
\]

Then
\[
\partial_tH_t=-4zH_t''-2H_t',
\]
and direct differentiation gives

\[
\boxed{
\partial_tE_t
=
-4zE_t''
-2E_t'
+
8z\frac{(E_t')^2}{E_t}.
}
\tag{V.1}
\]

**Kill:** Jacobi–Trudi duality does not turn the de Bruijn–Newman deformation into
another copy of the same linear heat equation.  The reciprocal coordinate evolves
nonlinearly.

---

# Round 3 — Universal bilinear harmonic obstruction

For every choice of adaptive weights \(R,A\),

\[
\Delta_k^2(rk)=0,
\qquad
\Delta_r^2(rk)=0.
\]

Hence
\[
\boxed{
L(rk)=
R\Delta_k^2(rk)+A\Delta_r^2(rk)=0.
}
\tag{V.2}
\]

More generally
\[
c_0+c_1r+c_2k+c_3rk
\]
lies in the kernel.

Therefore boundary control plus a generic polynomial-growth bound cannot yield a
Phragmén–Lindelöf close.

The critical invisible growth scale is bilinear area:
\[
rk.
\]

A successful no-escape theorem must rule out an \(rk\)-scale mode, not merely show
that \(V\) is finite or polynomial.

---

# Round 4 — Exact Schur representation in the PF phase

Assume the deformed generating function is in the PF-infinity phase:
\[
G_t(z)
=
a_0(t)\prod_{j\ge1}(1+\alpha_j(t)z),
\qquad
\alpha_j(t)>0.
\]

Then
\[
a_n(t)=a_0(t)e_n(\alpha(t)).
\]

For the consecutive Toeplitz minor,
\[
D_{r,k}(t)
=
a_0(t)^r
\det[e_{k+j-i}(\alpha(t))]_{i,j=0}^{r-1}.
\]

Dual Jacobi–Trudi gives the exact identity

\[
\boxed{
D_{r,k}(t)
=
a_0(t)^r\,s_{(r^k)}(\alpha(t)).
}
\tag{V.3}
\]

Here \((r^k)\) denotes the rectangle with \(k\) rows and \(r\) columns.

This representation is valid throughout the real-zero phase and converts determinant
sensitivity into tableau combinatorics.

---

# Round 5 — Occupancy-cap theorem

Define
\[
q_j
=
\alpha_j\frac{\partial}{\partial\alpha_j}
\log s_{(r^k)}(\alpha).
\]

Because the Schur polynomial has a positive semistandard-tableau expansion, \(q_j\)
is the expected number of appearances of symbol \(j\).

In a rectangle with \(r\) columns, columns are strictly increasing.  Therefore any
fixed symbol can appear at most once in each column:

\[
\boxed{
0\le q_j\le r.
}
\tag{V.4}
\]

Homogeneity gives
\[
\boxed{
\sum_j q_j=rk.
}
\tag{V.5}
\]

Hence the normalized sensitivities
\[
p_j:=\frac{q_j}{rk}
\]
satisfy

\[
\boxed{
0\le p_j\le\frac1k,
\qquad
\sum_jp_j=1.
}
\tag{V.6}
\]

This is the central exact theorem of Encirclement V:

> **No individual zero parameter can carry more than \(1/k\) of the normalized
> log-sensitivity of a rectangular minor.**

---

# Round 6 — Exact Schur distortion theorem

Let \(\alpha_j,\beta_j>0\), and set
\[
\delta_j=\log(\alpha_j/\beta_j).
\]

Every tableau monomial in \(s_{(r^k)}\) has exponents
\[
0\le m_j\le r,
\qquad
\sum_jm_j=rk.
\]

Suppose that for some \(J\),
\[
|\delta_j|\le M_J
\quad(j\le J),
\]
and
\[
|\delta_j|\le\varepsilon_J
\quad(j>J).
\]

Then every monomial ratio lies between
\[
\exp[-rJM_J-\varepsilon_Jrk]
\]
and
\[
\exp[rJM_J+\varepsilon_Jrk].
\]

Since all Schur coefficients are nonnegative,

\[
\boxed{
\left|
\log\frac{s_{(r^k)}(\alpha)}
{s_{(r^k)}(\beta)}
\right|
\le
rJM_J+\varepsilon_Jrk.
}
\tag{V.7}
\]

Consequently,

\[
\boxed{
\frac1{rk}
\left|
\log\frac{s_{(r^k)}(\alpha)}
{s_{(r^k)}(\beta)}
\right|
\le
\frac{JM_J}{k}+\varepsilon_J.
}
\tag{V.8}
\]

If the zero parameters at two real-zero times agree asymptotically in the tail, then
their rectangular-minor free energies differ by \(o(rk)\) as \(k\to\infty\).

This kills a possible bilinear distortion of the determinant *free energy* in the PF
phase.

---

# Round 7 — Sparse angular phase-budget theorem

The Schur representation is algebraic and continues to complex-conjugate zero
parameters.

Suppose all parameters are positive real except conjugate pairs
\[
\rho_\ell e^{\pm i\theta_\ell}.
\]

For any tableau monomial, the phase contributed by pair \(\ell\) is
\[
(m_{\ell,+}-m_{\ell,-})\theta_\ell.
\]

Since each exponent is at most \(r\),

\[
|\arg(\text{monomial})|
\le
r\sum_\ell|\theta_\ell|.
\]

Therefore:

## Theorem V-A — sparse phase positivity

If

\[
\boxed{
r\sum_\ell|\theta_\ell|<\frac{\pi}{2},
}
\tag{V.9}
\]

then every tableau monomial has positive real part.  Conjugation symmetry makes the
whole Schur polynomial real, hence

\[
\boxed{
D_{r,k}>0.
}
\tag{V.10}
\]

This is a sparse angular version of a sector-stability principle.

---

# Round 8 — Single-pair detection-delay theorem

If precisely one conjugate pair has angular defect \(\theta\), while every other zero
parameter is positive real, then V-A gives

\[
\boxed{
r|\theta|<\frac{\pi}{2}
\quad\Longrightarrow\quad
D_{r,k}>0
\quad\text{for every }k.
}
\tag{V.11}
\]

Thus any Toeplitz minor capable of detecting that pair must have order at least

\[
\boxed{
r\ge\frac{\pi}{2|\theta|}.
}
\tag{V.12}
\]

As an off-axis pair approaches the negative real axis, the required detecting order
diverges.

This is an exact quantitative explanation for the escape-to-infinity phenomenon.

---

# Round 9 — Refined top-\(k\) angular budget

The bound in V-A can be sharpened.

A tableau of shape \((r^k)\) has total degree \(rk\), and no variable exponent exceeds
\(r\).  If the angular defects are sorted
\[
\vartheta_1\ge\vartheta_2\ge\cdots\ge0,
\]
then the largest possible total monomial phase is obtained by assigning exponent \(r\)
to the \(k\) largest defects.

Hence

\[
\boxed{
|\arg(\text{monomial})|
\le
r\sum_{j=1}^{k}\vartheta_j.
}
\tag{V.13}
\]

Therefore

\[
\boxed{
r\sum_{j=1}^{k}\vartheta_j<\frac{\pi}{2}
\quad\Longrightarrow\quad
D_{r,k}>0.
}
\tag{V.14}
\]

This gives a two-parameter angular positivity region adapted to the rectangular minor
itself.

It also shows exactly why finite verified-zero information cannot close RH: once
\(r,k\to\infty\), the relevant angular budget samples an unbounded portion of the zero
set.

---

# Round 10 — Terminal close attempt

The strongest possible synthesis of the harmonic and Schur sides is now:

### Harmonic side
The logarithmic heat velocity is adaptive harmonic, but the operator cannot see an
\(rk\) mode.

### Schur side
In the PF phase, tail zero motion is diluted:
\[
p_j\le1/k.
\]
Thus asymptotically matching zero locations force only \(o(rk)\) changes in normalized
determinant free energy.

### Collision side
Sign, however, is more delicate than free energy.  A single conjugate pair with tiny
angle can remain invisible until
\[
r\asymp|\theta|^{-1}.
\]

Therefore:

**Kill:** an \(o(rk)\) free-energy estimate is not enough to preserve total
positivity.

The surviving gap is a phase-control theorem, not a magnitude-control theorem.

---

# Terminal candidate V-B — Collision-Angle No-Escape Theorem

Let \(t_*\) be a hypothetical positive de Bruijn–Newman threshold and let the zero
parameters just below \(t_*\) have angular defects
\[
\vartheta_1(t)\ge\vartheta_2(t)\ge\cdots.
\]

Prove that for every \(t>0\) and every rectangular scale \((r,k)\),

\[
\boxed{
r\sum_{j=1}^{k}\vartheta_j(t)<\frac{\pi}{2}.
}
\tag{V.15}
\]

Then every consecutive minor is positive by V.14, giving PF-infinity at \(t\), hence
\[
\Lambda\le0.
\]

Combined with Rodgers–Tao,
\[
\Lambda\ge0,
\]
this would give
\[
\Lambda=0
\]
and RH.

**V-B is unproved.**

In this raw form it is intentionally recognized as being very close to the original
angular content of RH.  The value of Encirclement V is that it identifies the exact
finite-dimensional quantity that must be controlled:
\[
\boxed{
r\sum_{j=1}^{k}\vartheta_j.
}
\]

The next useful attack must derive a nontrivial bound on this quantity from heat-flow
dynamics, zero density, or pair-correlation information.  Re-proving only magnitude
or free-energy control will not close the problem.

---

# Ten-round court ledger

## Exact / banked in-session

- reciprocal nonlinear heat equation V.1;
- universal bilinear harmonic mode V.2;
- PF-phase rectangular Schur representation V.3;
- occupancy cap V.4–V.6;
- Schur distortion theorem V.7–V.8;
- sparse phase positivity V.9–V.10;
- single-pair detection delay V.11–V.12;
- top-\(k\) angular budget V.13–V.14.

## Killed

- generic reversible-walk/Dirichlet-energy close;
- dual coordinate obeys the same linear heat equation;
- polynomial-growth Phragmén–Lindelöf without excluding \(rk\);
- free-energy \(o(rk)\) control as sufficient for sign preservation.

## External inputs retained

- explicit cubic Toeplitz wedge for the Riemann xi coefficients;
- verified-zero PF order around \(9.4\times10^{12}\);
- de Bruijn–Newman upper bound \(0.2\);
- Rodgers–Tao lower bound \(\Lambda\ge0\);
- real-zero dynamics and Riemann–von Mangoldt scale in the PF phase.

## Live frontier

- derive a genuine upper bound on the top-\(k\) angular defect
  \[
  \sum_{j=1}^{k}\vartheta_j(t)
  \]
  from de Bruijn–Newman dynamics, strong enough to beat \(1/r\) in the critical
  two-scale region.

---

# Final disposition

\[
\boxed{
\textbf{MAJOR REDUCTION / STRICT FRONTIER — RH NOT CLOSED.}
}
\]

The ten faithful rounds did not produce a fake close.  They did produce a sharper
reason the previous no-escape program stops:

> **magnitude is diluted, but phase can still accumulate.**

That is the exact frontier to attack next.
