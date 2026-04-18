#### Sequence

- sequence/suite/Folge
	$(x_{n})=(x_n)_{n \in \mathbb{N}}=(x_0, x_1, x_2, \dots):=\varphi: \mathbb{N} \to X$
	$(x_j)_{j \ge m}:=\psi: m + \mathbb{N} \to X$
	- $x_n := \varphi(n)$: das $n$-te **Glied**

```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd}
\mathbb N \arrow[rr, "\varphi"'] \arrow[dr, "s_m(n)=m+n"'] & & X \\  
& m+\mathbb N \arrow[ur, "\psi"'] &
\end{tikzcd}

\begin{tikzcd}
\mathbb N \arrow[rr, "n\mapsto x_{m+n}"'] \arrow[dr, "n\mapsto m+n"'] & & X \\  
& \{m,m+1,m+2,\dots\} \arrow[ur, "j\mapsto x_j"'] &
\end{tikzcd}
\end{document}
```
```tikz
\usepackage{tikz-cd}
\usepackage{amssymb}
\begin{document}
\begin{tikzcd} \mathbb N \arrow[r, "s_m", "\sim"'] & m+\mathbb N \arrow[r, "\psi"] & X \end{tikzcd}
\end{document}
```
- property/propriété/Eigenschaft
	- fast alle: $\exists m\in \mathbb{N}, \forall n \ge m$, $E(x_n)$ wahr ist.
	- unendlich viele: $\exists N\in \mathbb{N}, \text{Anz}(N) = \infty$ und gilt $E(x_n), n\in N$
		- Anzahl
- subsequence/sous-suite/Teilfolge
	Es sei $\varphi = (x_n)\in X^\mathbb{N}$, und $\psi:\mathbb{N}\to \mathbb{N}$ sei strikt wachsend.
	Dann heißt $\varphi \circ \psi :=(x_{n_k})_{k \in \mathbb{N}} ∈ X^\mathbb{N}$ Teilfolge von $\varphi$.
	- $n_k := ψ(k)$

#### Sequence Space

sequence space/espace de suites/Folgenraum

- $c_{00} \subsetneq \ell_1 \subsetneq c_0 \subsetneq c \subsetneq \ell_{\infty} \subsetneq s$

- Vektorraum aller Zahlenfolgen
	$$
	s=s(\mathbb{K})=\mathbb{K}^\mathbb{N}
	$$
	- eine kommutative $\mathbb{K}$-Algebra mit Eins
	  bezügl. der punktweisen Verknüpfungen.
- Vektorraum der konvergenten Folgen
	收敛列加法、数乘
	$$
	c=c(\mathbb{K}):=\{ (x_{n}) ∈ s ; (x_{n})\text{ konvergiert}\}
	$$
	- $c$ ist ein Untervektorraum von $s$.
	零列$\times$有界、收敛列$\times$收敛列
	- $c$ ist eine Unteralgebra von $s$.
	几乎所有项非零的收敛列倒数
- Vektorraum der Nullfolgen
	$$
	c_{0}(\mathbb{K}):=\{ (x_{n}) ∈ s ; (x_{n})\text{ converges with}\lim x_{n}=0\}
	$$
	- $c_{0}$ ist ein Untervektorraum von $c$.
	- $c_0$ est ein eigentliches Ideal in $c$.
- $\lim$
	$$
	\lim:c\to \mathbb{K}, (x_{n})\mapsto \lim{x_{n}}
	$$
	ist linear.
	- $\text{ker}(\lim)=c_{0}$
	- $\lim:c\to \mathbb{K}$ ist ein Algebrenhomomorphismus.
	- Die Linearität der Abbildung $\lim$ überträgt sich auch auf Reihen.

https://projecteuclid.org/journals/pacific-journal-of-mathematics/volume-42/issue-1/Topologies-on-sequences-spaces/pjm/1102968025.pdf

[Folgenräume – „Mathe für Nicht-Freaks“ – Wikibooks, Sammlung freier Lehr-, Sach- und Fachbücher](https://de.wikibooks.org/wiki/Mathe_f%C3%BCr_Nicht-Freaks:_Folgenr%C3%A4ume)

- Für $m \in \mathbb{N}^\times$ seien
	$$
	s(\mathbb{K}^m) := \text{Abb}(\mathbb{N}, \mathbb{K}^m) = (\mathbb{K}^m)^{\mathbb{N}}
	$$
	- Abbildung
	$$
	c(\mathbb{K}^m) := \{ (x_n) \in s(\mathbb{K}^m) ; (x_n) \text{ ist konvergent} \}
	$$
	- (a) $c(\mathbb{K}^m)$ ist ein Untervektorraum von $s(\mathbb{K}^m)$.
	- (b) Die Abbildung $\lim : c(\mathbb{K}^m) \to \mathbb{K}^m, \quad (x_n) \mapsto \lim_{n \to \infty} (x_n)$  ist definiert und linear.
	- (c) Für $(\lambda_n) \in c(\mathbb{K})$ und $(x_n) \in c(\mathbb{K}^m)$ mit $\lambda_n \to \alpha$ und $x_n \to a$ gilt $\lambda_n x_n \to \alpha a$ in $\mathbb{K}^m$.

##### $\ell_p$
- Vektorraum der beschränkten Folgen
	$$
	\ell_{\infty} := \ell_{\infty}(\mathbb{K}) := B(\mathbb{N}, \mathbb{K})
	$$
	$\|(x_n)\|_{\infty} = \sup_{n \in \mathbb{N}} |x_n|, \quad (x_n) \in \ell_{\infty}$
	- $c_0$ und $c$ sind normierte Vektorräume bezüglich der Supremumsnorm, und $c_0 \subseteq c \subseteq \ell_\infty$ als Vektorräume.
	- $c_0$ ist ein abgeschlossener Untervektorraum von $\ell_\infty$.
- Vektorraum der absolut summierbaren Folgen
	$$
	\ell_1 := \ell_1(\mathbb{K}) := \left( \{ (x_k) \in s ; \sum x_k \text{ ist absolut konvergent} \}, \|\cdot\|_1 \right)
	$$
	$\|(x_k)\|_1 := \sum_{k=0}^{\infty} |x_k| .$
	- (a) $\ell_1$ ist ein Banachraum.
	- (b) $\ell_1$ ist ein echter Untervektorraum von $\ell_\infty$ mit $\|\cdot\|_\infty \le \|\cdot\|_1$.
	- (c) Die von $\ell_\infty$ auf $\ell_1$ induzierte Norm ist zu der $\ell_1$-Norm nicht äquivalent. (Hinweis: Man betrachte die Folge $(\xi_j)$ mit $\xi_j := (x_{j,k})_{k \in \mathbb{N}}$, wobei $x_{j,k} = 1$ für $k \le j$, und $x_{j,k} = 0$ für $k > j$ gilt.)
- 
	$$
	\ell_p := \{ (x_n) \in s ; \sum_n |x_n|^p < \infty \}
	$$
	- $p\geq 1$: $p$-norm $\|\cdot\|_p$
	- $0<p<1$: $d_p(x,y)$ (an F-norm)