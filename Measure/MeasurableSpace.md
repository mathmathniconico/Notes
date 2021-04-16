
# 可測空間と測度空間



## 可測空間

__定義__ $S$を集合とする。$\mathscr{A}\subset 2^{S}$は以下を満たすとする。

- $\emptyset\in\mathscr{A}$である。
- $A\in\mathscr{A}$なら$S\backslash A\in\mathscr{A}$である。
- $A_{n}\in\mathscr{A}$なら$\bigcup_{n\in\mathbb{N}}A_{n}\in\mathscr{A}$である。

このとき$\mathscr{A}$は$S$上の$\sigma$ **加法族**と呼び、組$( S, \mathscr{A} )$を **可測空間** （measurable space）と呼ぶ。$A\subset S$は$A\in\mathscr{A}$のとき$\mathscr{A}$可測あるいは単に可測という。

> 定義に解釈を求めても仕方ないが、可算という視点で物事を捉える、というのが測度論の基本的な考え方とするならば、有限の立場で議論する論理学（特に命題論理）のアナロジーという意味で、この定義は自然である。

$\sigma$加法族は歴史的な経緯から呼び方が安定しない。例えば完全加法族、可算加法族、$\sigma$-集合代数、$\sigma$-集合体、$\sigma$-体、トライブ（tribe）などと呼ばれている。

- $\lbrace \emptyset, S \rbrace$や$2^{S}$は$\sigma$加法族である。

$\sigma$加法族は基本的な集合演算に関して閉じている。可測な集合の差集合$A\backslash B$（$A, B\in\mathscr{A}$）や可算交叉$\bigcap_{n\in\mathbb{N}}A_{n}$（$A_{n}\in\mathscr{A}$）などは全て可測である。

__命題__ 写像$f\colon S\rightarrow T$について以下が成り立つ。

- $( T, \mathscr{B} )$が可測空間なら$f^{\flat}\mathscr{B}:=\lbrace f^{-1}( B ) : B\in\mathscr{B} \rbrace$は$S$上の$\sigma$加法族となる。
- $( S, \mathscr{A} )$が可測空間なら$f^{\sharp}\mathscr{A}:=\lbrace B\subset T : f^{-1}( B )\in\mathscr{A} \rbrace$は$T$上の$\sigma$加法族となる。

> $f^{\sharp}\mathscr{A}$は$\lbrace f( A ) : A\in\mathscr{A} \rbrace$ではないことに注意。

__定義__ $( S, \mathscr{A} ), ( T, \mathscr{B} )$を可測空間とする。写像$f\colon S\rightarrow T$が$f^{\flat}\mathscr{B}\subset\mathscr{A}$を満たすとき、つまり任意の$B\in\mathscr{B}$について$f^{-1}( B )\in\mathscr{A}$を満たすとき、$f$は$(\mathscr{A}, \mathscr{B})$可測、あるいは単に **可測** （measurable）であるという。

> 可測空間と可測写像は圏を為す。これを$\mathbf{meas}$と記す。
