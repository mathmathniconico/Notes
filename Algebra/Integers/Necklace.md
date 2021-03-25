
# ネックレス合同

有限体の理論で有用らしいが、数が何らかの組合せで表せるというのは純粋に楽しい。

数論的函数のうち整数値を取るもの全体を$\mathbb{A}_{\mathbb{Z}}$とする。和や畳み込みは整数値であることを変えず、また$0$や$\varepsilon$も整数値なので、$\mathbb{A}_{\mathbb{Z}}$は$\mathbb{A}$の部分環となる。

__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

1. $f$は$\mathbb{A}_{\mathbb{Z}}$において可逆である。
1. $f(1)=\pm 1$である。

特に$\mathbb{A}_{\mathbb{Z}}^{\times}\lt\mathbb{A}^{\times}$は部分群となる。

（証明）$f\ast g=\varepsilon$なら$1=\varepsilon(1)=f(1)g(1)$より$f(1)=\pm 1$である。逆に$f(1)=\pm 1$のとき$f$は$\mathbb{A}$において可逆である。このとき逆元の作り方より$\neg f$は整数値を取る。よって$\neg f\in\mathbb{A}_{\mathbb{Z}}$となる。$\square$

> この命題はRotaの定理に一般化される。

__定義__ $n\in\mathbb{N}_{1}$に対し$\mathbb{Z}/n\mathbb{Z}$の元を対応させる写像全体を$\mathbb{A}_{\equiv}$と表す。写像$\mathbb{A}_{\mathbb{Z}}\rightarrow\mathbb{A}_{\equiv}$を以下で定める。

- $f\in\mathbb{A}_{\mathbb{Z}}$に対し$\overline{f}(n):=\overline{f(n)}\in\mathbb{Z}/n\mathbb{Z}$を対応させる。

このとき$f\mapsto\overline{f}$は全射である。また$\mathbb{A}_{\equiv}$において成分毎の和と積を定義でき、$\overline{f+g}=\overline{f}+\overline{g}$や$\overline{f\cdot g}=\overline{f}\cdot \overline{g}$を満たす。

__命題__ $f, g\in\mathbb{A}_{\mathbb{Z}}$とする。以下が成り立つ。

- $\overline{f}=0, \overline{g}=0$なら$\overline{f\ast g}=0$が成り立つ。
- $u\in\mathbb{A}_{\mathbb{Z}}^{\times}$は可逆かつ$\overline{u}=0$を満たすとする。$\overline{f\ast u}=0$なら$\overline{f}=0$が成り立つ。

（証明）$(f\ast g)(n)=\sum_{ab=n}f(a)g(b)$である。仮定より$a\vert f(a), b\vert g(b)$だから$n\vert f(a)g(b)$となり、$(f\ast g)(n)\equiv_{n}0$を得る。

$\overline{f}\neq 0$とする。$f(n)\not\equiv_{n}0$となる最小の$n$を取り$(f\ast u)(n)=\sum_{ab=n}f(a)u(b)$を考える。仮定より$b\vert u(b)$かつ$a\lt n$について$a\vert f(a)$であり、$u$は可逆なので$(f\ast u)(n)\equiv_{n}f(n)u(1)=\pm f(n)\not\equiv_{n}0$を得る。$\square$

__定義__ $f, z\in\mathbb{A}_{\mathbb{Z}}$とする。$f$は$\overline{f\ast z}=0$を満たすとき$z$自明という。

- $z$が可逆のとき$\neg z$は$z$自明である。

__命題__ $z\in\mathbb{A}_{\mathbb{Z}}^{\times}$は可逆とする。$f, g\in\mathbb{A}_{\mathbb{Z}}$について以下が成り立つ。

- $f$は$\neg z$自明、$g$は$z$自明とする。このとき$f$は$g$自明である。
- $f$は$g$自明、$g$は$z$自明とする。更に$g$が可逆なら$f$は$\neg z$自明である。

