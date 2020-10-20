
# 半順序集合のIncidence Algebra

## Rotaの定理

$( P_{0}, \le )$を半順序集合（partially ordered set, poset）とする。

$$
P_{1}:=\lbrace \lbrack x, y \rbrack : x, y\in P_{0}, x\le y \rbrace
$$

と置けば、

$$
\begin{aligned} s\lbrack x, y \rbrack&=x, & t\lbrack x, y \rbrack&=y, & \lbrack y, z \rbrack\circ\lbrack x, y \rbrack&=\lbrack x, z \rbrack \end{aligned}
$$

及び$1_{x}=( x, x )$で$( P_{0}, P_{1}, s, t, \circ, 1 )$は小さな圏となる。

特に半順序集合が局所有限（$x\le z\le y$なる$z$は有限個）のとき、この小さな圏も局所有限であり、したがってincidence coalgebra $P$やincidence algebra $P^{\mathrm{dual}}$を定義できる。

半順序集合のincidence algebraで重要な性質は次の命題だろう。以下$\vert x, y \vert$で$\lbrace z : x\le z \le y \rbrace$の元の個数を表す。

**命題** 以下が成り立つ。

- $\vert x, x \vert=1$である。
- $x\le z\lt y$のとき$\vert x, z \vert\lt\vert x, y \vert$が成り立つ。
- $x\lt z\le y$のとき$\vert z, y \vert\lt\vert x, y \vert$が成り立つ。

（証明）一つ目は$x\le y\le x$なら$y=x$より明らか。二つ目も$x\le t\le z$なら$x\le t\le y$だが$t\le z\lt y$より$t\neq y$となることから分かる。$\square$

**定理**（Rotaの定理） $\phi\in P^{\mathrm{dual}}$について以下は同値である。

- $\phi$は可逆である。つまりある$\psi\in P^{\mathrm{dual}}$が存在して$\phi\ast\psi=\psi\ast\phi=\varepsilon$が成り立つ。
- 任意の$x\in P_{0}$について$\phi( \lbrack x, x \rbrack )\in R$は可逆である。

（証明）$\phi$が可逆なら

$$
\phi\ast\psi( \lbrack x, x \rbrack )=\phi( \lbrack x, x \rbrack )\psi( \lbrack x, x \rbrack )=\varepsilon( \lbrack x, x \rbrack )=1
$$

より$\phi( \lbrack x, x \rbrack )$は可逆である。逆は$\psi$を具体的に構成することで得られる。まず$\psi( \lbrack x, x \rbrack ):=\phi( \lbrack x, x \rbrack )^{-1}$と置く。$x\lt y$に対しては$\vert x, y \vert$に関して帰納的に定義する。

$$
\varepsilon( \lbrack x, y \rbrack )=( \phi\ast\psi )( \lbrack x, y \rbrack )=\sum_{x\le z\le y}\phi( \lbrack x, z \rbrack )\psi( \lbrack z, y \rbrack )
$$

が成り立てばよいので、

$$
\psi( \lbrack x, y \rbrack ):=-\phi( \lbrack x, x \rbrack )^{-1}\sum_{x\le z\lt y}\phi( \lbrack x, z \rbrack )\psi( \lbrack z, y \rbrack )
$$

と置けばよい。これで$\phi$の右側逆元$\psi_{R}$の存在が言えたが、同様に左側逆元$\psi_{R}$の存在も言える。両者が一致することは、良く知られているように

$$
\psi_{L}=\psi_{L}\ast\varepsilon=\psi_{L}\ast\phi\ast\psi_{R}=\varepsilon\ast\psi_{R}=\psi_{R}
$$

より従う。$\square$



## メビウス函数

Rotaの定理の応用として任意の$\lbrack x, y \rbrack\in P_{1}$で$\mathfrak{z}( \lbrack x, y \rbrack )=1$を取る写像$\mathfrak{z}$は可逆となる。この逆元$\mu:=\mathfrak{z}^{-1}\in P^{\mathrm{dual}}$を$P$の**メビウス函数**と呼ぶ。このときいわゆる**メビウス反転**

$$
\Phi=\phi\ast\mathfrak{z}\Longrightarrow \phi=\Phi\ast\mu
$$

が成り立つ。つまり

$$
\Phi( f )=\sum_{x\le z\le y}\phi( \lbrack x, z \rbrack )\Longrightarrow\phi( f )=\sum_{x\le z\le y}\Phi( \lbrack x, z \rbrack )\mu( \lbrack z, y \rbrack )
$$

が成り立つ。

更に$N$を$P$のイデアルとして、$\mu$は$N$上で恒等的にゼロとする。このとき$\mu\in( C/N )^{\mathrm{dual}}$と見なせるが、これを$C/N$のメビウス函数と呼ぶ。

- $\varepsilon( N )=0$より$1_{x}\notin N$である。
- $\mathfrak{z}$は$( C/N )^{\mathrm{dual}}$の元ではない。

**疑問** $\mu$は$N$上で恒等的にゼロとなるか？

広義において、incidence coalgebraはその剰余余代数を含むとする。またincidence algebraは、上記の双対代数を含むとする。



## 補足

Rotaの定理は一般には成り立たない。というのも小さな圏がループを持っていたり、自分自身への射が複数存在すると帰納法が働かないので逆元を構成できない。命題で挙げた条件をうまい具合に翻訳できれば、もう少し良い形のRotaの定理が示せるだろうけどよく分からない。
