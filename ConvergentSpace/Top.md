
# 位相

## 位相空間と連続写像

以下は内田伏一に依る。

__定義__ $X$を集合とする。$\mathcal{O}\subset 2^{X}$は以下を満たすとする。

- $\emptyset\in\mathcal{O}, X\in\mathcal{O}$である。
- $U, V\in\mathcal{O}$なら$U\cap V\in\mathcal{O}$である。
- $\Lambda$を集合とする。任意の$\lambda\in\Lambda$について$U_{\lambda}\in\mathcal{O}$なら$\bigcup_{\lambda\in\Lambda}U_{\lambda}\in\mathcal{O}$である。

このとき組$( X, \mathcal{O} )$を位相空間（topological space）と呼び、$\mathcal{O}$を$X$上の位相（topology）あるいは開集合系と呼ぶ。集合$U\in\mathcal{O}$は（$\mathcal{O}$）開（open）という。

例えば$\mathcal{O}=\lbrace \emptyset, X \rbrace$は包含関係における最小の位相を定め、密着位相（indiscrete topology）と呼ばれる。また$\mathcal{O}=2^{X}$は包含関係における最大の位相を定め、離散位相（discrete topology）と呼ばれる。この二つは自明（trivial）な位相とも呼ばれる。

> 位相は「近さの一般化」とよく言われるが、上の定義だとその感覚が良く分からないだろう。実は位相には同値な公理系が複数存在し、そのうちの一つに「近傍系」を利用するものがある。

__定義__ $( X, \mathcal{O} )$を位相空間とする。$F\subset X$が$X\backslash F\in\mathcal{O}$を満たすとき集合$F$は（$\mathcal{O}$）閉（closed）という。

__命題__ 位相空間$( X, \mathcal{O} )$において、閉集合全体$\mathfrak{A}$は以下を満たす。

- $X\in\mathfrak{A}, \emptyset\in\mathfrak{A}$である。
- $F, G\in\mathfrak{A}$なら$F\cup G\in\mathfrak{A}$である。
- $\Lambda$を集合とする。任意の$\lambda\in\Lambda$について$F_{\lambda}\in\mathfrak{A}$なら$\bigcap_{\lambda\in\Lambda}F_{\lambda}\in\mathfrak{A}$である。

逆にこれを満たす$\mathfrak{A}\subset 2^{X}$に対し、$\mathfrak{A}$を閉集合とする$X$上の位相が唯一つ存在する。

__定義__ $( X, \mathcal{O} )$を位相空間、$A\subset X$とする。$x\in X$について以下を定める。

- ある開集合$U\in\mathcal{O}$により$x\in U\subset A$となるとき$x$は$A$の内点という。内点全体を$A^{i}$で表し$A$の内部（interior）と呼ぶ。
- $x$が$X\backslash A$の内点であるとき$x$は$A$の外点という。$A$の外点全体を$A^{e}$で表し$A$の外部（exterior）と呼ぶ。
- $x$が$A$の内点でも外点でもないとき$x$は$A$の境界点という。$A$の境界点全体を$A^{f}$で表し$A$の境界（frontier）と呼ぶ。
- 任意の開集合$U\in\mathcal{O}$について$x\in U$なら$U\cap A\neq\emptyset$が成り立つとき$x$は$A$の触点という。$A$の触点全体を$\overline{A}$あるいは$A^{a}$で表し$A$の閉包（closure）と呼ぶ。

> $A^{i}$は$A$に含まれる最大の開集合であり、$\overline{A}$は$A$を含む最小の閉集合である。

写像$i\colon A\mapsto A^{i}$を開核作用子、写像$k\colon A\mapsto\overline{A}$を閉包作用子という。

__命題__ 位相空間$( X, \mathcal{O} )$の開核作用子$i$を考える。$A, B\subset X$について以下が成り立つ。

- $i( X )=X$である。
- $i( A )\subset A$である。
- $i( A\cap B )=i( A )\cap i( B )$である。
- $i( i( A ) )=i( A )$である。

逆にこれを満たす写像$i$に対し、$i( A )$を$A$の内部とする$X$上の位相が唯一つ存在する。

（証明）$\mathcal{O}:=\lbrace U : i( U )=U \rbrace$とすればよい。$\square$

__命題__ （クラトウスキイの公理系）位相空間$( X, \mathcal{O} )$の閉包作用子$k$を考える。$A, B\subset X$について以下が成り立つ。

