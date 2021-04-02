
# 前位相空間

__定義__ $X$を収束空間とする。任意の$x\in X$について$\mathscr{N}_{x}\rightarrow x$であるとき、**前位相空間** （pretopological space）と呼ぶ。

- $X$が前位相空間なら、$\mathscr{F}\rightarrow x$であることと$\mathscr{N}_{x}\subset\mathscr{F}$は同値になる。

__補題__ $X$を収束空間、$Y$を前位相空間とする。$f\colon X\rightarrow Y$を写像、$x\in X$とする。TFAE

1. $f$は$x$で連続である。
1. $\mathscr{N}_{f(x)}\subset f_{\ast}\mathscr{N}_{x}$が成り立つ。

（証明）$f$は$x$で連続とする。$V\in\mathscr{N}_{f(x)}$とする。フィルター$\mathscr{F}\rightarrow x$について$f_{\ast}\mathscr{F}\rightarrow f(x)$だから、隣接フィルターの定義より$V\in f_{\ast}\mathscr{F}$を得る。つまりある$F\in\mathscr{F}$が存在して$f(F)\subset V$特に$F\subset f^{-1}(V)$が成り立つ。よって$f^{-1}(V)\in\mathscr{F}$である。$\mathscr{F}$は任意なので$f^{-1}(V)\in\mathscr{N}_{x}$となる。$U:=f^{-1}(V)$とすれば$f(U)=f(f^{-1}(V))\subset V$を満たす。故に$V\in f_{\ast}\mathscr{N}_{x}$を得る。

下を仮定する。$\mathscr{F}\rightarrow x$とする。$\mathscr{N}_{x}\subset \mathscr{F}$だから$f_{\ast}\mathscr{N}_{x}\subset f_{\ast}\mathscr{F}$を得る。仮定より$\mathscr{N}_{f(x)}\subset f_{\ast}\mathscr{F}$だから、$Y$は前位相空間より$f_{\ast}\mathscr{F}\rightarrow f(x)$である。$\square$

__系__ $X, Y$を前位相空間、$f\colon X\rightarrow Y$を全単射とする。TFAE

1. $f$は同型である。（$f, f^{-1}$が連続射である。）
1. 任意の$x\in X$について$\mathscr{N}_{f(x)}=f\mathscr{N}_{x}$が成り立つ。

（証明）補題より以下は同値である。

1. $f$は連続射である。
1. 任意の$x\in X$について$\mathscr{N}_{f(x)}\subset f\mathscr{N}_{x}$である。

同様に以下は同値である。

1. $f^{-1}$は連続射である。
1. 任意の$y\in Y$について$\mathscr{N}_{f^{-1}(y)}\subset f^{-1}\mathscr{N}_{y}$である。

ここで$\mathscr{N}_{f^{-1}(y)}\subset f^{-1}\mathscr{N}_{y}$は$x=f^{-1}(y)$とすると$\mathscr{N}_{x}\subset f^{-1}\mathscr{N}_{f(x)}$であり、従って$f\mathscr{N}_{x}\subset\mathscr{N}_{f(x)}$と等しい。$\square$

__命題__ $X_{i}$を前位相空間とする。集合$X$には$\lbrace f_{i}\colon X\rightarrow X_{i} \rbrace$による始収束構造が定まっているとする。このとき$X$は前位相空間である。

（証明）各$x\in X$について$f_{i}$は$x$で連続だから補題より$\mathscr{N}_{f_{i}(x)}\subset (f_{i})_{\ast}\mathscr{N}_{x}$である。$X_{i}$は前位相空間だから$\mathscr{N}_{f_{i}(x)}\rightarrow f_{i}(x)$より$(f_{i})_{\ast}\mathscr{N}_{x}\rightarrow f_{i}(x)$である。始収束構造の定義より$\mathscr{N}_{x}\rightarrow x$を得る。$\square$

> 特に前位相空間の直積は前位相空間である。

__定理__ 有限収束空間は前位相空間である。

（証明）$X$を有限収束空間、$x\in X$とする。$N\in\mathscr{N}_{x}$のうち、元の個数が最小のものをとる。このとき最小性から$\mathscr{N}_{x}=\langle N \rangle$となる。そこで$\langle N \rangle=\bigcap_{y\in N}\langle y \rangle\rightarrow x$を示したい。ある$y\in N$が存在して$\langle y \rangle\rightarrow x$でないとする。このとき$A\subset X$について$\langle A \rangle\rightarrow x$なら$N\setminus\lbrace y \rbrace\in\langle A \rangle$が成り立つ。実際$\langle A \rangle\rightarrow x$より$\langle N \rangle=\mathscr{N}_{x}\subset\langle A \rangle$だから$A\subset N$であり、$N\setminus\lbrace y \rbrace\notin\langle A \rangle$と仮定すると$A\not\subset N\setminus\lbrace y \rbrace$より$y\in A$となる。これは$\langle A \rangle\subset\langle y \rangle\rightarrow x$より矛盾する。ところで有限集合上のフィルターは単項フィルターであるから、$A$の任意性より$N\setminus\lbrace y \rbrace\in\mathscr{N}_{x}$が従う。しかしこれは$N$の最小性に矛盾するため、任意の$y\in N$について$\langle y \rangle\rightarrow x$でなければならない。収束空間の定義より有限回のwedge積で閉じているため$\mathscr{N}_{x}\rightarrow x$を得る。以上より$X$は前位相空間である。$\square$