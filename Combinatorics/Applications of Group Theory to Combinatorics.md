![[Algebraic Structures#Algebraic Structure Ladder (Set → Field)]]

封闭性！封闭性！封闭性！

##### 证明所有置换构成一个群

置换：双射

- 封闭：复合后仍双射
- 结合：复合
- 逆：双射
- 幺：e

##### 轮换

$(a_{1},a_{2},\dots,a_{k}):a_{1}\mapsto a_{2}, a_{2}\mapsto a_{3}, \dots, a_{k}\mapsto a_{1}$ 

k阶轮换: $p^k=e:a_{1}\mapsto a_{1}, \dots, a_{k}\mapsto a_{k}$

轮换


[浅谈置换群计数](https://codgician.me/zh-hans/posts/2020/03/permutation-group/)

对于任意置换的不交轮换分解是唯一的

- 恒等置换
- 非恒等置换，$\exists i, σ(i)\neq i$
	$(i,σ(i),σ^2(i),σ^3(i),\dots,σ^{t-1}(i))$ （t取最小）是一个轮换（抽屉原理）

[abstract algebra - Logic for decomposing a permutation into different products composed of transpositions - Mathematics Stack Exchange](https://math.stackexchange.com/questions/499613/logic-for-decomposing-a-permutation-into-different-products-composed-of-transpos)

（对换/换位）**A transposition is a cycle of length 2.**

It might be helpful to recall that the decomposition of a permutation into transpositions is _**not unique**_. We are assured only that any valid decomposition of a given permutation will always yield either a product of an even number of transposition, or a product of an odd number of transpositions, never both.

##### Polya 定理

#### 例题

##### 例7.9.1 正三角形置换群

>[!faq] 正三角形置换群
>- 旋转对称映射（绕重心逆时针旋转0、120°、240°）
>- 反射对称映射（绕对称轴1A, 2B, 3C 反转180°）

##### 例7.9.2 正方形对称群

>[!faq] 正方形对称群
>- 旋转对称映射（绕重心逆时针旋转0、90°、180°、270°）$p_{1}\dots p_{4}$
>- 反射对称映射（绕对称轴A-A', B-B', 1-3, 2-4 反转180°）$p_{5}\dots p_{8}$

**只有 8 个**来自正方形的刚体对称——这就是**二面体群 $D_4$**。

将1、2；1、4分别做扭转的非刚体运动/柔性运动，再对其做与$p_{1}\dots p_{8}$相应的变换，各8种置换。

共24种置换，得到$S_{4}$，但它不是“正方形对称群”，一般不会保持正方形的边-顶点邻接结构（例如 $(1,2)$ 会把边 $2-3$ 变成 $1-3$，这不是原来的边），因此它**不是正方形作为几何图形/四边形骨架的对称**。


##### 例7.10.1 等边三角形顶点着色

>[!faq] 等边三角形顶点着色
>红绿蓝三色对等边三角形顶点着色

$|\text{Sym}(\bigtriangleup)|=6$

$Q_{1}=S_{3}=\text{Sym}(\bigtriangleup)=\{(1)(2)(3), (1 2 3), (1 3 2), (1) (2 3), (2) (1 3), (3) (1 2)\}$

不等价的着色方案数：

$$
l_{1}=\frac{1}{6}(1\times3^3+2\times 3^1+ 3\times 3^2)=10
$$

若考虑只有旋转没有反转：

$Q_{2}=\{(1)(2)(3), (1 2 3), (1 3 2)\}$

$$
l_{2}=\frac{1}{3}(1\times3^3+2\times 3^1)=11
$$

##### 例7.10.2 正方形4小格着色

>[!faq] 正方形4小格着色
>两种颜色对正方形4小格顶点着色

是否可以视为对正方形4顶点着色？

有点儿多，不如直接枚举…… $2^4=16$，

$S=\{1,2,3,4\} C=\{黑,白\} C^S=\{f_1,...,f_{16}\}$

这里$Q=\{q_{1},q_{2},q_{3},q_{4}\}$，是针对$S$的置换集（绕大的正方形中心逆时针旋转）。


$$
Q:
\begin{cases}
q_{1}=(1)(2)(3)(4) &(旋转0°) \\
q_{1}=(1 2 3 4) &(旋转90°) \\
q_{1}=(1 3)(2 4) &(旋转180°) \\
q_{1}=(4 3 2 1) &(旋转270°)
\end{cases}
$$
对应于$C^S$上的置换集为$\{p_{1},p_{2},p_{3},p_{4}\}$，代入Polya定理得 L=6。

这 6 类着色直观上是什么？

按“黑点个数 + 两黑点相对位置”分：

1. 0 黑（全白）
2. 4 黑（全黑）
3. 1 黑
4. 3 黑
5. 2 黑且相邻
6. 2 黑且对角（相对）

共 6 类。

**这里为什么不用考虑反射对称或非刚体运动？**

反射要不要算：取决于题目把“镜像”算不算同一种

* 若你认为图案在桌面上只能**旋转**来比较（不允许翻面、也不把镜像当同一个），用 **旋转群 (C_4)**（4 元）。
* 若你认为镜像也视为相同（例如可以把纸翻过来、或你把镜像也当等价），就该用 **(D_4)**（8 元）。

##### 例7.12.2 正六边形顶点着色

>[!faq] 正六边形顶点着色
>红黄蓝三色，正六边形顶点着色。正六边形可以绕几何中心或沿对称轴翻转。

绕中心旋转0, 60, 120, 180, 240, 300度，过三对顶点、三对边中点轴，共12个置换。

- (1)(2)(3)(4)(5)(6) 6
- (1 2 3 4 5 6) 1
- (1 3 5)(2 4 6) 2
- (1 4)(2 5)(3 6) 3
- (1 5 3)(2 6 4) 2
- (6 5 4 3 2 1) 1

- (1)(4)(2 6)(3 5) 4
- (3)(6)(1 5)(2 4) 4
- (2)(5)(1 6)(3 4) 4

- (1 6)(2 5)(3 4) 3
- (1 2)(3 6)(4 5) 3
- (1 4)(2 3)(5 6) 3

$$
L=\frac{1}{12}(2·3^1+2·3^2+4·3^3+3·3^4+3^6)=92
$$

#### 习题

##### 1. 证明是群

>[!faq] 证明成群
>（1）$G_1=\{x|x=3k,k\in \mathbb{Z}\}$，$\forall a,b \in G_{1}$，$a + b:=a+_{\mathbb{Z}}b$
>（2）$G_2=\{1,2,4,7,8,11,13,14\}$，$\forall a,b \in G_{2}$，$a\cdot b=ab\mod 15$
>（3）$G_3=\{1,2,4,8,16,32\}$，$\forall a,b \in G_{3}$，$a\cdot b=ab\mod 21$。证明其为循环群，给出生成元。

（1）$G_{1}=3\mathbb{Z}$
$\forall a, b, c\in G_{1}$ 令其分别为 $a=3k_{1}, b=3k_{2}, c=3k_{3}$
- 封闭性：$a+b=3k_{1}+3k_{2}=3(k_{1}+k_{2})$
	$k_{1}+k_{2}\in \mathbb{Z} \implies a+b=3(k_{1}+k_{2})\in G_{1}$
- 结合性：与整数加法相容。。
- 幺元：
	- $0+a=a+0=a$
- 逆元：
	- $-k_{1}\in \mathbb{Z} \implies 3(-k_{1})=-3k_{1}\in \mathbb{Z}$
	- $-3k_{1}+a=a+(-3k_{1})=0$

（2）**整数模 n 乘法群**/**模 n 既约剩余类** $U(15)$，阶 8

可知$\forall g\in G_{2}$, $\gcd(g, 15)=1$，且$G_2$包含了15以内所有与其互质的数。

- 封闭性：$\forall a, b\in G_{2}, \gcd(a,15)=1, \gcd(b, 15)=1, \gcd(ab, 15)=\gcd(ab \mod 15, 15)=1$
	- $d|m \land d|n \iff d|n \land d|(m-qn)$
	- $\implies \gcd(m,n)=\gcd(qn+r,n)=\gcd(r,n)$
- 结合性：$\forall a,b,c\in G_{2}$
	- $(a·b)·c= (ab \mod 15)·c=  (abc \mod 15)\mod 15=  abc \mod 15$
	- $a·(b·c)= a·(bc \mod 15)=  (abc \mod 15)\mod 15=  abc \mod 15$
	- $a·(b·c)\equiv(a·b)·c \mod 15$
- 幺元：
	- $1·a\equiv a·1 \mod 15$
- 逆元：
	- $\forall a\in G_{2}, ax\equiv 1 \mod 15$
	- Bézout 定理：$ax+by=1$ 有整数解 $\iff gcd(a,b)=1$
		$\forall a\in G_{2}, \gcd(a,15)=1$ $\implies$ $\exists y\in \mathbb{Z}, ax-15y=1$ $\implies$ $ax\equiv 1 \mod 15$
	- 但是需不需要再证明 $x\in G_{2}$？尽管对于该题可以简单枚举得到。
		证明：令 $x'\equiv x\pmod{15}$，取 $x'\in\{0,1,\dots,14\}$。则 $ax'\equiv 1\pmod{15}$.
		于是 $x'$ 也是模 15 的单位，即 $\gcd(x',15)=1$，所以 $x'\in U(15)=G_2$
（3）$G_{3}=\left \langle \, 2 \, \right \rangle$，阶 6 循环群

- 封闭性：$\forall a, b\in G_{2}, \gcd(a,15)=1, \gcd(b, 15)=1, \gcd(ab, 15)=\gcd(ab \mod 15, 15)=1$
	- $\gcd(m,n)=\gcd(qn+r,n)=\gcd(r,n)$ $d|m \land d|n \iff d|n \land d|(m-qn)$
- 结合性：同（2）
- 幺元：
	- $1·a\equiv a·1 \mod 21$
- 逆元：
	- 观察得到 $\forall a \in G_{1}, gcd(a, 21)=1$
	- Bézout 定理：$ax+by=1\iff gcd(a,b)=1$
		$\forall a\in G_{2}, \gcd(a,15)=1$ $\implies$ $\exists y\in \mathbb{Z}, ax-15y=1$ $\implies$ $ax\equiv 1 \mod 15$
	- 同（2），是否需要给出 $x\in G_{2}$ 的证明？尽管此题注意到 $2^6=64\equiv 1 \mod 21$ 后易得。
- 循环群 $G = \left \langle \, g \, \right \rangle = \left\{ g^k | \; k \in \mathbb{Z} \right\}$
	- $1\equiv 2^6 \mod 21$
	- $2\equiv 2^7 \mod 21$
	- $4\equiv 2^8 \mod 21$
	- $8\equiv 2^9 \mod 21$
	- $16 \equiv 2^{10} \mod 21$
	- $32 \equiv 2^{11} \mod 21$
	- $G = \left \langle 2\right \rangle$
事实上可以证：$G_{3}$ $\cong$ 整数同余加法群 $\mathbb{Z}/6\mathbb{Z}$

##### 2. 求子群

>[!faq] 求子群
>求 1. 中的所有子群。

（群论的Lagrange定理）子群的阶整除原群的阶

$G_{1}$：$3\mathbb{Z}$ 的子群为 $3m\mathbb{Z}$ 形式，无穷多：$\{0\}, 3\mathbb{Z}（自身也别忘）, 6\mathbb{Z}, 9\mathbb{Z}\dots$

$G_{2}$：
子群的阶必须整除 8：可能是 $1,2,4,8$。

先算几个元素的阶（模 15）：

- $1$ 阶 1
- $14\equiv-1$ 阶 2
- $4^2\equiv 1$，所以 $\langle 4\rangle=\{1,4\}$（阶 2）
- $11^2\equiv 1$，所以 $\langle 11\rangle=\{1,11\}$（阶 2）
- $2^2=4,\ 2^4\equiv1$，所以 $\langle 2\rangle=\{1,2,4,8\}$（阶 4）
- $7^2\equiv4,\ 7^4\equiv1$，所以 $\langle7\rangle=\{1,7,4,13\}$（阶 4）
- $8$ 也生成同一个：$\langle8\rangle=\{1,8,4,2\}=\{1,2,4,8\}$
- $13$ 也生成 $\{1,7,4,13\}$

所以**全部子群**是：

- 阶 1：{1}
- 阶 2：{1,14},\ {1,4},\ {1,11}
- 阶 4：{1,2,4,8},\ {1,4,7,13}
- 阶 8：整个群 $G_2$

$G_{3}$：

循环群阶 6 的子群与 6 的因子一一对应：阶 (1,2,3,6)。

- 阶 1：{1}
- 阶 2：由 $2^3\equiv 8$ 生成 $\langle 8\rangle=\{1,8\}$ （**之前漏了**）
- 阶 3：由 $2^2\equiv 4$（或 $2^4\equiv 16$）生成  $\langle 4\rangle=\{1,4,16\}$
- 阶 6：整个 $G_3$

##### 4. 验证是群


>[!faq] 验证函数复合成群
>$f_{1}(x)=x$
>$f_{2}(x)=\frac{1}{x}$
>$f_{3}(x)=1-x$
>$f_{4}(x)=\frac{1}{1-x}$
>$f_{5}(x)=\frac{x-1}{x}$
>$f_{6}(x)=\frac{x}{x-1}$


* $f_1(x)=x$: $0\mapsto 0,\ 1\mapsto 1,\ \infty\mapsto \infty$
* $f_2(x)=\frac{1}{x}$: $0\mapsto \infty,\ 1\mapsto 1,\ \infty\mapsto 0$
* $f_3(x)=1-x$: $0\mapsto 1,\ 1\mapsto 0,\ \infty\mapsto \infty$
* $f_4(x)=\frac{1}{1-x}$: $0\mapsto 1,\ 1\mapsto \infty,\ \infty\mapsto 0$
* $f_5(x)=\frac{x-1}{x}$: $0\mapsto \infty,\ 1\mapsto 0,\ \infty\mapsto 1$
* $f_6(x)=\frac{x}{x-1}$: $0\mapsto 0,\ 1\mapsto \infty,\ \infty\mapsto 1$

因此它们都在**置换**三点集 $\{0,1,\infty\}$。把每个 (f) 送到它诱导的置换
$$
\varphi(f)\in S_{{0,1,\infty}}\cong S_3.
$$
而 **Möbius 变换由三点像唯一决定**：如果两个分式线性变换在 $0,1,\infty$ 上取值相同，它们就完全相同。所以 $\varphi$ 是**单射**。

又因为我们这里一共有 6 个互不相同的变换，而 $S_3$ 也恰好有 6 个元素，所以 $\varphi$ 还是**满射**，从而：

* 这 6 个函数在复合下**封闭**；
* 它们构成一个 6 阶群，且与 $S_3$**同构**。

* **结合律**：函数复合本来就满足结合律，$(f\circ g)\circ h=f\circ(g\circ h)$。
* **单位元**：(f_1(x)=x)。
* **逆元**：由置换观点（或直接算）可得
$$
  f_1^{-1}=f_1,\quad
  f_2^{-1}=f_2,\quad
  f_3^{-1}=f_3,\quad
  f_4^{-1}=f_5,\quad
  f_5^{-1}=f_4,\quad
  f_6^{-1}=f_6.
$$
  （顺便：$f_2,f_3,f_6$ 都是 2 阶；$f_4,f_5$ 是 3 阶。）

取
$$
s=f_3(x)=1-x,\qquad t=f_2(x)=\frac1x,
$$
则
$$
s^2=t^2=e,\qquad (t\circ s)^3=e,
$$
其中 $t\circ s=f_4$。这正是 (S_3) 的经典表示。

##### 7. 正五角星顶点着色

>[!faq] 正五角星顶点着色
>五个顶点各m种颜色，可以有多少种方案

正五角星的 5 个顶点的对称群就是五边形的二面体群

绕中心旋转72度，过5个轴，共10个置换。

- (1)(2)(3)(4)(5)
- (1 2 3 4 5)
- (1 3 5 2 4)
- (1 4 2 5 3)
- (5 4 3 2 1)

- (1)(2 5)(3 4)
- ... 同理，总共有5个，对应不相交轮换数为2。

$$
L=\frac{1}{10}(4·m^1+5·m^3+m^5)
$$
##### 8. 正方形四格着色

>[!faq] 正方形四格着色
>正方形均分4格，用两种颜色对4个格子着色，其中认为两种颜色互换后使之一致的方案属同一类。

在例7.10.2的基础上（不能直接除以2！！！）

4种

把黑白互换视作同类后，4 类可以选代表图案为：

1. **全同色**（全黑 $\sim$ 全白）
2. **一个异色 + 三个同色**（“单点”型；1 黑 $\sim$ 3 黑）
3. **两黑两白且相邻成一条“多米诺”**（2 黑相邻；换色后仍是这种型）
4. **两黑两白且对角（棋盘格）**（换色后仍是这种型）

正好 4 类。