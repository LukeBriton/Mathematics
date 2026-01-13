  >[!todo] 待学
>- [ ] 特征多项式、最小多项式、首一多项式、零化多项式
>- [ ] Cayley-Hamilton定理
>- [ ] 对角化
>- [ ] Jordan

#### 例题

##### 例4.3.5 一阶线性非齐次递推方程

>[!faq] 普通母函数求递推关系
>$a_{n}-5a_{n-1}+6a_{n-2}=2^n(n\geq 2)$

$$
\begin{align}
\text{求通解：}&λ^2-5λ+6=0 \\
&λ_{1}=2,λ_{2}=3 \\
\text{求特解：}&λ-2=0 \\
&λ_{3}=2 \text{（撞根）} \\
&a_{n}=(A_{1}+A_{2}n)2^n+B 3^n \\
\text{试特解：}&A_{2}n 2^n-5A_{2}(n-1)2^{n-1}+6A_{2}(n-2)2^{n-2}=2^n \\
&A_{2}=-2 \\
&a_{n}=(A-2n)2^n+B 3^n =A2^n+B3^n-n2^{n+1}\\
\end{align}
$$
当 $a_{0}=1, a_{1}=-2$
$a_{0}=1=A+B,a_{1}=-2=2A+3B-4$
$a_n=(1-2n)2^n$

##### 例4.3.7 Fibonacci

>[!faq] Fibonacci
>$$
>\begin{cases}
>F_{n}=F_{n-1}+F_{n-2} \\
>F_{1}=F_{2}=1
>\end{cases}
>$$

$$
F_{n}=\frac{1}{\sqrt{ 5 }}\left[ \left( \frac{1+\sqrt{ 5 }}{2} \right)^n - \left( \frac{1-\sqrt{ 5 }}{2} \right)^n \right]
$$
##### 例4.4.1 爬楼梯

>[!faq] 登神长街
>爬楼梯，每次智能1或2级，上到n级的方法。

$$
a_{n}=a_{n-1}+a_{n-2}, a_{1}=1, a_{2}=2 \implies a_{n}=F_{n+1}=\frac{1}{\sqrt{ 5 }}\left[ \left( \frac{1+\sqrt{ 5 }}{2} \right)^{n+1} - \left( \frac{1-\sqrt{ 5 }}{2} \right)^{n+1} \right]
$$

##### 例4.4.2 棋盘染色（推广到n位p进制数不允许某个连续串）

>[!faq] 棋盘染色问题
>$1\times n$棋盘，每块红或蓝色，相邻两块不能都染成红色，染法$a_{n}$种。

$a_n$
- 染红色：$n-1$的块只能是蓝色，所以从$1·1·a_{n-2}$
- 染蓝色：$1·1·a_{n-1}$ 
$a_{1}=2, a_{2}=3$

$$
a_{n}=a_{n-1}+a_{n-2}, a_{1}=2, a_{2}=3 \implies a_{n}=F_{n+2}=\frac{1}{\sqrt{ 5 }}\left[ \left( \frac{1+\sqrt{ 5 }}{2} \right)^{n+2} - \left( \frac{1-\sqrt{ 5 }}{2} \right)^{n+2} \right]
$$

>[!faq] 类似问题扩展
>（1）无两个1相连的n位二进制数共有$F_{n+2}$个。
>（2）无两个0（或两个1，其实等价）相连的n位3进制数共有？p进制数共有？

（1）与棋盘染色问题结构等价。
（2）

按“首位是不是0”分状态：
- 首位不是 $0$ 的串有 $(p-1)a_{n-1}$
- 首位是 $0$，次位必非 $0$，这样的串有 $(p-1)a_{n-2}$

也可按“最后一位是不是 0”分状态：

* $b_n$：长度 $n$ 串以 **0** 结尾且合法的个数
* $c_n$：长度 $n$ 串以 **非 0**（即 $1,\dots,p-1$）结尾且合法的个数
  则 $a_n=b_n+c_n$。

转移：

1. 以 0 结尾：倒数第二位不能是 0，所以必须以非 0 结尾
$$
   b_n = c_{n-1}.
$$
2. 以非 0 结尾：末位有 $p-1$ 种选法，前面任意合法
$$
   c_n = (p-1)a_{n-1}.
