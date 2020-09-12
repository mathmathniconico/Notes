
## Continuous Convergence Structure

__定義__ $X, Y$を収束空間とする。次の記号を導入する。

- $X$から$Y$への連続射全体を$C(X, Y)$と表す。
- $F\subset C(X, Y)$と$A\subset X$について、$FA:=\lbrace f(a) : f\in F, a\in A \rbrace$と表す。
- $C(X, Y)$のフィルター$\mathscr{F}$及び$X$のフィルター$\mathscr{A}$について、$\mathscr{F}\cdot\mathscr{A}:=\langle \lbrace FA : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle$と表す。

> $F, G\subset C(X, Y)$及び$A, B\subset X$について$FA\cup GB\supset(F\cup G)(A\cap B)$が成り立つ。

__定理__ $C(X, Y)$のフィルター$\mathscr{F}$及び連続射$f\colon X\rightarrow Y$に対し、$\mathscr{F}\rightarrow f$を以下で定める。

- $X$において$\mathscr{A}\rightarrow x$なら、$\mathscr{F}\cdot\mathscr{A}\rightarrow f(x)$である。

このとき$\rightarrow$は$C(X, Y)$上の収束構造を定める。即ち$C(X, Y)$は収束空間となる。

（証明）まず連続射$f\colon X\rightarrow Y$について$\langle f \rangle\rightarrow f$を示したい。$\mathscr{A}\rightarrow x$として$\langle f \rangle\cdot\mathscr{A}\rightarrow f(x)$を示せば良い。$f\in\lbrace f \rbrace$より$\lbrace f \rbrace\in\langle f \rangle$である。

$$
f\mathscr{A}=\lbrace f(A) : A\in\mathscr{A} \rbrace=\lbrace \langle f \rangle A : A\in\mathscr{A} \rbrace\subset\lbrace FA : F\in\langle f \rangle, A\in\mathscr{A} \rbrace
$$

より$f_{\ast}\mathscr{A}\subset\langle f \rangle\cdot\mathscr{A}$を得る。$f$は連続なので$f_{\ast}\mathscr{A}\rightarrow f(x)$であり、従って$\langle f \rangle\cdot\mathscr{A}\rightarrow f(x)$を得る。

次に$\mathscr{F}\rightarrow f, \mathscr{F}\subset\mathscr{G}$について$\mathscr{G}\rightarrow f$を示したい。$\mathscr{A}\rightarrow x$として

$$
\lbrace FA : F\in\mathscr{F}, A\in\mathscr{A} \rbrace\subset\lbrace GA : G\in\mathscr{G}, A\in\mathscr{A} \rbrace
$$

より$\mathscr{F}\cdot\mathscr{A}\subset\mathscr{G}\cdot\mathscr{A}$である。故に$\mathscr{G}\cdot\mathscr{A}\rightarrow f(x)$を得る。

最後に$\mathscr{F}, \mathscr{G}\rightarrow f$について$\mathscr{F}\cap\mathscr{G}\rightarrow f$を示したい。$\mathscr{A}\rightarrow x$とする。$V\in\mathscr{F}\cdot\mathscr{A}\cap\mathscr{G}\cdot\mathscr{A}$に対し、$F\in\mathscr{F}, G\in\mathscr{G}, A, B\in\mathscr{A}$が存在して$FA, GB\subset V$を満たす。$V\supset FA\cup GB\supset(F\cup G)(A\cap B)$なので、$F, G\subset F\cup G$より$F\cup G\in\mathscr{F}\cap\mathscr{G}$が分かる。故に$\mathscr{F}\cdot\mathscr{A}\cap\mathscr{G}\cdot\mathscr{A}\subset(\mathscr{F}\cap\mathscr{G})\cdot\mathscr{A}$だから、$(\mathscr{F}\cap\mathscr{G})\cdot\mathscr{A}\rightarrow f(x)$を得る。$\square$

__定義__ 定理の収束構造を$C(X, Y)$の **Continuous Convergence Structure(CCS)** と呼び、特に断らない限り$C(X, Y)$はこの意味での収束空間とする。

評価写像$\mathrm{eval}\colon C(X, Y)\times X\rightarrow Y$を$\mathrm{eval}(f, x)=f(x)$で定める。

__命題__ $X, Y$を収束空間とする。$\mathscr{F}$を$X$のフィルター、$f\colon X\rightarrow Y$を連続射とする。TFAE

- $C(X, Y)$において$\mathscr{F}\rightarrow f$である。
- $X$において$\mathscr{A}\rightarrow x$なら、$Y$において$\mathrm{eval}_{\ast}(\mathscr{F}\prod\mathscr{A})\rightarrow f(x)$である。

（証明）$\mathscr{A}$を$X$のフィルターとする。$\mathscr{F}\prod\mathscr{A}=\langle \lbrace F\times A : F\in\mathscr{A}, A\in\mathscr{A} \rbrace \rangle$だから、

$$
\begin{aligned}
\mathrm{eval}_{\ast}(\mathscr{F}\prod\mathscr{A}) &=\mathrm{eval}_{\ast}\langle \lbrace F\times A : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=\langle \mathrm{eval}\lbrace F\times A : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=\langle \lbrace FA : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=\mathscr{F}\cdot\mathscr{A}
\end{aligned}
$$

が成り立つ。命題の同値性はこの等式より従う。$\square$

__系__ $\mathrm{eval}\colon C(X, Y)\times X\rightarrow Y$は連続射である。