（証明）$\overline{f\ast\neg z}=0$とする。$\overline{g\ast z}=0$なので先の命題より$\overline{f\ast g}=\overline{(f\ast\neg z)\ast(g\ast z)}=0$となる。逆に$\overline{f\ast g}=0$かつ$\overline{g\ast z}=0$とする。$g$が可逆より$z\ast g$も可逆である。故に同じく先の命題より$\overline{f\ast\neg z}=0$を得る。$\square$

可逆な$z$について、$z$自明な函数$g$について$g$自明という概念は、可逆な$g$について考える限り同じものとなる。

__定義__ $z\in\mathbb{A}_{\mathbb{Z}}^{\times}$は可逆とする。$f\in\mathbb{A}_{\mathbb{Z}}$が$\neg z$自明のとき、$z$と **ネックレス合同** （necklace congruence）であるという。

> $z=\mathfrak{z}$の場合は、メビウス反転公式より具体的な条件が分かる。

__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

1. $f$は$\mathfrak{z}$とネックレス合同である。
1. $k, m\in\mathbb{N}_{1}$とする。素数$p$は$m$と互いに素とする。このとき$f(p^{k}m)\equiv_{p^{k}}f(p^{k-1}m)$が成り立つ。

（証明）$\overline{f\ast\mu}=0$とする。メビウス反転公式より$f=(f\ast\mu)\ast\mathfrak{z}$、従って

$$
\begin{aligned}
f(p^{k}m) &=\sum_{d\vert p^{k}m}(f\ast\mu)(d)=\sum_{d\vert p^{k-1}m}(f\ast\mu)(d)+\sum_{d\vert m}(f\ast\mu)(p^{k}d) \\
&=f(p^{k-1}m)+\sum_{d\vert m}(f\ast\mu)(p^{k}d)
\end{aligned}
$$

が成り立つ。ここで$(f\ast\mu)(p^{k}d)\equiv_{p^{k}d}0$だから特に$p^{k}$の倍数である。故に$f(p^{k}m)\equiv_{p^{k}}f(p^{k-1}m)$を得る。

逆を示す。$n\in\mathbb{N}_{1}$の一つの素因数を$p$として、$p$と互いに素な$m$により$n=p^{k}m$と表す。このとき

$$
\begin{aligned}
(f\ast\mu)(n)&=\sum_{s=0}^{k}\sum_{ab=m}f(p^{s}a)\mu(p^{k-s}b) \\
&=\sum_{ab=m}f(p^{k-1}a)\mu(pb)+\sum_{ab=m}f(p^{k}a)\mu(b) \\
&\equiv_{p^{k}}\sum_{ab=m}f(p^{k}a)(-1)\mu(b)+\sum_{ab=m}f(p^{k}a)\mu(b)=0
\end{aligned}
$$

となる。これが全ての素因数に対して言えるので$(f\ast\mu)(n)\equiv_{n}0$を得る。$\square$

> 同値条件に$f(n)\equiv_{n}f(n/p)$がある資料もあったが強すぎるように思う。$f(p^{k})\equiv_{p^{k}}f(p^{k-1})$がある資料もあったが弱すぎるように思う。


写像$f\colon X\rightarrow X$に対して以下を定める。

- $f^{n}$の不動点全体を$\mathrm{Fix}f^{n}:=\lbrace x\in X : f^{n}(x)=x \rbrace$とする。
- ある$x\in X$について、$x, f(x), \dotsc, f^{n-1}(x)$が相違かつ$f^{n}(x)=x$を満たすとき、集合$\lbrace x, f(x), \dotsc, f^{n-1}(x) \rbrace$を長さ$n$のサイクルと呼ぶ。この全体を$C_{n}(f)$とする。

> $n\neq m$について$F\in C_{n}(f), G\in C_{m}(f)$なら$F\cap G=\emptyset$である。

