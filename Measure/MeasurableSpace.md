
# 可測空間と測度空間



## 可測空間

__定義__ $S$を集合とする。$\mathscr{A}\subset 2^{S}$は以下を満たすとする。

- $\emptyset\in\mathscr{A}$である。
- $A\in\mathscr{A}$なら$S\backslash A\in\mathscr{A}$である。
- $A_{n}\in\mathscr{A}$なら$\bigcup_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$である。

このとき$\mathscr{A}$は$S$上の$\sigma$ **加法族** （additive class of sets）と呼び、組$( S, \mathscr{A} )$を **可測空間** （measurable space）と呼ぶ。このとき$A\in\mathscr{A}$は$\mathscr{A}$可測あるいは単に可測であるという。

> 可算という視点で物事を捉える、というのが測度論の基本的な考え方である。これは有限の立場で議論する論理学（特に命題論理）のアナロジーと思うことができる。

$\sigma$加法族は歴史的な経緯から呼び方が安定しない。例えば完全加法族、可算加法族、$\sigma$-集合代数、$\sigma$-集合体、$\sigma$-体、トライブ（tribe）などと呼ばれている。

- $\lbrace \emptyset, S \rbrace$や$2^{S}$は$\sigma$加法族である。

__命題__ $\mathscr{A}\subset 2^{S}$を$\sigma$加法族とする。

- $A, B\in\mathscr{A}$について$A\backslash B\in\mathscr{A}$である。
- $A_{n}\in\mathscr{A}$について$\bigcap_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$である。

（証明）$X\in\mathscr{A}$より従う。$\square$

__命題__ 写像$f\colon S\rightarrow T$について以下が成り立つ。

- $( T, \mathscr{B} )$が可測空間なら$f^{\flat}\mathscr{B}:=\lbrace f^{-1}( B ) : B\in\mathscr{B} \rbrace$は$S$上の$\sigma$加法族となる。
- $( S, \mathscr{A} )$が可測空間なら$f^{\sharp}\mathscr{A}:=\lbrace B\subset T : f^{-1}( B )\in\mathscr{A} \rbrace$は$T$上の$\sigma$加法族となる。

> $f^{\sharp}\mathscr{A}$は$\lbrace f( A ) : A\in\mathscr{A} \rbrace$ではないことに注意。

__定義__ $( S, \mathscr{A} ), ( T, \mathscr{B} )$を可測空間とする。写像$f\colon S\rightarrow T$は以下を満たすとする。

- $f^{\flat}\mathscr{B}\subset\mathscr{A}$である。つまり任意の$B\in\mathscr{B}$について$f^{-1}( B )\in\mathscr{A}$である。

このとき$f$は$(\mathscr{A}, \mathscr{B})$可測、あるいは単に **可測** （measurable）であるという。

> 可測空間と可測写像は圏を為す。これを$\mathbf{meas}$と記す。




## $\sigma$加法族の生成と可測空間の積

与えられた集合族を含むような$\sigma$加法族が欲しいとき、生成という手法が有効である。まず次が成り立つ。

- $\sigma$加法族の任意の交叉は$\sigma$加法族である。つまり任意の$\lambda\in\Lambda$について$\mathscr{A}_{\lambda}$を$\sigma$加法族とすると、$\bigcap_{\lambda\in\Lambda}\mathscr{A}_{\lambda}$も$\sigma$加法族となる。

そこで生成を次のように定義する。

__定義__ $\mathscr{G}\subset 2^{S}$について、$\mathscr{G}$を含む$S$上の$\sigma$加法族全体の交叉を$\sigma\lbrack \mathscr{G} \rbrack_{S}$あるいは$\sigma\lbrack \mathscr{G} \rbrack$と記し、$\mathscr{G}$により$S$上で **生成** （generate）された$\sigma$加法族と呼ぶ。このとき$A\in\sigma\lbrack \mathscr{G} \rbrack$は$\mathscr{G}$可測であるという。

値域の可測性が生成により与えられているとき、写像の可測性は生成元のみを考えれば十分である。

