
# 半加法族


ホップの拡張定理により、有限加法族上の前測度を$\sigma$加法族上の測度へと拡張できる条件が分かった。しかし有限加法族上の前測度でさえ簡単には与えることができない。そこでより単純な集合族のクラスとその上の前測度から、有限加法族上の前測度を構成すること、および$\sigma$加法族上の測度へと拡張することを考えたい。

まず有限加法族の生成について述べる。有限加法族も$\sigma$加法族と同様に、任意の交叉で有限加法族となる。

__定義__ $\mathscr{G}\subset 2^{S}$とする。$\mathscr{G}$を含む$S$上の有限加法族全体の交叉を$\sigma_{0}\lbrack \mathscr{G} \rbrack_{S}$あるいは単に$\sigma_{0}\lbrack \mathscr{G} \rbrack$で記し、$\mathscr{G}$により$S$上で生成された有限加法族と呼ぶ。

> 特に$\sigma_{0}\lbrack \mathscr{G} \rbrack$は$\mathscr{G}$を含む最小の有限加法族となる。



<!--


\subsection{半加法族}
\begin{Def}{}{}
集合$S$において$\mathscr{S}\subset 2^{S}$が次の3条件を満たすとき、$\mathscr{S}$は$S$上の半加法族であるという。
\begin{EnumCond}
\item$\emptyset\in\mathscr{S}$である。
\item$A, B\in\mathscr{S}$なら$A\cap B\in\mathscr{S}$である。
\item$A\in\mathscr{S}$なら有限個の互いに素な元$A_{1}, \dotsc, A_{n}\in\mathscr{S}$を用いて$S\backslash A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。
\end{EnumCond}
\end{Def}

この定義がどこから来るのか疑問に思うかもしれないが、一つの理由としては拡張定理の証明にある。
証明では有限加法族の性質を、まず$\lbrace C\cap A \rbrace, \lbrace C\backslash A \rbrace$が$E\cap A, E\backslash A$の被覆であることを示すのに用いた。
そこで$C\backslash A=C\cap( S\backslash A )$に注意しつつ、有限加法族の2番目の条件を緩めたのが上の定義になる。
被覆となるためには$S\backslash A$自身が$\mathscr{A}$の元である必要はなく、$\mathscr{A}$による有限和で表せればよいという発想である。

半加法族も名前が安定しない。集合半代数などと呼ばれたこともある。

$\mathscr{S}\subset 2^{S}$を半加法族とする。$A, B\in\mathscr{S}$に対し、半加法族の定義より$S\backslash B=\bigsqcup_{i=1}^{m}B_{i}$と表せる。従って
\[ A\backslash B=A\cap( S\backslash B )=A\cap\bigsqcup_{i=1}^{m}B_{i}=\bigsqcup_{i=1}^{m}( A\cap B_{i} ) \]
となるが、右辺は$A\backslash B$が$\mathscr{S}$による非交叉有限和で表せることを意味している。（この性質は後で半環の節で述べる。）これより半加法族において、非自明だが面白い性質を示すことができる。

\begin{Lem}{}{}
$\mathscr{S}\subset 2^{S}$を半加法族とする。任意の$A\in\mathscr{S}$及び$A_{1}, \dotsc, A_{n}\in\mathscr{S}$に対し、互いに素な$B_{1}, \dotsc, B_{m}\in\mathscr{S}$が存在して
\[ A\backslash\bigcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}B_{j} \]
と表せる。
\end{Lem}

\begin{proof}
（証明）上の議論より$A\backslash A_{1}=\bigsqcup_{j=1}^{m}C_{j}$なる互いに素な$\lbrace C_{j} \rbrace\subset\mathscr{S}$が取れる。
$( A\backslash A_{1} )\backslash A_{2} = \bigsqcup_{j=1}^{m}( C_{j}\backslash A_{2} )$より、
再び$C_{j}\backslash A_{2}=\bigsqcup_{k=1}^{m_{j}}D_{j, k}$なる互いに素な$\lbrace D_{j, k} : k=1, \dotsc, m_{j} \rbrace\subset\mathscr{S}$が取れて、
$( A\backslash A_{1} )\backslash A_{2} = \bigsqcup_{j=1}^{m}\bigsqcup_{k=1}^{m_{j}}D_{j, k}$を満たす。
このとき$\lbrace D_{j, k} \rbrace\subset\mathscr{S}$は互いに素である。以上を繰り返せば良い。$\square$
\end{proof}

半加法族の生成する有限加法族は、元の形が良く分かる集合になっている。

\begin{Prop}{}{}
$\mathscr{S}\subset 2^{S}$を半加法族とする。このとき$\sigma_{0}\lbrack \mathscr{S} \rbrack$は$\mathscr{S}$の元の非交叉有限和で表される集合全体である。
\end{Prop}

