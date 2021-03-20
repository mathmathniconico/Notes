
# 群の作用

__定義__ $G$を群、$X$を集合とする。演算$\cdot\colon G\times X\rightarrow X$は以下を満たすとする。

- $a, b\in G, x\in X$について$(ab)\cdot x = a\cdot (b\cdot x)$が成り立つ。
- $x\in X$について$1_{G}\cdot x=x$が成り立つ。ただし$1_{G}$は$G$の単位元とする。

このとき$\cdot$を$G$の$X$への **作用** （action）と呼び、$G\curvearrowright X$と書く。作用が明らかなときは$a\cdot x$を$ax$と略記する。

> 作用は群の準同型$G\rightarrow\mathrm{Sym}X$とみなせる。実際$a\in G$について等式$\phi_{a}(x)=a\cdot x$により作用と準同型$\phi\colon G\rightarrow\mathrm{Sym}X$は一対一に対応する。この意味で$\phi\colon G\curvearrowright X$と表す。

__定義__ $G\curvearrowright X$を群の作用とする。

- $x\in X$について$\mathrm{Orb}_{x}:=\lbrace ax : a\in G \rbrace$を$x$の **軌道** （orbit）と呼ぶ。軌道全体を$X/G$で表す。
- $x\in X$について$\mathrm{Stab}_{x}:=\lbrace a\in G : ax=x \rbrace$を$x$の **固定群** （stabilizer）と呼ぶ。これは$G$の部分群となる。
- $S\subset X$について$X^{S}:=\lbrace y\in X : \forall s\in S, sy=y \rbrace$を$S$の **不変集合** （invariable set）と呼ぶ。$S=\lbrace a \rbrace$のときは$X^{a}$と書く。

__例__ 作用の例をいくつか挙げる。$G$を群、$H, K\lt G$を部分群とする。

- 作用$H\curvearrowright G/K$が$h\cdot\overline{x}:=\overline{hx}$で定まる。$G=H$のとき対応する準同型の核は$\bigcap_{x\in G}xKx^{-1}$であり$K$内で最大の正規部分群となる。
- 作用$H\curvearrowright G$が$h\cdot x:=hxh^{-1}$で定まる。$\mathrm{Orb}_{x}$は$x$の$H$ **共役類** と呼ばれる。
- 作用$H\times K\curvearrowright HK$が$(h, k)\cdot x:=hxk^{-1}$で定まる。
- $n\le\vert G \vert$について$G_{n}:=\lbrace S\subset G : \vert S \vert=n \rbrace$とする。作用$G\curvearrowright G_{n}$が$g\cdot S:=gS=\lbrace gs : s\in S \rbrace$で定まる。

__命題__ （Cayley）群$G$は対称群$\mathrm{Sym}G$の部分群に同型である。

（証明）作用$G\curvearrowright G$を$g\cdot a=ga$で定める。対応する準同型$\phi\colon G\rightarrow\mathrm{Sym}G$が単射であることを示せばよい。そこで任意の$a\in G$について$ga=a$が成り立つとする。特に$g=g1_{G}=1_{G}$より$g$は単位元となる。$\square$

__定義__ $G\curvearrowright X$を群の作用とする。

- $G\rightarrow\mathrm{Sym}X$が単射のとき、$G\curvearrowright X$は **効果的** （effective）という。
- 任意の$x, y\in X$に対して、ある$a\in G$が存在して$ax=y$が成り立つとき、$G\curvearrowright X$は **推移的** （transitive）という。




## 有限群と作用

以下$G$は有限群とする。

__補題__ $G\curvearrowright X$を作用とする。$x, y\in X$に対して関係$x\sim y$を、ある$a\in G$が存在して$ax=y$のとき定める。以下が成り立つ。

- 関係$\sim$は$X$上の同値関係であり、$x\in X$の同値類は$\mathrm{Orb}_{x}$である。
- $g\in G, x\in X$について$g^{-1}( \mathrm{Stab}_{gx} )g=\mathrm{Stab}_{x}$が成り立つ。よって$x\sim y$なら固定群の位数は一致する。
- $x\in X$について$\vert \mathrm{Orb}_{x} \vert=(G : \mathrm{Stab}_{x})$が成り立つ。特に$\vert G \vert=\vert\mathrm{Orb}_{x}\vert\cdot\vert \mathrm{Stab}_{x} \vert$である。

（証明）一番上は明らか。$a\in\mathrm{Stab}_{gx}$なら$agx=gx$であり$g^{-1}ag\in\mathrm{Stab}_{x}$を得る。逆も同様。最後は$H:=\mathrm{Stab}_{x}$として全射$G\ni a\mapsto aH$を考える。$ax=bx$なら$b^{-1}a\in H$より$a\theta_{H}b$となるから、$aH\neq bH$なら$ax\neq bx$である。逆も同様なので$\mathrm{Orb}_{x}\ni ax\mapsto aH$は全単射である。残りの等式はラグランジュの定理より従う。$\square$

__命題__ $H, K\lt G$を部分群とする。このとき$\vert H \vert\cdot\vert K \vert=\vert HK \vert\cdot\vert H\cap K \vert$が成り立つ。

（証明）作用$H\times K\curvearrowright HK$を$(h, k)\cdot x:=hxk^{-1}$で定める。$\mathrm{Orb}_{1_{G}}=HK$だから

$$
\vert HK \vert=\vert \mathrm{Orb}_{1_{G}} \vert=(H\times K : \mathrm{Stab}_{1_{G}})
$$

となる。一方$\mathrm{Stab}_{1_{G}}=\lbrace (h, k)\in H\times K : h=k \rbrace$より$H\cap K$と集合として同型になる。ラグランジュの定理より

$$
\vert H \vert\cdot\vert K \vert=\vert H\times K \vert=(H\times K : \mathrm{Stab}_{1_{G}})\vert \mathrm{Stab}_{1_{G}} \vert=\vert HK \vert\cdot\vert H\cap K \vert
$$

となる。$\square$

__定理__ （orbit counting lemma）群の作用$G\curvearrowright X$が軌道を$r$個持つとする。このとき

$$
r=\frac{1}{\vert G \vert}\sum_{a\in G}\vert X^{a} \vert
$$

が成り立つ。

> バーンサイドの補題とも呼ばれるがBurnsideは著書に掲載しただけらしい。実際はCauchyとFrobeniusに依るので、コーシー・フロベニウスの数え上げとも呼ぶ。

（証明）$\lbrace (a, x)\in G\times X : ax=x \rbrace$を二通りで数え上げる。まず$a\in G$を固定すると$x$として$X^{a}$の元が取れるので濃度は$\sum_{a\in G}\vert X^{a} \vert$となる。一方で$x\in X$を固定すると$a$として$\mathrm{Stab}_{x}$の元が取れる。よって濃度は

$$
\sum_{x\in X}\vert \mathrm{Stab}_{x} \vert=\sum_{x\in X}\frac{\vert G \vert}{\vert \mathrm{Orb}_{x} \vert}=\vert G \vert\sum_{x\in X}\frac{1}{\vert \mathrm{Orb}_{x} \vert}
$$

となる。右辺の和の部分は、各軌道上で$1$を取るので$r$と等しい。$\square$