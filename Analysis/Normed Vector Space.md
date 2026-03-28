#### Basics

- norm/norme/Norm
	$\|\cdot\| : E \to \mathbb{R}^+$ with 正定、正齐次/半范数、三角不等式/次可加
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

