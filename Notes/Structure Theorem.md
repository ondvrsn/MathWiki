<div class="topSpace"></div>

Date Created: 23/07/2023 20:35:54
Tags: #Type/Theorem #Topic/Module_Theory

Proved by: [[Characterizations of PIDs#^torsion-free-iff-free]], [[Free Module#^universal-property-of-free-modules]], [[Basic properties of rank]], [[Splitting Lemma]], [[Characterization of UFDs#^pid-implies-ufd]], [[Bezout's Identity]], [[Isomorphism Theorems]], [[Chinese Remainder Theorem]]
References: <i>Not Applicable</i>
Justifications: <i>Not Applicable</i>

Specializations: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

``` ad-Theorem
title: Theorem (Structure Theorem for Finitely-generated Modules over PIDs).

Let $M$ be a finitely-generated module over a PID $R$. Then we have a decomposition $M\iso R^{\rk M}\oplus\Tor M$, and furthermore:
* (Elementary Divisors). There exist distinct prime ideals $\gen{p_i}\nsubgrp R$ and positive integers $\alpha_{ij}\in\N$ such that $\Tor M\iso\bigoplus_{i=1}^n\bigoplus_{j=1}^mR/\langle p_i^{\alpha_{ij}}\rangle$.
* (Invariant Factors). There exist an ascending chain $\gen{a_1}\supseteq\gen{a_2}\supseteq\cdots\supseteq\gen{a_m}$ of non-zero ideals $\gen{a_j}\nsubgrp R$ such that $\Tor M\iso\bigoplus_{j=1}^mR/\!\gen{a_j}$.

Both decompositions of $\Tor M$ are unique up to a permutation of the factors.

```

<b>Remark.</b> Taking $R\coloneqq\Z$ gives us the <i>Structure Theorem for Finitely-generated Abelian Groups</i>.<span style="float:right;">$\blacklozenge$</span>

---

<i>Proof.</i> We claim that the exact sequence $0\to\Tor M\to M\to M/\Tor M\to 0$ splits. Indeed, since $M/\Tor M$ is torsion-free and $R$ is a PID, we see that $M/\Tor M$ is free so $\pi:M\onto M/\Tor M$ admits a splitting $\phi:M/\Tor M\to M$ mapping the basis elements $e_i\mapsto m_i\in\pi^{-1}\!\l(e_i\r)\in M$. Since $\rk\l(M/\Tor M\r)=\rk M$, we obtain the desired torsion decomposition $M\iso R^{\rk M}\oplus\Tor M$. Henceforth, we assume w.l.o.g. that $M=\Tor M$; its decomposition will proceed in several steps.
1. <i>Primary Decomposition.</i> We first prove that $M\iso\bigoplus_\mf{p}M\l(\mf{p}\r)$, where $M\l(\mf{p}\r)\coloneqq\l\{m\in M\st\ex\alpha\in\N:p^\alpha m=0\r\}$ for each prime ideal $\mf{p}\coloneqq\gen{p}\nsubgrp R$.
2. <i>Elementary Divisors.</i> Next, for each $\mf{p}\coloneqq\gen{p}$, we show that $M\l(\mf{p}\r)\iso\bigoplus_{j=1}^mR/\!\gen{p^{\alpha_j}}$ for some unique $m\in\N$ and unique positive integers $\alpha_1\leq\cdots\leq\alpha_m$.
3. <i>Invariant Factors.</i> Finally, we combine the primes into a unique ascending chain of non-zero ideals $\gen{a_j}\nsubgrp R$, giving us the invariant factors decomposition of $M$.

---

<i>Primary Decomposition.</i> For all $a\in R$, let $M_a$ denote the kernel of the endomorphism $m\mapsto am$. Since $M$ is torsion, we see that $\Ann M\neq\l\{0\r\}$ and so there is some $a\in R$ such that $M_a=M$. Since $R$ is also a UFD, write $a=u\prod_{i=1}^{n}p_i^{\alpha_i}$, and set $b\coloneqq p_1^{\alpha_1}$ and $c\coloneqq a/b$. We claim that $M=M_b\oplus M_c$, from which the result follows by induction.
* Since $b\perp c$, Bézout’s Identity furnishes $r,s\in R$ so that $rb+sc=1$. Take $m\in M$, so $m=rbm+scm$. Then $c\l(rbm\r)=arm=0$ and $b\l(scm\r)=asm=0$, so $m\in M_b+M_c$. Furthermore, if $bm=cm=0$, then $m=rbm+scm=0$.

---

<i>Elementary Divisors.</i> For ease of notation, assume w.l.o.g. that $M=M\l(\mf{p}\r)$. Write $M=\gen{x_j}_{j=1}^m$ for some $m\in\N$ and $x_j\in M$. Let $\alpha\in\N$ be the smallest integer so that $p^\alpha M=0$ and let $x\in M$ have order $\gen{p^\alpha}$. Set $\bar{M}\coloneqq M/\!\gen{x}$ and consider the exact sequence $0\to\gen{x}\to M\to\bar{M}\to0$. We need the following lemma.
* If $\bar{y}\in\bar{M}$ has order $\gen{p^\beta}$ for some $\beta\in\N$, then it admits a representative $y\in M$ having the same order. Indeed, let $z\in\pi^{-1}\!\l(\bar{y}\r)$, so $\pi\l(p^\beta z\r)=p^\beta\pi\l(z\r)=p^\beta\bar{y}=0$ and hence $p^\beta z\in\gen{x}$. Thus $p^\beta z=rx$ for some $r\in R$. Observe that $0=p^\alpha z=p^{\alpha-\beta}rx$, so, since $\ord x=\gen{p^\alpha}$, we have $r=p^\beta s$ for some $s\in R$. Set $y\coloneqq z-sx$, which projects onto $\bar{y}$. Its order is $\gen{p^\beta}$ since $p^\beta y=p^\beta z-p^\beta sx=rx-rx=0$ and $\ord y\subseteq\ord\pi\l(y\r)=\gen{p^\beta}$.

We now prove that $M\iso\bigoplus_{j=1}^{m}R/\!\gen{p^{\alpha_j}}$ by induction. If $m=1$, then $M=\gen{x_1}$ is cyclic and we are done. In general, assume w.l.o.g. that $\ord x_m=\gen{p^\alpha}$. Then $\bar{M}\coloneqq M/\!\gen{x_m}$ is generated by $\gen{x_j}_{j=1}^{m-1}$, so it admits a decomposition $\bar{M}\iso\bigoplus_{j=1}^{m-1}R/\!\gen{p^{\alpha_j}}$ for positive integers $\alpha_1\leq\cdots\leq\alpha_{m-1}$. For each $1\leq j\leq m-1$, the module $R/\!\gen{p^{\alpha_j}}$ is cyclic and hence can be generated by some $\bar{y}_j$ of order $\gen{p^{\alpha_j}}$. The above lemma then furnishes representatives $y_j$ of $\bar{y_j}$ having the same order, where we have $\gen{y_j}\iso R/\!\gen{p^{\alpha_j}}$ since the map $R\to\gen{y_j}:r\mapsto ry_j$ is surjective with kernel $\ord y_j=\gen{p^{\alpha_j}}$. This induces an isomorphism $\psi:\bar{M}\to\bigoplus_{j=1}^{m-1}\gen{y_j}$ such that $\pi\circ\psi=\id$, so the exact sequence $0\to\gen{x_m}\to M\to\bar{M}\to0$ splits and gives us the desired isomorphism $M\iso\gen{x_m}\oplus\bigoplus_{j=1}^{m-1}R/\!\gen{p^{\alpha_j}}\iso\bigoplus_{j=1}^mR/\!\gen{p^{\alpha_j}}$ with $\alpha_m\coloneqq\alpha$.
* To show uniqueness, take $k\in\N$ and consider the quotient $p^kM/p^{k+1}M$ as an $R/\mf{p}$-vector space. Restricting to each factor $N_j\coloneqq R/\!\gen{p^{\alpha_j}}$ and observing that
$$\begin{equation}
    p^kN_j/p^{k+1}N_j\iso\frac{p^kR}{p^{\alpha_j}R}\bigg{/}\frac{p^{k+1}R}{p^{\alpha_j}R}\iso
    \begin{dcases}
        R/\mf{p} & \textrm{if }\alpha_j>k \\
        \l\{0\r\} & \textrm{else}
    \end{dcases}
\end{equation}$$
shows that the dimension of $p^kM/p^{k+1}M$ is the number of $\alpha_j$’s greater than $k$. But these dimensions are invariants of $M$, so the number of $\alpha_j$’s greater than $k$ for any fixed $k$ is uniquely determined by $M$, as desired.

---

<i>Invariant Factors.</i> Finally, we use the Chinese Remainder Theorem to combine terms in the elementary divisors decomposition to obtain the invariant factors as
$$\begin{equation}
    M\iso\bigoplus_{i=1}^{n}\bigoplus_{j=1}^{m}R/\!\gen{p_i^{\alpha_{ij}}}=\bigoplus_{j=1}^{m}\l(\bigoplus_{i=1}^{n}R/\!\gen{p_i^{\alpha_{ij}}}\r)\iso\bigoplus_{j=1}^{m}R/\!\gen{a_j},
\end{equation}$$
where $a_j\coloneqq\prod_{i=1}^{n}p_i^{\alpha_{ij}}$. Since $\alpha_{ij}$ increases for each fixed $i$, we see that $a_1\divides\cdots\divides a_m$ and hence we obtain an ascending chain $\gen{a_1}\supseteq\gen{a_2}\supseteq\cdots\supseteq\gen{a_m}$ of non-zero ideals $\gen{a_j}\nsubgrp R$. As for uniqueness, suppose $b_1\divides\cdots\divides b_{m'}$ is another set of invariant factors of $M$. Then $a_m$ and $b_{m'}$ are both the product of the largest prime powers of the elementary divisors of $M$, so they coincide and the result follows by induction.<span style="float:right;">$\blacksquare$</span>
