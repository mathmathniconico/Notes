
# 群の作用




## 群の作用

__定義__ $G$を群、$X$を集合とする。演算$\cdot\colon G\times X\rightarrow X$は以下を満たすとする。

- $a, b\in G, x\in X$について$(ab)\cdot x = a\cdot (b\cdot x)$が成り立つ。
- $x\in X$について$1_{G}\cdot x=x$が成り立つ。ただし$1_{G}$は$G$の単位元とする。

このとき$\cdot$を$G$の$X$への **作用** （action）と呼び、$G\curvearrowright X$と書く。作用が明らかなときは$a\cdot x$を$ax$と略記する。



> $X$の置換（$X$から$X$への全単射）全体$\mathrm{Sym}X$は合成に関して群となる。

作用は群の準同型$G\rightarrow\mathrm{Sym}X$のことである。

















__定義__ $G\curvearrowright X$を群の作用とする。$x\in X, S\subset G$とする。

- $\mathrm{Orb}_{x}:=\lbrace ax : a\in G \rbrace$を$x$の **軌道** （orbit）と呼ぶ。
- $\mathrm{Stab}_{x}:=\lbrace a\in G : ax=x \rbrace$を$x$の **固定群** （stabilizer）と呼ぶ。これは$G$の部分群となる。
- $\mathrm{Fix}_{S}X:=\lbrace x\in X : \forall s\in S, sx=x \rbrace$を$S$の **不変集合** （invariable set）と呼ぶ。




## 有限群と作用

以下$G$は有限群とする。

> 部分群$H\lt G$に対し、同値関係$a\theta_{H}b$を$b^{-1}a\in H$で定めた。このとき$a\in G$を含む同値類は$\overline{a}=\lbrace b\in G : b\theta_{H}a \rbrace=aH$で与えられる。

__定義__ $H\lt G$を部分群とする。同値関係$\theta_{H}$による同値類を **左剰余類** （left coset）と呼び、その個数を$(G : H)$と表す。

各剰余類は非交叉であり、その元の個数はちょうど$\vert H \vert$に等しい。従って

$$
\vert G \vert=( G : H )\vert H \vert
$$

が成り立つ。

__補題__ $G\curvearrowright X$を作用とする。$x, y\in X$に対して関係$x\sim y$を、ある$a\in G$が存在して$ax=y$のとき定める。以下が成り立つ。

- 関係$\sim$は$X$上の同値関係であり、$x\in X$の同値類は$\mathrm{Orb}_{x}$である。
- $g\in G, x\in X$について$g^{-1}( \mathrm{Stab}_{gx} )g=\mathrm{Stab}_{x}$が成り立つ。よって$x\sim y$なら固定群の位数は一致する。
- $x\in X$について$\vert \mathrm{Orb}_{x} \vert=(G : \mathrm{Stab}_{x})$が成り立つ。特に$\vert G \vert=\vert\mathrm{Orb}_{x}\vert\cdot\vert \mathrm{Stab}_{x} \vert$である。

（証明）一番上は明らか。$a\in\mathrm{Stab}_{gx}$なら$agx=gx$であり$g^{-1}ag\in\mathrm{Stab}_{x}$を得る。逆も同様。最後は$H:=\mathrm{Stab}_{x}$として全射$G\ni a\mapsto aH$を考える。$ax=bx$なら$b^{-1}a\in H$より$a\theta_{H}b$となるから、$aH\neq bH$なら$ax\neq bx$である。逆も同様なので$\mathrm{Orb}_{x}\ni ax\mapsto aH$は全単射である。残りの等式はラグランジュの定理より従う。$\square$







__命題__ $H, K\lt G$を部分群とする。このとき$\vert H \vert\cdot\vert K \vert=\vert HK \vert\cdot\vert H\cap K \vert$が成り立つ。

（証明）直積群$H\times K$の$HK$への作用を$(h, k)\cdot x:=hxk^{-1}$で定める。$\mathrm{Orb}_{1_{G}}=HK$だから

$$
\vert HK \vert=\vert \mathrm{Orb}_{1_{G}} \vert=(H\times K : \mathrm{Stab}_{1_{G}})
$$

