
# 可測空間と測度空間



## 可測空間

__定義__ $S$を集合とする。$\mathscr{A}\subset 2^{S}$は以下を満たすとする。

- $\emptyset\in\mathscr{A}$である。
- $A\in\mathscr{A}$なら$S\backslash A\in\mathscr{A}$である。
- $A_{n}\in\mathscr{A}$なら$\bigcup_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$である。

このとき$\mathscr{A}$は$S$上の$\sigma$**加法族**と呼び、組$( S, \mathscr{A} )$を **可測空間** （measurable space）と呼ぶ。このとき$A\in\mathscr{A}$は$\mathscr{A}$可測あるいは単に可測であるという。

> 定義に解釈を求めても仕方ないが、可算という視点で物事を捉える、というのが測度論の基本的な考え方とするならば、有限の立場で議論する論理学（特に命題論理）のアナロジーという意味で、この定義は自然である。

$\sigma$加法族は歴史的な経緯から呼び方が安定しない。例えば完全加法族、可算加法族、$\sigma$-集合代数、$\sigma$-集合体、$\sigma$-体、トライブ（tribe）などと呼ばれている。

- $\lbrace \emptyset, S \rbrace$や$2^{S}$は$\sigma$加法族である。

$\sigma$加法族は基本的な集合演算に関して閉じている。可測な集合の差集合$A\backslash B$（$A, B\in\mathscr{A}$）や可算交叉$\bigcap_{n\in\mathbb{N}}A_{n}$（$A_{n}\in\mathscr{A}$）などは全て可測である。

__命題__ 写像$f\colon S\rightarrow T$について以下が成り立つ。

- $( T, \mathscr{B} )$が可測空間なら$f^{\flat}\mathscr{B}:=\lbrace f^{-1}( B ) : B\in\mathscr{B} \rbrace$は$S$上の$\sigma$加法族となる。
- $( S, \mathscr{A} )$が可測空間なら$f^{\sharp}\mathscr{A}:=\lbrace B\subset T : f^{-1}( B )\in\mathscr{A} \rbrace$は$T$上の$\sigma$加法族となる。

> $f^{\sharp}\mathscr{A}$は$\lbrace f( A ) : A\in\mathscr{A} \rbrace$ではないことに注意。

__定義__ $( S, \mathscr{A} ), ( T, \mathscr{B} )$を可測空間とする。写像$f\colon S\rightarrow T$が$f^{\flat}\mathscr{B}\subset\mathscr{A}$を満たすとき、つまり任意の$B\in\mathscr{B}$について$f^{-1}( B )\in\mathscr{A}$を満たすとき、$f$は$(\mathscr{A}, \mathscr{B})$可測、あるいは単に **可測** （measurable）であるという。

> 可測空間と可測写像は圏を為す。これを$\mathbf{Meas}$と記す。




## $\sigma$加法族の生成と可測空間の積

次に可測空間$X=( S, \mathscr{A} )$と可測空間$Y=( T, \mathscr{B} )$の対象としての積$X\prod Y$を考えたい。射が全体空間における写像であることを考えれば、あるいは集合の圏$\mathbf{Set}$への忘却函手の存在を考えれば、積対象の全体空間は$S\times T$で定めるのが妥当だろう。更に射影$p\colon X\prod^{\mathrm{cat}}Y\rightarrow X$の存在を考慮すると、少なくとも$A\times T, S\times B$（$A\in\mathscr{A}, B\in\mathscr{B}$）の形をした集合は可測となる必要がある。しかし一般にこれらの集合は$\sigma$加法族を成さない。このような場合には生成という方法が有効になる。

まず$\sigma$加法族の任意の交叉は$\sigma$加法族である。つまり任意の$\lambda\in\Lambda$について$\mathscr{A}_{\lambda}$を$\sigma$加法族とすると、$\bigcap_{\lambda\in\Lambda}\mathscr{A}_{\lambda}$も$\sigma$加法族となる。そこで生成を次のように定義する。

__定義__ $\mathscr{G}\subset 2^{S}$について、$\mathscr{G}$を含む$S$上の$\sigma$加法族全体の交叉を$\sigma\lbrack \mathscr{G} \rbrack_{S}$あるいは$\sigma\lbrack \mathscr{G} \rbrack$と記し、$\mathscr{G}$により$S$上で **生成** （generate）された$\sigma$加法族と呼ぶ。このとき$A\in\sigma\lbrack \mathscr{G} \rbrack$は$\mathscr{G}$-可測であるという。

