---
mathLink: auto
---

<div class="topSpace"></div>

Date Created: 22/01/2023 22:29:15
Tags: #Theorem #Topics/Ring_Theory #Courses/MATH457

Proved by: [[Irreducible implies prime (UFD)]], [[Basic properties of irreducible and prime elements]], [[Ideal is prime iff quotient is an integral domain]], [[Basic properties of polynomial rings (integral domain)]]
References: _Not Applicable_
Justifications: _Not Applicable_

Specializations: _Not Applicable_
Generalizations: _Not Applicable_

``` ad-Theorem
title: Theorem (Gauss$\textrm{'}$s Lemma for Primitivity of Polynomials).

_Let $R$ be a UFD. For all $f,g\in R\l[x\r]$, we have $\cont\l(fg\r)=\cont\l(f\r)\cont\l(g\r)$._

```

_Proof_. We first show that for all $f'$ and $g'$ primitive, their product $f'g'$ is also primitive. Then, since $f=\alpha f'$ and $g=\beta g'$ for some primitives $f',g'\in R\l[x\r]$ where $\ideal{\alpha}=\cont\l(f\r)$ and $\ideal{\beta}=\cont\l(g\r)$, we see that
$$\begin{equation}
    \cont\l(fg\r)=\cont\l(\alpha\beta f'g'\r)=\alpha\beta\cont\l(f'g'\r)=\alpha\beta\ideal{1}=\ideal{\alpha\beta}=\ideal{\alpha}\ideal{\beta}=\cont\l(f\r)\cont\l(g\r).
\end{equation}$$
Suppose now that $f$ and $g$ are primitive.
* To show that $fg$ is also primitive, we need to show that for all $p\in R$, $p$ does not divide at least one coefficient of $fg$. But $R$ is a UFD, so it suffices to prove this for $p\in R$ prime since every $r\in R\comp R^\times$ can be factored into irreducibles, which are prime in a UFD; we do not need to prove it for units $u\in R^\times$ since contents are defined as GCD _ideals_, which are invariant under units.

Let $p$ be prime in $R$, so $\ideal{p}$ is a prime ideal. Then $\bar{R}\coloneqq R/\ideal{p}$ is an integral domain, and the homomorphism $\phi:R\to\bar{R}:r\mapsto\bar{r}$ mapping $r+\ideal{p}$ extends to a homomorphism
$$\begin{equation}
    \psi:R\l[x\r]\to\bar{R}\l[x\r]\ \ \ \ \ \ \ \ \textrm{mapping}\ \ \ \ \ \ \ \ \sum_{i=0}^{n}r_ix^i\mapsto\sum_{i=0}^{n}\bar{r_i}x^i.
\end{equation}$$
Note that $\psi\l(f\r)\neq0$, for otherwise all the coefficients $\bar{a_i}=a_i+\ideal{p}$ modulo $p$ are $0$, and hence $a_i\in\ideal{p}$ for all $i$. But then $p$ divides all coefficients of $f$, contradicting the assumption that $f$ is primitive. Similarly $\psi\l(g\r)\neq0$, so, since $\bar{R}\l[x\r]$ is an integral domain, we see that $\psi\l(fg\r)=\psi\l(f\r)\psi\l(g\r)\neq0$. Thus $p$ does not divide all coefficients of $fg$, so $fg$ is primitive.<span style="float:right;">$\blacksquare$</span>