
## フィルター射（始フィルターと終フィルター）

集合$X$とフィルター$\mathscr{F}\subset 2^{X}$の組$(X, \mathscr{F})$を **フィルター付き集合** と呼ぶ。

__定義__ フィルター付き集合$(X, \mathscr{F}), (Y, \mathscr{G})$について、写像$f\colon X\rightarrow Y$が以下を満たすとき **フィルター射** という。

- 任意の$G\in\mathscr{G}$について$f^{-1}(G)\in\mathscr{F}$である。

これは$Y$のフィルター$\mathscr{G}$が集合族$\mathscr{S}\subset 2^{Y}$で生成されているとき次と同値になる。

- 任意の$S\in\mathscr{S}$について$f^{-1}(S)\in\mathscr{F}$である。

> フィルター射の合成はフィルター射になる。よってフィルター付き集合とフィルター射は圏を為す。圏としては始対象$(\emptyset, \lbrace \emptyset \rbrace)$と終対象$(\lbrace \ast \rbrace, \lbrace\lbrace \ast \rbrace\rbrace)$がある。


### 始フィルター

__定義__ $X$を集合とする。添え字$i\in I$について、$(Y_{i}, \mathscr{G}_{i})$をフィルター付き集合、$f_{i}\colon X\rightarrow Y_{i}$を写像とする。

$$
\bigcup f_{i}^{-1}\mathscr{G}_{i}=\lbrace f_{i}^{-1}( G_{i} )\subset X : G_{i}\in\mathscr{G}_{i}, i\in I \rbrace
$$

が生成する$X$のフィルターを、$\lbrace f_{i} \rbrace$による **始フィルター** と呼ぶ。

- 上で定義した始フィルターは各$f_{i}$をフィルター射とする最小のフィルターである。

始フィルターは次の普遍性を満たす。

__定理__ $(X, \mathscr{F}), (Y_{i}, \mathscr{G}_{i})$をフィルター付き集合、$f_{i}\colon X\rightarrow Y_{i}$とする。TFAE

- 任意のフィルター付き集合$(Z, \mathscr{H})$及び$h\colon Z\rightarrow X$について、$f_{i}\circ h$がフィルター射であることと$h$がフィルター射であることは同値である。
- $\mathscr{F}$は$\lbrace f_{i} \rbrace$による始フィルターである。

（証明）$\lbrace f_{i} \rbrace$による始フィルターを$\mathcal{I}$とおく。

上から下を示す。まず$(Z, \mathscr{H})=(X, \mathscr{F})$として$h=\mathrm{id}_{X}$とする。$\mathrm{id}_{X}$はフィルター射だから、仮定より$f_{i}=f_{i}\circ\mathrm{id}_{X}$もフィルター射である。始フィルターの最小性より$\mathcal{I}\subset\mathscr{F}$を得る。逆は$(Z, \mathscr{H})=(X, \mathcal{I})$として$h(x)=x$とする。始フィルターの定義より$f_{i}\circ h$はフィルター射である。仮定より$h$もフィルター射であるから$\mathscr{F}\subset\mathcal{I}$となる。

$\mathscr{F}=\mathcal{I}$とする。$(Z, \mathscr{H})$をフィルター付き集合、$h\colon Z\rightarrow X$とする。

$$
\mathcal{I}=\langle \lbrace f_{i}^{-1}(G_{i})\subset X : G_{i}\in\mathscr{G}_{i} \rbrace \rangle
$$

だから、以下は同値である。

- $h$はフィルター射である。
- 任意の$i\in I, G_{i}\in\mathscr{G}_{i}$について$h^{-1}(f_{i}^{-1}(G_{i}))\in\mathscr{H}$である。
- 任意の$i\in I, G_{i}\in\mathscr{G}_{i}$について$(f_{i}\circ h)^{-1}(G_{i})\in\mathscr{H}$である。
- 任意の$i\in I$について$f_{i}\circ h$はフィルター射である。

以上より下から上が成り立つ。$\square$

定理の系として次の推移性が成り立つ。

__系__ $X$を集合、$\lbrace Y_{i} : i\in I \rbrace$を集合族、$\lbrace (Z_{ij}, \mathscr{H}_{ij}) : i\in I, j\in J_{i} \rbrace$をフィルター付き集合の族とする。$f_{i}\colon X\rightarrow Y_{i}, g_{ij}\colon Y_{i}\rightarrow Z_{ij}$を写像とする。$Y_{i}$は$\lbrace g_{ij} : j\in J_{i} \rbrace$による始フィルター$\mathscr{G}_{i}$でフィルター付き集合とみなせる。このとき$\lbrace g_{ij}\circ f_{i} : i\in I, j\in J_{i} \rbrace$による始フィルターと、$\lbrace f_{i} : i\in I \rbrace$による始フィルターは一致する。