\begin{proof}
（証明）$\mathscr{S}$の元の非交叉有限和で表される集合全体を$\mathscr{A}$と書く。$\sigma_{0}\lbrack \mathscr{S} \rbrack\supset\mathscr{A}$は明らかなので逆を示そう。
$\mathscr{G}\subset\mathscr{A}$なので、$\mathscr{A}$が有限加法族であることを示せば良い。$\emptyset\in\mathscr{A}$は明白。
$A, B\in\mathscr{A}$に対して$A=\bigsqcup_{i=1}^{n}A_{i}, B=\bigsqcup_{j=1}^{m}B_{j}$（$A_{i}, B_{j}\in\mathscr{S}$）と表せば、
$A\cap B=\bigsqcup_{i, j}A_{i}\cap B_{j}$であり、$\mathscr{S}$は半加法族だから$A_{i}\cap B_{j}\in\mathscr{S}$である。
従って$A\cap B\in\mathscr{A}$が分かる。$S\backslash A=\bigcap_{i=1}^{n}( S\backslash A_{i} )$だが、
$A_{i}\in\mathscr{S}$より$S\backslash A_{i}$は$\mathscr{S}$の元の非交叉有限和で表せる。つまり$S\backslash A_{i}\in\mathscr{A}$である。
既に示したように$\mathscr{A}$は有限交叉で閉じているから$S\backslash A\in\mathscr{A}$である。
以上により$\mathscr{A}$は有限加法族であり、生成の最小性から$\sigma_{0}\lbrack \mathscr{S} \rbrack=\mathscr{A}$を得る。$\square$
\end{proof}




\subsection{半加法族上の前測度}
\begin{Def}{}{}
$\mathscr{S}\subset 2^{S}$を半加法族とする。集合函数$\mu\colon\mathscr{S}\rightarrow\lbrack 0, \infty \rbrack$が正値かつ有限加法的であるとき、
$\mu$は半加法族$\mathscr{S}$上の前測度という。
\end{Def}

有限加法族上の前測度のときとは違い、有限加法性は「互いに素な$A, B\in\mathscr{S}$に対して$\mu( A\sqcup B )=\mu( A )+\mu( B )$が成り立つ」を条件にすることはできない。

半加法族上の前測度は単調かつ有限劣加法的であるが、少し一般的な形で述べておくと便利である。

\begin{Prop}{}{}
$\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。次が成り立つ。
\begin{EnumCond}
\item$A\in\mathscr{S}$及び互いに素な$A_{1}, \dotsc, A_{n}\in\mathscr{S}$に対し、
\[ \bigsqcup_{i=1}^{n}A_{i}\subset A \Rightarrow \sum_{i=1}^{n}\mu( A_{i} )\le\mu( A ) \]
が成り立つ。
\item$B\in\mathscr{S}$及び$B_{1}, \dotsc, B_{n}\in\mathscr{S}$に対し、
\[ B\subset\bigcup_{i=1}^{n}B_{i} \Rightarrow \mu( B ) \le\sum_{i=1}^{n}\mu( B_{i} ) \]
が成り立つ。
\end{EnumCond}

特に$\mu$は単調かつ有限劣加法的である。
\end{Prop}

\begin{proof}
（証明）補題より互いに素な$D_{1}, \dotsc, D_{m}\in\mathscr{S}$が存在して$A\backslash\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}D_{j}$と表せる。
$\bigsqcup_{i=1}^{n}A_{i}\subset A$とする。このとき$A=\bigsqcup_{i=1}^{n}A_{i}\sqcup\bigsqcup_{j=1}^{m}D_{j}$であり、$\mu$は有限加法的であるから
\[ \mu( A )=\sum_{i=1}^{n}\mu( A_{i} )+\sum_{j=1}^{m}\mu( D_{j} )\ge\sum_{i=1}^{n}\mu( A_{i} ) \]
が成り立つ。

$B\subset\bigcup_{i=1}^{n}B_{i}$とする。$B=\bigcup_{i=1}^{n}( B\cap B_{i} )$なので、
\[ C_{i}:=( B\cap B_{i} )\backslash\bigcup_{j=1}^{i-1}( B\cap B_{j} ) \]
と置けば、$B=\bigsqcup_{i=1}^{n}C_{i}$と互いに素な和で表せる。ここで$B\cap B_{j}\in\mathscr{S}$だから、
補題より互いに素な$\lbrace D_{i, j} : j=1, \dotsc, n_{i} \rbrace\subset\mathscr{S}$が存在して$C_{i}=\bigsqcup_{j=1}^{n_{i}}D_{i, j}$と表せる。
$\mu$は有限加法的であり、$\bigsqcup_{j=1}^{n_{i}}D_{i, j}=C_{i}\subset B_{i}$であるから、上の結果より
\[ \mu( B )=\mu\left( \bigsqcup_{i=1}^{n}\bigsqcup_{j=1}^{n_{i}}D_{i, j} \right)=\sum_{i=1}^{n}\sum_{j=1}^{n_{i}}\mu( D_{i, j} )\le\sum_{i=1}^{n}\mu( B_{i} ) \]
が成り立つ。$\square$
\end{proof}

