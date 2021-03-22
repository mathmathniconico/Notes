
# ネックレス合同

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

> 畳み込みは定義できないので、どのように振舞うかを調べることには価値がある。

__命題__ $f, g\in\mathbb{A}_{\mathbb{Z}}$とする。以下が成り立つ。

- $\overline{f}=0, \overline{g}=0$なら$\overline{f\ast g}=0$が成り立つ。
- $u\in\mathbb{A}_{\mathbb{Z}}^{\times}$は可逆かつ$\overline{u}=0$とする。$\overline{f\ast u}=0$なら$\overline{f}=0$が成り立つ。

（証明）$(f\ast g)(n)=\sum_{ab=n}f(a)g(b)$である。仮定より$a\vert f(a), b\vert g(b)$だから$n\vert f(a)g(b)$となり、$(f\ast g)(n)\equiv_{n}0$を得る。

$\overline{f}\neq 0$とする。$f(n)\not\equiv_{n}0$となる最小の$n$を取り$(f\ast u)(n)=\sum_{ab=n}f(a)u(b)$を考える。仮定より$b\vert u(b)$かつ$a\lt n$について$a\vert f(n)$であり、$u$は可逆なので$(f\ast u)(n)\equiv_{n}f(n)u(1)=\pm f(n)\not\equiv_{n}0$を得る。$\square$

__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

1. $\overline{f\ast\mu}=0$が成り立つ。
1. $\overline{g\ast\mathfrak{z}}=0$を満たす$g\in\mathbb{A}_{\mathbb{Z}}$について$\overline{f\ast g}=0$が成り立つ。
1. $k, m\in\mathbb{N}_{1}$とする。素数$p$は$m$と互いに素とする。このとき$f(p^{k}m)\equiv_{p^{k}}f(p^{k-1}m)$が成り立つ。
1. $n\in\mathbb{N}_{1}$と素数$p\vert n$について$f(n)\equiv_{n}f(n/p)$が成り立つ。

（証明）$1\Leftrightarrow 2$を示す。$\overline{f\ast\mu}=0$とする。$\overline{g\ast\mathfrak{z}}=0$なら先の命題より$\overline{f\ast g}=\overline{(f\ast\mu)\ast(\mathfrak{z}\ast g)}=0$を得る。逆に2番目を仮定すると、$\overline{\mu\ast\mathfrak{z}}=\overline{\varepsilon}=0$より$\overline{f\ast\mu}=0$となる。

$1\Rightarrow 3$を示す。$\overline{f\ast\mu}=0$とする。メビウス反転公式より$f=(f\ast\mu)\ast\mathfrak{z}$、従って

$$
\begin{aligned}
f(p^{k}m) &=\sum_{d\vert p^{k}m}(f\ast\mu)(d)=\sum_{d\vert p^{k-1}m}(f\ast\mu)(d)+\sum_{d\vert m}(f\ast\mu)(p^{k}d) \\
&=f(p^{k-1}m)+\sum_{d\vert m}(f\ast\mu)(p^{k}d)
\end{aligned}
$$

が成り立つ。ここで$(f\ast\mu)(p^{k}d)\equiv_{p^{k}d}0$だから特に$p^{k}$の倍数である。故に$f(p^{k}m)\equiv_{p^{k}}f(p^{k-1}m)$を得る。


__補題__ （necklace counting lemma）