__命題__ $( S, \mathscr{A} ), ( T, \sigma\lbrack \mathscr{G} \rbrack )$を可測空間、$f\colon S\rightarrow T$を写像とする。TFAE

1. $f$は可測である。
1. 任意の$G\in\mathscr{G}$について$f^{-1}( G )\in\mathscr{A}$である。

（証明）$f$を$(\mathscr{A}, \sigma\lbrack \mathscr{G} \rbrack)$可測とする。$f^{\flat}\sigma\lbrack \mathscr{G} \rbrack\subset\mathscr{A}$より、任意の$B\in\sigma\lbrack \mathscr{G} \rbrack$について$f^{-1}(B)\in\mathscr{A}$である。特に$G\in\mathscr{G}\subset\sigma\lbrack \mathscr{G} \rbrack$より$f^{-1}(G)\in\mathscr{A}$である。

下が成り立つとすると、$\mathscr{G}\subset f^{\sharp}\mathscr{A}$である。$f^{\sharp}\mathscr{A}$は$\sigma$加法族だから、生成の最小性より$\sigma\lbrack \mathscr{G} \rbrack\subset f^{\sharp}\mathscr{A}$を得る。任意の$B\in\sigma\lbrack \mathscr{G} \rbrack$について$B\in f^{\sharp}\mathscr{A}$より$f^{-1}(B)\in\mathscr{A}$である。これは$f$が$(\mathscr{A}, \sigma\lbrack \mathscr{G} \rbrack)$可測であることに他ならない。$\square$

生成の応用として、可測空間の直積について考える。可測空間$( S, \mathscr{A} )$と可測空間$( T, \mathscr{B} )$の直積は、$S\times T$上の$\sigma$加法族を、射影が可測写像となるように定義すれば良い。

__定義__ $\mathscr{A}\times T\cup S\times\mathscr{B}=\lbrace A\times T, S\times B : A\in\mathscr{A}, B\in\mathscr{B} \rbrace$により生成される$S\times T$上の$\sigma$加法族を$\mathscr{A}\otimes\mathscr{B}$と記し、積$\sigma$加法族という。また組$( S\times T, \mathscr{A}\otimes\mathscr{B} )$を積可測空間という。

次のように普遍性が成り立つ。つまり積可測空間は圏$\mathbf{meas}$における積対象である。

__命題__ $f\colon P\rightarrow S, g\colon P\rightarrow T$を可測写像とする。このとき唯一つの可測写像$h\colon P\rightarrow S\times T$が存在して、射影と図式を可換にする。つまり$p\colon S\times T\rightarrow S, q\colon S\times T\rightarrow T$を射影とすれば$f=h\circ p, g=h\circ q$が成り立つ。

（証明）$h( x ):=( f( x ), g( x ) )$と定める。可測性は先の命題より$A\in\mathscr{A}, B\in\mathscr{B}$について$h^{-1}( A\times T ), h^{-1}( S\times B )\subset P$が可測であることを示せばよいが、例えば$h^{-1}( A\times T )=f^{-1}( A )\cap g^{-1}( T )$より$f, g$の可測性から従う。逆に図式を可換にする$h$はこのような形をしていなければならない。$\square$

> 三つ以上の積についても普遍性を示すことが出来る。つまり圏$\mathbf{meas}$は有限積を持つ圏である。

__命題__ $\mathscr{G}\subset 2^{S}, \mathscr{H}\subset 2^{T}$に対し、$\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack = \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack$が成り立つ。

（証明）$\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack$は$(\sigma\lbrack \mathscr{G} \rbrack\times T)\cup (S\times\sigma\lbrack \mathscr{H} \rbrack )$により生成される$\sigma$加法族である。これは$(\mathscr{G}\times T)\cup(S\times\mathscr{H})$を含むので、生成の最小性より

$$
\sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack\subset\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack
$$

を得る。

逆を示したい。まず$\sigma\lbrack \mathscr{G} \rbrack\times T$は$\mathscr{G}\times T$を含む$\sigma$加法族なので$\sigma\lbrack \mathscr{G} \rbrack\times T=\sigma\lbrack \mathscr{G}\times T \rbrack$である。故に

