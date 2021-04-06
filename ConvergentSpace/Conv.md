
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

- 始収束構造は各$f_{i}$を連続射とする最大の収束構造である。実際$(X, \iota)$を始収束構造、$f_{i}\colon(X, \lambda)\rightarrow (Y_{i}, \phi_{i})$を連続射とすると、$\mathscr{F}\in\lambda(x)$なら$(f_{i})_{\ast}\mathscr{F}\in\phi_{i}(f_{i}(x))$であり、故に$\mathscr{F}\in\iota(x)$を得る。従って$\lambda(x)\subset\iota(x)$が成り立つ。

始収束構造は次の普遍性を満たす。

__定理__ $(X, \lambda), (Y_{i}, \phi_{i})$を収束空間、$f_{i}\colon X\rightarrow Y_{i}$を写像とする。TFAE

1. 任意の収束空間$(Z, \psi)$及び写像$h\colon Z\rightarrow X$について、$f_{i}\circ h$が連続射であることと$h$が連続射であることは同値である。
1. $X$は$\lbrace f_{i} \rbrace$による始収束空間である。

（証明）上から下を示す。$(Z, \psi)$として$(X, \lambda)$を取ると$h:=\mathrm{id}_{X}$は連続射だから仮定より$f_{i}=f_{i}\circ h$も連続射である。故に始収束構造の最大製より$\lambda(x)\subset\iota(x)$を得る。逆は$(Z, \psi)$として$\lbrace f_{i} \rbrace$による始収束構造$(X, \iota)$を取り、$h(x):=x$と定める。始収束構造の定義より$\mathscr{F}\in\iota(x)$なら$(f_{i})_{\ast}\mathscr{F}\in\phi_{i}(f_{i}(x))$だが、$(f_{i})_{\ast}\mathscr{F}=(h\circ f_{i})_{\ast}\mathscr{F}$より$h\circ f_{i}$が連続と分かる。従って仮定より$h$は連続である。このとき$\mathscr{F}\in\iota(x)$なら$\mathscr{F}=h_{\ast}\mathscr{F}\in\lambda(x)$より$\iota(x)\subset\lambda(x)$を得る。以上より$\lambda(x)=\iota(x)$である。

$(X, \lambda)=(X, \iota)$は$\lbrace f_{i} \rbrace$による始収束構造だから以下は同値である。

1. $f_{i}\circ h\colon (Z, \psi)\rightarrow (Y_{i}, \phi_{i})$が連続射である。
1. $\mathscr{F}\in\psi(z)$について$(f_{i})_{\ast}(h_{\ast}\mathscr{F})=(f_{i}\circ h)_{\ast}\mathscr{F}\in\phi_{i}(f_{i}(h(z)))$である。
1. $\mathscr{F}\in\psi(z)$について$h_{\ast}\mathscr{F}\in \iota(h(z))$である。
1. $h\colon (Z, \psi)\rightarrow (X, \iota)$は連続射である。

以上より下から上が成り立つ。$\square$

__系__ $X$を集合、$\lbrace Y_{i} : i\in I \rbrace$を集合族、$\lbrace (Z_{ij}, \phi_{ij}) : i\in I, j\in J_{i} \rbrace$を収束空間とする。$f_{i}\colon X\rightarrow Y_{i}, g_{ij}\colon Y_{i}\rightarrow Z_{ij}$を写像とする。$Y_{i}$は$\lbrace g_{ij} : j\in J_{i} \rbrace$による始収束構造$\iota_{i}$で収束空間とみなせる。このとき$\lbrace g_{ij}\circ f_{i} : i\in I, j\in J_{i} \rbrace$による始収束構造と、$\lbrace f_{i} : i\in I \rbrace$による始収束構造は一致する。

（証明）$\lbrace g_{ij}\circ f_{i} : i\in I, j\in J_{i} \rbrace$による始収束構造を$\alpha$、$\lbrace f_{i} : i\in I \rbrace$による始収束構造を$\beta$とする。定理より以下は同値である。

1. $h\colon (Z, \psi)\rightarrow (X, \alpha)$が連続射である。
1. 任意の$i\in I, j\in J_{i}$について$(g_{ij}\circ f_{i})\circ h=g_{ij}\circ(f_{i}\circ h)\colon (Z, \psi)\rightarrow (Z_{ij}, \phi_{ij})$が連続射である。
1. 任意の$i\in I$について$f_{i}\circ h\colon (Z, \psi)\rightarrow(Y_{i}, \iota_{i})$が連続射である。
1. $h\colon (Z, \psi)\rightarrow (X, \beta)$が連続射である。

$(Z, \psi)=(X, \alpha)$として$h(x)=x$を取れば上から下を辿って$\alpha(x)\subset\beta(x)$を得る。同様に$\psi=\beta$とすれば下から上を辿って$\beta(x)\subset\alpha(x)$を得る。故に$\alpha(x)=\beta(x)$である。$\square$




### 収束空間の逆像、部分収束空間

__定義__ $(Y, \lambda)$を収束空間、$f\colon X\rightarrow Y$を写像とする。$\lbrace f \rbrace$による始収束構造を収束空間の **逆像** と呼び、$f^{\ast}\lambda$と表す。

> 特に部分集合$X\subset Y$に対して、$X$上の収束構造を入射$X\rightarrow Y$より定めることができる。




### 収束空間の直積

__定義__ $Y_{i}$を収束空間、$X=\prod Y_{i}$として$p_{i}\colon X\rightarrow Y_{i}$を射影とする。$\lbrace p_{i} \rbrace$による始収束空間を収束空間$Y_{i}$の直積と呼ぶ。

__命題__ $X_{i}$を収束空間、$X=\prod X_{i}$をその直積、$p_{i}\colon X\rightarrow X_{i}$を射影とする。収束空間$Z$と連続射$f_{i}\colon Z\rightarrow X_{i}$に対し、ある唯一つの連続射$h\colon Z\rightarrow X$が存在して$f_{i}=p_{i}\circ h$を満たす。

（証明）$h(z):=(f_{i}(z))$が連続射となることを示せばよい。$Z$において$\mathscr{H}\rightarrow z$とする。$f_{i}$は連続射なので$(f_{i})_{\ast}\mathscr{H}\rightarrow f_{i}(z)$が成り立つ。推移性より$(f_{i})_{\ast}=p_{i}\circ h_{\ast}$だから$p_{i}(h_{\ast}\mathscr{H})=( f_{i} )_{\ast}\mathscr{H}\rightarrow f_{i}(z)=p_{i}( h(z) )$が成り立つ。故に$h_{\ast}\mathscr{H}\rightarrow h(z)$を得る。$\square$

> 収束空間の直積は圏$\mathbf{Conv}$における直積対象である。