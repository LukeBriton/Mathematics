#### Basics

- norm/norme/Norm
	$\|\cdot\| : E \to \mathbb{R}^+$
	with 正定、正齐次/半范数、三角不等式/次可加
	- Lipschitz-stetig (Die umgekehrte Dreiecksungleichung)
- normierter Vektorraum $(E, \|\cdot\|)$
- von der Norm induzierte Metrik
	Es sei $E := (E, \|\cdot\|)$ ein normierter Vektorraum,
	$d: E \times E \to \mathbb{R}^{+}, \quad (x, y) \mapsto \|x - y\|$
	- Alle Aussagen die für metrische Räume gemacht wurden, auch für $E$. Insbesondere sind also die Begriffe „Umgebung“, „Häufungspunkt“ und „Konvergenz“ in $E$ wohldefiniert.
	- Alle Aussagen bei denen *nicht* von der Körperstruktur von $\mathbb{K}$ oder der Ordnungsstruktur von $\mathbb{R}$ Gebrauch gemacht wurde, ohne weiteres auf Folgen in $E$ übertragen werden können.
- umgekehrte Dreiecksungleichung
- diskrete Metrik
	Es auf jedem von 0 verschiedenen Vektorraum $V$ eine Metrik gibt, bezüglich derer $V$ beschränkt ist.
	Hingegen folgt aus der positive Homogenität, daß es auf $V$ keine Norm geben kann, bezüglich derer $V$ normbeschränkt ist.
- Betragsnorm $|\cdot|$ auf $\mathbb{K}$
	$\mathbb{K} := (\mathbb{K}, |\cdot|)$
- induzierte Norm
- die Produktnorm auf $E := E_1 \times \dots \times E_m$, $(E_j, \|\cdot\|_j)$
	$\|x\|_{\infty} := \max\limits_{1 \le j \le m} \|x_j\|_j, \quad  x = (x_1, \dots, x_m) \in E$
	- Maximumsnorm
		$|x|_{\infty} := \max\limits_{1 \le j \le m} |x_j|, \quad x = (x_1, \dots, x_m) \in \mathbb{K}^m.$
- der euklidischen Norm
	$|x| := \sqrt{(x|x)} = \sqrt{\sum_{j=1}^{m} |x_j|^2}, \quad x = (x_1, \dots, x_m) \in \mathbb{K}^m$
- die Summennorm
	$|x|_1 := \sum_{j=1}^{m} |x_j|, \quad x = (x_1, \dots, x_m) \in \mathbb{K}^m$
- Äquivalente Normen
	Es sei $E$ ein Vektorraum. Wir nennen zwei Normen $\|\cdot\|_1$ und $\|\cdot\|_2$ auf $E$ äquivalent, falls es ein $K \ge 1$ gibt mit
	$$
	\frac{1}{K} \|x\|_1 \le \|x\|_2 \le K \|x\|_1, \quad x \in E.
	$$
	In diesem Fall schreiben wir $\|\cdot\|_1 \sim \|\cdot\|_2$.
	- $|\cdot|_1 \sim |\cdot| \sim |\cdot|_\infty \quad \text{auf } \mathbb{K}^m$
		$\mathbb{B}^m \subset \mathbb{B}_\infty^m \subset \sqrt{m}\mathbb{B}^m, \quad \mathbb{B}_1^m \subset \mathbb{B}^m \subset \sqrt{m}\mathbb{B}_1^m.$
	Auf $\mathbb{K}^m$ sind alle Normen äquivalent
	- Es seien $E$ und $F$ normierte Vektorräume und $X \subset E$.
	  Dann ist die Stetigkeit von $f: X \to F$ in $x_0 \in X$ unabhängig von der Wahl äquivalenter Normen auf $E$ und auf $F$.
