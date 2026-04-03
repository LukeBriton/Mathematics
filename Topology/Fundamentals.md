#### Preliminaries

der offene/abgeschlossene Ball
- In $\mathbb{K}=\mathbb{R}$ oder $\mathbb{C}$
	- $\mathbb{K}=\mathbb{R}$
		das offene/abgeschlossene Intervall
	- $\mathbb{K}=\mathbb{C}$
	  die offene/abgeschlossene Kreisscheibe 
		$\mathbb{D}(a, r)$, $\bar{\mathbb{D}}(a, r)$
		Einheitskreisscheibe $\mathbb{D}$, $\bar{\mathbb{D}}$
- In dem metrischen Raum $X:=(X,d)$
- In dem normierten Vektorraum $E := (E, \|\cdot\|)$
	$\mathbb{B}(a, r)$, $\bar{\mathbb{B}}(a, r)$
	Einheitsball $\mathbb{B} := \mathbb{B}(0,1)$, $\bar{\mathbb{B}} := \bar{\mathbb{B}}(0,1)$
	$r\mathbb{B} = \mathbb{B}(0,r)$, $r\bar{\mathbb{B}} = \bar{\mathbb{B}}(0,r)$, $a + r\mathbb{B} = \mathbb{B}(a,r)$, $a + r\bar{\mathbb{B}} = \bar{\mathbb{B}}(a,r)$.
- Es bezeichne $\mathbb{B}^m$ den reellen offenen euklidischen Einheitsball, d.h. $\mathbb{B}^m := \mathbb{B}_{\mathbb{R}^m},$
	$\mathbb{B}_{\infty}^{m} = \underbrace{\mathbb{B}_{\infty}^{1} \times \cdots \times \mathbb{B}_{\infty}^{1}}_{m} = (-1, 1)^{m}$
	Für $\mathbb{B}^m$ oder $\mathbb{B}_1^m$ gibt es keine analoge Darstellung.
- Umgebungsbegriff
	Es seien $E = (E, \|\cdot\|)$ ein normierter Vektorraum und $\|\cdot\|_1$ eine zu $\|\cdot\|$ äquivalente Norm auf $E$. Setzen wir $E_1 := (E, \|\cdot\|_1)$, so gilt
	$$
	\mathcal{U}_E(a) = \mathcal{U}_{E_1}(a) , \quad a \in E
	$$
	d.h., der Umgebungsbegriff hängt nur von der Äquivalenzklasse der Norm ab; äquivalente Normen liefern dieselben Umgebungen.
- $\mathbb{C} := \mathbb{R} + i\mathbb{R}$
	$\mathbb{C} \ni z = x + iy \leftrightarrow (x, y) \in \mathbb{R}^2$
	$\mathbb{C}^m \ni (z_1, \dots, z_m) = (x_1 + iy_1, \dots, x_m + iy_m) \leftrightarrow (x_1, y_1, \dots, x_m, y_m) \in \mathbb{R}^{2m}$
	- Bezüglich dieser kanonischen Identifikation gilt
		$\mathbb{B}_{\mathbb{C}^m} = \mathbb{B}^{2m} = \mathbb{B}_{\mathbb{R}^{2m}}$ und folglich $\mathcal{U}_{\mathbb{C}^m} = \mathcal{U}_{\mathbb{R}^{2m}}$
	Somit können bei **topologischen Fragen**, d.h. bei Untersuchungen, in welchen Aussagen über Umgebungen von Punkten gemacht werden, die Mengen $\mathbb{C}^m$ und $\mathbb{R}^{2m}$ miteinander identifiziert werden.
- Die Begriffe „Häufungspunkt“ und „Konvergenz“ sind **topologische Konzeptionen**, d.h., sie verwenden nur den Umgebungsbegriff und sind somit invariant unter Übergang zu äquivalenten Normen.

#### Openness

$X:=(X,d)$ 度量空间，$a\in A \subseteq X$
- $a$ 是 $A$ 的**内点**：有邻域包含之
- $A$ 是**开集**：各点均内点
	- 开球是开集（次可加性）

- $X = (X, ‖·‖)$ 在与其等价的范数上也开

- 度量空间中各点均有开邻域
	考虑 diameter of a metric space...
	Amann 书中仅仅提及度量空间的子集 d-bounded/bounded in X (w.r.t. d) 及其 diam

- $\mathcal{T}$ 为 $X$ 中开集的集族
	(1) $∅, X$ 开
	(2) 开集的任意并开
		（有类直和？）
	(3) 开集的有限（？）交开
		反例：$⋂(-1/n , 1/n)$
	- $M$ be a set, $\mathcal{T}\subseteq P(M)$ satisfying (1)-(3)
		- $\mathcal{T}$: $M$ 上拓扑，其中元素为开集。
			topology on $X$ induced from the metric $d$
			若 $X$ 赋范，$\mathcal{T}$ 范数拓扑
		- $(M, \mathcal{T})$: 拓扑空间

#### Closedness

Es sei $X$ ein metrischer Raum.
Eine Teilmenge $Y$ von $X$ heißt **abgeschlossen**, wenn für jede Folge $(y_n)$ in $Y$, die in $X$ konvergiert, gilt: $\lim y_n \in Y$.

 $A \subseteq X$
 - A 闭，若其补集开
	(1) $∅, X$ 闭
	(2) 闭集的任意交闭
	(3) 闭集的有限并闭
		反例：$⋃ (-1/n, 1/n)^c$ =$(-\infty, -1]⋃[1,\infty) ⋃ ... = \mathbb{R}\backslash\{0\}$
		$\{0\}$ 是单点集，故以上应是开集

c.f. cluster point of sequence: 任意邻域，无限多项。

 $A \subseteq X, x\in X$
- accumulation point of $A$: $x$ 的任意邻域与 $A$ 有交。
- limit point of $A$: $x$ 的任意邻域还包含 $A$ 中别的点。
	limit point $\subseteq$ accumulation point
- $\bar{A} =\{\text{accumulation points of }A\} = \text{cl}(A)$
	- $A \subseteq \bar{A}$
	- $A = \bar{A} \Longleftrightarrow A\text{ is closed}$

- limit point $\Longleftrightarrow$ $\exists\{x_n\} \in A\backslash\{x\}$ 收敛于 $x$
- accumulation point $\Longleftrightarrow$ $\exists\{x_n\} \in A$ 收敛于 $x$

- $A$ 是闭集
- $A$ 包含所有 limit points
- 所有在 $X$ 上收敛的 $\{x_n\}\in A^\mathbb{N}$，极限 $\in A$

闭包：最小闭集/包含之的闭集之交
- $\bar{A} =\{\text{accumulation points of }A\} = \text{cl}(A)$

内部：最大开集/含于其的开集之并
- $\overset{\circ}{A} =\{\text{interior points of }A\} = \text{int}(A)$

边界：$∂A := \bar{A}\backslash\overset{\circ}{A} = \bar{A}\cap(\overset{\circ}{A})^c$
- 边界是闭的
- $x$ 在边界上 $\Longleftrightarrow$ 任意邻域均与 $A$ 和 $\overset{\circ}{A}$ 有交

#### The Hausdorff Condition

$x\neq y\in X$，分别存在邻域使得二者无交。

一点的全部邻域，其交为 singleton

- 度量空间上的单点集为闭集。

- 度量空间均为 Hausdorff 空间