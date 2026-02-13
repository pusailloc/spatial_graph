---
{"dg-publish":true,"dg-permalink":"/spatial-graph-theory/topological-invariants/","permalink":"/spatial-graph-theory/topological-invariants/","tags":["math/topology","knot-theory","concept/invariant","paper/conway-gordon","paper/adams-knot-book"]}
---

## 1. Linking Number 

### Integer vs. Mod 2

| 特性        | Integer Linking Number ($lk \in \mathbb{Z}$) | Mod 2 Linking Number ($lk \in \mathbb{Z}_2$) |
| :-------- | :------------------------------------------- | :------------------------------------------- |
| **定义**    | 交叉点符号的代数和 (Signed sum)                       | 代数和的奇偶性 (Parity)                             |
| **定向敏感性** | **敏感** (改变方向会导致变号)                           | **不敏感** ($x \equiv -x \pmod 2$)              |
| **信息量**   | 高 (包含缠绕方向和圈数)                                | 低 (仅包含“是否奇数次缠绕”)                             |
| **应用场景**  | 精细分类 (Integral Lifting)                      | 存在性证明 (CGS Theorem regarding $K_6$)          |

> [!important] 为什么 $K_6$ 定理使用 Mod 2?
> 完全图 $K_6$ 通常被视为无向图。如果我们使用整数 $lk$，必须人为给每个三角形指定方向，这会导致结果依赖于选择。使用 Mod 2 则消除这种歧义，使 $\sum lk \pmod 2$ 成为图本身的内蕴性质。

---

## 2. Arf Invariant (Arf 不变量)

Arf 不变量是 **Knots (纽结)** 的一种二值不变量，常用于检测结的存在性。

> [!abstract] 定义
> Arf 不变量是一个映射函数：
> $$ \text{Arf}: \{ \text{Knots in } \mathbb{R}^3 \} \to \{0, 1\} $$

### 性质

1.  **Detection (探测能力)**:
    *   若 $\text{Arf}(K) = 1 \implies K$ is a **Non-trivial Knot**.
    *   若 $\text{Arf}(K) = 0 \implies K$ is Undetermined (Unknot，也可以是某些 Complex Knots).
2.  **Additivity (加性)**:
    在连通和 (Connected Sum) 运算下：
    $$ \text{Arf}(K_1 \# K_2) \equiv \text{Arf}(K_1) + \text{Arf}(K_2) \pmod 2 $$

### 例子

| Knot Type | Name                    | Arf Value | Conclusion                       |
| :-------- | :---------------------- | :-------- | :------------------------------- |
| $0_1$     | Unknot (平凡结)            | **0**     | Baseline                         |
| $3_1$     | Trefoil Knot (三叶结)      | **1**     | $\implies$ Knotted               |
| $4_1$     | Figure-Eight Knot (8字结) | **1**     | $\implies$ Knotted               |
| $5_1$     | Cinquefoil Knot         | **1**     | $\implies$ Knotted               |
| --        | (Certain Pretzel Knots) | 0         | Can be knotted but Arf invisible |

### 与 CGS 定理的关联

在 $K_7$ 的 Intrinsic Knotting 定理中：
$$ \sum_{\text{Hamiltonian Cycles } H} \text{Arf}(H) \equiv 1 \pmod 2 $$
由于和为 1，必然存在某个 $H$ 使得 $\text{Arf}(H) = 1$。
根据性质 2，该 $H$ 必然是非平凡结。

---