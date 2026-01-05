#### Continuous linear maps

- Completeness of $\mathcal{L}(E,F)$
	$(A_{n})$ 是 $\mathcal{L}(E,F)$ 中 Cauchy 列
	- $\text{Hom}(E,F)$ 的子空间 $\implies$ 线性 $\implies$ $(A_{n}x)$ 为 $F$ 中的 Cauchy 列 $\implies$ 定义 $A: E\to F, x\mapsto \lim A_{n}x$ （线性）
	- $(A_n)$ 在 $\mathcal{L}(E,F)$ 中有界 $\implies$ $‖A_{n}x‖\le α‖x‖$ $\xRightarrow{\lim}$ $‖Ax‖\le α‖x‖$ $\implies$ $A$ 在 $\mathcal{L}(E,F)$ 中
	- $‖A_{n}x-A_{m}x‖\le ε$ $\xRightarrow{m→ ∞}$ $‖A_{n}x-Ax‖\le ε$ $\implies$ $‖A_{n}-A‖=\sup_{‖x‖\le 1}‖A_{n}x-Ax‖ \le ε$

- $\mathcal{L}\text{is}(E,F)$ (topologically) isomorphic:
	- 连续线性同构 $A:E\to F$，s.t. $A^{-1}$ 连续，i.e. $A \in \mathcal{L}(F,E)$
	write $E \cong F$ if $\mathcal{L}\text{is}(E,F)$ is not empty, which in normed vector spaces always means “topologically isomorphic”
- $\mathcal{L}\text{aut}(E)$ topologically automorphism 自同构群

- $\mathcal{L}(\mathbb{K},F)$ 与 $F$ 典范地等距同构
	$\mathcal{L}(\mathbb{K},F) \to F, A\mapsto A1$
	- 线性、入射
	- 证总有 $A_{v}1=v$，满射
	- 证等距（两个范数都是同一集合的上确界？）

- $E \cong F$ $\implies$ $E$ is Banach $\iff$ $F$ is Banach
	Cauchy 列 $\mapsto$ Cauchy 列
	收敛列 $\mapsto$ 收敛列

- $T : E → \mathbb{K}^n, v=\sum\limits_{i}^{n}x_{i}e_{i}\mapsto (x_{1},x_{2}, \dots,x_{n})$
	- Cauchy–Schwarz $\implies$ $T^{-1} \in \mathcal{L}(\mathbb{K}^n,E)$
	- 范数等价 $\implies$ $T \in \mathcal{L}(E, \mathbb{K}^n)$

- 有限维赋范向量空间
	- 范数等价
	- 完备（Banach）
	- $\text{Hom}(E,F) = \mathcal{L}(E,F)$ （继而连续）
	- + 内积 $\implies$ Hilbert
	- renormed with an equivalent Hilbert norm $\implies$ Hilbert

- Matrix representations
	$\mathcal{L}(E,F) \to \mathbb{K}^{m\times n}, A\mapsto [A]_{\mathcal{E,F}}$
	- Hilbert-Schmidt norm
	- $\mathbb{K}^{m\times n}$ 等距同构于 $\mathbb{K}^{mn}$
	- 矩阵表示是拓扑同构
	- 矩阵乘相当于换基

- In analysis, we will consider all maps of metric spaces in the space of continuous linear maps between two Banach spaces $E$ and $F$ 

- exponential map
	$\mathcal{L}(E)\to \mathcal{L}(E), A\mapsto e^A=\sum\limits_{k=0}^∞A^k/k!$
	- $‖A^k‖\le ‖A‖^k$ $\implies$ $\sum_{k}α^k/k!$ is a majorant of $\sum_{k}A^k/k!$ for all $α\ge‖A‖$ $\implies$ 收敛 

- $U:= U_{A}:\mathbb{K}\to \mathcal{L}(E), t\mapsto e^{tA}$
	 - $U\in C^∞(\mathbb{K},\mathcal{L}(E))$
	 - $\dot{U}=AU$
	 - $U$ 是 additive group 到 the multiplicative group 的群同态

- 线性微分方程
	- $\dot{x}=Ax+f(t), t\in \mathbb{R}$

