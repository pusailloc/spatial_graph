---
{"dg-publish":true,"permalink":"//introduction/"}
---


## 一: 定义
### 1. 基础定义

**范畴设定**：本文在分段线性范畴 (Piecewise Linear Category) 下讨论。

*   **空间嵌入 (Spatial Embedding)**
    *   定义：一个有限图 $G$ 到 3-球面 ($S^3$) 的嵌入 $f$。
    *   记号：$G$ 的所有空间嵌入的集合记为 $SE(G)$。

*   **空间图 (Spatial Graph)**
    *   定义：空间嵌入的像 $f(G)$。

*   **周围同痕（合痕） (Ambient Isotopic)**
    *   定义：对于两个空间图 $f(G)$ 和 $g(G)$，如果存在 3-球面的保定向自同胚 (orientation-preserving self-homeomorphism) $\Phi$，使得 $\Phi(f(G)) = g(G)$，则称它们是周围同痕的。
    *   记号：$f(G) \cong g(G)$。

*   **圈 (Cycle) 与 $p$-圈 ($p$-cycle)**
    *   定义：$G$ 中同胚于圆的子图称为 **圈 (Cycle)**。包含恰好 $p$ 个顶点的圈称为 **$p$-圈 ($p$-cycle)**。

### 2. 圈对与链环 

*   **不相交圈对集合 (Set of pairs of disjoint cycles)**
    *   $\Gamma^{(2)}(G)$：$G$ 中所有不相交圈对的集合。
    *   $\Gamma_{p,q}(G)$：$\Gamma^{(2)}(G)$ 的子集，由所有包含一个 $p$-圈和一个 $q$-圈的对组成。
    *   **(p, q)-圈对 ((p, q)-pair of cycles)**：$\Gamma_{p,q}(G)$ 中的元素。

*   **构造成分 2-分支链环 (Constituent 2-component link)**
    *   定义：对于 $\Gamma^{(2)}(G)$ 中的元素 $\lambda$ 和 $SE(G)$ 中的元素 $f$，称 $f(\lambda)$ 为 $f(G)$ 的构造成分 2-分支链环。
    *   **类型 (p, q) (Type (p, q))**：如果 $\lambda$ 是一个 $(p, q)$-圈对，则称 $f(\lambda)$ 的类型为 $(p, q)$。

*   **哈密顿圈对 (Hamiltonian pair of cycles)**
    *   定义：如果 $\lambda$ 包含 $G$ 的**所有**顶点，则称 $\lambda$ 为哈密顿圈对。
    *   对应链环：此时 $f(\lambda)$ 称为 $f(G)$ 的 **2-分支哈密顿链环 (2-component Hamiltonian link)**。

### 3. 内蕴性质

*   **内蕴链 (Intrinsically Linked)**
    *   定义：如果对于 $G$ 的**任意**空间嵌入 $f \in SE(G)$，都存在一个 $\Gamma^{(2)}(G)$ 中的元素 $\lambda$，使得 $f(\lambda)$ 是一个不可分离的 (nonsplittable) 2-分支链环，则称图 $G$ 是内蕴链的。

### 4. 链集与极小性 

*   **链集 (Linked Set)**
    *   对于图 $G$ 的不相交圈对集合 $\Lambda(G)$，如果对于 $G$ 的**任意**空间嵌入 (spatial embedding) $f$，都存在 $\Lambda(G)$ 中的一个元素 $\lambda$，使得 $f(\lambda)$ 是一个不可分离的 2-分支链环 (nonsplittable 2-component link)，则称 $\Lambda(G)$ 是 **Linked (链系的/链接的)**。
*   **极小链 (Minimally Linked)**
    *   如果 $\Lambda(G)$ 的任何**真子集 (proper subset)** 都不是 Linked 的，则称 $\Lambda(G)$ 是 **Minimally Linked (极小链系的)**。

### 5. 边收缩与子式

*   **边收缩 (Edge Contraction)**
    *   定义：将图中的一条非环边 $e$ 收缩为一个新顶点 $v$ 的操作（如图 1 所示）。
*   **顶点分裂 (Vertex Splitting)**
    *   定义：边收缩的逆操作。
*   **拓扑平凡 (Topologically Trivial)**
    *   定义：如果边收缩（或顶点分裂）不改变图的拓扑类型，则称其为拓扑平凡的。
    *   条件：这通常等价于边 $e$ 的两个端点中至少有一个度数 (degree) 为 2。
*   **子式 (Minor)**
    *   定义：如果图 $H$ 可以从 $G$ 的子图 $G'$ 通过有限次边收缩得到，则称 $H$ 是 $G$ 的 **子式 (Minor)**
    *   **真子式 (Proper Minor)**：如果 $H \neq G$，则称 $H$ 为 $G$ 的真子式。

*   **子式极小内蕴链图 (Minor-minimal intrinsically linked graph)**
    *   定义：如果一个内蕴链图 $G$ 的所有真子式都不是内蕴链的，则称 $G$ 是子式极小内蕴链图。
    
## 二: 结论

