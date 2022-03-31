---
custom_alias: Linear system $A\v{x}=\v{b}$ is consistent $\Leftrightarrow$ $\v{b}\in\colsp\l(A\r)$
---

<br />
<br />

Date Created: 30/03/2022 17:56:16
Tags: #Proposition #Open

Proved by: _Not Applicable_
Generalizations: _Not Applicable_

Examples: _Not Applicable_
Counterexamples: _Not Applicable_

``` ad-Proposition
title: Proposition.

_Let $K$ be a field and consider the $\l(m\times n\r)$-linear system_
$$\begin{equation}
    A\v{x}=\v{b}\ \ \ \ \Leftrightarrow\ \ \ \ \l\{\begin{alignedat}{7}
        &a_{11}x_1&&\,+&&\,\cdots\,&&\,+\,&&a_{1n}x_n&&=\ &&b_1\\
        &\vdotswithin{a_{11}x_1}&&&&&&&&\vdotswithin{a_{1n}x_n}&&&&\vdotswithin{b_1}\\
        &a_{m1}x_1&&\,+\,&&\,\cdots\,&&\,+\,&&a_{mn}x_n&&=&&b_m
    \end{alignedat}\r.
\end{equation}$$
_of equations over $K$. Then $A\v{x}=\v{b}$ is consistent iff $\v{b}\in\colsp\l(A\r)$._

```

_Proof_. For all $j\in\l\{1,\dots,n\r\}$, let $\v{a}_j\coloneqq\l[a_{ij}\ \ \cdots\ \ a_{mj}\r]^\trans$ be the columns of $A$. Observe that the linear system can be written as a vector equation as follows:
$$\begin{equation}
    \begin{aligned}
        \v{b}&=\l[\sum_{j=1}^na_{ij}x_j\r]_{i\in\l\{1,\dots,m\r\}} && \textrm{Definition of matrix multiplication} \\
        &=\l[\sum_{j=1}^na_{1j}x_j\ \ \cdots\ \ \sum_{j-1}^na_{mj}x_j\r]^\trans && \textrm{Notation; transpose} \\
        &=\sum_{j=1}^n\l[a_{1j}x_j\ \ \cdots\ \ a_{mj}x_j\r]^\trans && \textrm{Definition of matrix addition} \\
        &=\sum_{j=1}^nx_j\l[a_{1j}\ \ \cdots\ a_{mj}\r]^\trans && \textrm{Definition of scalar(-matrix) multiplication} \\
        &=\sum_{j=1}^nx_j\v{a}_j. && \textrm{Definition of $\v{a}_j$}
    \end{aligned}
\end{equation}$$
It follows then that $A\v{x}=\v{b}$ is consistent with (at least a) solution $\v{s}\coloneqq\l\langle s_1,\dots,s_n\r\rangle$ iff $\v{b}$ is a linear combination
$$\begin{equation}
    \v{b}=\sum_{j=1}^ns_j\v{a}_j;
\end{equation}$$
that is, iff $\v{b}\in\colsp\l(A\r)$.<span style="float:right;">$\blacksquare$</span>