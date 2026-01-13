- 观察、归纳
- 差分
- 递推关系 $\Longleftrightarrow$ 线性动态系统、矩阵、特征多项式、谱
- 生成函数、形式幂级数
- 特征根法
- 不动点

1. 通项公式
2. 递推公式
3. 平均&统计属性
4. 渐进公式 $p_{n} \sim n\log n \Longleftrightarrow π(x) \sim \frac{x}{\log x}$
5. 单峰、凸性
6. 等式

目的：解决**不尽相异元素的部分排列和组合**

#### 组合的母函数

$S = \{n_{1}\cdot e_{1}, n_{2}\cdot e_{2},\dots, n_{m}\cdot e_{m}\}$，$n_{1}+n_{2}+\dots+n_{m}=n$ （均非负）
$$
G(x)=\prod\limits_{i=1}^m\sum\limits_{j=0}^{n_{i}}x^j=\sum\limits_{r=0}^na_{r}x^r
$$

##### r 无重组合：
 $S = \{1·e_{1}, 1·e_{2},\dots, 1·e_{n}\}$
$$
G(x)=(1+x)^n
$$
$x^r$ 系数 $C(n,r)=C_{n}^r$

##### r 无限可重组合：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=\prod\limits_{i=1}^n\sum\limits_{j=0}^{∞}x^j=\left( \sum\limits_{j=0}^{∞}x^j \right)^n=\frac{1}{(1-x)^n}
$$
$x^r$ 系数 $RC(∞, r) = C_{n+r-1}^r$
> [!tip] $$[x^r]\frac{1}{(1-x)^n}=\binom{n+r-1}{r}$$
> $$
> (1+x+x^2+x^3+\dots+x^i+\dots)^n
> =\sum\limits_{r=0}^∞\binom{n+r-1}{r}x^r
> $$
> $x^r=x^{j_1}x^{j_2}\cdots x^{j_n}=x^{j_1+\cdots+j_n}.$
> 问题演变成求解的个数
> $$
> \begin{cases}
> j_{i}\geq0 \\
> j_{1}+j_{2}+\dots+j_{n}=r
> \end{cases}
> $$

##### 每个元素至少取1个的 r 可重组合（$r\geq n$）：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=\prod\limits_{i=1}^n\sum\limits_{j=1}^{∞}x^j=\left( \sum\limits_{j=1}^{∞}x^j \right)^n=\left(\frac{x}{1-x}\right)^n
$$
$x^r$ 系数 $C_{r-1}^{n-1}$
> [!tip] $$\frac{x}{1-x}$$
> $$
> x+x^2+x^3+\dots+x^i+\dots=-1+1+x+x^2+x^3+\dots+x^i+\dots=\frac{1}{1-x}-1=\frac{x}{1-x}
> $$
> $x^r=x^{j_1}x^{j_2}\cdots x^{j_n}=x^{j_1+\cdots+j_n}.$
> 问题演变成求解的个数$C_{n+r-n-1}^{r-n}=C_{r-1}^{n-1}$
> $$
> \begin{cases}
> j_{i}\geq1 \\
> j_{1}+j_{2}+\dots+j_{n}=r
> \end{cases}
> $$

