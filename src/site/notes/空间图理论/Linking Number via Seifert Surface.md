---
{"dg-publish":true,"dg-permalink":"/spatial-graph-theory/linking-number-seifert-surface/","permalink":"/spatial-graph-theory/linking-number-seifert-surface/","tags":["math/topology","concept/explanation","paper/nikkuni"]}
---


## 1. 大纲

相比于投影图数交叉点，**Seifert Surface (赛弗特曲面)** 定义提供了一个三维实体的几何视角。理解该定义需遵循以下三个步骤：

1.  **Surface Spanning (张成曲面)**: 曲线 $K_1$ 定义了一个曲面 $F_1$。
2.  **Orientation (定向关联)**: $K_1$ 的方向决定了 $F_1$ 的法向量方向。
3.  **Intersection (穿刺计数)**: 曲线 $K_2$ 穿过 $F_1$ 的净次数。

## 2. 说明

### Step 1: 构造曲面 $F_1$
对于任意封闭曲线 $K_1$（蓝色），存在一个曲面 $F_1$（灰色区域），使得 $K_1$ 是 $F_1$ 的唯一边界。
$$ \partial F_1 = K_1 $$
### Step 2: 确定法向量 $\vec{n}$
使用 **右手定则** 建立联系：
*   右手四指指向 $K_1$ 的遍历方向。
*   右手大拇指指向即为曲面 $F_1$ 的法向量 $\vec{n}$ (即曲面的“正向”侧)。

### Step 3: 计算穿刺 (Intersection)
观察第二条曲线 $K_2$（红色）如何穿过曲面 $F_1$。在每个交点 $p$ 处比较两个向量：
1.  $\vec{v}$: 曲线 $K_2$ 在点 $p$ 处的切向量（前进方向）。
2.  $\vec{n}$: 曲面 $F_1$ 在点 $p$ 处的法向量。

> [!abstract] 符号法则 (Sign Convention)
> *   **Case (+1)**: $\vec{v}$ 与 $\vec{n}$ 夹角为锐角（方向大致相同）。即 $K_2$ 从 $F_1$ 的反面穿出到正面。
> *   **Case (-1)**: $\vec{v}$ 与 $\vec{n}$ 夹角为钝角（方向大致相反）。即 $K_2$ 从 $F_1$ 的正面刺入到反面。

### 结果公式
$$ lk(K_1, K_2) = \sum_{p \in K_2 \cap F_1} \text{sign}(p) $$

> [!example] 示例分析：Hopf Link
> 1.  $K_1$ 是一个圆圈，张成一个圆盘 $F_1$。
> 2.  $K_2$ 是另一个圆圈，穿过这个圆盘的中心。
> 3.  $K_2$ 只穿过圆盘 **一次**。
> 4.  根据方向设定，如果是同向穿过，结果为 $+1$；反之 $-1$。
> 5.  这就是为什么 Hopf Link 的 $lk$ 是 $\pm 1$。

