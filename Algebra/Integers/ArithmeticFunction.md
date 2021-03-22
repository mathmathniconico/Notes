
# 数論的函数

自然数から複素数への写像を数論的函数と呼ぶ。数をひとまとめに扱うというアイディアは、自然数の整除関係を通して多くの興味深い事実の宝庫である。




## 数論的函数の為す環

__定義__ $f\colon\mathbb{N}_{1}\rightarrow\mathbb{C}$を **数論的函数** （arithmetic function）と呼び、全体を$\mathbb{A}$と表す。

- 定数函数を対応させることで$\mathbb{C}\subset\mathbb{A}$とみなせる。特に恒等的に$1$を取る数論的函数を$\mathfrak{z}$と表す。
- $\delta_{k}(k)=1$、$n\neq k$のとき$\delta_{k}(n)=0$とする。特に$k=1$のとき$\varepsilon:=\delta_{1}$と表す。

__命題__ $f, g\in\mathbb{A}$とする。これらの和$f+g$と **畳み込み** （convolution）$f\ast g$を$n\in\mathbb{N}_{1}$に対して

$$
\begin{aligned}
(f+g)(n) &:=f(n)+g(n), \\
(fg)(n) &:=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)=\sum_{ab=n}f(a)g(b)
\end{aligned}
$$

と定める。このとき$(\mathbb{A}, +, \ast)$は$0$をゼロ、$\varepsilon$をイチとする単位的可換環である。

（証明）和に関してアーベル群となることは明らか。畳み込みは可換であり、また$\varepsilon$が乗法単位元であることも明白。

結合律を示す。$f, g, h$を数論的函数とする。$n\in\mathbb{N}_{1}$について

$$
\begin{aligned}
( (f\ast g)\ast h )(n) &=\sum_{ab=n}(f\ast g)(a)h(b)=\sum_{ab=n}\sum_{cd=a}f(c)g(d)h(b) \\
&=\sum_{cbd=n}f(c)g(d)h(b)=\sum_{ce=n}f(c)\sum_{bd=e}g(d)h(b) \\
&=\sum_{ce=n}f(c)(g\ast h)(e)=( f\ast( g\ast h) )(n)
\end{aligned}
$$

より従う。

両側分配性を示す。$f, g, h$を数論的函数とする。$n\in\mathbb{N}_{1}$について

$$
\begin{aligned}
( f\ast(g+h) )(n) &:=\sum_{d\vert n}f(d)(g+h)\left( \frac{n}{d} \right) \\
&=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)+\sum_{d\vert n}f(d)h\left( \frac{n}{d} \right) \\
&=(f\ast g)(n)+(f\ast h)(n)
\end{aligned}
$$

より左分配性が従う。右分配性も同様である。$\square$

- $\delta_{k}\ast\delta_{l}=\delta_{kl}$が成り立つ。

__命題__ $\mathbb{A}$は整域である。

（証明）ゼロでない数論的函数$f, g$が$f\ast g=0$を満たすとする。$f, g\neq 0$より$f(a), g(b)\neq 0$となるような最小の自然数$a, b$が取れる。$d\lt a$のとき$f(d)=0$であり、$d\gt a$のとき$g(ab/d)=0$より

$$
(f\ast g)(ab)=\sum_{d\vert ab}f(d)g\left( \frac{ab}{d} \right)=f(a)g(b)\neq 0
$$

より矛盾する。$\square$

__定義__ 数論的函数$f$が畳み込みに関して可逆のとき、その逆元を$\neg f$と表す。

> 可逆な元全体$\mathbb{A}^{\times}$は乗法により群となるのであった。

__命題__ $f$を数論的函数とする。TFAE

1. $f$は可逆である。
1. $f(1)\neq 0$である。

（証明）$f\ast g=\varepsilon$とする。$(f\ast g)(1)=f(1)g(1)=\varepsilon(1)=1$より$f(1)\neq 0$である。

逆に$f(1)\neq 0$が成り立つとする。$g(1):=1/f(1)$として$n\gt 1$に対して

$$
g(n):=-\frac{1}{f(1)}\sum_{ab=n, b\lt n}f(a)g(b)
$$

と帰納的に定める。このとき$f\ast g=\varepsilon$が成り立つ。$\square$

> 素数を小さい順に並べて$p_{i}$とする。$n\in\mathbb{N}_{1}$に対して、$n$の$p_{i}$の指数部を$\nu_{i}(n)$で表し数列$\nu_{n}:=( \nu_{i}(n) )_{i}$を取る。このとき$f\in\mathbb{A}$に対して$\sum f(n)t^{\nu_{n}}=\sum f(n)\prod t_{i}^{\nu_{i}(n)}$を対応させる写像は形式的冪級数環$\mathbb{C}\llbracket t_{1}, t_{2}, \dotsc \rrbracket$との同型を与える。従って$\mathbb{A}$はUFDである。