![[Permutations and Combinations#16. 整数有序分拆]]
##### 每个元素出现非负偶数次的 r 可重组合：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=(1+x^2+x^4+\dots+x^{2n}+\dots)^n=\frac{1}{(1-x^2)^n}
$$
$x^r$ 系数
$$
a_{r}=
\begin{cases}
0\text{（}r\text{为奇数）} \\
C\left( n+\frac{r}{2} -1, \frac{r}{2} \right)\text{（}r\text{为偶数）}
\end{cases}
$$
##### 每个元素出现奇数次的 r 可重组合：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=(x+x^3+x^5+\dots+x^{2n+1}+\dots)^n=\left(\frac{x}{1-x^2}\right)^n
$$
$x^r$ 系数
$$
a_{r}=
\begin{cases}
0\text{（}r-n\text{为奇数）} \\
C\left( n+\frac{r-n}{2} -1, \frac{r-n}{2} \right) \text{（}r-n\text{为偶数）}
\end{cases}
$$
##### 元素 $e_{i}$ 至少出现 $k_{i}$ 次的 r 可重组合：
$S = \{n_{1}\cdot e_{1}, n_{2}\cdot e_{2},\dots, n_{m}\cdot e_{m}\}$，$n_{1}+n_{2}+\dots+n_{m}=n$ （均非负）
$$
G(x)=\prod\limits_{i=1}^m\sum\limits_{j=k_{i}}^{n_{i}}x^j=\sum\limits_{r=k}^na_{r}x^r
$$
$x^r$ 系数 $a_r$, $k=k_{1}+k_{2}+\dots+k_{m}$

#### 排列的母函数

$S = \{n_{1}\cdot e_{1}, n_{2}\cdot e_{2},\dots, n_{m}\cdot e_{m}\}$，$n_{1}+n_{2}+\dots+n_{m}=n$ （均非负）
$$
G(x)=\prod\limits_{i=1}^m\sum\limits_{j=0}^{n_{i}} \frac{x^j}{j!}=\sum\limits_{r=0}^na_{r} \frac{x^r}{j!}
$$
$\frac{x^r}{j!}$ 系数 $a_{r}$

##### r 无重排列：
$S = \{1·e_{1}, 1·e_{2},\dots, 1·e_{n}\}$
$$
G(x)=\left( 1+ \frac{x}{1!} \right)^n
$$
$x^r$ 系数 $C(n,r)r!=P_{n}^r$
##### r 无限可重排列：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=\prod\limits_{i=1}^n\sum\limits_{j=0}^{∞} \frac{x^j}{j!}=\left( \sum\limits_{j=0}^{∞} \frac{x^j}{j!} \right)^n=e^{nx}=\sum\limits_{r=0}^{∞} n^r\frac{x^r}{r!}
$$
$x^r$ 系数 $RP(∞, r) = n^r$

##### 每个元素至少取1个的 r 可重排列（$r\geq n$）：
$S = \{∞\cdot e_{1}, ∞\cdot e_{2},\dots, ∞\cdot e_{n}\}$
$$
G(x)=\prod\limits_{i=1}^n\sum\limits_{j=1}^{∞}\frac{x^j}{j!}=\left( \sum\limits_{j=1}^{∞}\frac{x^j}{j!} \right)^n=(e^x-1)^n=\sum\limits_{r=0}^{∞}\left( \sum\limits_{i=0}^{n}(-1)^iC_{n}^i(n-i)^r \right) \frac{x^r}{r!}
$$
$x^r$ 系数 $\sum\limits_{i=0}^{n}(-1)^iC_{n}^i(n-i)^r$

##### 元素 $e_{i}$ 至少出现 $k_{i}$ 次的 r 可重组合：
$S = \{n_{1}\cdot e_{1}, n_{2}\cdot e_{2},\dots, n_{m}\cdot e_{m}\}$，$n_{1}+n_{2}+\dots+n_{m}=n$ （均非负）
$$
G(x)=\prod\limits_{i=1}^m\sum\limits_{j=k_{i}}^{n_{i}}\frac{x^j}{j!}
$$
- $S = \{n_{1}\cdot e_{1}, n_{2}\cdot e_{2},\dots, n_{m}\cdot e_{m}\}$，$n_{1}+n_{2}+\dots+n_{m}=n$ （均非负） 令 $r=n$
	得全排列数

#### 无序分拆

$n$ 的分拆中，不考虑各分量的顺序，从大到小排列：
$$
\begin{cases}
n=n_{1}+n_{2}+\dots+n_{k},k\ge1 \\
n_{1}\geq n_{2}\geq \dots \geq n_{i}\geq1
\end{cases}
$$
$(n_{1},n_{2},\dots,n_{k})$ $n$ 的 k 无序分拆，分拆数 $P_{k}(n)$，$n_1$ 称为最大分项。

Ferrers 图共轭/转置 $\implies$ n 的所有 k 分拆的个数 $=$ 把 n 分拆成最大分项等于 k 的分拆数

**问题转换**：设满足后一种条件的 $k$ 分拆数也为 $P_{k}(n)$，将 $n$ 分拆为 $k$ 项（每一项的大小不受限制）
的分拆数等于将 $n$ 分拆为最大分项的 $k$（分项个数不限）的分拆数。

##### 最大分项 $n_{1}=k$ 的分拆

$$
\begin{cases}
1x_{1}+2x_{2}+\dots+kx_{k}=n \\
x_{i}\geq 0\quad(i=1,2,\dots,k-1) \\
x_{k}\geq 1
\end{cases}
$$

$$
\begin{align}
G(x)&=(1+x+x^2+\dots)(1+x^2+(x^2)^2+\dots)\dots(x^k+(x^k)^2+\dots) \\
&=\frac{1}{1-x}\frac{1}{1-x^2}\dots\left( \frac{1}{1-x^k}- 1\right) \\
&=\frac{1}{1-x}\frac{1}{1-x^2}\dots\frac{x^k}{1-x^k} \\
&=\sum\limits_{n=k}^{∞}P_{k}(n)x^n
\end{align}
$$

##### 最大分项 $n_{1}\leq k$ 的分拆
$$
\begin{cases}
1x_{1}+2x_{2}+\dots+kx_{k}=n \\
x_{i}\geq 0\quad(i=1,2,\dots,k)
\end{cases}
$$

$$
\begin{align}
G(x)&=(1+x+x^2+\dots)(1+x^2+(x^2)^2+\dots)\dots(1+x^k+(x^k)^2+\dots) \\
&=\frac{1}{1-x}\frac{1}{1-x^2}\dots\frac{1}{1-x^k} \\
&=\sum\limits_{n=k}^{∞}r_{k}(n)x^n
\end{align}
$$
$r_{k}$ 是 $n$ 的最大分项不超过 $k$ 的分项个数


#### 例题

##### 例3.1.6 取鞋不成对

>[!faq] 取鞋不成对
>n双互相不同的鞋，取r只（$r\leq n$），要求其中没有任何两只成对。

分组选择/二次分配

- $G(x)=(1+x)^n$ 各双均有不取或取两种
- $C_{n}^r2^r$：n中取r双，每双有2种
- 左脚右脚先后取：
	$$
	\binom{n}{0}\binom{n-1}{r}+\binom{n}{1}\binom{n-1}{r-1}+\dots+\binom{n}{i}\binom{n-1}{r-i}+\dots+\binom{n}{r}\binom{n-1}{0}=\binom{n}{r}2^r
	$$

归纳为
>[!note]
>$S$ 中共有 $m$ 类元素，其中第 $i$ 类有 $n_{i}$ 个，且同类的元素也互不相同（比如左、右），元素 $e_{i}$ 至少出现 $k_{i}$ 次的 r 组合
>$$
>G(x)=\prod\limits_{i=1}^m\sum\limits_{j=k_{i}}^{n_{i}}\binom{n_{i}}{j}x^j
>$$
>第 $i$ 类有 $n_i$ 个互不相同的元素，写成$\{e_{i1},e_{i2},\dots,e_{in_i}\}$
>
>每个具体元素是“取/不取”，生成函数因子都是 $(1+x)$。于是整个第 $i$ 类的贡献是
>$$
>(1+x)^{n_i}=\sum_{j=0}^{n_i}\binom{n_i}{j}x^j.
>$$
>这正是 $\binom{n_i}{j}$ 出现的来源：**它就是把 $n_i$ 个不同元素的 $(1+x)$ 相乘后展开得到的系数**。
>
>原来的“同质多重集合”相当于：这一类不是 $n_i$ 个不同的 $(1+x)$，而是只有“取 $j$ 个”这一件事，因子才是 $\sum x^j$。

>[!faq] 分书
>5本**相同**的书，分给3个班，各同学视为不同，每人最多一本，且甲、乙两班最少1本，甲班最多5本，乙班最多6本，丙班最少2本，最多9本。

$5=1+1+3=1+2+2=2+1+2$

书相同，实际上是书挑人，各班相当于袜子。

$$
\binom{5}{1}\binom{6}{1}\binom{9}{3}+\binom{5}{1}\binom{6}{2}\binom{9}{2}+\binom{5}{2}\binom{6}{1}\binom{9}{2}=2520+2700+2160=7380
$$

不能认为是$\binom{20}{5}=15504$

##### 例3.1.7 搬书（两人本数相同）

>[!faq] 搬书
>甲乙丙 n （$n\geq3$）本相同的书搬到办公室，要求甲乙本数相同。

好似没有上界了

（还是分奇偶好）

偶数：
$$
n=0+0+n=1+1+(n-2)=2+2+(n-4)=3+3+(n-6)=n/2+n/2+0
$$
奇数：
$$
n=0+0+n=1+1+(n-2)=2+2+(n-4)=3+3+(n-6)=(n-1)/2+(n-1)/2+1
$$

$$
\left\lceil  \frac{n+1}{2} \right\rceil
$$

母函数：设法表示 $x^n=x^kx^kx^{n-2k}=x^{2k}x^{n-2k}$。
$$
\begin{align}
G(x)&=\left( 1+ x^2+x^4+\dots+x^{2k}+\dots+x^{2\left\lfloor  \frac{n}{2}  \right\rfloor }+\dots \right)(1+x+x^2+\dots+x^{n-2k}+\dots+x^n+\dots) \\
&=\frac{1}{1-x^2}\frac{1}{1-x} \\
&=\frac{1}{1-x} \frac{1}{1+x} \frac{1}{1-x} =\frac{A}{1+x}+\frac{B}{1-x}+\frac{C}{(1-x)^2} \text{（部分分式、待定系数）}\\
&=\frac{1}{4}\frac{1}{1+x}+\frac{1}{4}\frac{1}{1-x}+\frac{1}{2}\frac{1}{(1-x)^2}\text{(How?)} \\
\frac1{1+x}&=\sum_{n\ge0}(-1)^n x^n, \\
\frac1{1-x}&=\sum_{n\ge0}x^n, \\
\frac1{(1-x)^2}&=\sum_{n\ge0}(n+1)x^n \\
[x^n]G(x)=&\frac14(-1)^n+\frac14+\frac12(n+1)
=\frac{n+1}{2}+\frac{1+(-1)^n}{4}
\end{align}
$$

![[Generating Function#r 无限可重组合：]]

直接取系数（不用部分分式也行）$G(x)=\sum_{k\ge0}x^{2k}\sum_{t\ge0}x^t.$

要得到 $x^n$，必须 $2k\le n$，每个 $k$ 都对应唯一 $t=n-2k$。所以
$$
[x^n]G(x)=\#{k:0\le k\le \lfloor n/2\rfloor}=\left\lfloor\frac n2\right\rfloor+1.
$$

##### 例3.3.5（例3.1.6推广）

>[!faq] 取鞋不成对，排成一列
> n双互相不同的鞋，取r只（$r\leq n$），要求其中没有任何两只成对，所取 r 只排成一列。

$C_{n}^r2^r r!=P_{n}^r 2^r$：n中取r双，每双有2种，再排序

>[!note] 不同球、不同盒子
> （1）r个不同球->n个不同盒子，每个盒子最多放一个球，每个盒子中有两个相异格子，故需进行二次分配。
> （2）$S$ 中共有 $m$ 类元素，其中第 $i$ 类有 $n_{i}$ 个，且同类的元素也互不相同（比如左、右），元素 $e_{i}$ 至少出现 $k_{i}$ 次、最多出现 $t_{i}$ 次的排列
>$$
>G(x)=\prod\limits_{i=1}^m\sum\limits_{j=k_{i}}^{t_{i}}\binom{n_{i}}{j} j!\frac{x^j}{j!}=\prod\limits_{i=1}^m\sum\limits_{j=k_{i}}^{t_{i}}P_{n_{i}}^{j}\frac{x^j}{j!}
>$$

##### 例3.4.1 无序分拆（各分项不同，即不重复）

>[!faq] 无序分拆（各分项不同，即不重复）
> 1、2、3、4g砝码各一枚，若要求各砝码只能放在天平的一边，能称出几种重量？有几种可能方案？

$$
\begin{cases}
n=n_{1}+n_{2}+\dots+n_{k},k\ge1 \\
n_{1}\geq n_{2}\geq \dots \geq n_{i}\geq1
\end{cases}
$$
$$
\begin{align}
G(x)&=(1+x)(1+x^2)(1+x^3)(1+x^4) \\
&=(1+x+x^2+x^3)(1+x^3+x^4+x^7) \\
&=1+x+x^2+x^3+x^3+x^4+x^5+x^6+x^4+x^5+x^6+x^7+x^7+x^8+x^9+x^{10} \\
&=1+x+x^2+2x^3+2x^4+2x^5+2x^6+2x^7+x^8+x^9+x^{10}
\end{align}
$$
$$
\begin{align}
G(x,y,z,w)&=(1+x)(1+y^2)(1+z^3)(1+w^4) \\
&=(1+x+y^2+xy^2)(1+z^3+w^4+z^3w^4) \\
&=1+x+y^2+xy^2+z^3+xz^3+y^2z^3+xy^2z^3+w^4+xw^4+y^2w^4+xy^2w^4+z^3w^4+xz^3w^4+y^2z^3w^4+xy^2z^3w^4
\end{align}
$$

组合关心的是元素的个数，本例关心的是元素的加权和（每个元素赋予一定的权值）。对于组合而言，母函数为 $(1+x)(1+y)(1+z)(1+w)$

##### 例3.4.2 无序分拆（各分项无限重复）

>[!faq] 无序分拆（各分项无限重复）
> 1、2、3分邮票，贴出不同面值面值方案？

$$
\begin{align}
G(x)&=(1+x+x^2+\dots)(1+x^2+(x^2)^2+\dots)(1+x^3+(x^3)^2+\dots) \\
&=\frac{1}{1-x}\frac{1}{1-x^2}\frac{1}{1-x^3} \\
&=\frac{1}{1-x-x^3+x^4+x^5-x^6} \\
&=1+x+2x^2+3x^3+4x^4+5x^5+7x^6\text{(How?)}
\end{align}
$$
乘 $x^k$ 会把系数整体“右移” $k$ 位：
$$
x^k G(x)=x^k\sum_{n\ge0}a_n x^n=\sum_{n\ge0} a_n x^{n+k}
=\sum_{m\ge k} a_{m-k}x^m.
$$

* $G(x)=\sum_{m\ge0} a_m x^m$
* $-xG(x)=-\sum_{m\ge1} a_{m-1}x^m$
* $-x^2G(x)=-\sum_{m\ge2} a_{m-2}x^m$
* $+x^4G(x)=+\sum_{m\ge4} a_{m-4}x^m$
* $+x^5G(x)=+\sum_{m\ge5} a_{m-5}x^m$
* $-x^6G(x)=-\sum_{m\ge6} a_{m-6}x^m$

$$
\begin{align}
G(x)&=\sum_{n\geq0}a_{n}x^n \\
(1-x-x^2+x^4+x^5-x^6)G(x)&=1 \text{（比较系数）} \\
&=G(x)-xG(x)-x^2G(x)+x^4G(x)+x^5G(x)-x^6G(x) \\
&=\sum_{m\ge0}\bigl(a_m-a_{m-1}-a_{m-2}+a_{m-4}+a_{m-5}-a_{m-6}\bigr)x^m \\
\end{align}
$$
约定 $a_j=0, j < 0$

右边
$$
1=\sum_{m\ge0} b_m x^m,\quad b_0=1,\ b_m=0\ (m\ge1).
$$
于是 $a_m-a_{m-1}-a_{m-2}+a_{m-4}+a_{m-5}-a_{m-6}=b_m.$

$a_0=b_0=1$
$m\geq 1$：$a_m-a_{m-1}-a_{m-2}+a_{m-4}+a_{m-5}-a_{m-6}=0 \iff a_m=a_{m-1}+a_{m-2}-a_{m-4}-a_{m-5}+a_{m-6}$ 

- $a_{1}=a_{0}=1$
- $a_{2}=a_{1}+a_{0}=2$
- $a_{3}=a_{2}+a_{1}=3$
- $a_{4}=a_{3}+a_{2}-a_{0}=4$
- $a_5=a_{4}+a_{3}-a_{1}-a_{0}=5$
- $a_6=a_{5}+a_{4}-a_{2}-a_{1}+a_{0}=7$

###### 例3.4.3 有序分拆

有序分拆：4=3+1=2+2=2+1+1=1+3=1+2+1=1+1+2=1+1+1+1

或者用 $C(r-1, n-1)$ 代入 $n=1, 2, 3$（因为无4分面值，取不到最大分项4）

$C(4-1, 1-1) = 1, C(4-1, 2-1) = 3, C(4-1, 3-1) = 3$

##### 例3.4.5 无序分拆（各分项有限不重复）

>[!faq] 无序分拆（各分项有限不重复）
> （1）1g 3枚，2g 4枚，4g 2枚砝码各一枚，若要求各砝码只能放在天平的一边，能称出几种重量？有几种可能方案？
> （2）若砝码**可以放在天平的两边**，但两边不能同时有同样重量的砝码。给出母函数、称出2g重物体的不同称法。

（1）

$$
\begin{align}
G(x)&=(1+x+x^2+x^3)(1+x^2+x^4+x^6+x^8)(1+x^4+x^{16}) \\
&= 1+x+2x^2+2x^3+3x^4+4x^6+\dots+x^{19}
\end{align}
$$

（2）
$$
\begin{align}
G(x)&=\left( \frac{1}{x^3}+\frac{1}{x^2}+\frac{1}{x}+1+x+x^2+x^3 \right)\left( \frac{1}{x^8}+\frac{1}{x^6}+\frac{1}{x^4}+\frac{1}{x^2}+1+x^2+x^4+x^6+x^8 \right)\left( \frac{1}{x^8}+\frac{1}{x^4}+1+x^4+x^8 \right) \\
&=\dots \\
&=\dots+13x^2+\dots
\end{align}
$$

13种

（天平两边放有同一重量的砝码，使得相同砝码抵消）采用上面的母函数无法反映。
#### 习题

##### 3. 证明母函数

>[!faq] 证明序列的母函数
> $C(n,n), C(n+1,n), C(n+2,n),\dots$ 的母函数为 $\frac{1}{(1-x)^{n+1}}$

$$
\left( \frac{1}{1-x} \right)^n=\sum\limits_{r=0}^{\infty}\binom{n+r-1}{r}x^r \implies \left( \frac{1}{1-x} \right)^{n+1}=\sum\limits_{r=0}^{\infty}\binom{n+1+r-1}{r}x^r=\sum\limits_{r=0}^{\infty}\binom{n+r}{r}x^r
$$

故 $x_r$的系数 $a_{r}= \binom{n+r}{r}$

##### 4. 求母函数

Too difficult to be true:
https://chatgpt.com/share/6963d5ee-04fc-8011-8d5b-2e10e6a9d2eb

>[!faq] 求序列$\{a_{n}\}$的母函数
> $S = \{∞\cdot e_{1}, ∞\cdot e_{2}, ∞\cdot e_{3},  ∞\cdot e_{4}\}$，$a_{n}$是S的满足下列条件的n组合数：
> （1）S中每个元素都出现奇数次
> （2）S中每个元素出现3的倍数次
> （3）$e^1$ 不出现，$e^2$ 至多出现一次。
> （4）$e^1$ 只出现 1、3或11次，$e_{2}$ 只出现2、4或5次。
> （5）S中每个元素至少出现10次。

（1）
$$
\begin{align}
G(x)&=(x+x^3+x^5+\dots+x^{2n+1}+\dots)^4 \\
&=\left( \frac{1}{1-x}-\frac{1}{1-x^2} \right)^4 \\
&=\left( \frac{x}{1-x^2} \right)^4 \\
\end{align}
$$

$$
a_{r}=
\begin{cases}
0\text{（}r-4\text{为奇数）} \\
C\left( 4+\frac{r-4}{2} -1, \frac{r-4}{2} \right) \text{（}r-4\text{为偶数）}
\end{cases}
$$
（2）
$$
\begin{align}
G(x)&=(1+x^3+x^6+\dots+x^{3n}+\dots)^4 \\
&=\left( \frac{1}{1-x^3} \right)^4 \\
&=\left( \frac{1}{1-x} \right)^4 \left( \frac{1}{1+x+x^2} \right)^4\\ \\
&=?
\end{align}
$$
（3）
$$
\begin{align}
G(x)&=1·(1+x)·(1+x+x^2+\dots)(1+x+x^2+\dots) \\
&= \frac{1+x}{(1-x)^2} \\
&=?
\end{align}
$$
（4）
$$
\begin{align}
G(x)&=(x+x^3+x^{11})(x^2+x^4+x^5)(1+x+x^2+\dots)(1+x+x^2+\dots) \\
&=?
\end{align}
$$
（5）
$$
\begin{align}
G(x)&=(x^{10}+x^{11}+x^{12}+\dots)^4 \\
&=?
\end{align}
$$

##### 6. 求母函数

>[!faq] 求序列$\{a_{n}\}$的母函数
> 重集 $S = \{∞\cdot b_{1}, ∞\cdot b_{2}, ∞\cdot b_{3},  ∞\cdot b_{4}, ∞\cdot b_{5}, ∞\cdot b_{6}\}$，$a_{r}$是B的满足下列条件的r组合数：
> （1）每个 $b_i$ 出现3的倍数次
> （2）$b_{1},b_{2}$ 至多出现一次，$b_{3},b_{4}$ 至少出现两次，$b_{5},b_{6}$ 最多出现4次。
> （3）$b_{1}$ 出现偶数次，$b_{2}$ 出现奇数次，$b_{3}$ 出现3的倍数次，$b_{4}$ 出现5的倍数次。
> （4）每个 $b_{i}$ 至多出现8次。

（1）
$$
\begin{align}
G(x)&=(1+x^3+x^6+\dots+x^{3i}+\dots)^6 \\
&=\left( \frac{1}{1-x^3} \right)^6 \\
&=\left( \frac{1}{1-x} \right)^6 \left( \frac{1}{1+x+x^2} \right)^6\\ \\
&=?
\end{align}
$$

（2）
$$
\begin{align}
G(x)&=(1+x)^2(x^2+x^3+x^4+\dots)^2(1+x+x^2+x^3+x^4)^2 \\
&=?
\end{align}
$$
（3）
$$
\begin{align}
G(x)&=(1+x^2+x^4+\dots+x^{2i}+\dots)(x+x^3+x^5+\dots+x^{2i+1}+\dots)(1+x^3+x^6+\dots+x^{3i}+\dots)(1+x^5+x^{10}+\dots+x^{5i}+\dots)(1+x+x^2+x^3+\dots)^2 \\
&=\frac{1}{1-x^2}\frac{x}{1-x^2}\frac{1}{1-x^3}\frac{1}{1-x^5}\left( \frac{1}{1-x} \right)^2 \\
&=?
\end{align}
$$
（4）
$$
\begin{align}
G(x)&=(1+x+x^2+x^3+x^4+\dots+x^{8})^6 \\
&=?
\end{align}
$$
##### 9. 母函数

>[!faq] 各家选人
> 每家出一到两个人参加。设共n个家庭，现从中选出r人。
> （1）设每个家庭都是3口之家，有多少不同选法？当n=50，多少种？
> （2）设n家中两家有4口人，其他家庭都是3口人，多少种？

（1）

$$
\begin{align}
G(x)&=(\binom{3}{1}x+\binom{3}{2}x^2)^n \\
&=3^n(x+x^2)^n \\
&=3^nx^n(x+1)^n \\
&=3^n\sum_{k}\binom{n}{k}x^{k+n} \\
&=\sum_{r}3^n\binom{n}{r-n}x^r
\end{align}
$$

>[!fail] 谬解
>最大分项<=2的整数分拆？
>$$
>\begin{cases}
>1x_{1}+2x_{2}=r \\
>x_{i}\geq 0\quad(i=1,2,\dots,n)
>\end{cases}
>$$
>这一步的含义变成了：你允许“从同一个家庭同时选 1 人和选 2 人”的贡献在乘积里混在一起（相当于把“家庭”拆成了两类独立物品），这就**不是原来的模型**了，所以会错。
>
>它在数“用若干个 1 人单位和若干个 2 人单位凑出总人数 $r$，其中每个单位都有 3 种类型选择”的方案数；并且这些单位是“可重复取”的（因为是几何级数），没有总数量上限（不像原题有 $n$ 家的上限）。

$$
\begin{align}
G(x)&=(1+\binom{3}{1}x+\binom{3}{1}^2x^2+\dots+\binom{3}{1}^n x^n)(1+\binom{3}{2}x^2+\binom{3}{2}^2(x^2)^2+\dots+\binom{3}{2}^n(x^2)^n) \\
&=\sum\limits_{r=0}^{∞}\sum\limits_{i=0}^{r}\binom{3}{1}^i x^i \binom{3}{2}^{r-i}x^{r-i} \\
&=\sum\limits_{r=0}^{∞}\sum\limits_{i=0}^{\lfloor r/2 \rfloor }\binom{3}{1}^{r-2i} x^{r-2i} \binom{3}{2}^{i}x^{2i} \\
&=\sum\limits_{r=0}^{∞}\sum\limits_{i=0}^{\lfloor r/2 \rfloor }\binom{3}{1}^{r-i} x^{r} \\
&=\sum\limits_{r=0}^{∞}(\binom{3}{1}^{\lceil r/2 \rceil }+\dots+\binom{3}{1}^r) x^{r}
 \\
a_{r}&=(1+\dots+3^r)-(1+\dots+3^{\lfloor r/2 \rfloor}) \\
&=\frac{1-3^r-1+3^{\lfloor r/2 \rfloor}}{1-3} \\
&=\frac{3^r-3^{\lfloor r/2 \rfloor}}{2}
\end{align}
$$
（2）

$$
\begin{align}
G(x)&=(\binom{3}{1}x+\binom{3}{2}x^2)^{n-2}(\binom{4}{1}x+\binom{4}{2}x^2)^2 \\
&=3^{n-2}(x+x^2)^{n-2}(4x+6x^2)^{2} \\
&=\sum_{r}3^{n-2}\binom{n-2}{r-n+2}x^r (16x^2+48x^3+36x^4) \\
a_r&=3^{n-2}\Big(
16\binom{n-2}{k}
+48\binom{n-2}{k-1}
+36\binom{n-2}{k-2}
\Big)
\end{align}
$$
##### 13. 无序分拆（实则母函数）

>[!faq] 无序分拆（各分项有限不重复）
> 1g 2枚，2g 3枚，5g 3枚砝码各一枚，要求这8个砝码只能放在天平的一边，能称出几种重量？有几种可能方案？

2g的之前写错了！！！

$$
\begin{align}
G(x)&=(1+x+x^2)(1+x^2+x^4+x^6)(1+x^5+x^{10}+x^{15}) \\
&= (1+x+2x^2+x^3+2x^4+x^5+2x^6+x^7+x^8)(1+x^5+x^{10}+x^{15})\\
\end{align}
$$
0~23，都能凑出，24种。


##### 14. 不定方程

>[!faq] 不定方程（正整数解组的个数）
> 

- 不定方程：相同的球->不同的盒子，不许空盒
- 整数分拆：相同的球->相同的盒子（根据最大分项是否必须取到，区分空盒与否）

$$
\begin{cases}
x_{i}\gt0 \\
x_{1}+x_{2}+\dots+x_{n}=r
\end{cases}
\iff
\begin{cases}
y_{i}+1\ge1 \text{（不要把}x_i, y_{i}\text{的地位弄反）}\\
(y_{1}+1)+(y_{2}+1)+\dots+(y_{n}+1)=r
\end{cases}
\implies {n+r-n-1 \choose r-n}={r-1 \choose n-1}
$$

##### 15. 不定方程

>[!faq] 不定方程
> $x+y+z=24$ 大于1的整数解的个数。

$$
\begin{cases}
x_{i}\gt1 \\
x_{1}+x_{2}+x_{3}=24
\end{cases}
\iff
\begin{cases}
y_{i}+1\gt1\iff y_{i}\geq 1\iff y_{i}>0 \\
(y_{1}+1)+(y_{2}+1)+(y_{3}+1)=24
\end{cases}
\implies
\binom{r-1}{n-1}=
\binom{21-1}{2}=190
$$

记混了！！！

$\binom{n+r-1}{r}$适用于可空，$\binom{r-1}{n-1}$适用于非空，上面的是在非空基础上让其变成2。

或者直接考虑：先都分2、2、2，再对剩下18进行隔板。

#### 生成函数推导

All rows in your table are **ordinary generating functions** (OGFs):

$$  
G(x)=\sum_{k\ge 0} a_k x^k .  
$$

They are obtained from a few “master tricks”:

- Master tricks

**(A) Geometric series**  
$$  
\frac1{1-x}=\sum_{k\ge0}x^k\qquad(|x|<1,\text{ or as a formal series}).  
$$

**(B) Scaling**  
If $G(x)=\sum a_k x^k$, then $G(ax)=\sum a_k (ax)^k$.  
So $\sum a^k x^k=\sum (ax)^k=\frac1{1-ax}$.

**(C) Differentiate to bring down $k$**  
$$  
G'(x)=\sum_{k\ge1} k a_k x^{k-1},\qquad  
xG'(x)=\sum_{k\ge0} k a_k x^{k}.  
$$
So the operator $x\frac{d}{dx}$ multiplies coefficients by $k$.

**(D) Integrate to divide by $k$**  
If $G(x)=\sum_{k\ge0} a_k x^k$, then  
$$  
\int_0^x \frac{G(t)}{t},dt=\sum_{k\ge1}\frac{a_k}{k}x^k.  
$$

**(E) Binomial / negative binomial series**  
For any $\alpha$ (real/complex),  
$$  
(1+x)^\alpha=\sum_{k\ge0}\binom{\alpha}{k}x^k,\quad  
\binom{\alpha}{k}=\frac{\alpha(\alpha-1)\cdots(\alpha-k+1)}{k!}.  
$$  
For integer $n\ge0$,  
$$  
\frac1{(1-x)^{n+1}}=\sum_{k\ge0}\binom{n+k}{k}x^k.  
$$

**(F) Taylor series**  
$$  
e^u=\sum_{k\ge0}\frac{u^k}{k!},\quad  
\cos u=\sum_{k\ge0}\frac{(-1)^k u^{2k}}{(2k)!},\quad  
\sin u=\sum_{k\ge0}\frac{(-1)^k u^{2k+1}}{(2k+1)!},  
$$  
$$  
\arctan u=\sum_{k\ge0}\frac{(-1)^k u^{2k+1}}{2k+1}.  
$$

---

Now derive **each row** in your table

- 1) $a_k=1$

$$  
G(x)=\sum_{k\ge0}1\cdot x^k=\sum_{k\ge0}x^k=\frac1{1-x}  
$$  
(by (A)).

---

- 2) $a_k=a^k$

$$  
G(x)=\sum_{k\ge0}a^k x^k=\sum_{k\ge0}(ax)^k=\frac1{1-ax}  
$$  
(by (B)+(A)).

---

- 3) $a_k=k$

Start from  $\frac1{1-x}=\sum x^k$. Apply  $x\frac{d}{dx}$:  
$$  
x\frac{d}{dx}\left(\frac1{1-x}\right)  
= x\frac{1}{(1-x)^2}  
=\frac{x}{(1-x)^2}  
$$  
and on the series side  
$$  
x\frac{d}{dx}\left(\sum_{k\ge0}x^k\right)=\sum_{k\ge0}k x^k.  
$$  
So  
$$  
\sum_{k\ge0}k x^k=\frac{x}{(1-x)^2}.  
$$

---

- 4) $a_k=k+1$

