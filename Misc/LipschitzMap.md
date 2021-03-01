
# 距離空間とリプシッツ写像



__定義__ $X$を集合とする。実函数$\rho\colon X\times X\rightarrow \mathbb{R}$は以下を満たすとする。

- $a, b\in X$について$\rho(a, b)\ge 0$および$\rho(a, a)=0$が成り立つ。（正値性）
- $a, b\in X$について$\rho(a, b)=0$なら$a=b$が成り立つ。（非退化性）
- $a, b\in X$について$\rho(a, b)=\rho(b, a)$が成り立つ。（対称性）
- $a, b, c\in X$について$\rho(a, c)\le \rho(a, b)+\rho(b, c)$が成り立つ。（三角不等式）

このとき$\rho$を$X$上の **距離** （metric）と呼び、組$(X, \rho)$を **距離空間** （metric space）と呼ぶ。

> 距離空間の一般化については名称が統一されていない。ここでは距離空間の条件から非退化性を除いたものを半距離（semimetric）、対称性を除いたものを準距離（quasimetric）、三角不等式を除いたものを前距離（premetric）、対称性と三角不等式を除いたものを擬距離（pseudometric）と呼ぶ。更に三角不等式に類する不等式を課す場合もある。

- 距離が明らかなときは$\rho(a, b)$の代わりに$\vert a-b \vert$を用いる。この記法はあくまで形式的なもので、$X$上の「引き算」ではない。

__定義__ $X, Y$を距離空間とする。$\alpha\ge 0$に対して、函数$f\colon X\rightarrow Y$であって任意の$a, b\in X$について

$$
\vert f(a)-f(b) \vert\le \alpha\cdot\vert a-b \vert
$$

を満たすもの全体を$\mathrm{Lip}_{\alpha}(X, Y)$と表す。写像$f\colon X\rightarrow Y$が

$$
\mathrm{Lip}(X, Y):=\bigcup_{\alpha\ge 0}\mathrm{Lip}_{\alpha}(X, Y)
$$

に属するとき、$f$は **リプシッツ** （Lipschitz）であるという。

__命題__ リプシッツ写像$f\colon X\rightarrow Y$は連続である。

（証明）$f\in\mathrm{Lip}_{\alpha}(X, Y)$とする。$\varepsilon\gt 0$に対し、$\delta:=\varepsilon/\alpha$と置く。このとき$\vert a-b \vert\lt\delta$なら

$$
\vert f(a)-f(b) \vert\le\alpha\cdot\vert a-b \vert\lt\varepsilon
$$

より$f$は連続である。$\square$

一般に写像$f\colon X\rightarrow Y$に対して$f$の **リプシッツ数** （Lipschitz number）を

$$
Lf:=\mathrm{sup}\left\lbrace \frac{\vert f(a)-f(b) \vert}{\vert a-b \vert} : a, b\in X, a\neq b \right\rbrace\cup\lbrace 0 \rbrace
$$

と定める。$f$がリプシッツであることと$Lf\lt\infty$は同値となる。

> 非退化性よりwell-definedとなる。$a\neq b$の条件を外して$0/0:=0$としてもよいが、半距離空間においては$\vert a-b \vert=0$であっても$f(a)=f(b)$が言えず$x/0$の扱いに困るので、$f$に条件を課すなどの工夫が必要かもしれない。

__例__ $(X, \rho)$を距離空間とする。$p\in X$について$\rho_{p}\colon X\rightarrow\mathbb{R}$を$\rho_{p}(a):=\rho(a, p)$と定める。三角不等式より

$$
\vert \rho_{p}(a)-\rho_{p}(b) \vert=\vert \rho(a, p)-\rho(b, p) \vert\le\rho(a, b)
$$

が成り立つ。従って$\rho_{p}\in\mathrm{Lip}_{1}(X, \mathbb{R})$である。

- 恒等写像$\mathrm{id}_{X}\colon X\rightarrow X$はリプシッツである。リプシッツ数は$1$である。
- リプシッツ写像$f\colon X\rightarrow Y, g\colon Y\rightarrow X$の合成$g\circ f\colon X\rightarrow Z$もまたリプシッツであり$L(g\circ f)\le Lf\cdot Lg$が成り立つ。

> 対象を距離空間、射をリプシッツ写像として圏$\mathrm{Lip}$が定まる。対象を完備距離空間に限定すれば充満部分圏$\mathrm{compLip}$が定まる。更に距離空間の完備化は函手$\mathrm{Lip}\rightarrow\mathrm{compLip}$を定めるが、次の命題よりこれらが随伴であることが分かる。

__命題__ $X, Y$を完備距離空間、$D\subset X$は稠密とする。リプシッツ写像$f\colon D\rightarrow Y$に対し、唯一つのリプシッツ写像$h\colon X\rightarrow Y$が存在して、$h\vert_{D}=f$かつ$Lh=Lf$を満たす。

（証明）一意性は$D\subset X$が稠密であることと、リプシッツ写像が連続であることから従う。

__命題__ （isomorphism-closed）$X$を完備距離空間、$Y$を距離空間とする。$f\colon X\rightarrow Y$は全射かつ双リプシッツ（特に$f$が同型）なら$Y$は完備である。