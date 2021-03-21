
# ネックレス合同

数論的函数のうち整数値を取るもの全体を$\mathbb{A}_{\mathbb{Z}}$とする。和や畳み込みは整数値であることを変えず、また$0$や$\varepsilon$も整数値なので、$\mathbb{A}_{\mathbb{Z}}$は$\mathbb{A}$の部分環となる。

__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

- $f$は$\mathbb{A}_{\mathbb{Z}}$において可逆である。
- $f(1)=\pm 1$である。

特に$\mathbb{A}_{\mathbb{Z}}^{\times}\lt\mathbb{A}^{\times}$は部分群となる。

（証明）$f\ast g=\varepsilon$なら$1=\varepsilon(1)=f(1)g(1)$より$f(1)=\pm 1$である。逆に$f(1)=\pm 1$のとき$f$は$\mathbb{A}$において可逆である。このとき逆元の作り方より$\neg f$は整数値を取る。よって$\neg f\in\mathbb{A}_{\mathbb{Z}}$となる。$\square$








$n\in\mathbb{N}_{1}$に対し$\mathbb{Z}/n\mathbb{Z}$の元を対応させる写像全体を$\mathbb{A}_{\equiv}$と表す。写像$\mathbb{A}_{\mathbb{Z}}\rightarrow\mathbb{A}_{\equiv}$を以下で定める。

- $f\in\mathbb{A}_{\mathbb{Z}}$に対し$\overline{f}(n):=\overline{f(n)}\in\mathbb{Z}/n\mathbb{Z}$を対応させる。

このとき$f\mapsto\overline{f}$は全射である。また$\mathbb{A}_{\equiv}$において成分毎の和と積を定義でき、$\overline{f+g}=\overline{f}+\overline{g}$や$\overline{f\cdot g}=\overline{f}\cdot \overline{g}$を満たす。


__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

- $\overline{f\ast\mu}=0$が成り立つ。
- $\overline{g\ast\mathfrak{z}}=0$を満たす$g\in\mathbb{A}_{\mathbb{Z}}$について$\overline{f\ast g}=0$が成り立つ。
- $n\in\mathbb{N}_{1}$と素数$p\vert n$について$f(n)\equiv_{n}f(n/p)$が成り立つ。
- 素数$p$と$k\in\mathbb{N}$、$p$と互いに素な$m\in\mathbb{N}_{1}$について$f(p^{k+1}m)\equiv_{p^{k+1}}f(p^{k}m)$が成り立つ。









__補題__ （necklace counting lemma）