Differentiate  $\frac1{1-x}$:  
$$  
\frac{d}{dx}\left(\frac1{1-x}\right)=\frac1{(1-x)^2}.  
$$  
But  
$$  
\frac{d}{dx}\left(\sum_{k\ge0}x^k\right)=\sum_{k\ge1}k x^{k-1}  
=\sum_{k\ge0}(k+1)x^k.  
$$  
Hence  
$$  
\sum_{k\ge0}(k+1)x^k=\frac1{(1-x)^2}.  
$$

---

- 5) $a_k=k^2$

Use trick (C) again: if  $G_1(x)=\sum kx^k=\frac{x}{(1-x)^2}$, then  
$$  
xG_1'(x)=\sum k^2 x^k.  
$$  
Compute:  
$$  
G_1(x)=x(1-x)^{-2}  
$$  
$$  
G_1'(x)=(1-x)^{-2}+x\cdot 2(1-x)^{-3}  
=\frac{1-x+2x}{(1-x)^3}  
=\frac{1+x}{(1-x)^3}.  
$$  
Multiply by  $x$:  
$$  
\sum_{k\ge0}k^2x^k=xG_1'(x)=\frac{x(1+x)}{(1-x)^3}.  
$$

---

- 6) $a_k=k(k+1)$

Just rewrite:  
$$  
k(k+1)=k^2+k.  
$$  
So its OGF is the sum of the OGFs for  $k^2$ and  $k$:  
$$  
\sum k(k+1)x^k  
=\frac{x(1+x)}{(1-x)^3}+\frac{x}{(1-x)^2}  
=\frac{x(1+x)+x(1-x)}{(1-x)^3}  
=\frac{2x}{(1-x)^3}.  
$$