__補題__ （necklace counting lemma）写像$f\colon X\rightarrow X$は任意の$d$について$\vert \mathrm{Fix}f^{d} \vert\lt\infty$を満たすとする。このとき

$$
\vert C_{n}(f) \vert=\frac{1}{n}\sum_{d\vert n}\mu(n/d)\vert \mathrm{Fix}f^{d} \vert
$$

が成り立つ。特に$n\mapsto\vert \mathrm{Fix}f^{n} \vert$は$\mathfrak{z}$とネックレス合同である。

（証明）$x\in X$について$f^{n}(x)=x$とする。$f^{d}(x)=x$となる最小の$1\le d\le n$が取れる。ある$q, 0\le r\lt d$が存在して$n=qd+r$となるが

$$
x=f^{n}(x)=f^{r}(f^{qd}(x))=f^{r}(x)
$$

より$r=0$なので$d\vert n$を得る。また$0\le i\lt j\le d$について$f^{i}(x)=f^{j}(x)$なら$f^{d-j+i}(x)=f^{d}(x)=x$より$d-j-i=0$つまり$i=0, j=d$である。よって$\lbrace x, f(x), \dotsc, f^{d-1}(x) \rbrace\in C_{d}(f)$を得る。逆に$d\vert n$について$x\in F\in C_{d}(f)$とすると$x\in\mathrm{Fix}(f^{n})$である。よって

$$
\vert \mathrm{Fix}f^{n} \vert=\sum_{d\vert n}d\cdot\vert C_{d}(f) \vert
$$

が成り立つ。$g(n)=\vert \mathrm{Fix}f^{n} \vert, h(n)=n\cdot\vert C_{n}(f) \vert$とすると$g=\mathfrak{z}\ast h$である。故に$h=g\ast\mu$だから

$$
n\cdot\vert C_{n}(f) \vert=\sum_{d\vert n}\mu(n/d)\cdot\vert \mathrm{Fix}f^{d} \vert
$$

を得る。$\square$

> 例えば$X$が有限集合なら常に補題の条件を満たす。

__定理__ （necklace theorem、メビウス函数によるフェルマーの小定理B）$a$を整数、$m$を正の整数とする。このとき

$$
\sum_{d\vert m}\mu(m/d)a^{d}\equiv_{m}0
$$

が成り立つ。

（証明）合同式なので$a\gt 0$としてよい。$N=\mathrm{lcm}(1, \dotsc, m)$として、$X=\lbrace \nu\colon\mathbb{Z}/N\mathbb{Z}\rightarrow\lbrace 1, \dotsc, a \rbrace \rbrace$とする。これは番号の振られた輪状に並ぶ$N$個の玉の$a$色での塗り分けである。ここで輪の回転$f\colon\nu(x)\mapsto\nu(x+1)$を考える。このとき$d\vert m$について$\nu\in\mathrm{Fix}f^{d}$は$\nu(0), \dotsc, \nu(d-1)$で決まるので$a^{d}$通り存在する。故に$\vert \mathrm{Fix}f^{d} \vert=a^{d}$が$d\vert m$で成り立つ。ところでnecklace counting lemmaより

$$
\sum_{d\vert n}\mu(n/d)\vert \mathrm{Fix}f^{d} \vert\equiv_{n}0
$$

が任意の$n$で成り立つから、特に$n=m$とすれば定理の式を得る。$\square$

> 定理より$f(d):=a^{d}$が$\mathfrak{z}$とネックレス合同である。totient函数$\varphi$は$\varphi(1)=1$より可逆で、$\varphi\ast\mathfrak{z}=\angle$だから$\overline{\varphi\ast\mathfrak{z}}=0$である。故に$\varphi$もまた$\mathfrak{z}$自明であり、故に$f$は$\varphi$自明でもあり$\overline{f\ast\varphi}=0$が成り立つ。これはtotient函数によるフェルマーの小定理Bに他ならない。