- Matrix norm
	Für $m, n \in \mathbb{N}^\times$ bezeichnet $\mathbb{K}^{m \times n}$ die Menge aller $(m \times n)$-Matrizen mit Einträgen aus $\mathbb{K}$. Wir können $\mathbb{K}^{m \times n}$ als die Menge aller Abbildungen von $\{1, \dots, m\} \times \{1, \dots, n\}$ in $\mathbb{K}$ auffassen.
	- Dann ist $\mathbb{K}^{m \times n}$ mit den punktweisen Verknüpfungen ein Vektorraum.
		Hierbei sind $\alpha A$ und $A + B$ für $\alpha \in \mathbb{K}$ und $A, B \in \mathbb{K}^{m \times n}$ die aus der Linearen Algebra bekannten Operationen der Multiplikation einer Matrix mit einem Skalar und der Addition zweier Matrizen.
		- (a) Durch
			$|A| := \left( \sum_{j=1}^{m} \sum_{k=1}^{n} |a_{jk}|^2 \right)^{1/2}, \quad A = [a_{jk}] \in \mathbb{K}^{m \times n}$
			wird auf $\mathbb{K}^{m \times n}$ eine Norm definiert. (Frobenius norm)
			- [matrices - The Frobenius norm is not an operator norm - Mathematics Stack Exchange](https://math.stackexchange.com/questions/3354914/the-frobenius-norm-is-not-an-operator-norm)
			- [normed spaces - Frobenius norm is not induced - Mathematics Stack Exchange](https://math.stackexchange.com/questions/588481/frobenius-norm-is-not-induced)
			- [linear algebra - Operator norm induced by Frobenius norm - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2600330/operator-norm-induced-by-frobenius-norm)
			- [matrices - Why is the Frobenius norm of a matrix greater than or equal to the spectral norm? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/252819/why-is-the-frobenius-norm-of-a-matrix-greater-than-or-equal-to-the-spectral-norm)
		- (b) Die folgenden Abbildungen definieren äquivalente Normen:
			(1) $[a_{jk}] \mapsto \sum_{j=1}^{m} \sum_{k=1}^{n} |a_{jk}|$ ($1$-norm)
			(2) $[a_{jk}] \mapsto \max_{1 \le j \le m} \sum_{k=1}^{n} |a_{jk}|$ ($\infty$-norm)
			(3) $[a_{jk}] \mapsto \max_{1 \le k \le n} \sum_{j=1}^{m} |a_{jk}|$
			(4) $[a_{jk}] \mapsto \max_{\substack{1 \le j \le m \\ 1 \le k \le n}} |a_{jk}|$ (max norm)
- Es sei $n \in \mathbb{N}^\times$. In der Linearen Algebra wird gezeigt, daß für $A = [a_{jk}] \in \mathbb{K}^{n \times n}$ die **Determinante**, $\det A$, von $A$ durch
	$$
	\det A = \sum_{\sigma \in S_n} (\text{sign } \sigma) a_{1\sigma(1)} \cdots a_{n\sigma(n)}
	$$
	gegeben ist. Man zeige, daß die Abbildung
	$$
	\mathbb{K}^{n \times n} \to \mathbb{K}, \quad A \mapsto \det A
	$$
	stetig ist. (Hinweis: Durch die Bijektion
	$$
	\mathbb{K}^{m \times n} \to \mathbb{K}^{mn}, \quad \begin{bmatrix} a_{11} & \dots & a_{1n} \\ \vdots & \ddots & \vdots \\ a_{m1} & \dots & a_{mn} \end{bmatrix} \mapsto (a_{11}, \dots, a_{1n}, a_{21}, \dots, a_{mn})
	$$
	wird $\mathbb{K}^{m \times n}$ mit der natürlichen Topologie versehen.)
	- $\mathbb K^{n\times n}\xrightarrow{\text{flattening}}\mathbb K^{n^2}\xrightarrow{\text{polynomial }P}\mathbb K$

[vector spaces - Difference between metric and norm made concrete: The case of Euclid - Mathematics Stack Exchange](https://math.stackexchange.com/questions/38634/difference-between-metric-and-norm-made-concrete-the-case-of-euclid)

[general topology - Metric spaces and normed vector spaces - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1607957/metric-spaces-and-normed-vector-spaces)

- Taxicab/Manhattan norm: $\|x\|_{1}$
- Euclidean norm: $\|x\|_{2}$
- Chebyshev/uniform/supremum/infinity norm: $\|x\|_{\infty}$
- $p$-norm: $\|x\|_{p}$ 幂平均不等式

[What does "all norms are equivalent" actually mean? : r/mathematics](https://www.reddit.com/r/mathematics/comments/11jfhxf/what_does_all_norms_are_equivalent_actually_mean/?rdt=53222)

[general topology - Definition of Equivalent Norms - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1380191/definition-of-equivalent-norms)

#### Supplementals

[Normed vector space - Wikipedia](https://en.wikipedia.org/wiki/Normed_vector_space)

Every normed vector space can be "uniquely extended" to a Banach space, which makes normed spaces intimately related to Banach spaces. Every Banach space is a normed space but converse is not true. For example, the set of the [finite sequences](https://en.wikipedia.org/wiki/Finite_sequence "Finite sequence") of real numbers can be normed with the [Euclidean norm](https://en.wikipedia.org/wiki/Euclidean_norm "Euclidean norm"), but it is not complete for this norm.

Of special interest are [complete](https://en.wikipedia.org/wiki/Complete_space "Complete space") normed spaces, which are known as _[Banach spaces](https://en.wikipedia.org/wiki/Banach_space "Banach space")_. Every normed vector space $V$ sits as a dense subspace inside some Banach space; this Banach space is essentially uniquely defined by $V$ and is called the _[completion](https://en.wikipedia.org/wiki/Cauchy_completion "Cauchy completion")_ of $V$.

Two norms on the same vector space are called _[equivalent](https://en.wikipedia.org/wiki/Equivalent_norm "Equivalent norm")_ if they define the same [topology](https://en.wikipedia.org/wiki/Topology_\(structure\) "Topology (structure)"). On a finite-dimensional vector space (but not infinite-dimensional vector spaces), all norms are equivalent (although the resulting metric spaces need not be the same) And since any Euclidean space is complete, we can thus conclude that all finite-dimensional normed vector spaces are Banach spaces.

此处等价有类TCS中 $\Theta$，见 Godement 书。

Normable spaces

Metrizable topological vector space

