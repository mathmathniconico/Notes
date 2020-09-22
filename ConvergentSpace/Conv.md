
## 収束空間と連続射

__定義__ $X$を集合とする。各点$x\in X$について$\lambda(x)$をフィルターの族とする。$\lambda\colon x\mapsto\lambda(x)$は以下を満たすとする。

- $\langle x \rangle\in\lambda(x)$である。
- $\mathscr{F}\in\lambda(x)$とする。フィルター$\mathscr{G}\subset 2^{X}$について$\mathscr{F}\subset\mathscr{G}$なら$\mathscr{G}\in\lambda(x)$である。
- $\mathscr{F}, \mathscr{G}\in\lambda(x)$なら$\mathscr{F}\cap\mathscr{G}\in\lambda(x)$である。

このとき$\lambda$を**収束構造**（convergent structure）と呼び、組$(X, \lambda)$を **収束空間** （convergent space）と呼ぶ。$\mathscr{F}\in\lambda(x)$のときフィルター$\mathscr{F}$は$x$に収束するといい、$x$は$\mathscr{F}$の収束先や極限点などという。

フィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\in\lambda(x)$であることを$\mathscr{F}\rightarrow x$と書けば$\lambda$を明示せずに収束空間を定義できる。これはフィルター全体$\Phi(X)$について$\Phi(X)\times X$の部分集合としての「関係」である。

__定義__ $X, Y$を収束空間、$f\colon X\rightarrow Y$を写像とする。任意のフィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\rightarrow x$なら$f_{\ast}\mathscr{F}\rightarrow f(x)$であるとき、$f$は$x$で **連続** （continuous）であるという。任意の$x\in X$で$f$が連続のとき、$f$を **連続射** と呼ぶ。

- 終フィルターの推移性より、連続射の合成もまた連続射である。

収束空間と連続射は圏を為す。これを$\mathbf{Conv}$と書く。

> 始対象は$(X=\emptyset, \lambda=\emptyset)$、終対象は$(Y=\lbrace \ast \rbrace, \lambda(\ast)=\lbrace\emptyset, \lbrace \ast \rbrace \rbrace=2^{Y})$である。


### 収束構造の例（反射的有向グラフ）

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

> 条件$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$は$(v, u)\in E_{1}$なら$(f(v), f(u))\in E_{2}$を意味する。従って$f$が連続であることは、$f$がグラフ準同型であることに他ならない。

半順序集合は反射的有向グラフとみなせる。このとき連続射は順序を保つ写像に他ならない。


### 収束空間の積

__命題__ $X_{i}$を収束空間とする。$p_{i}\colon X=\prod_{j\in I}X_{j}\rightarrow X_{i}$を射影とする。$X$において関係$\mathscr{F}\rightarrow x$を以下で定める。

- 任意の$i\in I$について$p_{i}\mathscr{F}\rightarrow p_{i}(x)$が成り立つ。

このとき$\mathscr{F}\rightarrow x$は収束構造を定める。

（証明）$p_{i}\langle x \rangle=\langle p_{i}(x) \rangle\rightarrow p_{i}(x)$より$\langle x \rangle\rightarrow x$である。

$\mathscr{F}\rightarrow x, \mathscr{G}\supset\mathscr{F}$とする。$p_{i}\mathscr{G}\supset p_{i}\mathscr{F}\rightarrow p_{i}(x)$より$p_{i}\mathscr{G}\rightarrow p_{i}(x)$である。

$\mathscr{F}, \mathscr{G}\rightarrow x$とする。$p_{i}\mathscr{F}, p_{i}\mathscr{G}\rightarrow p_{i}(x)$より$p_{i}\mathscr{F}\cap p_{i}\mathscr{G}\rightarrow p_{i}(x)$であるから、$p_{i}(\mathscr{F}\cap\mathscr{G})\supset p_{i}\mathscr{F}\cap p_{i}\mathscr{G}$を示せば良い。$V\in p_{i}\mathscr{F}\cap p_{i}\mathscr{G}$とする。ある$F\in\mathscr{F}, G\in\mathscr{G}$が存在して$V=p_{i}(F)=p_{i}(G)$と表せる。

$$
\begin{aligned}
F\subset p_{i}^{-1}(p_{i}(F))&=p_{i}^{-1}(V),& G\subset p_{i}^{-1}(p_{i}(G))=p_{i}^{-1}(V)
\end{aligned}
$$

より$p_{i}^{-1}(V)\in\mathscr{F}\cap\mathscr{G}$が分かる。よって$V=p_{i}(p_{i}^{-1}(V))\in p_{i}(\mathscr{F}\cap\mathscr{G})$である。以上より$p_{i}(\mathscr{F}\cap\mathscr{G})\rightarrow p_{i}(x)$を得る。$\square$

__定義__ 上記の収束構造により$X=\prod X_{i}$は収束空間となる。これを収束空間$X_{i}$の積と呼ぶ。

収束空間の積は次の普遍性を満たす。つまり圏$\mathbf{Conv}$における積対象である。

__命題__ $X_{i}$を収束空間、$X=\prod X_{i}$をその積、$p_{i}\colon X\rightarrow X_{i}$を射影とする。収束空間$Z$と連続射$f_{i}\colon Z\rightarrow X_{i}$に対し、ある唯一つの連続射$h\colon Z\rightarrow X$が存在して$f_{i}=p_{i}\circ h$を満たす。

（証明）$h(z):=(f_{i}(z))$が連続射となることを示せばよい。$Z$において$\mathscr{H}\rightarrow z$とする。$f_{i}$は連続射なので$(f_{i})_{\ast}\mathscr{H}\rightarrow f_{i}(z)$が成り立つ。推移性より$(f_{i})_{\ast}=p_{i}\circ h_{\ast}$だから$p_{i}(h_{\ast}\mathscr{H})=( f_{i} )_{\ast}\mathscr{H}\rightarrow f_{i}(z)=p_{i}( h(z) )$が成り立つ。故に$h_{\ast}\mathscr{H}\rightarrow h(z)$を得る。$\square$