- $k( \emptyset )=\emptyset$である。
- $k( A )\supset A$である。
- $k( A\cup B )=k( A )\cup k( B )$である。
- $k( k( A ) )=k( A )$である。

逆にこれを満たす写像$k$に対し、$k( A )$を$A$の閉包とする$X$上の位相が唯一つ存在する。

（証明）$\mathcal{O}:=\lbrace U : k( X\backslash U )=X\backslash U \rbrace$とすればよい。$\square$

__定義__ $( X, \mathcal{O} )$を位相空間、$a\in X$とする。$N\subset X$が$a\in N^{i}$を満たすとき、$a$の近傍（neighborhood）と呼ぶ。$a$の近傍全体を$\mathfrak{N}( a )$で表し、$a$の近傍系と呼ぶ。

__命題__ （ハウスドルフの公理系）位相空間$( X, \mathcal{O} )$の近傍系を考える。$a\in X$について以下が成り立つ。

- $X\in\mathfrak{N}( a )$であり、$N\in\mathfrak{N}( a )$なら$a\in N$である。
- $N, M\in\mathfrak{N}( a )$なら$N\cap M\in\mathfrak{N}( a )$である。
- $N\in\mathfrak{N}( a )$であり、$N\subset M$なら$M\in\mathfrak{N}( a )$である。
- $N\in\mathfrak{N}( a )$について、ある$M\in\mathfrak{N}( a )$が存在し、任意の$b\in M$について$N\in\mathfrak{N}( b )$が成り立つ。

逆にこれを満たす写像$a\mapsto\mathfrak{N}( a )$に対し、$\mathfrak{N}( a )$を$a$の近傍系とする$X$上の位相が唯一つ存在する。 

（証明）$\mathcal{O}:=\lbrace N : a\in N \Rightarrow N\in\mathfrak{N}( a ) \rbrace$とすればよい。$\square$

