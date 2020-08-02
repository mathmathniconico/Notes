
## 超フィルター

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

__定義__ $X$の真フィルターに関して、包含順序で極大なものを **超フィルター** （ultra filter）と呼ぶ。

点フィルターは超フィルターである。実際$\langle x \rangle\subsetneq\mathscr{F}$なるフィルターを取ると、ある$F\in\mathscr{F}$が存在して$F\notin\langle x \rangle$である。つまり$F$は$\lbrace x \rbrace$を含まないので$x\notin F$である。一方$\lbrace x \rbrace\in\mathscr{F}$より$F\cap\lbrace x \rbrace=\emptyset\in\mathscr{F}$となり$\mathscr{F}$は自明である。

__定理__ 真フィルター$\mathscr{F}\subset 2^{X}$について、$\mathscr{F}$を含む超フィルターが存在する。

（証明）$X$のフィルター全体を$\Phi(X)$とする。$\Psi:=\lbrace \mathscr{G}\in\Phi(X) : \mathscr{F}\subset\mathscr{G}\neq 2^{X} \rbrace$の全順序部分集合$\tau$を考える。このとき$\bigcup_{\mathscr{A}\in\tau}\mathscr{A}$は真フィルターであり、$\tau$の$\Psi$における上界を与えている。故に$\Psi$は帰納的で、Zornの補題おり極大元$\mathscr{U}$を持つ。これは$\mathscr{F}$を含む超フィルターである。$\square$

超フィルターは次の特徴付けを持つ。

__補題__ $\mathscr{U}\subset 2^{X}$をフィルターとする。TFAE

- $\mathscr{U}$は超フィルターである。
- $A\subset X$について$A\in\mathscr{U}$か$X\backslash A\in\mathscr{U}$のどちらか一方が成り立つ。

（証明）下を仮定する。$\mathscr{U}\subsetneq\mathscr{V}$なるフィルターを取ると、ある$V\in\mathscr{V}$が存在して$V\notin\mathscr{U}$である。仮定より$X\backslash V\in\mathscr{U}\subset\mathscr{V}$だから、$V\cap(X\backslash V)=\emptyset\in\mathscr{V}$より$\mathscr{V}$は自明である。

$\mathscr{U}$を超フィルターとする。$A\notin\mathscr{U}$について$\mathscr{U}_{\neg A}$は$\mathscr{U}, X\backslash A$を含む真フィルターである。極大性より$\mathscr{U}=\mathscr{U}_{\neg A}$となり$X\backslash A\in\mathscr{U}$を得る。$\square$

> 真フィルター$\mathscr{F}$に対して、$S\notin\mathscr{F}$の補集合$X\backslash S$を次々と添加していくことができた。この操作はどこまで可能だろうか。補題によれば、その疑問に対する解答が超フィルターである。

__命題__ $\mathscr{U}\subset 2^{X}$を超フィルターとする。$S_{1}, \dotsc, S_{n}\subset X$について$S_{1}\cup\dotsb S_{n}\in\mathscr{U}$なら、ある$j$が存在して$S_{j}\in\mathscr{U}$が成り立つ。

（証明）$n$に関する帰納法で示す。$n=2$のとき$S_{1}, S_{2}\notin\mathscr{U}$とする。補題より$X\backslash S_{1}, X\backslash S_{2}\in\mathscr{U}$である。しかし$X\backslash (S_{1}\cup S_{2})=(X\backslash S_{1})\cap (X\backslash S_{2})\in\mathscr{U}$より$S_{1}\cup S_{2}\notin\mathscr{U}$を得る。$n=k+1$のとき$(S_{1}\cup\dotsb\cup S_{k})\cup S_{k+1}\in\mathscr{U}$とする。$S_{k+1}\notin\mathscr{U}$なら$n=2$の場合より$S_{1}\cup\dotsb\cup S_{k}\in\mathscr{U}$となる。$\square$