半加法族$\mathscr{S}\subset 2^{S}$について$\sigma_{0}\lbrack \mathscr{S} \rbrack$は$\mathscr{S}$の元の非交叉有限和として表される集合全体だったことを思い出そう。
つまり$A\in\sigma_{0}\lbrack \mathscr{S} \rbrack$について互いに素な$A_{1}, \dotsc, A_{n}\in\mathscr{S}$が存在して$A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。

\begin{Prop}{}{}
$\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。
集合函数$\mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$を
$A=\bigsqcup_{i=1}^{n}A_{i}\in\sigma_{0}\lbrack \mathscr{S} \rbrack$に対し、
\[ \sigma_{0}( A )=\sigma_{0}\left( \bigsqcup_{i=1}^{n}A_{i} \right):=\sum_{i=1}^{n}\mu( A_{i} ) \]
で定める。このとき$\mu_{0}$は有限加法族$\sigma_{0}\lbrack \mathscr{S} \rbrack$上の前測度となる。
\end{Prop}

\begin{proof}
（証明）$\mu_{0}$がwell-definedであることを示そう。すなわち$\mu_{0}( A )$が$A$の表示に依らないことを示す。
$A=\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}A^{\prime}_{j}$とする。$\mu$は有限加法的であるから
\[ \sum_{i=1}^{n}\mu( A_{i} )=\sum_{i=1}^{n}\sum_{j=1}^{m}\mu( A_{i}\cap A^{\prime}_{j} )=\sum_{j=1}^{m}A^{\prime}_{j} \]
となり、表示に依らないことが分かる。

$\mu_{0}( \emptyset )=0$は明白。$A=\bigsqcup_{i=1}^{n}A_{i}, B=\bigsqcup_{j=1}^{m}B_{j}$は互いに素であるとする。$\lbrace A_{i}, B_{j} \rbrace$も互いに素だから、
\[ \mu_{0}( A\sqcup B )=\sum_{i=1}^{n}\mu( A_{i} )+\sum_{j=1}^{m}\mu( B_{j} )=\mu_{0}( A )+\mu_{0}( B ) \]
を得る。$\square$
\end{proof}

上記命題において、定義から明らかに$\mu$の拡張となる$\sigma_{0}\lbrack \mathscr{S} \rbrack$上の前測度は一意的であることが分かる。

\begin{Lem}{}{}
$\mu$を半加法族$\mathscr{S}\subset 2^{S}$上の前測度、その拡張を$\mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$とする。このとき以下は同値である。
\begin{EnumEquiv}
\item$\mu_{0}$は可算加法的である。
\item$\mu$は弱可算劣加法的である。
\end{EnumEquiv}
\end{Lem}

\begin{proof}
（証明）上から下は明らかなので逆を示そう。互いに素な$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\sigma_{0}\lbrack \mathscr{S} \rbrack$を取り、
$B:=\bigsqcup_{n\in\mathbb{N}}A_{n}\in\sigma_{0}\lbrack \mathscr{S} \rbrack$とする。
このときある有限集合$\mathscr{A}_{n}, \mathscr{B}\subset\mathscr{S}$が存在して
\begin{align*}
A_{n}&=\bigsqcup_{G\in\mathscr{A}_{n}}G, & B&=\bigsqcup_{H\in\mathscr{B}}H
\end{align*}
と表せる。

