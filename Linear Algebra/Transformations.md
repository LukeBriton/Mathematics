#### linear transformation (a.k.a. operator)

Observe that for polynomials the definition of differentiation (and integral) can be given  
purely algebraically, and does not need the usual theory of limiting processes.

The words “transformation”, “transform”, “mapping”,  “map”, “operator”, “function” all denote the same object.

#### transformations as vectors

#### product of transformations

#### polynomial of transformations

Let 𝑥 be a polynomial of degree 𝑛 − 1, say; $𝐷^𝑛𝑥$  = $𝐷^𝑘 𝐷^{𝑛−𝑘}$

We mention this example to bring out the disconcerting fact implied by the answer to the last question; the product of two transformations may vanish even though neither one of them is zero. A non-zero transformation whose product with some non-zero transformation is zero is called a divisor of zero.

#### inverse

- non-commutativity
- existence of divisors of zero
- invertibility

| 视角    |                        |                   |                                |
| ----- | ---------------------- | ----------------- | ------------------------------ |
| 函数    | left-inverse           | right-inverse     | inverse                        |
| 映射    | injective / one-to-one | surjective / onto | bijective / 1-1 correspondence |
| 态射    | monomorphism           | epimorphism       | isomorphism                    |
| 矩阵    | full column rank       | full row rank     | full rank                      |
| 线性方程组 | 解若存在则唯一（不保存在）<br>      | 任意均有解（不保唯一）       | 任意均有唯一解                        |

[Why the underlying function of a monomorphism may not be an injection](https://mathoverflow.net/questions/93603/why-the-underlying-function-of-a-monomorphism-may-not-be-an-injection)

[Is every monomorphism an injection?](https://math.stackexchange.com/questions/1644035/is-every-monomorphism-an-injection)

[Are monomorphisms in all concretizable categories with certain objects injections?](https://math.stackexchange.com/questions/4537090/are-monomorphisms-in-all-concretizable-categories-with-certain-objects-injection)

#### matrix

感觉 Treil 讲的最好

方块矩阵看师大

#### invariance

invariant subspace

#### reducibility

If $\mathcal{M}$ and $\mathcal{N}$ are two subspaces such that both are invariant under 𝐴 and such  
that $\mathcal{V}$ is their direct sum, then 𝐴 is reduced (decomposed) by the pair ($\mathcal{M }$, $\mathcal{N}$ ).

The difference between invariance and reducibility is that, in the former case, among the  
collection of all subspaces invariant under 𝐴 we may not be able to pick out any two, other than $\mathcal{O}$ and $\mathcal{V}$, with the property that $\mathcal{O}$ is their direct sum.

某种意义上的分块矩阵

#### projection TODO

直和

idempotent

symmetry

direct sum decomposition

#### combinations of projections

the underlying field of scalars is such that $1+1\neq 0$

#### adjoint

**伴随矩阵**（adjoint, transpose 转置, algebraic adjoint, dual 对偶）：

埃尔米特伴随、共轭转置

参见：[Adjoint functors](https://en.wikipedia.org/wiki/Adjoint_functors), [Transpose_of_a_linear_map](https://en.wikipedia.org/wiki/Transpose_of_a_linear_map)、[Conjugate transpose](https://en.wikipedia.org/wiki/Conjugate_transpose)

比较：[Hermitian adjoint](https://en.wikipedia.org/wiki/Hermitian_adjoint)

In [finite dimensions](https://en.wikipedia.org/wiki/Dimension_\(vector_space\) "Dimension (vector space)") where operators can be represented by [matrices](https://en.wikipedia.org/wiki/Matrix_\(mathematics\) "Matrix (mathematics)"), the Hermitian adjoint is given by the [conjugate transpose](https://en.wikipedia.org/wiki/Conjugate_transpose "Conjugate transpose") (also known as the Hermitian transpose).

**古典伴随矩阵**（adjugate, classical adjoint）：代数余子式构成的矩阵的转置，求逆矩阵用的

the [adjoint operator](https://en.wikipedia.org/wiki/Hermitian_adjoint "Hermitian adjoint") which for a matrix is the [conjugate transpose](https://en.wikipedia.org/wiki/Conjugate_transpose "Conjugate transpose").

- one-to-one
- anti-isomorphism 反同构（运算反序）

#### change of basis

covariant

contravariant

cogrediently

contragrediently

#### similarity

An invertible linear transformation is an automorphism.

conversely, every automorphism is an invertible linear transformation.

#### quotient transformations

#### proper value (a.k.a. eigenvalue)

a simple proper value is one whose multiplicity is equal to 1

The set of proper values of 𝐴 is sometimes called the spectrum of 𝐴.

Note that the spectrum of 𝐴 is the same as the set of all scalars 𝜆 for which 𝐴 − 𝜆 is not invertible

#### multiplicity

By the so-called fundamental theorem of algebra, a polynomial equation over the field of 
complex numbers always has at least one root;

There are other fields, besides the field of complex numbers, over which every polynomial equation is solvable; they are called algebraically closed fields.

we may conclude that proper values always exist (with algebraically closed fields)