（証明）$C(X, Y)$において$\mathscr{F}\rightarrow (f, x)$とする。$p_{i}$を射影として$p_{1}\mathscr{F}\rightarrow f, p_{2}\mathscr{F}\rightarrow x$が成り立つ。$p_{1}\mathscr{F}\rightarrow f$より、上の命題から$\mathrm{eval}_{\ast}(p_{1}\mathscr{F}\prod p_{2}\mathscr{F})\rightarrow f(x)$を得る。$\mathscr{F}\supset p_{1}\mathscr{F}\prod p_{2}\mathscr{F}$より$\mathrm{eval}_{\ast}\mathscr{F}\rightarrow f(x)$を得る。$\square$

CCSは次の普遍性を満たし、従って圏$\mathbf{Conv}$における冪対象を定める。

__系__ $Y, Z$を収束空間とする。任意の収束空間$X$及び連続射$g\colon X\times Y\rightarrow Z$に対し、ある連続射$h\colon X\rightarrow C(Y, Z)$が唯一つ存在し、$\mathrm{eval}\colon C(Y, Z)\times Y\rightarrow Z$について$g=\mathrm{eval}\circ(h\times\mathrm{id}_{Y})$が成り立つ。

（証明）$x\in X$に対し、$h(x)=f_{x}\colon Y\rightarrow Z$を$y\mapsto f_{x}(y)=g(x, y)$で定める。

まず$f_{x}$が連続射であることを示す。$Y$において$\mathscr{G}\rightarrow y$とする。$\langle x \rangle\rightarrow x$について$\langle x \rangle\prod\mathscr{G}\rightarrow (x, y)$である。$g$は連続なので$g_{\ast}(\langle x \rangle\prod\mathscr{G})\rightarrow g(x, y)$である。ここで$\langle x \rangle\prod\mathscr{G}=\langle \lbrace F\times G : F\in\langle x \rangle, G\in\mathscr{G} \rbrace \rangle$より、$g_{\ast}(\langle x \rangle\prod\mathscr{G})=\langle \lbrace g(F\times G) : F\in\langle x \rangle, G\in\mathscr{G} \rbrace \rangle$が成り立つ。一方

$$
(f_{x})_{\ast}\mathscr{G}=\langle \lbrace f_{x}(G) : G\in\mathscr{G} \rbrace \rangle=\langle \lbrace g(\lbrace x \rbrace\times G) : G\in\mathscr{G} \rbrace \rangle
$$

だから、それぞれの生成系はprefilterである。実際prefilterであることは$F, A\in\langle x \rangle, G, B\in\mathscr{G}$として

$$
g(F\times G)\cap g(A\times B)\supset g(F\times G\cap A\times B)\supset g(F\cap A\times G\cap B)
$$

などから分かる。故に生成系は$\lbrace g(F\times G) \rbrace\dashv\lbrace g(\lbrace x \rbrace\times G) \rbrace$を満たし、$g_{\ast}(\langle x \rangle\prod\mathscr{G})\subset (f_{x})_{\ast}\mathscr{G}$を得る。（逆の包含も$\lbrace g(F\times G) \rbrace\supset\lbrace g(\lbrace x \rbrace\times G) \rbrace$より成り立つ。）よって$(f_{x})_{\ast}\mathscr{G}\rightarrow g(x, y)=f_{x}(y)$を得る。

次に$h$が連続であることを示す。$X$において$\mathscr{F}\rightarrow x$とする。$C(Y, Z)$において$h_{\ast}\mathscr{F}\rightarrow h(x)=f_{x}$であることを示すには、定理より$Y$において$\mathscr{A}\rightarrow y$として$Z$において$\mathrm{eval}_{\ast}(h_{\ast}\mathscr{F}\prod\mathscr{A})\rightarrow f_{x}(y)=g(x, y)$を示せば良い。

$$
\begin{aligned}
(h\times\mathrm{id}_{Y})_{\ast}(\mathscr{F}\prod\mathscr{A}) &= (h\times\mathrm{id}_{Y})_{\ast}\langle \lbrace F\times A : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=\langle (h\times\mathrm{id}_{Y})\lbrace F\times A : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=\langle \lbrace h(F)\times A : F\in\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&\subset\langle \lbrace V\times A : V\in h_{\ast}\mathscr{F}, A\in\mathscr{A} \rbrace \rangle \\
&=h_{\ast}\mathscr{F}\prod\mathscr{A}
\end{aligned}
$$

より（逆の包含も成り立つ。）

$$
\begin{aligned}
\mathrm{eval}_{\ast}(h_{\ast}\mathscr{F}\prod\mathscr{A}) &\supset \mathrm{eval}_{\ast}( (h\times\mathrm{id}_{Y})_{\ast}(\mathscr{F}\prod\mathscr{A}) ) \\
&=(\mathrm{eval}\circ(h\times\mathrm{id}_{Y}))_{\ast}(\mathscr{F}\prod\mathscr{A}) \\
&=g_{\ast}(\mathscr{F}\prod\mathscr{A})
\end{aligned}
$$

を得る。今$\mathscr{F}\rightarrow x, \mathscr{G}\rightarrow y$だから$\mathscr{F}\rightarrow\prod\mathscr{A}\rightarrow (x, y)$であり、$g$は連続なので$g_{\ast}(\mathscr{F}\prod\mathscr{A})\rightarrow g(x, y)$つまり$\mathrm{eval}_{\ast}(h_{\ast}\mathscr{F}\prod\mathscr{A})\rightarrow g(x, y)$が従う。$\square$

> 上の写像$h$は$\lambda g$とも書かれ、カリー化と呼ばれたりする。

以上より圏$\mathbf{Conv}$は以下を満たし、従って **カルテシアン閉圏** である。

- 終対象が存在する。
- 有限直積対象が存在する。
- 冪対象が存在する。