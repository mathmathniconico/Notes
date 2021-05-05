
# 半加法族


ホップの拡張定理により、有限加法族上の前測度を$\sigma$加法族上の測度へと拡張できる条件が分かった。しかし有限加法族上の前測度でさえ簡単には与えることができない。そこでより単純な集合族のクラスとその上の前測度から、有限加法族上の前測度を構成すること、および$\sigma$加法族上の測度へと拡張することを考えたい。

まず有限加法族の生成について述べる。有限加法族も$\sigma$加法族と同様に、任意の交叉で有限加法族となる。

__定義__ $\mathscr{G}\subset 2^{S}$とする。$\mathscr{G}$を含む$S$上の有限加法族全体の交叉を$\sigma_{0}\lbrack \mathscr{G} \rbrack_{S}$あるいは単に$\sigma_{0}\lbrack \mathscr{G} \rbrack$で記し、$\mathscr{G}$により$S$上で生成された有限加法族と呼ぶ。

> 特に$\sigma_{0}\lbrack \mathscr{G} \rbrack$は$\mathscr{G}$を含む最小の有限加法族となる。

__定義__ $\mathscr{S}\subset 2^{S}$は次の3条件を満たすとする。

- $\emptyset\in\mathscr{S}$である。
- $A, B\in\mathscr{S}$なら$A\cap B\in\mathscr{S}$である。
- $A\in\mathscr{S}$なら有限個の互いに素な元$A_{1}, \dotsc, A_{n}\in\mathscr{S}$を用いて$S\setminus A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。

このとき$\mathscr{S}$を$S$上の **半加法族** （semi-additive family of sets）と呼ぶ。

この定義の出処は拡張定理の証明にある。証明の中で$\lbrace C\cap A \rbrace, \lbrace C\setminus A \rbrace$が$E\cap A, E\setminus A$の被覆であることを示すのに有限加法族の性質を用いた。そこで$C\setminus A=C\cap( S\setminus A )$に注意しつつ、有限加法族の条件を緩めたのが上の定義になる。被覆となるためには$S\setminus A$自身が$\mathscr{A}$の元である必要はなく、$\mathscr{A}$による有限和で表せれば良い。

> 半加法族も名前が安定しない。集合半代数などと呼ばれたこともある。

$\mathscr{S}\subset 2^{S}$を半加法族とする。$A, B\in\mathscr{S}$について、半加法族の定義より$S\setminus B=\bigsqcup_{i=1}^{m}B_{i}$と表せる。従って

$$
A\setminus B=A\cap( S\setminus B )=A\cap\bigsqcup_{i=1}^{m}B_{i}=\bigsqcup_{i=1}^{m}( A\cap B_{i} )
$$

となるが、右辺は$A\setminus B$が$\mathscr{S}$による非交叉有限和で表せることを意味している。（この性質は後で半環の節で述べる。）これより半加法族において、非自明だが面白い性質を示すことができる。

__補題__ $\mathscr{S}\subset 2^{S}$を半加法族とする。任意の$A\in\mathscr{S}$及び$A_{1}, \dotsc, A_{n}\in\mathscr{S}$に対し、互いに素な$B_{1}, \dotsc, B_{m}\in\mathscr{S}$が存在して

$$
A\setminus\bigcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}B_{j}
$$

と表せる。

（証明）上の議論より$A\setminus A_{1}=\bigsqcup_{j=1}^{m}C_{j}$なる互いに素な$\lbrace C_{j} \rbrace\subset\mathscr{S}$が取れる。$( A\setminus A_{1} )\setminus A_{2} = \bigsqcup_{j=1}^{m}( C_{j}\setminus A_{2} )$より、再び$C_{j}\setminus A_{2}=\bigsqcup_{k=1}^{m_{j}}D_{j, k}$なる互いに素な$\lbrace D_{j, k} : k=1, \dotsc, m_{j} \rbrace\subset\mathscr{S}$が取れて、$( A\setminus A_{1} )\setminus A_{2} = \bigsqcup_{j=1}^{m}\bigsqcup_{k=1}^{m_{j}}D_{j, k}$を満たす。このとき$\lbrace D_{j, k} \rbrace\subset\mathscr{S}$は互いに素である。以上を繰り返せば良い。$\square$

半加法族の生成する有限加法族は、形が良く分かる集合になっている。