#### 结论 (1)：全圈对集合的极小性与 Petersen 族
> [! notes] 
> 图 $G$ 的**所有**不相交圈对的集合（即 $\Gamma^{(2)}(G)$）是 **极小链 (Minimally Linked)** 的
> 当且仅当 :
> 图 $G$ 本质上等同于 **Petersen 族 (Petersen family)** 中的一个图。

#### 结论 (2)：完全图中的哈密顿极小链集
> [! notes] 
> 对于任意两个整数 $p, q \ge 3$，在完全图 $K_{p+q}$ 中：
> 存在一个由 **哈密顿 $(p, q)$-圈对 (Hamiltonian (p, q)-pairs of cycles)** 组成的 **极小链 (Minimally Linked)** 集合。
> 且该集合的大小 **至多为 18 个元素 (at most 18 elements)**。

## 三: 背景
研究背景与动机
1.  **Conway-Gordon / Sachs**: $K_6$ 包含 nonsplittable $(3,3)$-link。
2.  **Extension**: $K_n (n \ge 7)$ 包含 $K_6$，故也包含 Link。
3.  **Theorem 1.1 ([[空间图理论/主要结果即应用#4.应用\|also known]])**:
    对于任意 $p, q \ge 3$，在 $K_{p+q}$ 的任意空间嵌入中，都存在非平凡的 **Hamiltonian $(p,q)$-link**。
    $$ \implies \Gamma_{p,q}(K_{p+q}) \text{ is a Linked set.} $$
虽然 $\Gamma_{p,q}(K_{p+q})$ 是 Linked Set，但它太大了。
> "Our purpose... is to ensure that we capture a nonsplittable Hamiltonian link... by the image of a **smaller family**."

目标是寻找 **Minimally Linked** 的子集，其大小是常数级的 (at most 18)，而非随 $n$ 阶乘增长。
为了应对 $n$ 增大时圈对数量激增的问题，本文旨在寻找**极小链集 (Minimally Linked Set)**。

> [!important] Proposition 1.2 
> 设 $\Lambda(G)$ 是 $\Gamma^{(2)}(G)$ 的一个 **Linked** 子集。
> $\Lambda(G)$ 是 **极小链 (minimally linked)** 的，当且仅当 (if and only if)：
>
> 对于 $\Lambda(G)$ 中的**任意**元素 $\lambda$，都存在一个 $G$ 的空间嵌入 $f_\lambda \in SE(G)$ 满足以下两个条件：
> 1.  $f_\lambda(\lambda)$ 是一个 **不可分离链环 (nonsplittable link)**；
> 2.  对于 $\Lambda(G) \setminus \{\lambda\}$ 中的**任意**元素 $\lambda'$，$f_\lambda(\lambda')$ 都是一个 **分离链环 (split link)**。
>
> **直观理解**：集合中的每一个圈对 $\lambda$ 都是“必不可少”的。如果去掉 $\lambda$，剩下的集合就不再能保证捕捉到链环了（因为存在 $f_\lambda$ 让剩下的都断开）。

> [!important] Proposition 1.2
> $\Lambda(G)$ is minimally linked  $\iff$  $\forall \lambda \in \Lambda(G)$,   $\exists f_\lambda \in SE(G)$ such that   $f_\lambda(\lambda)$ is nonsplittable, but   $f_\lambda(\lambda')$ is split for all $\lambda' \in \Lambda(G) \setminus \{\lambda\}$.

## 四: 图形

> [!important] The Petersen Family (Petersen 族)
> 这是一个已知的经典结果：
> 所有的 **子式极小内蕴链图** 恰好构成了 **Petersen Family**。
>
> **成员 (共 7 个，见 Fig. 2)**：
> *   $K_6$ (完全图)
> *   $Q_7, Q_8$
> *   $P_7, P_8, P_9, P_{10}$
>
> **重要性质**：对于内蕴链图 $G$，其“全圈对集合 $\Gamma^{(2)}(G)$ 的极小性”与“图 $G$ 本身的子式极小性”是等价的（这将在 Theorem 1.3 中证明）。

> [!image]- Figure 2: The Petersen Family
> ![Pasted image 20260206113736.png](/img/user/%E5%9B%BE%E7%89%87/Pasted%20image%2020260206113736.png)
> *   第一排 (Top): $K_6$ (6点完全连接), $Q_7$ (7点), $Q_8$ (8点)。
> *   第二排 (Bottom): $P_7$, $P_8$, $P_9$, $P_{10}$ (Petersen Graph, 10点, 内外五边形互连)。
> *   这些图展示了从完全图结构向稀疏图结构（彼得森图）的演变过程。

为了在完全图中捕捉特定类型的哈密顿链环，本文特别引入了以下三个图（见 Fig. 3）：

*   **$G_8$**：用于构建 $(p, 3)$-pairs (针对 $K_{p+3}$)。
*   **$G_9$**：用于构建 $(p, 4)$-pairs (针对 $K_{p+4}$)。
*   **$G_{10}$**：用于构建 $(p, q)$-pairs (针对 $K_{p+q}$)。

>[! notes]- Figure 3
>![Pasted image 20260213103248.png](/img/user/%E5%9B%BE%E7%89%87/Pasted%20image%2020260213103248.png)

## 五: 定理

首先关于“全圈对集合”的分类定理，将其与著名的 Petersen 族联系起来。

> [!abstract] Theorem 1.3
> 设 $G$ 是一个没有 0 度或 1 度顶点的图。
> $\Gamma^{(2)}(G)$（即 $G$ 的所有不相交圈对的集合）是 **极小链 (minimally linked)** 的，当且仅当：
> **$G$ 同胚于 Petersen 族 (Petersen family) 中的某一个图。**

为了解决完全图 $K_{p+q}$ 的问题，作者构造了三个特殊的图 $G_8, G_9, G_{10}$（见 Fig. 3），并显式地给出了它们的极小链集。

> [!example]- List of Cycles for $G_8$ (Type 5, 3)
> **Definition of $\Lambda(G_8)$**: The subset of $\Gamma_{5,3}(G_8)$ consisting of the following **12** Hamiltonian pairs:
>
> *   $[1\ 8\ 7\ 2\ 3] \cup [4\ 5\ 6]$, $\quad [1\ 2\ 8\ 7\ 3] \cup [4\ 5\ 6]$, $\quad [1\ 2\ 3\ 8\ 7] \cup [4\ 5\ 6]$
> *   $[1\ 8\ 7\ 2\ 4] \cup [3\ 5\ 6]$, $\quad [1\ 8\ 7\ 2\ 5] \cup [4\ 3\ 6]$, $\quad [1\ 8\ 7\ 2\ 6] \cup [4\ 5\ 3]$
> *   $[6\ 2\ 8\ 7\ 3] \cup [4\ 5\ 1]$, $\quad [5\ 2\ 8\ 7\ 3] \cup [4\ 1\ 6]$, $\quad [4\ 2\ 8\ 7\ 3] \cup [1\ 5\ 6]$
> *   $[1\ 4\ 3\ 8\ 7] \cup [2\ 5\ 6]$, $\quad [1\ 5\ 3\ 8\ 7] \cup [4\ 2\ 6]$, $\quad [1\ 6\ 3\ 8\ 7] \cup [4\ 5\ 2]$

> [!example]- List of Cycles for $G_9$ (Type 5, 4)
> **Definition of $\Lambda(G_9)$**: The subset of $\Gamma_{5,4}(G_9)$ consisting of the following **9** Hamiltonian pairs:
>
> *   $[1\ 8\ 7\ 2\ 6] \cup [4\ 9\ 5\ 3]$, $\quad [1\ 8\ 7\ 2\ 4] \cup [3\ 5\ 9\ 6]$, $\quad [1\ 8\ 7\ 2\ 5] \cup [4\ 3\ 6\ 9]$
> *   $[6\ 2\ 8\ 7\ 3] \cup [4\ 9\ 5\ 1]$, $\quad [4\ 2\ 8\ 7\ 3] \cup [1\ 5\ 9\ 6]$, $\quad [5\ 2\ 8\ 7\ 3] \cup [4\ 1\ 6\ 9]$
> *   $[1\ 6\ 3\ 8\ 7] \cup [4\ 9\ 5\ 2]$, $\quad [1\ 4\ 3\ 8\ 7] \cup [2\ 5\ 9\ 6]$, $\quad [1\ 5\ 3\ 8\ 7] \cup [4\ 2\ 6\ 9]$

> [!example]- List of Cycles for $G_{10}$ (Type 5, 5)
> **Definition of $\Lambda(G_{10})$**: The subset of $\Gamma_{5,5}(G_{10})$ consisting of the following **18** Hamiltonian pairs:
>
> *   $[1\ 8\ 7\ 2\ 3] \cup [4\ 10\ 9\ 5\ 6]$, $\quad [1\ 8\ 7\ 2\ 3] \cup [4\ 5\ 10\ 9\ 6]$, $\quad [1\ 8\ 7\ 2\ 3] \cup [4\ 5\ 6\ 10\ 9]$
> ......

它们的应用：

> [!important] Theorem 1.4
> Let $G$ be one of the graphs $G_8, G_9, G_{10}$. Then $\Lambda(G)$ (as defined above) is **minimally linked**.

在完全图中的应用：利用上述构造，我们可以用**极少量**的特定圈对，捕捉完全图 $K_{p+q}$ 中的哈密顿链。

> [!success] Theorem 1.5 (Main Application)
>
> 1.  **For $K_{p+3}$ ($p \ge 5$)**:
>     存在一个由 **12 个元素** 组成的 $\Gamma_{p,3}(K_{p+3})$ 的极小链子集。
> 2.  **For $K_{p+4}$ ($p \ge 3$)**:
>     存在一个由 **9 个元素** 组成的 $\Gamma_{p,4}(K_{p+4})$ 的极小链子集。
> 3.  **For $K_{p+q}$ ($p, q \ge 5$)**:
>     存在一个由 **18 个元素** 组成的 $\Gamma_{p,q}(K_{p+q})$ 的极小链子集。

*注：这表明无论 $n$ 多大，我们只需要“埋伏 (lying in ambush)”在至多 18 个特定的哈密顿圈对上，就能捕捉到不可分离链环。