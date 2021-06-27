
# 位相正則性

位相正則性とは可測集合が開集合とコンパクト集合により近似されることを主張する概念である。

__定義__ $(X, \mathcal{O})$は位相空間、$\mu:\mathscr{A}\rightarrow [0, \infty]$は測度とする。以下$\mathcal{K}$はコンパクト集合全体とする。

- $A\in\mathscr{A}$について$\mu (A)=\sup\lbrace \mu (K) : K\subset A, K\in\mathcal{K}\cap\mathscr{A} \rbrace$のとき$\mu$ **内部正則**（inner regular）という。
- $A\in\mathscr{A}$について$\mu (A)=\inf\lbrace \mu (U) : A\subset U, U\in\mathcal{O}\cap\mathscr{A} \rbrace$のとき$\mu$ **外部正則** （outer regular）という。特に$A, X\setminus A$が$\mu$外部正則のとき、$\mu$両側外部正則（two-sided outer regular）という。
- $A\in\mathscr{A}$について$\mu$内部正則かつ$\mu$外部正則であるとき$\mu$ **正則** （regular）という。
- 任意の$A\in\mathscr{A}$が$\mu$内部正則（resp. $\mu$外部正則、$\mu$両側外部正則、$\mu$正則）のとき$\mu$は内部正則（resp. 外部正則、両側外部正則、正則）という。

　特に$\sigma\lbrack \mathcal{O} \rbrack\subset\mathscr{A}$のとき、$A\in\mathscr{A}$が$\mu$外部正則であることと、任意の$\varepsilon>0$に対して開集合$G$が存在して$A\subset G, \mu (G\setminus A)=0$であることは同値になる。そこで$\mu$外部正則な集合全体を$\mathscr{A}_{+}$と表す。また両側$\mu$外部正則な集合全体を$\mathscr{A}_{0}$と書く。$A\in\mathscr{A}$が両側$\mu$外部正則であることと、任意の$\varepsilon>0$に対して開集合$G$と閉集合$F$が存在して$F\subset A\subset G, \mu (G\setminus F)\lt\varepsilon$とできることは同値である。

　以下$\sigma\lbrack \mathcal{O} \rbrack\subset\mathscr{A}$であるとする。

__命題__ $\mathscr{A}_{+}$は可算和で閉じる。

（証明）$\lbrace A_{n} \rbrace\subset\mathscr{A}_{+}, A:=\bigcup A_{n}$とする。$\varepsilon\gt 0$に対して開集合$G_{n}$を$A_{n}\subset G_{n}$かつ

$$
\mu (G_{n}\setminus A_{n})\lt\frac{\varepsilon}{2^{n}}
$$

を満たすように取れる。$G:=\bigcup G_{n}$と置けば開集合で$G\setminus A\subset\bigcup G_{n}\setminus A_{n}$であるから$\mu (G\setminus A)\le\sum\mu (G_{n}\setminus A_{n})\lt\varepsilon$が成り立つ。故に$A\in\mathscr{A}_{+}$を得る。$\square$

　開集合の加算交叉で表される集合を$G_{\delta}$-集合または内極限集合と言った。同様に閉集合の加算和で表される集合を$F_{\sigma}$集合と言う。

__定義__ 任意の閉集合が$G_{\delta}$集合であるとき、その位相空間は$G_{\delta}$空間と呼ぶ。

例えば距離空間$(X, \rho)$は$G_{\delta}$空間である。実際開集合$O$に対して

$$
F_{n}:=\left\lbrace x\in X\mid \rho(x, X\setminus O)\le\frac{1}{n} \right\rbrace
$$

と定めれば$F_{n}$は閉集合で、かつ$O=\bigcup F_{n}$と表せる。

__命題__ $\mu$が有限なら$\mathscr{A}_{+}$は可算交叉で閉じる。特に位相空間$(X, \mathcal{O})$が$G_{\delta}$空間なら$\mathcal{O}\subset\mathscr{A}_{0}$が成り立つ。このとき$\mathscr{A}_{0}$は$\sigma$加法族だから$\sigma\lbrack \mathcal{O} \rbrack\subset\mathscr{A}_{0}$が成り立つ。

<!--
\begin{Proof}
$\mu$は有限とする。$\{A_{n}\}\subset\mathscr{A}_{+}, A:=\bigcap A_{n}$とする。
$\varepsilon>0$に対して開集合$G_{n}$を$A_{n}\subset G_{n}$かつ
\[ \mu (G_{n}\setminus A_{n})<\frac{\varepsilon}{2^{n+1}} \]
を満たすように取れる。$G:=\bigcap G_{n}\in\mathscr{A}$と置く。
ここで$H_{n}:=\bigcap_{j=1}^{n}G_{j}$は$A$を含む開集合であって$H_{n}\searrow G$を満たす。
$\mu$は有限だから測度の減少列連続性より、ある番号$N$が存在して
\[ \mu (H_{N}\setminus G)<\frac{\varepsilon}{2} \]
を満たす。$G\setminus A\subset \bigcup (G_{n}\setminus A_{n})$であるから
\[ \mu (H_{N}\setminus A)\le\mu (H_{N}\setminus G)+\mu (G\setminus A)
<\frac{\varepsilon}{2}+\sum\mu (G_{n}\setminus A_{n})\le\varepsilon \]
を得る。