__命題__ $\mathscr{S}\subset 2^{S}$を半加法族とする。このとき$\sigma_{0}\lbrack \mathscr{S} \rbrack$は$\mathscr{S}$の元の非交叉有限和で表される集合全体である。

（証明）$\mathscr{S}$の元の非交叉有限和で表される集合全体を$\mathscr{A}$とする。$\mathscr{A}\subset\sigma_{0}\lbrack \mathscr{S} \rbrack$は明らかなので逆を示そう。$\mathscr{S}\subset\mathscr{A}$より$\mathscr{A}$が有限加法族であることを示せば良い。

$\emptyset\in\mathscr{A}$は明白。$A_{i}, B_{j}\in\mathscr{S}$について$A=\bigsqcup_{i=1}^{n}A_{i}, B=\bigsqcup_{j=1}^{m}B_{j}\in\mathscr{A}$とする。$A\cap B=\bigsqcup_{i, j}A_{i}\cap B_{j}$となるが、$\mathscr{S}$は半加法族なので$A_{i}\cap B_{j}\in\mathscr{S}$である。故に$A\cap B\in\mathscr{A}$を得る。また$S\setminus A=\bigcap_{i=1}^{n}( S\setminus A_{i} )$となるが、$A_{i}\in\mathscr{S}$より$S\setminus A_{i}$は$\mathscr{S}$の元の非交叉有限和で表せる。つまり$S\setminus A_{i}\in\mathscr{A}$であり、$\mathscr{A}$は有限交叉で閉じているから$S\setminus A\in\mathscr{A}$を得る。以上より$\mathscr{A}$は有限加法族であり、生成の最小性から$\sigma_{0}\lbrack \mathscr{S} \rbrack=\mathscr{A}$を得る。$\square$




## 半加法族上の前測度

__定義__ $\mathscr{S}\subset 2^{S}$を半加法族とする。集合函数$\mu\colon\mathscr{S}\rightarrow\lbrack 0, \infty \rbrack$は正値かつ有限加法的とする。このとき$\mu$を半加法族$\mathscr{S}$上の前測度という。

> 有限加法族上の前測度のときとは違い、有限加法性は「互いに素な$A, B\in\mathscr{S}$に対して$\mu( A\sqcup B )=\mu( A )+\mu( B )$が成り立つ」と置き換えることはできない。

__命題__ $\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。次が成り立つ。

- $A\in\mathscr{S}$及び互いに素な$A_{1}, \dotsc, A_{n}\in\mathscr{S}$について$\bigsqcup_{i=1}^{n}A_{i}\subset A$なら$\sum_{i=1}^{n}\mu( A_{i} )\le\mu( A )$が成り立つ。
- $B\in\mathscr{S}$及び$B_{1}, \dotsc, B_{n}\in\mathscr{S}$について$B\subset\bigcup_{i=1}^{n}B_{i}$なら$\mu( B ) \le\sum_{i=1}^{n}\mu( B_{i} )$が成り立つ。

特に$\mu$は単調かつ有限劣加法的である。

（証明）補題より互いに素な$D_{1}, \dotsc, D_{m}\in\mathscr{S}$が存在して$A\setminus\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}D_{j}$と表せる。$\bigsqcup_{i=1}^{n}A_{i}\subset A$とする。このとき$A=\bigsqcup_{i=1}^{n}A_{i}\sqcup\bigsqcup_{j=1}^{m}D_{j}$であり、$\mu$は有限加法的であるから

$$
\mu( A )=\sum_{i=1}^{n}\mu( A_{i} )+\sum_{j=1}^{m}\mu( D_{j} )\ge\sum_{i=1}^{n}\mu( A_{i} )
$$

が成り立つ。

$B\subset\bigcup_{i=1}^{n}B_{i}$とする。$B=\bigcup_{i=1}^{n}( B\cap B_{i} )$なので、

$$
C_{i}:=( B\cap B_{i} )\setminus\bigcup_{j=1}^{i-1}( B\cap B_{j} )
$$

と置けば、$B=\bigsqcup_{i=1}^{n}C_{i}$と互いに素な和で表せる。ここで$B\cap B_{j}\in\mathscr{S}$だから、補題より互いに素な$\lbrace D_{i, j} : j=1, \dotsc, n_{i} \rbrace\subset\mathscr{S}$が存在して$C_{i}=\bigsqcup_{j=1}^{n_{i}}D_{i, j}$と表せる。$\mu$は有限加法的であり、$\bigsqcup_{j=1}^{n_{i}}D_{i, j}=C_{i}\subset B_{i}$であるから、上の結果より

