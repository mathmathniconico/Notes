
# 積測度空間と測度の一致



## 積可測空間上の測度

測度空間$( S, \mathscr{A}, \mu_{S} )$及び$( T, \mathscr{B}, \mu_{T} )$に対して、積可測空間$( S\times T, \mathscr{A}\otimes\mathscr{B} )$上の測度を構成しよう。積$\sigma$加法族は

$$
\mathscr{A}\otimes\mathscr{B}=\sigma\lbrack \mathscr{A}\times T\cup S\times\mathscr{B} \rbrack
$$

と定義されるが、基となる集合族$\mathscr{A}\times T\cup S\times\mathscr{B}$はやや扱い難い。

__命題__ $S\in\mathscr{G}\subset 2^{S}, T\in\mathscr{H}\subset 2^{T}$とする。このとき

$$
\sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack = \sigma\lbrack \mathscr{G}\times\mathscr{H} \rbrack
$$

が成り立つ。特に$( S, \mathscr{A} ), ( T, \mathscr{B} )$が可測空間のとき

$$
\sigma\lbrack \mathscr{A}\times T\cup S\times\mathscr{B} \rbrack = \sigma\lbrack \mathscr{A}\times\mathscr{B} \rbrack
$$

が成り立つ。

（証明）$S\in\mathscr{G}, T\in\mathscr{H}$より$\mathscr{G}\times T\cup S\times\mathscr{H} \subset \mathscr{G}\times\mathscr{H}$となるため左辺は右辺を含む。$G\times H\in\mathscr{G}\times\mathscr{H}$について

$$
G\times H=G\times T\cap S\times H\in\sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

より逆も成り立つ。$\square$

__命題__ $( S, \mathscr{A} ), ( T, \mathscr{B} )$は可測空間とする。このとき$\mathscr{A}\times\mathscr{B}$は半加法族である。

（証明）まず$\emptyset=\emptyset\times\emptyset\in\mathscr{A}\times\mathscr{B}$である。次に$A\times B, C\times D\in\mathscr{A}\times\mathscr{B}$に対し、

$$
A\times B\cap C\times D=( A\cap C )\times( B\times D )\in\mathscr{A}\times\mathscr{B}
$$

である。また

