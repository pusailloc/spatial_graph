---
{"dg-publish":true,"permalink":"//cycle-hamiltonian-cycle/","tags":["math/graph-theory","math/topology","concept/definition","paper/nikkuni"]}
---


## 1. 基础定义体系

明确图 $G=(V, E)$ 中的路径结构 

### Cycle (圈)

> [!abstract] 定义
> **Cycle** 是一个顶点和边互不重复（除首尾外）的闭合路径。
> 
> 形式化表示：
> 设序列 $C = (v_0, e_1, v_1, \dots, e_k, v_k)$，若满足以下条件：
> 1. **闭合性 (Closed)**: $v_0 = v_k$
> 2. **简单性 (Simple)**: $\forall i, j \in \{1, \dots, k\}$, 若 $i \neq j$, 则 $v_i \neq v_j$ (起点 $v_0$ 除外)。
> 
> 则称 $C$ 为一个长度为 $k$ 的圈，记为 $C_k$。

> [!image]+ 图片说明 
> ![Pasted image 20260117135534.png](/img/user/%E5%9B%BE%E7%89%87/Pasted%20image%2020260117135534.png)
> 左侧展示一个简单的三角形 $C_3$ 作为 Cycle 示例；右侧展示一个自交的路径,Not a Cycle。

---

### Hamiltonian Cycle (哈密顿圈)

> [!abstract] 定义
> **Hamiltonian Cycle** 是一个**遍历图中所有顶点**的 Cycle，即：
> 
>  对于图 $G=(V, E)$，若存在一个 Cycle $H$，满足：
> $$ V(H) = V(G) $$
> 即 $H$ 经过 $G$ 中每一个顶点恰好一次。

> [!important] 关键性质
> 1. **包含关系**: $\{Hamiltonian\ Cycles\} \subset \{Cycles\}$。
> 2. **必要条件**: 若图 $G$ 有 Hamiltonian Cycle，则 $G$ 必须是连通的（Connected）且没有割边（Bridge）。[[空间图理论/Hamiltonian Cycle 必要条件解释\|Hamiltonian Cycle 必要条件解释]]
> 3. **计算复杂度**: 一般图中寻找 Hamiltonian Cycle 是 **NP-complete** 问题。

> [!image]+ 图片说明
> ![Petersen Graph.png|331](/img/user/%E5%9B%BE%E7%89%87/Petersen%20Graph.png)![Pasted image 20260117140421.png|539](/img/user/%E5%9B%BE%E7%89%87/Pasted%20image%2020260117140421.png)
> “彼得森图 (Petersen Graph)”，其不包含 Hamiltonian Cycle。“立方体图 (Cube Graph)”，高亮显示其存在的 Hamiltonian Cycle。

---
## 2. 在 Spatial Graph Theory 中的应用

在 $\mathbb{R}^3$ 空间嵌入的图（Spatial Graph）中：

*   **Cycle 的几何形态**: 对应于简单的闭曲线（Simple Closed Curve）。在三维空间中，一个 Cycle 就是一个 **Knot (结)**。
*   **Hamiltonian Cycle 的拓扑意义**:
    *   若空间图 $G$ 包含 Hamiltonian Cycle，该 Cycle 定义了一个特定的 Knot Type。
    *   研究重点通常在于该 Hamiltonian Cycle 与图中*剩余边*（Edges in $E(G) \setminus E(H)$）之间的 **Linking Number** 或同调性质。
