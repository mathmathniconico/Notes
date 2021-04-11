
# ユークリッド整域

> 整環とは単位的可換環であってゼロ環でないもの

__定義__ $R$を整環とする。写像$E\colon R\setminus\lbrace 0 \rbrace\rightarrow \mathbb{N}_{0}$は以下を満たすとする。

- $a, b\in R, \neq 0$について$E(ab)\ge E(a)$を満たす。
- $a, b\in R$について、$b=qa+r$を満たす$q, r\in R$が存在して、$r=0$または$N(r)\lt N(a)$が成り立つ。

このとき組$(R, E)$あるいは単に$R$を **ユークリッド整域** （Euclidean domain, ED）と呼ぶ。

__補題__ $(R, E)$はEDとする。$N(1)$は最小値を取る。

（証明）$a\in R$について$E(a)=E(1\cdot a)\ge E(1)$である。$\square$

__命題__ $(R, E)$はEDとする。$R^{\times}=\lbrace u\in R, \neq 0 : E(u)=E(1) \rbrace$である。

（証明）