# Convolution

## Symbol

[Tensor product symbol and convolution](https://math.stackexchange.com/questions/649819/tensor-product-symbol-and-convolution)

$f * g,\ f \otimes g $

In the neural networks (e.g. in Tensorflow) there are convolutional layers which use a tensor product. The latter symbol($\otimes$) stands for tensor product. It is not applicable in all convolution-scenarios.

## Intuition

[pr.probability - What is convolution intuitively? - MathOverflow](https://mathoverflow.net/questions/5892/what-is-convolution-intuitively)

If random variable $X$ has a probability distribution of $f(x)$ and random variable $Y$ has a probability distribution $g(x)$ then $(f∗g)(x)$, the convolution of $f$ and $g$, is the probability distribution of $X+Y$. This is the only intuition I have for what convolution means.

Are there any other intuitive models for the process of convolution?

I remember as a graduate student that Ingrid Daubechies frequently referred to convolution by a bump function as "blurring" - its effect on images is similar to what a short-sighted person experiences when taking off his or her glasses (and, indeed, if one works through the geometric optics, convolution is not a bad first approximation for this effect). I found this to be very helpful, not just for understanding convolution per se, but as a lesson that one should try to use physical intuition to model mathematical concepts whenever one can.

More generally, if one thinks of functions as fuzzy versions of points, then convolution is the fuzzy version of addition (or sometimes multiplication, depending on the context). The probabilistic interpretation is one example of this (where the fuzz is a a probability distribution), but one can also have signed, complex-valued, or vector-valued fuzz, of course.

I prefer sound to Terry Tao's light. Listen to my voice through a wall. At each moment in time, you hear not just what I am saying now, but also some reverberation from what I said moments ago. So if I make a sound given by $f(t)$ (density of air), you hear a linear combination $h(0)f(t)+h(1)f(t−1)+h(2)f(t−2)+…$, or a continuous version of that, i.e. $h∗f$. The function $h(τ)$ is how much you hear from $τ$ seconds before the current time. If $h(τ)$ decays slowly, my voice is muffled by reverb.

Fourier theory shows that recovering my voice $f(t)$

is difficult when $\hat{h}(ξ)$ is very small at some frequencies $ξ$: the wall doesn't vibrate at those frequencies.

If $h(τ)≠0$ for some negative $τ$, you can hear me before I speak!

Sounds like the air between my wife and me has $h(τ)≠0$ for negative $τ$...

**There are many other good answers to this question, just TODO for the moment.**

[real analysis - Definition of convolution? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/714507/definition-of-convolution)

Intuitively, and abusing the notation a bit, you can consider the convolution as

$$
(f*g)(x) = \int_{p+q=x}f(p)g(q)
$$

This makes it clear that $f∗g=g∗f$.

Consider the discrete analogue: Given two functions $a:k↦a(k)$ and $b:l↦b(l)$ we are collecting (i.e., summing up) for given $r$ all products $a(k)b(l)$ where $k+l=r$. This is the right thing to do, e.g., when multiplying two power series

$$
a(z):=∑_{k=0}^∞a_kz^k,\ b(z):=∑_{l=0}^∞b_lz^l .
$$

Then $c(z):=a(z)b(z)$ can be written as $c(z)=∑^∞_{r=0}c_rz^r$ with

$$
c_r:=∑_{k+l=r}a_kb_l=∑_{l=0}^ra_{r−l}b_l(r≥0) .
$$

This is expressed by saying that the sequence $c:=(c_r),\ r≥0$ is the convolution of the two sequences $a:=(a_k),\ k≥0$ and $b:=(b_l),\ l≥0$, in short: $c=a∗b$.

A similar argument can be put forward when dealing with the sum of two independent random variables $X$ and $Y$ having probabilities $p_k$ and $q_l$ of assuming the values $k$ and $l$, respectively.

Translating this into a continuous setting we have

$$
(f∗g)(x)=∫^∞_{−∞}f(x−t)g(t) dt ,
$$

assuming that the integral on the right hand side makes sense.

You could think of simple examples as this:

Impulse response $g(x)$ is zero except for $x=10,$ $g(10)=1$. This could mean "dog is barking 10 seconds after he has seen a cat".

Then the convolution could be explained as: The volume at which the dog is barking at time $t$ is the amount of cats he has seen $10$ seconds **before** time $t$. Which is $t$ **minus** $10$ seconds.

This is clear when you write 

$$
∫f(y)g(x−y)dy=∫g(z)f(x−z)dz
$$

: the response now $(x)$ is the function $f(x)$ multipled by $g(0)$ plus all the responses that started $z$ seconds ago (whose impulse response is now $g(z)$), when the function had value $f(x-z)$. Clearly, for non causal responses, $z$ can be negative, and the sum extends to the future $(z<0)$.

## Convolutional Network
