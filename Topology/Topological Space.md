#### Open/Close Ball

der offene/abgeschlossene Ball
- In $\mathbb{K}=\mathbb{R}$ oder $\mathbb{C}$
	- $\mathbb{K}=\mathbb{R}$
		das offene/abgeschlossene Intervall
	- $\mathbb{K}=\mathbb{C}$
	  die offene/abgeschlossene Kreisscheibe 
		$\mathbb{D}(a, r)$, $\bar{\mathbb{D}}(a, r)$
		Einheitskreisscheibe $\mathbb{D}$, $\bar{\mathbb{D}}$
- In dem metrischen Raum $X:=(X,d)$
	- Der offene Ball $\mathbb{B}(a, r)$ ist offen.
	- Der abgeschlossene Ball $\bar{\mathbb{B}}(x, r)$ ist abgeschlossen.
- In dem normierten Vektorraum $E := (E, \|\cdot\|)$
	$\mathbb{B}(a, r)$, $\bar{\mathbb{B}}(a, r)$
	Einheitsball $\mathbb{B} := \mathbb{B}(0,1)$, $\bar{\mathbb{B}} := \bar{\mathbb{B}}(0,1)$
	$r\mathbb{B} = \mathbb{B}(0,r)$, $r\bar{\mathbb{B}} = \bar{\mathbb{B}}(0,r)$, $a + r\mathbb{B} = \mathbb{B}(a,r)$, $a + r\bar{\mathbb{B}} = \bar{\mathbb{B}}(a,r)$.
- Es bezeichne $\mathbb{B}^m$ den reellen offenen euklidischen Einheitsball, d.h. $\mathbb{B}^m := \mathbb{B}_{\mathbb{R}^m},$
	$\mathbb{B}_{\infty}^{m} = \underbrace{\mathbb{B}_{\infty}^{1} \times \cdots \times \mathbb{B}_{\infty}^{1}}_{m} = (-1, 1)^{m}$
	Für $\mathbb{B}^m$ oder $\mathbb{B}_1^m$ gibt es keine analoge Darstellung.

#### Topological Space

topological space/espace topologique/topologischer Raum
- Für das Mengensystem $\mathfrak{T} := \{ O \subseteq X ; O \text{ ist offen} \}$ gelten folgende Aussagen:
	- (i) $\emptyset, X \in \mathfrak{T}$.
		- $\emptyset$ und $X$ sind abgeschlossen.
	- (ii) Aus $O_\alpha \in \mathfrak{T}$ für $\alpha \in \mathbf{A}$ folgt $\bigcup_\alpha O_\alpha \in \mathfrak{T}$, d.h., beliebige Vereinigungen offener Mengen sind offen.
		- *Beliebige Durchschnitte abgeschlossener Mengen sind abgeschlossen.*
		- Unendliche Vereinigungen abgeschlossener Mengen brauchen nicht abgeschlossen zu sein.
			- Beispielsweise gilt $\bigcup_{n=1}^{\infty} [\mathbb{B}(0, 1/n)]^c = \mathbb{R}^\times$ in $\mathbb{R}$.
	- (iii) Aus $O_0, \dots, O_n \in \mathfrak{T}$ folgt $\bigcap_{k=0}^n O_k \in \mathfrak{T}$, d.h., endliche Durchschnitte offener Mengen sind offen.
		- *Endliche Vereinigungen abgeschlossener Mengen sind abgeschlossen.*
		- Unendliche Durchschnitte offener Mengen brauchen nicht offen zu sein.
			- In $\mathbb{R}$ gilt z.B. $\bigcap_{n=1}^{\infty} \mathbb{B}(0, 1/n) = \{0\}$
- Die Eigenschaften (i)–(iii) verwenden nur die Mengenoperationen $\bigcup$ and $\bigcap$. Somit können wir diese Eigenschaften axiomatisch für beliebige Mengensysteme fordern.
- Genauer sei $M$ eine Menge, und $\mathfrak{T} \subseteq \mathfrak{P}(M)$ sei ein Mengensystem mit den Eigenschaften (i)–(iii).
	- Dann heißt $\mathfrak{T}$ **Topologie** auf $M$,
	- und die Elemente von $\mathfrak{T}$ werden als **offene Mengen** bezügl. $\mathfrak{T}$ bezeichnet.
	- Schließlich heißt das Paar $(M, \mathfrak{T})$ **topologischer Raum**.
- Es sei $\mathfrak{T} \subseteq \mathfrak{P}(X)$ das Mengensystem.
	- Dann ist $\mathfrak{T}$ **die von der Metrik $d$ erzeugte Topologie** auf $X$.
	- Ist $X$ ein normierter Vektorraum und ist die Metrik von der Norm induziert, heißt $\mathfrak{T}$ **Normtopologie**.

#### 聚点、触点

