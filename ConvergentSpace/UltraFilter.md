
# 超フィルターと準コンパクト


## 超フィルター

__定義__ $X$の真フィルターに関して、包含順序で極大なものを **超フィルター** （ultra filter）と呼ぶ。

点フィルターは超フィルターである。実際$\langle x \rangle\subsetneq\mathscr{F}$なるフィルターを取ると、ある$F\in\mathscr{F}$が存在して$F\notin\langle x \rangle$である。つまり$F$は$\lbrace x \rbrace$を含まないので$x\notin F$である。一方$\lbrace x \rbrace\in\mathscr{F}$より$F\cap\lbrace x \rbrace=\emptyset\in\mathscr{F}$となり$\mathscr{F}$は自明である。

__定理__ 真フィルター$\mathscr{F}\subset 2^{X}$について、$\mathscr{F}$を含む超フィルターが存在する。

（証明）$X$のフィルター全体を$\Phi(X)$とする。$\Psi:=\lbrace \mathscr{G}\in\Phi(X) : \mathscr{F}\subset\mathscr{G}\neq 2^{X} \rbrace$の全順序部分集合$\tau$を考える。このとき$\bigcup_{\mathscr{A}\in\tau}\mathscr{A}$は真フィルターであり、$\tau$の$\Psi$における上界を与えている。故に$\Psi$は帰納的で、Zornの補題より極大元$\mathscr{U}$が存在する。これは$\mathscr{F}$を含む超フィルターである。$\square$

超フィルターは次の特徴付けを持つ。

__補題__ $\mathscr{U}\subset 2^{X}$をフィルターとする。TFAE

- $\mathscr{U}$は超フィルターである。
- $A\subset X$について$A\in\mathscr{U}$か$X\backslash A\in\mathscr{U}$のどちらか一方が成り立つ。

（証明）下を仮定する。$\mathscr{U}\subsetneq\mathscr{V}$なるフィルターを取ると、ある$V\in\mathscr{V}$が存在して$V\notin\mathscr{U}$である。仮定より$X\backslash V\in\mathscr{U}\subset\mathscr{V}$だから、$V\cap(X\backslash V)=\emptyset\in\mathscr{V}$より$\mathscr{V}$は自明である。

$\mathscr{U}$を超フィルターとする。$A\notin\mathscr{U}$について$\mathscr{U}_{\neg A}$は$\mathscr{U}, X\backslash A$を含む真フィルターである。極大性より$\mathscr{U}=\mathscr{U}_{\neg A}$となり$X\backslash A\in\mathscr{U}$を得る。$\square$

> 真フィルター$\mathscr{F}$に対して、$S\notin\mathscr{F}$の補集合$X\backslash S$を次々と添加していくことができた。この操作はどこまで可能だろうか。この補題はその疑問に対する解答が超フィルターであることを表している。

__命題__ 以下が成り立つ。

- $\mathscr{U}\subset 2^{X}$を超フィルターとする。$S_{1}, \dotsc, S_{n}\subset X$について$S_{1}\cup\dotsb\cup S_{n}\in\mathscr{U}$なら、ある$j$が存在して$S_{j}\in\mathscr{U}$が成り立つ。
- $\mathscr{U}_{1}, \dotsc, \mathscr{U}_{n}\subset 2^{X}$を超フィルターとする。超フィルター$\mathscr{V}\subset 2^{X}$について$\mathscr{U}_{1}\cap\dotsb\cap\mathscr{U}_{n}\subset\mathscr{V}$なら、ある$j$について$\mathscr{V}=\mathscr{U}_{j}$が成り立つ。
- 真フィルター$\mathscr{F}\subset 2^{X}$について、$\mathscr{F}$は$\mathscr{F}$を含む超フィルターの共通部分と一致する。

（証明）$n$に関する帰納法で示す。$n=2$のとき$S_{1}, S_{2}\notin\mathscr{U}$とする。補題より$X\backslash S_{1}, X\backslash S_{2}\in\mathscr{U}$である。しかし$X\backslash (S_{1}\cup S_{2})=(X\backslash S_{1})\cap (X\backslash S_{2})\in\mathscr{U}$より$S_{1}\cup S_{2}\notin\mathscr{U}$を得る。$n=k+1$のとき$(S_{1}\cup\dotsb\cup S_{k})\cup S_{k+1}\in\mathscr{U}$とする。$S_{k+1}\notin\mathscr{U}$なら$n=2$の場合より$S_{1}\cup\dotsb\cup S_{k}\in\mathscr{U}$となる。

任意の$j$について$\mathscr{V}\neq\mathscr{U}_{j}$とする。$\mathscr{V}$は超フィルターだから$\mathscr{U}_{j}$に含まれない、つまりある$U_{j}\in\mathscr{U}_{j}$が存在して$U_{j}\notin\mathscr{V}$を満たす。つまり$X\backslash U_{j}\in\mathscr{V}$である。

