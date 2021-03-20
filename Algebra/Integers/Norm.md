
# 数論的函数のノルム


## 位数と次数

__定義__ ゼロでない数論的函数$f$に対して、以下を定める。

- $\mathrm{supp}(f):=\lbrace k : f(k)\neq 0 \rbrace$を$f$の **台** （support）と呼ぶ。
- $\mathrm{ord}(f):=\mathrm{min}( \mathrm{supp}(f) )$を$f$の **位数** （order）と呼ぶ。
- $\mathrm{deg}(f):=\mathrm{min}\lbrace \Omega(k) : k\in\mathrm{supp}(f) \rbrace$を$k$の **次数** （degree）と呼ぶ。

$f=0$に対しては$\mathrm{ord}0=\infty, \mathrm{deg}0=-1$と定めておく。

__命題__ 数論的函数$f, g$及び$c\in\mathbb{C}^{\times}$に対して以下が成り立つ。

- $\mathrm{ord}(f+g)\ge\mathrm{min}\lbrace \mathrm{ord}(f), \mathrm{ord}(g) \rbrace$が成り立つ。
- $\mathrm{ord}(cf)=\mathrm{ord}f$が成り立つ。
- $\mathrm{ord}(f)=1\Longleftrightarrow f\in\mathbb{A}^{\times}$である。
- $\mathrm{ord}(f\ast g)=\mathrm{ord}(f)\mathrm{ord}(g)$が成り立つ。
- $\mathrm{deg}(f+g)\ge\mathrm{min}\lbrace \mathrm{deg}(f), \mathrm{deg}(g) \rbrace$が成り立つ。
- $\mathrm{deg}(cf)=\mathrm{deg}(f)$が成り立つ。
- $\mathrm{deg}(f)=0\Longleftrightarrow f\in\mathbb{A}^{\times}$である。
- $\mathrm{deg}(f\ast g)=\mathrm{deg}(f)+\mathrm{deg}(g)$が成り立つ。

（証明）



$\square$


__定義__ $\vert f \vert:=1/\mathrm{ord}f$を$f$の **ノルム** （norm）と呼ぶ。$\vert 0 \vert=0$



## 各論

### 約数の個数と総和

$n$の約数の個数を$d(n)$と表す。

$$
\mathfrak{z}\ast\mathfrak{z}(n)=\sum_{d\vert n}1=d(n)
$$

より$d=\mathfrak{z}\ast\mathfrak{z}$である。

__定義__ $k\in\mathbb{Z}$に対し$\mathfrak{z}_{k}$を以下で定める。

- $\mathfrak{z}_{0}:=\varepsilon$とする。
- $k\gt 0$について$\mathfrak{z}_{k}:=\mathfrak{z}\ast\dotsb\ast\mathfrak{z}$を$k$個の畳み込みとする。
- $k\gt 0$について$\mathfrak{z}_{-k}:=\mu\ast\dotsb\ast\mu$を$k$個の畳み込みとする。

$n$の約数の和を$\sigma(n)$と表す。

$\sigma(n)=\sum_{d\vert n}d=\angle\ast\mathfrak{z}(n)$より$\sigma=\angle\ast\mathfrak{z}$が成り立つ。




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

__定義__ $n$と互いに素な$1$以上$n$以下の整数の個数を$\varphi(n)$で表し、オイラーの **totient函数** と呼ぶ。





## まとめ

| 名称 | 記号 | 定義 | 性質 |
|-|-|-|-|
| 重複込みの素因数函数 | $\Omega(n)$ | $n$の素因数を重複込みで数えた個数。ただし$\Omega(1)=0$ | 完全加法的 |
| 素因数函数 | $\omega(n)$ | $n$の互いに異なる素因数の個数。ただし$\omega(1)=0$ | 加法的 |
| Liouville函数 | $\lambda(n)$ | $\lambda(n):=(-1)^{\Omega(n)}$ | 完全乗法的 |
| 対角函数 | $\angle(n)$ | $\angle(n):=n$ | 完全乗法的 |
| 約数の個数 | $d(n)$ | $n$の約数（$1$以上$n$以下）の個数 | |
| 約数の総和 | $\sigma(n)$ | $n$の約数（$1$以上$n$以下）を足し上げたもの | $\sigma=\angle\ast\mathfrak{z}$ |
| 畳み込み整数 | $\mathfrak{z}_{k}(n)$ | $k$個の$\mathfrak{z}$の畳み込み（$\mathfrak{z}_{0}=\varepsilon, \mathfrak{z}_{-1}=\mu$） | $\mathfrak{z}_{2}=d$ |
| totient函数 | $\varphi(n)$ | $n$と互いに素な整数（$1$以上$n$以下）の個数 | $\varphi\ast\mathfrak{z}=\angle$ |
| 対数函数 | $L(n)$ | $n$の対数の主値 | 完全加法的 |
| von Mangoldt函数 | $\Lambda(n)$ | 素数の冪$p^{e}$について$\Lambda(p^{e})=\mathrm{log}p$、それ以外は$0$ | $\Lambda=\mu\ast L$ |
| 一般von Mangoldt函数 | $\Lambda_{r}(n)$ | $\Lambda_{r}:=\mu\ast L^{r}$ | $\Lambda_{r+1}=L\Lambda_{r}+\Lambda\ast\Lambda_{r}$ |