## 位相ライクな概念（近傍、open、closed）

以下、収束空間$X$に対し、$X$のフィルター全体を$\Phi(X)$、真フィルター全体を$\Phi_{\lt 1}(X)$で表す。

### 補拡大

__定義__ $\mathscr{A}\subset 2^{X}$を集合族とする。$S\subset X$は$S\notin\mathscr{A}$を満たすとする。

$$
\mathscr{A}_{\neg S}:=\lbrace V\subset X : \exists A\in\mathscr{A}, A\backslash S\subset V \rbrace
$$

を$\mathscr{A}$の$S$による **補拡大** と呼ぶ。

__命題__ $\mathscr{A}\subset 2^{X}$を集合族とする。$S\subset X$は$S\notin\mathscr{A}$を満たすとする。次が成り立つ。

- $V\in\mathscr{A}_{\neg S}, V\subset W$なら$W\in\mathscr{A}_{\neg S}$である。
- $\mathscr{A}\subset\mathscr{A}_{\neg S}, X\backslash S\in\mathscr{A}_{\neg S}$である。
- フィルター$\mathscr{F}$について$\mathscr{A}\subset\mathscr{F}, X\backslash S\in\mathscr{F}$なら$\mathscr{A}_{\neg S}\subset\mathscr{F}$である。
- $\mathscr{A}$がprefilterなら$\mathscr{A}_{\neg S}$はフィルターである。
- $\mathscr{A}$が真フィルターなら$\mathscr{A}_{\neg S}$は真フィルターである。

（証明）上三つは明らか。

$\mathscr{A}$はprefilterとする。$V, W\in\mathscr{A}_{\neg S}$とする。ある$A, B\in\mathscr{A}$が存在して$A\backslash S\subset V, B\backslash S\subset W$である。

$$
V\cap W\supset (A\backslash S)\cap(B\backslash S)=(A\cap B)\backslash S
$$

が成り立つ。prefilterの性質より、ある$C\in\mathscr{A}$が存在して$(A\cap B)\backslash S\supset C\cap S$である。故に$V\cap W\in\mathscr{A}_{\neg S}$を得る。

$\mathscr{A}$を真フィルターとする。$\emptyset\in\mathscr{A}_{\neg S}$とすると、ある$A\in\mathscr{A}$が存在して$A\backslash S\subset\emptyset$である。$A\subset S$より$S\in\mathscr{A}$となり矛盾する。故に$\emptyset\notin\mathscr{A}_{\neg S}$である。$\square$

> $\mathscr{A}$がprefilterなら、$\mathscr{A}_{\neg S}$は$\mathscr{A}$と$X\backslash S$を含む最小のフィルターである。


### 近傍、open、closed

__定義__ $X$を収束空間とする。$x\in X$に対し、

$$
\mathscr{N}_{x}:=\cap\lbrace \mathscr{F}\in\Phi(X) :  \mathscr{F}\rightarrow x \rbrace
$$

を **近傍フィルター** （neighborhood filter）と呼ぶ。$N\in\mathscr{N}_{x}$を$x$の近傍と呼ぶ。

> 近傍フィルターはフィルターのwedge積だからフィルターである。

__定義__ $X$を収束空間、$U, A\subset X$とする。以下を定める。

- 任意の$x\in U$について$U\in\mathscr{N}_{x}$が成り立つとき、$U$はopenという。
- $\mathrm{cl}(A):=\lbrace x\in X : \exists\mathscr{F}\in\Phi_{\lt 1}(X), A\in\mathscr{F}, \mathscr{F}\rightarrow x \rbrace$と定める。$\mathrm{cl}(A)=A$が成り立つとき、$A$はclosedという。

> 上の$\mathrm{cl}(A)$は$A$の閉包（closure）やKatětov閉包、preclosure、Čech閉包などと呼ばれる。

__命題__ $X$を収束空間、$A, B\subset X$とする。以下が成り立つ。

- $\emptyset, X$はclosedである。
- $A\subset\mathrm{cl}(A)$が成り立つ。
- $A\subset B$なら$\mathrm{cl}(A)\subset\mathrm{cl}(B)$が成り立つ。
- $\mathrm{cl}(A\cup B)=\mathrm{cl}(A)\cup\mathrm{cl}(B)$が成り立つ。特に$A, B$がclosedなら$A\cup B$もclosedである。

