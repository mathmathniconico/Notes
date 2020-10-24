
# 位相空間の収束構造

$X$を位相空間とする。$x\in X$の近傍系$\mathfrak{N}(x)$はフィルターである。

そこで$X$の収束構造$\mathscr{F}\rightarrow x$を$\mathfrak{N}({x})\subset\mathscr{F}$で定めることができる。実際$N\in\mathfrak{N}(x)$なら$x\in N$より$N\in\langle x \rangle$だから$\langle x \rangle\rightarrow x$である。$\mathscr{F}\rightarrow x, \mathscr{F}\subset\mathscr{G}$について$\mathfrak{N}(x)\subset\mathscr{F}\subset\mathscr{G}$より$\mathscr{G}\rightarrow x$である。また$\mathfrak{N}(x)\subset\mathscr{F}, \mathscr{G}$なら$\mathfrak{N}(x)\subset\mathscr{F}\cap\mathscr{G}$も成り立つ。特に$\mathfrak{N}(x)\rightarrow x$である。

__定義__ 上記の収束構造を **位相より誘導される収束構造** と呼ぶ。

__命題__ $(X, \mathcal{O})$を位相空間、$\phi$を誘導される収束構造とする。以下が成り立つ。

- $x\in X$について$\mathscr{N}_{x}=\mathfrak{N}(x)$が成り立つ。特に$\mathscr{N}_{x}\rightarrow x$である。
- $\mathcal{O}_{\phi}=\mathcal{O}$が成り立つ。特に$x\in X$について$\mathfrak{N}_{x}=\mathfrak{N}(x)$が成り立つ。

（証明）$\mathscr{N}_{x}$は$\mathfrak{N}(x)\subset\mathscr{F}$を満たすフィルター$\mathscr{F}$たちの共通部分と等しい。特に$\mathfrak{N}(x)\rightarrow x$だから$\mathscr{N}_{x}=\mathfrak{N}(x)$が成り立つ。

$U\in\mathcal{O}_{\phi}$とする。$x\in U$について、$U$はopenだから$U\in\mathscr{N}_{x}=\mathfrak{N}(x)$である。よって開集合$V_{x}\in\mathcal{O}$が存在して$x\in V_{x}\subset U$を満たす。選択公理よりこのような$V_{x}$を取れば$U=\bigcup_{x\in U}V_{x}$だから$U\in\mathcal{O}$である。逆に$U\in\mathcal{O}$とする。$x\in U$について$U\in\mathfrak{N}(x)=\mathscr{N}_{x}$だから$U$はopenである。故に$U\in\mathcal{O}_{\phi}$である。$\square$

> 位相空間$(X, \mathcal{O})$において、誘導される収束構造に関するフィルター開位相$\mathcal{O}_{\phi}$は元の位相$\mathcal{O}$と一致し、元の位相の近傍系$\mathfrak{N}(x)$と隣接フィルター$\mathscr{N}_{x}$及びフィルター開位相の近傍系$\mathfrak{N}_{x}$は一致する。

__補題__ $(X, \mathcal{O}_{X}), (Y, \mathcal{O}_{Y})$を位相空間、$\phi_{X}, \phi_{Y}$を各々の誘導される収束構造とする。以下が成り立つ。

- 連続写像$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$について、$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$が成り立つ。
- 連続射$f\colon (X, \phi_{X})\rightarrow (Y, \phi_{Y})$について、$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$が成り立つ。

（証明）$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$を連続写像とする。$N\in\mathfrak{N}(f(x))$なら、ある開集合$U\in\mathcal{O}_{Y}$が存在して$x\in U\subset N$を満たす。このとき$x\in f^{-1}(U)\subset f^{-1}(N)$だが、$f$は連続写像なので$f^{-1}(U)\in\mathcal{O}_{X}$である。よって$f^{-1}(N)\in\mathfrak{N}(x)$であり、$f(f^{-1}(N))\subset N$より$N\in f_{\ast}\mathfrak{N}(x)$が従う。

$f\colon (X, \phi_{X})\rightarrow (Y, \phi_{Y})$を連続射とする。$\mathfrak{N}(x)\rightarrow x$より$f_{\ast}\mathfrak{N}(x)\rightarrow f(x)$である。故に$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$を得る。$\square$

__命題__ $(X, \mathcal{O}_{X}), (Y, \mathcal{O}_{Y})$を位相空間、$\phi_{X}, \phi_{Y}$を各々の誘導される収束構造とする。$f\colon X\rightarrow Y$を写像とする。TFAE

1. $f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$は連続写像である。
1. $f\colon (X, \phi_{X})\rightarrow (Y, \phi_{Y})$は連続射である。

（証明）$f$を連続写像とする。$X$において$\mathscr{F}\rightarrow x$つまり$\mathfrak{N}(x)\subset\mathscr{F}$とすると、補題より$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)\subset f_{\ast}\mathscr{F}$となる。故に$f_{\ast}\mathscr{F}\rightarrow f(x)$を得る。

$f$を連続射とする。$U\in\mathcal{O}_{Y}$とする。$x\in f^{-1}(U)$について、$U$はopenだから補題より$U\in\mathscr{N}_{f(x)}=\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$である。故にある$V_{x}\in\mathfrak{N}(x)$が存在して$f(V_{x})\subset U$を満たす。特に$V_{x}$は開集合としてよい。$x\in V_{x}\subset f^{-1}(f(V))\subset f^{-1}(U)$が成り立つ。選択公理より$f^{-1}(U)\in\mathcal{O}_{X}$を得る。$\square$

__定義__ 函手$F\colon\mathbf{Top}\rightarrow\mathbf{Conv}$を以下で定義する。

- 位相空間$(X, \mathcal{O})$について、$\phi$を誘導される収束構造として、収束空間$(X, \phi)$を対応させる。
- 連続写像$f\colon X\rightarrow Y$について、連続射$f\colon X\rightarrow Y$を対応させる。

__定理__ 函手$F$は忠実充満である。更に$T\circ F=\mathrm{id}_{\mathbf{Top}}$が成り立つ。

（証明）位相空間$(X, \mathcal{O})$と誘導される収束構造$\phi$について、$TF(X, \mathcal{O})=T(X, \phi)=(X, \mathcal{O}_{\phi})$である。$\mathcal{O}_{\phi}=\mathcal{O}$より対象の間は恒等になる。また$T$も$F$も射の対応は写像として変わらないので忠実であり、$T\circ F$が射の間も恒等になることが分かる。$F$の充満性は連続写像と連続射の同値性より従う。$\square$
