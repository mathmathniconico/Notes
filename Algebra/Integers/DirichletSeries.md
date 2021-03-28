
# ディリクレ級数

__定義__ $f\in\mathbb{A}$とする。形式的な級数

$$
Df(s):=\sum_{n\ge 1}\frac{f(n)}{n^{s}}
$$

を **ディリクレ級数** （Dirichlet's series）と呼ぶ。

- $\mathfrak{z}\in\mathbb{A}$のディリクレ級数$\zeta(s):=\sum_{n\ge 1}\frac{1}{n^{s}}$は **リーマンのゼータ函数** （Riemann's zeta function）と呼ばれる。

__命題__ 数論的函数にディリクレ級数を対応させる写像は畳み込みを級数の形式的積に写し、従って環準同型である。

（証明）$f, g\in\mathbb{A}$とする。

$$
\begin{aligned}
\left( \sum_{n\ge 1}\frac{f(n)}{n^{s}} \right)\cdot\left( \sum_{n\ge 1}\frac{g(n)}{n^{s}} \right) &=\sum_{n\ge 1}\sum_{ab=n}\frac{f(a)}{a^{s}}\frac{g(b)}{b^{s}}=\sum_{n\ge 1}\frac{1}{n^{s}}\sum_{ab=n}f(a)g(b) \\
&=\sum_{n\ge 1}\frac{(f\ast g)(n)}{n^{s}}
\end{aligned}
$$

より畳み込みを級数の積に写す。$\square$

- $\mu\ast\mathfrak{z}=\varepsilon$だから$D\mu\cdot D\mathfrak{z}=1$より$\sum_{n\ge 1}\frac{\mu(n)}{n^{s}}=\frac{1}{\zeta(s)}$が成り立つ。
- $\angle(n):=n$のディリクレ級数は$\sum_{n\ge 1}\frac{n}{n^{s}}=\zeta(s-1)$である。$\angle=\varphi\ast\mathfrak{z}$より、$\sum_{n\ge 1}\frac{\varphi(n)}{n^{s}}=\frac{\zeta(s-1)}{\zeta(s)}$である。