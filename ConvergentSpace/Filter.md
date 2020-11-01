
# フィルターとprefilter

## フィルター

__定義__ $X$を集合とする。$\mathscr{F}\subset 2^{X}$が以下を満たすとき$X$の **フィルター** と呼ぶ。

- $X\in\mathscr{F}$である。
- $V\in\mathscr{F}, V\subset W$なら$W\in\mathscr{F}$である。
- $V, W\in\mathscr{F}$なら$V\cap W\in\mathscr{F}$である。

フィルター$\mathscr{F}$について、$\emptyset\in\mathscr{F}$と$\mathscr{F}=2^{X}$は同値になる。

- $\emptyset\in\mathscr{F}$のとき、 **自明フィルター** と呼ぶ。
- $\emptyset\notin\mathscr{F}$のとき、 **真フィルター** と呼ぶ。

> 基本的には真フィルターが本質的であり、自明フィルターは理論的な完備さに対応している。

例えば次のようなものがある。

- $\lbrace X \rbrace$は$X$のフィルターである。$2^{X}$も$X$のフィルターである。
- 集合$X$において$X\backslash S$が有限となる$S\subset X$全体はフィルターである。このようなフィルターを補有限フィルターという。$X$が有限集合のときは自明フィルターであり、無限集合のときは真フィルターである。

__命題__ 集合族$\mathscr{S}\subset 2^{X}$について、$\mathscr{S}$を含む最小のフィルターが存在する。

（証明）任意の$n\in\mathbb{N}$と有限個の$S_{1}, \dotsc, S_{n}\in\mathscr{S}$について$S_{1}\cap\dotsm\cap S_{n}$を含む集合全体を考えればよい。ただし$n=0$の場合は交叉を全体集合$X$としておく。つまり

$$
\lbrace F\subset X : \exists n\in\mathbb{N}, \exists S_{1}, \dotsc, S_{n}\in\mathscr{S}, S_{1}\cap\dotsb\cap S_{n}\subset F \rbrace
$$

は$\mathscr{S}$を含む最小のフィルターとなる。$\square$

> $\langle \emptyset \rangle=\lbrace X \rbrace$である。

__定義__ $\mathscr{S}$を含む最小のフィルターを$\langle \mathscr{S} \rangle$と表し、$\mathscr{S}$が **生成するフィルター** と呼ぶ。

- 最小性より、フィルター$\mathscr{F}$について$\langle \mathscr{F} \rangle=\mathscr{F}$である。

$A\subset X$について$\lbrace A \rbrace$が生成するフィルターを **単項フィルター** と呼び、誤解の恐れが無い場合は$\langle A \rangle$と表す。特に$x\in X$について$A=\lbrace x \rbrace$が生成するフィルターを **点フィルター** と呼び、同様に$\langle x \rangle$と表す。

> フィルターは素朴な概念なので、これ以上のことは何も言えない。しかしその素朴さから数学の様々な場面で用いられ、豊富な付加構造を伴うことが重要である。


## prefilter

真フィルターより弱い概念を導入する。

__定義__ $\mathscr{B}\subset 2^{X}, \neq\emptyset$が以下を満たすとき$X$の **prefilter** と呼ぶ。

- $A, B\in\mathscr{B}$なら、ある$C\in\mathscr{B}$が存在して$C\subset A\cap B$が成り立つ。

同様に$\emptyset\notin\mathscr{B}$のとき **真prefilter** と呼ぶ。

> フィルターの場合と異なり、$\emptyset\in\mathscr{B}$だからといって自明（$\mathscr{B}=2^{X}$）とは限らない。

- フィルターはprefilterである。真フィルターは真prefilterである。

__命題__ $\mathscr{B}\subset 2^{X}$をprefilterとする。このとき

$$
\langle \mathscr{B} \rangle=\lbrace F\subset X : \exists B\in\mathscr{B}, B\subset F \rbrace
$$

が成り立ち、特に右辺は$\mathscr{B}$を含む最小のフィルターである。

更に$\mathscr{B}$が真prefilterのとき$\langle \mathscr{B} \rangle$は真フィルターである。

（証明）左辺が右辺を含むことは定義より明らか。$F\in\langle \mathscr{B} \rangle$とすると、$B_{1}, \dotsc, B_{n}\in\mathscr{B}$が存在して$B_{1}\cap\dotsm\cap B_{n}\subset F$となる。prefilterの定義から$n$を一つずつ減らすことができて、結局ある$B\in\mathscr{B}$が存在して$B\subset F$となる。（$n=0$の場合は$\mathscr{B}\neq\emptyset$より従う。）

$\emptyset\in\langle \mathscr{B} \rangle$とすると、ある$B\in\mathscr{B}$が存在して$B\subset\emptyset$である。故に$B\in\mathscr{B}$が従う。$\square$


## 補拡大

様々な場所で用いられるテクニックとして補拡大というものがある。

__定義__ $\mathscr{A}\subset 2^{X}$を集合族とする。$S\subset X$は$S\notin\mathscr{A}$を満たすとする。

$$
\mathscr{A}_{\neg S}:=\lbrace V\subset X : \exists A\in\mathscr{A}, A\backslash S\subset V \rbrace
$$

を$\mathscr{A}$の$S$による **補拡大** と呼ぶ。

__命題__ $\mathscr{A}\subset 2^{X}$を集合族とする。$S\subset X$は$S\notin\mathscr{A}$を満たすとする。次が成り立つ。

- $V\in\mathscr{A}_{\neg S}, V\subset W$なら$W\in\mathscr{A}_{\neg S}$である。
- $\mathscr{A}\subset\mathscr{A}_{\neg S}, X\backslash S\in\mathscr{A}_{\neg S}$である。
- フィルター$\mathscr{F}$について$\mathscr{A}\subset\mathscr{F}, X\backslash S\in\mathscr{F}$なら$\mathscr{A}_{\neg S}\subset\mathscr{F}$である。
- $\mathscr{A}$がprefilterなら$\mathscr{A}_{\neg S}$はフィルターである。特に$\mathscr{A}_{\neg S}$は$\mathscr{A}$と$X\backslash S$を含む最小のフィルターである。
- $\mathscr{A}$が真フィルターなら$\mathscr{A}_{\neg S}$は真フィルターである。

（証明）上三つは明らか。

$\mathscr{A}$はprefilterとする。$V, W\in\mathscr{A}_{\neg S}$とする。ある$A, B\in\mathscr{A}$が存在して$A\backslash S\subset V, B\backslash S\subset W$である。prefilterの定義より、ある$C\in\mathscr{A}$が存在して$C\subset A\cap B$である。

$$
C\backslash S\subset (A\cap B)\backslash S=(A\backslash S)\cap (B\backslash S)\subset  V\cap W
$$

より$V\cap W\in\mathscr{A}_{\neg S}$を得る。最小性は明らかだろう。

$\mathscr{A}$を真フィルターとする。$\emptyset\in\mathscr{A}_{\neg S}$とすると、ある$A\in\mathscr{A}$が存在して$A\backslash S\subset\emptyset$である。$A\subset S$より$S\in\mathscr{A}$となり矛盾する。故に$\emptyset\notin\mathscr{A}_{\neg S}$である。$\square$

