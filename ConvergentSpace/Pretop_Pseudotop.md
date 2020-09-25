
__命題__ $X$を収束空間とする。$x\in X$の近傍系を$\mathfrak{N}_{x}$とする。このとき次が成り立つ。

- $\mathfrak{N}_{x}\subset\mathscr{N}_{x}$が成り立つ。
- $N\in\mathscr{N}_{x}\Longleftrightarrow x\notin\mathrm{pcl}(X\backslash N)$が成り立つ。

（証明）$N\in\mathfrak{N}_{x}$とすると、ある開集合$U\in\mathcal{O}$が存在して$x\in U\subset N$を満たす。$U$はopenだから$U\in\mathscr{N}_{x}$である。よって$N\in\mathscr{N}_{x}$である。

$N\in\mathscr{N}_{x}$とする。$x\in\mathrm{pcl}(X\backslash N)$なら、真フィルター$\mathscr{F}\rightarrow x$が存在して$X\backslash N\in\mathscr{F}$を満たす。近傍フィルターの定義より$N\in\mathscr{F}$となり矛盾する。逆に$N\notin\mathscr{N}_{x}$とする。あるフィルター$\mathscr{F}\rightarrow x$が存在して$N\notin\mathscr{F}$である。$\mathscr{F}$は真フィルターだから$\mathscr{F}$の$N$による補拡大$\mathscr{F}_{\neg N}$は$\mathscr{F}$と$X\backslash N$を含む真フィルターとなる。このとき$\mathscr{F}_{\neg N}\rightarrow x$より$x\in\mathrm{cl}(X\backslash N)$である。$\square$


__命題__ $A\subset X$について$f(\mathrm{pcl}(A))\subset\mathrm{pcl}(f(A))$が成り立つ。

（証明）$x\in\mathrm{pcl}(A)$について$y=f(x)$とする。ある真フィルター$\mathscr{F}\rightarrow x$が存在して$A\in\mathscr{F}$である。このとき$f_{\ast}\mathscr{F}$は真フィルターだが、$f$は連続なので$f_{\ast}\mathscr{F}\rightarrow f(x)=y$であり$f(A)\in f_{\ast}\mathscr{F}$である。従って$y\in\mathrm{pcl}( f(A) )$を得る。$\square$

収束空間はフィルター開位相により位相空間としての構造を持つ。また連続射はフィルター開位相における連続写像である。これは即ち収束空間の圏$\mathbf{Conv}$から位相空間の圏$\mathbf{Top}$への函手が定まることを意味する。

__定理__ 函手$\mathbf{Conv}\rightarrow\mathbf{Top}$は忠実である。

（証明）対応する射は写像として等しいので忠実である。$X, Y$を収束空間、$\mathcal{O}_{X}, \mathcal{O}_{Y}$をフィルター開位相とする。連続写像$f\colon (X, \mathcal{O}_{X})\rightarrow (Y, \mathcal{O}_{Y})$とする。$X$において$\mathscr{F}\rightarrow x$とする。$\mathscr{F}\subset\mathscr{N}_{x}$である。


> $X, Y$を位相空間とする。連続写像$f\colon X\rightarrow Y$は、一般的に次の同値条件で定義される。
> - 任意の$x\in X$に対し、$N\in\mathfrak{N}_{f(x)}$なら$f^{-1}(N)\in\mathfrak{N}_{x}$である。ただし$\mathfrak{N}_{\ast}$は位相に関する$\ast$の近傍系である。
> - 開集合$U\subset Y$について$f^{-1}(U)\subset X$は開集合である。
> - 閉集合$F\subset Y$について$f^{-1}(F)\subset X$は閉集合である。
> - $A\subset X$に対して$f(\overline{A})\subset\overline{f(A)}$が成り立つ。ただし$\overline{\ast}$は位相に関する$\ast$の閉包である。
> 