
# 乗法的な数論的函数

__定義__ $f$をゼロでない数論的函数とする。互いに素な$m, n$について$f(mn)=f(m)f(n)$が成り立つとき、$f$は **乗法的** （multiplicative）という。乗法的な数論的函数全体を$\mathrm{Mul}(\mathbb{A})$と表す。

- $\mathfrak{z}$と$\varepsilon$は乗法的である。
- $f$が乗法的なら$f(1)=1$である。従って先の命題より$f$は可逆である。
- 乗法的な数論的函数は素数の冪$p^{e}$での値により決まる。つまり$f(1)=1$及び$f(\prod p^{e}):=\prod f(p^{e})$により定まる。




## メビウス函数

__命題__ $\mathrm{Mul}(\mathbb{A})\lt\mathbb{A}^{\times}$は部分群である。特に$f, g\in\mathbb{A}$が乗法的なら$f\ast g$及び$\neg f$は乗法的である。

（証明）互いに素な$m, n$に対し、$d\vert mn$のとき唯一つの$d_{1}\vert m, d_{2}\vert n$が存在して$d=d_{1}d_{2}$となる。特に$d_{1}, d_{2}$は互いに素なので

$$
\begin{aligned}
(f\ast g)(mn) &=\sum_{ab=mn}f(a)g(b)=\sum_{a_{1}b_{1}=m}\sum_{a_{2}b_{2}=n}f(a_{1}a_{2})g(b_{1}b_{2}) \\
&=\sum_{a_{1}b_{1}=m}\sum_{a_{2}b_{2}=n}f(a_{1})f(a_{2})g(b_{1})g(b_{2}) \\
&=\left( \sum_{a_{1}b_{1}=m}f(a_{1})g(b_{1}) \right)\left( \sum_{a_{2}b_{2}=m}f(a_{2})g(b_{2}) \right) \\
&=(f\ast g)(m)(f\ast g)(n)
\end{aligned}
$$

となる。

$h(1):=1$として、$h$の素数の冪に対する値を

$$
\sum_{ab=p^{e}}f(a)h(b)=0
$$

から帰納的に定める。このとき乗法的な数論的函数$h$が定まる。先の議論より$f\ast h\in\mathrm{Mul}(\mathbb{A})$である。定義より$(f\ast h)(1)=1$かつ素数の冪$p^{e}$について$(f\ast h)(p^{e})=0$である。$\varepsilon$も乗法的で$\varepsilon(1)=1, \varepsilon(p^{e})=0$を満たす。従って両者は一致し$f\ast h=\varepsilon$を得る。$\square$

> 実は$\ast$を「和」とする環構造があることが知られている。

__定義__ 以下で定まる数論的函数$\mu$を **メビウス函数** と呼ぶ。

- $\mu(1)=1$とする。
- $n$の素因数分解が$2$次以上の素因子を持つとき$\mu(n)=0$とする。
- $n$が相異な$s$個の素数の積のとき$\mu(n)=(-1)^{s}$とする。（このとき$n$はsquare-freeという。$n=1$のときは$s=0$と思って良い。）

> 例えば$15=3\times 5$より$\mu(15)=(-1)^{2}=1$である。一方で$12=2^{2}\times 3$はsquare-freeでないから$\mu(12)=0$である。

__命題__ メビウス函数$\mu$について以下が成り立つ。

- メビウス函数は乗法的である。
- $\mu\ast\mathfrak{z}=\varepsilon$が成り立つ。つまり$\mu=\neg\mathfrak{z}$である。

（証明）$m, n$は互いに素とする。このとき$mn$がsquare-freeであることと$m$と$n$がsquare-freeであることは同値である。$m, n$が相異な$s, t$個の素数の積とすると$\mu(mn)=(-1)^{s+t}=(-1)^{s}(-1)^{t}=\mu(m)\mu(n)$を得る。

定義より$\mu(1)=\varepsilon(1)$である。$n\gt 1$のとき$p_{1}^{e_{1}}\dotsm p_{r}^{e_{r}}$を$n$の素因数分解とする。