$$
\sigma\lbrack \mathscr{G} \rbrack\times T=\sigma\lbrack \mathscr{G}\times T \rbrack\subset\sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

である。$S\times\sigma\lbrack \mathscr{H} \rbrack$についても同様だから、

$$
\sigma\lbrack \mathscr{G} \rbrack\times T\cup S\times\sigma\lbrack \mathscr{H} \rbrack \subset \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

を得る。生成の最小性より$\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack \subset \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack$を得る。$\square$




## 測度空間

測度とは、長さや面積、体積といった概念の抽象化あるいは精密化である。$\sigma$加法族と違い簡単には作ることができないため、適切な集合族の上で定義された「前測度」を拡張して構成されることが多い。ここでは単純に$\lbrack 0, \infty \rbrack$値のものを考える。


集合$A, B$は$A\cap B=\emptyset$のとき **互いに素** （coprime）であるという。二つ以上についても同様に定める。

__定義__ $S$を空でない集合とする。集合族$\mathscr{G}\subset 2^{S}$は空集合を含むとする。写像$\mu\colon\mathscr{G}\rightarrow\lbrack 0, \infty \rbrack$を集合函数という。更に以下を定める。

- $\mu( \emptyset )=0$のとき$\mu$は **正値** （positive）という。
- $A_{1}, \dotsc, A_{m}\in\mathscr{G}$は互いに素とする。$A:=\bigsqcup_{i=1}^{m}A_{i}\in\mathscr{G}$なら$\mu( A )=\sum_{i=1}^{m}\mu( A_{i} )$であるとき、$\mu$は **有限加法的** （finite-additive）という。
- $\lbrace A_{n} \rbrace_{n\in\mathbb{N}}\subset\mathscr{G}$は互いに素とする。$A:=\bigsqcup_{n\in\mathbb{N}} A_{n}\in\mathscr{G}$なら$\mu( A )=\sum_{n\in\mathbb{N}}\mu( A_{n} )$であるとき、$\mu$は **可算加法的** （countable-additive）という。

__定義__ $\mathscr{A}\subset 2^{S}$を$\sigma$加法族とする。集合函数$\mu\colon\mathscr{A}\rightarrow\lbrack 0, \infty \rbrack$が正値かつ可算加法的とする。このとき$\mu$は$\mathscr{A}$上の **測度** （measure）あるいは可測空間$( S, \mathscr{A} )$上の測度と呼び、組$( S, \mathscr{A}, \mu )$を **測度空間** （measure space）と呼ぶ。

例えば次のようなものがある。

- 可測な集合に対して$0$を対応させる写像は測度になる。これを自明測度と呼ぶ。
- $A\in\mathscr{A}$が有限集合なら元の個数を対応させ、無限集合のときは$\infty$を対応させると測度になる。これを **数え上げ測度** （counting measure）と呼ぶ。
- $x\in S$に対して写像$\delta_{x}\colon\mathscr{A}\rightarrow\lbrack 0, \infty \rbrack$を、$x\in A$なら$\delta_{x}( A )=1$と定め、$x\notin A$なら$\delta_{x}( A )=0$と定めると測度になる。これを **ディラック測度** （Dirac's measure）と呼ぶ。

> 測度空間を対象とする圏を考える際、射の範囲が問題になる。$( S, \mathscr{A}, \mu_{S} ), ( T, \mathscr{B}, \mu_{T} )$を測度空間、$f\colon S\rightarrow T$を可測写像とする。
> 
> - 任意の$B\in\mathscr{B}$について$\mu_{S}( f^{-1}( B ) )=\mu_{T}( B )$を満たす（測度保存な）可測写像を射とする圏を$\mathbf{Meas}_{=}$と記す。
> - 任意の$B\in\mathscr{B}$について$\mu_{S}( f^{-1}( B ) )\le\mu_{T}( B )$を満たす（測度増大な）可測写像を射とする圏を$\mathbf{Meas}_{\le}$と記す。
> - 任意の可測写像を射とする圏を$\mathbf{Meas}$と記す。
> 
> とはいえ実際には上記のような圏を考える状況は限られており、通常は位相や群演算などの付加的な構造を加味した圏を調べることが多い。