値域の可測性が生成により与えられているとき、写像の可測性は生成元のみを考えれば十分である。

__命題__ $( S, \mathscr{A} ), ( T, \sigma\lbrack \mathscr{G} \rbrack )$を可測空間、$f\colon S\rightarrow T$を写像とする。TFAE

- $f$は可測である。
- 任意の$G\in\mathscr{G}$について$f^{-1}( G )\in\mathscr{A}$である。

（証明）上から下は明白。下が成り立つとすると、任意の$G\in\mathscr{G}$について$G\in f( \mathscr{A} )$が成り立つ。すなわち$\mathscr{G}\subset f( \mathscr{A} )$となるが、今$f( \mathscr{A} )$は$\sigma$加法族であるから、生成の最小性より$\sigma\lbrack \mathscr{G} \rbrack\subset f( \mathscr{A} )$が従う。これは$f$が可測であることを表している。$\square$

__定義__ $(\mathscr{A}\times T)\cup (S\times\mathscr{B})=\lbrace A\times T, S\times B : A\in\mathscr{A}, B\in\mathscr{B} \rbrace$により生成される$S\times T$上の$\sigma$加法族を$\mathscr{A}\prod\mathscr{B}$と記し、積$\sigma$加法族という。また組$( S\times T, \mathscr{A}\prod\mathscr{B} )$を積可測空間という。

積可測空間は圏$\mathbf{Meas}$における積対象である。実際次のように普遍性が成り立つ。

__命題__ $( P, \mathscr{F} )$を可測空間、$f\colon P\rightarrow S, g\colon P\rightarrow T$を可測写像とする。このとき唯一つの可測写像$h\colon P\rightarrow S\times T$が存在して、図式を可換にする。

（証明）$h( x ):=( f( x ), g( x ) )$と定めればよい。可測性は先の命題より$A\in\mathscr{A}, B\in\mathscr{B}$について$h^{-1}( A\times T ), h^{-1}( S\times B )\in\mathscr{F}$を示せばよいが、例えば

$$
h^{-1}( A\times T )=f^{-1}( A )\cap g^{-1}( T )\in\mathscr{F}
$$

より$f, g$の可測性から従う。逆に図式を可換にする$h$はこのような形をしていなければならない。$\square$

三つ以上の積についても普遍性を示すことが出来る。つまり圏$\mathbf{Meas}$は有限積を持つ圏である。

__命題__ $\mathscr{G}\subset 2^{S}, \mathscr{H}\subset 2^{T}$に対し、$\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack = \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack$が成り立つ。

（証明）

$$
\sigma\lbrack \mathscr{G} \rbrack\times T\cup S\times\sigma\lbrack \mathscr{H} \rbrack \supset \mathscr{G}\times T\cup S\times\mathscr{H}
$$

である。故に生成すれば最小性から

$$
\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack \supset \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

が従う。

逆を示すために$\sigma\lbrack \mathscr{G} \rbrack\times T\subset\sigma\lbrack \mathscr{G}\times T \rbrack$を示す。射影$\mathrm{proj}\colon S\times T\rightarrow S$を考えれば

$$
\begin{align*}
\mathrm{proj}\left( \sigma\lbrack \mathscr{G}\times T \rbrack \right) &= \left\lbrace A\subset S : A\times T\in\sigma\lbrack \mathscr{G}\times T \rbrack \right\rbrace \\
&\supset \lbrace A\subset S : A\times T\in\mathscr{G}\times T \rbrace = \mathscr{G}
\end{align*}
$$


となる。故に最小性より$\mathrm{proj}\left( \sigma\lbrack \mathscr{G}\times T \rbrack \right)\supset\sigma\lbrack \mathscr{G} \rbrack$を得る。つまり

$$
\sigma\lbrack \mathscr{G} \rbrack\times T\subset\sigma\lbrack \mathscr{G}\times T \rbrack\subset\sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

が従う。$S\times\sigma\lbrack \mathscr{H} \rbrack$についても同様だから、

$$
\sigma\lbrack \mathscr{G} \rbrack\times T\cup S\times\sigma\lbrack \mathscr{H} \rbrack \subset \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack
$$

が分かる。故に最小性より$\sigma\lbrack \mathscr{G} \rbrack\otimes\sigma\lbrack \mathscr{H} \rbrack \subset \sigma\lbrack \mathscr{G}\times T\cup S\times\mathscr{H} \rbrack$が従う。$\square$

