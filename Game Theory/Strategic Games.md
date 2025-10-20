#### Strategic game

$\succeq$ $\preceq$

- players (finite set $N$)
- actions (non empty set $A_{i},i\in N$)
- preference relation $\succeq_{i}$ on $A=\prod_{j\in N} A_{j}$
	
	- sometimes most naturally defined not over action profiles but over their consequence
		- a set $C$ of consequences
		- a function $g: A → C$
		- a profile $(\succeq_{i}^*)$ of preference relations over $C$, $a \succeq_{i}^* b$ if and only if $g(a) \succeq_{i}^* g(b)$
	- sometimes the consequence of an action profile is affected by an exogenous random variable
		- a set $C$ of consequences
		- a probability space $\Omega$
		- a function $g:A\times \Omega → C$, $g(a, \omega)$ consequence, $\omega\in \Omega$ the realization of the random variable
		- a profile $(\succeq_{i}^*)$ of preference relations over $C$, $a \succeq_{i}^* b$ if and only if $g(a) \succeq_{i}^* g(b)$

[game theory - Nash Equilibrium and Pareto efficiency - Economics Stack Exchange](https://economics.stackexchange.com/questions/14548/nash-equilibrium-and-pareto-efficiency)

[game theory - Definition of Pareto efficiency and prisoner's dilemma - Economics Stack Exchange](https://economics.stackexchange.com/questions/27145/definition-of-pareto-efficiency-and-prisoners-dilemma)

[game theory - Difference between Nash equilibrium and Pareto Efficiency - Economics Stack Exchange](https://economics.stackexchange.com/questions/30303/difference-between-nash-equilibrium-and-pareto-efficiency)
