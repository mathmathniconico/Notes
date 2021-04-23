
# 有限加法族

__定義__ $S$を空でない集合とする。$\emptyset\in\mathscr{G}\subset 2^{S}$とし、$\mu\colon\mathscr{G}\rightarrow\lbrack 0, \infty \rbrack$を集合函数とする。

- 互いに素な$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$について、$A:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\mathscr{G}$なら$\mu( A )\le\sum_{n\in\mathbb{N}}\mu( A_{n} )$であるとき$\mu$は **弱可算劣加法的** （weak countable-subadditive）という。
- 互いに素な$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$について、$A:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\mathscr{G}$なら$\mu( A )\ge\sum_{n\in\mathbb{N}}\mu( A_{n} )$であるとき$\mu$は **弱可算優加法的** （weak countable-superadditive）という。
- $\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$について、$A_{n}\nearrow A\in\mathscr{G}$なら$\lim_{n\rightarrow\infty}\mu( A_{n} )=\mu( A )$であるとき$\mu$は **増大列連続** という。
- $\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$について、$A_{n}\searrow A\in\mathscr{G}, \mu( A_{1} )\lt \infty$なら$\lim_{n\rightarrow\infty}\mu( A_{n} )=\mu( A )$であるとき$\mu$は **減少列連続** であるという。

> 減少列連続は$\mu( A_{1} )\lt\infty$を仮定しているので注意。

既に外測度による測度の構成について述べた。しかしその値を具体的に求めることは難しい。そこで基本となる集合族のクラスを絞り、その上に測度の類似物を与えることで、その測度への拡張問題として捉えなおす。例えば$\mathbb{R}$上の$a$から$b$までの区間に対し$\vert b-a \vert$を対応させるようなことを考える。

前節の定理の証明中でも軽く触れたが、有限加法族とは$\sigma$加法族の条件のうち可算和を有限和に置き換えたものを満たすクラスのことである。このクラスにおいても測度の類似物を考えることができ、これを「有限加法族上の前測度」という。前測度という言葉は標語的に用いるもので、より正確を期するには「有限加法族上の正値有限加法的集合函数」と述べるべきだろう。

> 「有限加法族上の前測度」について成り立つ性質は、もちろん$\sigma$加法族上の測度に対しても成り立つ。

__定義__ $S$を集合とする。$\mathscr{A}\subset 2^{S}$は以下を満たすとする。

- $\emptyset\in\mathscr{A}$である。
- $A\in\mathscr{A}$なら$S\backslash A\in\mathscr{A}$である。
- $A, B\in\mathscr{A}$なら$A\cup B\in\mathscr{A}$である。

このとき$\mathscr{A}$は$S$上の **有限加法族** （finitary additive class）であるという。

> 有限加法族も歴史的経緯から名前が安定しない。集合代数や集合体とも呼ばれている。

- $\mathscr{A}\subset 2^{S}$を有限加法族とする。このとき$A, B\in\mathscr{A}$について$A\cap B, A\backslash B\in\mathscr{A}$が成り立つ。

__注意__ $\mu\colon\mathscr{A}\rightarrow\lbrack 0, \infty \rbrack$を有限加法族$\mathscr{A}$上の集合函数とする。TFAE

1. $\mu$は有限加法的である。
1. 互いに素な$A, B\in\mathscr{A}$について$\mu( A\sqcup B )=\mu( A )+\mu( B )$が成り立つ。

また同様に次も同値となる。

1. $\mu$は有限劣加法的である。
1. $A, B\in\mathscr{A}$について$\mu( A\cup B )\le\mu( A )+\mu( B )$が成り立つ。

> この注意は前節の定理の証明中にも暗に使用している。



## 有限加法族上の前測度

__定義__ $\mathscr{A}\subset 2^{S}$を有限加法族とする。集合函数$\mu\colon\mathscr{A}\rightarrow\lbrack 0, \infty \rbrack$が正値かつ有限加法的であるとき、$\mu$は有限加法族$\mathscr{A}$上の前測度（premeasure）あるいはジョルダン測度という。

有限加法族上の前測度は単調かつ有限劣加法的である。実際$A, B\in\mathscr{A}$について、$A\subset B$なら

