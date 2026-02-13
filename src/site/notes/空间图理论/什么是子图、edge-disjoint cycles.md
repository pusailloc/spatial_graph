---
{"dg-publish":true,"permalink":"//edge-disjoint-cycles/","tags":["math/graph-theory","concept/structure","paper/nikkuni"]}
---


## 1. Subgraph (子图)

> [!abstract] 定义
> 图 $H=(V', E')$ 是图 $G=(V, E)$ 的 **Subgraph**，当且仅当：
> $$ V' \subseteq V \quad \text{and} \quad E' \subseteq E $$
> 且 $E'$ 中的每条边的端点都必须属于 $V'$。

> [!example] 类型区分
> *   **一般子图**: 任意满足上述条件的图。
> *   **Spanning Subgraph (生成子图)**: 满足 $V' = V$ 的子图。即包含原图所有顶点。
>     *   *Link*: [[空间图理论/什么是 cycle,Hamiltonian cycle\|Hamiltonian Cycle]] 是特殊的生成子图。
> *   **Induced Subgraph (导出子图)**: 选定顶点集 $V'$ 后，包含 $G$ 中所有两个端点都在 $V'$ 中的边的子图。

---
## 2. Edge-disjoint Cycles (边不相交圈)

在研究图的分解或空间图的交互作用时，需区分圈的独立性。

> [!abstract] 定义
> 设 $C_1, C_2$ 是图 $G$ 中的两个 Cycle。若满足：
> $$ E(C_1) \cap E(C_2) = \emptyset $$
> 则称 $C_1$ 和 $C_2$ 为 **Edge-disjoint (边不相交)**。

### 辨析：边不相交 vs 顶点不相交

| 属性       | Edge-disjoint (边不相交)             | Vertex-disjoint (顶点不相交/Disjoint) |     |
| :------- | :------------------------------- | :------------------------------- | --- |
| **定义**   | $E(C_1) \cap E(C_2) = \emptyset$ | $V(C_1) \cap V(C_2) = \emptyset$ |     |
| **公共顶点** | **允许**                           | **禁止**                           |     |
| **公共边**  | 禁止                               | 自动禁止 (Implied)                   |     |
| **拓扑形态** | 可能像 "8" 字形或花束                    | 完全分离的两个圆环 (Link)                 |     |
| **应用**   | 图的分解 (Decomposition)             | 环绕数 (Linking Number) 的计算对象       |     |

### 推论
1. **强弱关系**: Vertex-disjoint $\implies$ Edge-disjoint。反之不成立。
2. **Cycle Decomposition**: 如果一个图的每条边都恰好属于某一个圈，则该图可以分解为一组 Edge-disjoint cycles.
