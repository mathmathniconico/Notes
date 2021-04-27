
# 外測度

__定義__ $\emptyset\in\mathscr{G}\subset 2^{S}$とする。集合函数$\mu\colon\mathscr{G}\rightarrow\lbrack 0, \infty \rbrack$について以下を定める。

- $A, B\in\mathscr{G}$について$A\subset B$なら$\mu( A )\le\mu( B )$のとき **単調** （monotone）という。
- $A_{1}, \dotsc, A_{m}\in\mathscr{G}$について$A:=\bigcup_{i=1}^{m}A_{i}\in\mathscr{G}$なら$\mu( A )\le\sum_{i=1}^{m}\mu( A_{i} )$のとき **有限劣加法的** （finite-subadditive）という。
- $\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$について$A:=\bigcup_{n\in\mathbb{N}} A_{n}\in\mathscr{G}$なら$\mu( A )\le\sum_{n\in\mathbb{N}}\mu( A_{n} )$のとき **可算劣加法的** （countable-subadditive）という。

> $\sigma$加法族上の測度は上記の性質を全て満たしている。

__定義__ 集合函数$\mu\colon 2^{S}\rightarrow\lbrack 0, \infty \rbrack$は正値、単調、可算劣加法的とする。このとき$\mu$を **外測度** （outer measure）と呼ぶ。

> カラテオドリ（Caratheodory's）の外測度とも呼ばれる。

測度の概念については、ユークリッド空間$\mathbb{R}^{n}$上の$n$次元体積が念頭にあることは言うまでもない。まず矩形に対し、各辺の長さの積をその体積とする。一般の図形についてはいくつかの矩形で覆い、その体積の総和の下限を取ることで「外側の体積」を定義する。

__定義__ $\emptyset\in\mathscr{E}\subset 2^{S}$とする。$A\subset S$について、$\mathscr{C}\subset\mathscr{E}$が可算かつ$A\subset\bigcup_{C\in\mathscr{C}}C$を満たすとき、$\mathscr{C}$を$A$の **被覆** （covering）と呼ぶ。

__補題__ $\emptyset\in\mathscr{E}\subset 2^{S}$とする。集合函数$\mu_{0}\colon\mathscr{E}\rightarrow\lbrack 0, \infty \rbrack$は正値とする。更に集合函数$\mu\colon 2^{S}\rightarrow\lbrack 0, \infty \rbrack$を以下で定める。

- $A\subset S$が$\mathscr{E}$の可算個の元で覆えないとき$\mu(A):=\infty$とする。
- $A\subset S$が被覆を持つとき、被覆$\mathscr{C}$に関する$\sum_{C\in\mathscr{C}}\mu_{0}(C)$の下限を$\mu(A)$とする。

このとき$\mu$は外測度となる。

（証明）$\mathscr{C}=\lbrace \emptyset \rbrace$を取れば$\emptyset$の被覆となるから$\mu( \emptyset )\le\mu_{0}( \emptyset )=0$より$\mu$は正値である。

$A\subset B$に対して$B$の被覆は$A$の被覆でもあるから単調性を得る。

可算劣加法的であることを示すために$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset 2^{S}$を取り$A:=\bigcup_{n\in\mathbb{N}}A_{n}$とする。ある$A_{n}$に被覆が存在しなければ$A$の被覆も存在せず、$\infty \le \infty$となり主張は正しい。全ての$A_{n}$に被覆が存在するとしてよい。$\varepsilon\gt 0$とする。下限の定義より$A_{n}$の被覆$\mathscr{C}_{n}$を、

$$
\sum_{C\in\mathscr{C}_{n}}\mu_{0}( C )\le\mu( A_{n} )+\frac{\varepsilon}{2^{n}}
$$

を満たすように取れる。このとき$\mathscr{C}=\bigcup_{n\in\mathbb{N}}\mathscr{C}_{n}$は$A$の被覆なので

$$
\begin{aligned}
\mu( A ) &\le \sum_{C\in\mathscr{C}}\mu_{0}( C ) \le \sum_{n\in\mathbb{N}}\sum_{C\in\mathscr{C}_{n}}\mu_{0}( C ) \\
&\le \sum_{n\in\mathbb{N}}\left( \mu( A_{n} )+\frac{\varepsilon}{2^{n}} \right) = \sum_{n\in\mathbb{N}}\mu( A_{n} )+\varepsilon
\end{aligned}
$$

となる。$\varepsilon$は任意だから$\mu( A )\le\sum_{n\in\mathbb{N}}\mu( A_{n} )$を得る。$\square$

__注意__ 一般に$E\in\mathscr{E}$なら$\lbrace E \rbrace$が$E$の被覆となるので$\mu( E )\le\mu_{0}( E )$が成り立つ。

補題の方法で定義された外測度を$\mu_{0}\colon\mathscr{E}\rightarrow\lbrack 0, \infty \rbrack$から誘導された外測度と呼ぶこともある。この値については次の特徴付けがある。

__命題__ $\emptyset\in\mathscr{E}\subset 2^{S}$とする。$\mu$を$\mu_{0}\colon\mathscr{E}\rightarrow\lbrack 0, \infty \rbrack$から誘導された外測度とする。このとき$B\subset S$について

