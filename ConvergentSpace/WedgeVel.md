
# Wedge積とVel積

__定義__ $\mathscr{A}, \mathscr{B}\subset 2^{X}$をprefilterとする。関係$\mathscr{A}\dashv\mathscr{B}$を以下で定める。

- 任意の$A\in\mathscr{A}$について、ある$B\in\mathscr{B}$が存在して$B\subset A$が成り立つ。

このとき$\mathscr{B}$は$\mathscr{A}$より **細かい** （finer）、あるいは$\mathscr{A}$は$\mathscr{B}$より **粗い** （coarser）という。

> この定義は次の意味で整合的である。

__命題__ $\mathscr{A}, \mathscr{B}\subset 2^{X}$をprefilterとする。TFAE

1. $\mathscr{A}\dashv\mathscr{B}$である。
1. $\langle \mathscr{A} \rangle\subset\langle \mathscr{B} \rangle$である。

関係$\dashv$は反射的（$\mathscr{A}\dashv\mathscr{A}$）かつ推移的（$\mathscr{A}\dashv\mathscr{B}, \mathscr{B}\dashv\mathscr{C}$なら$\mathscr{A}\dashv\mathscr{C}$）である。そこで関係$\mathscr{A}\sim\mathscr{B}$を$\mathscr{A}\dashv\mathscr{B}$かつ$\mathscr{B}\dashv\mathscr{A}$（つまり生成するフィルターが等しい）で定めると$\sim$は同値関係となる。

__定義__ $\mathscr{G}, \mathscr{G}\subset 2^{X}$をフィルターとする。集合としての共通部分$\mathscr{G}\cap\mathscr{F}$もまたフィルターである。一般に$\mathscr{F}_{\lambda}, \lambda\in\Lambda$をフィルターの族として、$\bigcap_{\lambda\in\Lambda}\mathscr{F}_{\lambda}$もまたフィルターである。このとき

$$
\begin{aligned}
\mathscr{F}\wedge\mathscr{G} &:=\mathscr{F}\cap\mathscr{G}, & \bigwedge_{\lambda\in\Lambda}\mathscr{F}_{\lambda} &:=\bigcap_{\lambda\in\Lambda}\mathscr{F}_{\lambda}
\end{aligned}
$$

をフィルターの **wedge積** という。

> フィルターのwedge積は、与えられたフィルターより粗いフィルターとなる。

__命題__ $\mathscr{A}, \mathscr{B}\subset 2^{X}$をprefilterとする。以下が成り立つ。

- $\mathscr{A}\vee\mathscr{B}:=\lbrace A\cap B : A\in\mathscr{A}, B\in\mathscr{B} \rbrace$はprefilterである。
- $\mathscr{A}\vee\mathscr{B}$は$\mathscr{A}, \mathscr{B}$より細かい。つまり$\mathscr{A}, \mathscr{B}\dashv\mathscr{A}\vee\mathscr{B}$が成り立つ。
- $\mathscr{A}\vee\mathscr{B}$は$\dashv$に関する上限を与える。つまり$\mathscr{A}, \mathscr{B}\dashv\mathscr{C}$なら$\mathscr{A}\vee\mathscr{B}\dashv\mathscr{C}$が成り立つ。

（証明）$A_{1}, A_{2}\in\mathscr{A}, B_{1}, B_{2}\in\mathscr{B}$として$V=A_{1}\cap B_{1}, W=A_{2}\cap B_{2}\in\mathscr{A}\vee\mathscr{B}$を取る。$\mathscr{A}$はprefilterだから、ある$A\in\mathscr{A}$が存在して$A\subset A_{1}\cap A_{2}$である。同様に$B\in\mathscr{B}$が存在して$B\subset B_{1}\cap B_{2}$である。$A\cap B\in\mathscr{A}\vee\mathscr{B}$であり、

$$
A\cap B\subset A_{1}\cap A_{2}\cap B_{1}\cap B_{2}\subset V\cap W
$$

より$\mathscr{A}\vee\mathscr{B}$はprefilterであることが分かる。

$\mathscr{A}\dashv\mathscr{A}\vee\mathscr{B}$であることは明らか。実際$A\in\mathscr{A}$に対して、任意の$B\in\mathscr{B}$について$A\cap B\subset A$である。