$$
\sum_{d\vert n}\mu(d)=\sum_{d\vert p_{1}\dotsm p_{r}}\mu(d)=\sum_{i=0}^{r}\left( \begin{matrix} r \\ i \end{matrix} \right)(-1)^{i}=(1-1)^{r}=0
$$

より$\mu\ast\mathfrak{z}=\varepsilon$が成り立つ。$\square$

__系__ （メビウス反転）$f\in\mathbb{A}$とする。このとき$G(n):=\sum_{d\vert n}f(d)$と定めると

$$
f(n)=\sum_{ab=n}\mu(a)G(b)
$$

が成り立つ。

逆に$g\in\mathbb{A}$とする。このとき$F(n):=\sum_{ab=n}\mu(a)g(b)$と定めると

$$
g(n)=\sum_{d\vert n}F(d)
$$

が成り立つ。

（証明）$G=f\ast\mathfrak{z}, F=g\ast\mu$なので$\mu=\neg\mathfrak{z}$より従う。$\square$

> $\mathfrak{z}, \mu$が乗法的なので、$f$が乗法的なら$G$も乗法的であり、$g$が乗法的なら$F$も乗法的である。




## 各論

### 約数の個数と総和

$n$の約数の個数を$d(n)$と表す。

$$
\mathfrak{z}\ast\mathfrak{z}(n)=\sum_{d\vert n}1=d(n)
$$

より$d=\mathfrak{z}\ast\mathfrak{z}$である。

__定義__ $k\in\mathbb{Z}$に対し$d_{k}$を以下で定める。

- $d_{0}:=\varepsilon$とする。
- $k\gt 0$について$d_{k}:=\mathfrak{z}\ast\dotsb\ast\mathfrak{z}$を$k$個の畳み込みとする。
- $k\gt 0$について$d_{-k}:=\mu\ast\dotsb\ast\mu$を$k$個の畳み込みとする。

$n$の約数の和を$\sigma(n)$と表す。

$\sigma(n)=\sum_{d\vert n}d=\mathrm{id}\ast\mathfrak{z}(n)$より$\sigma=\mathrm{id}\ast\mathfrak{z}$が成り立つ。




### 対数函数

$L(n):=\mathrm{Log}(n)$を対数函数と呼ぶ。これは完全加法的であり、任意の$n, m\in\mathbb{N}_{1}$に対して$L(mn)=L(m)+L(n)$が成り立つ。完全加法的な函数のpointwiseな積は、畳み込みに関する微分として特徴付けられる。

__命題__ $F\in\mathbb{A}$とする。TFAE

- $F$は完全加法的である。
- $g, h\in\mathbb{A}$について$F\cdot(g\ast h)=(F\cdot g)\ast h+g\ast(F\cdot h)$が成り立つ。

（証明）$F$は完全加法的とする。$g, h\in\mathbb{A}$について

$$
\begin{aligned}
( F\cdot(g\ast h) )(n) &=F(n)(g\ast h)(n)=\sum_{ab=n}F(n)g(a)h(b) \\
&=\sum_{ab=n}(F(a)+F(b))g(a)h(b) \\
&=\sum_{ab=n}(F\cdot g)(a)h(b)+\sum_{ab=n}g(a)(F\cdot h)(b) \\
&=( (F\cdot g)\ast h )(n)+( g\ast(F\cdot h) )(n)
\end{aligned}
$$

より従う。

逆に下を仮定する。$\delta_{m}, \delta_{n}$に対して

$$
\begin{aligned}
(F\cdot(\delta_{m}\ast\delta_{n}))(mn) &=F(mn)\delta_{mn}(mn)=F(mn), \\
((F\cdot\delta_{m})\ast\delta_{n})(mn)+(\delta_{m}\ast(F\cdot\delta_{n}))(mn)&=F(m)+F(n)
\end{aligned}
$$

より$F$は完全加法的である。

__命題__ （ライプニッツ則）

> TODO


### その他

__定義__ $n$と互いに素な$1$以上$n$以下の整数の個数を$\phi(n)$で表し、オイラーの **totient函数** と呼ぶ。

> von Mangoldt函数$\Lambda$