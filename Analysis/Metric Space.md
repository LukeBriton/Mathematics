#### Basics

- metric/métrique/Metrik
	$d: X \times X \to \mathbb{R}^+$ with 正定、对称、三角不等式/次可加性
- metrischer Raum $(X, d)$
- $\mathbb{K}$ has the natural metric
	$\mathbb{K} \times \mathbb{K} \to \mathbb{R}^{+}, \quad (x, y) \mapsto |x - y|.$
- induced metric & metric subspace
- discrete metric
	$d(x,y)=1-\delta_{xy}$
- product metric on $X := X_1 \times \cdots \times X_m$, $(X_j, d_j)$, $1 \le j \le m$
	$d(x, y) := \max\limits_{1 \le j \le m} d_j(x_j, y_j)$,
	$x = (x_1, \dots, x_m) \in X$
	$y = (y_1, \dots, y_m) \in X$
	- $\mathbb{B}_X(a, r) = \prod\limits_{j=1}^{m} \mathbb{B}_{X_j}(a_j, r), \quad \bar{\mathbb{B}}_X(a, r) = \prod\limits_{j=1}^{m} \bar{\mathbb{B}}_{X_j}(a_j, r)$
- umgekehrte Dreiecksungleichung
- Umgebung von $a\in X$: 包含开球
	- die Menge aller Umgebungen des Punktes: $\mathcal{U}(a) := \mathcal{U}_X(a) := \{ U \subseteq X ; U \text{ ist Umgebung von } a \} \subseteq \mathcal{P}(X) .$
	- die offene/abgeschlossene $ε$-Umgebung von $a$:
		$\mathbb{B}(a, ε)$ und $\bar{\mathbb{B}}(a, ε)$
	- [general topology - Must every point have its own singleton as a neighborhood? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2337205/must-every-point-have-its-own-singleton-as-a-neighborhood)
	  [real analysis - Can a neighbourhood of a point be an singleton set? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/474746/can-a-neighbourhood-of-a-point-be-an-singleton-set)

- equivalent metrics
	Zwei Metriken $d_1$ und $d_2$ auf einer Menge $X$ heißen **äquivalent**, wenn es zu jedem $x \in X$ und jedem $\varepsilon > 0$ positive Zahlen $r_1$ und $r_2$ gibt mit
	$$
	\mathbb{B}_1(x, r_1) \subset \mathbb{B}_2(x, \varepsilon), \quad \mathbb{B}_2(x, r_2) \subset \mathbb{B}_1(x, \varepsilon).
	$$
	Hierbei bezeichnet $\mathbb{B}_j$ den Ball in $(X, d)$, $j = 1, 2$.
	- $d_1$ und $d_2$ sind genau dann äquivalent, wenn $d_1$ zugleich stärker und schwächer als $d_2$ ist, d.h., falls für jedes $x \in X$ gilt: $\mathfrak{U}_{X_1}(x) = \mathfrak{U}_{X_2}(x)$.
- Es seien $d_1$ und $d_2$ Metriken auf $X$ und $X_j := (X, d_j)$, $j = 1, 2$. Dann heißt $d_1$ **stärker** als $d_2$, wenn für jedes $x \in X$ gilt: $\mathfrak{U}_{X_1}(x) \supseteq \mathfrak{U}_{X_2}(x)$, d.h., wenn jeder Punkt mehr $d_1$-Umgebungen als $d_2$-Umgebungen besitzt. In diesem Fall sagt man auch, $d_2$ sei **schwächer** als $d_1$.
	- $d_1$ ist genau dann stärker als $d_2$, wenn die natürliche Injektion $i: X_1 \to X_2$, $x \mapsto x$ stetig ist.
		$U\in \mathfrak U_{X_1}(x) \cancel\implies i(U)\in \mathfrak U_{X_2}(x)$
		$V\in \mathfrak U_{X_2}(x)\implies i^{-1}(V)\in \mathfrak U_{X_1}(x)$
		- $i^{-1}(V)=V$
		$V\in \mathfrak U_{X_2}(x)\implies V\in \mathfrak U_{X_1}(x)$
		- $\implies\mathfrak U_{X_2}(x)\subseteq \mathfrak U_{X_1}(x)$
[abstract algebra - Difference between "space" and "algebraic structure" - Mathematics Stack Exchange](https://math.stackexchange.com/questions/174108/difference-between-space-and-algebraic-structure)

#### Supplementals

[Complete metric space](https://en.wikipedia.org/wiki/Complete_metric_space)

The space $\mathbb{R}$ of real numbers and the space $\mathbb{C}$ of [complex numbers](https://en.wikipedia.org/wiki/Complex_number "Complex number") (with the metric given by the absolute difference) are complete, and so is [Euclidean space](https://en.wikipedia.org/wiki/Euclidean_space "Euclidean space") $\mathbb{R}^n$, with the [usual distance](https://en.wikipedia.org/wiki/Euclidean_distance "Euclidean distance") metric. In contrast, [infinite-dimensional](https://en.wikipedia.org/wiki/Dimension_\(vector_space\) "Dimension (vector space)") [normed vector spaces](https://en.wikipedia.org/wiki/Normed_vector_space "Normed vector space") may or may not be complete; those that are complete are [Banach spaces](https://en.wikipedia.org/wiki/Banach_space "Banach space"). The space $C[a, b]$ of [continuous real-valued functions on a closed and bounded interval](https://en.wikipedia.org/wiki/Continuous_functions_on_a_compact_Hausdorff_space "Continuous functions on a compact Hausdorff space") is a Banach space, and so a complete metric space, with respect to the [supremum norm](https://en.wikipedia.org/wiki/Supremum_norm "Supremum norm"). However, the supremum norm does not give a norm on the space $C(a, b)$ of continuous functions on $(a, b)$, for it may contain [unbounded functions](https://en.wikipedia.org/wiki/Bounded_function "Bounded function"). Instead, with the [topology](https://en.wikipedia.org/wiki/Topological_space "Topological space") of [compact convergence](https://en.wikipedia.org/wiki/Compact_convergence "Compact convergence"), $C(a, b)$ can be given the structure of a [Fréchet space](https://en.wikipedia.org/wiki/Fr%C3%A9chet_space "Fréchet space"): a [locally convex topological vector space](https://en.wikipedia.org/wiki/Locally_convex_topological_vector_space "Locally convex topological vector space") whose topology can be induced by a complete [translation-invariant](https://en.wikipedia.org/wiki/Metric_space#Normed_vector_spaces "Metric space") metric.

[Is the absolute value function a metric? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1893283/is-the-absolute-value-function-a-metric)

If $x\in \mathbb{R}$, then $|x| = \|x\|_1 = \|x\|_2 = \|x\|_{\infty}$