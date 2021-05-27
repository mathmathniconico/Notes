
# ルベーグ・スティルチェス測度

測度の例として（ボレル集合族上の）ルベーグ測度を定義する。ルベーグ測度の構成法はいくつかあるが、ここでは右連続非減少函数の定めるスティルチェス測度の1つとして与える。



## 半環と測度

測度について議論する上で恐らく最弱の集合族の1つが半環だろう。

__定義__ $S$を集合とする。$\mathscr{S}\subset 2^{S}$は次の3条件を満たすとする。

- $\emptyset\in\mathscr{S}$である。
- $A, B\in\mathscr{S}$なら$A\cap B\in\mathscr{S}$である。
- $A, B\in\mathscr{S}$なら互いに素な$C_{1}, \dotsc, C_{n}\in\mathscr{S}$が存在して$A\backslash B=\bigsqcup_{i=1}^{n}C_{i}$と表せる。

このとき$\mathscr{S}$を$S$上の半環と呼ぶ。

> 半加法族は半環であり、半環が全体集合$S$を含むとき半加法族となる。

半加法族に対して成り立った補題が、半環上でも全く同じ証明により成立する。

__補題__ $\mathscr{S}\subset 2^{S}$を半環とする。$A\in\mathscr{S}$及び$A_{1}, \dotsc, A_{n}\in\mathscr{S}$について、互いに素な$B_{1}, \dotsc, B_{m}\in\mathscr{S}$が存在して

$$
A\backslash\bigcup_{i=1}^{n}A_{i}=\bigsqcup_{j=1}^{m}B_{j}
$$

と表せる。

__定義__ $\mathscr{S}\subset 2^{S}$を半環とする。集合函数$\mu\colon\mathscr{S}\rightarrow\lbrack 0, \infty \rbrack$が正値かつ有限加法的であるとき、$\mu$は半環$\mathscr{S}$上の前測度という。

次の命題も半加法族のときと全く同様に示すことができる。

__命題__ $\mu$を半環$\mathscr{S}\subset 2^{S}$上の前測度とする。

- $A\in\mathscr{S}$及び互いに素な$A_{1}, \dotsc, A_{n}\in\mathscr{S}$について$\bigsqcup_{i=1}^{n}A_{i}\subset A$なら$\sum_{i=1}^{n}\mu( A_{i} )\le\mu( A )$である。
- $B\in\mathscr{S}$及び$B_{1}, \dotsc, B_{n}\in\mathscr{S}$について$B\subset\bigcup_{i=1}^{n}B_{i}$なら$\mu( B )\le\sum_{i=1}^{n}\mu( B_{i} )$である。

特に$\mu$は単調かつ有限劣加法的である。

__命題__ $\mu$を半環$\mathscr{S}\subset 2^{S}$上の前測度とする。$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{S}$に対し、互いに素な$\lbrace D_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{S}$が存在して、

$$
\begin{aligned}
\bigcup_{n\in\mathbb{N}}A_{n}&=\bigsqcup_{n\in\mathbb{N}}D_{n}, & \sum_{n\in\mathbb{N}}\mu( A_{n} )&\ge\sum_{n\in\mathbb{N}}\mu( D_{n} )
\end{aligned}
$$

が成り立つ。

（証明）$B_{1}=A_{1}, B_{n+1}=A_{n+1}\backslash \bigcup_{i=1}^{n}A_{i}$とする。補題より互いに素な$D_{n, 1}, \dotsc, D_{n, m_{n}}\in\mathscr{S}$が存在して$B_{n}=\bigsqcup_{i=1}^{m_{n}}D_{n, i}$と表せる。このとき$\bigcup_{n\in\mathbb{N}}=\bigsqcup_{n\in\mathbb{N}}B_{n}$が成り立つ。$\mu$は単調かつ有限加法的なので

