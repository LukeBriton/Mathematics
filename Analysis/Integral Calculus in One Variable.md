
#### Bounded linear operators

- $\mathcal{L}(E,F):= (\mathcal{L}(E,F), ‖·‖)=\{ A ∈ \text{Hom}(E, F ) ; A\text{ is bounded} \}$
	- $\exists α\ge 0$, $\forall x\in E$, s.t. $‖Ax‖\le α‖x‖$
	- operator norm $‖A‖:=\inf\{α\ge 0; ‖Ax‖\le α‖x‖, \forall x\in E\}$ 是范数
	- $‖A‖ = \sup\limits_{x\in \mathbb{B}_{E}} ‖Ax‖$
	- Lipschitz continuous & uniformly continuous
	- $A \in \mathcal{L}(E,F) \iff$ 将有界集映为有界集（bounded 所指）
	- $\mathcal{L}(E,F) \subseteq \text{Hom}(E, F)$
	- $\mathcal{L}(E)$ normed algebra with unity

- $K$-vector space $\mathcal{A}$
$$
\mathcal{A} \times \mathcal{A}\to \mathcal{A}, (a,b)\mapsto a\odot b
$$
	- $(\mathcal{A}, +, \odot)$ 环
	- 分配律、相容性（双线性运算）

- normed algebra
- Banach algebra

- $A \in \text{Hom}(E,F)$
	- 连续 $\iff$
	- 在 $0$ 处连续 $\iff$
	- $A \in \mathcal{L}(E,F)$

[Bounded operator - Wikipedia](https://en.wikipedia.org/wiki/Bounded_operator)

Outside of functional analysis, when a function $f:X\to Y$ is called "[bounded](https://en.wikipedia.org/wiki/Bounded_function "Bounded function")" then this usually means that its [image](https://en.wikipedia.org/wiki/Image_of_a_function "Image of a function") $f ( X )$ is a bounded subset of its codomain. A linear map has this property if and only if it is identically $0$. Consequently, in functional analysis, when a linear operator is called "bounded" then it is never meant in this abstract sense (of having a bounded image).