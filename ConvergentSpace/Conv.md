
## 収束空間

### 終フィルター

[フィルター射](/FilterMap.md)のところで始フィルターというものを導入した。この逆向きで定義される概念が終フィルターである。

__定義__ $X$を集合とする。添え字$i\in I$について、$(Z_{i}, \mathscr{H}_{i})$をフィルター付き集合、$f_{i}\colon Z_{i}\rightarrow X$を写像とする。

$$
\bigcup f_{i}\mathscr{H}_{i}=\lbrace f_{i}( H_{i} )\subset X : H_{i}\in\mathscr{H}_{i}, i\in I \rbrace
$$

が生成する$X$のフィルターを、$\lbrace f_{i} \rbrace$による **終フィルター** と呼ぶ。

- 上で定義した終フィルターは各$f_{i}$をフィルター射とする最大のフィルターである。

> $(X, \mathscr{F})$が各$f_{i}$をフィルター射とするなら、$F\in\mathscr{F}$に対して$f_{i}^{-1}(F)\in\mathscr{H}_{i}$である。$f_{i}(f_{i}^{-1}(F))\subset F$より$F$は終フィルターに属する。

始フィルターと同様に終フィルターは次の普遍性と推移性を満たす。

__定理__ $(X, \mathscr{F}), (Z_{i}, \mathscr{H}_{i})$をフィルター付き集合、$f_{i}\colon H_{i}\rightarrow X$とする。TFAE

- 任意のフィルター付き集合$(Y, \mathscr{G})$及び$h\colon X\rightarrow Y$について、$h\circ f_{i}$がフィルター射であることと$h$がフィルター射であることは同値である。
- $\mathscr{F}$は$\lbrace f_{i} \rbrace$による終フィルターである。

__系__ $X$を集合、$\lbrace Y_{i} : i\in I \rbrace$を集合族、$\lbrace (Z_{ij}, \mathscr{H}_{ij} : i\in I, j\in J_{i} ) \rbrace$をフィルター付き集合の族とする。$f_{i}\colon Y_{i}\rightarrow X, g_{ij}\colon Z_{ij}\rightarrow Y_{i}$を写像とする。$Y_{i}$は$\lbrace g_{ij} : j\in J_{i} \rbrace$による終フィルター$\mathscr{G}_{i}$でフィルター付き集合とみなせる。このとき$\lbrace g_{ij}\circ f_{i} : i\in I, j\in J_{i} \rbrace$による終フィルターと、$\lbrace f_{i} : i\in I \rbrace$による終フィルターは一致する。

__定義__ $(X, \mathscr{F})$をフィルター付き集合、$f\colon X\rightarrow Y$を写像とする。$\lbrace f \rbrace$による終フィルターを **像フィルター** と呼び、$f_{\ast}\mathscr{F}$と表す。

> 真フィルターの像フィルターは真フィルターになる。

__命題__ $f\colon X\rightarrow Y$を写像とする。集合族$\mathscr{S}\subset 2^{X}$について

$$
f_{\ast}\langle \mathscr{S} \rangle=\langle f\mathscr{S} \rangle
$$

が成り立つ。

（証明）$f_{\ast}\langle \mathscr{S} \rangle\supset f\langle \mathscr{S} \rangle\supset f\mathscr{S}$より、生成の最小性から$f_{\ast}\langle \mathscr{S} \rangle\supset \langle f\mathscr{S} \rangle$を得る。逆に$F\in f_{\ast}\langle \mathscr{S} \rangle$とする。ある$G\in\langle \mathscr{S} \rangle$が存在して$f(G)\subset F$である。更にある$H\in\mathscr{S}$が存在して$H\subset G$より、$f(H)\subset f(G)\subset F$となる。故に$F\in\langle f\mathscr{S} \rangle$を得る。$\square$

超フィルターと像フィルターの関係が興味深い。

__命題__ $f\colon X\rightarrow Y$を写像とする。以下が成り立つ。

- $\mathscr{U}\subset 2^{X}$をの超フィルターとすると、$f_{\ast}\mathscr{U}\subset 2^{Y}$も超フィルターである。
- $\mathscr{F}\subset 2^{X}$を真フィルターとする。$f_{\ast}\mathscr{F}$を含む超フィルター$\mathscr{V}\subset 2^{Y}$について、ある$X$の超フィルター$\mathscr{U}\subset 2^{X}$が存在して$\mathscr{F}\subset\mathscr{U}$かつ$f_{\ast}\mathscr{U}=\mathscr{V}$を満たす。

（証明）$W\notin f_{\ast}\mathscr{U}$とする。$f(f^{-1}(W))\subset W$より$f^{-1}(W)\notin\mathscr{U}$である。超フィルターの特徴付けより$X\backslash f^{-1}(W)\in\mathscr{U}$を得る。$f(X\backslash f^{-1}(W))\subset Y\backslash W$より$Y\backslash W\in f_{\ast}\mathscr{U}$である。

