
# 例：反射的有向グラフ

ここでは反射的有向グラフを例に、収束構造とそのフィルター開位相を考察する。

**有向グラフ**（directed graph）とは、頂点の集合$V$と、向き付けられた辺の集合$E\subset V\times V$の組$(V, E)$である。（$(v, u)\in E$は始点$v$から終点$u$への有向辺とする。）有向グラフが**反射的**（reflexible）とは、任意の頂点$v\in V$について$(v, v)\in E$が成り立つことをいう。

さて、反射的有向グラフ$(V, E)$において、頂点$v\in V$を始点とする有向辺の終点全体

$$
\overrightarrow{v}:=\lbrace u\in V : (v, u)\in E \rbrace
$$

を考える。このとき収束構造$\mathscr{F}\rightarrow v$を$\overrightarrow{v}\in\mathscr{F}$で定めることができる。実際$(v, v)\in E$より$v\in\overrightarrow{v}$だから$\overrightarrow{v}\in\langle v \rangle$故に$\langle v \rangle\rightarrow v$である。$\mathscr{F}\rightarrow v, \mathscr{F}\subset\mathscr{G}$とすれば$\overrightarrow{v}\in\mathscr{F}\subset\mathscr{G}$より$\mathscr{G}\rightarrow v$である。$\overrightarrow{v}\in\mathscr{F}, \mathscr{G}$なら$\overrightarrow{v}\in\mathscr{F}\cap\mathscr{G}$も成り立つ。このようにして反射的有向グラフは収束空間となる。

- 単項フィルター$\langle \overrightarrow{v} \rangle$は$v$に収束する。つまり$\langle \overrightarrow{v} \rangle\rightarrow v$が成り立つ。

__定理__ $(V_{1}, E_{1}), (V_{2}, E_{2})$を反射的有向グラフとする。$f\colon V_{1}\rightarrow V_{2}$を写像とする。$v\in V_{1}$とする。TFAE

1. $f$は$v$で連続である。
1. $f(\overrightarrow{v})\subset\overrightarrow{f(v)}$が成り立つ。

（証明）$f$が$v$で連続とすると、$\langle \overrightarrow{v} \rangle\rightarrow v$より$f_{\ast}\langle \overrightarrow{v} \rangle\rightarrow f(v)$である。つまり$\overrightarrow{f(v)}\in f_{\ast}\langle \overrightarrow{v} \rangle=\langle f(\overrightarrow{v}) \rangle$だから、$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$となる。

逆に$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$なら、$\mathscr{F}\rightarrow v$について$\overrightarrow{v}\in\mathscr{F}$より$f(\overrightarrow{v})\in f\mathscr{F}\subset f_{\ast}\mathscr{F}$である。従ってフィルターの性質より$\overrightarrow{f(v)}\in f_{\ast}\mathscr{F}$を得る。つまり$f$は$v$で連続となる。$\square$

条件$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$は$(v, u)\in E_{1}$なら$(f(v), f(u))\in E_{2}$を意味する。従って$f$が連続であることは、$f$がグラフ準同型であることに他ならない。

- 半順序集合は反射的有向グラフとみなせる。このとき連続射は順序を保つ写像に他ならない。

次にこの収束構造に対するフィルター開位相を考察する。

まず隣接フィルターを考える。フィルター$\mathscr{F}$について$\mathscr{F}\rightarrow v$の定義は$\overrightarrow{v}\in\mathscr{F}$である。このとき$F\supset\overrightarrow{v}$なら$F\in\mathscr{F}$より$\langle \overrightarrow{v} \rangle\subset\mathscr{F}$が成り立つ。特に$\langle \overrightarrow{v} \rangle\rightarrow v$だから、結局$\mathscr{N}_{v}=\langle \overrightarrow{v} \rangle$が分かる。

$U$がopenであるとは任意の$v\in U$について$U\in\langle \overrightarrow v \rangle$つまり$\overrightarrow{v}\subset U$が成り立つことだから、これが全ての$v\in U$で成り立つということは、矢印の先を辿れるところまで$U$が全て含むことを意味する。

__例__ 連続射でないが連続写像の例を与える。$a, b, c$を頂点として、$a\rightarrow b\rightarrow c\rightarrow a$というサイクルで定まるグラフの収束空間を$Y$とする。それぞれ双方向としたものを$X$とする。$f\colon X\rightarrow Y$を頂点上の恒等写像とすると、グラフ準同型でないので連続射でない。しかしopenな部分集合はどちらも$\lbrace a, b, c \rbrace, \emptyset$のみなので、openの逆像はopenであり連続写像である。

> $X$と$Y$は同じ位相（密着位相）を定めるが、収束構造（この場合はグラフ構造）としては異なる。