---

- 7) $a_k=k(k+1)(k+2)$

Use the negative-binomial coefficient identity:  
$$  
\binom{k+2}{3}=\frac{k(k+1)(k+2)}{6}  
\quad\Rightarrow\quad  
k(k+1)(k+2)=6\binom{k+2}{3}.  
$$  
Also  
$$  
\frac1{(1-x)^4}=\sum_{k\ge0}\binom{k+3}{3}x^k  
$$  
(by (E) with  $n=3)$. Multiply by  $x$:  
$$  
\frac{x}{(1-x)^4}=\sum_{k\ge1}\binom{k+2}{3}x^k.  
$$  
Multiply by  $6$:  
$$  
\sum_{k\ge0}k(k+1)(k+2)x^k=\frac{6x}{(1-x)^4}  
$$  
(the  $k=0$ term is  $0$, consistent).

---

- 8) $a_0=0,; a_k=\dfrac{a^k}{k}$ for  $k\ge1$

Start from geometric series with  $ax$:  
$$  
\frac1{1-ax}=\sum_{k\ge0}a^k x^k.  
$$  
Integrate using (D) (or directly use  $-\ln(1-u)=\sum u^k/k)$:  
$$  
\int_0^x \frac{1}{1-a t},dt  
=\sum_{k\ge0}a^k\int_0^x t^k,dt  
=\sum_{k\ge0}\frac{a^k x^{k+1}}{k+1}.  
$$  
Shift index  $m=k+1$:  
$$  
-\frac1a\ln(1-ax)=\sum_{m\ge1}\frac{a^{m-1}x^m}{m}  
\quad\Rightarrow\quad  
-\ln(1-ax)=\sum_{m\ge1}\frac{a^{m}x^m}{m}.  
$$  
So  $a_m=a^m/m$ and  $a_0=0$.