となる。一方$\mathrm{Stab}_{1_{G}}=\lbrace (h, k)\in H\times K : h=k \rbrace$より$H\cap K$と集合として同型になる。よって

$$
\vert H \vert\cdot\vert K \vert=\vert H\times K \vert=(H\times K : \mathrm{Stab}_{1_{G}})\vert \mathrm{Stab}_{1_{G}} \vert=\vert HK \vert\cdot\vert H\cap K \vert
$$

となる。$\square$

__定理__ （バーンサイドの補題）群の作用$G\curvearrowright X$が軌道を$r$個持つとする。このとき

$$
r=\frac{1}{\vert G \vert}\sum_{a\in G}\vert \mathrm{Fix}_{a}X \vert
$$

が成り立つ。

> Burnsideは著書に掲載しただけで、実際の結果はCauchy及びFrobeniusによるものらしい。

（証明）$\lbrace (a, x)\in G\times X : ax=x \rbrace$を二通りで数え上げる。まず$a\in G$を固定すると$x$として$\mathrm{Fix}_{a}X$の元が取れる。よって濃度は

$$
\sum_{a\in G}\vert \mathrm{Fix}_{a}X \vert
$$

となる。一方で$x\in X$を固定すると$a$として$\mathrm{Stab}_{x}$の元が取れる。よって濃度は

$$
\sum_{x\in X}\vert \mathrm{Stab}_{x} \vert=\sum_{x\in X}\frac{\vert G \vert}{\vert \mathrm{Orb}_{x} \vert}=\vert G \vert\sum_{x\in X}\frac{1}{\vert \mathrm{Orb}_{x} \vert}
$$

となる。ところで右辺の和の部分は、各起動毎に$1$を取るので$\vert G \vert\cdot r$と等しい。$\square$


<!--
__例__ フェルマーの小定理をやや一般的な条件で示そう。$a$を整数、$m$を正の整数とする。このとき

$$
\sum_{k=1}^{m}a^{(k, m)}\equiv 0 \mod{m}
$$

が成り立つ。

（証明）まず$a\gt 0$に対して証明する。







まず$ a\gt 0 $に対して証明する。一般の群$ G $に対し、$ G $から$ \lbrace 1, 2, \dotsc, a \rbrace $への写像全体を$ X $と置く。
このとき$ \phi\in X $に対し$ g\cdot\phi(h):=\phi(hg^{-1}) $と定めると$ g\cdot\phi\in X $が定まり、$ G $の$ X $への作用を定める。
$ g\phi=\phi $は任意の$ h\in G $に対し$ \phi(hg^{-1})=\phi(h) $となることと同値になる。故に$ \phi $は$ h\langle g \rangle $上定数となる。
即ち$ \phi $として$ (G:\langle g \rangle)=\frac{\sharp G}{\mathrm{ord}g} $個の自由度があることが分かる。従って
\[ \sharp\mathrm{Fix}_{g}X=a^{\frac{\sharp G}{\mathrm{ord}g}} \]
を得る。定理より
\[ \frac{1}{\sharp G}\sum_{g\in G}a^{\frac{\sharp G}{\mathrm{ord}g}} \]
は定数となるから、
\[ \sum_{g\in G}a^{\frac{\sharp G}{\mathrm{ord}g}}\equiv 0\mod{\sharp G} \]
が従う。この式は$ a\mod{\sharp G} $で成立するから$ a\gt 0 $である必要はない。

特に$ G=\mathbb{Z}/m\mathbb{Z} $を加法群と見なせば$ k\in G $の位数は$ \frac{m}{(k, m)} $となり系が証明される。$ \square $



## 推移的な作用



__定義__ $G\curvearrowright X$を群の作用とする。

- $G\rightarrow\mathrm{Sym}X$が単射のとき、$G\curvearrowright X$は **効果的** （effective）という。
- 任意の$x, y\in X$に対して、ある$a\in G$が存在して$ax=y$が成り立つとき、$G\curvearrowright X$は **推移的** （transitive）という。

-->