$$
\mu( B )=\mu\left( \bigsqcup_{i=1}^{n}\bigsqcup_{j=1}^{n_{i}}D_{i, j} \right)=\sum_{i=1}^{n}\sum_{j=1}^{n_{i}}\mu( D_{i, j} )\le\sum_{i=1}^{n}\mu( B_{i} )
$$

が成り立つ。$\square$

半加法族$\mathscr{S}\subset 2^{S}$について$\sigma_{0}\lbrack \mathscr{S} \rbrack$は$\mathscr{S}$の元の非交叉有限和として表される集合全体であった。すなわち$A\in\sigma_{0}\lbrack \mathscr{S} \rbrack$は互いに素な$A_{1}, \dotsc, A_{n}\in\mathscr{S}$により$A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。

$\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。このとき$\sum_{i=1}^{n}\mu(A_{i})$は上記の表示に依らず決まる。実際$A=\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}B_{j}$とすると、$\mu$は有限加法的であるから

$$
\sum_{i=1}^{n}\mu( A_{i} )=\sum_{i=1}^{n}\sum_{j=1}^{m}\mu( A_{i}\cap B_{j} )=\sum_{j=1}^{m}\mu(B_{j})
$$

となる。従って集合函数$\mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$を$\mu_{0}(A):=\sum_{i=1}^{n}\mu(A_{i})$により定めることができる。

__命題__ $\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。上記の$\mu_{0}$は有限加法族$\sigma_{0}\lbrack \mathscr{S} \rbrack$上の前測度となる。

（証明）$\mu_{0}( \emptyset )=0$は明白。互いに素な$A, B\in\sigma_{0}\lbrack \mathscr{S} \rbrack$について、$A=\bigsqcup_{i=1}^{n}A_{i}, B=\bigsqcup_{j=1}^{m}B_{j}$を$\mathscr{S}$の元による非交叉有限和による表示とする。$\lbrace A_{i}, B_{j} \rbrace$も互いに素なので$A\sqcup B=\bigsqcup_{i=1}^{n}A_{i}\sqcup\bigsqcup_{j=1}^{m}B_{j}$も$\mathscr{S}$の元による非交叉有限和による表示を与える。従って

$$
\mu_{0}( A\sqcup B )=\sum_{i=1}^{n}\mu( A_{i} )+\sum_{j=1}^{m}\mu( B_{j} )=\mu_{0}( A )+\mu_{0}( B )
$$

を得る。$\square$

> $\mu$の拡張となる$\sigma_{0}\lbrack \mathscr{S} \rbrack$上の前測度は一意的である。

__補題__ $\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度、その拡張を$\mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$とする。TFAE

1. $\mu_{0}$は可算加法的である。
1. $\mu$は弱可算劣加法的である。

（証明）上から下は明らかなので逆を示そう。互いに素な$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\sigma_{0}\lbrack \mathscr{S} \rbrack$について$B:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\sigma_{0}\lbrack \mathscr{S} \rbrack$とする。$A_{n}, B\in\sigma_{0}\lbrack \mathscr{S} \rbrack$は有限集合$\mathscr{A}_{n}, \mathscr{B}\subset\mathscr{S}$により

$$
\begin{aligned}
A_{n}&=\bigsqcup_{G_{n}\in\mathscr{A}_{n}}G_{n}, & B&=\bigsqcup_{H\in\mathscr{B}}H
\end{aligned}
$$

と表せる。

さて$\mathscr{A}:=\bigcup_{n\in\mathbb{N}}\mathscr{A}_{n}\subset\mathscr{S}$は互いに素である。更に

$$
\bigsqcup_{H\in\mathscr{B}}H=B=\bigsqcup_{n\in\mathbb{N}}A_{n}=\bigsqcup_{n\in\mathbb{N}}\bigsqcup_{G_{n}\in\mathscr{A}_{n}}G_{n}=\bigsqcup_{G\in\mathscr{A}}G
$$

