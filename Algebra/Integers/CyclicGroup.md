
# 巡回群

__定義__ $G$を群とする。$G$の濃度$\vert G \vert$を群$G$の **位数** （order）という。

__定義__ $G$を群とする。$S\subset G$を含む最小の部分群を$\langle S \rangle$と表し、$S$が **生成** （generate）する部分群あるいは$S$によって生成される部分群という。

- $\langle S \rangle$は$S$を含む部分群たちの共通部分として表される。

__定義__ $G$を群とする。$g\in G$が生成する部分群

$$
\langle g \rangle:=\langle \lbrace g \rbrace \rangle=\lbrace g^{n} : n\in\mathbb{Z} \rbrace
$$

について、その位数を$g$の **位数** （order）と呼び$\mathrm{ord}g$で表す。特に$G=\langle g \rangle$のとき$G$を **巡回群** （cyclic group）と呼び、$g$を$G$の **生成元** （generator）と呼ぶ。

- 巡回群はアーベル群である。

__例__ 以下に巡回群の例を挙げる。

- $\mathbb{Z}$は加法に関して巡回群である。生成元は$1$である。
- $\mathbb{Z}/m\mathbb{Z}$は加法に関して位数$m$の巡回群である。生成元は$1+m\mathbb{Z}$である。


__命題__ $G=\langle g \rangle$を巡回群とする。部分群$H\lt G$に対し、ある整数$n\ge 0$が存在して$H=\langle g^{n} \rangle$が成り立つ。特に巡回群の部分群は巡回群である。

（証明）まず$H=\lbrace 1_{G} \rbrace=\langle g^{0} \rangle$は巡回群である。$H\neq\lbrace 1_{G} \rbrace$のときゼロでない整数$n\neq 0$が存在して$g^{n}\in H$となるが、特に$g^{-n}=(g^{n})^{-1}\in H$より$n\gt 0$として良い。このような最小の$n$を取る。$h\in H$は$h=g^{m}$と表せるが、整除定理により$m=qn+r$となる整数$q, 0\le r\lt n$が一意的に存在する。$g^{r}=h(g^{n})^{-q}\in H$より$n$の最小性から$r=0$と分かる。故に$h=(g^{n})^{q}\in\langle g^{n} \rangle$である。$\square$

従って巡回群の部分群は$n\ge 0$について$\langle g^{n} \rangle$の形の部分群で尽くされる。

__系__ $G=\langle g \rangle$を位数無限の巡回群、$n, m\ge 0$とする。TFAE

- $\langle g^{n} \rangle\subset\langle g^{m} \rangle$である。
- $m\vert n$である。

（証明）上を仮定すると$g^{n}=(g^{m})^{k}$と表されるから$n=mk$より$m\vert n$を得る。逆も同様である。$\square$

特に$\langle g^{n} \rangle=\langle g^{m} \rangle$なら$n=m$である。つまり位数無限の巡回群に関しては、その部分群の構造が自然数の整除関係で完全に決定される。



## 有限巡回群

以下、$G=\langle g \rangle$を位数$n$の巡回群とする。ラグランジュの定理より$G$の部分群の位数は$n$を割り切る。

__定理__ $m\vert n$に対し、位数$m$の$G$の部分群が唯一つ存在する。

（証明）


有限群$G$の部分群の位数が全て異なるなら、巡回群である。