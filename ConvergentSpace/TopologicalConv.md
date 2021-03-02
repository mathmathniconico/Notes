
# 位相空間の収束構造（位相収束構造）

位相空間$(X, \mathcal{O})$において$x\in X$の近傍系$\mathfrak{N}(x)$はフィルターである。そこで$X$の収束構造$\mathscr{F}\rightarrow x$を$\mathfrak{N}({x})\subset\mathscr{F}$で定めることができる。実際$N\in\mathfrak{N}(x)$なら$x\in N$より$N\in\langle x \rangle$だから$\langle x \rangle\rightarrow x$である。$\mathscr{F}\rightarrow x, \mathscr{F}\subset\mathscr{G}$について$\mathfrak{N}(x)\subset\mathscr{F}\subset\mathscr{G}$より$\mathscr{G}\rightarrow x$である。また$\mathfrak{N}(x)\subset\mathscr{F}, \mathscr{G}$なら$\mathfrak{N}(x)\subset\mathscr{F}\cap\mathscr{G}$も成り立つ。特に$\mathfrak{N}(x)\rightarrow x$である。

__定義__ 上記の収束構造を$F\mathcal{O}$と表し **$\mathcal{O}$収束構造** と呼ぶ。

__命題__ $(X, \mathcal{O})$を位相空間とする。以下が成り立つ。

- $x\in X$について$\mathscr{N}_{x}=\mathfrak{N}(x)$が成り立つ。特に$\mathscr{N}_{x}\rightarrow x$である。
- $TF\mathcal{O}=\mathcal{O}$が成り立つ。特に$x\in X$について$\mathfrak{N}_{x}=\mathfrak{N}(x)$が成り立つ。
- $A\subset X$について$\mathrm{pcl}(A)=\overline{A}$が成り立つ。

（証明）$\mathscr{N}_{x}$は$\mathfrak{N}(x)\subset\mathscr{F}$を満たすフィルター$\mathscr{F}$たちの共通部分と等しい。特に$\mathfrak{N}(x)\rightarrow x$だから$\mathscr{N}_{x}=\mathfrak{N}(x)$が成り立つ。

$U\in TF\mathcal{O}$とする。$x\in U$について、$U$はopenだから$U\in\mathscr{N}_{x}=\mathfrak{N}(x)$である。よって開集合$V\in\mathcal{O}$が存在して$x\in V\subset U$を満たす。開近傍による開集合の特徴付けより$U\in\mathcal{O}$である。逆に$U\in\mathcal{O}$とする。$x\in U$について$U\in\mathfrak{N}(x)=\mathscr{N}_{x}$だから$U$はopenである。故に$U\in TF\mathcal{O}$である。

$A\subset\mathrm{pcl}(A)\subset\overline{A}$より、preclosureが閉集合であることを示せば良い。$x\in X\backslash\mathrm{pcl}(A)$とする。$A=X\backslash (X\backslash A)$より$X\backslash A\in\mathscr{N}_{x}=\mathfrak{N}(x)$である。よってある開集合$U\in\mathcal{O}$が存在して$x\in U\subset X\backslash A$が成り立つ。$y\in U$について$U$はopenだから$U\in\mathscr{N}_{y}$より$y\notin\mathrm{pcl}(X\backslash U)$となる。$A\subset X\backslash U$だから$y\notin\mathrm{pcl}(A)$が分かる。$x\in U\subset X\backslash\mathrm{pcl}(A)$だから、開近傍による開集合の特徴付けより$X\backslash\mathrm{pcl}(A)\in\mathcal{O}$が従う。$\square$

> 位相空間$(X, \mathcal{O})$に対して、$\mathcal{O}$収束構造に関する隣接位相$TF\mathcal{O}$は元の位相$\mathcal{O}$と一致し、隣接フィルター$\mathscr{N}_{x}$及び隣接位相の近傍系$\mathfrak{N}_{x}$は元の位相の近傍系$\mathfrak{N}(x)$と一致する。そして$\mathcal{O}$収束構造に関するpreclosureは元の位相における閉包と一致する。

__補題__ $(X, \mathcal{O}_{X}), (Y, \mathcal{O}_{Y})$を位相空間とする。以下が成り立つ。

- 連続写像$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$について、$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$が成り立つ。
- 連続射$f\colon (X, F\mathcal{O}_{X})\rightarrow (Y, F\mathcal{O}_{Y})$について、$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$が成り立つ。

（証明）$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$を連続写像とする。$N\in\mathfrak{N}(f(x))$なら、ある開集合$U\in\mathcal{O}_{Y}$が存在して$x\in U\subset N$を満たす。このとき$x\in f^{-1}(U)\subset f^{-1}(N)$だが、$f$は連続写像なので$f^{-1}(U)\in\mathcal{O}_{X}$である。よって$f^{-1}(N)\in\mathfrak{N}(x)$であり、$f(f^{-1}(N))\subset N$より$N\in f_{\ast}\mathfrak{N}(x)$が従う。

