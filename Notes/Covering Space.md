---
mathLink: auto
---

<div class="topSpace"></div>

Date Created: 18/05/2023 00:45:42
Tags: #Type/Definition #Topic/Topology

Types: [[Universal Cover]], [[Normal Cover]]
Examples: _Not Applicable_
Constructions: [[Covering Space Isomorphism]], [[Category of Covering Maps]]
Generalizations: _Not Applicable_

Properties: [[Covering Homotopy Theorem]], [[Basic properties of covering spaces]], [[Independence of base point]]
Sufficiencies: _Not Applicable_
Equivalences: [[Galois Correspondence of Covering Spaces]]
Justifications: [[Connected implies well-defined number of sheets]]

``` ad-Definition
title: Definition.

_Let $X$ be a topological space. A **covering map of $X$** is a continuous map $p:\widetilde{X}\to X$ from a path-connected space $\widetilde{X}$ such that for all $x_0\in X$, there exists a neighborhood $U$ of $x_0$ in $X$ where_ $p^{-1}\!\l(U\r)=\coprod_{i\in I}V_i$ _for some disjoint open sets $V_i$ of $\widetilde{X}$ and where each_ $\l.p\r|_{V_i}:V_i\to U$ _is a homeomorphism._
* _If $p:\widetilde{X}\to X$ is a covering map, then $\widetilde{X}$ is said to be a **covering space of $X$**, the neighborhood $U$ is said to be **evenly-covered** by the **sheets** $V_i\subseteq\widetilde{X}$._
* _The cardinality $n\coloneqq\l|p^{-1}\!\l(x_0\r)\r|$ is independent of $x_0$ and is said to be the **number of sheets of $p$**. We say that $p$ is an **$n$-sheeted covering**._
* _The **monodromy action of $\pi_1\l(X,x_0\r)$ on fibers** is the action $\phi:\pi_1\l(X,x_0\r)\to\Aut\!\l(p^{-1}\!\l(x_0\r)\r)\!$ given by $\l[\gamma\r]\cdot\widetilde{x}\coloneqq\widetilde{\gamma}\l(0\r)$ where $\widetilde{\gamma}$ is the lift of $\gamma$ ending at $\widetilde{x}$._

```

**Remark.** Covering maps are stronger than fibrations in the sense that the lifting is unique. We have the following unique lifting properties.
* For each path $\gamma:I\to X$ starting at some point $x_0\in X$ and each $\widetilde{x}_0\in p^{-1}\!\l(x_0\r)$ there exists a unique path $\widetilde{\gamma}:I\to\widetilde{E}$ starting at $\widetilde{x}_0$ lifting $\gamma$.
* For each homotopy $\gamma_t:I\to X$ of paths and each lift $\widetilde{\gamma}_0:I\to\widetilde{X}$ of $\gamma_0$, there exists a unique homotopy $\widetilde{\gamma}_t:I\to\widetilde{X}$ of paths lifting $\gamma_t$.

The resulting homotopy $\widetilde{\gamma}_t$ is a homotopy _of paths_ since as $t$ varies, the endpoints $\widetilde{\gamma}_t\!\l(0\r)$ and $\widetilde{\gamma}_t\!\l(1\r)$ are curves in $\widetilde{X}$ that lift the constant curves at $\gamma_t\!\l(0\r)$ and $\gamma_t\!\l(1\r)$, respectively. By uniqueness of liftings of paths, we see that $\widetilde{\gamma}_t\!\l(0\r)$ and $\widetilde{\gamma}_t\!\l(1\r)$ are constant curves at the lifts of $\gamma_t\!\l(0\r)$ and $\gamma_t\!\l(1\r)$, respectively, as desired.<span style="float:right;">$\blacklozenge$</span>

---

**Remark.** We define covering spaces to be path-connected. If not, we can always restrict to path-components. This implies that $X$ is path-connected too. Also, note that any local property of $X$ is inherited by $\widetilde{X}$. In particular, if $X$ is locally path-connected, then so is $\widetilde{X}$.<span style="float:right;">$\blacklozenge$</span>