$$
X\backslash \left( \bigcup_{k=1}^{n}U_{k} \right)=\bigcap_{k=1}^{n}(X\backslash U_{k})\in\mathscr{V}
$$

より$U:=\bigcup_{k=1}^{n}U_{k}\notin\mathscr{V}$である。ところが$U_{j}\subset U$より$U\in\mathscr{U}_{j}$を得る。つまり$U\in\mathscr{U}_{1}\cap\dotsb\cap\mathscr{U}_{n}\subset\mathscr{V}$となり矛盾する。

$\mathscr{F}$を含む超フィルターの共通部分を$\Upsilon$とする。（wedge積なので真フィルターである。）$\mathscr{F}\subset\Upsilon$は明らかなので逆を示す。ある$U\in\Upsilon$が存在して$U\notin\mathscr{F}$とする。このとき$\mathscr{F}_{\neg U}$は$\mathscr{F}, X\backslash U$を含む真フィルターである。$\mathscr{F}_{\neg U}$を含む超フィルターの一つを$\mathscr{V}$とする。$\mathscr{F}\subset\mathscr{F}_{\neg U}\subset\mathscr{V}$より$\Upsilon\subset\mathscr{V}$である。$U\in\Upsilon\subset\mathscr{V}$だが、$X\backslash U\in\mathscr{F}_{\neg U}\subset\mathscr{V}$となり矛盾する。$\square$

> 上の事実を有限の場合に確認しておこう。

__命題__ $\mathscr{U}\subset 2^{X}$を超フィルターとする。$\mathscr{U}$が有限集合を持つなら$\mathscr{U}$は点フィルターである。

（証明）$\mathscr{U}$の有限集合のうち元の個数が最小のものを$F\in\mathscr{U}$とする。$G\subsetneq F$について$G\notin\mathscr{U}$だから、$\mathscr{U}_{\neg G}$は$\mathscr{U}$を含む真フィルターとなる。極大性より$\mathscr{U}=\mathscr{U}_{\neg G}$だが、$F\in\mathscr{U}$より$F\backslash G\in\mathscr{U}_{\neg G}=\mathscr{U}$である。$F$の最小性より$G=\emptyset$でなければならず、従って$F$は一元集合でなければならない。点フィルターは超フィルターだから$\langle F \rangle=\mathscr{U}$を得る。$\square$

特に$X$が有限集合のとき以下が成り立つ。

- 超フィルターと点フィルターは同値である。
- 真フィルターは単項フィルターである。

一つ目は上の命題より明白。二つ目は元の個数が最小の要素を取ればよい。

> 有限集合$X$において、真フィルターは単項フィルターだから、これを$\langle A \rangle$とすれば$A=\lbrace a_{1}, \dotsc, a_{n} \rbrace$と表せる。このとき$\langle A \rangle=\langle a_{1} \rangle\cap\dotsb\cap\langle a_{n} \rangle$が成り立ち、右辺の点フィルターは超フィルターである。

__命題__ $f\colon X\rightarrow Y$を写像とする。以下が成り立つ。

- $\mathscr{U}\subset 2^{X}$を超フィルターとすると、$f_{\ast}\mathscr{U}\subset 2^{Y}$も超フィルターである。
- $\mathscr{F}\subset 2^{X}$を真フィルターとする。$f_{\ast}\mathscr{F}$を含む超フィルター$\mathscr{V}\subset 2^{Y}$について、ある$X$の超フィルター$\mathscr{U}\subset 2^{X}$が存在して$\mathscr{F}\subset\mathscr{U}$かつ$f_{\ast}\mathscr{U}=\mathscr{V}$を満たす。

（証明）$W\notin f_{\ast}\mathscr{U}$とする。$f(f^{-1}(W))\subset W$より$f^{-1}(W)\notin\mathscr{U}$である。超フィルターの特徴付けより$X\backslash f^{-1}(W)\in\mathscr{U}$を得る。$f(X\backslash f^{-1}(W))\subset Y\backslash W$より$Y\backslash W\in f_{\ast}\mathscr{U}$である。

$V\in\mathscr{V}$について$X\in\mathscr{F}$より$f(X)\subset Y\backslash V$なら$Y\backslash V\in f_{\ast}\mathscr{F}\subset\mathscr{V}$より矛盾する。故に$f^{-1}(V)\neq\emptyset$であり、従って$f^{\ast}\mathscr{V}$は真フィルターである。更に$\mathscr{F}$と$f^{\ast}\mathscr{V}$はmeshである。実際$F\in\mathscr{F}$及び$V\in\mathscr{V}$について$f(F)\cap V=\emptyset$なら$f(F)\subset Y\backslash V$より$Y\backslash V\in f_{\ast}\mathscr{F}\subset\mathscr{V}$となり矛盾する。以上より$\mathscr{F}\vee f^{\ast}\mathscr{V}$は真フィルターである。これを含む超フィルター$\mathscr{U}$を取れば、$\mathscr{F}\subset\mathscr{U}$であり、$\mathscr{V}\subset f_{\ast}(f^{\ast}\mathscr{V})\subset f_{\ast}\mathscr{U}$と極大性より$\mathscr{V}=f_{\ast}\mathscr{U}$を得る。$\square$

