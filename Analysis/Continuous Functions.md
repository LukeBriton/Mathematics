We have the following chain of strict inclusions for functions over a closed and bounded non-trivial interval of the real line: 
- Continuously differentiable $⊂$ Lipschitz continuous $⊂$ $α$-Hölder continuous
where $0 < α ≤ 1$. We also have
- Lipschitz continuous $⊂$ absolutely continuous $⊂$ uniformly continuous $⊂$ continuous.

#### norm & metric

[vector spaces - Difference between metric and norm made concrete: The case of Euclid - Mathematics Stack Exchange](https://math.stackexchange.com/questions/38634/difference-between-metric-and-norm-made-concrete-the-case-of-euclid)

[general topology - Metric spaces and normed vector spaces - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1607957/metric-spaces-and-normed-vector-spaces)

#### Continuity

- More precisely, a function is continuous if arbitrarily small changes in its value can be assured by restricting to sufficiently small changes of its argument.
- En première approche, une fonction f est **continue** si, à des variations infinitésimales de l'[antécédent](https://fr.wikipedia.org/wiki/Ant%C3%A9c%C3%A9dent_\(math%C3%A9matiques\) "Antécédent (mathématiques)") x, correspondent des variations infinitésimales de l'[image](https://fr.wikipedia.org/wiki/Image_\(math%C3%A9matiques\) "Image (mathématiques)") _f_(_x_).

> [!note] 连续
>continuity/continuité/Stetigkeit
>Es sei $f:X\to Y$ zwischen den $(X, d_X)$ und $(Y, d_Y)$,
>$f$ ist stetig in $x_0\in X$:
>- 函数值的任意邻域，总包含自变量某个邻域的像。
>	$\forall V\ni f(x_0)$, $\exists U\ni x_0$, s.t. $f(U)\subseteq V$
>	- $\forall \varepsilon>0$, $\exists \delta>0$, s.t. $f\big(B_X(x_0,\delta)\big)\subseteq B_Y\big(f(x_0),\varepsilon\big).$
>- 列连续 Folgenstetigkeit
>	- Folgenkriterium
>	für jede Folge $(x_k)$ in $X$ mit $\lim x_k = x$ gilt: $\lim f(x_k) = f(x)$.
>		- „stetige Funktionen mit Grenzwertbildungen verträglich sind“
>		  $\lim f(x_k) = f(\lim x_k)$
>		  für jede konvergente Folge $(x_k)$ in $X$. Es sei $f: X \to Y$ stetige zwischen metrischen Räumen.
>- $f = (f_1, \dots, f_m) : X \to \mathbb{K}^m$ 各分量连续
>	$f(x_n) \to f(x) \iff f_k(x_n) \xrightarrow[n \to \infty]{} f_k(x), \quad k = 1, \dots, m.$
>	- $f : X \to \mathbb{C}$ 实部、虚部连续
>- （实变函数）左、右连续

- 若把它误读成“包含**所有**邻域的像”，就变成“局部常值”，太强。
	$\exists U\ni x_0$, $\forall V\ni f(x_0)$, s.t. $f(U)\subseteq V$
	then $f(U)\subseteq \bigcap_{V\ni f(x_0)} V$
	- In metric (indeed $T_1$) spaces, $\bigcap_{V\ni f(x_0)} V=\{f(x_0)\}$.
	  So $f(U)\subseteq \{f(x_0)\}$
	- Une **fonction localement constante** est une fonction définie sur un espace topologique, telle qu'en chaque point il existe un voisinage sur lequel la fonction est constante.

[Open and closed maps - Wikipedia](https://en.wikipedia.org/wiki/Open_and_closed_maps)
- "Strongly open map" if whenever $U$ is an open subset of the domain $X$, then $f(U)$ is an open subset of $f$'s codomain $Y$.
	$\forall U\ni x_0$, $\exists V\ni f(x_0)$, s.t. $V\subseteq f(U)$
https://dummit.cos.northeastern.edu/teaching_fa22_4555/complexanalysis_5_local_behavior_of_holomorphic_functions_v1.00.pdf
- More explicitly, nonconstant holomorphic functions are "locally onto": if $f (z_0) = w_0$, then near $z_0$, $f$ takes all values sufficiently near $w_0$, in the sense that for any $\epsilon > 0$ there exists an $r > 0$ such that for any $w$ with $|w − w_0| < r$, there exists some $z$ with $|z − z_0| < \epsilon$ with $f (z) = w$.
	$\forall U\ni x_0$, $\exists V\ni f(x_0)$, s.t. $V\subseteq f(U)$
- $f$ 在 $x_0$ 处把每个邻域映成 $f(x_0)$ 的一个邻域
	$\forall \delta>0$, $\exists \varepsilon>0$, s.t. $B_Y\big(f(x_0),\varepsilon\big)\subseteq f\big(B_X(x_0,\delta)\big).$

- $f(x_{0})$ 附近的值，总能被足够接近 $x_{0}$ 的点取到
	$\forall V\ni f(x_0)$, $\exists U\ni x_0$, s.t. $V\subseteq f(U)$
	- 例如 $f(x)=x^2$ 在 $x_0=0$ 连续，但 $f(U)$ 不可能覆盖 $0$ 的任何对称邻域（会缺少负数）

> [!note] 连续
>$f$ ist stetig:
>- $f^{-1}:\mathcal{T}_Y\to\mathcal{T}_X$
>	- 开集的前像为开
>	- 闭集的前像为闭
>	反之不亦然：
>		- $A=\{(x, y)\in \mathbb{R}^2| xy=1\}$ 闭，$\text{pr}_1(\cdot)$ 连续，但 $\text{pr}_1(A)$ 开。
>		- $y=x^2, x\in(-1,1), y\in[0,1)$

$\implies$ Dann ist für jedes $y \in Y$ die Faser $f^{-1}(y)$ von $f$ abgeschlossen in $X$, d.h., Lösungsmengen von Gleichungen mit stetigen Funktionen sind abgeschlossen.

$\implies$ Lösungsmengen von Ungleichungen Es seien $f : X \to \mathbb{R}$ stetig und $r \in \mathbb{R}$. Dann ist $\{ x \in X ; f(x) \le r \}$ abgeschlossen in $X$, und $\{ x \in X ; f(x) < r \}$ ist offen in $X$.
- $\{ x \in X ; f(x) \le r \} = f^{-1}((-\infty, r])$
- $\{ x \in X ; f(x) < r \} = f^{-1}((-\infty, r)) .$

- Abrundungsfunktion, auch Gaußklammer ($[x]$)
	$\lfloor \cdot \rfloor : \mathbb{R} \to \mathbb{R}$, $x \mapsto \lfloor x \rfloor:=\max\{k\in \mathbb{Z}; k\leq x\}$
	- stetig in $x_0 \in \mathbb{R} \setminus \mathbb{Z}$
	- rechtsseitig, aber nicht linksseitig stetig in $x_0 \in \mathbb{Z}$.
- Dirichletfunktion
	$$
	f(x) := \begin{cases} 1, & x \in \mathbb{Q}, \\ 0, & x \in \mathbb{R} \setminus \mathbb{Q}, \end{cases}
	$$
	ist nirgends stetig, d.h. in jedem Punkt unstetig.
- Lipschitz-stetig & Lipschitz-Konstante $α>0$
	$d(f(x), f(y)) \le \alpha d(x, y), \quad x, y \in X.$
- die kanonischen Projektionen
	Es seien $E_1, \dots, E_m$ normierte Vektorräume.
	Dann ist $E := E_1 \times \dots \times E_m$ bezüglich der Produktnorm $\|\cdot\|_{\infty}$ ein normierter Vektorraum.
	$\mathrm{pr}_k: E \to E_k, \quad x = (x_1, \dots, x_m) \mapsto x_k, \quad 1 \le k \le m,$
	- Jede $\mathrm{pr}_k$ ist Lipschitz-stetig.
	- $\mathrm{pr}_k: \mathbb{K}^m \to \mathbb{K}$
		- Der abgeschlossene $n$-dimensionale Einheitswürfel $I^n := \{ x \in \mathbb{R}^n ; 0 \le x_k \le 1, 1 \le k \le n \}$ ist abgeschlossen in $\mathbb{R}^n$.
			$$
			  I^n = \bigcap_{k=1}^{n} (\{ x \in \mathbb{R}^n ; \text{pr}_k(x) \le 1 \} \cap \{ x \in \mathbb{R}^n ; \text{pr}_k(x) \ge 0 \} )
			  $$
	- Es seien $k, n \in \mathbb{N}^\times$ mit $k \le n$. Dann ist $\mathbb{K}^k$ abgeschlossen in $\mathbb{K}^n$.
		- $\mathrm{pr} : \mathbb{K}^n \to \mathbb{K}^{n-k} , \quad (x_1, \dots, x_n) \mapsto (x_{k+1}, \dots, x_n) .$
			- $\mathbb{K}^k = \mathrm{pr}^{-1}(0)$
	- $z \mapsto \mathrm{Re}(z)$, $z \mapsto \mathrm{Im}(z)$
- Abstandsfunktion
	Abstand von $x$ zu $M$
	$d(\cdot, M):X\to \mathbb{R}, x\mapsto d(x,M):=\inf_{m∈M} d(x,m)$
	- Lipschitz-stetig
- Isometrie
	$d(f(x), f(x')) = d(x, x')$ für $x, x' \in X$ gilt
	- „die Abstände erhält“
	- In general not bijective 
	  [group theory - Prove that an isometry is a bijection - Mathematics Stack Exchange](https://math.stackexchange.com/questions/498985/prove-that-an-isometry-is-a-bijection)
	  [metric spaces - If $f: M\to M$ an isometry, is $f$ bijective? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/340326/if-f-m-to-m-an-isometry-is-f-bijective)
	- Sind $E$ und $F$ normierte Vektorräume und ist $T: E \to F$ linear,
		so ist $T$ genau dann eine Isometrie, wenn gilt $\|Tx\| = \|x\|, \quad x \in E.$
		- isometrischer Isomorphismus
			$T$ ist außerdem surjektiv
			- $T^{-1}: F \to E$ ist ebenfalls isometrisch.
- Vektorraum der stetigen Abbildungen $C(X, F)\subseteq F^X$
	Es seien $X$ ein metrischer Raum, $F$ ein normierter Vektorraum.
	$f : \text{dom}(f) \subseteq X \to F$, $g : \text{dom}(g) \subseteq X \to F$
		seien stetig in $x_0 \in \text{dom}(f) \cap \text{dom}(g)$.
	- die Summe von $f$ und $g$
		$\text{dom}(f + g) := \text{dom}(f) \cap \text{dom}(g)$
		$f + g : \text{dom}(f + g) \to F,$ $x \mapsto f(x) + g(x)$
	- das $\lambda$-fache von $f$ und $g$
		$\lambda f : \text{dom}(f) \to F,$ $x \mapsto \lambda f(x)$
	- $f + g$ und $\lambda f$ sind stetig in $x_0$.
	Gilt $F = \mathbb{K}$
	- $\text{dom}(f \cdot g) := \text{dom}(f) \cap \text{dom}(g)$
		$f \cdot g : \text{dom}(f \cdot g) \to \mathbb{K}, \quad x \mapsto f(x) \cdot g(x)$ ist stetig in $x_0$.
	Gelten $F = \mathbb{K}$ und $g(x_0) \neq 0$
	- $\text{dom}(f/g) := \text{dom}(f) \cap \{ x \in \text{dom}(g) ; g(x) \neq 0 \}$
		$f/g : \text{dom}(f/g) \to \mathbb{K}, \quad x \mapsto f(x)/g(x)$ ist stetig in $x_0$.
	- 有理函数 连续
	- $\mathbb{K}^n$ 上多项式 连续

- Stetigkeit von Kompositionen
	Es seien $X$, $Y$ und $Z$ metrische Räume.
	Ferner sei $f: X \to Y$ stetig in $x \in X$, und $g: Y \to Z$ sei stetig in $f(x) \in Y$.
	- Dann ist die Komposition $g \circ f: X \to Z$ stetig in $x$.
	- Die Umkehrung ist falsch, d.h., aus der Stetigkeit von $g \circ f$ folgt i. allg. nicht, daß $f$ oder $g$ stetig ist.
- Es sei $f: X \to E$ stetig in $x_0$.
	- Dann ist die Norm von $f$,
	  $\|f\|: X \to \mathbb{R}, \quad x \mapsto \|f(x)\|$ stetig in $x_0$.
	- Die Exponentialfunktion $\exp: \mathbb{C} \to \mathbb{C}$ ist stetig.

- Einseitige Stetigkeit 单边连续 （限于 $\mathbb{R}$ 上序结构）
	$f(x_{0})$ 的邻域，总包含 $x_{0}$ 的某个左/右 $δ$-邻域
	- 左/右连续 $\Longleftrightarrow$ 小于/大于其的序列收敛

- sign
	$$
	\operatorname{sign} : \mathbb{R} \to \mathbb{R}, \quad x \mapsto \begin{cases} -1, & x < 0, \\ 0, & x = 0, \\ 1, & x > 0, \end{cases}
	$$
	- ist in 0 weder linksseitig noch rechtsseitig stetig.

- zigzag/?/Zack
	$$
	\text{zigzag}(x) := |\lfloor x + 1/2 \rfloor - x|, \quad x \in \mathbb{R},
	$$
	- (a) $\text{zigzag}(x) = |x|$ für $|x| \le 1/2$.
	- (b) $\text{zigzag}(x+n) = \text{zigzag}(x)$, $x \in \mathbb{R}$, $n \in \mathbb{Z}$.
	- (c) $\text{zigzag}$ ist stetig.

- Die Funktion
	$$
	f: \mathbb{Q} \to \mathbb{R}, \quad x \mapsto \begin{cases} 0, & x < \sqrt{2}, \\ 1, & x > \sqrt{2}, \end{cases}
	$$
	ist stetig.

- Es sei $f: \mathbb{R} \to \mathbb{R}$ ein stetiger Homomorphismus der additiven Gruppe $(\mathbb{R}, +)$.
	- Man zeige$^8$, daß $f$ linear ist, d.h., daß es ein $a \in \mathbb{R}$ gibt mit $f(x) = ax$, $x \in \mathbb{R}$.
	  (Hinweis: Für $n \in \mathbb{N}$ gilt $f(n) = nf(1)$. Daraus schließe man, daß $f(q) = qf(1)$ für $q \in \mathbb{Q}$ gilt die Dichtheit von $\mathbb{Q}$ in $\mathbb{R}$)
		- für $n\in\mathbb N$:
		  $$
		  f(n)=f(\underbrace{1+\cdots+1}_{n\text{-mal}})
=\underbrace{f(1)+\cdots+f(1)}_{n\text{-mal}}
=nf(1)=an.
		  $$
		  - für $m\in\mathbb Z$:
		    - $0=f(0)=f(n+(-n))=f(n)+f(-n)$
			- $f(-n)=-f(n)$
			$f(m)=am$
		- für $q\in\mathbb Q$, etwa $q=\frac mn$ mit $m\in\mathbb Z$, $n\in\mathbb N\setminus{0}$.
			$$
			n f(q)=\underbrace{f(q)+\cdots+f(q)}_{n\text{-mal}}=f(nq)=f(m)=am.
			$$
		- Wähle eine Folge rationaler Zahlen $(q_k)$ mit $q_k\to x$
			$$
			f(x)=f\left(\lim_{k\to\infty} q_k\right)
=\lim_{k\to\infty} f(q_k)
=\lim_{k\to\infty} a q_k
=a x.
			$$
			mit $a=f(1)$
	
	- Man kann beweisen, daß es unstetige Homomorphismen von $(\mathbb{R}, +)$ gibt.
	  Solche konstruiert man mithilfe einer Hamelbasis von $\mathbb{R}$ über $\mathbb{Q}$.
- Es seien $V$ und $W$ normierte Vektorräume, und $f: V \to W$ sei ein stetiger Gruppenhomomorphismus von $(V, +)$ nach $(W, +)$. Man beweise, daß $f$ linear ist.
  (Hinweis: Es seien $\mathbb{K} = \mathbb{R}$, $x \in V$ und $q \in \mathbb{Q}$. Dann gilt $f(qx) = qf(x)$.)
	- Wähle eine Folge rationaler Zahlen $(q_k)$ mit $q_k\to q$
		Dann gilt in $V$ $q_k x\to q x$
	- denn die Skalarmultiplikation ist in einem normierten Vektorraum stetig
		$\|q_kx-q x\|=|q_k-q|\|x\|\to 0$
	- Daher gilt
	  $$
	  f(qx) = \lim_{k\to\infty} f(q_kx) = \lim_{k\to\infty} q_k f(x) = qf(x)
	  $$
	- a $\mathbb{R}$-linear map $f:\mathbb{C}→\mathbb{C}$ is $\mathbb{C}$-linear iff $f(i)=if(1)$.
	- [complex analysis - Difference between $\mathbb{R}$-linear and $\mathbb{C}$-linear maps - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1147609/difference-between-mathbbr-linear-and-mathbbc-linear-maps)
 
- Es sei $X$ ein metrischer Raum, und $f, g \in \mathbb{R}^X$ seien stetig in $x_0$. Man beweise oder widerlege:
	- $|f|$
	- $f^+ := 0 \vee f=\frac{f+|f|}{2}$
	- $f^- := 0 \vee (-f) = \frac{|f|-f}{2}$
	- $f\vee g=\frac{f+g+|f-g|}{2}$
	- $f\wedge g=\frac{f+g-|f-g|}{2}$
	sind stetig in $x_0$.

- Man betrachte die Abbildung
	$$
	f: \mathbb{R}^2 \to \mathbb{R}, \quad (x, y) \mapsto \begin{cases} xy/(x^2 + y^2), & (x, y) \neq (0, 0), \\ 0, & (x, y) = (0, 0), \end{cases}
	$$
	und setze für ein festes $x_0 \in \mathbb{R}$:
	$$
	f_1: \mathbb{R} \to \mathbb{R}, \quad x \mapsto f(x, x_0), \quad f_2: \mathbb{R} \to \mathbb{R}, \quad x \mapsto f(x_0, x).
	$$
	Dann gelten:
	- (a) $f_1$ und $f_2$ sind stetig.
	- (b) $f$ ist stetig in $\mathbb{R}^2 \setminus \{(0,0)\}$ und unstetig in $(0,0)$. (Hinweis: Für eine Nullfolge $(x_n)$ betrachte man $f(x_n, x_n)$.)

- Man zeige, daß jede lineare Abbildung von $\mathbb{K}^n$ nach $\mathbb{K}^m$ Lipschitz-stetig ist.
	 - Do we need Choice to pick a basis?
		Not here.
		For $\mathbb K^n$ and $\mathbb K^m$, there is already a canonical basis:
		 $e_1=(1,0,\dots,0),\dots,e_n=(0,\dots,0,1).$
		 So no Axiom of Choice issue arises.
		More generally, for an arbitrary finite-dimensional vector space, one can construct a basis directly from a finite spanning set; this also does not require the full Axiom of Choice.
	- Is a basis only meaningful in an inner product space?
		No. A **basis** makes sense in every vector space.
		What needs an inner product is the notion of an **orthonormal basis**. So your instinct “all bases are created equal for linearity” is basically right.
	- Is componentwise continuity enough?
		Yes, in finite products it is. But for Lipschitz continuity, the cleanest route is usually a direct norm estimate, not a componentwise argument.
	
	Let $f:\Bbb K^n\to\Bbb K^m$ be linear and fix any norms $\|\cdot\|_n$ on $\Bbb K^n$ and $\|\cdot\|_m$ on $\Bbb K^m$.
	Set
	$$
	\|A\|_{\mathrm{op}} := \sup_{\|x\|_n=1} \|Ax\|_m
	$$
	In finite dimensions this is **finite** (e.g., represent $f$ by a matrix and use an entrywise bound, or use compactness of the unit sphere). Then for all $x,y$,
	$$
	\|f(x)-f(y)\|_m = \|A(x-y)\|_m \le \|A\|_{\mathrm{op}}\|x-y\|_n,
	$$
	so $f$ is Lipschitz with constant $\alpha=\|f\|_{\mathrm{op}}$.
	
	If you specifically use Euclidean norms, $\alpha$ can be taken to be the largest singular value of the matrix of $f$ (i.e., $\alpha=\sqrt{\lambda_{\max}(M^*M)})$.
	
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
- Es sei $A \in \text{End}(\mathbb{K}^n)$. Man beweise, daß die Abbildung 
	$$
	\mathbb{K}^n \to \mathbb{K}, \quad x \mapsto (Ax|x)
	$$
	stetig ist. 
	- $\mathbb K^n\xrightarrow{\Phi}\mathbb K^n \times \mathbb K^n\xrightarrow{\langle\cdot,\cdot\rangle}\mathbb K, x\mapsto (Ax,x)\mapsto (Ax\mid x)$

- Es seien $X$ und $Y$ metrische Räume und $f: X \to Y$. Dann heißt die Funktion
	$$
	\omega_f(x, \cdot) : (0, \infty) \to \mathbb{R}, \quad \varepsilon \mapsto \sup_{y,z \in \mathbb{B}(x, \varepsilon)} d(f(y), f(z))
	$$
	**Stetigkeitsmodul** von $f$ in $x \in X$. Wir setzen
	$$
	\omega_f(x) := \inf_{\varepsilon>0} \omega_f(x, \varepsilon) .
	$$
	Man zeige, daß $f$ genau dann in $x$ stetig ist, wenn $\omega_f(x) = 0$ gilt.
	- [real analysis - What exactly is a modulus of continuity? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/681580/what-exactly-is-a-modulus-of-continuity)

- Die Wurzelfunktion $w: \mathbb{R}^+ \to \mathbb{R}$, $x \mapsto \sqrt{x}$ ist stetig, aber nicht Lipschitz-stetig.
	- Jedoch ist $w|_{[a, \infty)}$ für jedes $a > 0$ Lipschitz-stetig.

#### Compactness

$X:=(X,d)$ 中
- 覆盖：能盖住所给集合的一族集合
- 开覆盖：各集均开
- 紧：任意开覆盖，有有限开覆盖子集。
	任意开覆盖，有有限子覆盖。