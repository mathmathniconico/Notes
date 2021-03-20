
# ネックレス合同

数論的函数のうち整数値を取る場合を考える。和や畳み込みは整数値であることを変えず、また$0$や$\varepsilon$も整数値なので、整数値を取る数論的函数全体$\mathbb{A}_{\mathbb{Z}}$は$\mathbb{A}$の部分環となる。

$n\in\mathbb{N}_{1}$に対し$\mathbb{Z}/n\mathbb{Z}$の元を対応させる写像全体を$\mathbb{A}_{\equiv}$と表す。写像$\mathbb{A}_{\mathbb{Z}}\rightarrow\mathbb{A}_{\equiv}$を以下で定める。

- $f\in\mathbb{A}_{\mathbb{Z}}$に対し$\overline{f}(n):=\overline{f(n)}\in\mathbb{Z}/n\mathbb{Z}$を対応させる。

このとき$f\mapsto\overline{f}$は全射である。また$\mathbb{A}_{\equiv}$は成分毎の和と積を定義でき、$\overline{f+g}=\overline{f}+\overline{g}$や$\overline{f\cdot g}=\overline{f}\cdot \overline{g}$を満たす。更に$\overline{f_{1}}=\overline{f_{2}}, \overline{g_{1}}=\overline{g_{2}}$なら

$$
\begin{aligned}
\overline{f_{1}\ast g_{1}}(n) &=\overline{\sum_{ab=n}f_{1}(a)g_{1}(b)}=\sum_{ab=n}\overline{f_{1}(a)}\cdot\overline{g_{1}(b)} \\
&=\sum_{ab=n}\overline{f_{2}(a)}\cdot\overline{g_{2}(b)}=\overline{\sum_{ab=n}f_{2}(a)g_{2}(b)} \\
&=\overline{f_{2}\ast g_{2}}(n)
\end{aligned}
$$

だから、$\mathbb{A}_{\equiv}$上にも畳み込みを定義でき、$f\mapsto\overline{f}$は$+, \cdot, \ast$を保つ準同型となる。









__命題__ $f\in\mathbb{A}_{\mathbb{Z}}$とする。TFAE

- $f$は$\mathbb{A}_{\mathbb{Z}}$において可逆である。
- $f(1)=\pm 1$である。

特に$\mathbb{A}_{\mathbb{Z}}^{\times}\lt\mathbb{A}^{\times}$は部分群となる。

（証明）$f\ast g=\varepsilon$なら$1=\varepsilon(1)=f(1)g(1)$より$f(1)=\pm 1$である。逆に$f(1)=\pm 1$のとき$f$は$\mathbb{A}$において可逆である。このとき逆元の作り方より$\neg f$は整数値を取る。よって$\neg f\in\mathbb{A}_{\mathbb{Z}}$となる。$\square$













__補題__ （necklace counting lemma）