---

- 9) $a_k=\dfrac{(-1)^k}{(2k)!}$

Use  $\cos u$ Taylor series (F):  
$$  
\cos u=\sum_{k\ge0}\frac{(-1)^k u^{2k}}{(2k)!}.  
$$  
Put  $u=\sqrt{x}$, so  $u^{2k}=x^k$:  
$$  
\cos \sqrt{x}=\sum_{k\ge0}\frac{(-1)^k}{(2k)!}x^k.  
$$

---

- 10) $a_k=\dfrac{(-1)^k}{(2k+1)!}$

Use  $\sin u$:  
$$  
\sin u=\sum_{k\ge0}\frac{(-1)^k u^{2k+1}}{(2k+1)!}.  
$$  
Divide by  $u$ and set  $u=\sqrt{x}$:  
$$  
\frac{\sin \sqrt{x}}{\sqrt{x}}  
=\sum_{k\ge0}\frac{(-1)^k}{(2k+1)!}x^k.  
$$

---

- 11) $a_k=\dfrac{(-1)^k}{2k+1}$

Use  $\arctan u$:  
$$  
\arctan u=\sum_{k\ge0}\frac{(-1)^k u^{2k+1}}{2k+1}.  
$$  
Divide by  $u$, set  $u=\sqrt{x}$:  
$$  
\frac{\arctan \sqrt{x}}{\sqrt{x}}  
=\sum_{k\ge0}\frac{(-1)^k}{2k+1}x^k.  
$$