__命題__ $\mathscr{U}_{1}, \dotsc, \mathscr{U}_{n}\subset 2^{X}$を超フィルターとする。超フィルター$\mathscr{V}\subset 2^{X}$について$\mathscr{U}_{1}\cap\dotsb\cap\mathscr{U}_{n}\subset\mathscr{V}$なら、ある$j$について$\mathscr{V}=\mathscr{U}_{j}$が成り立つ。

（証明）任意の$j$について$\mathscr{V}\neq\mathscr{U}_{j}$とする。$\mathscr{V}$は超フィルターだから$\mathscr{U}_{j}$に含まれない、つまりある$U_{j}\in\mathscr{U}_{j}$が存在して$U_{j}\notin\mathscr{V}$を満たす。つまり$X\backslash U_{j}\in\mathscr{V}$である。

$$
X\backslash \left( \bigcup_{k=1}^{n}U_{k} \right)=\bigcap_{k=1}^{n}(X\backslash U_{k})\in\mathscr{V}
$$

より$U:=\bigcup_{k=1}^{n}U_{k}\notin\mathscr{V}$である。ところが$U_{j}\subset U$より$U\in\mathscr{U}_{j}$を得る。つまり$U\in\mathscr{U}_{1}\cap\dotsb\cap\mathscr{U}_{n}\subset\mathscr{V}$となり矛盾する。$\square$

__命題__ $\mathscr{U}\subset 2^{X}$を超フィルターとする。$\mathscr{U}$が有限集合を持つなら$\mathscr{U}$は点フィルターである。

（証明）$\mathscr{U}$の有限集合のうち元の個数が最小のものを$F\in\mathscr{U}$とする。$G\subsetneq F$について$G\notin\mathscr{U}$だから、$\mathscr{U}_{\neg G}$は$\mathscr{U}$を含む真フィルターとなる。極大性より$\mathscr{U}=\mathscr{U}_{\neg G}$だが、$F\in\mathscr{U}$より$F\backslash G\in\mathscr{U}_{\neg G}=\mathscr{U}$である。$F$の最小性より$G=\emptyset$でなければならず、従って$F$は一元集合でなければならない。点フィルターは超フィルターだから$\langle F \rangle=\mathscr{U}$を得る。$\square$

$X$が有限集合のとき以下が成り立つ。

- 超フィルターと点フィルターは同値である。
- 真フィルターは単項フィルターである。

一つ目は上の命題より明白。二つ目は元の個数が最小の要素を取ればよい。

> $X$が有限集合のとき、任意の真フィルターは単項フィルターである。これを$\langle A \rangle$とすれば$A=\lbrace a_{1}, \dotsc, a_{n} \rbrace$と表せる。このとき$\langle A \rangle=\langle a_{1} \rangle\cap\dotsb\cap\langle a_{n} \rangle$が成り立ち、右辺の点フィルターは超フィルターである。つまり超フィルターの共通部分として真フィルターが表される。実は一般にこの事実が成立する。

__命題__ 真フィルター$\mathscr{F}\subset 2^{X}$について、$\mathscr{F}$は$\mathscr{F}$を含む超フィルターの共通部分と一致する。

（証明）$\mathscr{F}$を含む超フィルターの共通部分を$\Upsilon$とする。（wedge積なので真フィルターである。）$\mathscr{F}\subset\Upsilon$は明らかなので逆を示す。ある$U\in\Upsilon$が存在して$U\notin\mathscr{F}$とする。このとき$\mathscr{F}_{\neg U}$は$\mathscr{F}, X\backslash U$を含む真フィルターである。$\mathscr{F}_{\neg U}$を含む超フィルターの一つを$\mathscr{V}$とする。$\mathscr{F}\subset\mathscr{F}_{\neg U}\subset\mathscr{V}$より$\Upsilon\subset\mathscr{V}$である。$U\in\Upsilon\subset\mathscr{V}$だが、$X\backslash U\in\mathscr{F}_{\neg U}\subset\mathscr{V}$となり矛盾する。$\square$