$f\colon (X, F\mathcal{O}_{X})\rightarrow (Y, F\mathcal{O}_{Y})$を連続射とする。$\mathfrak{N}(x)\rightarrow x$より$f_{\ast}\mathfrak{N}(x)\rightarrow f(x)$である。故に$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$を得る。$\square$

__命題__ $(X, \mathcal{O}_{X}), (Y, \mathcal{O}_{Y})$を位相空間、$f\colon X\rightarrow Y$を写像とする。TFAE

1. $f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$は連続写像である。
1. $f\colon (X, F\mathcal{O}_{X})\rightarrow (Y, F\mathcal{O}_{Y})$は連続射である。

（証明）$f$を連続写像とする。$X$において$\mathscr{F}\rightarrow x$つまり$\mathfrak{N}(x)\subset\mathscr{F}$とすると、補題より$\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)\subset f_{\ast}\mathscr{F}$となる。故に$f_{\ast}\mathscr{F}\rightarrow f(x)$を得る。

$f$を連続射とする。$U\in\mathcal{O}_{Y}$とする。$x\in f^{-1}(U)$について、$U$はopenだから補題より$U\in\mathscr{N}_{f(x)}=\mathfrak{N}(f(x))\subset f_{\ast}\mathfrak{N}(x)$である。故にある$V\in\mathfrak{N}(x)$が存在して$f(V)\subset U$を満たす。特に$V$は開集合としてよい。$x\in V\subset f^{-1}(f(V))\subset f^{-1}(U)$が成り立つ。開近傍による開集合の特徴付けより$f^{-1}(U)\in\mathcal{O}_{X}$を得る。$\square$

> 以上より$\mathbf{Top}$から$\mathbf{Conv}$への函手を定義できる。

__定義__ 函手$F\colon\mathbf{Top}\rightarrow\mathbf{Conv}$を以下で定義する。

- 位相空間$(X, \mathcal{O})$について、収束空間$(X, F\mathcal{O})$を対応させる。
- 連続写像$f\colon X\rightarrow Y$について、連続射$f\colon X\rightarrow Y$を対応させる。

__定理__ 函手$F$は忠実充満である。更に$T\circ F=\mathrm{id}_{\mathbf{Top}}$が成り立つ。

（証明）位相空間$(X, \mathcal{O})$について、$TF(X, \mathcal{O})=T(X, F\mathcal{O})=(X, TF\mathcal{O})$である。$TF\mathcal{O}=\mathcal{O}$より対象の間は恒等になる。また$T$も$F$も射の対応は写像として変わらないので忠実であり、$T\circ F$が射の間も恒等になることが分かる。$F$の充満性は連続写像と連続射の同値性より従う。$\square$

__命題__ $(X, \phi)$を収束空間、$(Y, \mathcal{O}_{Y})$を位相空間とする。$\mathbf{Conv}$において同型$(X, \phi)\simeq (Y, F\mathcal{O}_{Y})$が成り立つなら、$X$の位相$\mathcal{O}_{X}$が存在して、$T\phi=\mathcal{O}_{X}$かつ$\mathbf{Top}$において同型$(X, \mathcal{O}_{X})\simeq (Y, \mathcal{O}_{Y})$が成り立つ。

（証明）$f\colon (X, \phi)\rightarrow (Y, F\mathcal{O}_{Y})$を同型とする。$U\in\mathcal{O}_{X}$を$f(U)\in\mathcal{O}_{Y}$で定めると位相になる。実際$f(X)=Y\in\mathcal{O}_{Y}$及び$f(\emptyset)=\emptyset\in\mathcal{O}_{Y}$が成り立つ。また$f(U), f(V)\in\mathcal{O}_{Y}$なら$f(U\cap V)=f(U)\cap f(V)\in\mathcal{O}_{Y}$である。$f(U_{\lambda})\in\mathcal{O}_{Y}$なら$f(\bigcup U_{\lambda})=\bigcup f(U_{\lambda})\in\mathcal{O}_{Y}$である。

$U\in\mathcal{O}$とする。$f(U)\in\mathcal{O}_{Y}=TF\mathcal{O}_{Y}$だから$f(U)$は$F\mathcal{O}_{Y}$でopenである。$f$は同型なので$U$も$\phi$でopenである。故に$U\in T\phi$である。逆も同様だから$\mathcal{O}=T\phi$である。

$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$が$\mathbf{Top}$の同型を与えることは、連続写像と連続射の同値性より従う。$\square$

> 従って$\mathbf{Top}$を$\mathbf{Conv}$のstrictly full subcategoryとみなせる。つまり真の意味で$\mathbf{Top}$を$\mathbf{Conv}$の一部として扱うことができる。