$$
\mu( B )=\inf\lbrace \mu( A ) : A\in\sigma\lbrack \mathscr{E} \rbrack, B\subset A \rbrace
$$

が成り立つ。更にこの式を実現する$A\in\sigma\lbrack \mathscr{E} \rbrack$が存在する。

（証明）$A\in\sigma\lbrack \mathscr{E} \rbrack$とする。$B\subset A$なら外測度の単調性より$\mu( B )\le\mu( A )$を得る。右辺の下限を取れば

$$
\mu( B )\le\inf\lbrace \mu( A ) : A\in\sigma\lbrack \mathscr{E} \rbrack, B\subset A \rbrace
$$

を得る。

逆を示す。$\mu( B )\lt\infty$としてよい。$\mathscr{C}\subset\mathscr{E}$を$B$の被覆とすると$\sigma$加法性より$B\subset\bigcup_{C\in\mathscr{C}}C\in\sigma\lbrack \mathscr{E} \rbrack$となる。$A$として$\bigcup_{C\in\mathscr{C}}C$を取れば

$$
\inf\lbrace \mu( A ) : A\in\sigma\lbrack \mathscr{E} \rbrack, B\subset A \rbrace \le \mu\left( \bigcup_{C\in\mathscr{C}}C \right) \le \sum_{C\in\mathscr{C}}\mu( C ) \le \sum_{C\in\mathscr{C}}\mu_{0}( C )
$$

を得る。被覆に関する下限を取れば

$$
\inf\lbrace \mu( A ) : A\in\sigma\lbrack \mathscr{E} \rbrack, B\subset A \rbrace\le\mu( B )
$$

を得る。

以上より$\lbrace A_{n} \rbrace\subset\sigma\lbrack \mathscr{E} \rbrack$を$B\subset A_{n}$かつ$\mu( A_{n} )\searrow\mu( B )$を満たすように取れる。このとき$A:=\bigcap_{n\in\mathbb{N}}A_{n}\in\sigma\lbrack \mathscr{E} \rbrack$とすれば$B\subset A\subset A_{n}$より単調性から$\mu( B )\le\mu( A )\le\mu( A_{n} )$を得る。特に右辺は$\mu( B )$へ収束するから$\mu( B )=\mu( A )$となる。$\square$




## 外測度による測度の構成

__定義__ $\mu\colon 2^{S}\rightarrow\lbrack 0, \infty \rbrack$を外測度とする。$A\subset S$は以下を満たすとする。

- 任意の$E\subset S$について$\mu( E )=\mu( E\cap A )+\mu( E\backslash A )$が成り立つ。

このとき$A$はカラテオドリ可測、あるいは$\mu$可測であるという。

> 次の定義を導入したことがカラテオドリの偉大さだろう。元の着想はルベーグに依るらしく、ルベーグ自身は$E$として矩形を考えていたそうだ。私自身はこの定義についてよく理解していない。

ところで$E=( E\cap A )\cup( E\backslash A )$であるから、外測度の可算劣加法性より$\mu( E )\le\mu( E\cap A )+\mu( E\backslash A )$は常に成り立つ。つまりカラテオドリ可測であることを示すには$\mu( E )\ge\mu( E\cap A )+\mu( E\backslash A )$を示せば十分である。

__補題__ $A, B\subset S$とする。$A$がカラテオドリ可測なら、任意の$E\subset S$について

$$
\mu( E\cap( A\cup B ) ) = \mu( E\cap A )+\mu( ( E\backslash A )\cap B )
$$

が成り立つ。特に$A, B$が互いに素なら

$$
\mu( E\cap( A\sqcup B ) ) = \mu( E\cap A )+\mu( E\cap B )
$$

が成り立つ。

（証明）$A$をカラテオドリ可測とする。$E\subset S$とすると

$$
\begin{aligned}
\mu( E\cap( A\cup B ) ) &= \mu( ( E\cap( A\cup B ) )\cap A ) + \mu( ( E\cap( A\cup B ) )\backslash A ) \\
&= \mu( E\cap A )+\mu( ( E\backslash A )\cap B )
\end{aligned}
$$

より従う。$\square$

__定理__ 外測度$\mu\colon 2^{S}\rightarrow\lbrack 0, \infty \rbrack$について$\mathscr{M}_{\mu}$をカラテオドリ可測な集合全体とする。このとき$\mathscr{M}_{\mu}$は$\sigma$加法族であり、$\mu$の$\mathscr{M}_{\mu}$への制限は可測空間$( S, \mathscr{M}_{\mu} )$上の測度である。

（証明）まず$E\subset S$について$\mu( E\cap\emptyset )+\mu( E\backslash\emptyset )=\mu( \emptyset )+\mu( E )=\mu( E )$より$\emptyset$はカラテオドリ可測である。また$A$がカラテオドリ可測なら

$$
\mu( E\cap( S\backslash A ) )+\mu( E\backslash( S\backslash A ) ) = \mu( E\backslash A )+\mu( E\cap A )=\mu( E )
$$

より$S\backslash A$もカラテオドリ可測となる。