が成り立つ。よって$H\in\mathscr{B}$は$H=\bigsqcup_{G\in\mathscr{A}}( G\cap H )$と表せる。$\mathscr{S}$は半加法族だから$G\cap H\in\mathscr{S}$であり、仮定より$\mu( H )\le\sum_{G\in\mathscr{A}}\mu( G\cap H )$を得る。同様に$G\in\mathscr{A}$は$G=\bigsqcup_{H\in\mathscr{B}}( G\cap H )$と表せる。$\mathscr{B}$は有限集合なので$\mu$の有限加法性から$\mu( G )=\sum_{H\in\mathscr{B}}\mu( H\cap G )$を得る。以上より

$$
\begin{aligned}
\mu_{0}( B )&=\sum_{H\in\mathscr{B}}\mu( H )\le\sum_{H\in\mathscr{B}}\sum_{G\in\mathscr{A}}\mu( G\cap H ) \\
&=\sum_{G\in\mathscr{A}}\mu( G )=\sum_{n\in\mathbb{N}}\sum_{G\in\mathscr{A}_{n}}\mu( G ) \\
&=\sum_{n\in\mathbb{N}}\mu_{0}( A_{n} )
\end{aligned}
$$

となる。（ここで非負実数に関する和の順序の交換可能性を用いた。）つまり$\mu_{0}$は弱可算劣加法的である。$\mu_{0}$は有限加法族上の前測度だから、これは可算加法的であることと同値である。$\square$

> 補題より半加法族上の前測度についても可算加法性、可算劣加法性、弱可算劣加法性は全て同値となる。

__定理__ （半加法族上の前測度に対する拡張定理）$\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。TFAE

1. $\sigma\lbrack \mathscr{S} \rbrack=\sigma\lbrack \sigma_{0}\lbrack \mathscr{S} \rbrack \rbrack$上の測度$\widehat{\mu}$が存在して$\widehat{\mu}|_{\mathscr{S}}=\mu$を満たす。つまり$A\in\mathscr{S}$なら$\widehat{\mu}( A )=\mu( A )$が成り立つ。
1. $\mu$は弱可算劣加法的である。

（証明）ホップの拡張定理の証明に沿って示すことが出来る。$ \mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$を$\mu$の拡張とする。

まず外測度$\widehat{\mu}$の構成に関して、$\sigma_{0}\lbrack \mathscr{S} \rbrack$の元が$\mathscr{S}$の元の非交叉有限和で書けるので、$\mu$から誘導される外測度も$\mu_{0}$から誘導される外測度も等しい。

次に$\mathscr{S}\subset\mathscr{M}_{\widehat{\mu}}$を示したい。$A\in\mathscr{S}$及び$E\subset S$とする。$\mathscr{S}$は半加法族なので$A_{1}, \dotsc, A_{n}\in\mathscr{S}$が存在して$S\setminus A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。$\mathscr{C}\subset\mathscr{S}$を$E$の被覆とすると$\lbrace C\cap A : C\in\mathscr{C} \rbrace\subset\mathscr{S}$は$E\cap A$の被覆となる。また$C\in\mathscr{C}$について

$$
C\setminus A=C\cap( S\setminus A )=C\cap\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{i=1}^{n}( C\cap A_{i} )
$$

より$\lbrace C\cap A_{i} : C\in\mathscr{C}, i=1, \dotsc, n \rbrace\subset\mathscr{S}$は$E\setminus A$の被覆となる。よって

$$
\begin{aligned}
\widehat{\mu}( E\cap A )+\widehat{\mu}( E\setminus A ) &\le \sum_{C\in\mathscr{C}}\mu( C\cap A )+\sum_{C\in\mathscr{C}}\sum_{i=1}^{n}\mu( C\cap A_{i} ) \\
&=\sum_{C\in\mathscr{C}}\left( \mu( C\cap A )+\sum_{i=1}^{n}\mu( C\cap A_{i} ) \right)
\end{aligned}
$$

となる。ところで
$$
C=( C\cap A )\sqcup ( C\setminus A )=( C\cap A )\sqcup( C\cap A_{1} )\sqcup\dotsb\sqcup( C\cap A_{n} )
$$

より$C\in\mathscr{C}$より$\mu$の有限加法性から

$$
\mu( C\cap A )+\sum_{i=1}^{n}\mu( C\cap A_{i} )=\mu( C )
$$

が従う。

残りの部分はホップの拡張定理と同様に従う。ただし、補題より半加法族上でも$\mu$の弱可算劣加法性が可算加法性と同値であることを用いる。$\square$