## メビウス函数

__定義__ ゼロでない数論的函数$f$が以下を満たすとき、**乗法的** （multiplicative）であるという。

- 互いに素な$m, n$について$f(mn)=f(m)f(n)$が成り立つ。

乗法的な数論的函数全体を$\mathrm{Mul}(\mathbb{A})$と表す。

- $\mathfrak{z}$と$\varepsilon$は乗法的である。
- $f$が乗法的なら$f(1)=1$である。従って先の命題より$f$は可逆である。
- 乗法的な数論的函数は素数の冪$p^{e}$での値により決まる。つまり$f(1)=1$及び$f(\prod p^{e}):=\prod f(p^{e})$により定まる。

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

から帰納的に定める。このとき乗法的な数論的函数$h$が定まる。先の議論より$f\ast h\in\mathrm{Mul}(\mathbb{A})$もまた乗法的である。定義より$(f\ast h)(1)=1$かつ素数の冪$p^{e}$について$(f\ast h)(p^{e})=0$である。$\varepsilon$も乗法的で$\varepsilon(1)=1, \varepsilon(p^{e})=0$を満たす。従って両者は一致し$f\ast h=\varepsilon$を得る。$\square$

__定義__ 以下で定まる数論的函数$\mu$を **メビウス函数** と呼ぶ。

- $\mu(1)=1$とする。
- $n$が相異な$s$個の素数の積のとき$\mu(n)=(-1)^{s}$とする。（このとき$n$はsquare-freeという。$n=1$のときは$s=0$と思って良い。）
- それ以外のとき、つまり$n$の素因数分解が$2$次以上の素因子を持つとき$\mu(n)=0$とする。

> 例えば$15=3\times 5$より$\mu(15)=(-1)^{2}=1$である。一方で$12=2^{2}\times 3$はsquare-freeでないから$\mu(12)=0$である。

__命題__ メビウス函数$\mu$について以下が成り立つ。

- メビウス函数は乗法的である。
- $\mu\ast\mathfrak{z}=\varepsilon$が成り立つ。つまり$\mu=\neg\mathfrak{z}$である。

（証明）$m, n$は互いに素とする。このとき$mn$がsquare-freeであることと$m$と$n$がsquare-freeであることは同値である。$m, n$が相異な$s, t$個の素数の積とすると$\mu(mn)=(-1)^{s+t}=(-1)^{s}(-1)^{t}=\mu(m)\mu(n)$を得る。つまり$\mu$は乗法的である。

$\mathfrak{z}$も乗法的なので$\mu\ast\mathfrak{z}$は乗法的である。定義より$(\mu\ast\mathfrak{z})(1)=1=\varepsilon(1)$である。素数の冪$p^{e}$に対して

$$
(\mu\ast\mathfrak{z})(p^{e})=\sum_{i=0}^{r}\mu(p^{i})=\mu(1)+\mu(p)=1-1=0
$$

より$\varepsilon(p^{e})$と一致する。故に$\mu\ast\mathfrak{z}=\varepsilon$である。$\square$

__系__ （メビウス反転公式）$f\in\mathbb{A}$とする。このとき$G(n):=\sum_{d\vert n}f(d)$と定めると

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








## まとめ

- 数論的函数全体$\mathbb{A}$は和と畳み込みにより環となる。
- $f$が畳み込みで可逆なことと$f(1)\neq 0$は同値である。
- 乗法的なら可逆であり、全体$\mathrm{Mul}(\mathbb{A})\lt\mathbb{A}^{\times}$は部分群である。
- 恒等的に$1$を取る函数$\mathfrak{z}$の逆元がメビウス函数$\mu$である。

| 名称 | 記号 | 定義 | 性質 |
|-|-|-|-|
| 定数函数 | $c$ | 恒等的に$c\in\mathbb{C}$ |  |
| z函数 | $\mathfrak{z}$ | 定数函数$1$ | 乗法的 |
| デルタ函数（$k\ge 1$） | $\delta_{k}(n)$ | $n=k$のとき$1$、$n\neq k$のとき$0$ | $\delta_{k}\ast\delta_{l}=\delta_{kl}$ |
| 畳み込み単位元 | $\varepsilon$ | $\delta_{1}$ | 乗法的 |
| メビウス函数 | $\mu(n)$ | $\mu(1)=1$、$n$が相異な$s$個の素数の積なら$\mu(n)=(-1)^{s}$、それ以外は$0$ | 乗法的、$\mu=\neg\mathfrak{z}$ |