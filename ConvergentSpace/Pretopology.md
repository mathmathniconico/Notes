
# 前位相空間

__定義__ $X$を収束空間とする。任意の$x\in X$について$\mathscr{N}_{x}\rightarrow x$であるとき、**前位相空間** （pretopological space）と呼ぶ。

- $X$が前位相空間なら、$\mathscr{F}\rightarrow x$であることと$\mathscr{N}_{x}\subset\mathscr{F}$は同値になる。

__補題__ $X$を収束空間、$Y$を前位相空間とする。$f\colon X\rightarrow Y$を写像、$x\in X$とする。TFAE

1. $f$は$x$で連続である。
1. 任意の$V\in\mathscr{N}_{f(x)}$に対して$U\in\mathscr{N}_{x}$が存在して$f(U)\subset V$を満たす。

（証明）上を仮定する。$V\in\mathscr{N}_{f(x)}$について$U:=f^{-1}(V)\in\mathscr{N}_{x}$を示せばよい。フィルター$\mathscr{F}\rightarrow x$について、$f$は連続射だから$f_{\ast}\mathscr{F}\rightarrow f(x)$となる。隣接フィルターの定義より$V\in f_{\ast}\mathscr{F}$を得る。つまりある$F\in\mathscr{F}$が存在して$f(F)\subset V$特に$F\subset f^{-1}(V)$が成り立つ。よって$f^{-1}(V)\in\mathscr{F}$であり、これが任意に言えるので$f^{-1}(V)\in\mathscr{N}_{x}$を得る。

逆に下を仮定する。$X$において$\mathscr{F}\rightarrow x$とすると、仮定より$\mathscr{N}_{f(x)}\subset f_{\ast}\mathscr{F}$が成り立つ。$Y$が前位相空間より$\mathscr{N}_{f(x)}\rightarrow f(x)$だから$f_{\ast}\mathscr{F}\rightarrow f(x)$を得る。$\square$

__系__ $X, Y$を前位相空間、$f\colon X\rightarrow Y$を写像とする。TFAE

1. $f$は連続射である。
1. 任意の$x\in X$について$\mathscr{N}_{f(x)}\subset f_{\ast}\mathscr{N}_{x}$が成り立つ。

特に$f$は全単射とする。TFAE

1. $f$は同型である。（$f, f^{-1}$が連続射である。）
1. $\mathscr{N}_{f(x)}=f\mathscr{N}_{x}$が成り立つ。

> TODO: なんか変？

<!--
（証明）上を仮定する。$X$が前位相空間だから$\mathscr{N}_{x}\rightarrow x$である。$f$は連続射なので$f_{\ast}\mathscr{N}_{x}\rightarrow f(x)$となる。故に$\mathscr{N}_{f(x)}\subset f_{\ast}\mathscr{N}_{x}$を得る。

下を仮定する。$x\in X$とする。任意の$V\in\mathscr{N}_{f(x)}$について$V\in f_{\ast}\mathscr{N}_{x}$より、ある$U\in\mathscr{N}_{x}$が存在して$f(U)\subset V$を満たす。補題より$f$は$x$で連続である。
-->