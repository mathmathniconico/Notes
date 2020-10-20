
# ガロア拡大

## 自己同型

同型とはその名の通り、体として同じ型であることを表す。つまり同型という対応によって一方の演算がそのまま他方の演算に写るため、代数的には両者が同一なものとみなすことが出来る。

基礎体$k$を共有する拡大$K/k, L/k$に対し、写像$\sigma\colon K\rightarrow L$が$k$上の**同型**であるとは、準同型（演算をそのまま写す）であって、全単射であり、$k$上で恒等写像のときをいう。このとき$K$と$L$は同型といい、$K\cong L$と表す。特に$K=L$のとき$K$上の**自己同型**と呼び、その全体を$\mathrm{Aut}( K/k )$と表す。自己同型全体は写像の合成で**群**を為し、一般に元$\alpha\in K$に対する$\sigma\in\mathrm{Aut}( K/k )$の作用を$\alpha^{\sigma}:=\sigma( \alpha )$と表す。

上記を要約したものが以下のリストである。なお写像の合成は$\sigma, \tau\in\mathrm{Aut}( K/k )$に対して、$\sigma$の後に$\tau$を作用させることを$\tau\circ\sigma$あるいは$\sigma\tau$と書く。

- $\alpha, \beta\in K$について$( \alpha+\beta )^{\sigma}=\alpha^{\sigma}+\beta^{\sigma}, ( \alpha\beta )^{\sigma}=\alpha^{\sigma}\beta^{\sigma}$である。
- $\sigma$について$\sigma^{-1}\in\mathrm{Aut}( K/k )$が存在して$\sigma\circ\sigma^{-1}=\sigma^{-1}\circ\sigma=\mathrm{id}$は恒等写像である。
- $c\in k$について$c^{\sigma}=c$である。
- $\alpha\in K$について$\alpha^{\mathrm{id}}=\alpha$である。
- $\alpha\in K$について$( \alpha^{\sigma} )^{\tau}=\alpha^{\sigma\tau}=\alpha^{( \tau\circ\sigma )}$である。

では有限次拡大$K/k$において、$\alpha\in K$について単拡大$k( \alpha )$と同型な体はどれくらいあるだろうか。$\sigma\colon k( \alpha )\rightarrow K$を中への同型（$K/k$のある中間体への同型）とする。

$$
f( x )=a_{0}+a_{1}x+\dotsb+a_{n-1}x^{n-1}+a_{n}x^{n}\in k\lbrack x \rbrack
$$

について$\alpha$が$f$の根とする。このとき

$$
f( \alpha )=a_{0}+a_{1}\alpha+\dotsb+a_{n-1}\alpha^{n-1}+a_{n}\alpha^{n}=0
$$

であるが、

$$
f( \alpha )^{\sigma}=a_{0}+a_{1}\alpha^{\sigma}+\dotsb+a_{n-1}( \alpha^{\sigma} )^{n-1}+a_{n}( \alpha^{\sigma} )^{n}=0
$$

となる。つまり$\alpha^{\sigma}$もまた$f$の根であることが分かる。特に$f$として$\alpha$の最小多項式$p$を取れば、$p$の別の根$\beta$について同型

$$
k( \alpha )\cong k\lbrack x \rbrack/( p )\cong k( \beta )
$$

を得る。体の同型はベクトル空間としての同型でもあり、更に$k( \alpha )$の基底は$\alpha$の冪で表せるから、中への同型$\sigma$は$\alpha$の行き先で決まる。このことから、中への同型は最小多項式の$K$における根と一対一に対応する。（同型の像とは対応しないことに注意。）

**例** $\mathbb{Q}( \sqrt[3]{2} )/\mathbb{Q}$において、自己同型は恒等写像のみである。実際$\sqrt[3]{2}$の最小多項式$x^{3}-2$の根は$\sqrt[3]{2}, \omega\sqrt[3]{2}, \omega^{2}\sqrt[3]{2}$であるが、$\mathbb{Q}( \sqrt[3]{2} )$に含まれるのは$\sqrt[3]{2}$のみである。

**例** $\mathbb{Q}( \omega )/\mathbb{Q}$において、自己同型は恒等写像と$\omega\mapsto \omega^{2}$の2通りある。実際$\omega$の最小多項式$x^{2}+x+1$の根は$\omega, \omega^{2}$であり、$\omega^{2}=-1-\omega\in\mathbb{Q}( \omega )$となる。

**例** $\mathbb{Q}( \omega, \sqrt[3]{2} )/\mathbb{Q}$において、$\mathbb{Q}( \sqrt[3]{2} )$と同型なのは他に$\mathbb{Q}( \omega\sqrt[3]{2} ), \mathbb{Q}( \omega^{2}\sqrt[3]{2} )$である。

**問** $k( \alpha )\cong k( \beta )$から何が言える？



## ガロア拡大

拡大$K/k$において、$\mathrm{Aut}( K/k )$は$K$の元に対して作用している。つまり$\sigma, \tau\in\mathrm{Aut}( K/k )$及び$\alpha\in K$について

- $\alpha^{\mathrm{id}}=\alpha$
- $\alpha^{\sigma\tau}=( \alpha^{\sigma} )^{\tau}$

が成り立つ。

一般に上記のような作用が与えられたとき、その作用で不変な部分を考えることができる。$S\subset\mathrm{Aut}( K/k ), \neq\emptyset$について、

$$
\Psi( S )=K^{S}:=\lbrace \alpha\in K : \forall\sigma\in S, \alpha^{\sigma}=\alpha \rbrace
$$

と定めると、これは$K/k$の中間体となる。

あるいは、ある部分を不変とする作用全体を考えることもできる。$k\subset T\subset K$について、

$$
\Phi( T )=\mathrm{Aut}( K/k )_{T}:=\lbrace \sigma\in\mathrm{Aut}( K/k ) : \forall\alpha\in T, \alpha^{\sigma}=\alpha \rbrace
$$

と定めると、これは$\mathrm{Aut}( K/k )$の部分群となる。（$T$を不変とする$\sigma, \tau$に対して$\sigma\tau$も$T$を不変とする。）

この2つの事実から、$K/k$の中間体と$\mathrm{Aut}( K/k )$の部分群との間の反変的な（互いに包含関係が逆となる）対応関係が見えてくる。$\Psi$の像は部分群が大きくなるほど小さくなる。

| $\Psi$による像 | $\mathrm{Aut}( K/k )$の部分群 |
|-|-|
| $K^{\lbrace \mathrm{id} \rbrace}=K$ | $\lbrace\mathrm{id}\rbrace$ |
| $K^{H}$ | $H$ |
| ？ | $\mathrm{Aut}( K/k )$ |

$\Phi$の像は中間体が小さくなるほど大きくなる。

| $K/k$の中間体 | $\Phi$による像 |
|-|-|
| $K$ | $\mathrm{Aut}( K/k )_{K}=\lbrace \mathrm{id} \rbrace$ |
| $M$ | $\mathrm{Aut}( K/k )_{M}=\mathrm{Aut}( K/M )$ |
| k | $\mathrm{Aut}( K/k )_{k}=\mathrm{Aut}( K/k )$ |

表中の？に注目してほしい。綺麗な対応を作りたければ、

$$
K^{\mathrm{Aut}( K/k )}=k
$$

が成り立つことが望ましい。

**定義** 拡大$K/k$は$K^{\mathrm{Aut}( K/k )}=k$を満たすとき、**ガロア拡大**と呼ぶ。特にこのとき$\mathrm{Aut}( K/k )$は$\mathrm{Gal}( K/k )$と表し**ガロア群**と呼ぶ。
