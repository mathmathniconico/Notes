
# 数論的函数

自然数から複素数への写像を数論的函数と呼ぶ。一見するとつまらない概念に思えるかもしれないが、自然数の整除関係を通して多くの興味深い事実を得ることができる。




## 数論的函数の為す環

__定義__ $f\colon\mathbb{N}_{1}\rightarrow\mathbb{C}$を **数論的函数** （arithmetic function）と呼ぶ。

- 恒等的に定数$c\in\mathbb{C}$を取る定数函数は数論的函数である。特に$\mathfrak{z}(n):=1$を$\mathfrak{z}$函数と呼ぶ。
- $\varepsilon(1):=1$及び$n\neq 1$について$\varepsilon(n):=0$とする。このとき$\varepsilon$は数論的函数である。

__命題__ $f, g$を数論的函数とする。これらの和$f+g$と **畳み込み積** （convolution product）$f\ast g$を$n\in\mathbb{N}_{1}$に対して

$$
\begin{aligned}
(f+g)(n) &:=f(n)+g(n), \\
(fg)(n) &:=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)=\sum_{ab=n}f(a)g(b)
\end{aligned}
$$

と定める。このとき数論的函数全体は$\varepsilon$をイチとする単位的可換環である。

（証明）和に関してアーベル群となることは明らか。特に定数函数$0(n):=0$である。

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

より左分配性が従う。右分配性も同様である。

畳み込み積が可換なことは定義より明らか。また$\varepsilon$が乗法単位元であることも明白。$\square$

__命題__ 数論的函数全体は整域である。

（証明）数論的函数$f, g\neq 0$が$f\ast g=0$を満たすとする。$f, g\neq 0$より$f(a), g(b)\neq 0$となるような最小の自然数$a, b$が取れる。$d\lt a$のとき$f(d)=0$であり、$d\gt a$のとき$g(ab/d)=0$より

$$
(f\ast g)(ab)=\sum_{d\vert ab}f(d)g\left( \frac{ab}{d} \right)=f(a)g(b)\neq 0
$$

より矛盾する。$\square$

__定義__ 数論的函数$f$が畳み込み積に関して可逆のとき、その逆元を$f^{(-1)}$と表す。

__命題__ $f$を数論的函数とする。TFAE

- $f$は可逆である。
- $f(1)\neq 0$である。

（証明）$f\ast g=\varepsilon$とする。$(f\ast g)(1)=f(1)g(1)=\varepsilon(1)=1$より$f(1)\neq 0$である。

逆に$f(1)\neq 0$が成り立つとする。$g(1):=1/f(1)$として$n\gt 1$に対して

$$
g(n):=-\frac{1}{f(1)}\sum_{ab=n, b\lt n}f(a)g(b)
$$

と帰納的に定める。このとき$f\ast g=\varepsilon$が成り立つ。$\square$

> 素数を小さい順に並べて$p_{i}$とする。$n\in\mathbb{N}_{1}$に対して、$n$の$p_{i}$の指数部を$\nu_{i}(n)$で表し、数列$\nu_{n}:=( \nu_{i}(n) )_{i}$を取る。このとき数論的函数$f$に関して$\sum f(n)t^{\nu_{n}}=\sum f(n)\prod t_{i}^{\nu_{i}(n)}$を対応させる写像は形式的冪級数環$\mathbb{C}\lbrack\lbrack t_{1}, t_{2}, \dotsc \rbrack\rbrack$との同型を与える。従って数論的函数全体はUFDである。




## 乗法的函数

__定義__ $f$を数論的函数とする。$m$と$n$が互いに素のとき$f(mn)=f(m)f(n)$が成り立つとき、$f$は **乗法的** （multiplicative）という。

> TODO 乗法的函数



メビウス函数$\mu$を以下で定める。

- $\mu(1)=1$とする。
- $n$の素因数分解が$2$次以上の素因子を持つとき$\mu(n)=0$とする。
- $n$が相異な$s$個の素数の積のとき（square-freeという）$\mu(n)=(-1)^{s}$とする。

> 例えば$n=15=3\times 5$より$\mu(15)=(-1)^{2}=1$となる。一方で$n=12=2^{2}\times 3$より$\mu(12)=0$となる。

__命題__ メビウス函数$\mu$について以下が成り立つ。

- メビウス函数は乗法的である。
- $\mu\ast\mathfrak{z}=\varepsilon$が成り立つ。

__系__ （メビウス反転）数論的函数$f$は乗法的とする。このとき

$$
g(n):=\sum_{d\vert n}f(d)
$$

と定めると、$g$もまた乗法的で

$$
f(n)=\sum_{ab=n}f(a)g(b)
$$

が成り立つ。

逆に



__例__ 以下に数論的函数の例を挙げる。

- 定数函数、特に恒等的に$1$を取る$\mathfrak{z}$函数
- 数論的函数の乗法単位元$\varepsilon$
- メビウス函数$\mu$
- 約数函数$d$
- $\phi(n)$は$n$と互いに素な$1$以上$n$以下の整数の個数とする。（オイラーの **totient函数** と呼ぶ。）
- $L(n):=\log{n}$とする。