$$
\sum_{n\in\mathbb{N}}\mu( A_{n} )\ge\sum_{n\in\mathbb{N}}\mu( B_{n} )=\sum_{n\in\mathbb{N}}\sum_{i=1}^{m_{n}}\mu( D_{n, i} )
$$

となる。

半環上の前測度に対する測度への拡張問題については以下の定理が成り立つ。

__定理__ （カラテオドリの拡張定理）$\mu$は半環$\mathscr{S}\subset 2^{S}$上の前測度とする。TFAE

1. $\sigma\lbrack \mathscr{S} \rbrack$上の測度$\widehat{\mu}$が存在して$\widehat{\mu}|_{\mathscr{S}}=\mu$を満たす。つまり$A\in\mathscr{S}$なら$\widehat{\mu}( A )=\mu( A )$が成り立つ。
1. $\mu$は弱可算劣加法的である。

（証明）ホップの拡張定理と同様に証明したい。まず外測度$\widehat{\mu}$の構成に関しては、$\mu$から誘導される外測度を考える。

次に$\mathscr{S}\subset\mathscr{M}_{\widehat{\mu}}$を示したい。$A\subset\mathscr{S}$及び$E\subset S$を取る。$E$の被覆$\mathscr{C}\subset\mathscr{S}$を取れば、$\lbrace C\cap A : C\in\mathscr{C} \rbrace\subset\mathscr{S}$は$E\cap A$の被覆となる。また半環の定義より各$C\in\mathscr{C}$に対して、互いに素な$D^{C}_{1}, \dotsc, D^{C}_{n( C )}\in\mathscr{S}$が存在して$C\backslash A=\bigsqcup_{i=1}^{n( C )}D^{C}_{i}$と表せる。このとき$\lbrace D^{C}_{i} : C\in\mathscr{C}, 1\le i \le n( C ) \rbrace\subset\mathscr{S}$は$E\backslash A$の被覆となる。故に

$$
\begin{aligned}
\widehat{\mu}( E\cap A )+\widehat{\mu}( E\backslash A )&\le\sum_{C\in\mathscr{C}}\mu( C\cap A )+\sum_{C\in\mathscr{C}}\sum_{i=1}^{n( C )}\mu( D^{C}_{i} ) \\
&=\sum_{C\in\mathscr{C}}\left( \mu( C\cap A )+\sum_{i=1}^{n( C )}\mu( D^{C}_{i} ) \right)
\end{aligned}
$$

となる。このとき
$$
C=( C\cap A )\sqcup\bigsqcup_{i=1}^{n( C )}D^{C}_{i}
$$

であるから、$C\in\mathscr{S}$より$\mu$の有限加法性が使えて結局

$$
\mu( C\cap A )+\sum_{i=1}^{n( C )}\mu( D^{C}_{i} )=\mu( C )
$$

が従う。

以上により$\widehat{\mu}$は$\sigma\lbrack \mathscr{S} \rbrack$上の測度となることが分かった。最後に$\mathscr{S}$上での値を見てみよう。まず$A\in\mathscr{S}$に対して定義より$\widehat{\mu}( A )\le\mu( A )$が成り立つ。逆を示すために$A$の被覆$\mathscr{C}\subset\mathscr{S}$を取る。先の命題より、互いに素な$\lbrace D_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{S}$が存在して

$$
\begin{aligned}
\bigcup_{C\in\mathscr{C}}C&=\bigsqcup_{n\in\mathbb{N}}D_{n}, & \sum_{C\in\mathscr{C}}\mu( C )&\ge\sum_{n\in\mathbb{N}}\mu( D_{n} )
\end{aligned}
$$

を満たす。$\lbrace D_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{S}$も$A$の被覆となるから、$\mu$の弱可算劣加法性及び単調性より

$$
\mu( A ) = \mu\left( \bigsqcup_{n\in\mathbb{N}}A\cap D_{n} \right) \le \sum_{n\in\mathbb{N}}\mu( A\cap D_{n} ) \le \sum_{n\in\mathbb{N}}\mu( D_{n} ) \le \sum_{C\in\mathscr{C}}\mu( C )
$$

