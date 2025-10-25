**[Continuously differentiable](https://en.wikipedia.org/wiki/Continuously_differentiable "Continuously differentiable")** ⊂ **Lipschitz continuous** ⊂ α**-[Hölder continuous](https://en.wikipedia.org/wiki/H%C3%B6lder_continuous "Hölder continuous")**,
where 0 < α ≤ 1. We also have 
**Lipschitz continuous** ⊂ **[absolutely continuous](https://en.wikipedia.org/wiki/Absolutely_continuous "Absolutely continuous")** ⊂ **[uniformly continuous](https://en.wikipedia.org/wiki/Uniformly_continuous "Uniformly continuous")** ⊂ **[continuous](https://en.wikipedia.org/wiki/Continuous_function "Continuous function")**.
#### norm & metric

[vector spaces - Difference between metric and norm made concrete: The case of Euclid - Mathematics Stack Exchange](https://math.stackexchange.com/questions/38634/difference-between-metric-and-norm-made-concrete-the-case-of-euclid)

[general topology - Metric spaces and normed vector spaces - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1607957/metric-spaces-and-normed-vector-spaces)
#### Continuity

More precisely, a function is continuous if arbitrarily small changes in its value can be assured by restricting to sufficiently small changes of its argument.

En première approche, une fonction f est **continue** si, à des variations infinitésimales de l'[antécédent](https://fr.wikipedia.org/wiki/Ant%C3%A9c%C3%A9dent_\(math%C3%A9matiques\) "Antécédent (mathématiques)") x, correspondent des variations infinitésimales de l'[image](https://fr.wikipedia.org/wiki/Image_\(math%C3%A9matiques\) "Image (mathématiques)") _f_(_x_).

- $f(x_{0})$的邻域，总包含$x_{0}$的**某个**邻域所成像。
	$\forall V\ni f(x_0)\ \exists U\ni x_0:\ f(U)\subseteq V$
	- $X ⊆ \mathbb{R}$ ，连续 $\Longleftrightarrow$ 左、右连续
	- 开集 $O\subseteq Y$, $f^{-1}(O)$ 也开（开集的前像为开，$f^{-1}:\mathcal{T}_{Y}\to\mathcal{T}_{X}$）
	- 闭集 $A\subseteq Y$, $f^{-1}(A)$ 也闭（闭集的前像为闭）
		反之不亦然：
		- $A=\{(x, y)\in \mathbb{R}^2| xy=1\}$ 闭，$\text{pr}_1(\cdot)$ 连续，但 $\text{pr}_1(A)$ 开。
		- $y=x^2, x\in(-1,1), y\in[0,1)$   
- 若把它误读成“包含**所有**邻域的像”，就变成“局部常值”，太强。
	$\exists U\ni x_0\ \forall V\ni f(x_0):\ f(U)\subseteq V$

在度量空间/任意 $T_1$ 空间里：对任一点 $y_0$，**所有邻域的交等于单点 $\{y_0\}$**。  

理由（拓扑版）：$T_1$ 的定义是任意两点可用邻域把对方排除；等价地，单点集是闭集。于是对任何 $y\neq y_0$，都能找一个含 $y_0$ 的邻域把 $y$ 排除掉，所以 $y$ 不在“所有邻域的交”里，只有 $y_0$ 留下。([T1 space - Wikipedia](https://en.wikipedia.org/wiki/T1_space?utm_source=chatgpt.com))

理由（度量版，更直观）：  
$$
\bigcap_{\varepsilon>0} B\big(y_0,\varepsilon\big)={y_0}.  
$$
若 $y\neq y_0$，取 $\varepsilon=\tfrac12 d(y,y_0)>0$，则 $y\notin B(y_0,\varepsilon)$，所以 $y$ 不在交里；而 $y_0$ 显然在每个球里。度量空间是 Hausdorff，从而必为 $T_1$。([Metric Space is Hausdorff - ProofWiki](https://proofwiki.org/wiki/Metric_Space_is_Hausdorff?utm_source=chatgpt.com))

若存在**同一个**邻域 $U\ni x_0$ 使  $\forall\ V\ni f(x_0)\quad f(U)\subseteq V,$

那么
$$
f(U)\subseteq \bigcap_{V\ni f(x_0)} V=\{f(x_0)\},  
$$
于是 $f$ 在 $U$ 上恒等于 $f(x_0)$，也就是**在 $x_0$ 附近局部常值**。这比连续强得多（例如恒等函数在 $\mathbb{R}$ 上处处连续，但绝不是局部常值）。

- $f(x_{0})$附近的值，总能被足够接近$x_{0}$的点取到
	$\forall V\ni f(x_0)\ \exists U\ni x_0:\ V\subseteq f(U)$
	怪怪的

例如 $f(x)=x^2$ 在 $x_0=0$ 连续，但 $f(U)$ 不可能覆盖 $0$ 的任何对称邻域（会缺少负数）


- $f$ 在 $x_0$ 处把所有邻域映到一个邻域
	$\forall \delta>0\ \exists \varepsilon>0:\ B_Y\big(f(x_0),\varepsilon\big)\subseteq f\big(B_X(x_0,\delta)\big).$

*locally onto*: for any $\delta>0$ there exists $\varepsilon>0$ such that for every $w$ with $|w-w_0|<\varepsilon$ there is a $z$ with $|z-z_0|<\delta$ and $f(z)=w$. That’s precisely $B_Y(f(x_0),\varepsilon)\subset f(B_X(x_0,\delta))$. 

https://dummit.cos.northeastern.edu/teaching_fa22_4555/complexanalysis_5_local_behavior_of_holomorphic_functions_v1.00.pdf

- Dirichlet function

- Lipschitz continuous & Lipschitz constant α

- distance function $d(\cdot, M):X\to \mathbb{R}, x\mapsto d(x,M):=\inf_{m∈M} d(x,m)$

- isometry

- Sequential Continuity
	$f : X → Y$，$X$ 内**任意**极限为 $x$ 的数列 $(x_{k})$，$\lim f(x_{k})=f(x)$
	**任意** 数列项的函数值的极限 $=$ 数列极限的函数值
	- 函数连续 $\Longleftrightarrow$ 序列连续

- vector space of continuous functions ($f+g$, $\lambda f$)
	$C(X, F)\subseteq F^X$
	- $F = \mathbb{K}$, $f\cdot g$ 连续
	- $F = \mathbb{K}$, $g(x)\neq0$, $f/ g$ 连续
	- 有理函数 连续
	- $\mathbb{K}^n$ 上多项式 连续

- 复合函数 连续

- 函数 范数 连续

- $f = (f_1, . . . , f_m)$ 连续 $\Longleftrightarrow$ 分量连续

- 单边连续 （限于 $\mathbb{R}$ 上）
	$f(x_{0})$ 的邻域，总包含 $x_{0}$ 的某个左/右 $δ$-邻域
	- 左右连续 $\Longleftrightarrow$ 小于/大于其的序列收敛
	- 左右连续 $\Longleftrightarrow$ 收敛

- Show that any linear function from $\mathbb{K}^n$ to $\mathbb{K}^m$ is Lipschitz continuous

#### Compactness

$X:=(X,d)$ 中
- 覆盖：能盖住所给集合的一族集合
- 开覆盖：各集均开
- 紧：任意开覆盖，有有限开覆盖子集。
	任意开覆盖，有有限子覆盖。

### Exercise

#### 12: Show that any linear function from $\mathbb{K}^n$ to $\mathbb{K}^m$ is Lipschitz continuous.

Train of thought of mine:

Since implicitly it assumes both vector spaces to be finite-dimensional, it's "natural" to have a basis (standard/natural/canonical basis perhaps), though I'm not very clear if there is a natural choice (maybe in the sense of categorical naturaelity?), and seems it depends on (or is equivalent to?) Axiom of Choice.

Anyway, we can have one (quite standard) basis like $\mathbf{e_1} = (1, ..., 0)^T$, $\mathbf{e_2} = (0, 1, ..., 0)^T$, ..., etc. in a vector space (though someone told me it's only meaningful an inner product space, for me it's like "all bases are created equal" when only considering linearity). Then we have some isomorphism between matrix representation $\mathrm{M}$ and the linear function $f$, and it maps basis $\{\mathbf{e}_{j}\}_{j\le n}$ to $\{\epsilon_{i}\}_{i\le m}$ (both defined with Kronecker delta) through $\epsilon_{i}=\text{a linear combination of  }\{\mathbf{e}_{j}\}$, maybe we can write it as $\epsilon_{i} = f_{i}({\{\mathbf{e}_{j}\}})$. Since all linear functions are done with the given basis, one can just ignore scalars temporarily...

Then, I have a feeling, for $f = (f_1, f_2, ..., f_m)$ is continuous when it's component-wise continuous (though I'm not quite clear about its proof), why don't we prove its Lipschitz continuity in a similar way?

That is, we need to prove there is some Lipschitz constant α, s.t.
$$
\begin{align*}
& d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y}))\le αd(\mathbf{x},\mathbf{y})\\
& \mathbf{x} = (x_{1}, x_{2}, \dots, x_{n})^T\\
& \mathbf{y} = (y_{1}, y_{2}, \dots, y_{n})^T\\
\end{align*}
$$
How to define the metric... <= induce it from a norm ($\mathbb{K}^n$ and $\mathbb{K}^m$ are normed)

"Unless otherwise stated, we consider $\mathbb{K}^m$ to be endowed with the Euclidean inner product (·|·) and the induced Euclidean norm"

$$
\begin{align*}
d(\mathbf{x},\mathbf{y}) &= ‖\mathbf{x}-\mathbf{y}‖\\
&= ‖(x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T‖ \\
d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y})) &= ‖f_{1}(\mathbf{x})-f_{1}(\mathbf{y})‖ \\
&= ‖f_{1}(\mathbf{x} - \mathbf{y})‖\\
& = ‖f_{1}((x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T) ‖\\
& = ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n} ‖\\
& = ‖((x_{1}-y_{1})M_{11}, (x_{2}-y_{2})M_{12}, \dots, (x_{n}-y_{n})M_{1n})^T‖\\
\text{Without loss of generality, let }& M_{11}\text{ be}\max \{M_{1j}\},\ j\le m,\ \text{then we shall have}\\
d(f_{1}(\mathbf{x}), f_{1}(\mathbf{y})) &\le ‖((x_{1}-y_{1})M_{11}, (x_{2}-y_{2})M_{11}, \dots, (x_{n}-y_{n})M_{11})^T‖ \\
&= M_{11}‖(x_{1}-y_{1}, x_{2}-y_{2}, \dots, x_{n}-y_{n})^T‖\\
&= M_{11}d(\mathbf{x},\mathbf{y})
\end{align*}
$$
For all $f_{i}$s, $d(f_{i}(\mathbf{x}), f_{i}(\mathbf{y}))\le\max\{M_{i1}\}d(\mathbf{x},\mathbf{y})$, $i\le m$.

$$
\begin{align*}
d(f(\mathbf{x}), f(\mathbf{y})) &= ‖f(\mathbf{x}) - f(\mathbf{y})‖ \\
&= ‖f(\mathbf{x} - \mathbf{y})‖\\
&= ‖f_{1}(\mathbf{x} - \mathbf{y}) + f_{2}(\mathbf{x} - \mathbf{y}) + \dots + f_{m}(\mathbf{x} - \mathbf{y})‖\\
& = ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n}\\
&\quad+(x_{1}-y_{1})M_{21}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{22}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{2n}\mathbf{e}_{n}\\
&\quad+(x_{1}-y_{1})M_{m1}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{m2}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{mn}\mathbf{e}_{n}‖\\
&\le ‖(x_{1}-y_{1})M_{11}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{12}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{1n}\mathbf{e}_{n}‖\\
&\quad+‖(x_{1}-y_{1})M_{21}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{22}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{2n}\mathbf{e}_{n}‖\\
&\quad+‖(x_{1}-y_{1})M_{m1}\mathbf{e}_{1}+ (x_{2}-y_{2})M_{m2}\mathbf{e}_{2} + \dots + (x_{n}-y_{n})M_{mn}\mathbf{e}_{n}‖\\
&\le M_{11}d(\mathbf{x},\mathbf{y}) + M_{21}d(\mathbf{x},\mathbf{y}) +\dots+ M_{m1}d(\mathbf{x},\mathbf{y})\\
&\le \max\{M_{i1}\}d(\mathbf{x},\mathbf{y})
\end{align*}
$$


$id = \mathbf{e} \otimes \mathbf{v}$

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
	V \arrow[r, "f"] \arrow[d, "\mathbf{e}^j"'] & W \arrow[d, "\mathbf{\epsilon}_i"] \\
	\mathbb{R}^n \arrow[r, "T"']                & \mathbb{R}^m                      
\end{tikzcd}
\end{document}
```
$$
\begin{align*}
T&=\sum\limits_{i=1}^{m}\sum\limits_{j=1}^{n} A_{j}^i\mathbf{e}^j\otimes\mathbf{\epsilon}_i, \mathbf{e}^j\text{为对偶基}\\
T(v)&=\sum\limits_{1\leq i\leq m, 1\leq j\leq n} A_{j}^i\mathbf{e}^j(v)\mathbf{\epsilon}_i\\
&=\sum\limits_{i,j} A_{j}^iv_{j}\mathbf{\epsilon}_i\\
\end{align*}
$$