　$\mathcal{O}\subset\mathscr{A}_{+}$は明らか。$X\setminus O$は閉集合だから、$G_{\delta}$-空間の定義により可算個の開集合$O_{n}$を用いて
$X\setminus O=\bigcap O_{n}$と表せる。故に$X\setminus O\in\mathscr{A}_{+}$なので$\mathcal{O}\subset\mathscr{A}_{0}$を得る。
$\mathscr{A}_{0}$は$\sigma$-加法族になるので$\sigma[\mathcal{O}]\subset\mathscr{A}_{0}$が分かる。
\end{Proof}

\begin{Prop}
測度$\mu$に対し、ある$\{B_{n}\}\subset\mathcal{O}$が存在して$B_{n}\nearrow X, \mu (B_{n})<\infty$を満たすとする。
このとき$\sigma[\mathcal{O}]\subset\mathscr{A}_{0}$が成り立つ。
\end{Prop}
\begin{Proof}
$B\in\mathscr{A}$に対して$\mu_{n}(B):=\mu (B\cap B_{n})$と定めると$\mu_{n}:\mathscr{A}\rightarrow [0, \infty]$は有限測度となる。
$A\in\sigma[\mathcal{O}]$及び$\varepsilon>0$を取る。このとき$A\cap B_{n}\in\sigma[\mathcal{O}]\subset\mathscr{A}$である。
$G, H\in\mathcal{O}$として$A\cap B_{n}\subset G, X\setminus (A\cap B_{n})\subset H$かつ
$\mu_{n}(G\setminus (A\cap B_{n})), \mu_{n}(H\setminus (X\setminus (A\cap B_{n})))<\varepsilon$を満たすように取れる。
ここで$G_{n}:=G\cap B_{n}, H_{n}:=H\cap B_{n}$と置くと$G_{n}, H_{n}\in\mathcal{O}$であり、
$\mu (G_{n}\setminus (A\cap B_{n})), \mu (H_{n}\setminus (X\setminus (A\cap B_{n})))<\varepsilon$を満たす。
故に$A\cap B_{n}\in\mathscr{A}_{0}\subset\mathscr{A}_{+}$が従う。ここで$\mathscr{A}_{+}$は可算和で閉じるから
$A=\bigcup (A\cap B_{n})\in\mathscr{A}_{+}$を得る。一方$X\setminus A\in\sigma[\mathcal{O}]\subset\mathscr{A}_{+}$であるから
結局$A\in\mathscr{A}_{0}$を得る。
\end{Proof}

　完備化との関係を見る。

\begin{Prop}
$(X, \mathcal{O})$は$G_{\delta}$-空間、$\mu:\mathscr{A}\rightarrow [0, \infty]$は
$\sigma[\mathcal{O}]\subset\mathscr{A}_{0}$なる測度とする。
$(\mathscr{A}^{\mu}, \mu^{*})$を$(\mathscr{A}, \mu)$の完備化とすると、
$A\in\sigma[\mathcal{O}]^{\mu}$は両側$\mu^{*}$-外部正則となる。つまり$\sigma[\mathcal{O}]^{\mu}\subset\mathscr{A}_{0}$となる。
\end{Prop}
\begin{Proof}
$A_{0}, A_{1}\in\sigma[\mathcal{O}]$を$A_{0}\subset A\subset A_{1}$かつ$\mu (A_{1}\setminus A_{0})=0$であるように取れる。
$A_{j}\in\mathscr{A}_{0}$より閉集合$F$及び開集合$G$を
\[ F\subset A_{0}, A_{1}\subset G, \mu (A_{0}\setminus F), \mu (G\setminus A_{1})<\frac{\varepsilon}{2} \]
となるように取れる。故に
\[ F\subset A\subset G, \mu^{*}(G\setminus F)=\mu (G\setminus F)
=\mu (G\setminus A_{1})+\mu (A_{1}\setminus A_{0})+\mu (A_{0}\setminus F)<\varepsilon \]
が成り立つ。
\end{Proof}

　距離空間$(X, \rho)$の開集合全体を$\mathcal{O}_{\rho}$とし、この上のボレル集合体を$\mathscr{B}(X):=\sigma[\mathcal{O}_{\rho}]$と書く。
この上の測度$\mu:\mathscr{B}(X)\rightarrow [0, \infty]$に対して
\[ B\in\mathscr{B}(X)\textup{が有界なら}\mu (B)<\infty \]
という条件を加える。このとき例えば適当な点$a\in X$を取り、$B_{n}:=\{x\in X\mid \rho (x, a)<n\}$と置けば$B_{n}$は開集合でかつ
$B_{n}\nearrow X, \mu (B_{n})<\infty$を満たすので、$\mu$は両側外部正則であり、更に先の命題により$\mu^{*}$も両側外部正則となる。

