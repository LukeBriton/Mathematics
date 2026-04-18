> Der Begriff der Konvergenz erlaubt uns
> - to add together infinite sets of numbers (or vectors)
> - unendlich viele (Rechen-)Operationen durchzuführen
> was die Analysis von der Algebra unterscheidet.

#### Cluster Points

> [!note] 聚点
>- 任意邻域，总有无穷多项。
>- 任意邻域，任意尾列，总有项。
>- 任意 $ε$ ，任意尾列，总有项在 $ε$-开球里。
>	任意 $ε$-开邻域 ，任意尾列，总有项。

$$
\varphi: \mathbb{N} \longleftrightarrow \mathbb{Q}, x_{n}:=\varphi(n)\implies\forall x\in \mathbb{R}\text{ is a cluster point of }(x_{n}).
$$

#### Convergence of sequences

> [!note] 收敛
>- 任意邻域，几乎所有项。
>- 任意邻域，总有尾列。
>- 任意 $\varepsilon$，总有尾列在 $ε$-开球里。
> 	任意 $ε$-开邻域 ，总有尾列。
	 收敛的条件比聚点更强。

- 收敛$\implies$有界
- 收敛$\implies$有唯一聚点/极限
	有唯一聚点$\cancel{ \implies }$收敛
- 有界+有聚点$\cancel{ \implies }$收敛
	- [real analysis - Show a bound sequence with a cluster point is indeed convergent - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1014909/show-a-bound-sequence-with-a-cluster-point-is-indeed-convergent)
	- [general topology - In what metric spaces does bounded + unique limit point imply convergence of a sequence? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4762540/in-what-metric-spaces-does-bounded-unique-limit-point-imply-convergence-of-a-s)
	- [ca.classical analysis and odes - Sequence that converge if they have an accumulation point - MathOverflow](https://mathoverflow.net/questions/24508/sequence-that-converge-if-they-have-an-accumulation-point)
	- [Simple examples of proper metric spaces? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/792253/simple-examples-of-proper-metric-spaces)

- 收敛$\implies$子列收敛于聚点
- 是聚点 $\Longleftrightarrow$ 有子列收敛焉
	$$
	n_0 := 0, \quad n_k := \min\{m \in \mathbb{N} ; m > n_{k-1}, x_m \in \mathbb{B}(a, 1/k)\}, \quad k \in \mathbb{N}^\times.
	$$
	Nun schließen wir aus dem Wohlordnungsprinzip, daß $n_k$ für jedes $k ∈ \mathbb{N}^×$ wohldefiniert ist.
	
- 比较审敛
	Es seien $(x_n)$, $(y_n)$ konvergente Folgen in $\mathbb{R}$. Ferner gelte $x_n \le y_n$ für unendlich viele $n \in \mathbb{N}$. Dann folgt:
	$$
	\lim x_n \le \lim y_n .
	$$
	- aus $x_n < y_n$ folgt nicht $\lim x_n < \lim y_n$.
- 夹逼定理
	Es seien $(x_n)$, $(y_n)$ und $(z_n)$ reelle Zahlenfolgen mit $x_n \le y_n \le z_n$ für fast alle $n \in \mathbb{N}$, und es gelte
	$$\lim x_n = \lim z_n =: a.$$
	Dann konvergiert auch $(y_n)$ gegen $a$.
- 收敛 $\Longleftrightarrow$ 绝对值收敛
- 收敛 $\Longleftrightarrow$ 各分量收敛 （little to be gained）
	- 复数列收敛 $\Longleftrightarrow$ 实部、虚部收敛

- product metric on $X := X_1 \times \cdots \times X_m$, $(X_j, d_j)$, $1 \le j \le m$
	$(x_n) = ((x_n^1, \dots, x_n^m))_{n \in \mathbb{N}}$
	$a := (a^1, \dots, a^m)$
	$\lim x_n \to a \iff \lim x_n^j \to a^j$.
	- a sequence of vectors is convergent iff the sequences of its components are convergent (? by equivalence of metrics)
- Es seien $m \in \mathbb{N}^\times$ und $x_n = (x_n^1, \dots, x_n^m) \in \mathbb{K}^m$ für $n \in \mathbb{N}$. Dann sind äquivalent:
	- (i) Die Folge $(x_n)_{n \in \mathbb{N}}$ konvergiert in $\mathbb{K}^m$ gegen $x = (x^1, \dots, x^m)$.
	- (ii) Für jedes $k \in \{1, \dots, m\}$ konvergiert die Folge $(x_n^k)_{n \in \mathbb{N}}$ in $\mathbb{K}$ gegen $x^k$. (komponentenweise Konvergenz)
	Eine Folge in $\mathbb{K}^m$ konvergiert genau dann, wenn sie komponentenweise konvergiert.


- Bolzano-Weierstraß
	$\mathbb{K}^m$ 上有界 $\implies$ 有收敛子列&聚点

- 收敛 $\implies$ Cauchy列
	完备：Cauchy列 $\implies$ 收敛 

#### Bounded Sets

bounded/beschränkt
- $d$-beschränkt/beschränkt in $X$ (bezüglich der Metrik $d$)
	Eine Teilmenge $Y \subseteq X$, $\exists M > 0, \forall x, y \in Y, d(x, y) \le M$.
	$\text{diam}(Y) := \sup\limits_{x,y \in Y} d(x, y)$
	$d(x,y)$ 上有界，$\sup{d(x,y)}$ 为直径。
- normbeschränkt/beschränkt in $E$
	in dem von der Norm induzierten metrischen Raum beschränkt ist.
	- $X \subseteq E$ ist beschränkt $\iff$ Es ein $r > 0$ gibt mit $X \subseteq r\mathbb{B}$.

- 像集有界，数列有界
- 像集有界，函数有界
	- Supremumsnorm
		Für $u \in E^X$ setzen wir
		$\|u\|_{\infty} := \|u\|_{\infty, X} := \sup\limits_{x \in X} \|u(x)\| \in \mathbb{R}^{+} \cup \{\infty\}.$

- 有界函数向量空间
	$$
	B(X,E):=(B(X, E), ‖·‖_{∞}):=\{ u ∈ E^X ; u\text{ ist beschränkt} \}
	$$
	ist ein Untervektorraum von $E^X$
	- $(E, ‖·‖)$ Banach $\implies$ $B(X,E)$ Banach
		- $B(E, F ) ∩ \text{Hom}(E, F ) = {0}.$
	- 有界数列向量空间 $\ell_{\infty}$

#### Monotone Sequences

- 单调有界，收敛于确界
	Jede wachsende (bzw. fallende) beschränkte Folge $(x_n)$ in $\mathbb{R}$ konvergiert, und es gilt
	$$
	x_n \uparrow \sup\{x_n; n \in \mathbb{N}\} \quad (\text{bzw. } x_n \downarrow \inf\{x_n; n \in \mathbb{N}\})
	$$
- 一些个重要极限（我好嫌计算。。）

#### Infinite Limits

- $\bar{\mathbb{R}}$ 上无合适度量，以ad hoc定义扩展 $\mathbb{R}$。
	- $\bar{\mathbb{R}}$ 上“收敛”包括趋于无穷（converge improperly）。
	- $\mathbb{R}$ 中单调数列在 $\bar{\mathbb{R}}$ 上“收敛”。

- $\bar{\mathbb{R}}$ 中的上下极限（**任意**数列均有）
	- Limes superior (der kleinste Häufungspunkt)
		$$
		\limsup := \overline{\lim}\limits_{n \to \infty} x_n := \lim_{n \to \infty} \left( \sup_{k \ge n} x_k \right) = \inf_{n \in \mathbb{N}} \left( \sup_{k \ge n} x_k \right)
		$$
	- Limes inferior (der größte Häufungspunkt)
		$$
		\liminf := \underline{\lim}\limits_{n \to \infty} x_n := \lim_{n \to \infty} \left( \inf_{k \ge n} x_k \right) = \sup_{n \in \mathbb{N}} \left( \inf_{k \ge n} x_k \right)
		$$
	- $\bar{\mathbb{R}}$ 上收敛 $\Longleftrightarrow$ $\overline{\lim} x_n \le \underline{\lim} x_n$

#### Completeness

Cauchyfolgen
- 任意 $\varepsilon$，总有尾列，任两项距离小于 $\varepsilon$。
- translationsinvariant
	Sind $(x_n)$ eine Cauchyfolge und $a$ ein beliebiger Vektor in $E$, so ist auch die „um $a$ verschobene“ Folge $(x_n + a)$ eine Cauchyfolge.
	- Dies zeigt insbesondere, daß Cauchyfolgen *nicht* mit Umgebungen beschrieben werden können.
	- [Translation invariant metrics and topological groups - Mathematics Stack Exchange](https://math.stackexchange.com/questions/976933/translation-invariant-metrics-and-topological-groups)
- 收敛 $\implies$ Cauchy列
	Cauchy列$\cancel{\implies}$收敛
- Cauchy列 $\implies$ 有界
- Cauchy列有收敛子列 $\implies$ 收敛

completeness/complétude/Vollständigkeit
complete/complet/vollständig
- Cauchy列 $\implies$ （有界 $\implies$ 有收敛子列 $\implies$）收敛 
- Die Vollständigkeit eines normierten Vektorraumes $E$ ist invariant unter Übergang zu äquivalenten Normen
- $\mathbb{K}^m$ ist ein Banachraum.
- Es seien $X$ eine nichtleere Menge und $E = (E, \|\cdot\|)$ ein Banachraum.
	Dann ist auch $B(X, E)$ ein Banachraum.

- $\mathbb{Q}^\mathbb{N}$ 有幺交换环
	- $\bar{a}=(a,a,\dots,a)$，则 $\bar{1}$ 为其幺元
	- $\mathcal{R}:=\{\text{Cauchy sequences}\in \mathbb{Q}^\mathbb{N}\}$ 是其子环 From Exercise I.8.6, we know that $\mathcal{R}$ cannot be a field （？）
	- $\mathbf{c}_{0}:=\{\text{Null sequences}\in \mathbb{Q}^\mathbb{N}\}$ 是 $\mathcal{R}$ 的非平凡真理想
	- $R = \mathcal{R}/\mathbf{c}_{0}$
		$\mathbb{Q}\to R, a\mapsto [\bar{a}]=\bar{a}+\mathbf{c}_{0}$ 入射，$\mathbb{Q}$ 作为 $R$ 的子环
		$\mathcal{P}:=\{\text{strictly positive sequences}\in \mathcal{R}\cup\mathbf{c}_{0}\}$
		- $(R, \le)$ 有序环，在$\mathbb{Q}$上诱导自然序
			$[r]<[s]:\Leftrightarrow s-r\in\mathcal{P}$
		- $R$ 是域
		- $\mathbb{Q}$ 上单调有界序列 $\implies$ Cauchy
		- $R$ 中单调有界序列 $\implies$ 有确界
		- $R$ 是 $\mathbb{Q}$ 的有序域扩张

#### Convergence of Series

- 级数收敛:=部分和序列收敛

- $\sum x_{k}$ 收敛 $\implies$ $(x_{k})$ 零列

- 调和级数发散（非柯西列）
- 几何级数 $|a|?1$

- Cauchy-Kriterium
	部分和序列是 Cauchy 列
- 非负级数 $∑x_{k} \text{ mit } x_k \ge 0$
	$∑ x_k < ∞ \Longleftrightarrow ∑ x_k \text{ konvergiert}$
- Alternierende Reihen 交错级数
  $± ∑(−1)^kx_{k} \text{ mit } x_{k}\ge{0}$
	- Leibnizsches-Kriterium
		$(x_{k})$ 非负单减零列 $\implies$ $∑(−1)^kx_{k}$ 收敛
	- 交错调和级数

- 实数的各进制展开

- $\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{Z}, x\to \lfloor x \rfloor$

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
	\begin{tikzcd}
		\mathsf{\mathbb{R}}
		\arrow[bend left=50, r, "\mathrm{floor\ or\ ceiling}", ""' name=U]
		\arrow[bend right=50, r, "" name=D, "\supset"'] &
		\mathsf{\mathbb{Z}} &
		
	\end{tikzcd}
\end{document}
```

- $g\ge{2}$ 各实数均有 base $g$ expansion
	- This expansion is unique if expansions satisfying $x_{k} = g − 1$ for almost all $k ∈ N$ are excluded. (e.g. $1.94\dot{9}$)
	- $x$ is a rational number if and only if its base $g$ expansion is periodic
	 $x=\lfloor x \rfloor+r,\ r\in[0, 1)$
		Too many technical details...

#### Absolute Convergence

absolut/bedingt konvergent
- 绝对收敛 $\implies$ 收敛
- 条件收敛

- Majorantenkriterium 强级数（majorant）审敛准则
	- $\sum x_k$ in $E$ und $\sum a_k$ in $\mathbb{R}^+$.
		  Dann heißt die Reihe $\sum a_k$ **Majorante** (bzw. **Minorante**) für $\sum x_k$:
		  falls es ein $K \in \mathbb{N}$ gibt mit $|x_k| \le a_k$ für alle $k \ge K$ (bzw. $a_k \le |x_k|$). 
	- (in einem Banachraum) 有强级数 $\implies$ 绝对收敛
- Wurzelkriterium 根值审敛法
	$α:=\overline{\lim}\sqrt[k]{|x_{k}|}$
	$α<1$: konvergiert absolut
	$α>1$: divergiert
	$α=1$: oder
- Quotientenkriterium 比值审敛法
	$K_0 \text{ mit } x_{k} \neq 0 \text{ für } k\geq K_{0}$
	$\exists K \geq K_{0}$
	- $\exists q\in(0,1), \frac{|x_{k+1}|}{|x_{k}|}\le q, k\geq K$: konvergiert absolut
	- $\frac{|x_{k+1}|}{|x_{k}|}\ge 1, k\geq K$: divergiert

- die Exponentialfunktion 指数函数
	$\text{exp}:\mathbb{C}\to \mathbb{C}, z\mapsto \sum\limits_{k=0}^\infty \frac{z^k}{k!}$
	- Exponentialreihe: $\sum z^k/k!$
	- die Funktionalgleichung der Exponentialfunktion
	  $\exp(x) \cdot \exp(y) = \exp(x + y), \quad x, y \in \mathbb{C}$
	- $\exp(r) = e^r, \quad r \in \mathbb{Q},$

- rearrangement/réarrangement/Umordnung/重排
	- Ist $\sigma$ eine Permutation von $\mathbb{N}$ mit $\sigma(k) = k$ für fast alle $k \in \mathbb{N}$, so haben $\sum x_k$ und $\sum_k x_{\sigma(k)}$ das gleiche Konvergenzverhalten, und ihre Werte stimmen überein, falls die Reihen konvergieren.
	- Das Kommutativgesetz der Addition für „unendlich viele Summanden“ im allgemeinen nicht gilt, d.h., eine konvergente Reihe kann nicht beliebig umgeordnet werden, ohne ihren Wert zu verändern.
	- Umordnungssatz 重排定理
		绝对收敛 $\implies$ 重排绝对收敛&值相同
- double series/séries double/Doppelreihen/
	$x_{jk}:=x(j, k)=x: \mathbb{N} \times \mathbb{N} \to E$
	Die Abbildung $x$ kann im doppelt-unendlichen Schema
	$$
	\begin{array}{ccccc}
x_{00} & x_{01} & x_{02} & x_{03} & \dots \\
x_{10} & x_{11} & x_{12} & x_{13} & \dots \\
x_{20} & x_{21} & x_{22} & x_{23} & \dots \\
x_{30} & x_{31} & x_{32} & x_{33} & \dots \\
\vdots & \vdots & \vdots & \vdots & \ddots
\end{array}
	$$
	dargestellt werden.
	- Die Menge $\mathbb{N} \times \mathbb{N}$ ist abzählbar, d.h., es gibt eine Bijektion $\alpha: \mathbb{N} \to \mathbb{N} \times \mathbb{N}$, eine **Abzählung** von $\mathbb{N} \times \mathbb{N}$. Ist $\alpha$ eine solche Abzählung, so nennen wir die Reihe $\sum_n x_{\alpha(n)}$ **Anordnung** der Doppelreihe $\sum x_{jk}$.
	- Fixieren wir $j \in \mathbb{N}$ bzw. $k \in \mathbb{N}$, so heißen die Reihen $\sum_k x_{jk}$ bzw. $\sum_j x_{jk}$ $j$-te **Zeilenreihe** bzw. $k$-te **Spaltenreihe** von $\sum x_{jk}$.
	Konvergiert jede Zeilen- bzw. jede Spaltenreihe, so können wir die **Reihe der Zeilensummen** $\sum_j (\sum_{k=0}^{\infty} x_{jk})$ bzw. die **Reihe der Spaltensummen**$^5$ $\sum_k (\sum_{j=0}^{\infty} x_{jk})$ betrachten.
	- Wir nennen die Doppelreihe $\sum x_{jk}$ **summierbar**, wenn
		$$
		\sup_{n \in \mathbb{N}} \sum_{j,k=0}^{n} |x_{jk}| < \infty
$$
		gilt.
- Doppelreihensatz
	Es sei $\sum x_{jk}$ eine summierbare Doppelreihe. Dann gelten folgende Aussagen:
	- (i) Jede Anordnung $\sum_n x_{\alpha(n)}$ von $\sum x_{jk}$ konvergiert absolut gegen einen von der Abzählung $\alpha$ unabhängigen Wert $s \in E$.
	- (ii) Die Reihe der Zeilensummen $\sum_j (\sum_{k=0}^{\infty} x_{jk})$ und die Reihe der Spaltensummen $\sum_k (\sum_{j=0}^{\infty} x_{jk})$ konvergieren absolut, und es gilt
		$$
		\sum_{j=0}^{\infty} \left( \sum_{k=0}^{\infty} x_{jk} \right) = \sum_{k=0}^{\infty} \left( \sum_{j=0}^{\infty} x_{jk} \right) = s .
		$$

- Cauchyprodukte/Faltungsprodukt
	$$
	\sum_j x_{\delta(j)} = \sum_n z_n = \sum_n \left( \sum_{k=0}^{n} x_k y_{n-k} \right) .
	$$
	- Cauchyprodukte von Reihen
	  Die Reihen $\sum x_j$ und $\sum y_k$ seien absolut konvergent in $\mathbb{K}$. Dann konvergiert das Cauchyprodukt $\sum_n \sum_{k=0}^n x_k y_{n-k}$ von $\sum x_j$ und $\sum y_k$ absolut, und es gilt
	  $$
	  \left(\sum_{j=0}^{\infty} x_j\right) \left(\sum_{k=0}^{\infty} y_k\right) = \sum_{n=0}^{\infty} \sum_{k=0}^{n} x_k y_{n-k} .
	  $$
		- Es ist für bedingt konvergente Reihen i. allg. falsch.

- Es sei $\sum x_k$ eine bedingt konvergente Reihe in $\mathbb{R}$.
  Wir setzen $x^+ := \max\{x, 0\}$ und $x^- := \max\{-x, 0\}$ für $x \in \mathbb{R}$.
	- Die Reihen $\sum x_k^+$ und $\sum x_k^-$ divergieren.
	Beweis:
	- $\sum x_k^+ - \sum x_k^- =\sum x_k<\infty$
	- $\sum x_k^+ + \sum x_k^- = \sum |x_k|=\infty$
	$\implies \sum x_k^+ =\infty, \sum x_k^- =\infty$

> Since $x_k=x_k^+-x_k^-$ and $|x_k|=x_k^++x_k^-$, for the partial sums
> $$
P_n=\sum_{k=1}^n x_k^+,\quad N_n=\sum_{k=1}^n x_k^-,\quad S_n=\sum_{k=1}^n x_k
$$
> we have
> $$
S_n=P_n-N_n,\qquad \sum_{k=1}^n|x_k|=P_n+N_n.
$$
> If $P_n$ were bounded, then as an increasing sequence it would converge; since $S_n\to s$, also $N_n=P_n-S_n$ would converge. Hence $P_n+N_n$ would converge, contradicting $\sum|x_k|=\infty$. Therefore $P_n\to+\infty$. Similarly $N_n\to+\infty$.

- der **Umordnungssatz von Riemann**
  Ist $\sum x_k$ eine bedingt konvergente Reihe in $\mathbb{R}$,
	- so gibt es zu jeder Zahl $s \in \mathbb{R}$ eine Permutation $\sigma$ von $\mathbb{N}$ mit $\sum_k x_{\sigma(k)} = s$.
	- Ferner gibt es eine Permutation $\tau$ von $\mathbb{N}$, so daß $\sum_k x_{\tau(k)}$ divergiert.
  (Hinweis: Man verwende Aufgabe 3 und approximiere $s \in \mathbb{R}$ von oben und von unten durch geeignete Kombinationen von Partialsummen der Reihen $\sum x_k^+$ und $-\sum x_k^-$.)
	- Konstruktion einer Umordnung mit Summe $s$:
		Deshalb kann man durch positives Aufaddieren die Zielzahl $s$ von unten überschreiten und durch negative Glieder wieder von oben unterschreiten. Da die letzten „Überschreitungs-“ bzw. „Unterschreitungs-“Schritte immer kleiner werden, nähern sich die Partialsummen $s$ an.
	- Konstruktion einer divergenten Umordnung
		Wir machen fast dasselbe, nur mit wechselnden Schranken:
		- Nimm positive Glieder, bis die Summe (>1) ist.
		- Dann negative Glieder, bis die Summe (<0) ist.
		- Dann wieder positive Glieder, bis die Summe (>2) ist.
		- Dann negative Glieder, bis die Summe (<0) ist.
		- Dann positive Glieder, bis die Summe (>3) ist.
		- usw.


- $ℓ_1$ space