$$
( S\times T )\setminus( A\times B )=( S\setminus A )\times B\sqcup( S\setminus A )\times( T\setminus B )\sqcup( A\times( T\setminus B )
$$

より、$\mathscr{A}\times\mathscr{B}$の元の非交叉有限和で書ける。従って$\mathscr{A}\times\mathscr{B}$は半加法族である。$\square$

$\mathscr{A}\otimes\mathscr{B}=\sigma\lbrack \mathscr{A}\times\mathscr{B} \rbrack$上の測度を構成するために拡張定理を用いる。そのためにはまず、半加法族$\mathscr{A}\times\mathscr{B}$上の前測度を与えなければならない。

__補題__ $( S, \mathscr{A}, \mu_{S} ), ( T, \mathscr{B}, \mu_{T} )$を測度空間とする。このとき集合函数$\mu\colon\mathscr{A}\times\mathscr{B}\rightarrow\lbrack 0, \infty \rbrack$を、$A\times B\in\mathscr{A}\times\mathscr{B}$に対し

$$
\mu( A\times B ):=\mu_{S}( A )\mu_{T}( B )
$$

で定める。このとき$\mu$は半加法族$\mathscr{A}\times\mathscr{B}$上の前測度となる。

（証明）正値であることは明らかなので、有限加法的であることを示す。$A_{1}\times B_{1}, \dotsc, A_{n}\times B_{n}\in\mathscr{A}\times\mathscr{B}$に対し、$\bigsqcup_{i=1}^{n}A_{i}\times B_{i}=A\times B\in\mathscr{A}\times\mathscr{B}$であるとする。このとき

$$
\mu( A\times B )=\sum_{i=1}^{n}\mu( A_{i}\times B_{i} )
$$

が成り立つことを$n$に関する帰納法で示そう。

$n=1$のときは$\mu( A\times B )=\mu( A_{1}\times B_{1} )$より正しい。

$n=k$に対して成り立つとして、$n=k+1$を考える。このとき

$$
( A_{k+1}\times B_{k+1} )\sqcup\bigsqcup_{i=1}^{k}( A_{i}\times B_{i} )=A\times B
$$

だから、

$$
(A\setminus A_{k+1} )\times( B\setminus B_{k+1} )=\bigsqcup_{i=1}^{k}( A_{i}\setminus A_{k+1} )\times( B_{i}\setminus B_{k+1} )
$$

が成り立つ。帰納法の仮定より

$$
\mu_{S}( A\setminus A_{k+1} )\mu_{T}( B\setminus B_{k+1} )=\sum_{i=1}^{k}\mu_{S}( A_{i}\setminus A_{k+1} )\mu_{T}( B_{i}\setminus B_{k+1} )
$$

が成り立つ。同様にして

$$
\begin{aligned}
\mu_{S}( A\setminus A_{k+1} )\mu_{T}( B\cap B_{k+1} ) &= \sum_{i=1}^{k}\mu_{S}( A_{i}\setminus A_{k+1} )\mu_{T}( B_{i}\cap B_{k+1} ), \\
\mu_{S}( A\cap A_{k+1} )\mu_{T}( B\setminus B_{k+1} ) &= \sum_{i=1}^{k}\mu_{S}( A_{i}\cap A_{k+1} )\mu_{T}( B_{i}\setminus B_{k+1} )
\end{aligned}
$$

も成り立つ。ここで$i=1, \dotsc, k$について$\mu_{S}( A_{i}\cap A_{k+1} )\mu_{T}( B_{i}\cap B_{k+1} )\gt 0$と仮定すると、

$$
( A_{i}\cap A_{k+1} )\times( B_{i}\cap B_{k+1} )=( A_{i}\times B_{i} )\cap( A_{k+1}\times B_{k+1} )\neq\emptyset
$$

となり矛盾する。故に$\mu_{S}( A_{i}\cap A_{k+1} )\mu_{T}( B_{i}\cap B_{k+1} )=0$であり、

$$
\begin{aligned} \mu( A\times B ) &= \mu_{S}( A )\mu_{T}( B ) \\
&= ( \mu_{S}( A\setminus A_{k+1} )+\mu_{S}( A\cap A_{k+1} ) )( \mu_{T}( B\setminus B_{k+1} )+\mu_{T}( B\cap B_{k+1} ) ) \\
&=\left( \sum_{i=1}^{k}( \mu_{S}( A_{i}\setminus A_{k+1} )+\mu_{S}( A_{i}\cap A_{k+1} ) )( \mu_{T}( B_{i}\setminus B_{k+1} )+\mu_{T}( B_{i}\cap B_{k+1} ) ) \right) +\mu_{S}( A_{k+1} )\mu_{T}( B_{k+1} ) \\
 &= \sum_{i=1}^{k+1}\mu_{S}( A_{i} )\mu_{T}( B_{i} )
\end{aligned}
$$

を得る。$\square$

__定理__ 上記補題の$\mu$は弱可算劣加法的である。

（証明）集合$X$上の可算被覆$\mathscr{C}=\lbrace C_{1}, C_{2}, \dotsc \rbrace\subset 2^{X}$を考える。まず写像$f\colon X\rightarrow 2^{\mathbb{N}}$を以下で定める。

- $x\in X$及び$n\in\mathbb{N}$について、$x\in C_{n}$なら$f(x)_{n}=1$、$x\notin C_{n}$なら$f(x)_{n}=0$とする。

このとき$p\in 2^{\mathbb{N}}$について

$$
f^{-1}(u)=\bigcap_{p_{i}=1}C_{i}\cap\bigcap_{p_{i}=0}( X\setminus C_{i} )
$$

であり、従って$f^{-1}( 0 )=\emptyset$及び$X=\bigsqcup_{p\in 2^{\mathbb{N}}}f^{-1}(p)$が成り立つ。

さて互いに素な$\lbrace A_{n}\times B_{n} \rbrace\subset\mathscr{A}\times\mathscr{B}$について、$\bigsqcup_{n\in\mathbb{N}}A_{n}\times B_{n}=A\times B\in\mathscr{A}\times\mathscr{B}$であるとする。$\bigcup_{n\in\mathbb{N}}A_{n}=A, \bigcup_{n\in\mathbb{N}}B_{n}=B$より、写像$f\colon A\rightarrow 2^{\mathbb{N}}, g\colon B\rightarrow 2^{\mathbb{N}}$を上記のように定めることができる。更に$\mathscr{A}, \mathscr{B}$は$\sigma$加法族だから、$p, q\in 2^{\mathbb{N}}$について$f^{-1}(p)\in\mathscr{A}, g^{-1}(q)\in\mathscr{B}$が成り立つ。$\mu_{S}, \mu_{T}$は測度だから可算加法的なので

$$
\begin{aligned}
\mu( A\times B ) &= \mu_{S}( A )\mu_{T}( B ) \\
&= \left( \sum_{p\in 2^{\mathbb{N}}}\mu_{S}( f^{-1}(p) ) \right)\left( \sum_{q\in 2^{\mathbb{N}}}\mu_{T}( g^{-1}(q) ) \right) \\
&=\sum_{p, q}\mu_{S}( f^{-1}(p) )\mu_{T}( g^{-1}(q) ) \\
&= \sum_{p, q}\mu( f^{-1}(p)\times g^{-1}(q) )
\end{aligned}
$$

を得る。

ところで$( x, y )\in A\times B$について、ある$n$が存在して$( x, y )\in A_{n}\times B_{n}$であり、従って$f( x )_{n}=g( y )_{n}=1$である。故に$p, q\in 2^{\mathbb{N}}$が任意の$n$について$p_{n}=q_{n}=1$でないなら、$f^{-1}(p)\times g^{-1}(q)=\emptyset$であり、特に$\mu$は前測度なので$\mu( f^{-1}(p)\times g^{-1}(q) )=0$である。以上より

$$
\begin{aligned}
\sum_{p, q}\mu(f^{-1}(p)\times g^{-1}(q)) &=\sum_{\exists n(p_{n}=q_{n}=1)}\mu( f^{-1}(p)\times g^{-1}(q) ) \\
&\le \sum_{n\in\mathbb{N}}\sum_{p_{n}=q_{n}=1}\mu( f^{-1}(p)\times g^{-1}(q) ) \\
&=\sum_{n\in\mathbb{N}}\sum_{p_{n}=q_{n}=1}\mu_{S}( f^{-1}(p) )\mu_{T}( g^{-1}(q) ) \\
\end{aligned}
$$

を得る。ここで$A=\bigsqcup_{p\in 2^{\mathbb{N}}}f^{-1}(p)$より、$A_{n}=\bigsqcup_{p}f^{-1}(p)\cap A_{n}=\bigsqcup_{p_{n}=1}f^{-1}(p)$である。よって

$$
\mu_{S}(A_{n})\mu_{T}(B_{n})=\left(\sum_{p_{n}=1}\mu_{S}(f^{-1}(p))\right)\left(\sum_{q_{n}=1}\mu_{T}(g^{-1}(q))\right)=\sum_{p_{n}=q_{n}=1}\mu_{S}(f^{-1}(p))\mu_{T}(g^{-1}(q))
$$

だから、結局

$$
\mu(A\times B)\le\sum_{n\in\mathbb{N}}\sum_{p_{n}=q_{n}=1}\mu_{S}( f^{-1}(p) )\mu_{T}( g^{-1}(q) )=\sum_{n\in\mathbb{N}}\mu_{S}(A_{n})\mu_{T}(B_{n})
$$

を得る。つまり$\mu$は弱可算劣加法的である。$\square$

従って拡張定理より$\mu$の拡張となる$\mathscr{A}\otimes\mathscr{B}=\sigma\lbrack \mathscr{A}\times\mathscr{B} \rbrack$上の測度が存在する。これをもって測度空間$( S, \mathscr{A}, \mu_{S} ), ( T, \mathscr{B}, \mu_{T} )$の積としたいのだが、実は拡張は一意でない。




## ディンキン族

__定義__ $S$を集合とする。$\mathscr{D}\subset 2^{S}$は次の3条件を満たすとする。

- $S\in\mathscr{D}$である。
- $A, B\in\mathscr{D}, A\subset B$なら$B\setminus A\in\mathscr{D}$である。
- $\lbrace D_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{D}$が単調増大列（$D_{1}\subset D_{2}\subset\dotsm$）なら$\bigcup_{n\in\mathbb{N}}D_{n}\in\mathscr{D}$である。

このとき$\mathscr{D}$を$S$上の **ディンキン族** と呼ぶ。

> $\sigma$加法族はディンキン族である。またディンキン族$\mathscr{D}$について$\emptyset=S\setminus S\in\mathscr{D}$であり、$A\in\mathscr{D}$なら$S\setminus A\in\mathscr{D}$も明らかだが、可算合併に関しては一般に成り立たない。ただし$\lbrace A_{n} \rbrace\subset\mathscr{D}$について単調増大列$B_{n}:=\bigcup_{i=1}^{n}A_{i}$を作ることができるので、$B_{n}\in\mathscr{D}$が常に成り立つのであれば$\sigma$加法族であることが分かる。

ディンキン族も任意の交叉でディンキン族となる。従って生成を考えることができる。

__定義__ $\mathscr{G}\subset 2^{S}$とする。$\mathscr{G}$を含むディンキン族全体の交叉を$D\lbrack \mathscr{G} \rbrack_{S}$や$D\lbrack \mathscr{G} \rbrack$と記し、$\mathscr{G}$により$S$上で生成されたディンキン族と呼ぶ。

__命題__ $\mathscr{G}\subset 2^{S}$とする。$A\in D\lbrack \mathscr{G} \rbrack$に対して

$$
\mathscr{D}_{A}:=\lbrace B\in D\lbrack \mathscr{G} \rbrack : A\cap B\in D\lbrack \mathscr{G} \rbrack \rbrace
$$

と定めると$\mathscr{D}_{A}$は$A$を含むディンキン族となる。

（証明）$A\cap S= A\in D\lbrack \mathscr{G} \rbrack$より$S\in\mathscr{D}_{A}$である。

$B, C\in D\lbrack \mathscr{G} \rbrack, B\subset C$に対して$A\cap ( C\setminus B )=( A\cap C )\setminus( A\cap B )$となる。ここで$A\cap B, A\cap C\in D\lbrack \mathscr{G} \rbrack$は$A\cap B\subset A\cap C$を満たすので、$C\setminus B\in\mathscr{D}_{A}$を得る。

単調増大列$\lbrace B_{n} \rbrace_{n\in\mathbb{N}}\subset D\lbrack \mathscr{G} \rbrack$を取る。$A\cap\bigcup_{n\in\mathbb{N}}B_{n}=\bigcup_{n\in\mathbb{N}}( A\cap B_{n} )$だが、これは単調増大列$\lbrace A\cap B_{n} \rbrace_{n\in\mathbb{N}}\subset D\lbrack \mathscr{G} \rbrack$の極限で表せる。故に$\bigcup_{n\in\mathbb{N}}B_{n}\in\mathscr{D}_{A}$も従う。

$A\in\mathscr{D}_{A}$は定義より明らか。$\square$

__補題__ （ディンキンの補題）$\mathscr{G}\subset 2^{S}$は有限交叉で閉じるとする。すなわち$G_{1}, \dotsc, G_{n}\in\mathscr{G}$について、

$$
\bigcap_{i=1}^{n}G_{i}\in\mathscr{G}
$$

を満たすとする。このとき$D\lbrack \mathscr{G} \rbrack=\sigma\lbrack \mathscr{G} \rbrack$が成り立つ。

（証明）$\sigma$加法族はディンキン族なので最小性より$D\lbrack \mathscr{G} \rbrack\subset\sigma\lbrack \mathscr{G} \rbrack$である。

逆は$D\lbrack \mathscr{G} \rbrack$が$\sigma$加法族であることを示せば良い。そこで

$$
\mathscr{D}:=\lbrace A\in D\lbrack \mathscr{G} \rbrack : \mathscr{D}_{A}=D\lbrack \mathscr{G} \rbrack \rbrace
$$

と定める。このとき$\mathscr{G}\subset\mathscr{D}$が成り立つ。実際$A\in\mathscr{G}$とすると、任意の$G\in\mathscr{G}$について仮定より$A\cap G\in\mathscr{G}$である。$\mathscr{G}\subset D\lbrack \mathscr{G} \rbrack$であるから$\mathscr{G}\subset\mathscr{D}_{A}$である。ここで$\mathscr{D}_{A}$はディンキン族だから最小性より$D\lbrack \mathscr{G} \rbrack\subset\mathscr{D}_{A}$を得る。逆も定義より明らかなので$D\lbrack \mathscr{G} \rbrack=\mathscr{D}_{A}$が成り立つ。以上より$A\in \mathscr{D}$を得る。

$\mathscr{D}$が$S$上のディンキン族となることを示そう。まず$\mathscr{D}_{S}=D\lbrack \mathscr{G} \rbrack$より$S\in\mathscr{D}$である。

$A, B\in\mathscr{D}, A\subset B$について$B\setminus A\in\mathscr{D}$を示したい。$A, B\in D\lbrack \mathscr{G} \rbrack$より$B\setminus A\in D\lbrack \mathscr{G} \rbrack$である。従って$\mathscr{G}\subset\mathscr{D}_{B\setminus A}$を示せば良い。$G\in\mathscr{G}$とする。このとき$\mathscr{G}\subset \mathscr{D}_{A}, \mathscr{D}_{B}$より$A\cap G, B\cap G\in D\lbrack \mathscr{G} \rbrack$だから、

$$
( B\setminus A )\cap G=( B\cap G )\setminus( A\cap G )\in D\lbrack \mathscr{G} \rbrack
$$

を得る。故に$G\in \mathscr{D}_{B\setminus A}$である。

同様に単調増大列$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{D}$を取れば、$G\in\mathscr{G}$に対し$( \bigcup_{n\in\mathbb{N}} )\cap G=\bigcup_{n\in\mathbb{N}}( G\cap A_{n} )$が成り立つ。これは単調増大列$\lbrace G\cap A_{n} \rbrace_{n\in\mathbb{N}}\subset D\lbrack \mathscr{G} \rbrack$の極限だから$D\lbrack \mathscr{G} \rbrack = \mathscr{D}_{\bigcup_{n\in\mathbb{N}}}$を得る。

以上より$\mathscr{D}$は$\mathscr{G}$を含む$S$上のディンキン族であり、特に$\mathscr{D}=D\lbrack \mathscr{G} \rbrack$が成り立つ。

$\mathscr{D}=D\lbrack \mathscr{G} \rbrack$は有限交叉で閉じている。実際$A, B\in\mathscr{D}$とすると、$B\in\mathscr{D}_{B}=\mathscr{D}_{A}$より$A\cap B\in D\lbrack \mathscr{G} \rbrack=\mathscr{D}$を得る。特に$A\cup B=S\setminus( ( S\setminus A )\cap( S\setminus B ) )\in\mathscr{D}$より有限合併でも閉じている。従って$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{D}$について$B_{n}:=\bigcup_{i=1}^{n}A_{i}\in\mathscr{D}$と定めれば$\lbrace B_{n} \rbrace_{n\in\mathbb{N}}$は$\mathscr{D}$における単調増大列となる。従って$\bigcup_{n\in\mathbb{N}}A_{n}=\bigcup_{n\in\mathbb{N}}B_{n}\in\mathscr{D}$となる。$\square$



<!--


\subsection{測度の一致}
\begin{Def}{}{}
単調な集合函数$\mu\colon\mathscr{G}\rightarrow\lbrack 0, \infty \rbrack$に対し以下を定める。
\begin{EnumCond}
\item$S\in\mathscr{G}$であり、$\mu( G )\lt\infty$のとき$\mu$は有限（finite）であるという。
\item ある$\lbrace G_{n} \rbrace\subset\mathscr{G}$が存在して$G_{n}\nearrow S, \mu( G_{n} )\lt\infty$を満たすとき$\mu$は$\sigma$-有限であるという。
\end{EnumCond}
\end{Def}

\begin{Prop}{}{}
可測空間$( S, \mathscr{A} )$上の有限な測度$\mu_{1}, \mu_{2}$に対し、$\mu_{1}( S )=\mu_{2}( S )$なら
\[ \mathscr{D}:=\lbrace D\in\mathscr{A} : \mu_{1}( D )=\mu_{2}( D ) \rbrace \]
はディンキン族である。
\end{Prop}

\begin{proof}
（証明）定義より$S\in\mathscr{D}$である。$A, B\in\mathscr{D}, A\subset B$とする。$\mu_{j}$は有限な測度だから$\mu_{j}( B\setminus A )=\mu_{j}( B )-\mu_{j}( A )$となる。
故に$B\setminus A\in\mathscr{D}$となる。また単調増大列$\lbrace A_{n} \rbrace\subset\mathscr{D}$に対し、$A_{0}:=\emptyset, B_{n}:=A_{n}\setminus A_{n-1}$と定めれば
\[ \mu_{j}\left( \bigcup_{n\in\mathbb{N}} \right)=\mu_{j}\left( \bigsqcup_{n\in\mathbb{N}}B_{n} \right)=\sum_{n\in\mathbb{N}}\mu_{j}( A_{n}\setminus A_{n-1} ) \]
が成り立つ。$A_{n}\setminus A_{n-1}\in\mathscr{D}$より$\bigcup_{n\in\mathbb{N}}A_{n}\in\mathscr{D}$が従う。$\square$
\end{proof}

\begin{Thm}{}{}
$\mathscr{G}\subset 2^{S}$は有限交叉で閉じるとする。$\sigma\lbrack \mathscr{G} \rbrack$上の測度$\mu_{1}, \mu_{2}$は、$\mathscr{G}$上で一致し、更に
$\mu_{0}:=\mu_{j}|_{\mathscr{G}}$は$\sigma$-有限とする。このとき$\mu_{1}=\mu_{2}$が成り立つ。
\end{Thm}

\begin{proof}
（証明）単調増大な$\lbrace G_{n} \rbrace\subset\mathscr{G}$を、$G_{n}\nearrow S, \mu_{0}( G_{n} )\lt\infty$を満たすように取る。
$A\in\sigma\lbrack \mathscr{G} \rbrack$に対して$A\cap G_{n}\nearrow A$であるから、増大列連続性より$\mu_{j}( A )=\lim_{n\in\mathbb{N}}\mu( A\cap G_{n} )$が成り立つ。

$A\in\sigma\lbrack \mathscr{G} \rbrack$に対して$\widetilde{\mu}_{j}( A ):=\mu_{j}( A\cap G_{n} )$と定めると、
$\widetilde{\mu}_{j}$は$\sigma\lbrack \mathscr{G} \rbrack$上の有限な測度となる。ここで
\[ \mathscr{D}_{n}:=\lbrace A\in\sigma\lbrack \mathscr{G} \rbrack : \widetilde{\mu}_{1}( A )=\widetilde{\mu}_{2}( A ) \rbrace \]
と置くと、先の命題よりこれはディンキン族となる。ディンキンの補題より$\sigma\lbrack \mathscr{G} \rbrack=D\lbrack \mathscr{G} \rbrack$であるから、
最小性より$\mathscr{D}_{n}=\sigma\lbrack \mathscr{G} \rbrack$となる。よって$\mu_{1}( A\cap G_{n} )=\mu_{2}( A\cap G_{n} )$であるから、$\mu_{1}=\mu_{2}$が従う。$\square$
\end{proof}

\begin{Cor}{}{}
$( S, \mathscr{A}, \mu_{S} ), ( T, \mathscr{B}, \mu_{T} )$を測度空間とする。$\mu_{S}, \mu_{T}$が$\sigma$-有限であるとき、
前測度$\mu\colon\mathscr{A}\times\mathscr{B}\rightarrow\lbrack 0, \infty \rbrack$の拡張は一意的である。
\end{Cor}

\begin{proof}
（証明）$\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{A}, \lbrace B_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{B}$として
\begin{align*}
A_{n}&\nearrow S, & B_{n}&\nearrow T, & \mu_{S}( A_{n} ), \mu_{T}( B_{n} )&\lt\infty
\end{align*}
を満たすように取る。ここで$C_{n}=A_{n}\times B_{n}\in\mathscr{A}\times\mathscr{B}$とすれば
\begin{align*}
C_{n}&\nearrow S\times T, & \mu( C_{n} )&=\mu_{S}( A_{n} )\mu_{T}( B_{n} )\lt\infty
\end{align*}
が成り立つ。従って$\mu$は$\sigma$-有限であるため、定理から拡張は一意的であることが分かる。$\square$
\end{proof}

\begin{Def}{}{}
系において$\mu$の拡張となる可測空間$( S\times T, \mathscr{A}\otimes\mathscr{B} )$上の測度は一意的に存在する。
これを$\mu_{S}\otimes\mu_{T}$と記し、$\mu_{S}$と$\mu_{T}$の積測度と呼ぶ。このとき$( S\times T, \mathscr{A}\otimes\mathscr{B}, \mu_{S}\otimes\mu_{T} )$を積測度空間と呼ぶ。
\end{Def}

ただし積測度空間は圏における積対象ではない。

-->