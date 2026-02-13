---
{"dg-publish":true,"permalink":"//hamiltonian-cycle/"}
---



q: 为什么若图 有 [[空间图理论/什么是 cycle,Hamiltonian cycle\|Hamiltonian Cycle]]，则  必须是连通的（Connected）且没有割边（Bridge）。

a: 因为：
1. 连通性 (Connectedness): Hamiltonian Cycle 需要遍历图中所有的顶点恰好一次，并且回到起点。如果图不连通，那么至少存在两个顶点之间没有路径相连，这使得无法形成一个包含所有顶点的闭合路径。因此，图必须是连通的。
2. **无割边 (No Bridges)**: 割边是指删除该边后会使图变得不连通的边。如果图中有割边，那么删除这条割边后，图会被分成两个或多个连通分量。在这种情况下，不可能存在一个闭合路径能够遍历所有顶点并回到起点，因为割边的存在会中断这个路径。因此，图中不能有割边。

这两个条件确保了图中存在一条可以遍历所有顶点并返回起点的闭合路径，即 Hamiltonian Cycle。