Es seien $A \subset X$ und $x \in X$. Wir nennen $x$ **Berührungspunkt** von $A$, falls jede Umgebung von $x$ in $X$ einen nichtleeren Durchschnitt mit $A$ hat.

Das Element $x \in X$ heißt **Häufungspunkt** von $A$, wenn jede Umgebung von $x$ in $X$ einen von $x$ verschiedenen Punkt von $A$ enthält. Schließlich setzen wir
$$
\overline{A} := \{ x \in X ; x \text{ ist Berührungspunkt von } A \} .
$$

Es ist sorgfältig zu unterscheiden zwischen dem Begriff „Häufungspunkt einer Menge $A$“ und dem Begriff „Häufungspunkt einer Folge $(x_n)$“.
Außerdem muß ein Häufungspunkt von $A$ natürlich nicht in $A$ liegen.

##### Comparison

|      | French               | German          | English            |
| ---- | -------------------- | --------------- | ------------------ |
| 触点   | point adhérent       | Berührpunkte    | adherent point     |
| 极限点  | point limite         | Häufungspunkt   | limit point        |
| 集合聚点 | point d’accumulation | Häufungspunkt   | accumulation point |
| 数列聚点 | valeur d'adhérence   | Häufungspunkt   | cluster point      |
| 数列极限 | limite               | Grenzwert/Limes | limit              |