（証明）$\lbrace g_{ij}\circ f_{i} : i\in I, j\in J_{i} \rbrace$による始フィルターを$\mathcal{I}$、$\lbrace f_{i} : i\in I \rbrace$による始フィルターを$\mathcal{J}$とする。$(Z, \mathscr{H})$をフィルター付き集合、$h\colon Z\rightarrow X$とする。定理より以下は同値である。

- $h\colon (Z, \mathscr{H})\rightarrow(X, \mathcal{I})$がフィルター射である。
- 任意の$i\in I, j\in J_{i}$について$(g_{ij}\circ f_{i})\circ h=g_{ij}\circ(f_{i}\circ h)\colon (Z, \mathscr{H})\rightarrow (Z_{ij}, \mathscr{H}_{ij})$がフィルター射である。
- 任意の$i\in I$について$f_{i}\circ h\colon(Z, \mathscr{H})\rightarrow(Y_{i}, \mathscr{G}_{i})$がフィルター射である。
- $h\colon(Z, \mathscr{H})\rightarrow(X, \mathcal{J})$がフィルター射である。

$(Z, \mathscr{H})=(X, \mathcal{I})$として$h(x)=x$を取れば上から下へ辿って$\mathcal{J}\subset\mathcal{I}$を得る。同様に$\mathscr{H}=\mathcal{J}$とすれば下から上へ辿って$\mathcal{I}\subset\mathcal{J}$を得る。故に$\mathcal{I}=\mathcal{J}$である。$\square$

始フィルターで定義できる概念がいくつかある。

- $(Y, \mathscr{G})$をフィルター付き集合、$f\colon X\rightarrow Y$を写像とする。$\lbrace f \rbrace$による始フィルターを **逆像フィルター** と呼び、$f^{\ast}\mathscr{G}$と表す。
- $(Y_{i}, \mathscr{G}_{i})$をフィルター付き集合、$X=\prod Y_{i}$として、$p_{i}\colon X\rightarrow Y_{i}$を射影とする。$\lbrace p_{i} \rbrace$による始フィルターを **直積フィルター** と呼び、$\prod\mathscr{G}_{i}$と表す。

__系__ $(Y_{i}, \mathscr{G}_{i})$をフィルター付き集合とする。$(\prod Y_{i}, \prod\mathscr{G}_{i})$は直積対象である。つまり次の普遍性を満たす。

- $(Z, \mathscr{H})$をフィルター付き集合、$g_{i}\colon (Z, \mathscr{H})\rightarrow (Y_{i}, \mathscr{G}_{i})$をフィルター射とする。このときあるフィルター射$h\colon (Z, \mathscr{H})\rightarrow (\prod Y_{i}, \prod \mathscr{G}_{i})$が存在して、$p_{i}\circ h=g_{i}$を満たす。

（証明）集合としての直積の定義より$p_{i}\circ h=g_{i}$を満たす写像$h\colon Z\rightarrow \prod Y_{i}$が唯一つ存在する。$g_{i}$がフィルター射なので、定理より$h$はフィルター射である。$\square$


### 終フィルター

始フィルターの逆向きで定義される概念が終フィルターである。

__定義__ $X$を集合とする。添え字$i\in I$について、$(Z_{i}, \mathscr{H}_{i})$をフィルター付き集合、$f_{i}\colon Z_{i}\rightarrow X$を写像とする。

$$
\bigcup f_{i}\mathscr{H}_{i}=\lbrace f_{i}( H_{i} )\subset X : H_{i}\in\mathscr{H}_{i}, i\in I \rbrace
$$

が生成する$X$のフィルターを、$\lbrace f_{i} \rbrace$による **終フィルター** と呼ぶ。

- 上で定義した終フィルターは各$f_{i}$をフィルター射とする最大のフィルターである。

> 実際$(X, \mathscr{F})$が各$f_{i}$をフィルター射とするなら、$F\in\mathscr{F}$に対して$f_{i}^{-1}(F)\in\mathscr{H}_{i}$である。$f_{i}(f_{i}^{-1}(F))\subset F$より$F$は終フィルターに属する。

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

__系__ $f\colon X\rightarrow Y$が全射のとき、フィルター$\mathscr{F}\subset 2^{X}$について

$$
f_{\ast}\mathscr{F}=f\mathscr{F}
$$

が成り立つ。

（証明）$f\mathscr{F}=\lbrace f(F) : F\in\mathscr{F} \rbrace$がフィルターであることを示せば上の命題より従う。ところで全射性より$G\subset Y$について$f(f^{-1}(G))=G$が成り立つから、$\mathscr{F}$がフィルターであることがそのまま$f\mathscr{F}$がフィルターであることに遺伝する。$\square$

> 以下、$f$が全射であることが明らかな場合は、$f_{\ast}\mathscr{F}=f\mathscr{F}$を断り無く用いる。