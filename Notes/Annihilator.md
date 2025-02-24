---
mathLink-blocks:
    order: Order
---

<div class="topSpace"></div>

Date Created: 28/07/2023 13:37:03
Tags: #Type/Definition #Topic/Module_Theory

Types: <i>Not Applicable</i>
Examples: [[Cayley-Hamilton Theorem#^minimal-polynomial]]
Constructions: <i>Not Applicable</i>
Generalizations: <i>Not Applicable</i>

Properties: <i>Not Applicable</i>
Sufficiencies: <i>Not Applicable</i>
Equivalences: <i>Not Applicable</i>
Justifications: [[Integers#^subgroups-of-integers]]

``` ad-Definition
title: Definition.

Let $X\subseteq M$ be a subset of an $R$-module $M$. The <b>annihilator of $X$</b> is $\Ann X\coloneqq\l\{r\in R\st rX=0\r\}$.

```

<b>Remark.</b> Note that $\Ann M\nsubgrpeq R$ is an ideal. If $M$ is finitely-generated over an integral domain $R$, then $M$ is torsion iff $\Ann M\neq\l\{0\r\}$. Indeed, the product of the non-zero annihilators of the generating elements of $M$ is in $\Ann M$, and is non-zero since $R$ is an integral domain.<span style="float:right;">$\blacklozenge$</span>

---

<b>Remark.</b> For a PID $R$ and a singleton $\l\{x\r\}\subseteq R$, we call $\ord x\coloneqq\Ann x$ the <b>order of $x$</b>. This generalizes the notion of the order of a group element. Indeed, consider the homomorphism $\phi:R\to M$ mapping $r\mapsto rx$, whose kernel is generated by $\gen{a}$ for some $a\in R$. Then $\ord x=\Ann x=\ker\phi=\gen{a}$, so, for $\Z$-modules, we see that $\ord x=m\Z$ for some $m\in\Z$. This integer is the order of $x$ as an abelian group.
^order
* As in $\catgrp$, if $f:M\to N$ is an $R$-module homomorphism, then $\ord x\subseteq\ord f\l(x\r)$. Indeed, if $r\in\ord x$, then $rf\l(x\r)=f\l(rx\r)=0$ and so $r\in\ord f\l(x\r)$.<span style="float:right;">$\blacklozenge$</span>