（証明）フィルター$\mathscr{F}$が$\emptyset\in\mathscr{F}$を満たすなら$\mathscr{F}=2^{X}$となる。よって$\mathrm{cl}(\emptyset)=\emptyset$である。

$a\in A$に対し、$\langle a \rangle$は真フィルターである。$A\in\langle a \rangle$かつ$\langle a \rangle\rightarrow a$より$a\in\mathrm{cl}(A)$を得る。従って$A\subset\mathrm{cl}(A)$である。特に$A=X$のとき$X\subset\mathrm{cl}(X)\subset X$より$X$はclosedである。

$a\in\mathrm{cl}(A)$とする。真フィルター$\mathscr{F}\rightarrow a$が存在して$A\in\mathscr{F}$を満たす。$A\subset B$より$B\in\mathscr{F}$だから$a\in\mathrm{cl}(B)$である。

$\mathrm{cl}(A)\cup\mathrm{cl}(B)\subset\mathrm{cl}(A\cup B)$は上より明らか。逆に$x\in\mathrm{cl}(A\cup B)$とすると、真フィルター$\mathscr{F}\rightarrow x$が存在して$A\cup B\in\mathscr{F}$を満たす。もし$A\in\mathscr{F}$なら$x\in\mathrm{cl}(A)$となるので命題は示される。$A\notin\mathscr{F}$のとき、$\mathscr{F}$の$A$による補拡大$\mathscr{F}_{\neg A}$を考える。これは$\mathscr{F}$と$X\backslash A$を含む真フィルターなので$(A\cup B)\cap(X\backslash A)\subset B$を含む。故に$B\in\mathscr{F}_{\neg A}$である。一方で$\mathscr{F}\subset\mathscr{F}_{\neg A}$より$\mathscr{F}_{\neg A}\rightarrow x$である。以上より$x\in\mathrm{cl}(B)$を得る。$\square$

> $\mathrm{cl}(\mathrm{cl}(A))=A$を満たせば$\mathrm{cl}$は位相空間における閉包作用素となり位相を定めるが、もちろんこれは一般に成り立たない。

__定理__ $X$を収束空間、$U\subset X$とする。TFAE

1. $U$はopenである。
1. $X\backslash U$はclosedである。

（証明）$U$をopenとする。$x\in\mathrm{cl}(X\backslash U)$とすると、真フィルター$\mathscr{F}\rightarrow x$が存在して$X\backslash U\in\mathscr{F}$である。$x\in U$なら$U\in\mathscr{N}_{x}\subset\mathscr{F}$だが、$\emptyset U\cap(X\backslash U)\in\mathscr{F}$より矛盾する。故に$x\notin U$である。従って$\mathrm{cl}(X\backslash U)\subset X\backslash U$を得る。逆は上の命題より従う。

$U$がopenでないとする。ある$x\in U$が存在して、$U\notin\mathscr{N}_{x}$を満たす。つまりあるフィルター$\mathscr{F}\rightarrow x$が存在して$U\notin\mathscr{F}$である。特に$\mathscr{F}$は真フィルターである。さて、$\mathscr{F}$の$U$による補拡大$\mathscr{F}_{\neg U}$を考える。これは$\mathscr{F}$と$X\backslash U$を含む真フィルターだから、$\mathscr{F}_{\neg U}\rightarrow x$であり、$x\in\mathrm{cl}(X\backslash U)$が分かる。ところで$x\notin X\backslash U$より、$(X\backslash U)\subsetneq\mathrm{cl}(X\backslash U)$である。故に$X\backslash U$はclosedでない。$\square$

__系__ $X$を収束空間とする。以下が成り立つ。

- $\emptyset, X$はopenである。
- $U, V$がopenなら$U\cap V$もopenである。

近傍は位相空間の場合と同じようにclosureを用いて特徴付けることができる。

__命題__ $X$を収束空間とする。$N\subset X, x\in X$とする。TFAE

