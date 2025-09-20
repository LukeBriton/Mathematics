# Chap. 2 VECTORS

## 20. Vector spaces

set $ℙ$ of all polynomials with real coefficients

$ℙ_3$ of all real polynomials of degree less than or equal to $3$

Many questions can and should be asked about the conditions that define vector spaces: one worrisome question has to do with multiplication, and another one, easier, has to do with zero.

Why, it is natural to ask, is a multiplicative structure not imposed on vector spaces? Wouldn't it be natural and useful to define $(α, β) · (γ, δ) = (αγ, βδ)$ (similarly to how addition is defined in $ℝ^2$)?

或者，是否可以如同复数的乘法一样：（但是，如何拓展？）

$$
(α, β) · (γ, δ) = (αγ-βδ, αδ+βγ)
$$

其乘法的**结合律**或许从“模乘除，角加减”的意义上更易于理解。

$$
(γ, δ) · (α, β)  = (γα-δβ, δα+γβ)（交换律）\\
1 = (1,0)（有幺元）\\
z^{-1}=\frac{\bar z}{|z|^2}（有逆元）\\
$$

乘法交换群、$1\ne0$

$$
\begin{align*}
((α, β) + (γ, δ)) · (ε, ζ) &= (α + γ, β + δ) · (ε,ζ)\\
&= ((α + γ)ε - (β + δ)ζ, (α + γ)ζ + (β + δ)ε)\\
&= ((αε - βζ) + (γε - δζ), (αζ + βε) + (γζ - δε)\\
&= (α, β) · (ε,ζ) + (γ, δ) · (ε,ζ)
\end{align*}
$$

乘法分配律

$\implies$ 域

- $ℙ$ 多项式环，但多项式的乘法逆非常不可能是多项式

- $ℙ_3$ 乘法不封闭

- $𝕍:=\{(α, β, γ)|\ α,β,γ\inℝ,\ α + β + γ = 0\}$

### Problem 20

**Problem 20.** Do the **scalar zero law**,

$$
0x = 0,
$$

and the **vector zero law**,

$$
α0 = 0,
$$

follow from the conditions in the definition of vector spaces, or could they be false?

> Solution:
> 
> $0x \xrightarrow{标量+} (1-1)x \xrightarrow{向量分配} 1x - 1x \xrightarrow{标量幺元} x - x \xrightarrow{向量逆元} 0$
> 
> $α0\xrightarrow{标量+}α(id-id)\xrightarrow{标量分配}αid-αid（死胡同）$

> Hint:
> 
> The 0 element of any additive group is characterized by the fact that 0 + 0 = 0. How can it happen that αx = 0? Related question worth asking: how can it happen that αx = x?
> 
> $ax = x\implies ax-x = 0\implies (a-1)x=0=0x\implies a=1$

## 23. Subspaces

It has already been noted (see Solution 20) that every field is a vector space over itself. In particular, $ℝ$ is a vector space over $ℝ$, but, and this is more interesting, $ℝ$ is a vector space over $ℚ$ also — just forget how to multiply real numbers by anything except rational numbers. In this situation, where $ℝ$ is regarded as a rational vector space, the subset $ℚ$ of $ℝ$ is a new example of a subspace, and so is the larger subset $ℚ(\sqrt{2})$ (see Problem 16). In the same spirit, $ℂ$ (with the operation of addition) is a vector space over $ℂ$, and it is also a vector space over $ℝ$; from the latter point of view, the set $ℝ$ is a subspace (a real subspace of $ℂ$)

总觉得以下和分析（甚至泛函？）有千丝万缕的关系

The set of all real-valued functions defined on, say, a closed interval is a vector space over $ℝ$ if vector addition and scalar multiplication are defined in the obvious pointwise fashion. The set of all continuous functions is an example of a subspace of that  
space.

A different generalization of $ℝ^n$ is the set of all infinite sequences $\{ξ_1, ξ_2, ξ_3, . . .\}$, of real numbers; an example of a subspace is the subset consisting of all those sequences for which the series $\sum^∞_{n=1}ξ_n$ is convergent, and a subspace of that subspace is the subset of all those sequences for which the series is absolutely convergent.

[Bs space - Wikipedia](https://en.wikipedia.org/wiki/Bs_space)