を得る。右辺の下限を取れば$\mu( A )\le\widehat{\mu}( A )$が従う。$\square$

定理により、半環上の前測度に対しても、可算加法性、可算劣加法性、弱可算劣加法性は全て同値となる。




## スティルチェス測度

この節では、ユークリッド空間$\mathbb{R}$の通常の位相$\mathcal{O}$において、ボレル集合族$\sigma\lbrack \mathcal{O} \rbrack$上の測度として、スティルチェス測度の構成を行う。一般論ではなく具体例に関する内容であることから、連続性の公理に始まる実数$\mathbb{R}$の性質、あるいは距離空間としての位相的性質、そして解析的な連続性の扱い方などについては既知とする。ここで用いる大事な性質を一つ挙げるならば、有界閉区間のコンパクト性である。即ち、閉区間を任意個の開区間で覆ったとき、その中の有限個を選んで再び閉区間を覆うようにできる。コンパクト性については後の章で改めて議論する。

まず$\mathcal{O}$は開区間から為る可算開基$\mathcal{B}=\lbrace ( a, b ) : a, b\in\mathbb{Q}, a\lt b \rbrace$を持つ。つまり第2可算公理を満たすのだが、$\mathcal{O}$は測度論的には扱い難い。そこで次の集合族について考える。

