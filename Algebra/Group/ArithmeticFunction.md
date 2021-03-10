
# 数論的函数

__定義__ $f\colon\mathbb{N}_{1}\rightarrow\mathbb{C}$を **数論的函数** （arithmetic function）と呼ぶ。

__例__ 以下に数論的函数の例を挙げる。

- $\delta(1)=1$および$n\neq 1$のとき$\delta(n)=0$とする。
- $\underline{1}(n):=1$、$\underline{0}(n):=0$とする。
- $d(n)$は$n$の約数の個数とする。
- $\phi(n)$は$n$と互いに素な$1$以上$n$以下の整数の個数とする。（オイラーの **totient函数** と呼ぶ。）
- $L(n):=\log{n}$とする。

$f, g$を数論的函数とする。$f$と$g$の和$f+g$および **convolution積** $f\ast g$を

$$
\begin{aligned}
(f+g)(n) &:=f(n)+g(n) \\
(fg)(n) &:=\sum_{d\vert n}f(d)g\left( \frac{n}{d} \right)
\end{aligned}
$$

によって定める。このとき数論的函数全体は単位的可換環となる。