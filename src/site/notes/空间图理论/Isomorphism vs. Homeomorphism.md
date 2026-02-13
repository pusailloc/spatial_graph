---
{"dg-publish":true,"dg-permalink":"/spatial-graph-theory/isomorphism-vs-homeomorphism/","permalink":"/spatial-graph-theory/isomorphism-vs-homeomorphism/","tags":["math/graph-theory","math/topology","concept/distinction","paper/nikkuni"]}
---


# Concept Distinction: Isomorphism vs. Homeomorphism

在 Nikkuni 的 Lemma 2.2 中，子图 $F_{ij}^{(m)}$ 被描述为 "Not isomorphic to $K_{n-1}$ but homeomorphic to it"。理解这一区别是理解证明逻辑的前提。

## 1. 对比表 (Comparison Table)

| 维度       | **Isomorphism (同构)**             | **Homeomorphism (同胚)**             |     |
| :------- | :------------------------------- | :--------------------------------- | --- |
| **所属领域** | 组合图论 (Combinatorics)             | 拓扑学 (Topology)                     |     |
| **定义核心** | 顶点与边的双射，保邻接性                     | 空间的连续双射，保连通性                       |     |
| **顶点数量** | **必须严格相等** ($V_1=V_2$)           | **不重要** (可以通过细分增加)                 |     |
| **度的约束** | 对应顶点的度数必须相等                      | 不重要 (允许度数为2的节点)                    |     |
| **判定结果** | $F_{ij}^{(m)} \not\cong K_{n-1}$ | $F_{ij}^{(m)} \cong_{top} K_{n-1}$ |     |

## 2. 详细解析

### Why NOT Isomorphic? (组合视角)
*   **顶点数不等**: $K_{n-1}$ 有 $n-1$ 个顶点，而 $F_{ij}^{(m)}$ 有 $n$ 个顶点。这违反了图同构的基本必要条件。
*   **度数不匹配**: $F_{ij}^{(m)}$ 中存在度数为 2 的顶点 $m$ (连接 $i$ 和 $j$)，而 $K_{n-1}$ 是完全图，不存在度数为 2 的点 (除非 $n-1=3$)。

### Why Homeomorphic? (拓扑视角)
*   **视点转换**: 将图视为 **1-complex** (由线段和点组成的空间结构)。
*   **细分 (Subdivision)**: $F_{ij}^{(m)}$ 本质上是在 $K_{n-1}$ 的边 $\overline{ij}$ 上插入了一个点 $m$。
    $$ \text{Edge } \overline{ij} \xrightarrow{\text{insert } m} \text{Path } i-m-j $$
*   **拓扑等价**: 在连续变形下，一条线段和被点分割成的两条线段是无法区分的。因此两者在空间中具有相同的“形状”。

## 3. 证明中的作用 (The "Why")

> [!important] 核心逻辑
> **Linking Number** 是拓扑不变量，而非单纯的图不变量。
> 
> $$ \text{Homeomorphic} \implies \text{Same Linking Properties} $$
> 
>  利用这一点，在计算 $lk^2$ 时，合法地将针对 $K_{n-1}$ 的归纳假设应用到了 $F_{ij}^{(m)}$ 上，尽管它们在图论上并不相等。