__命題__ $\mathscr{I}:=\lbrace ( a, b \rbrack : a, b\in\mathbb{R}, a\lt b \rbrace\cup\lbrace \emptyset \rbrace$とする。このとき$\mathscr{I}$は半環であり、$\sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathscr{I} \rbrack$を満たす。

（証明）$\mathscr{I}$が半環となることは良い。差集合を取るときが特殊で、$( a, b \rbrack\subset( c, d \rbrack$のときに限り$( c, d \rbrack\backslash( a, b \rbrack=( c, a \rbrack\sqcup( b, d \rbrack$となるので$\mathscr{I}$の元の非交叉有限和である。

$( a, b \rbrack\in\mathscr{I}$に対し$a\lt c\lt b$なる$c\in\mathbb{Q}$を取る。また数列$( a_{n} )_{n\in\mathbb{N}}, ( b_{n} )_{n\in\mathbb{N}}\subset\mathbb{Q}$を$a_{n}\searrow a, b_{n}\searrow b, a\lt a_{n}\lt c\lt b\lt b_{n}$が成り立つように取る。このとき

$$
( a, b \rbrack=\left( \bigcap_{n\in\mathbb{N}}( c, b_{n} ) \right)\cup\left( \bigcup_{n\in\mathbb{N}}( a_{n}, c ) \right)
$$

であるから、$( a, b \rbrack\in\sigma\lbrack \mathcal{B} \rbrack$を得る。

逆に$( a, b )\in\mathcal{B}$に対し、数列$( b_{n} )_{n\in\mathbb{N}}\subset\mathbb{Q}$を$a\lt b_{n} \lt b$を満たすように取る。このとき

$$
( a, b )=\bigcup_{n\in\mathbb{N}}( a, b_{n} \rbrack
$$

であるから、$( a, b )\in\sigma\lbrack \mathscr{I} \rbrack$を得る。$\square$

<!-- 
以下ボレル集合族$\sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathcal{B} \rbrack=\sigma\lbrack \mathscr{I} \rbrack$のことを$\mathscr{B}( \mathbb{R} )$で表す。

\begin{Prop}{}{}
$\varphi\colon\mathbb{R}\rightarrow\mathbb{R}$は右連続な非減少函数とする。$( a, b \rbrack\in\mathscr{I}$に対し
\[ \mu( ( a, b \rbrack ):=\varphi( b )-\varphi( a ) \]
と定めると、$\mu$は半環$\mathscr{I}$上の前測度となる。
\end{Prop}

\begin{proof}
（証明）$\mu$が有限加法的であることは明らかだろう。
実際$( a, b \rbrack=( a_{1}, b_{1} \rbrack\sqcup\dotsm( a_{n}, b_{n} \rbrack$とすると、$a_{1}=a, a_{n+1}=b_{n}, b_{n}=b$より、
\begin{align*}
\mu( ( a, b \rbrack ) &= \varphi( b )-\varphi( a ) \\
&= ( \varphi( b_{n} )-\varphi( a_{n} ) )+\dotsm+( \varphi( b_{1} )-\varphi( a_{1} ) ) \\
&= \mu( ( a_{n}, b_{n} \rbrack )+\dotsm+\mu( ( a_{1}, b_{1} \rbrack )
\end{align*}
が成り立つ。

$\mu$が弱可算劣加法的であることを示そう。$( a, b \rbrack=\bigsqcup_{n\in\mathbb{N}}( a_{n}, b_{n} \rbrack$とする。
$\varepsilon\gt 0$とする。$\varphi$は右連続だから、十分小さな$\delta, \delta_{n} \gt 0$を取り、
\begin{align*}
\varphi( a+\delta )-\varphi( a )&\lt\frac{\varepsilon}{2}, & \varphi( b_{n}+\delta_{n} )-\varphi( b_{n} )\lt\frac{\varepsilon}{2^{n+1}}
\end{align*}
を満たすようにできる。$\lbrack a+\delta, b \rbrack\subset\bigcup_{n\in\mathbb{N}}( a_{n}, b_{n}+\delta_{n} )$より、
コンパクト性から有限集合$F\subset\mathbb{N}$を選び、特に$( a+\delta, b \rbrack\subset\bigcup_{n\in F}( a_{n}, b_{n}+\delta_{n} \rbrack$が成り立つようにできる。
$\mu$は半環$\mathscr{I}$上の前測度だから、
\begin{align*}
\mu( ( a, b \rbrack ) &= \varphi( b )-\varphi( a ) \\
&\lt \varphi( b )-\varphi( a+\delta )+\frac{\varepsilon}{2} \\
&= \mu( ( a+\delta, b \rbrack )+\frac{\varepsilon}{2} \\
&\le\sum_{n\in F}\mu( ( a_{n}, b_{n}+\delta_{n} \rbrack )+\frac{\varepsilon}{2} \\
&\lt \sum_{n\in F}\mu( ( a_{n}, b_{n} \rbrack )+\varepsilon \\
&\le \sum_{n\in\mathbb{N}}\mu( ( a_{n}, b_{n} \rbrack )+\varepsilon
\end{align*}
を得る。$\varepsilon$は任意だから、$\mu$の弱可算劣加法性が従う。$\square$
\end{proof}

拡張定理より$\mathscr{B}( \mathbb{R} )$上の測度であり、$\mathscr{I}$上で$\mu$と一致するものが存在する。
特に$\mu$は$\sigma$-有限なので、拡張された測度も$\sigma$-有限である。更に$\mathscr{I}$は有限交叉で閉じるので、このような測度は一意的である。

\begin{Def}{}{}
右連続な非減少函数$\varphi\colon\mathbb{R}\rightarrow\mathbb{R}$に対し、$\mathscr{B}( \mathbb{R} )$上の$\sigma$-有限な測度で、
$( a, b \rbrack\in\mathscr{I}$に対して$\mu( ( a, b \rbrack )=\varphi( b )-\varphi( a )$となるものを、
（ボレル集合族$\mathscr{B}( \mathbb{R} )$上の）スティルチェス測度（Stieltjes measure）と呼ぶ。

特に$\varphi( x )=x$のとき、（ボレル集合族$\mathscr{B}( \mathbb{R} )$上の）ルベーグ測度（Lebesgue measure）と呼ぶ。
\end{Def}

-->