次に$\mathscr{M}_{\mu}$が有限和に関して閉じていることを述べる。$A, B$をカラテオドリ可測とすると、補題より任意の$E\subset S$について

$$
\mu( E\cap( A\cup B ) ) = \mu( E\cap A )+\mu( ( E\backslash A )\cap B )
$$

が成り立つ。$E\backslash( A\cup B )=(E\backslash A )\backslash B$及び$A, B$が$\mu$可測であることを用いると

$$
\begin{aligned}
\mu( E\cap ( A\cup B ) )+\mu( E\backslash( A\cup B ) ) &= \mu( E\cap A )+\mu( ( E\backslash A )\cap B )+\mu( ( E\backslash A )\backslash B ) \\
&= \mu(E\cap A)+\mu(E\backslash A) \\
&= \mu(E)
\end{aligned}
$$

を得る。従って$A\cup B$はカラテオドリ可測となる。

> 以上より$\mathscr{M}_{\mu}$は後述する有限加法族であることが分かる。特に有限加法族$\mathscr{A}$は有限交叉や差集合で閉じている。実際$A, B\in\mathscr{A}$に対して$S=S\backslash \emptyset\in\mathscr{A}$であり、$A\cap B=A\backslash( S\backslash B )\in\mathscr{A}$であり、$A\backslash B=S\backslash( ( S\backslash A )\cup B )\in\mathscr{A}$である。

さて$\mu$の$\mathscr{M}_{\mu}$への制限を$\nu$とする。このとき$\nu\colon\mathscr{M}_{\mu}\rightarrow\lbrack 0, \infty \rbrack$は有限加法的である。実際、互いに素な$A, B\in\mathscr{M}_{\mu}$について、補題より任意の$E\subset S$について

$$
\mu( E\cap( A\sqcup B ) ) = \mu( E\cap A )+\mu( E\cap B )
$$

が成り立つ。特に$E=S$と置けば

$$
\nu( A\sqcup B )=\mu( A\sqcup B )=\mu( A )+\mu( B )=\nu( A )+\nu( B )
$$

を得る。$\mathscr{M}_{\mu}$は有限加法族なので二つずつ考えれば$\nu$が有限加法的であることも分かる。

ここで$\mathscr{M}_{\mu}$が$\sigma$加法族であることを示そう。$\lbrace A_{n} \rbrace\subset\mathscr{M}_{\mu}$とする。$B_{m}:=\bigcup_{n=1}^{m}A_{n}$と置けば、$B_{m}$はカラテオドリ可測であり$B_{m}\nearrow\bigcup_{n\in\mathbb{N}}A_{n}=\colon B$である。ここで

$$
C_{1}:=B_{1}, C_{n}:=B_{n}\backslash B_{n-1}
$$

と定めれば$C_{n}$もカラテオドリ可測であり、$B_{m}=\bigsqcup_{n=1}^{m}C_{n}$と非交叉和で表せる。補題より任意の$E\subset S$に対して

$$
\mu( E\cap B_{m} )=\sum_{n=1}^{m}\mu( E\cap C_{n} )
$$

が成り立つ。単調性より$\mu( E\backslash B )\le\mu( E\backslash B_{m} )$だから、$B_{m}$の$\mu$可測性より

$$
\mu( E )=\mu( E\cap B_{m} )+\mu( E\backslash B_{m} )\ge\sum_{n=1}^{m}\mu( E\cap C_{n} )+\mu( E\backslash B )
$$

となる。$m$は任意だから$\mu( E )\ge\sum_{n\in\mathbb{N}}\mu( E\cap C_{n} )+\mu( E\backslash B )$となる。ここで

$$
E\cap B=\bigcup_{n\in\mathbb{N}}( E\cap C_{n} )
$$

だから、外測度の可算劣加法性より$\sum_{n\in\mathbb{N}}\mu( E\cap C_{n} )\ge\mu( E\cap B )$を得る。従って$\mu( E )\ge\mu( E\cap B )+\mu( E\backslash B )$となり、これは$B$がカラテオドリ可測であることを意味している。

最後に$\nu$が可算加法的であることを示そう。$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{M}_{\mu}$は互いに素とする。$\mathscr{M}_{\mu}$は$\sigma$加法族であるから$A:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\mathscr{M}_{\mu}$である。外測度の可算劣加法性より

$$
\nu(A)=\mu\left( \bigsqcup_{n\in\mathbb{N}}A_{n} \right)\le\sum_{n\in\mathbb{N}}\mu( A_{n} )=\sum_{n\in\mathbb{N}}\nu( A_{n} )
$$

である。また単調性及び$\nu$が有限加法的であることから

$$
\nu( A )=\mu\left( \bigsqcup_{n\in\mathbb{N}}A_{n} \right)\ge\mu\left( \bigsqcup_{n=1}^{m}A_{n} \right)=\nu\left( \bigsqcup_{n=1}^{m}A_{n} \right)=\sum_{n=1}^{m}\nu( A_{n} )
$$

である。$m$は任意だから$\nu( A )\ge\sum_{n\in\mathbb{N}}\nu( A_{n} )$を得る。$\square$