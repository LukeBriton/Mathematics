#### Bilinear Form

[linear algebra - Is a bilinear form a tensor or a scalar "output'' of that tensor? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4477570/is-a-bilinear-form-a-tensor-or-a-scalar-output-of-that-tensor)

- Bilinear form $h(,):V\times V\to \mathbb{K}$
	$\text{Hom}^2(V\times V, \mathbb{K})\cong\text{Hom}(V\otimes V, \mathbb{K})=(V\otimes V)^*\cong V^*\otimes V^*$
	$h= \sum\limits_{i,j=1}^nh_{ij}\epsilon^i\otimes\epsilon^j$
	$[h]\in M_{n\times n}(\mathbb{K})$ 是相对于 $V$ 的基 $\{\mathbf{e}_i\}$ 的表示
	$$
\begin{align}
h(u,w)&= \sum\limits_{i,j=1}^nh_{ij}\epsilon^i\otimes\epsilon^j(u,w)\\
:&=\sum\limits_{i,j=1}^nh_{ij}\epsilon^i(u)\otimes\epsilon^j(w) \\
&=\sum\limits_{i,j=1}^nh_{ij}u_{i}w_{j} \\
&=[u]^T[h][w]
\end{align}
$$
	可能属性：
	- 退化：$\exists u,h(u,\cdot)=0$ 或 $\exists v,h(\cdot,v)=0$
	- 非退化
	- 对称
		$\implies$ 可对角化
		（证明：归纳法，某种程度上像是正交规范基的构造）
	- 反对称
	- symplectic：反对称、非退化
	- 若 $\mathbb{K}$ 是代数闭域
		非退化、对称 $\implies$ 有基使之单位阵（可逆？）
		（证明：仍是构造基，代数闭域有代数学基本定理成立）
		$\mathbb{P}^n$ 上任意两超平面，由非退化二次型给定的，同构（基域代数闭）。
		$\mathbb{P}^2$ 中任意两 smooth 二次曲线同构
		
- $q(v) := h(v, v)$