> このように超フィルターは像についてよく振舞う。

__命題__ $f\colon X\rightarrow Y$は全射とする。$Y$の超フィルター$\mathscr{V}\subset 2^{Y}$について、ある$X$の超フィルター$\mathscr{U}\subset 2^{X}$が存在して$f\mathscr{U}=\mathscr{V}$が成り立つ。

（証明）$f^{-1}\mathscr{V}$は真prefilterだから、それを含む真フィルターが存在し、さらにそれを含む超フィルター$\mathscr{U}$が存在する。このとき$f\mathscr{U}\supset f(f^{-1}\mathscr{V})=\mathscr{V}$より$f\mathscr{U}=\mathscr{V}$となる。$\square$





## 準コンパクト

__定義__ 収束空間$X$において、任意の超フィルターが収束するとき$X$は **準コンパクト** （quasi-compact）であるという。

> 収束空間$X$が有限集合なら準コンパクトである。実際有限集合において超フィルターは点フィルターなので、その点に収束する。

__命題__ 連続射$f\colon X\rightarrow Y$は全射とする。$X$が準コンパクトなら$Y$も準コンパクトである。

（証明）$\mathscr{V}\subset 2^{Y}$を$Y$の超フィルターとする。ある$X$の超フィルター$\mathscr{U}$が存在して$f\mathscr{U}=\mathscr{V}$である。$X$は準コンパクトだから$\mathscr{U}\rightarrow x$であり、$f$は連続なので$\mathscr{V}=f\mathscr{U}\rightarrow f(x)$となる。$\square$

__定理__ （チコノフの定理）$X_{i}$を収束空間、$X=\prod_{i\in I}X_{i}$をその直積とする。TFAE

1. $X_{i}$は準コンパクトである。
1. $X$は準コンパクトである。

（証明）$X$の超フィルター$\mathscr{U}$を取る。射影$p_{i}$は全射だから$p_{i}\mathscr{U}$は像フィルターであり、故に超フィルターである。$X_{i}$が準コンパクトとすると、ある$x_{i}\in X_{i}$が存在して$p_{i}\mathscr{U}\rightarrow x_{i}$となる。従って$x=(x_{i})$と置くと、$\mathscr{U}\rightarrow x$を得る。逆は$p_{i}$が全射かつ連続射であることから従う。$\square$

> このように収束空間においてはチコノフの定理を簡単に示せるが、もちろんこの準コンパクト性の概念が位相的なものと一致していることを示すべきだろう。

__命題__ 以下が成り立つ。

- 収束空間$(X, \phi)$が準コンパクトなら、位相空間$(X, T\phi)$は位相的準コンパクトである。
- 位相空間$(X, \mathcal{O})$が位相的準コンパクトなら、収束空間$(X, F\mathcal{O})$は準コンパクトである。

（証明）$(X, T\phi)$が位相的準コンパクトでないとする。つまりopenな$U_{i}$（$i\in I$）による被覆が存在して、有限個では覆えないとする。有限部分集合$J\subset I$について$A_{J}:=X\setminus\bigcup_{j\in J}U_{j}\neq\emptyset$と定める。$\lbrace A_{J} \rbrace$が生成するフィルターを$\mathscr{F}$とすると真フィルターとなる。よって$\mathscr{F}$を含む超フィルター$\mathscr{U}$が存在する。もし$(X, \phi)$が準コンパクトなら$\mathscr{U}\rightarrow x$となる$x\in X$が存在するが、$\lbrace U_{i} : i\in I \rbrace$は被覆なので$x\in U_{k}$となる$k\in I$が存在する。$U_{k}$はopenより$U_{k}\in\mathscr{U}$だが、$A_{\lbrace k \rbrace}=X\setminus U_{k}\in\mathscr{U}$より矛盾する。

$(X, F\mathcal{O})$が準コンパクトでないとする。位相収束構造において、収束しない超フィルター$\mathscr{U}$が存在する。任意の$x\in X$について$\mathfrak{N}(x)\not\subset\mathscr{U}$だから、ある$U_{x}\in\mathfrak{N}(x)$が存在して$U_{x}\notin\mathscr{U}$を満たす。更にある開集合$V_{x}\in\mathcal{O}$が存在して$x\in V_{x}\subset U_{x}$となる。特に$V_{x}\notin\mathscr{U}$だから超フィルターの特徴付けより$X\setminus V_{x}\in\mathscr{U}$が分かる。$(X, \mathcal{O})$が位相的準コンパクトなら$X=\bigcup_{x\in X}V_{x}$より、有限個を選んで$X=V_{x_{1}}\cup\dotsb\cup V_{x_{n}}$とできる。ところが$(X\setminus V_{x_{1}})\cap\dotsb\cap(X\setminus V_{x_{n}})=\emptyset\in\mathscr{U}$より矛盾する。$\square$

