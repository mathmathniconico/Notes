
# 収束空間と連続射

__定義__ $X$を集合とする。各点$x\in X$について$\phi(x)$をフィルターの族とする。$\phi\colon x\mapsto\phi(x)$は以下を満たすとする。

- $\langle x \rangle\in\phi(x)$である。
- $\mathscr{F}\in\phi(x)$とする。フィルター$\mathscr{G}\subset 2^{X}$について$\mathscr{F}\subset\mathscr{G}$なら$\mathscr{G}\in\phi(x)$である。
- $\mathscr{F}, \mathscr{G}\in\phi(x)$なら$\mathscr{F}\cap\mathscr{G}\in\phi(x)$である。

このとき$\phi$を**収束構造**（convergent structure）と呼び、組$(X, \phi)$を **収束空間** （convergent space）と呼ぶ。$\mathscr{F}\in\phi(x)$のときフィルター$\mathscr{F}$は$x$に収束するといい、$x$は$\mathscr{F}$の収束先や極限点などという。

フィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\in\phi(x)$であることを$\mathscr{F}\rightarrow x$と書けば$\phi$を明示せずに収束空間を定義できる。これはフィルター全体$\Phi(X)$について$\Phi(X)\times X$の部分集合としての「関係」である。

__定義__ $X, Y$を収束空間、$f\colon X\rightarrow Y$を写像とする。任意のフィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\rightarrow x$なら$f_{\ast}\mathscr{F}\rightarrow f(x)$であるとき、$f$は$x$で **連続** （continuous）であるという。任意の$x\in X$で$f$が連続のとき、$f$を **連続射** と呼ぶ。

- 終フィルターの推移性より、連続射の合成もまた連続射である。

収束空間と連続射は圏を為す。これを$\mathbf{Conv}$と書く。

> 始対象は$(X=\emptyset, \phi=\emptyset)$、終対象は$(Y=\lbrace \ast \rbrace, \phi(\ast)=\lbrace\emptyset, \lbrace \ast \rbrace \rbrace=2^{Y})$である。




## 始収束構造

フィルター付き集合の場合と同様に、収束空間に対しても始構造を定めることができる。

__命題__ $X$を集合とする。添え字$i\in I$について、$Y_{i}$を収束空間とする。$f_{i}\colon X\rightarrow Y_{i}$を写像とする。$X$のフィルター$\mathscr{F}$及び$x\in X$に対し、$\mathscr{F}\rightarrow x$を任意の$i\in I$について$(f_{i})_{\ast}\mathscr{F}\rightarrow f_{i}(x)$で定める。このとき$X$は収束空間となる。

（証明）$x\in X$とする。$i\in I$について$(f_{i})_{\ast}\langle x \rangle=\langle f_{i}(x) \rangle$より$\langle x \rangle\rightarrow x$である。

$\mathscr{F}\rightarrow x, \mathscr{F}\subset\mathscr{G}$を$X$のフィルターとする。$i\in I$について$(f_{i})_{\ast}\mathscr{G}\supset(f_{i})_{\ast}\mathscr{F}\rightarrow f_{i}(x)$だから、$(f_{i})_{\ast}\mathscr{G}\rightarrow f_{i}(x)$が成り立つ。従って$\mathscr{G}\rightarrow x$を得る。

$X$において$\mathscr{F}, \mathscr{G}\rightarrow x$とする。$i\in I$について$A\in(f_{i})_{\ast}\mathscr{F}\cap(f_{i})_{\ast}\mathscr{G}$とすると、ある$F\in\mathscr{F}, G\in\mathscr{G}$が存在して$f_{i}(F)\subset A, f_{i}(G)\subset A$を満たす。$f_{i}(F\cup G)=f_{i}(F)\cup f_{i}(G)\in\mathscr{F}\cap\mathscr{G}$は$A$に含まれるので、$A\in(f_{i})_{\ast}(\mathscr{F}\cap\mathscr{G})$が分かる。故に$(f_{i})_{\ast}(\mathscr{F}\cap\mathscr{G})\supset (f_{i})_{\ast}\mathscr{F}\cap(f_{i})_{\ast}\mathscr{G}\rightarrow x$より$\mathscr{F}\cap\mathscr{G}\rightarrow x$が従う。$\square$

__定義__ 上で定まる$X$の収束構造を$\lbrace f_{i} \rbrace$による **始収束構造** （initial convergent structure）と呼び、$X$を始収束空間と呼ぶ。

> 始収束構造は各$f_{i}$を連続射とする最小の収束構造である。

始収束構造は次の普遍性を満たす。

__命題__ $X, Y_{i}$を収束空間とする。$f_{i}\colon X\rightarrow Y_{i}$を写像とする。TFAE

1. 任意の収束空間$Z$及び写像$h\colon Z\rightarrow X$について、$f_{i}\circ h$が連続射であることと$h$が連続射であることは同値である。
1. $X$は$\lbrace f_{i} \rbrace$による始収束空間である。

（証明）$\square$

> TODO: 推移性

### 収束空間の逆像、部分収束空間

> TODO





### 収束空間の直積

__定義__ $Y_{i}$を収束空間、$X=\prod Y_{i}$として$p_{i}\colon X\rightarrow Y_{i}$を射影とする。$\lbrace p_{i} \rbrace$による始収束空間を収束空間$Y_{i}$の直積と呼ぶ。

> 収束空間の直積は圏$\mathbf{Conv}$における直積対象である。

__命題__ $X_{i}$を収束空間、$X=\prod X_{i}$をその直積、$p_{i}\colon X\rightarrow X_{i}$を射影とする。収束空間$Z$と連続射$f_{i}\colon Z\rightarrow X_{i}$に対し、ある唯一つの連続射$h\colon Z\rightarrow X$が存在して$f_{i}=p_{i}\circ h$を満たす。

<!-- 
（証明）$h(z):=(f_{i}(z))$が連続射となることを示せばよい。$Z$において$\mathscr{H}\rightarrow z$とする。$f_{i}$は連続射なので$(f_{i})_{\ast}\mathscr{H}\rightarrow f_{i}(z)$が成り立つ。推移性より$(f_{i})_{\ast}=p_{i}\circ h_{\ast}$だから$p_{i}(h_{\ast}\mathscr{H})=( f_{i} )_{\ast}\mathscr{H}\rightarrow f_{i}(z)=p_{i}( h(z) )$が成り立つ。故に$h_{\ast}\mathscr{H}\rightarrow h(z)$を得る。$\square$
-->