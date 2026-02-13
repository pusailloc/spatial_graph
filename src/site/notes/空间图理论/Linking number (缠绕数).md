---
{"dg-publish":true,"permalink":"//linking-number/","tags":["math/topology","knot-theory","concept/invariant","paper/nikkuni"]}
---


## 1. 基础设定

在空间图论中，Linking Number 是描述两个 **Vertex-disjoint** Cycles 在 $\mathbb{R}^3$ 中相互纠缠程度的拓扑不变量。

*   **对象**: Link $L = K_1 \cup K_2$，其中 $K_1, K_2$ 是 $\mathbb{R}^3$ 中的定向简单闭曲线。
*   **记号**: $lk(K_1, K_2)$。

## 2. 计算定义 (Diagrammatic)

基于正则投影图（Projection Diagram）的组合计算法。

> [!abstract] 公式
> $$ lk(K_1, K_2) = \frac{1}{2} \sum_{c \in \mathcal{C}(K_1, K_2)} \epsilon(c) $$
> 
> 其中：
> *   $\mathcal{C}(K_1, K_2)$ 是 $K_1$ 和 $K_2$ 之间所有交叉点的集合（不含自交点）。
> *   $\epsilon(c) \in \{+1, -1\}$ 是交叉点 $c$ 的符号。

### 交叉点符号判定 (Sign Convention)

> [!image]- 符号规则
> ![linking number.png](/img/user/%E5%9B%BE%E7%89%87/linking%20number.png)


1.  **Positive (+)**: 按照右手定则，上方线段的方向向量旋转进入下方线段方向。
2.  **Negative (-)**: 反之。

## 3. 几何定义 (Seifert Surface)

基于代数拓扑的同调定义，常见于理论推导。[[空间图理论/Linking Number via Seifert Surface\|定义解释]]

> [!abstract] 定义
> 设 $F_1$ 是以 $K_1$ 为边界的可定向曲面 ($\partial F_1 = K_1$)。
> $$ lk(K_1, K_2) = \text{Int}(K_2, F_1) $$
> 即 $K_2$ 与曲面 $F_1$ 的代数交点数（Signed intersection number）。

## 4. 意义

> [!important] 核心性质
> 1. **整数性**: $lk(K_1, K_2) \in \mathbb{Z}$。
> 2. **对称性**: $lk(K_1, K_2) = lk(K_2, K_1)$。
> 3. **同痕不变性 (Isotopy Invariance)**: 只要 $K_1$ 和 $K_2$ 不相交，连续变形不改变 $lk$ 值。


> [!example] 示例
> *   **Hopf Link**: $lk = \pm 1$ (最简单的非平凡连接)。
> *   **Whitehead Link**: $lk = 0$ (虽然 $lk=0$，但它们是连接在一起的)。