まず$\mathscr{A}:=\bigcup_{n\in\mathbb{N}}\mathscr{A}_{n}=\bigsqcup_{n\in\mathbb{N}}\mathscr{A}_{n}$だから、
\[ \bigsqcup_{H\in\mathscr{B}}H=B=\bigsqcup_{n\in\mathbb{N}}A_{n}=\bigsqcup_{n\in\mathbb{N}}\bigsqcup_{G\in\mathscr{A}_{n}}G=\bigsqcup_{G\in\mathscr{A}}G \]
が成り立つ。ここで$H\in\mathscr{B}$について$H=\bigsqcup_{G\in\mathscr{A}}( G\cap H )$である。$\mathscr{S}$は半加法族だから$G\cap H\in\mathscr{S}$であり、従って仮定より
\[ \mu( H )\le\sum_{G\in\mathscr{A}}\mu( G\cap H ) \]
を得る。同様に$G\in\mathscr{A}$について$G=\bigsqcup_{H\in\mathscr{B}}( H\cap G )$であり、$\mu$は有限加法的だから$\mu( G )=\sum_{H\in\mathscr{B}}\mu( H\cap G )$を得る。以上より
\begin{align*}
\mu_{0}( B )&=\sum_{H\in\mathscr{B}}\mu( H )\le\sum_{H\in\mathscr{B}}\sum_{G\in\mathscr{A}}\mu( G\cap H ) \\
&=\sum_{G\in\mathscr{A}}\mu( G )=\sum_{n\in\mathbb{N}}\sum_{G\in\mathscr{A}_{n}}\mu( G ) \\
&=\sum_{n\in\mathbb{N}}\mu_{0}( A_{n} )
\end{align*}
となる。（ここで非負実数に関する和の順序の交換可能性を用いた。）つまり$\mu_{0}$は弱可算劣加法的である。$\mu_{0}$は有限加法族上の前測度だから、これは可算加法的であることと同値である。$\square$
\end{proof}

補題より半加法族上の前測度について、可算加法性、可算劣加法性、弱可算劣加法性は全て同値となる。

\begin{Thm}{半加法族上の前測度に対する拡張定理}{}
$\mu$は半加法族$\mathscr{S}\subset 2^{S}$上の前測度とする。以下は同値である。
\begin{EnumEquiv}
\item$\sigma\lbrack \mathscr{S} \rbrack=\sigma\lbrack \sigma_{0}\lbrack \mathscr{S} \rbrack \rbrack$上の
測度$\widehat{\mu}$が存在して$\widehat{\mu}|_{\mathscr{S}}=\mu$を満たす。つまり$A\in\mathscr{S}$なら$\widehat{\mu}( A )=\mu( A )$が成り立つ。
\item$\mu$は弱可算劣加法的である。
\end{EnumEquiv}
\end{Thm}

\begin{proof}
（証明）ホップの拡張定理の証明に沿って示すことが出来る。$ \mu_{0}\colon\sigma_{0}\lbrack \mathscr{S} \rbrack\rightarrow\lbrack 0, \infty \rbrack$を$\mu$の拡張とする。

まず外測度$\widehat{\mu}$の構成に関しては、$\mu$から誘導される外測度も$\mu_{0}$から誘導される外測度も等しい。
これは$\sigma_{0}\lbrack \mathscr{S} \rbrack$の元が$\mathscr{S}$の元の非交叉有限和で書けることに依る。

次に$\mathscr{S}\subset\mathscr{M}_{\widehat{\mu}}$を示したい。$A\in\mathscr{S}$及び$E\subset S$を取る。
$\mathscr{S}$は半加法族なので$A_{1}, \dotsc, A_{n}\in\mathscr{S}$が存在して$S\backslash A=\bigsqcup_{i=1}^{n}A_{i}$と表せる。
$E$の被覆$\mathscr{C}\subset\mathscr{S}$を取れば、$\lbrace C\cap A : C\in\mathscr{C} \rbrace\subset\mathscr{S}$は$E\cap A$の被覆となる。また$C\in\mathscr{C}$について
\[ C\backslash A=C\cap( S\backslash A )=C\cap\bigsqcup_{i=1}^{n}A_{i}=\bigsqcup_{i=1}^{n}( C\cap A_{i} ) \]
より$\lbrace C\cap A_{i} : C\in\mathscr{C}, i=1, \dotsc, n \rbrace\subset\mathscr{S}$は$E\backslash A$の被覆となる。故に
\begin{align*}
\widehat{\mu}( E\cap A )+\widehat{\mu}( E\backslash A ) &\le \sum_{C\in\mathscr{C}}\mu( C\cap A )+\sum_{C\in\mathscr{C}}\sum_{i=1}^{n}\mu( C\cap A_{i} ) \\
&=\sum_{C\in\mathscr{C}}\left( \mu( C\cap A )+\sum_{i=1}^{n}\mu( C\cap A_{i} ) \right)
\end{align*}
となる。このとき
\[ C=( C\cap A )\sqcup ( C\backslash A )=( C\cap A )\sqcup( C\cap A_{1} )\sqcup\dotsb\sqcup( C\cap A_{n} ) \]
であるから、$C\in\mathscr{C}$より$\mu$の有限加法性が使えて結局
\[ \mu( C\cap A )+\sum_{i=1}^{n}\mu( C\cap A_{i} )=\mu( C ) \]
が従う。

残りの部分はホップの拡張定理と同様に従う。ただし補題より半加法族上でも$\mu$の弱可算劣加法性が可算加法性と同値であることを用いる。$\square$
\end{proof}

-->