　一方で内部正則性は単純には従わず、更なる条件を付け加える必要となる。
事実として完備距離空間において全有界かつ閉な集合はコンパクトになる。
\footnote{$K\subset X$が全有界とは、任意の$\delta>0$に対し有限個の半径$\delta$の開球で覆えることであった。}

\begin{Thm}[ウラム]
$X$が可分、即ち稠密な加算部分集合を持つとする。$A\in\mathscr{B}(X)^{\mu}$は両側$\mu^{*}$-外部正則であるから$\varepsilon>0$に対し
閉集合$F$及び開集合$G$が$F\subset A\subset G, \mu (G\setminus F)<\varepsilon$を満たすように取れた。
このとき$\mu^{*}(A)<\infty$なら上記の閉集合$F$として全有界なものが取れる。更に$X$が距離空間として完備なら$F$はコンパクトに取れる。
\end{Thm}
\begin{Proof}
$G\in\mathcal{O}$が$\mu (G)<\infty$を満たすとき、任意の$\varepsilon>0$に対して
全有界な閉集合$K$を$K\subset G, \mu (G\setminus K)<\infty$が取れることを示す。
$X$は可分なので、稠密な可算部分集合$D$を持つ。ここで$n\in\mathbb{N}$に対し
\[ I_{n}:=\left\{(x, m)\in D\times\mathbb{N}\mid m\ge n, \overline{B}(x; \frac{1}{m})\right\} \]
と定める。ただし$\overline{B}(x; r)$は$x$を中心とする半径$r$以下の元全体とする。
また$I_{n}$の有限部分集合列$I_{n}(l)\nearrow I_{n}$を取る。
\[ G=\bigcup_{(x, m)\in I_{n}}\overline{B}(x; \frac{1}{m}) \]
が成り立つことに注意すると、任意の$\varepsilon>0$及び$n$に対し、$l_{n}\in\mathbb{N}$が存在して
\[ K_{n}:=\bigcup_{(x, m)\in I_{n}(l_{n})}\overline{B}(x; \frac{1}{m}) \]
と置けば
\[ \mu (G)<\mu (K_{n})+\frac{\varepsilon}{2^{n}} \]
を満たすように取れる。$K:=\bigcap K_{n}$は全有界であり、また閉集合でもある。
特に$K\subset G$かつ$\mu (G\setminus K)\le\sum\mu (G\setminus K_{n})<\varepsilon$を満たす。
この$K$は$X$が完備なら先に述べた事実よりコンパクトになる。

　$A\in\mathscr{B}(X)^{\mu}$は$\mu^{*}(A)<\infty$を満たすとする。$\varepsilon>0$に対し閉集合$F$及び開集合$G$を取り、
\[ F\subset A\subset G, \mu (G\setminus F)<\frac{\varepsilon}{2} \]
を満たすようにできる。このとき
\[ \mu (G)=\mu (G\setminus F)+\mu (F)<\frac{\varepsilon}{2}+\mu^{*}(A)<\infty \]
であるから、先に述べたことより全有界かつ閉な$K\subset G$を
\[ \mu (G\setminus K)<\frac{\varepsilon}{2} \]
となるように取れる。$F\cap K\subset A$は全有界かつ閉で、
$\mu (G\setminus (F\cap K))\le \mu (G\setminus F)+\mu (G\setminus K)<\varepsilon$
を満たす。特に$X$が完備なら$K$がコンパクトだから$F\cap K$もコンパクトになる。　
\end{Proof}

\begin{Cor}
可分な完備距離空間上の測度$\mu:\mathscr{B}(X)\rightarrow [0, \infty]$が
有界な$B\in\mathscr{B}(X)$に対して$\mu (B)<\infty$を満たすとする。
このとき$\mu, \mu^{*}$は正則である。
\end{Cor}
\begin{Proof}
以下コンパクト集合全体を$\mathcal{K}$と書く。距離空間はハウスドウルフ空間でもあるのでコンパクト集合は閉集合でもある。
$A\in\mathscr{B}(X)^{\mu}$とする。$\sup_{A\supset K\in\mathcal{K}}\mu^{*}(K)\ge\mu^{*}(A)$を示せば十分である。
$\mu^{*}(A)<\infty$ならコンパクトな$F$を取り$\mu^{*}(A)=\mu (F)+\mu^{*}(A\setminus F)<\mu (F)+\varepsilon$と出来るので従う。
$\mu^{*}(A)=\infty$のときは単に閉集合として$F$が取れるが、
\[ \mu^{*}(F)=\mu (F)\ge\mu (A_{0})=\mu^{*}(A)=\infty \]
である。$\overline{B_{n}}\cap F$は有界閉集合だが$X$は完備距離空間なのでコンパクトになる。
これは$F$への増大列となるので結局$\mu^{*}$の増大列連続性より$\sup_{A\supset K\in\mathcal{K}}\mu^{*}(K)=\infty$となる。
\end{Proof}
-->