$V\in\mathscr{V}$について$X\in\mathscr{F}$より$f(X)\subset Y\backslash V$なら$Y\backslash V\in f_{\ast}\mathscr{F}\subset\mathscr{V}$より矛盾する。故に$f^{-1}(V)\neq\emptyset$であり、従って$f^{\ast}\mathscr{V}$は真フィルターである。更に$\mathscr{F}$と$f^{\ast}\mathscr{V}$は交わる。実際$F\in\mathscr{F}$及び$V\in\mathscr{V}$について$f(F)\cap V=\emptyset$なら$f(F)\subset Y\backslash V$より$Y\backslash V\in f_{\ast}\mathscr{F}\subset\mathscr{V}$となり矛盾する。以上より$\mathscr{F}\vee f^{\ast}\mathscr{V}$は真フィルターである。これを含む超フィルター$\mathscr{U}$を取れば、$\mathscr{F}\subset\mathscr{U}$であり、$\mathscr{V}\subset f_{\ast}(f^{\ast}\mathscr{V})\subset f_{\ast}\mathscr{U}$と極大性より$\mathscr{V}=f_{\ast}\mathscr{U}$を得る。$\square$


### 収束空間と連続射

__定義__ $X$を集合とする。各点$x\in X$について$\lambda(x)$をフィルターの族とする。$\lambda\colon x\mapsto\lambda(x)$が以下を満たすとき$(X, \lambda)$を **収束空間** （convergent space）と呼ぶ。

- $\langle x \rangle\in\lambda(x)$である。
- $\mathscr{F}\in\lambda(x)$とする。フィルター$\mathscr{G}\subset 2^{X}$について$\mathscr{F}\subset\mathscr{G}$なら$\mathscr{G}\in\lambda(x)$である。
- $\mathscr{F}, \mathscr{G}\in\lambda(x)$なら$\mathscr{F}\cap\mathscr{G}\in\lambda(x)$である。

フィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\in\lambda(x)$であることを$\mathscr{F}\rightarrow x$と書けば$\lambda$を明示せずに収束空間を定義できる。この意味で上記を満たす関係$\rightarrow$を収束構造（convergent structure）とも呼ぶ。（フィルター全体$\Phi(X)$について$\Phi(X)\times X$の部分集合としての「関係」である。）$\mathscr{F}\rightarrow x$のとき$\mathscr{F}$は$x$に収束するといい、$x$は$\mathscr{F}$の収束先や極限点ともいう。

__定義__ $X, Y$を収束空間、$f\colon X\rightarrow Y$を写像とする。任意のフィルター$\mathscr{F}\subset 2^{X}$について$\mathscr{F}\rightarrow x$なら$f_{\ast}\mathscr{F}\rightarrow f(x)$であるとき、$f$は$x$で **連続** （continuous）という。任意の$x\in X$で$f$が連続のとき、$f$を **連続射** と呼ぶ。

終フィルターの推移性より、連続射の合成もまた連続射である。

__例__ 有向グラフ（directed graph）とは、頂点の集合$V$と、向き付けられた辺の集合$E\subset V\times V$の組$(V, E)$である。（$(v, u)\in E$は始点$v$から終点$u$への有向辺とする。）有向グラフが反射的（reflexible）とは、任意の頂点$v\in V$について$(v, v)\in E$が成り立つことをいう。

さて、反射的有向グラフ$(V, E)$において、頂点$v\in V$を始点とする有向辺の終点全体

$$
\overrightarrow{v}:=\lbrace u\in V : (v, u)\in E \rbrace
$$

を考える。このとき収束構造$\mathscr{F}\rightarrow v$を$\overrightarrow{v}\in\mathscr{F}$で定めることができる。実際$(v, v)\in E$より$v\in\overrightarrow{v}$だから$\overrightarrow{v}\in\langle v \rangle$故に$\langle v \rangle\rightarrow v$である。$\mathscr{F}\rightarrow v, \mathscr{F}\subset\mathscr{G}$とすれば$\overrightarrow{v}\in\mathscr{F}\subset\mathscr{G}$より$\mathscr{G}\rightarrow v$である。$\overrightarrow{v}\in\mathscr{F}, \mathscr{G}$なら$\overrightarrow{v}\in\mathscr{F}\cap\mathscr{G}$も成り立つ。このようにして反射的有向グラフは収束空間となる。

- この収束構造では単項フィルター$\langle \overrightarrow{v} \rangle$は$v$に収束する。

__定理__ $(V_{1}, E_{1}, (V_{2}, E_{2})$を反射的有向グラフとする。$f\colon V_{1}\rightarrow V_{2}$を写像とする。$v\in V_{1}$とする。TFAE

- $f$は$v$で連続である。
- $f(\overrightarrow{v})\subset\overrightarrow{f(v)}$が成り立つ。

（証明）$f$が$v$で連続とすると、$\langle \overrightarrow{v} \rangle\rightarrow v$より$f_{\ast}\langle \overrightarrow{v} \rangle\rightarrow f(v)$である。つまり$\overrightarrow{f(v)}\in f_{\ast}\langle \overrightarrow{v} \rangle=\langle f(\overrightarrow{v}) \rangle$だから、$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$となる。

逆に$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$なら、$\mathscr{F}\rightarrow v$について$\overrightarrow{v}\in\mathscr{F}$より$f(\overrightarrow{v})\in f\mathscr{F}\subset f_{\ast}\mathscr{F}$である。従ってフィルターの性質より$\overrightarrow{f(v)}\in f_{\ast}\mathscr{F}$を得る。つまり$f$は$v$で連続となる。$\square$

> 条件$f(\overrightarrow{v})\subset\overrightarrow{f(v)}$は$(v, u)\in E_{1}$なら$(f(v), f(u))\in E_{2}$を意味する。従って$f$が連続であることは、$f$がグラフ準同型であることに他ならない。

- 半順序集合は反射的有向グラフとみなせる。このとき連続射は順序を保つ写像に他ならない。