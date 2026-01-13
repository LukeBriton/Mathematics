 - 二项式系数
	归纳 $\implies$ $(a+b)^{n}=\sum_{k=0}^{n}\binom{n}{k}a^{k}b^{n-k}$

- 多项式系数
	- $α=(α_{1},\ldots,α_{m})\in\mathbb{N}^{m}$ multi-index (of order m)
	- $|α|:=\sum α_{j}$
	- $α!=\prod (α_{j})!$
	- $α\leq\beta:\iff(α_{j}\leq\beta_{j},\ 1\leq j\leq m)$
	- $a^{α}:=\prod_{j=1}^{m}(a_{j})^{α_{j}}$
		$a=(a_{1},\ldots,a_{m})\in R^{m}$

$$
\binom{k}{α}:=\frac{k!}{α!} \text{（我的用法，当且仅当}|α|=k\text{）}
$$

This is the coefficient of $x^α$ in $(x_1+\cdots+x_m)^k$.

$$
\binom{k}{α}:=\frac{k!}{α!(k-|α|)!}
$$
This is the coefficient of $x^α$ in $(1+x_1+\cdots+x_m)^k$.

if $|\alpha|=k$, $(k-|\alpha|)!=0!=1$

归纳 $\implies$ for all $m \ge 2$
$$\Bigl{(}\sum_{j=1}^{m}a_{j}\Bigr{)}^{k}=\sum_{|α|=k}\frac{k!}{α!}a^{ α}\ ,\qquad a=(a_{1},\ldots,a_{m})\in R^{m}\ ,\quad k\in\mathbb{N}$$

