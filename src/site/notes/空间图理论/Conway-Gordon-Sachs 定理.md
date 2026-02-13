---
{"dg-publish":true,"permalink":"//conway-gordon-sachs/","tags":["math/spatial-graph-theory","concept/theorem","paper/conway-gordon"]}
---


# Conway-Gordon-Sachs Theorem

## 1. Intrinsic (内蕴性)
 
 如果图 $G$ 的 **任意** 空间嵌入 $f: G \to \mathbb{R}^3$ 都满足某种拓扑性质 $P$，则称 $G$ 具有 **Intrinsic $P$**。

## 2. Conway-Gordon Theorem (1983)

该定理包含两部分，分别针对 $K_6$ 和 $K_7$。

### Case 1: Intrinsic Linking of $K_6$

> [!important] 定理叙述
> 对于完全图 $K_6$ 的任意空间嵌入，所有 **顶点不相交的三角形对 (Disjoint Triangle Pairs)** 的 Linking Number 之和在模 2 意义下等于 1。
> 
> $$ \sum_{\{(T_1, T_2) | T_1 \cup T_2 \subset K_6, V(T_1)\cap V(T_2)=\emptyset\}} lk(T_1, T_2) \equiv 1 \pmod 2 $$

**逻辑推论**:
*   因为总和为奇数 ($1 \pmod 2$)，所以总和不可能为 0。
*   $\implies$ **至少存在一对** 三角形 $(T_i, T_j)$，使得 $lk(T_i, T_j) \neq 0$。即: Every Spatial Embedding of $K_{6}$ contains a non-trivial link
*   $\implies$ $K_6$ 是 **Intrinsically Linked** 的。

> [!image]- $K_6$ 示意图
> ![Pasted image 20260117161212.png|327](/img/user/%E5%9B%BE%E7%89%87/Pasted%20image%2020260117161212.png)
>存在互锁的一对三角形

### Case 2: Intrinsic Knotting of $K_7$

> [!important] 定理叙述
> 对于完全图 $K_7$ 的任意空间嵌入，其包含的所有 **Hamiltonian Cycles** 的 Arf Invariant 之和在模 2 意义下等于 1。
> 
> $$ \sum_{H \subset K_7} arf(H) \equiv 1 \pmod 2 $$

**逻辑推论**:
*   $\implies$ 至少有一项不为 0**至少存在一个** Hamiltonian Cycle 是非平凡纽结 (Non-trivial Knot)。
   （ 和为奇数 $\implies$ 和不为 0 $\implies$ 至少有一项不为 0 $\implies$ 至少有一个 Hamiltonian cycle $H$ 的 $arf(H) \neq 0$ $\implies$ $H$ 是一个非平凡结。）

*   $\implies$ $K_7$ 是 **Intrinsically Knotted** 的。
---

## 3. 关键逻辑

理解该定理证明思路的三个关键点：

### A. 为什么选择三角形对?
针对 $K_6$ ($|V|=6$)：
*   为了计算 $lk$，需要两个 disjoint cycles。
*   为了穷尽顶点，最优分割是 $3+3$。
*   3个顶点的圈即为 **三角形**。这是 $K_6$ 结构下唯一可能的 disjoint decomposition。

### B. 为什么求和?
单个子图的性质不是拓扑不变量。
*   可以通过连续变形（Isotopy）解开某一对特定的三角形，但这会迫使其他三角形对打结。
*   **求和** 捕捉了这种“按下葫芦浮起瓢”的全局约束。666

### C. 为什么使用 Mod 2?
基于 **Crossing Change (交叉点变换)** 的证明技巧：
1.  将任意复杂的嵌入变形为简单的“标准嵌入”（Trivial embedding），中间经过 $n$ 次交叉变换。
2.  每次交叉变换，$lk$ 值改变 $\pm 1$。
3.  在模 2 算术中，$+1 \equiv -1$。
4.  这使得证明“总和的奇偶性保持不变”在代数上变得非常简洁且强力。
