# Tensor

## Block Matrix

[linear algebra - Block matrices and tensor product notations. - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4458886/block-matrices-and-tensor-product-notations)

As a vector spaces I think we can think of it as again block matrices. 
But I am confused of the product of two block matrices in this case?

[is a Block matrix a Tensor? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/3561659/is-a-block-matrix-a-tensor)

I was wondering if when someone talks about a tensor rank 3 or 4 we can 
represent that 3D/4D matrix just as a simple block matrix? maybe I am 
being sloppy with the definitions but is just to maybe have an intuition
 of what is going on.

## Kronecker Product

[Kronecker product - Wikipedia](https://en.wikipedia.org/wiki/Kronecker_product)

In [mathematics](https://en.wikipedia.org/wiki/Mathematics "Mathematics"), the **Kronecker product**, sometimes denoted by ⊗, is an [operation](https://en.wikipedia.org/wiki/Operation_(mathematics) "Operation (mathematics)") on two [matrices](https://en.wikipedia.org/wiki/Matrix_(mathematics) "Matrix (mathematics)") of arbitrary size resulting in a [block matrix](https://en.wikipedia.org/wiki/Block_matrix "Block matrix"). It is a specialization of the [tensor product](https://en.wikipedia.org/wiki/Tensor_product "Tensor product") (which is denoted by the same symbol) from vectors to matrices and gives the matrix of the [tensor product](https://en.wikipedia.org/wiki/Tensor_product "Tensor product") linear map with respect to a standard choice of [basis](https://en.wikipedia.org/wiki/Basis_(linear_algebra) "Basis (linear algebra)"). The Kronecker product is to be distinguished from the usual [matrix multiplication](https://en.wikipedia.org/wiki/Matrix_multiplication "Matrix multiplication"), which is an entirely different operation. The Kronecker product is also sometimes called **matrix direct product**.

### Definition

If $A$ is an $m × n$ matrix and $B$ is a $p × q$ matrix, then the Kronecker product $A \otimes B$ is the $pm × qn$ block matrix:

$$
\mathbf{A}\otimes\mathbf{B} = \begin{bmatrix}
 a_{11} \mathbf{B} & \cdots & a_{1n}\mathbf{B} \\
 \vdots & \ddots & \vdots \\
 a_{m1} \mathbf{B} & \cdots & a_{mn} \mathbf{B}
\end{bmatrix},
$$

### Example

```latex
% \hline not working at end of line
% I encountered this while trying to preview on Github
% https://github.com/KaTeX/KaTeX/issues/2761
% BTW It seems that Github doesn't support display equation with comments like this.

% When exporting using Zettlr:
% ! Package amsmath Error: \begin{aligned} allowed only in math mode.
% See the amsmath package documentation for explanation.
% https://tex.stackexchange.com/questions/256920/package-amsmath-error-beginaligned-allowed-only-in-math-mode
% \[...\] invalid in Marktext
% Use \begin{align*} ... \end{align*} instead of aligned
% so you won't need to put everything inside math mode.
% However
% https://tex.stackexchange.com/questions/95402/what-is-the-difference-between-aligned-in-displayed-mode-and-starred-align
% The aligned environment can be used in many other situations, though, in which align* wouldn't work at all.
```

$$
\begin{equation*}
\begin{aligned}
  \begin{bmatrix}
    1 & 2 \\
    3 & 4 \\
  \end{bmatrix} \otimes
  \begin{bmatrix}
    0 & 5 \\
    6 & 7 \\
  \end{bmatrix} &=
  \begin{bmatrix}
    1 \begin{bmatrix}
      0 & 5 \\
      6 & 7 \\
    \end{bmatrix} & 
    2 \begin{bmatrix}
      0 & 5 \\
      6 & 7 \\
    \end{bmatrix} \\
    3 \begin{bmatrix}
      0 & 5 \\
      6 & 7 \\
    \end{bmatrix} & 
    4 \begin{bmatrix}
      0 & 5 \\
      6 & 7 \\
    \end{bmatrix} \\
  \end{bmatrix} \\ &= 
  \left[\begin{array}{cc|cc}
    1\times 0 & 1\times 5 & 2\times 0 & 2\times 5 \\
    1\times 6 & 1\times 7 & 2\times 6 & 2\times 7 \\
    \hline 3\times 0 & 3\times 5 & 4\times 0 & 4\times 5 \\
    3\times 6 & 3\times 7 & 4\times 6 & 4\times 7 \\
  \end{array}\right] \\ &=
  \left[\begin{array}{cc|cc}
     0 &  5 &  0 & 10 \\
     6 &  7 & 12 & 14 \\
     \hline 0 & 15 &  0 & 20 \\
    18 & 21 & 24 & 28
  \end{array}\right].
\end{aligned}
\end{equation*}
$$

## Matrix Multiplication, Tensor Contraction

[Reddit - Why isn't Tensor Multiplication defined like Matrix Multiplication is? : r/math](https://www.reddit.com/r/math/comments/y39whq/why_isnt_tensor_multiplication_defined_like/)

> Matrix multiplication is actually the composition of two operations: outer product and tensor contraction (aka "trace"). For matrices of compatible dimensions, there is a unique obvious way to do a contraction after the outer product, so that you get another matrix. But for general tensors, you need to explicitly specify which indices you want to contract.

> Matrix multiplication is called "contraction" when you apply it to tensors.
> 
> It's a more general operation, because you can apply it to any pair of indices, as long as one is an upper index and one is a lower index; you can also contract indices on two different tensors, but that's just the same thing as taking the tensor product then contracting the indices on the result. That's probably why you didn't see it described as a 'product' operation.
> 
> Matrix multiplication can *also* be performed by taking the tensor product of the two matrices, then contracting the lower index you got from the left matrix with the upper index from the right matrix. Hence why I said they're the same operation.

> Matrix multiplication isn't always defined. You can only multiply a $n\times m$ matrix by an $m\times k$ matrix. You can define the exact same operation for tensors as multidimensional arrays but they have to match up. You can multiply an $n\times m\times k$ tensor by a $k\times p\times q$ tensor to get an $n\times m\times p\times q$ tensor for example. The rule is the exact same as matrix multiplication. This is called tensor contraction in general.
> 
> The reason it isn't called multiplication is because tensors don't form an algebra this way. If you multiply two $3\times3\times3$ tensors you get a $3\times3\times3\times3$ tensor. It's only for degree 2 tensors (matrices) that contraction lands you back in degree two tensors (because 2+2-2=2, as opposed to 3+3-2=4).

Related: [Tensor contraction - Wikipedia](https://en.wikipedia.org/wiki/Tensor_contraction)

### Contraction in index notation

In [tensor index notation](https://en.wikipedia.org/wiki/Tensor_index_notation "Tensor index notation"), the basic contraction of a vector and a dual vector is denoted by

$$
\tilde f (\vec v) = f_\gamma v^\gamma,
$$

which is shorthand for the explicit coordinate summation

$$
f_\gamma v^\gamma = f_1 v^1 + f_2 v^2 + \cdots + f_n v^n
$$

(where $v^i$ are the components of $v$ in a particular basis and $f_i$ are the components of $f$ in the corresponding dual basis).

Since a general mixed [dyadic tensor](https://en.wikipedia.org/wiki/Dyadic_tensor "Dyadic tensor") is a linear combination of decomposable tensors of the form $f \otimes v$, the explicit formula for the dyadic case follows: let

$$
\mathbf{T} = T_{j}^i \mathbf{e}_i \otimes \mathbf{e}^j
$$

be a mixed dyadic tensor. Then its contraction is

```markdown
逆天 Github
The problem appears in inline/display style:
e.g.
$$ a_ad_sad $$ This works.
$$ \mathbb{R}_a^{ds}_{sas} $$ This doesn't even render at all!
$$ \(a_r)^{xy}_mno_{sx} $$ This doesn't render as well.
The exact problem I'm struggling with (parentheses also seem to be susceptible):
[LaTeX sometimes fails to render in markdown cells with some curly bracket + underscore combinations · Issue #2909 · ipython/ipython · GitHub](https://github.com/ipython/ipython/issues/2909/)
According to this, one can use ```math```：
[Markdown math not working properly · community · Discussion #19953 · GitHub](https://github.com/orgs/community/discussions/19953)
According to this, backslashing the underscore seems to do the trick：
[Subscript notation issue · Issue #329 · mathjax/MathJax · GitHub](https://github.com/mathjax/MathJax/issues/329)
Not a Solution:
[Getting superscripts in math mode without the ^ character - TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/246293/getting-superscripts-in-math-mode-without-the-character)
$\def\sp{^}a\sp{b}$
Mentioned Github/Mathjax:
[Italic style markdown should not be applied to text with *asterisks* before and after them · Issue #8264 · mattermost/mattermost · GitHub](https://github.com/mattermost/mattermost/issues/8264)
[A complex formula with two ‘_’ cannot be successfully converted into HTML source code · Issue #3067 · mathjax/MathJax · GitHub](https://github.com/mathjax/MathJax/issues/3067)
[Painful Upgrade to MathJax 3 | Chris Yeh](https://chrisyeh96.github.io/2020/03/29/mathjax3.html)
Similar Problems:
[Inappropriate Italic · Issue #60 · tpope/vim-markdown · GitHub](https://github.com/tpope/vim-markdown/issues/60)
[Typing second underscore in a paragraph makes italic from the first one · Issue #34 · ckeditor/github-writer · GitHub](https://github.com/ckeditor/github-writer/issues/34)
[Using underscore for subscript in text mode using underscore only - TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/328048/using-underscore-for-subscript-in-text-mode-using-underscore-only)
[latex3 - Subscripts and superscripts - TeX - LaTeX Stack Exchange](https://tex.stackexchange.com/questions/48815/subscripts-and-superscripts)
```

```math
T_{j}^i \mathbf{e}_i \cdot \mathbf{e}^j = T_{j}^i \delta_i {}^j = b T_{j}^j= T_{1}^1 + \cdots + T_{n}^n.
```

$$
T_{j}^i \mathbf{e}_i \cdot \mathbf{e}^j = T_{j}^i \delta_i {}^j = b T_{j}^j= T_{1}^1 + \cdots + T_{n}^n.
$$

A general contraction is denoted by labeling one [covariant](https://en.wikipedia.org/wiki/Covariance_and_contravariance_of_vectors "Covariance and contravariance of vectors") index and one [contravariant](https://en.wikipedia.org/wiki/Covariance_and_contravariance_of_vectors "Covariance and contravariance of vectors") index with the same letter, summation over that index being implied by the [summation convention](https://en.wikipedia.org/wiki/Summation_convention "Summation convention"). The resulting contracted tensor inherits the remaining indices of the original tensor. For example, contracting a tensor *T* of type (2,2) on the second and third indices to create a new tensor *U* of type (1,1) is written as

```math
T^{ab} {}_{bc} = \sum_{b}{T^{ab}{}_{bc}} = T^{a1} {}_{1c} + T^{a2} {}_{2c} + \cdots + T^{an} {}_{nc} = U^a {}_c .
```

$$
T^{ab} {}_{bc} = \sum_{b}{T^{ab}{}_{bc}} = T^{a1} {}_{1c} + T^{a2} {}_{2c} + \cdots + T^{an} {}_{nc} = U^a {}_c .
$$

By contrast, let

$$
\mathbf{T} = \mathbf{e}^i \otimes \mathbf{e}^j
$$

be an unmixed dyadic tensor. This tensor does not contract; if its base vectors are dotted, the result is the contravariant [metric tensor](https://en.wikipedia.org/wiki/Metric_(mathematics) "Metric (mathematics)"),

$$
g^{ij} = \mathbf{e}^i \cdot \mathbf{e}^j
$$

whose rank is 2.

### Direct Sum -> Tensor Product

Refer to *Linear Algebra: Finite-Dimensional Vector Spaces* (Halmos) for motivations. (TODO)

[Direct Sum vs. Direct Product vs. Tensor Product - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1334965/direct-sum-vs-direct-product-vs-tensor-product) (TODO)

## Terminology

### ✨ [Relationship between a tensor and the tensor product](https://math.stackexchange.com/questions/4537060/relationship-between-a-tensor-and-the-tensor-product) ✨

**Short answer**: To a mathematician, a tensor is just an element of a tensor product. As you ask in the comments, it is correct to say that a tensor is to a tensor product what a vector is to a vector space.

**Medium answer**: A tremendous amount of confusion here is caused by the fact that the word "tensor" has (at least) *five* different meanings which are rarely distinguished, and different communities of practitioners (e.g. mathematicians vs. physicists) default to different ones. Here they are:

1. A tensor is an element of a tensor product.
2. A tensor of type $(m,n)$ relative to a (usually finite-dimensional) vector space $V$ is an element of the tensor product $V^{⊗n}⊗(V^∗)^{⊗m}$
3. A tensor is a multidimensional array of numbers (a [hypermatrix](https://mathworld.wolfram.com/Hypermatrix.html)).
4. A tensor is a [tensor field](https://en.wikipedia.org/wiki/Tensor_field) (e.g. the [Riemann curvature tensor](https://en.wikipedia.org/wiki/Riemann_curvature_tensor) or the [stress-energy tensor](https://en.wikipedia.org/wiki/Stress%E2%80%93energy_tensor)).
5. A tensor is an object which transforms in a certain way under change of coordinates.

These concepts are of course related:

    2 is a special case of 1,
    3 is how you represent a tensor in sense either 1 or 2 using a choice of basis,
    5 is equivalent to either 2 or 4 depending on context,
    4 is a generalization of 2

but they are not the same and much confusion results from not carefully distinguishing them.

Additionally sense 2 is more sophisticated than it appears, because we have the freedom to interpret a tensor of type $(m,n)$ as a function between tensor products in $2^{m+n}$ different ways. For example, a tensor of type $(1,1)$ can be thought of as any of

- an element of $V⊗V^∗$,
- a linear map $V→V$,
- a linear map $V^∗→V^∗$, or
- a linear functional $V^∗⊗V→K$ where $K$ is the underlying field

and any of these representations may be appropriate depending on context.

### ✨ [machine learning - Why the sudden fascination with tensors? - Cross Validated](https://stats.stackexchange.com/questions/198061/why-the-sudden-fascination-with-tensors) ✨

So in machine learning / data processing *a tensor* appears to be simply defined as a multidimensional numerical array. An example of such a 3D tensor would be 1000 video frames of $640×480$ size. A usual $n×p$ data matrix is an example of a 2D tensor according to this definition.

**This is not how tensors are defined in mathematics and physics!**

A tensor can be defined as a multidimensional array obeying certain transformation laws under the change of coordinates ([see Wikipedia](https://en.wikipedia.org/wiki/Tensor#As_multidimensional_arrays) or the first sentence in [MathWorld article](http://mathworld.wolfram.com/Tensor.html)). A better but equivalent definition ([see Wikipedia](https://en.wikipedia.org/wiki/Tensor#Using_tensor_products)) says that a tensor on vector space $V$ is an element of $V⊗…⊗V^∗$. Note that this means that, when represented as multidimensional arrays, tensors are of size $p×p$ or $p×p×p$ etc., where $p$ is the dimensionality of $V$.

Of course one can construct a *tensor product* $V⊗W$ of an $p$-dimensional $V$ and $q$-dimensional $W$ but its elements are usually not called "tensors", as stated [e.g. here on Wikipedia](https://en.wikipedia.org/wiki/Tensor#Using_tensor_products):

> In principle, one could define a "tensor" simply to be an element of any tensor product. However, the mathematics literature usually reserves the term tensor for an element of a tensor product of a single vector space V and its dual, as above.

One example of a real tensor in statistics would be a covariance matrix. It is $p×p$ and transforms in a particular way when the coordinate system in the $p$-dimensional feature space $V$ is changed. It is a tensor. But a $n×p$ data matrix $X$ is not.

But can we at least think of $X$ as an element of tensor product $W⊗V$, where $W$ is $n$-dimensional and $V$ is $p$-dimensional? For concreteness, let rows in $X$ correspond to people (subjects) and columns to some measurements (features). A change of coordinates in $V$ corresponds to linear transformation of features, and this is done in statistics all the time (think of PCA). But a change of coordinates in $W$ does not seem to correspond to anything meaningful *(and I urge anybody who has a counter-example to let me know in the comments)*. So it does not seem that there is anything gained by considering $X$ as an element of $W⊗V$.

And indeed, the common notation is to write $X∈\mathbb{R}^{n×p}$, where $\mathbb{R}^{n×p}$ is a set of all $n×p$ matrices (which, by the way, [are defined](https://en.wikipedia.org/wiki/Matrix_(mathematics)) as rectangular arrays of numbers, without any assumed transformation properties).

**My conclusion is: (a) machine learning tensors are not math/physics tensors, and (b) it is mostly not useful to see them as elements of tensor products either.**

Instead, they are multidimensional generalizations of matrices. Unfortunately, there is no established mathematical term for that, so it seems that this new meaning of "tensor" is now here to stay.

### ✨ [linear algebra - How would you explain a tensor to a computer scientist? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4861085/how-would-you-explain-a-tensor-to-a-computer-scientist) ✨

A sound mathematical definition of a tensor product is not trivial, certainly not trivial to understand. Then working with tensors in addition also requires to grasp the concept of a vector space and its dual, and so on. That is not an obvious, or productive, path to take for a computer scientist, even though only an understanding of all this 
will reveal the *why* behind tensor operations that can be found in software libraries.

From a CS perspective I would explain that tensors are, indeed, multi-dimensional arrays *plus* a number of basic operations on them that have turned out to be very 
useful in a lot of applications. For example, most of the operations in a popular library as [numpy](https://numpy.org/) can be constructed from the following building blocks (not an exhaustive list):

- Reordering of indices.

- Applying a binary operator $⋆$ to arrays with equal dimensions: $(A⋆B)[I]=A[I]⋆B[I]$.

- Free tensor product of arrays: $(A⊗B)[I,J]=A[I]⋅B[J]$.

- Introducing additional indices of any dimension: $A′[I,J]=A[I]$.

- Contraction of two indices with equal dimension: $A′[I]=∑_kA[k,k,I]$.

Of course, there are also some not so trivial operations on certain tensors, such as inversion or $QR$ factorization, and so on. However, understanding how a library supports the operations above will make it much easier to understand. 
The often countless functions that a library offers are mostly just clever and optimized combinations of these basic operations. For example, a matrix multiplication is a combination of a free tensor product and a contraction. The trace of a square matrix is a contraction. And so on.

### ✨ [linear algebra - What is the difference between a tensor product and an outer product? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1951946/what-is-the-difference-between-a-tensor-product-and-an-outer-product) ✨

I have seen the tensor product written as

$$
\begin{equation*}
\begin{aligned}
  \begin{pmatrix}
    a \\
    b \\
  \end{pmatrix} \otimes
  \begin{pmatrix}
    c \\
    d \\
  \end{pmatrix} &=
  \begin{pmatrix}
    ac \\
    ad \\
    bc \\
    bd \\
  \end{pmatrix} \\
\end{aligned}
\end{equation*}
$$

However I have also seen it written as

$$
\begin{equation*}
\begin{aligned}
  \begin{pmatrix}
    a \\
    b \\
  \end{pmatrix} \otimes
  \begin{pmatrix}
    c \\
    d \\
  \end{pmatrix} &=
  \begin{pmatrix}
    a \\
    b \\
  \end{pmatrix}
  \begin{pmatrix}
    c & d \\
  \end{pmatrix}\\ &=
  \begin{pmatrix}
    ac & ad \\
    bc & bd \\
  \end{pmatrix}
\end{aligned}
\end{equation*}
$$

Which I have seen in the context of outer products. 
Why are there two ways to do a tensor product?

Both are different realizations of the tensor product.

Consider $V=\mathbb{R}^2$. Your first "equality" arises from the isomorphism

$$
V⊗V→\mathbb{R}^4 \\

e_1⊗e_1↦e_1; \\

e_1⊗e_2↦e_2; \\

e_2⊗e_1↦e_3; \\

e_2⊗e_2↦e_4. \\
$$

The second "equality" arises from the isomorphism

$V⊗V≃V⊗V^∗≃Hom(V,V)$, where the first isomorphism comes from the isomorphism of the dual with the space arising from the standard inner product of $\mathbb{R}^2$ (which is essentially just transposition), and the second one comes from $(w,v∗)↦v∗(⋅)w$. Note that it becomes a $2×2$ matrix in the end, which is exactly (not exactly, but represents canonically) an element of $Hom(\mathbb{R}^2,\mathbb{R}^2)$.

This is mathematically speaking. I don't know why one is more appropriate than the other in your context. What I can say is that the second way is very useful, because it allows us to translate an endomorphism in terms of something structurally and algebraically rich such as the tensor product. The first one seems to be simply a down to earth immediate way to realize the tensor product as an array.

### ✨ [abstract algebra - An Introduction to Tensors - Mathematics Stack Exchange](https://math.stackexchange.com/questions/10282/an-introduction-to-tensors?noredirect=1&lq=1) ✨

As a physics student, I've come across mathematical objects called **tensors** in several different contexts. Perhaps confusingly, I've also been given both the mathematician's and physicist's definition, which I believe are slightly different.

I currently think of them in the following ways, but have a tough time reconciling the different views:

- An extension/abstraction of scalars, vectors, and matrices in mathematics.
- A multi-dimensional array of elements.
- A mapping between vector spaces that represents a co-ordinate independent transformation.

In fact, I'm not even sure how correct these three definitions are. Is there a particularly relevant (rigorous, even) definition of tensors and their uses, that might be suitable for a mathematical physicist?

Direct answers/explanations, as well as links to good introductory articles, would be much appreciated.

At least to me, it is helpful to think in terms of bases.
(I'll only be talking about tensor products of finite-dimensional vector spaces here.)
This makes the universal mapping property that Zach Conn talks about a bit less abstract (in fact, almost trivial).

First recall that if $L:V→U$ is a linear map, then $L$ is completely determined by what it does to a basis ${e_i}$ for V: 

$$
L(x)=L(∑\limits_i x_ie_i)=∑\limits_i x_iL(e_i).
$$

(The coefficients of $L(e_i)$ in a basis for $U$ give the $i$th column in the matrix for $L$ with respect to the given bases.)

Tensors come into the picture when one studies *multilinear* maps. If $B:V×W→U$ is a bilinear map, then B is completely determined by the values $B(e_i,f_j)$ where ${e_i}$ is a basis for $V$ and ${f_j}$ is a basis for $W$:

$$
B(x,y)=B(∑\limits_i x_ie_i,∑\limits_j y_jf_j)=∑\limits_i∑\limits_jx_iy_jB(e_i,f_j).
$$

For simplicity, consider the particular case when $U=\mathbf{R}$;
then the values $B(e_i,f_j)$ make up a set of $N=mn$ real numbers (where $m$ and $n$ are the dimensions of $V$ and $W$), and these numbers are all that we need to keep track of in order to know everything about the bilinear map $B:V×W→\mathbf{R}$.

Notice that in order to compute $B(x,y)$ we don't really need to know the individual vectors $x$ and $y$, but rather the $N=mn$ numbers ${x_iy_j}$.
Another pair of vectors $v$ and $w$ with $v_iw_j=x_iy_j$ for all $i$ and $j$ will satisfy $B(v,w)=B(x,y)$.

This leads to the idea of splitting the computation of $B(x,y)$ into two stages.

Take an $N$-dimensional vector space $T$ (they're all isomorphic so it doesn't matter which one we take) with a basis $(g_1,…,g_N)$.
Given $x=∑x_ie_i$ and $y=∑y_jf_j$, first form the vector in $T$ whose coordinates with respect to the basis ${g_k}$ are given by the column vector

$$
(x_1y_1,…,x_1y_m,x_2y_1,…,x_2y_m,…,x_ny_1,…,x_ny_m)^T.
$$

Then run this vector through the *linear* map $\tilde{B}:T→\mathbf{R}$ whose matrix is the row vector

$$
(B_{11},…,B_{1m},B_{21},…,B_{2m},…,B_{n1},…,B_{nm}),
$$

where $B_{ij}=B(e_i,f_j)$. This gives, by construction, $∑∑B_{ij}x_iy_j=B(x,y)$.

We'll call the space $T$ the **tensor product** of the vector spaces $V$ and $W$ and denote it by $T=V⊗W$; it is “uniquely defined up to isomorphism”, and its elements are called **tensors**. The vector in T that we formed from $x∈V$ and $y∈W$ in the first stage above will be denoted $x⊗y$;
it's a “bilinear mixture” of $x$ and $y$ which doesn't allow us to reconstruct $x$ and $y$ individually, but still contains exactly all the information needed in order to compute $B(x,y)$ for any bilinear map $B$; we have $B(x,y)=\tilde{B}(x⊗y)$. This is the “universal property”; any bilinear map $B$ from $V×W$ can be computed by taking a “detour” through T, and this detour is unique, since the map $\tilde{B}$ is constructed uniquely from the values $B(e_i,f_j)$.

To tidy this up, one would like to make sure that the definition is basis-independent. One way is to check that everything transforms properly under changes of bases. Another way is to do the construction by forming a much bigger space and taking a quotient with respect to suitable relations (without ever mentioning bases). Then, by untangling definitions, one can for example show that a bilinear map $B:V×W→\mathbf{R}$ can be canonically identified with an element of the space $V^∗⊗W^∗$,
and dually an element of $V⊗W$ can be identified with a bilinear map $V^∗×W^∗→\mathbf{R}$. Yet other authors find this a convenient *starting* point, so that they instead *define* $V⊗W$ to be the space of bilinear maps $V^∗×W^∗→\mathbf{R}$.
So it's no wonder that one can become a little confused when trying to compare different definitions...

**There are many other good answers to this question, just TODO for the moment.**

### Many Other Questions

[terminology - Tensors in neural network literature: what's the simplest definition out there? - Cross Validated](https://stats.stackexchange.com/questions/233253/tensors-in-neural-network-literature-whats-the-simplest-definition-out-there)

[terminology - The meaning of tensors in the neural network community - Cross Validated](https://stats.stackexchange.com/questions/181556/the-meaning-of-tensors-in-the-neural-network-community)

[What, Exactly, Is a Tensor? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/657494/what-exactly-is-a-tensor)

[abstract algebra - What is the difference between tensors and tensor products? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/97764/what-is-the-difference-between-tensors-and-tensor-products)

[linear algebra - Two approaches to tensors? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4891790/two-approaches-to-tensors)

[hilbert spaces - How do outer products differ from tensor products? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1757901/how-do-outer-products-differ-from-tensor-products?rq=1) 力有所不逮

## Bilinear Form

[linear algebra - Is it misleading to think of rank-2 tensors as matrices? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2400/is-it-misleading-to-think-of-rank-2-tensors-as-matrices?rq=1)

Having picked up a rudimentary understanding of tensors from reading mechanics papers and Wikipedia, I tend to think of rank-2 tensors simply as square matrices (along with appropriate transformation rules). Certainly, if the distinction between vectors and dual vectors is ignored, a rank 2 tensor T seems to be simply a multilinear map $V×V→\mathbb{R}$, and (I think) any such map can be represented by a matrix $A$ using the mapping $(v,w)↦v^TAw$.

My question is this: Is this a reasonable way of thinking about things, at least as long as you're working in $\mathbb{R}^n$? Are there any obvious problems or subtle misunderstandings that this naive approach can cause? Does it break down when you deal with something other than Rn? In short, is it "morally wrong"?

btw, note that there is some inconsistency in terminology: one can speak about (m,n)-tensors — that is, multilinear maps $V^n×(V^∗)^m→\mathbb{R}$ (so your bilinear map is a (0,2)-tensor); and "rank-k tensor" may mean (k,0)-tensor ("covariant") or (0,k)-tensor ("contravariant") or sometimes any (n,m)-tensor with $n+m=k$.

It's not misleading as long as you change your notion of equivalence. When a matrix represents a linear transformation $V→V$, the correct notion of equivalence is similarity: $M≃B^{−1}MB$ where $B$ is invertible. When a matrix represents a bilinear form $V×V→\mathbb{R}$, the correct notion of equivalence is *congruence*: $M\cong B^TMB$ where B is invertible. As long as you keep this distinction in mind, you're fine.

You're absolutely right.

Maybe someone will find useful a couple of remarks telling the same story in coordinate-free way:

- What happens here is indeed identification of space with its dual: so a bilinear map $T:V×V→\mathbb{R}$ is rewritten as $V×V^∗→\mathbb{R}$ — which is exactly the same thing as a linear operator $A:V→V$ ;

- An identification of $V$ and $V^∗$ is exactly the same thing as a scalar product on $V$, and using this scalar product one can write $T(v,w)=(v,Aw)$;

- So orthogonal change of basis preserves this identification — in terms of Qiaochu Yuan's answer one can see this from the fact that for orthogonal matrix $B^T=B^{−1}$ (moral of the story: if you have a canonical scalar product, there is no difference between $T$ and $A$ whatsoever; and if you don't have one — see Qiaochu Yuan's answer.)

[linear algebra - Is a bilinear form a tensor or a scalar "output" of that tensor? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/4477570/is-a-bilinear-form-a-tensor-or-a-scalar-output-of-that-tensor)

My first remark for you is to NOT overlook the distinction between a vector space and its dual: if you do, then you're going to make things a lot harder on yourself in the medium-long run.

---

A bilinear form on V is as you said in your first sentence, a function $b:V×V→\mathbb{R}$. I don't know where you're getting the rest of the stuff from. You say

> doesn't this notion mean that $b$ itself must be an element of $\mathbb{R}$?

Absolutely not! It is a function $V×V→\mathbb{R}$. Functions are not real numbers. The target space of the function is a real number in this case, but the function itself is obviously not a real number. I'm not sure why you introduced $\mathbf{B}$ in your post. The object $b$ is what is of interest; you can call b a *bilinear functional on V* or a *bilinear form on V*, or you can also call it a (0,2)-*tensor* on $V^*$, so $b∈T^0_2(V)$ (again, $b∉\mathbb{R}$). The words *form* or *functional* merely emphasize that the target space is $\mathbb{R}$. The most agnostic way of saying it is that $b$ is a bilinear mapping from $V×V$ into $\mathbb{R}$; such a phrasing immediately generalizes to situations where you have three different vector spaces $V_1×V_2→V_3$.

Next, given two vectors $u,v∈V$, we get a number $b(u,v)∈\mathbb{R}$. We call this number the value/output of the bilinear form/functional/(0,2)-tensor $b$ on the pair of vectors $(u,v)$.

Next, you seem to be writing a basis-expansion of $b$, but unfortunately things are not in the right space. As you've currently written it, $b∈V⊗V$, but as I mentioned in my first sentence, you shouldn't disregard the dual. We have the canonical isomorphism (for finite-dimensional $V$):

$$
\text{Hom}^2(V×V;\mathbb{R})≅\text{Hom}(V⊗V;\mathbb{R})=(V⊗V)^∗\cong V^∗⊗V^∗.
$$

So, the object $b$ naturally wants to live in $V^∗⊗V^∗$, NOT $V⊗V$.

---

If you want to write things out using a basis, then fix a basis $\{e_1,…,e_n\}$ of $V$ (you don't even need orthonormality), and let $\{ϵ_1,…,ϵ_n\}$ be the dual basis. Then, you can write

$$
b = \sum\limits_{i,j = 1}^nb(e_i, e_j)ϵ_i\otimesϵ_j\equiv\sum\limits_{i,j = 1}^nb_{ij}ϵ_i\otimesϵ_j
$$

So, if $u,v∈V$, then you can write them as $u=∑\limits_{i=1}^nu_ie_i$ and $v=∑\limits_{i=1}^nv_ie_i$ for some numbers $u_i,v_i$ (in fact, $u_i=ϵ_i(u), v_i=ϵ_i(v)$, i.e the component $u_i∈\mathbb{R}$ equals the value of the covector $ϵ_i∈V^∗$ when evaluated on the vector $u∈V$). Then, the value $b(u,v)$ can be written as:

$$
\begin{equation*}
\begin{aligned}
  b(u,v) &= \sum\limits_{i,j = 1}^nb_{ij}(ϵ_i\otimesϵ_j)(u,v)
  \\ &:= \sum\limits_{i,j = 1}^n b_{ij}ϵ_i(u)\cdotϵ_j(v)
  \\ &= \sum\limits_{i,j = 1}^n b_{ij}u_iv_j
\end{aligned}
\end{equation*}
$$

The relation with matrices is that you can store these numbers $b_{ij},u_i,v_j$ as

$$
\begin{equation*}
\begin{aligned}
   [b]= \begin{pmatrix} 
        b_{11} & \dots  & b_{1n} \\
        \vdots & \ddots & \\
        b_{n1} & \dots  & b_{nn} 
        \end{pmatrix},
   [u]= \begin{pmatrix}
        u_1 \\
        \vdots \\
        u_n
        \end{pmatrix}, 
   [v]= \begin{pmatrix}
        v_1 \\
        \vdots \\
        v_n
        \end{pmatrix},\end{aligned}
\end{equation*}
$$

We call $[b]∈M_{n×n}(\mathbb{R})$ the *matrix representation of b* *relative to the basis* $\{e_1,…,e_n\}$ *of* $V$, and we call $[u]$ the *coordinate vector of $u$ relative to the basis* $\{e_1,…,e_n\}$ *of* $V$ (and likewise for $v$).

Then, $b(u,v)=[u]^t⋅[b]⋅[v]$. So, the value of the tensor on a pair of vectors can be carried out using matrix multiplication once you fix a basis $\{e_1,…,e_n\}$ of $V$ (but conceptually, bases should be the last thing on your mind).

---

(I wrote everything above with lower indices simply because you don't like upper indices, so I included explicitly the summation symbols as well; the natural way to write this would have been $\{e_1,…,e_n\}$ for the basis, $\{ϵ^1,…,ϵ^n\}$ for the dual basis, $u=u^ie_i$ and $v=v^je_j$ for the vectors, and $b=b_{ij}ϵ^i⊗ϵ^j$ for the tensor b. Note also the dual basis only comes up if you want to abstractly write b in terms of a basis as $b=b(e_i,e_j)ϵ^i⊗ϵ^j$).

[differential geometry - Why are bilinear maps represented as members of the tensor space $V^*\otimes V^*$ opposed to just members of the tensor space $V\otimes V$? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2636130/why-are-bilinear-maps-represented-as-members-of-the-tensor-space-v-otimes-v)

By the universal property of the tensor product, every bilinear map $V×V→k$, where k is the underlying field, corresponds uniquely to a linear map $V⊗V→k$. So almost by definition of the tensor product, the set of bilinear maps out of $V×V$ is the space $\text{Hom}_k(V⊗V,k)=:(V⊗V)^∗$.

Be careful though, it's true that if $V$ is finite dimensional we have isomorphisms $(V⊗V)^∗≅V^∗⊗V^∗≅V⊗V$. However, when $V$ is infinite dimensional we don't have $V≅V∗$, so that the identification of $(V⊗V)^∗$ with $V⊗V$ is no longer true.

Could you explain the part about how when $V$ is infinite dimensional we don't have $V≅V^∗$?

In general, if $V$ is infinite dimensional then $dim(V^∗)>dim(V)$. One can see this through the isomorphism $\text{Hom}_k(⨁\limits_{i∈I}V_i,k)≅∏\limits_{i∈I}\text{Hom}_k(V_i,k)$ and maybe an application of the axiom of choice. This means that $(V⊗V)^∗$ (i.e. $BilinearMaps(V×V,k)$) is in general bigger than $V⊗V$.

[linear algebra - extending bilinear form with tensor product - Mathematics Stack Exchange](https://math.stackexchange.com/questions/3201177/extending-bilinear-form-with-tensor-product)

## Rank

[matrices - Is the rank of a Tensor different from the rank of a Matrix? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2245849/is-the-rank-of-a-tensor-different-from-the-rank-of-a-matrix)

"number of dimensions" is a pretty terrible description. Looking at the website, their interpretation of "tensor" is not the same as the strict mathematical definition (which is to do with multilinear maps with certain properties).

As far as that program is concerned, a tensor is a vector of vectors of vectors of... of vectors, where the *rank* is the number of nestings of "of vectors", so

- A tensor of rank 1 is a vector, which is a one-dimensional array, `[a,b]`.

- A tensor of rank 2 is a vector of vectors, or a matrix, or a two-dimensional array, `[[a,b],[c,d]]`.

- A tensor of rank 3 is a vector of vectors of vectors, so something with three nestings, `[[[a,b],[c,d]],[[e,f],[g,h]]]` sort of thing.

- &c.

The "dimension" here is the (tensorial) rank, or the number of inputs you need to locate an entry. This is of course not the same as "dimension" in the sense that something has "dimension n" if is an ordered list of length n.

[Are matrices rank 2 tensors? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/192391/are-matrices-rank-2-tensors)

This question doesn't have a single good answer, because there isn't a universally agreed upon definition of "tensor" in mathematics. In particular:

1. Tensors are sometimes defined as multidimensional arrays, in the same way that a matrix is a two-dimensional array. From this point of view, a matrix is certainly a special case of a tensor.

2. In differential geometry and physics, "tensor" refers to a certain kind of object that can be described at a point on a manifold (though the word "tensor" is often used to refer to a *tensor field*, in which one tensor is chosen for every point). From this point of view, a matrix can be used to describe a rank-two tensor in local coordinates, but a rank-two tensor is not itself a matrix.

3. In linear algebra, "tensor" sometimes refers to an element of a [tensor product](http://en.wikipedia.org/wiki/Tensor_product),
   and sometimes refers to a certain kind of multilinear map. Again, neither of these is a generalization of "matrix", though you can get a matrix from a rank-two tensor if you choose a basis for your vector space.

You run into the same problem if you ask a question like "Is a vector just a tuple of numbers?" Sometimes a vector is defined as a tuple of numbers, in which case the answer is yes. However, in differential geometry and physics, the word "vector" refers to an element of the tangent space to a manifold, while in linear algebra, a "vector" may be any element of a vector space.

On a basic level, the statement "a vector is a rank 1 tensor, and a matrix is a rank 2 tensor" is roughly correct. This is certainly the simplest way of thinking about tensors, and is reflected in the [Einstein notation](http://en.wikipedia.org/wiki/Einstein_notation). However, it is important to appreciate the subtleties of this identification, and to realize that "tensor" often means something slightly different and more abstract than a multidimensional array.

[matrices - Are rank 3 tensors always cubes? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/3817753/are-rank-3-tensors-always-cubes)

## Miscellaneous

[matrices - Why matrix of rank one can be written as a tensor product of two vectors? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/1916619/why-matrix-of-rank-one-can-be-written-as-a-tensor-product-of-two-vectors)

Let a matrix $A$ have columns $a⃗_i, i=1,…,N$. A rank one matrix is characterised by the fact that all columns $\vec{a}_i$ are linearly dependent, that is

$$
\vec{a}_i=b_i\vec{a}
$$

for some vector $\vec{a}$  and scalars $b_i$. Thus, the matrix $A$ takes the form 

$$
A=(b_1\vec{a} ,…,b_N\vec{a})=\vec{a}\vec{b}^T=\vec{a}\otimes\vec{b} ,
$$

where $\vec{b}^T=(b_1,…,b_N)$.

[abstract algebra - Rank and determinant of a tensor product of matrices - Mathematics Stack Exchange](https://math.stackexchange.com/questions/2259063/rank-and-determinant-of-a-tensor-product-of-matrices)

## PyTorch

### torch.dot()

[python - How do I multiply matrices in PyTorch? - Stack Overflow](https://stackoverflow.com/questions/44524901/how-do-i-multiply-matrices-in-pytorch)

`torch.dot()` behaves differently to `np.dot()`. There's been some discussion about what would be desirable [here](https://github.com/pytorch/pytorch/issues/138). Specifically, `torch.dot()` treats both `a` and `b` as 1D vectors (irrespective of their original shape) and computes their inner product. The error is thrown because this behaviour makes your `a` a vector of length 6 and your `b` a vector of length 2; hence their inner product can't be computed. For matrix multiplication in PyTorch, use `torch.mm()`. Numpy's `np.dot()` in contrast is more flexible; it computes the inner product for 1D arrays and performs matrix multiplication for 2D arrays.

[`torch.matmul`](https://pytorch.org/docs/master/torch.html#torch.matmul) performs matrix multiplications if both arguments are `2D` and computes their dot product if both arguments are `1D`. For inputs of such dimensions, its behaviour is the same as `np.dot`. It also lets you do broadcasting or `matrix x matrix`, `matrix x vector` and `vector x vector` operations in batches.

### torch.mm(), torch.matmul(), torch.mul(), torch.bmm()

[python 3.x - What's the difference between torch.mm, torch.matmul and torch.mul? - Stack Overflow](https://stackoverflow.com/questions/73924697/whats-the-difference-between-torch-mm-torch-matmul-and-torch-mul)

#### 1. torch.mm(), torch.matmul(), torch.mul()

In short:

- `torch.mm` - performs a matrix multiplication **without broadcasting** - (2D tensor) *by* (2D tensor)
- `torch.mul` - performs a **elementwise** multiplication **with broadcasting** - (Tensor) *by* (Tensor or Number)
- `torch.matmul` - matrix product **with broadcasting** - (Tensor) *by* (Tensor) with different behaviors depending on the tensor shapes (dot product, matrix product, batched matrix products).

Some details:

1. `torch.mm` - performs a matrix multiplication **without broadcasting**

It expects two 2D tensors so **n×m** * **m×p** = **n×p**

From the documentation [torch.mm &mdash; PyTorch 2.3 documentation](https://pytorch.org/docs/stable/generated/torch.mm.html):

```python
This function does not broadcast. For broadcasting matrix products, see torch.matmul().
```

2. `torch.mul` - performs a **elementwise** multiplication **with broadcasting** - (Tensor) *by* (Tensor or Number)

Docs: [torch.mul &mdash; PyTorch 2.3 documentation](https://pytorch.org/docs/stable/generated/torch.mul.html)

`torch.mul` does not perform a matrix multiplication. It 
broadcasts two tensors and performs an elementwise multiplication. So 
when you uses it with tensors 1x4 * 4x1 it will work similar to:

```python
import torch

a = torch.FloatTensor([[1], [2], [3]])
b = torch.FloatTensor([[1, 10, 100]])
a, b = torch.broadcast_tensors(a, b)
print(a)
print(b)
print(a * b)
```

```python
tensor([[1., 1., 1.],
        [2., 2., 2.],
        [3., 3., 3.]])
tensor([[  1.,  10., 100.],
        [  1.,  10., 100.],
        [  1.,  10., 100.]])
tensor([[  1.,  10., 100.],
        [  2.,  20., 200.],
        [  3.,  30., 300.]])
```

3. `torch.matmul`

It is better to check out the official documentation [torch.matmul &mdash; PyTorch 2.3 documentation](https://pytorch.org/docs/stable/generated/torch.matmul.html) as it uses different modes depending on the input tensors. It may 
perform dot product, matrix-matrix product or batched matrix products 
with broadcasting.

As for your question regarding product of:

```python
tensor1 = torch.randn(10, 3, 4)
tensor2 = torch.randn(4)
```

it is a batched version of a product. please check this simple example for understanding:

```python
import torch

# 3x1x3
a = torch.FloatTensor([[[1, 2, 3]], [[3, 4, 5]], [[6, 7, 8]]])
# 3
b = torch.FloatTensor([1, 10, 100])
r1 = torch.matmul(a, b)

r2 = torch.stack((
    torch.matmul(a[0], b),
    torch.matmul(a[1], b),
    torch.matmul(a[2], b),
))
assert torch.allclose(r1, r2)
```

So it can be seen as a multiple operations stacked together across batch dimension.

Also it may be useful to read about broadcasting:

[Broadcasting semantics &mdash; PyTorch 2.3 documentation](https://pytorch.org/docs/stable/notes/broadcasting.html#broadcasting-semantics)

#### 2. torch.bmm()

I want to add the [introduction of `torch.bmm`](https://pytorch.org/docs/stable/generated/torch.bmm.html), which is batch matrix-matrix product.

```python
torch.bmm(input,mat2,*,out=None)→Tensor
```

**shape:** `(b×n×m),(b×m×p) -->(b×n×p)`

Performs a batch matrix-matrix product of matrices stored in `input` and `mat2`. `input` and `mat2` **must be 3-D tensors** each containing the same number of matrices.

This function **does not broadcast**.

**Example**

```python
input = torch.randn(10, 3, 4)
mat2 = torch.randn(10, 4, 5)
res = torch.bmm(input, mat2)
res.size()  # torch.Size([10, 3, 5])
```

#### Why do we do batch matrix-matrix product?

[deep learning - Why do we do batch matrix-matrix product? - Stack Overflow](https://stackoverflow.com/questions/50826644/why-do-we-do-batch-matrix-matrix-product)

In the seq2seq model, the encoder encodes the input sequences given in as mini-batches. Say for example, the input is `B x S x d` where B is the batch size, S is the maximum sequence length and d is 
the word embedding dimension. Then the encoder's output is `B x S x h` where h is the hidden state size of the encoder (which is an RNN).

Now while decoding (during training) *the input sequences are given one at a time*, so the input is `B x 1 x d` and the decoder produces a tensor of shape `B x 1 x h`. Now to compute the context vector, we need to compare this decoder hidden state with the encoder's encoded states.

So, consider you have two tensors of shape `T1 = B x S x h` and `T2 = B x 1 x h`. So if you can do batch matrix multiplication as follows.

```
out = torch.bmm(T1, T2.transpose(1, 2))
```

Essentially you are multiplying a tensor of shape `B x S x h` with a tensor of shape `B x h x 1` and it will result in `B x S x 1` which is the attention weight for each batch.

Here, the attention weights `B x S x 1` represent a 
similarity score between the decoder's current hidden state and 
encoder's all the hidden states. Now you can take the attention weights 
to multiply with the encoder's hidden state `B x S x h` by transposing first and it will result in a tensor of shape `B x h x 1`. And if you perform squeeze at dim=2, you will get a tensor of shape `B x h` which is your context vector.

This context vector (`B x h`) is usually concatenated to decoder's hidden state (`B x 1 x h`, squeeze dim=1) to predict the next token.

### torch.tensordot()

[multiplication - Multidimensional tensor product in PyTorch - Stack Overflow](https://stackoverflow.com/questions/63180601/multidimensional-tensor-product-in-pytorch)

In pytorch I have two tensors of dimensions [K,L,M] and [M,L,N]. I 
want to perform a standard tensor convolution product of those tensors 
along the middle two dimensions to obtain a [K,N] tensor. I couldn't 
find official documentation on how to perform those operations, perhaps 
it should be better done in some other library and then reconverted to 
pytorch tensor?

If by convolution you actually mean something like contraction, you're probably looking for [`torch.tensordot`](https://pytorch.org/docs/master/generated/torch.tensordot.html). You can specify the indices that should be contracted.

[torch.tensordot — PyTorch master documentation](https://pytorch.org/docs/master/generated/torch.tensordot.html)

Returns a contraction of a and b over multiple dimensions.

[`tensordot`](https://pytorch.org/docs/master/generated/torch.tensordot.html#torch.tensordot "torch.tensordot") implements a generalized matrix product.

```python
a = torch.arange(60.).reshape(3, 4, 5)
b = torch.arange(24.).reshape(4, 3, 2)
torch.tensordot(a, b, dims=([1, 0], [0, 1]))
'''
tensor([[4400., 4730.],
        [4532., 4874.],
        [4664., 5018.],
        [4796., 5162.],
        [4928., 5306.]])
'''

a = torch.randn(3, 4, 5, device='cuda')
b = torch.randn(4, 5, 6, device='cuda')
c = torch.tensordot(a, b, dims=2).cpu()
'''
tensor([[ 8.3504, -2.5436,  6.2922,  2.7556, -1.0732,  3.2741],
        [ 3.3161,  0.0704,  5.0187, -0.4079, -4.3126,  4.8744],
        [ 0.8223,  3.9445,  3.2168, -0.2400,  3.4117,  1.7780]])
'''

a = torch.randn(3, 5, 4, 6)
b = torch.randn(6, 4, 5, 3)
torch.tensordot(a, b, dims=([2, 1, 3], [1, 2, 0]))
'''
tensor([[  7.7193,  -2.4867, -10.3204],
        [  1.5513, -14.4737,  -6.5113],
        [ -0.2850,   4.2573,  -3.5997]])
'''
```

[Pytorch: Tensordot with non-contracting position - Stack Overflow](https://stackoverflow.com/questions/75410741/pytorch-tensordot-with-non-contracting-position)

### torch.kron()

[torch.kron — PyTorch 2.3 documentation](https://pytorch.org/docs/stable/generated/torch.kron.html)

torch.kron(*input*, *other*, ***, *out=None*) → [Tensor](https://pytorch.org/docs/stable/tensors.html#torch.Tensor "torch.Tensor")

```python
mat1 = torch.eye(2) # Returns a 2-D tensor with ones on the diagonal and zeros elsewhere.
mat2 = torch.ones(2, 2)
torch.kron(mat1, mat2)
'''tensor([[1., 1., 0., 0.],
        [1., 1., 0., 0.],
        [0., 0., 1., 1.],
        [0., 0., 1., 1.]])
'''
mat1 = torch.eye(2)
mat2 = torch.arange(1, 5).reshape(2, 2)
torch.kron(mat1, mat2)
'''
tensor([[1., 2., 0., 0.],
        [3., 4., 0., 0.],
        [0., 0., 1., 2.],
        [0., 0., 3., 4.]])
'''
```

[Kronecker Product - #10 by chunyuan_yuan - PyTorch Forums](https://discuss.pytorch.org/t/kronecker-product/3919/10)

[python - Batch Kronecker product of tensors - Stack Overflow](https://stackoverflow.com/questions/72231772/batch-kronecker-product-of-tensors)

```python
x = torch.randn(100,10,10) 
y = torch.randn(100,2,2)
z = torch.einsum('iab,icd->iacbd', x, y).view((100, 20, 20))
```

which is verified below as equivalent to taking Kronecker product over the last two dimensions:

```python
for xx, yy, zz in zip(x, y, z):
    assert zz.allclose(torch.kron(xx, yy))
```

### torch.einsum()

[Einsum is All you Need - Einstein Summation in Deep Learning](https://rockt.github.io/2018/04/30/einsum) ✨**VERY DETAILED, HIGHLY RECOMMENDED**✨

[Einstein notation - Wikipedia](https://en.wikipedia.org/wiki/Einstein_notation)

In [mathematics](https://en.wikipedia.org/wiki/Mathematics "Mathematics"), especially the usage of [linear algebra](https://en.wikipedia.org/wiki/Linear_algebra "Linear algebra") in [mathematical physics](https://en.wikipedia.org/wiki/Mathematical_physics) and [differential geometry](https://en.wikipedia.org/wiki/Differential_geometry "Differential geometry"), **Einstein notation** (also known as the **Einstein summation convention** or **Einstein summation notation**) is a notational convention that implies [summation](https://en.wikipedia.org/wiki/Summation "Summation") over a set of indexed terms in a formula, thus achieving brevity. As part of mathematics it is a notational subset of [Ricci calculus](https://en.wikipedia.org/wiki/Ricci_calculus "Ricci calculus"); however, it is often used in physics applications that do not distinguish between [tangent](https://en.wikipedia.org/wiki/Tangent_space "Tangent space") and [cotangent spaces](https://en.wikipedia.org/wiki/Cotangent_space "Cotangent space"). It was introduced to physics by [Albert Einstein](https://en.wikipedia.org/wiki/Albert_Einstein "Albert Einstein") in 1916.

[torch.einsum — PyTorch 2.3 documentation](https://pytorch.org/docs/stable/generated/torch.einsum.html)

```python
# trace
torch.einsum('ii', torch.randn(4, 4))
'''tensor(-1.2104)'''

# diagonal
torch.einsum('ii->i', torch.randn(4, 4))
'''tensor([-0.1034,  0.7952, -0.2433,  0.4545])'''

# outer product
x = torch.randn(5)
y = torch.randn(4)
torch.einsum('i,j->ij', x, y)
'''
tensor([[ 0.1156, -0.2897, -0.3918,  0.4963],
        [-0.3744,  0.9381,  1.2685, -1.6070],
        [ 0.7208, -1.8058, -2.4419,  3.0936],
        [ 0.1713, -0.4291, -0.5802,  0.7350],
        [ 0.5704, -1.4290, -1.9323,  2.4480]])
'''

# batch matrix multiplication
As = torch.randn(3, 2, 5)
Bs = torch.randn(3, 5, 4)
torch.einsum('bij,bjk->bik', As, Bs)
'''
tensor([[[-1.0564, -1.5904,  3.2023,  3.1271],
        [-1.6706, -0.8097, -0.8025, -2.1183]],

        [[ 4.2239,  0.3107, -0.5756, -0.2354],
        [-1.4558, -0.3460,  1.5087, -0.8530]],

        [[ 2.8153,  1.8787, -4.3839, -1.2112],
        [ 0.3728, -2.1131,  0.0921,  0.8305]]])
'''

# with sublist format and ellipsis
torch.einsum(As, [..., 0, 1], Bs, [..., 1, 2], [..., 0, 2])
'''
tensor([[[-1.0564, -1.5904,  3.2023,  3.1271],
        [-1.6706, -0.8097, -0.8025, -2.1183]],

        [[ 4.2239,  0.3107, -0.5756, -0.2354],
        [-1.4558, -0.3460,  1.5087, -0.8530]],

        [[ 2.8153,  1.8787, -4.3839, -1.2112],
        [ 0.3728, -2.1131,  0.0921,  0.8305]]])
'''

# batch permute
A = torch.randn(2, 3, 4, 5)
torch.einsum('...ij->...ji', A).shape
'''torch.Size([2, 3, 5, 4])'''

# equivalent to torch.nn.functional.bilinear
A = torch.randn(3, 5, 4)
l = torch.randn(2, 5)
r = torch.randn(2, 4)
torch.einsum('bn,anm,bm->ba', l, A, r)
'''
tensor([[-0.3430, -5.2405,  0.4494],
        [ 0.3311,  5.5201, -3.0356]])
'''
```

https://stackoverflow.com/questions/55894693/understanding-pytorch-einsum

[python - How does torch.einsum perform this 4D tensor multiplication? - Stack Overflow](https://stackoverflow.com/questions/66255238/how-does-torch-einsum-perform-this-4d-tensor-multiplication)

[python - Replicate operation tensor operation using `torch.tensordot()` and `torch.stack()` - Stack Overflow](https://stackoverflow.com/questions/74729268/replicate-operation-tensor-operation-using-torch-tensordot-and-torch-stack)