__定義__ $( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間、$a\in X$とする。写像$f\colon X\rightarrow Y$は以下を満たすとする。

- $N\in\mathfrak{N}( f( a ) )$なら$f^{-1}( N )\in\mathfrak{N}( a )$である。

このとき$f$は$a$において連続（continuous）であるという。

__命題__ $( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間、$f\colon X\rightarrow Y$を写像とする。TFAE

1. 任意の$a\in X$において$f$は連続である。
1. $U\subset Y$が$\mathcal{O}_{Y}$-開集合なら$f^{-1}( U )\subset X$は$\mathcal{O}_{X}$-開集合である。
1. $F\subset Y$が$\mathcal{O}_{Y}$-閉集合なら$f^{-1}( F )\subset X$は$\mathcal{O}_{X}$-閉集合である。
1. 任意の$A\subset X$に対し$f( \overline{A} )\subset\overline{f( A )}$が成り立つ。

__定義__ 上の4条件の何れか（従って全て）を満たすとき、$f$は位相空間$( X, \mathcal{O}_{X} )$から$( Y, \mathcal{O}_{Y} )$への連続写像という。

連続写像の合成は連続写像であり、恒等写像は連続写像である。故に位相空間と連続写像は圏の対象と射を定める。これを位相空間の圏といい圏$\mathbf{Top}$と記す。



## 位相の生成

__定義__ $( X, \mathcal{O} )$を位相空間、$\mathcal{B}\subset\mathcal{O}$とする。任意の開集合$U\in\mathcal{O}$に対し、ある$\mathcal{B}_{0}\subset\mathcal{B}$が存在して$U=\cup\mathcal{B}_{0}$と表せるとき、$\mathcal{B}$は位相$\mathcal{O}$の開基（open basis）であるという。

言い換えれば、任意の開集合$U\in\mathcal{O}$及び$x\in U$に対し、適当な$B\in\mathcal{B}$を取れば$x\in B\subset U$が成り立つようにできる。

__注意__ 集合族$\mathfrak{A}\subset 2^{X}$について$\mathfrak{A}$が空でないときは

$$
\begin{aligned}
\cup\mathfrak{A}&=\bigcup_{A\in\mathfrak{A}}A,& \cap\mathfrak{A}&=\bigcap_{A\in\mathfrak{A}}A
\end{aligned}
$$

と定め、

$$
\begin{aligned}
\cup\emptyset&=\emptyset, & \cap\emptyset&=X
\end{aligned}
$$

と定める。

> 通常の位相を持ったユークリッド空間$\mathbb{R}$の開基としては、例えば開区間全体がある。当然開集合全体も開基であり、位相については様々な開基を考えることが出来る。しかし、開基が定める位相は次の命題より一意的である。

__命題__ $X$を集合、$\mathcal{B}\subset 2^{X}$とする。TFAE

1. $\mathcal{B}$はある位相の開基である。
1. 次の2条件を満たす。
    - $X=\cup\mathcal{B}$である。
	- $B_{1}, B_{2}\in\mathcal{B}$及び$x\in B_{1}\cap B_{2}$について、ある$B\in\mathcal{B}$が存在して$x\in B\subset B_{1}\cap B_{2}$を満たす。

このとき$\mathcal{B}$を開基とする位相は一意的である。

（証明）位相$\mathcal{O}$が$\mathcal{B}$を開基とするなら、

$$
\mathcal{O}=\lbrace \cup\mathfrak{A} : \mathfrak{A}\subset\mathcal{B} \rbrace
$$

という等式を満たさなければならない。一意性はこれより明らか。また下の2条件を満たすとき、この等式で定めた$\mathcal{O}$は位相を定め、$\mathcal{B}$はその開基となる。上から下も簡単。$\square$

> TODO:

__定義__ $( X, \mathcal{O} )$を位相空間とする。位相$\mathcal{O}$が、高々可算個の開集合からなる開基を持つとき、第2可算公理を満たすという。

位相空間に対しても積を考えることが出来る。我々は可測空間において有限積しか今の所は考えていないので、位相空間においても同様に有限積のみを考えることにする。

__定義__ $( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間とする。

$$
\mathcal{O}_{X}\times\mathcal{O}_{Y}=\lbrace U\times V : U\in\mathcal{O}_{X}, V\in\mathcal{O}_{Y} \rbrace\subset 2^{X\times Y}
$$

は開基の2条件を満たし、ある一意的な位相$\mathcal{O}\subset 2^{X\times Y}$の開基となる。この位相を箱型積位相（box product topology）と呼び、$( X\times Y, \mathcal{O} )$を箱型積位相空間という。

> 実は、任意の添え字を持つ位相空間の族について、その直積集合上に積位相と呼ばれる位相を定めることができ、これを積位相空間、あるいは単に積空間と呼ぶ。このとき積空間と各成分への射影は普遍性を満たし、圏$\mathbf{Top}$における積対象となる。積空間の位相は一般的に箱型積位相とは異なるものだが、添え字集合が有限のときには一致する。従って上で定めた箱型積位相空間$( X\times Y, \mathcal{O} )$は、積空間であり、$( X, \mathcal{O}_{X} )$と$( Y, \mathcal{O}_{Y} )$の積対象でもある。これより、以下では「箱型」という用語は省略して述べる。

__命題__ $( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間とする。$\mathcal{B}_{X}, \mathcal{B}_{Y}$を$\mathcal{O}_{X}, \mathcal{O}_{Y}$の開基とすれば、$\mathcal{B}_{X}\times\mathcal{B}_{Y}$は積位相の開基となる。

特に$\mathcal{B}_{X}, \mathcal{B}_{Y}$が可算のとき、$\mathcal{B}_{X}\times\mathcal{B}_{Y}$も可算である。故に有限積は第2可算公理を保つ。

（証明）開基の2条件が成り立つことを示せば良い。$\square$









## TODO

__補題__ （開近傍による開集合の特徴付け）$(X, \mathcal{O})$を位相空間、$U\subset X$とする。TFAE

1. $U\in\mathcal{O}$である。
1. 任意の$x\in U$に対し、ある$V\in\mathcal{O}$が存在して$x\in V\subset U$である。

（証明）$U\in\mathcal{O}$なら$V$として$U$を取ればよい。逆は$x\in X$に対して$S_{x}:=\lbrace V\in\mathcal{O} : x\in V\subset U \rbrace$と置くと、仮定より$S_{x}\neq\emptyset$である。つまり$\exists V_{x}\in S_{x}$だが、集合$\lbrace V_{x} : x\in X \rbrace$を取りたい。ここで選択公理を使っても良いが、実は$V_{x}:=\cup S_{x}$と指定してしまえば必要ない。このとき$V_{x}\in\mathcal{O}$であり$x\in V_{x}\subset U$が成り立つ。従って$U=\bigcup_{x\in X}V_{x}\in\mathcal{O}$である。$\square$