$$

$$
a_n=(p-1)(a_{n-1}+a_{n-2}),a_1=p,\ a_2=p^2-1
$$

>[!tip] 如果是00、11都不能出现

3进制：
$a_{n}$
- 2：$a_{n-1}$
因为“末位是 0/1 时，倒数第二位有多种可能”，而这些可能会影响再往前一位能不能选 0/1 ——**不能直接乘一个 $a_{n-2}$​**，需要用“末位状态”来消掉依赖。

* $b_n$：长度为 $n$ 的 3 进制串（允许前导 0），**以 0 结尾**的个数；
* 由于对 0 和 1 的限制对称，“以 1 结尾”的个数也等于 $b_n$；
* $c_n$：长度为 $n$ 的串**以 2 结尾**的个数；
* $a_n = 2b_n + c_n$。

* 末位是 0：前一位不能是 0，所以前一位可以是 1 或 2
$$
  b_n = (\text{以 1 结尾的 }n-1\text{ 串})+(\text{以 2 结尾的 }n-1\text{ 串})
  = b_{n-1}+c_{n-1}.
$$
* 末位是 2：前一位随便
$$
  c_n = a_{n-1}.
$$
$$
a_{n}=2b_n + c_n=2(b_{n-1}+c_{n-1})+a_{n-1}=2b_{n-1}+c_{n-1}+a_{n-1}+c_{n-1}=2a_{n-1}+c_{n-1}=2a_{n-1}+a_{n-2}
$$
空串 $a_{0}$ 取1：
$a_{0}=1, a_{1}=3, a_{2}=7$

$a_3=17$ 容斥：3^3=27，含00的6个，含11的6个，000、111各重复1次，27-(6+6-2)=17

p 进制：
- 末位是0或1：$$b_{n} = b_{n-1}+c_{n-1}$$
- 末位在$\{2,\dots,p-1\}$，有p-2种：$$c_{n}=(p-2)a_{n-1}$$
$$
a_{n}=2b_n + c_n=2(b_{n-1}+c_{n-1})+(p-2)a_{n-1}=(p-1)a_{n-1}+c_{n-1}=(p-1)a_{n-1}+(p-2)a_{n-2}
$$

$a_0=1, a_1=p, a_2=p^2-1$ （因为长度 2 总共 $p^2$，只禁掉 00 和 11 两个。）

##### 例4.4.6 （见[[球、盒]]）


##### 例4.5.2 错排