$$
\mu( B )=\mu( A\sqcup( B\backslash A ) )=\mu( A )+\mu( B\backslash A )\ge\mu( A )
$$

であり、

$$
\mu( A\cup B )=\mu( A\sqcup( B\backslash A ) )=\mu( A )+\mu( B\backslash A )\le\mu( A )+\mu( B )
$$

である。

__補題__ $\mu$は有限加法族$\mathscr{A}\subset 2^{S}$上の前測度とする。TFAE

1. $\mu$は可算加法的である。
1. $\mu$は可算劣加法的である。
1. $\mu$は弱可算劣加法的である。

（証明）上から下は明白なので、一番下から一番上を示す。そのためには弱可算優加法的であることを示せば良い。互いに素な$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}$について、$A:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$とする。$\mu$は単調かつ有限加法的なので、$m$について

$$
\mu( A )\ge\mu\left( \bigsqcup_{n=1}^{m} A_{n} \right)=\sum_{n=1}^{m}\mu( A_{n} )
$$

が成り立つ。$m$は任意なので$\mu( A )\ge\sum_{n\in\mathbb{N}}\mu( A_{n} )$が成り立つ。$\square$

既に外測度から測度を構成できることを示した。更に有限加法族上の前測度に対し、その拡張となる測度を構成するための必要十分条件を得ることが出来る。

__定理__ （ホップの拡張定理）$\mu$は有限加法族$\mathscr{A}\subset 2^{S}$上の前測度とする。TFAE

- $\sigma\lbrack \mathscr{A} \rbrack$上の測度$\widehat{\mu}$が存在して$\widehat{\mu}|_{\mathscr{A}}=\mu$を満たす。つまり$A\in\mathscr{A}$なら$\widehat{\mu}( A )=\mu( A )$が成り立つ。
- $\mu$は弱可算劣加法的である。

（証明）上から下は明らか。下を仮定し、$\mu\colon\mathscr{A}\rightarrow\lbrack 0, \infty \rbrack$から誘導される外測度を$\widehat{\mu}$とする。このとき$\widehat{\mu}$可測集合全体$\mathscr{M}_{\widehat{\mu}}$は$\sigma$加法族であり、$\widehat{\mu}$はその上で測度となる。

まず$\sigma\lbrack \mathscr{A} \rbrack\subset\mathscr{M}_{\widehat{\mu}}$を示す。生成の最小性より$\mathscr{A}\subset\mathscr{M}_{\widehat{\mu}}$を示せば良いので、$A\in\mathscr{A}$がカレテオドリ可測であることを示そう。$E\subset S$と$E$の被覆$\mathscr{C}\subset\mathscr{A}$を取れば、$\mathscr{A}$は有限加法族なので

$$
\lbrace C\cap A : C\in\mathscr{C} \rbrace, \lbrace C\backslash A : C\in\mathscr{C} \rbrace\subset\mathscr{C}
$$

はそれぞれ$E\cap A, E\backslash A$の被覆となる。更に$\mu$は有限加法的だから

$$
\widehat{\mu}( E\cap A )+\widehat{\mu}( E\backslash A ) \le \sum_{C\in\mathscr{C}}( \mu( C\cap A )+\mu( C\backslash A ) ) = \sum_{C\in\mathscr{C}}\mu( C )
$$

となる。右辺の下限を取れば$\widehat{\mu}( E )$となるため、$A$はカラテオドリ可測である。

以上より$\widehat{\mu}$は$\sigma\lbrack \mathscr{A} \rbrack$上で測度となることが分かった。$\mathscr{A}$上での値を見てみよう。$A\in\mathscr{A}$に対して、定義より$\widehat{\mu}( A )\le\mu( A )$である。逆に$A$の被覆$\mathscr{C}\subset\mathscr{A}$について

$$
A= A\cap\bigcup_{C\in\mathscr{C}}C=\bigcup_{C\in\mathscr{C}}( A\cap C )
$$

となるが、補題より$\mu$の弱可算劣加法性は可算加法性、特に可算劣加法性と同値である。故に$A\cap C\in\mathscr{A}$及び単調性から

$$
\mu( A )=\mu\left( \bigcup_{C\in\mathscr{C}}( A\cap C ) \right)\le\sum_{C\in\mathscr{C}}\mu( A\cap C )\le\sum_{C\in\mathscr{C}}\mu( C )
$$

