
[Mathematical induction - Wikipedia](https://en.wikipedia.org/wiki/Mathematical_induction)

The **natural numbers** consist of a set $\mathbb{N}$, a distinguished element $0 ∈ \mathbb{N}$, and a (successor) function $ν : \mathbb{N} → \mathbb{N}^× := \mathbb{N}\backslash \{0\}$ with following properties:

- (N$_0$) $ν$ is injective.

- (N$_1$) If a subset $N$ of $\mathbb{N}$ contains $0$ and if $ν(n) ∈ N$ for all $n ∈ N$, then $N = \mathbb{N}$. (one form of the principle of induction)

A set M is called an infinite system, if there is an injective function $f : M → M$ such that $f (M ) ⊂ M$ .

Any infinite system contains a model for the natural numbers. Thus the question of the existence of the natural numbers can be reduced to the question of the existence of infinite systems.

It can be shown that $\mathbb{N}$ is itself an inductive set and that $(\mathbb{N}, 0, ν)$ satisfies the Peano axioms. Thus $(\mathbb{N}, 0, ν)$ is a model for the natural numbers.

The natural numbers are unique up to isomorphism. It is thus meaningful to speak 
of *the* natural numbers.

- 可以证明其上加法同乘法构成一交换半环。（冇加法逆）[Semiring - Wikipedia](https://en.wikipedia.org/wiki/Semiring)

- 集合的属于关系定义了自然数的序结构（全序、离散、良序）。
- 最小（自然）数原理 $\implies$ 强归纳法 （本质：良序原理 $\implies$ 超限归纳法）

- 消去律 $\implies$ 除法
- 良序原理 $\implies$ 分解质因数
- (N$_1$) $\implies$ 弱归纳法

The name "strong induction" does not mean that this method can prove more than "weak induction", but merely refers to the stronger hypothesis used in the induction step.


数学归纳法的应用：

- 同一结合运算反复运用，其表达式的值与括号顺序无关。
- 递推定义（累加、累乘、次幂、乘法的递归定义、阶乘）

