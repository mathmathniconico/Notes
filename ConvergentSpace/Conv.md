
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














## 収束空間の直積

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

__定義__ 上記の収束構造により$X=\prod X_{i}$は収束空間となる。これを収束空間$X_{i}$の直積と呼ぶ。

収束空間の直積は次の普遍性を満たす。つまり圏$\mathbf{Conv}$における直積対象である。

__命題__ $X_{i}$を収束空間、$X=\prod X_{i}$をその直積、$p_{i}\colon X\rightarrow X_{i}$を射影とする。収束空間$Z$と連続射$f_{i}\colon Z\rightarrow X_{i}$に対し、ある唯一つの連続射$h\colon Z\rightarrow X$が存在して$f_{i}=p_{i}\circ h$を満たす。

（証明）$h(z):=(f_{i}(z))$が連続射となることを示せばよい。$Z$において$\mathscr{H}\rightarrow z$とする。$f_{i}$は連続射なので$(f_{i})_{\ast}\mathscr{H}\rightarrow f_{i}(z)$が成り立つ。推移性より$(f_{i})_{\ast}=p_{i}\circ h_{\ast}$だから$p_{i}(h_{\ast}\mathscr{H})=( f_{i} )_{\ast}\mathscr{H}\rightarrow f_{i}(z)=p_{i}( h(z) )$が成り立つ。故に$h_{\ast}\mathscr{H}\rightarrow h(z)$を得る。$\square$