$A\in\mathscr{A}, B\in\mathscr{B}$として$V=A\cap B\in\mathscr{A}\vee\mathscr{B}$を取る。$\mathscr{A}, \mathscr{B}\dashv\mathscr{C}$より、$C_{1}, C_{2}\in\mathscr{C}$を$C_{1}\subset A, C_{2}\subset B$となるように取れる。$C_{1}\cap C_{2}\subset A\cap B=V$だが、$\mathscr{C}$はprefilterなので$C\in\mathscr{C}$が存在して$C\subset C_{1}\cap C_{2}\subset V$が成り立つ。故に$\mathscr{A}\vee\mathscr{B}\dashv\mathscr{C}$を得る。$\square$

__定義__ 上記の$\mathscr{A}\vee\mathscr{B}$をprefilterの **vel積**という。

> prefilterのvel積は、与えられたprefilterより細かいprefilterとなる。

__定義__ $\mathscr{S}, \mathscr{T}\subset 2^{X}$を集合族とする。以下が成り立つとき$\mathscr{S}$と$\mathscr{T}$は **mesh** という。

- 任意の$S\in\mathscr{S}$と任意の$T\in\mathscr{T}$について$S\cap T\neq\emptyset$が成り立つ。

特にprefilter $\mathscr{A}, \mathscr{B}$がmeshのとき$\mathscr{A}\vee\mathscr{B}$は真prefilterである。


__命題__ $\mathscr{F}, \mathscr{G}\subset 2^{X}$をフィルターとする。このとき$\mathscr{F}\vee\mathscr{G}$はフィルターである。

（証明）$V=F\cap G\in\mathscr{F}\vee\mathscr{G}$を取る。$V\subset W$とすると$F\subset W\cup F\in\mathscr{F}, G\subset W\cup G\in\mathscr{G}$である。故に

$$
W=W\cup V=( W\cup F )\cap( W\cup G )\in\mathscr{F}\vee\mathscr{G}
$$

を得る。$i=1, 2$に対して$V_{i}=F_{i}\cap G_{i}\in\mathscr{F}\vee\mathscr{G}$を取る。$F_{1}\cap F_{2}\in\mathscr{F}, G_{1}\cap G_{2}\in\mathscr{G}$より$V_{1}\cap V_{2}=( F_{1}\cap F_{2} )\cap( G_{1}\cap G_{2} )\in\mathscr{F}\vee\mathscr{G}$を得る。$\square$

特に$\mathscr{F}, \mathscr{G}$がmeshのとき$\mathscr{F}\vee\mathscr{G}$は真フィルターである。

__命題__ $\mathscr{A}, \mathscr{B}\subset 2^{X}$をprefilterとする。このとき

$$
\langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle=\langle \mathscr{A}\vee\mathscr{B} \rangle
$$

が成り立つ。

（証明）$\mathscr{A}, \mathscr{B}\dashv\mathscr{A}\vee\mathscr{B}$より$\langle \mathscr{A} \rangle, \langle \mathscr{B} \rangle\subset\langle \mathscr{A}\vee\mathscr{B} \rangle$である。prefilterとして$\langle \mathscr{A} \rangle, \langle \mathscr{B} \rangle\dashv\langle \mathscr{A}\vee\mathscr{B} \rangle$だから$\langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle\dashv\langle \mathscr{A}\vee\mathscr{B} \rangle$であり、従って$\langle \mathscr{A} \rangle\vee\langle \mathscr{B} \rangle\subset\langle \mathscr{A}\vee\mathscr{B} \rangle$を得る。

一方で$\mathscr{A}\subset\langle \mathscr{A} \rangle, \mathscr{B}\subset\langle \mathscr{B} \rangle$より$\mathscr{A}\vee\mathscr{B}\subset\langle \mathscr{A} \rangle\vee\langle\ \mathscr{B} \rangle$であり、この右辺はフィルターであることから、生成の最小性より従う。$\square$

> このようにvel積は生成と可換になる。$\mathscr{A}, \mathscr{B}$がmeshであれば$\langle \mathscr{A} \rangle, \langle \mathscr{B} \rangle$もmeshとなり、上記は真フィルターとなる。