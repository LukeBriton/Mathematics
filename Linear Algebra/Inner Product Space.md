#### Basics

- das Skalarprodukt (auch inneres Produkt oder Punktprodukt) 
	$(\cdot|\cdot) : E \times E \to \mathbb{K} , \quad (x, y) \mapsto (x|y)$ with 共轭对称、半双线性、正定
	- konjugiert symmetrisch
		$\mathbb{K} = \mathbb{R}$: symmetrisch
		$\mathbb{K} = \mathbb{C}$: hermitesch
	- konjugiert linear
		$\mathbb{K} = \mathbb{R}$: Bilinearform
		$\mathbb{K} = \mathbb{C}$: Sesquilinearform
- Prähilbertraum/Innenproduktraum $(E, (\cdot|\cdot))$
- das euklidische innere Produkt
	Für $m \in \mathbb{N}^\times$ und $x = (x_1, \dots, x_m)$ und $y = (y_1, \dots, y_m)$ in $\mathbb{K}^m$ setzen wir
	$$
	(x|y) := \sum_{j=1}^{m} x_j \overline{y}_j.
	$$
- Die Cauchy-Bunjakowski-Schwarz-Ungleichung
	Es sei $(E, (\cdot|\cdot))$ ein Innenproduktraum. Dann gilt  
	$|(x|y)|^2 \le (x|x)(y|y) , \quad x, y \in E$
	- Für $y = 0$
		$(x|y)=(x|0)=0\cdot(x|0)=0\implies |(x|y)|^2=0$
		$(x|x)(y|y)=(x|x)(0|0)=0$
	- Es sei also $y \neq 0$. Für $\alpha \in \mathbb{K}$ gilt dann:
		$$
		\begin{aligned}
		0 \le (x - \alpha y|x - \alpha y)
		&= (x|x-\alpha y)-\alpha(y|x-\alpha y) \\
		&= (x|x)-\bar{\alpha}(x|y)-\alpha(y|x)+\alpha\bar{\alpha}(y|y) \\
		&= (x|x)-(x|\alpha y)-(\alpha y|x)+\alpha\bar{\alpha}(y|y) \\
		&= (x|x)-[(x|\alpha y)+\overline{(x|\alpha y)}]+\alpha\bar{\alpha}(y|y) \\
		&= (x|x) - 2 \operatorname{Re}(x|\alpha y) + (\alpha y|\alpha y) \\
		&= (x|x) - 2 \operatorname{Re}(\overline{\alpha}(x|y)) + |\alpha|^2 (y|y) .
		\end{aligned}
		$$
		Wählen wir speziell $\alpha := (x|y)/(y|y)$, so folgt
		$0 \le (x|x) - 2 \operatorname{Re}\left(\frac{(x|y)}{(y|y)}(x|y)\right) + \frac{|(x|y)|^2}{(y|y)^2}(y|y) = (x|x) - \frac{|(x|y)|^2}{(y|y)} ,$
		Gilt $x \neq \alpha y$, so steht hier ein echtes Ungleichheitszeichen.
	(Klassische Cauchy-Schwarzsche Ungleichung) Es seien $\xi_1, \dots, \xi_m$ und $\eta_1, \dots, \eta_m$ Elemente von $\mathbb{K}$. Dann gilt
	$$
	\left|\sum_{j=1}^{m} \xi_j \overline{\eta_j}\right|^2 \le \left(\sum_{j=1}^{m} |\xi_j|^2\right) \left(\sum_{j=1}^{m} |\eta_j|^2\right)
	$$
- Hilbertnorm/die vom Skalarprodukt $(\cdot|\cdot)$ induzierte Norm
	$\|x\| := \sqrt{(x|x)} , \quad x \in E$
- Parallelogramm-identität
	$2(\|x\|^2 + \|y\|^2) = \|x + y\|^2 + \|x - y\|^2, \quad x, y \in E$
- orthogonal
	Es sei $(E, (\cdot|\cdot))$ ein Innenproduktraum.
	- Zwei Elemente $x, y \in E$ heißen orthogonal, wenn $(x|y) = 0$ gilt. Wir verwenden in diesem Fall die Notation $x \perp y$.
	- Eine Teilmenge $M \subseteq E$ heißt Orthogonalsystem, wenn $x \perp y$ für alle $x, y \in M$ mit $x \neq y$ gilt.
		Es sei $\{x_0, \dots, x_m\} \subseteq E$ ein Orthogonalsystem mit $x_j \neq 0$ für $0 \le j \le m$.
		- $\{x_0, \dots, x_m\}$ ist linear unabhängig.
		- (b) $\|\sum_{k=0}^m x_k\|^2 = \sum_{k=0}^m \|x_k\|^2$ (Satz des Pythagoras).
	- Schließlich heißt $M$ Orthonormalsystem, falls $M$ ein Orthogonalsystem ist mit $\|x\| = 1$ für $x \in M$.
		Es seien $B = \{u_0, \dots, u_m\}$ ein Orthonormalsystem im Innenproduktraum $(E, (\cdot|\cdot))$ und $F := \text{span}(B)$. Ferner sei
		$$
		p_F : E \to F, \quad x \mapsto \sum_{k=0}^{m} (x|u_k)u_k
		$$
		- (a) $x - p_F(x) \in F^{\perp}$, $x \in E$.
		- (b) $\|x - p_F(x)\| = \inf_{y \in F} \|x - y\|$, $x \in E$.
			(Für jedes $y \in F$ gilt die Beziehung $\|x - y\|^2 = \|x - p_F(x)\|^2 + \|p_F(x) - y\|^2$.)
		- (c) $\|x - p_F(x)\|^2 = \|x\|^2 - \sum_{k=0}^m |(x|u_k)|^2$, $x \in E$.
		- (d) $p_F \in \text{Hom}(E, F)$ mit $p_F^2 = p_F$.
		- (e) $\text{im}(p_F) = F$, $\ker(p_F) = F^{\perp}$ und $E = F \oplus F^{\perp}$.
		- Für $x \in E$ gilt $\sum_{k=0}^{m} |(x|u_k)|^2 \le \|x\|^2$.
		- Für $x \in F$ gelten
			$x = \sum_{k=0}^{m} (x|u_k)u_k \quad \text{und} \quad \|x\|^2 = \sum_{k=0}^{m} |(x|u_k)|^2 .$

- orthogonale Komplement
	Es sei $F$ ein Untervektorraum eines Innenproduktraumes $E$. Das orthogonale Komplement von $F$, d.h.
	$$
	F^{\perp} := \{ x \in E ; x \perp y, y \in F \},
	$$
	ist ein abgeschlossener Untervektorraum von $E$.
- 