が従う。右辺の下限を取り$\mu( A )\le\widehat{\mu}( A )$を得る。$\square$

> こうして有限加法族とその上の前測度が与えられたとき、その拡張となる$\sigma$加法族とその上の測度が存在することが示された。ちなみに拡張の一意性までは言えない。

更に次も成り立つ。前測度が測度に拡張されるとき、集合族に対するある種の連続性のようなものが成り立つ。

__命題__ $\mu$は有限加法族$\mathscr{A}\subset 2^{S}$上の前測度とする。TFAE

- $\mu$は可算加法的である。
- $\mu$は増大列連続かつ減少列連続である。
- $\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}$に対し以下が成り立つ。
    - $A_{n}\nearrow A\in\mathscr{A}, \mu( A )=\infty$なら$\lim_{n\rightarrow\infty}\mu( A_{n} )=\infty$である。
    - $A_{n}\searrow \emptyset, \mu( A_{1} )\lt\infty$なら$\lim_{n\rightarrow\infty}\mu( A_{n} )=0$である。

（証明）一番上から真ん中が成り立つことを示そう。まず増大列連続であることを示す。$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}$が$A_{n}\nearrow A\in\mathscr{A}$を満たすとする。$A=A_{1}\sqcup\bigsqcup_{n\in\mathbb{N}}( A_{n+1}\backslash A_{n} )$だから、$\mu$の可算加法性より$\mu( A )=\mu( A_{1} )+\sum_{n\in\mathbb{N}}\mu( A_{n+1}\backslash A_{n} )$となる。一方$A_{n}=A_{1}\sqcup\bigsqcup_{k=1}^{n}( A_{k+1}\backslash A_{k} )$だから

$$
\lim_{n\rightarrow\infty}\mu( A_{n} )=\mu( A_{1} )+\sum_{k=1}^{\infty}\mu( A_{k+1}\backslash A_{k} )=\mu( A )
$$

を得る。次に減少列連続であることを示そう。$\lbrace B_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}$が$B_{n}\searrow B\in\mathscr{A}, \mu( B_{1} )\lt\infty$を満たすとする。$B_{n}=B\sqcup\bigsqcup_{k\ge n}( B_{k}\backslash B_{k+1} )$だから、可算加法性より特に$n=1$として$\infty\gt\mu( B_{1} )\ge\sum_{n\in\mathbb{N}}\mu( B_{n}\backslash B_{n+1} )$となる。つまり$\lim_{n\rightarrow\infty}\sum_{k\ge n}\mu( B_{k}\backslash B_{k+1} )=0$だから

$$
\lim_{n\rightarrow\infty}\mu( B_{n} )=\mu( B )+\lim_{n\rightarrow\infty}\sum_{k\ge n}\mu( B_{k}\backslash B_{k+1} )=\mu( B )
$$

を得る。

真ん中から一番下は定義より明らか。

一番下から一番上が成り立つことを示そう。$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}$は互いに素であるとし、$A:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$であるとする。$B_{m}:=\bigsqcup_{n=1}^{m}A_{n}\in\mathscr{A}$とすると$B_{m}\nearrow A$である。$\mu( A )=\infty$のとき、仮定より

$$
\mu( A )=\infty=\lim_{m\rightarrow\infty}\mu( B_{m} )=\lim_{m\rightarrow\infty}\sum_{n=1}^{m}\mu( A_{n} )=\sum_{n\in\mathbb{N}}\mu( A_{n} )
$$

となる。$\mu( A )\lt\infty$のときは、$C_{1}:=A, C_{m+1}:=A\backslash B_{m}$とすると$C_{m}\searrow\emptyset$かつ$\mu( C_{1} )=\mu( A )\lt\infty$である。特に$B_{m}\subset A$なので$\mu( C_{m+1} )=\mu( A )-\mu( B_{m} )$が成り立つ。仮定より$\lim_{m\rightarrow\infty}\mu( C_{m} )=0$だから

$$
\sum_{n\in\mathbb{N}}\mu( A_{n} )=\lim_{m\rightarrow\infty}\mu( B_{m} )=\mu( A )-\lim_{m\rightarrow\infty}\mu( C_{m+1} )=\mu( A )
$$

を得る。$\square$