[[Inclusion–Exclusion Principle#例5.3.2 错排]]

>[!faq] 错排问题
>n个元素全排列，每个元素都不在自己原来位置上的排列数。

- $i$ 与某个数互换后，$n-2$ 个数错排。$(n-1) D_{n-2}$
- $i$ 不动，其他 $n-1$ 个数先错排，然后 $i$ 与其他每一个数互换位置。$(n-1) D_{n-1}$

$$
\begin{cases}
D_{n}=(n-1)(D_{n-1}+D_{n-2}) \\
D_{1}=0, D_{2}=1(D_{3}= 3)
\end{cases}
$$
与
$$
\begin{cases}
T_{n}=nT_{n-1}+(-1)^n (n\geq2) \\
T_{1}=0
\end{cases}
$$
是同一数列。

$$
D_{n}=n!\sum_{k=0}^n \frac{(-1)^n}{k!}\sim \frac{n!}{e}(n\gg 1)
$$
（容斥法见![[Inclusion–Exclusion Principle#例5.3.2 错排]]）
##### 例4.5.6（见例4.4.2）

##### 例4.5.7 圆形扇区染色

>[!faq] 圆形扇区染色
>圆盘，n个扇区，k种颜色，相邻扇形没有相同颜色，染法。

$$
\begin{cases}
a_{n}=(k-1)a_{n-2}+(k-2)a_{n-1} \\
a_0 = 1, a_1 = k, a_2 = k(k-1), a_3 = k(k-1)(k-2)
\end{cases}
$$

##### 例4.5.8 平面不连通区域划分

>[!faq] 平面不连通区域划分
>n个圆（$n\geq2$），任意两个圆都相交，但无3个圆共点，这n个圆把平面划分成多少个不连通的区域。

$a_{0}=1, a_{1}=2, a_{2}=4$

新加入的第n个圆，它与之前每一个圆都相交，产生$2(n-1)$个交点，圆周被这些交点分割成$2(n-1)$段弧，而每一段弧都位于加入前某一个已有区域内部；把这段弧画进去，就会把该区域**一分为二**，所以**每段弧都会让区域数 +1**。

$a_{n}=a_{n-1}+2(n-1), a_{1}=2$

$$
a_{n}=
\begin{cases}
n^2-n+2 & (n\geq 1) \\
1  & (n=0)
\end{cases}
$$

##### 例4.5.9 排序算法

>[!faq] 排序算法
>（1）选择排序
>（2）分治排序
>（3）快速排序（最坏、最好、平均）

（1）
$$
\begin{cases}
T(n)=T(n-1)+(n-1) \\
T(1)=0
\end{cases}
\implies T(n)=\frac{n(n-1)}{2}=O(n^2)
$$
（2）
$$
\begin{cases}
T(n)=2T\left( \frac{n}{2} \right)+(n-1) \\
T(1)=0
\end{cases}
\implies T(2^m)=m^{2m}-(2^m-1)\implies T(n)=n\log_{2}n-(n-1)=O(\log_{2}m)
$$
（3）
$$
C(n)=2(n+1)\log_{2}n+O(n)
$$

#### 习题

##### 10. 球内空间划分

>[!faq] 球内空间划分
>过一个球的中心做 $n$个平面，其中无3个平面过一直径，这些平面可把球的内部分成多少个两两无公共部分的区域？

新加入的第n个平面，它与之前每一个平面都相交于$(n-1)$条过球心的直线（在球内对应 $n−1$ 条直径方向）。

在平面$P_{n}$内，看它与球的交面：

圆盘被$(n-1)$条过球心的直线分割成 $2(n-1)$ 个扇形小块，而每出现一个扇形小块，就会把球内原来的一个区域**一分为二**，所以**每个扇形都会让区域数 +1**。

$a_{n}=a_{n-1}+2(n-1), a_{1}=2$

$$
a_{n}=
\begin{cases}
n^2-n+2 & (n\geq 1) \\
1  & (n=0)
\end{cases}
$$

##### 11. 空间划分

>[!faq] 空间划分
>设空间的 n 个平面两两相交，每3个平面有且只有一个公共点，任意4个平面都不共点，这样的n个平面把空间分割成多少个不重叠的区域？


* 任意两条 $\ell_i,\ell_j$ 都相交：因为对应三平面 $P_n,P_i,P_j$ 有且只有一个公共点，该点就在 (P_n) 上，所以 $\ell_i\cap \ell_j$ 是一个点；
* 任意三条 $\ell_i,\ell_j,\ell_k$ 不共点：否则四平面 $P_n,P_i,P_j,P_k$ 会共点，违背“任意4个平面都不共点”。

$P_n$​ 内的这 $m=n−1$ 条直线把平面 $P_n$​ 分成的区域数是经典公式

$$
L_m=1+m+\binom{m}{2}
$$

而 $P_n$​ 每切过球体/空间中的一个区域，就把它分成两块；新增区域数恰好等于 $P_n$​ 自身被这些交线分成的块数 $L_{n-1}$​。于是

$$
R_n = R_{n-1} + \Bigl(1+(n-1)+\binom{n-1}{2}\Bigr),R_{1}=1
$$
$$
\begin{align}
R_{n}&=\frac{n^3+5n+6}{6} \\
&= 1+\sum_{k=1}^{n}1+\sum_{k=1}^{n}(k-1)+\sum_{k=1}^{n}\binom{k-1}{2} \\
&= 1+n+\binom{n}{2}+\binom{n}{3}. \\
&=\frac{n^3+5n+6}{6}
\end{align}
$$

##### 12. 相邻位不同

>[!faq] 相邻位不同
>相邻位不同为0的n位二进制数中一共出现了多少个0？

- 首位是0：$a_{n-2}$
- 首位是1：$a_{n-1}$

$a_{n}=a_{n-1}+a_{n-2},a_{0}=1,a_{1}=2,a_{2}=3$

$a_n = F_{n+2}$

以上是“相邻位不同为0的n位二进制数”的个数

一共出现了多少个0？何意味

把所有满足“**不出现 00**（相邻两位不能同时为 0）”的 $n$ 位二进制串一一列出来；  
对每个串数一数里面有几个 0；**把这些 0 的个数加总**，得到的就是“0 一共出现了多少次”。

合法串要么以 **1** 结尾，要么以 **10** 结尾（不能以 00 结尾）：
$$S_n = S_{n-1}1 \sqcup S_{n-2}10$$
$$Z_n=\sum_{s\in S_n}(\text{串 }s\text{ 中 0 的个数}).$$
用同样的分解 $S_n=S_{n-1}1\sqcup S_{n-2}10$ 来数 0：

* 来自 $S_{n-1}1$：末位加的是 1，不新增 0，所以贡献 **就是** $Z_{n-1}$。
* 来自 $S_{n-2}10$：每个前缀串贡献原来的 0（总计 $Z_{n-2}$），并且末尾 **一定新添 1 个 0**，这样的串有 $a_{n-2}$ 个，所以还要再加 $a_{n-2}$。

$$
\begin{align}
Z_{n}&=Z_{n-1}+Z_{n-2}+a_{n-2}, \\
&=Z_{n-1}+Z_{n-2}+F_{n} \\ \\
Z_{0}&=F_{0} \\
Z_{1}&=F_{1} \\
Z_{2}&=Z_{1}+Z_{0}+F_{0}=F_{2} \\
Z_n&=\frac{nF_{n+2}+(n+2)F_n}{5}
\end{align}
$$


##### 13. 平面直线划分

>[!faq] 平面直线划分
>平面上有两两相交，无3线共点的n条直线，这n条直线把平面分成多少区域？


* 任意两条 $\ell_i,\ell_j$ 都相交
* 任意三条 $\ell_i,\ell_j,\ell_k$ 不共点

* 加入第 $m$ 条直线 $\ell_m$：

  * 它与之前的 $m-1$ 条直线各相交一次；
  * 且因为“无三线共点”，这 $m-1$ 个交点都**互不重合**，沿着 $\ell_m$ 排成一列。
  * 于是 $\ell_m$ 被这些交点切成 $m$ 段**（交点数 $m-1$ ⇒ 分成 $m$ 段）。

关键一步：**每一段线段都落在“加入前”的某一个区域内部**，画进去会把那个区域一分为二，因此每一段都会让区域数 **+1**。

所以新增区域数 = 段数 = $m$，即
$$
L_m = L_{m-1}+m.
$$
$L_0=1, L_1=2, L_2=4$
$$
L_m=1+m+\binom{m}{2}
$$


#### 一元线性递推

实数数列 $(a_0,a_1,a_2,\dots)$ 看作无限维向量，构成线性空间：
$$
\mathcal{V} = \{(a_0,a_1,\dots)\mid a_n\in\mathbb{R}\}
$$
定义**右移算子** (T)：
$$
(Ta)_n := a_{n+1}.
$$
直觉：$T$ 就是“把数列整体向前挪一位”。一般地，$(T^k a)_n = a_{n+k}$。

现在看一个典型的线性递推（常系数齐次）：
$$
a_{n+k} = c_{k-1} a_{n+k-1} + \dots + c_1 a_{n+1} + c_0 a_n.
$$
用 $T$ 来写：
$$
(T^k a)_n = c_{k-1} (T^{k-1}a)_n + \dots + c_1 (T a)_n + c_0 a_n.
$$
即：
$$
P(T)a:=\bigl(T^k - c_{k-1}T^{k-1} - \dots - c_1 T - c_0 I\bigr)a = 0,
$$
**递推公式 = 在线性空间 $\mathcal{V}$ 中，数列向量 $a$ 满足某个线性算子（零化多项式） $P(T)$ 的“零空间”（特征子空间？）约束：
$$
P(\lambda)=\lambda^k - c_{k-1}\lambda^{k-1} - \dots - c_0
$$
即特征多项式。

所有满足递推的数列构成 $\mathcal{V}$ 中的一个**线性子空间**。

对 $k$ 阶递推，定义“状态向量”：

$$
v_n =
\begin{pmatrix}
a_n\\
a_{n+1}\\
\vdots\\
a_{n+k-1}
\end{pmatrix}
\in \mathbb{R}^k.
$$

由递推关系：
$$
a_{n+k} = c_{k-1} a_{n+k-1} + \dots + c_0 a_n,
$$
可以写出：

$$
v_{n+1} =
\begin{pmatrix}
a_{n+1}\\
a_{n+2}\\
\vdots\\
a_{n+k}
\end{pmatrix}
=
A
\begin{pmatrix}
a_n\\
a_{n+1}\\
\vdots\\
a_{n+k-1}
\end{pmatrix}
= A v_n,
$$

（友矩阵/Frobenius块）矩阵$A$：
$$
A=
\begin{pmatrix}
0      & 1      & 0      & \cdots & 0\\
0      & 0      & 1      & \cdots & 0\\
\vdots & \vdots & \vdots & \ddots & \vdots\\
0      & 0      & 0      & \cdots & 1\\
c_0    & c_1    & c_2    & \cdots & c_{k-1}
\end{pmatrix}.
$$
$T$ 在循环基（循环子空间的一个基）下的矩阵。

##### 二重根

设矩阵在某个基下有一个 $2\times2$ Jordan 块：
$$
J =
\begin{pmatrix}
\lambda & 1\\
0 & \lambda
\end{pmatrix}.
$$

$$
J = \lambda I + N,\quad
N =
\begin{pmatrix}
0 & 1\\
0 & 0
\end{pmatrix}.
$$
注意两个事实：

1. $N$ 不是 0，但
2. $N^2 = 0$（因为再乘一次就把非零的那个 1 推到对角线外、变成 0 了）。

这一点很关键：**$N$ 是一个幂零矩阵（nilpotent）**。

可以像二项式一样展开：
$$
J^n = (\lambda I + N)^n
= \sum_{k=0}^n \binom{n}{k} \lambda^{n-k} N^k=\lambda^n I + n\lambda^{n-1} N.
$$
写成矩阵就是：
$$
J^n
=

\begin{pmatrix}
\lambda^n & n\lambda^{n-1}\\
0 & \lambda^n
\end{pmatrix}
= \lambda^n
\begin{pmatrix}
1 & \displaystyle\frac{n}{\lambda}\\
0 & 1
\end{pmatrix}.
$$

现在看它怎样作用在向量上。对任意$\begin{pmatrix} x\\ y\end{pmatrix},$
有
$$
J^n
\begin{pmatrix} x\\ y\end{pmatrix}
=

\begin{pmatrix}
\lambda^n x + n\lambda^{n-1} y\\
\lambda^n y
\end{pmatrix}
=

\lambda^n
\begin{pmatrix}
x + \dfrac{n}{\lambda} y\\
y
\end{pmatrix}.
$$
关键观察：**第一个分量是 $\lambda^n$ 乘上“关于 $n$ 的一次多项式”。**

把 $\lambda=2$ 代入，即：
$$
\begin{pmatrix}
a_n\\
*
\end{pmatrix}
= J^n
\begin{pmatrix}
x\\ y
\end{pmatrix}
\Rightarrow
a_n = \lambda^n\Bigl(x + \frac{n}{\lambda}y\Bigr)
= \underbrace{x\lambda^n}_{\alpha_1\lambda^n}
+\underbrace{\frac{y}{\lambda}n\lambda^n}_{\alpha_2n\lambda^n} .
$$

##### 三重根

三重根时，对应的 Jordan 块是
$$
J =
\begin{pmatrix}
\lambda & 1      & 0\\
0       & \lambda& 1\\
0       & 0      & \lambda
\end{pmatrix}
= \lambda I + N,\quad
N=
\begin{pmatrix}
0 & 1 & 0\\
0 & 0 & 1\\
0 & 0 & 0
\end{pmatrix}.
$$
此时

- $N\neq 0$；
- $N^2\neq 0$（只是在更上面的超对角线上）；
- 但 $N^3=0$。

同样用二项式展开：
$$
J^n = (\lambda I + N)^n
= \sum_{k=0}^n \binom{n}{k} \lambda^{n-k} N^k=\lambda^n I + n\lambda^{n-1}N + \binom{n}{2}\lambda^{n-2}N^2.
$$
##### m 重根

在友矩阵（companion matrix）那里：

- 特征多项式就是递推的特征方程；
- 某个根 $\lambda$ 的**代数重数 = 它对应所有 Jordan 块的大小之和**。

如果在这个特征值上恰好只有一个 Jordan 块，大小为 $m$，
那就对应了 $m$ 个线性无关解：
$$
\lambda^n,\ n\lambda^n,\ \dots,\ n^{m-1}\lambda^n.
$$

- 代数重数（algebraic multiplicity, AM）
	- $\chi_A(t) = \det(tI-A)=(t-\lambda)^m q(t),\quad q(\lambda)\neq 0,$
	- m： **$\lambda$ 在特征多项式里出现了几次**
- 几何重数（geometric multiplicity, GM）
	- $E_\lambda = \ker(A-\lambda I) = \{v\neq 0 : Av=\lambda v\}\cup\{0\}$
	- $\dim E_\lambda$ ：**“有多少个线性无关的特征向量方向”**
- $1 \le \text{GM}(\lambda) \le \text{AM}(\lambda).$
	- 如果 GM = AM，则这个特征值对应的部分可以完全对角化；
	- 如果 GM < AM，则这一部分出现了 Jordan 块，无法对角化，会有 $n\lambda^n$ 那种东西。
- 对于特征值 (\lambda)，它对应的 Jordan 块大小为 $s_1,\dots,s_r$，满足
$$
s_1 + \dots + s_r = \text{AM}(\lambda),\quad
r = \text{GM}(\lambda).
$$

* 每个大小为 $s$ 的 Jordan 块会贡献一条**长为 $s$** 的“广义特征向量链”，解的形态是
$$
\lambda^n, n\lambda^n, \dots, n^{s-1}\lambda^n
$$
  这种“多项式 $\times \lambda^n$”。

* 所有块加起来，一共得到 $AM(\lambda)$ 个线性无关解。

于是：
- AM 决定**总共有多少个解方向**；
- GM 决定**这些方向里有多少是“纯 $\lambda^n$”，有多少是带 $n$、$n^2$ 的链**；
- “块越大” ⇒ “多项式次数越高”。

循环矩阵的**极小多项式 = 特征多项式**，**每个特征值只出现一个 Jordan 块**。

* 若递推的特征方程 $(t-\lambda)^m=0$，
  对应伴随矩阵在 $\lambda$ 上一定是“一个大小为 $m$ 的 Jordan 块”；
* 所以 $GM(\lambda) = 1$，$AM(\lambda) = m$；
* 正好对应我们在数列书上用的公式：
$$
\lambda\ \text{是 }m\text{ 重根} \Rightarrow
a_n \text{中会出现 } \lambda^n,\ n\lambda^n,\ \dots,\ n^{m-1}\lambda^n.
$$

##### 复特征值

**特征值是复数 ≠ 一定循环**。  
它一般意味着“带振荡的指数行为”，只有在很特殊的条件下才会真正“循环”。

假设递推方程是实系数的（课本里那种线性递推），特征值如果有复数，一定是**共轭成对**出现：

$$  
\lambda_{1,2} = re^{\pm i\theta}.  
$$

对应的那两部分解是

$$
c_1 \lambda_1^n + c_2 \lambda_2^n  
= r^n\bigl(C_1 e^{in\theta} + C_2 e^{-in\theta}\bigr),  
$$

对实数初值来说，最终可以合并成

$$
a_n = r^n\bigl(A\cos(n\theta) + B\sin(n\theta)\bigr).  
$$

有重根：

$$
a_n = r^n\bigl[(A_{1}+A_{2}n+\dots+A_{m}n^{m-1})\cos(n\theta) + (B_{1}+B_{2}n+\dots+B_{m}n^{m-1})\sin(n\theta)\bigr].  
$$


所以：

- $r$ 决定**振幅是指数增长/衰减**；
    
- $\theta$ 决定**“振荡频率”**。


“循环”：存在正整数 $T$ 使得  
$$
a_{n+T} = a_n \quad \forall n  
$$
（非零解）。

用上面的形式来看，关键在于那部分：
$$
r^n e^{in\theta}.  
$$

想要 $a_{n+T} = a_n$ 对所有 n 成立，需要同时满足：

1. **模长不变**：  
    $$
    |r^{n+T}| = |r^n| \quad \Rightarrow\quad r^T = 1 \Rightarrow r=1.  
    $$
    否则振幅在变，就不可能周期（除非整条数列都是 0）。
    
2. **角度是“有理角”**：  
    $$ 
    e^{i(n+T)\theta} = e^{in\theta} \quad\forall n  
    \Rightarrow e^{iT\theta} = 1  
    \Rightarrow T\theta = 2\pi k,\ k\in\mathbb{Z}.  
    $$ 
    也就是说  
    $$
    \frac{\theta}{2\pi} \in \mathbb{Q}.  
    $$ 
    换成特征值，就是 $\lambda = e^{i\theta}$ 是**单位根**（root of unity）。
    

**要想“真正周期”，对应的复特征值必须：**

- 模长 (r=1)；
- 并且是单位根（角度是 (2\pi) 的有理倍数）。

针对一般复特征值分情况：

1. $|\lambda| = r \neq 1$：
    
    - 解形如 $r^n(\cos n\theta,\sin n\theta)$，振幅指数涨或指数降；
        
    - 会“抖动+变大/变小”，**不是周期**（除非解退化成 0）。
        
2. $|\lambda| = 1$ 但不是单位根（$\frac{\theta}{2\pi}$ 无理）：
    
    - 解是 $a_n = A\cos(n\theta)+B\sin(n\theta)$，振幅稳定、但**不重现周期**；
        
    - 序列会“看起来像在绕圈，但永远不重复”：是**准周期**，在单位圆上密绕。
        
3. $\lambda$ 是单位根：
    
    - 这部分解确实是**周期的**；
        
    - 再加上其它模 <1 的根都衰减掉，最后“极限行为”可能看起来周期。
        
4. 如果还有 Jordan 块（出现 $n\lambda^n$）：
    
    - 即便 $|\lambda|=1$，有个 $n$ 因子也会让振幅慢慢变大；
        
    - 于是**也不会真正周期**（除非对应系数为 0）。

在线性动态系统 $v_{n+1}=Av_n$ 里：

- 复特征值 $|\lambda|=1$：轨道在某个椭圆/圆上“旋转”；
    
- $|\lambda|\neq1$：轨道沿着某方向螺旋地离开/靠近原点。
    

只有当所有“旋转角度”都是 $2\pi\cdot\frac{p}{q}$ 这类有理角，并且没有 $n\lambda^n$ 这样的 Jordan 增长项时，轨道才会真的成**封闭多边形/多边形轨道**——对应到数列上，就是**周期序列**。

 ##### 非齐次

$$
L:= P(T)=T^k - c_{k-1}T^{k-1} - \dots - c_1 T - c_0 I
$$

$f$ **的零化子**：多项式 $Q$，使得 $Q(T)f=0$。

对右端 $f$，考虑它在 $T$ 作用下生成的**循环子空间**
$$
W := \mathrm{span}\{f, Tf, T^2f, \dots\}.
$$这是一个有限维 $T$-不变子空间（在“多项式 × 指数”的情形下）。

对 (T) 在一个有限维空间 (W) 上，总存在一个多项式 (Q) 使得
$$
  Q(T)|_W = 0,
$$
也就是说 $Q(T)w=0,\ \forall w\in W$。
这个 $Q$ 就是 $T|_W$ 的极小多项式。

* 我们其实是在说：**右端 $f$ 落在一个有限维的、$T$-不变的循环子空间 $W$ 里**；
* 然后找到 $T$ 在 $W$ 上的极小多项式 $Q$；
* 于是 $Q(T)$ 在 $W$ 上恒等于 0，特别是对 $f$ 有 $Q(T)f=0$.


$$
\begin{align}
f_{n}=3^n \implies (T-3I)f的第n项&=(Tf)n-3f_{n}=f_{n+1}-3f_{n}=3^{n+1}-3·3^n=0 \\
Q(T)=T-3I &\implies Q(\lambda)=\lambda-3
\end{align}
$$

$$
\begin{align}
f_{n}=n·3^n \implies (T-3I)^2f的第n项&=(T^2-6T+9I)f_{n} \\
&=f_{n+2}-6f_{n+1}+9f_{n} \\
&=(n+2)3^{n+2}-6(n+1)·3^{n+1}+9n·3^n \\
&=(9n+18-18n-18+9n)=0 \\
Q(T)=(T-3I)^2 &\implies Q(\lambda)=(\lambda-3)^2
\end{align}
$$

$\lambda$ 的 Jordan 块越大，需要的 $(T-\lambda I)^m$ 次数越高。

$$
La=f \implies Q(T)La=Q(T)f=0
$$
也即
$$
R(T)a:=Q(T)L=(Q·P)(T)=0
$$

- **非齐次方程的解被包含在一个更大维度的齐次解空间里**，
- 这个更大空间的“基解形式”由 $Q(\lambda)P(\lambda)$ 的根及重数决定。

之后多重根（撞根）的情况求解方法同齐次。

在一个有限维的“好空间”里（多项式×指数×三角），右边 $f_n$ 是下列基本块的有限线性组合：
- **指数类**：$\lambda^n$；
- **多项式类**：$n^m$；
- **多项式×指数**：$n^m\lambda^n$；
- **三角类**：$\cos(n\theta),\ \sin(n\theta)$（相当于 $\Re(e^{in\theta}))、(\Im(e^{in\theta})$）；

以及这些东西的**有限和**。

(1) $f_n = \lambda^n$

* $Tf = \lambda^{n+1} = \lambda f$，所以
  $$
  W=\mathrm{span}\{f\}
  $$
  一维；
* 极小多项式 $Q(\lambda)=\lambda-\lambda_0$，$Q(T)=T-\lambda_0 I$；
* 所以 $(T-\lambda_0 I)f=0$。

(2) $f_n = n\lambda^n$

* $\{f,Tf,T^2f,\dots\}$ 能张成一个 2 维子空间；
* 对这个子空间，$T$ 的矩阵是一个 $2\times2$ Jordan 块；
* 极小多项式 $Q(\lambda)=(\lambda-\lambda_0)^2$；
* 所以 $(T-\lambda_0 I)^2f=0$。

(3) $f_n = P(n)\lambda^n$，其中 (P) 是次数 (d) 的多项式

* 这时 $\mathrm{span}\{f,Tf,\dots\}$ 维数 $\le d+1$；
* $T$ 在这个子空间上的极小多项式是 $(\lambda-\lambda_0)^{d+1}$；
* 所以 $(T-\lambda_0 I)^{d+1} f = 0$。

(4) $f_n=\cos(n\theta)$ 或 $\sin(n\theta)$

* 你可以把它看成 $\Re(e^{in\theta}))、(\Im(e^{in\theta})$，对应复特征值 $e^{\pm i\theta}$；
* 最终有一个二阶算子可以杀掉它们：
$$
\bigl(T^2 - 2\cos\theta,T + I\bigr) f = 0;
$$
* 对应多项式是：$(\lambda-e^{i\theta})(\lambda-e^{-i\theta}) = \lambda^2 - 2\cos\theta\lambda + 1$。

$f$ 是上述东西的**有限和**

比如：
$$
f_n = (1+n)2^n + 5n^2 + 7\cos(\tfrac{\pi}{3} n).
$$

可以拆成三块 $f = f^{(1)}+f^{(2)}+f^{(3)}$，分别是：

* $f^{(1)}_n=(1+n)2^n$：湮灭子 $Q_1(T)=(T-2I)^2$；
* $f^{(2)}_n=5n^2$：湮灭子 $Q_2(T)=(T-I)^3$；
* $f^{(3)}_n=7\cos(\tfrac{\pi}{3} n)$：湮灭子 $Q_3(T)=T^2 - 2\cos(\tfrac{\pi}{3})T + I$。

要同时杀掉这三块，直接用
$$
Q(T) = Q_1(T)Q_2(T)Q_3(T),
$$
它一定能让 $Q(T)f=0$。
（更精细一点是取“多项式的最小公倍数”，但算递推时一般取乘积就够了，只是阶会高一些。）

**所以：只要右端 $f$ 是若干“指数/多项式/三角/它们的乘积”的有限线性组合，这个大空间是有限维的**，我们总能找到一个多项式湮灭子 $Q$。