[Point d'accumulation (mathématiques) — Wikipédia](https://fr.wikipedia.org/wiki/Point_d%27accumulation_\(math%C3%A9matiques\))

Pour un espace non $T_1$, la terminologie est fluctuante : certains auteurs appellent « point limite » ce qui est appelé ici « point d'accumulation » et réservent l'expression « point d'accumulation » pour la propriété en général plus forte signalée ici. C'est cette autre terminologie qui est adoptée dans l'article [Point adhérent](https://fr.wikipedia.org/wiki/Point_adh%C3%A9rent "Point adhérent").

[Point adhérent — Wikipédia](https://fr.wikipedia.org/wiki/Point_adh%C3%A9rent)

- Pour la première école, représentée par [Choquet](https://fr.wikipedia.org/wiki/Gustave_Choquet "Gustave Choquet"), [Schwartz](https://fr.wikipedia.org/wiki/Laurent_Schwartz_\(math%C3%A9maticien\) "Laurent Schwartz (mathématicien)") et Willard et adoptée dans l'article détaillé, les expressions « point d'accumulation » et « point limite » sont synonymes. Si _A_ est une partie d'un espace topologique, un point d'accumulation ou point limite de _A_ est un point _x_ dont tout [voisinage](https://fr.wikipedia.org/wiki/Voisinage_\(math%C3%A9matiques\) "Voisinage (mathématiques)") contient un point de _A_ distinct de _x_. Autrement dit, un point _x_ est un point d'accumulation de _A_ si et seulement s'il est adhérent à _A \ {x}_.
- Pour la deuxième école, représentée par [Steen](https://fr.wikipedia.org/wiki/Lynn_Arthur_Steen "Lynn Arthur Steen") et [Seebach](https://fr.wikipedia.org/wiki/J._Arthur_Seebach,_Jr. "J. Arthur Seebach, Jr.") et adoptée dans cet article, « point d'accumulation » désigne une propriété plus forte que « point limite ». On dit qu'un point _x_ de _E_ est un point d'accumulation de _A_ si tout [voisinage](https://fr.wikipedia.org/wiki/Voisinage_\(math%C3%A9matiques\) "Voisinage (mathématiques)") de _x_ contient une _infinité_ de points de _A_. Tout point d'accumulation de _A_ dans _E_ est donc un point limite de _A_, mais la réciproque n'est vraie que si _E_ est un [espace T1](https://fr.wikipedia.org/wiki/Espace_T1 "Espace T1") ou _a fortiori_ s'il est [séparé](https://fr.wikipedia.org/wiki/Espace_s%C3%A9par%C3%A9 "Espace séparé") (espace T2), en particulier s'il est [métrisable](https://fr.wikipedia.org/wiki/Espace_m%C3%A9trisable "Espace métrisable"). Mais dans un espace topologique quelconque, _A_ peut avoir des points limites qui ne sont pas des points d'accumulation. Par exemple, si _E_ est un [ensemble fini](https://fr.wikipedia.org/wiki/Ensemble_fini "Ensemble fini") non vide muni de la [topologie grossière](https://fr.wikipedia.org/wiki/Topologie_grossi%C3%A8re "Topologie grossière") et si _A_ est une partie stricte non vide de _E_, tout point de _E \ A_ est point limite de _A_ mais _A_ ne possède pas de point d'accumulation dans _E_.

[Berührungspunkt – Wikipedia](https://de.wikipedia.org/wiki/Ber%C3%BChrungspunkt)

**Berührungspunkt** oder **Berührpunkte** 

[Häufungspunkt – Wikipedia](https://de.wikipedia.org/wiki/H%C3%A4ufungspunkt)

(auch **Adhärenzpunkt**)

Zuweilen werden statt Häufungspunkt auch die Wörter _Häufungswert_, $β$-_Punkt_ oder _Grenzpunkt_ benutzt.



#### Openness

$X:=(X,d)$ ist ein metrischer Raum, $a \in U\subseteq A\subseteq X$

- interior point/point intérieur/innerer Punkt
	$a$ 是 $A$ 的内点： $\exists$ Umgebung $U$ von $a$.
	- 有邻域包含之

> [!note] 开集
>
>- 各点均为内点。
>- 

- Die Begriffe „innerer Punkt“ und „offene Menge“ hängen vom umgebenden metrischen Raum $X$ ab.

- Jeder Punkt in einem metrischen Raum eine *offene* Umgebung besitzt.
	Das hat **nichts Wesentliches mit Beschränktheit oder Durchmesser** zu tun.
	Beschränktheit sagt nur, dass alle Punkte einer Menge höchstens einen festen Abstand voneinander haben.
	-  Eine beschränkte Menge muss nicht offen sein, z.B. $[0,1]\subseteq \mathbb{R}$
	- Umgekehrt ist eine offene Umgebung nicht unbedingt beschränkt, denn $\mathbb{R}$ selbst ist offen in $\mathbb{R}$, aber unbeschränkt.

- [general topology - Are Singleton sets in $\mathbb{R}$ both closed and open? - Mathematics Stack Exchange](https://math.stackexchange.com/questions/17649/are-singleton-sets-in-mathbbr-both-closed-and-open)

- $\mathcal{T}$ 为 $X$ 中开集的集族
	(1) $∅, X$ 开
	(2) 开集的任意并开
		（有类直和？）
	(3) 开集的有限（？）交开
		反例：$⋂(-1/n , 1/n)$
	- $M$ be a set, $\mathcal{T}\subseteq P(M)$ satisfying (1)-(3)
		- $\mathcal{T}$: $M$ 上拓扑，其中元素为开集。
			topology on $X$ induced from the metric $d$
			若 $X$ 赋范，$\mathcal{T}$ 范数拓扑
		- $(M, \mathcal{T})$: 拓扑空间

#### Closedness

Es sei $X$ ein metrischer Raum.
Eine Teilmenge $Y$ von $X$ heißt **abgeschlossen**, wenn für jede Folge $(y_n)$ in $Y$, die in $X$ konvergiert, gilt: $\lim y_n \in Y$.

 $A \subseteq X$
 - A 闭，若其补集开
	(1) $∅, X$ 闭
	(2) 闭集的任意交闭
	(3) 闭集的有限并闭
		反例：$⋃ (-1/n, 1/n)^c$ =$(-\infty, -1]⋃[1,\infty) ⋃ ... = \mathbb{R}\backslash\{0\}$
		$\{0\}$ 是单点集，故以上应是开集

c.f. cluster point of sequence: 任意邻域，无限多项。

 $A \subseteq X, x\in X$
- accumulation point of $A$: $x$ 的任意邻域与 $A$ 有交。
- limit point of $A$: $x$ 的任意邻域还包含 $A$ 中别的点。
	limit point $\subseteq$ accumulation point
- $\bar{A} =\{\text{accumulation points of }A\} = \text{cl}(A)$
	- $A \subseteq \bar{A}$
	- $A = \bar{A} \Longleftrightarrow A\text{ is closed}$

- limit point $\Longleftrightarrow$ $\exists\{x_n\} \in A\backslash\{x\}$ 收敛于 $x$
- accumulation point $\Longleftrightarrow$ $\exists\{x_n\} \in A$ 收敛于 $x$

- $A$ 是闭集
- $A$ 包含所有 limit points
- 所有在 $X$ 上收敛的 $\{x_n\}\in A^\mathbb{N}$，极限 $\in A$

闭包：最小闭集/包含之的闭集之交
- $\bar{A} =\{\text{accumulation points of }A\} = \text{cl}(A)$

内部：最大开集/含于其的开集之并
- $\overset{\circ}{A} =\{\text{interior points of }A\} = \text{int}(A)$

边界：$∂A := \bar{A}\backslash\overset{\circ}{A} = \bar{A}\cap(\overset{\circ}{A})^c$
- 边界是闭的
- $x$ 在边界上 $\Longleftrightarrow$ 任意邻域均与 $A$ 和 $\overset{\circ}{A}$ 有交

#### The Hausdorff Condition

$x\neq y\in X$，分别存在邻域使得二者无交。

一点的全部邻域，其交为 singleton

- 度量空间上的单点集为闭集。

- 度量空间均为 Hausdorff 空间