1. $N$が$x$の近傍である。
1. $x\notin\mathrm{cl}(X\backslash N)$である。

（証明）$x\in\mathrm{cl}(X\backslash N)$なら、真フィルター$\mathscr{F}\rightarrow x$が存在して$X\backslash N\in\mathscr{F}$を満たす。$N\notin\mathscr{F}$だから$N\notin\mathscr{N}_{x}$である。

逆に$N\notin\mathscr{N}_{x}$とする。あるフィルター$\mathscr{F}\rightarrow x$が存在して$N\notin\mathscr{F}$である。$\mathscr{F}$は真フィルターだから$\mathscr{F}$の$N$による補拡大$\mathscr{F}_{\neg N}$は$\mathscr{F}$と$X\backslash N$を含む真フィルターとなる。このとき$\mathscr{F}_{\neg N}\rightarrow x$より$x\in\mathrm{cl}(X\backslash N)$である。$\square$

次に連続射との関係をみていく。位相空間とは異なり、連続性をopenやclosedで特徴付けることはできない。

__命題__ $f\colon X\rightarrow Y$は連続とする。このとき次が成り立つ。

- $U\subset Y$がopenなら、$f^{-1}(U)\subset X$もopenである。
- $F\subset Y$がclosedなら、$f^{-1}(F)\subset X$もclosedである。
- $A\subset X$について$f(\mathrm{cl}(A))\subset\mathrm{cl}(f(A))$が成り立つ。

（証明）$f(x)\in U$とする。フィルター$\mathscr{F}\rightarrow x$について、$f$は連続だから$f_{\ast}\mathscr{F}\rightarrow f(x)$である。$U$はopenなので$U\in f_{\ast}\mathscr{F}$となるが、ある$V\in\mathscr{F}$が存在して$f(V)\subset U$を満たす。$V\subset f^{-1}(f(V))\subset f^{-1}(U)$だから、$f^{-1}(U)\in\mathscr{F}$である。よって$f^{-1}(U)$はopenである。

$F\subset Y$がclosedなら$Y\backslash F$はopenである。今示したように$f^{-1}(Y\backslash F)=X\backslash f^{-1}(F)$もopenである。故に$f^{-1}(F)$はclosedである。

$x\in\mathrm{cl}(A)$について$y=f(x)$とする。ある真フィルター$\mathscr{F}\rightarrow x$が存在して$A\in\mathscr{F}$である。このとき$f_{\ast}\mathscr{F}$は真フィルターだが、$f$は連続なので$f_{\ast}\mathscr{F}\rightarrow f(x)=y$であり$f(A)\in f_{\ast}\mathscr{F}$である。従って$y\in\mathrm{cl}( f(A) )$を得る。$\square$


### 例：反射的有向グラフ

反射的有向グラフの収束空間$(V, E)$に関して、上記の概念を求めてみよう。

まずは近傍フィルターを考える。フィルター$\mathscr{F}$について$\mathscr{F}\rightarrow v$の定義は$\overrightarrow{v}\in\mathscr{F}$である。このとき$F\supset\overrightarrow{v}$なら$F\in\mathscr{F}$より$\langle \overrightarrow{v} \rangle\subset\mathscr{F}$が成り立つ。特に$\langle \overrightarrow{v} \rangle\rightarrow v$だから、結局$\mathscr{N}_{v}=\langle \overrightarrow{v} \rangle$が分かる。

$U$がopenであるとは任意の$v\in U$について$U\in\langle \overrightarrow v \rangle$つまり$\overrightarrow{v}\subset U$が成り立つことだから、これが全ての$v\in U$で成り立つということは、矢印の先を辿れるところまで$U$が全て含むことを意味する。

連続ではないがopenの逆像がopenとなる例は例えば次のようなものがある。$a, b, c$を頂点として、$a\rightarrow b\rightarrow c\rightarrow a$というサイクルで定まる収束空間を$Y$とする。それぞれ双方向としたものを$X$とする。$f\colon X\rightarrow Y$を頂点上の恒等写像とすると、グラフ準同型ではないので連続でない。しかしopenな部分集合はどちらも$\lbrace a, b, c \rbrace, \emptyset$のみなので、openの逆像はopenである。