---

- 12) $a_k=\binom{\alpha}{k}$  ($\alpha$ arbitrary)

Generalized binomial theorem (E):  
$$  
(1+x)^\alpha=\sum_{k\ge0}\binom{\alpha}{k}x^k.  
$$

---

- 13) $a_k=\dfrac{\alpha^k}{k!}$

Exponential series (F):  
$$  
e^{\alpha x}=\sum_{k\ge0}\frac{(\alpha x)^k}{k!}  
=\sum_{k\ge0}\frac{\alpha^k}{k!}x^k.  
$$

---

- 14) $a_k=\binom{n+k}{k}$ (typically  $n\in\mathbb{Z}_{\ge0}$)

Negative binomial series (E):  
$$  
\frac1{(1-x)^{n+1}}=\sum_{k\ge0}\binom{n+k}{k}x^k.  
$$

---

**One “unified view” (why many look like  $\frac{\text{poly}(x)}{(1-x)^m}$)**

Starting from  $\frac1{1-x}$, repeated application of  $x\frac{d}{dx}$ produces OGFs for polynomial sequences  $k, k^2, k^3,\dots$.  
Separately,  $\frac1{(1-x)^{m}}$ generates binomial coefficients  $\binom{k+m-1}{m-1}$, and products like  $k(k+1)\cdots(k+m-1)$ are just factorial multiples of those binomials—hence the clean forms  $\frac{C x}{(1-x)^{m+1}}$.

If you want, I can also show how to generate the next rows systematically (e.g.  $k^3, k^4$, or  $k(k+1)\cdots(k+r))$ using the operator  $x\frac{d}{dx}$ or the negative-binomial identity.