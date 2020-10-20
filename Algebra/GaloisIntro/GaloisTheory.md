
# 代数体のガロア理論

## 代数体

体$K$が$k=\mathbb{Q}$上の有限次拡大であるとき、$K$を代数体と呼ぶ。

**命題** 最小多項式はその分解体において重根を持たない。

（証明）$p\in k\lbrack x \rbrack$を最小多項式、$K$を分解体とする。$p$は$K\lbrack x \rbrack$において一次の積で表せるから

$$
p( x )=x^{n}+a_{n-1}x^{n-1}+\dotsb+a_{1}x+a_{0}=( x-\alpha_{1} )\dotsm( x-\alpha_{n} )
$$

と表せる。ただし$a_{0}, \dotsc, a_{n-1}\in k$であり、$\alpha_{1}, \dotsc, \alpha_{n}\in K$である。

$p$が重根$\alpha$を持つとしよう。このとき$K\lbrack x \rbrack$において$p( x )=( x-\alpha )^{2}g( x )$と表せるが、形式的な微分を考えると

$$
p^{\prime}( x )=nx^{n-1}+( n-1 )a_{n-1}x^{n-2}+\dotsb+a_{1}=2( x-\alpha )g( x )+( x-\alpha )^{2}g^{\prime}( x )
$$

となる。（ライプニッツ則と微分の線型性より従う。）左辺より$p^{\prime}\neq 0$は$k\lbrack x \rbrack$の元であり、右辺に$x=\alpha$を代入するとゼロとなることから$p^{\prime}$も$\alpha$を根に持つ。これは$p$の最小性に矛盾する。$\square$

$k=\mathbb{Q}$としたが、一般的な体$k$（$\mathbb{Q}$を含まない体）上では$p^{\prime}\equiv 0$の可能性があり、上記の命題が成り立たないので少し難しくなる。

**定理** 代数体は単拡大である。

（証明）$K/k$を有限次拡大とすると、ベクトル空間としての基底は有限個なので、有限集合$S$を用いて$K=k( S )$と表せる。従って2つの元で生成される体$K=k( \alpha, \beta )$が単拡大であることを示せば、一般の$K$についても帰納的に示せる。

$\alpha, \beta$の最小多項式を$p, q\in k\lbrack x \rbrack$とする。ここで積$pq$の分解体$L$を取ると、最小多項式は重根を持たないので、$L\lbrack x \rbrack$において

$$
\begin{aligned} p( x )&=\prod_{i=1}^{n}( x-\alpha_{i} ),& q( x )&=\prod_{j=1}^{m}( x-\beta_{j} ) \end{aligned}
$$

と相異な$\alpha_{i}\in L$と相異な$\beta_{j}\in L$で表せる。ここで$\alpha_{1}=\alpha, \beta_{1}=\beta$と仮定して良い。$m=1$のときは$k( \alpha, \beta )=k( \alpha )$である。$m\ge 2$のときは、$c\in k$を

$$
c\notin\left\lbrace \frac{\alpha-\alpha_{i}}{\beta{j}-\beta} : 1\le i \le n, 2\le j \le m \right\rbrace
$$

となるように取り、$\gamma=\alpha+c\beta$と置く。明らかに$k( \alpha, \beta )\supset k( \gamma )$である。$f( x ):=p( \gamma-cx )\in k( \gamma )\lbrack x \rbrack$を考える。$f( \beta )=p( \alpha )=0$より、$\beta$は$f$の根である。また$\beta$は$q$の根でもあるが、$f$と$q$の唯一の共通根となる。実際$f$は$\beta_{2}, \dotsc, \beta_{m}$を根に持たない。なぜなら

$$
f( \beta_{j} )=p( \gamma-c\beta_{j} )=p( \alpha+c( \beta-\beta_{j} ) )=\prod_{i=1}^{n}( ( \alpha-\alpha_{i} )-c( \beta_{j}-\beta ) )
$$

となるが、$c$は右辺のそれぞれがゼロにならないように取った。$\beta$の$k( \gamma )$上の最小多項式を$g$とすると、$g$は共通根が1つしかない$f$と$q$を割り切るので一次であり、$g=x-\beta$と分かる。$g\in k( \gamma )$より$\beta\in k( \gamma )$となる。故に$\alpha=\gamma-c\beta\in k( \gamma )$となり$K=k( \gamma )$を得る。つまり$K$は単拡大である。$\square$

**例** $\mathbb{Q}( \sqrt{2}, \sqrt{3} )$が単拡大であることを定理に沿って示してみよう。$\sqrt{2}, \sqrt{3}$の最小多項式は$p=x^{2}-2, q=x^{2}-3$である。よって

$$
\alpha_{1}=\sqrt{2}, \alpha_{2}=-\sqrt{2}, \beta_{1}=\sqrt{3}, \beta_{2}=-\sqrt{3}
$$

となる。従って$c\neq 0, \frac{\sqrt{2}}{2\sqrt{3}}$を取ればよいので$c=1$としてよい。つまり$\mathbb{Q}( \sqrt{2}, \sqrt{3} )=\mathbb{Q}( \sqrt{2}+\sqrt{3} )$である。実際$\gamma:=\sqrt{2}+\sqrt{3}$とすると、$\gamma^{2}=5+2\sqrt{6}$より$\sqrt{6}=\frac{1}{2}\gamma^{2}-\frac{5}{2}$であり、

$$
\sqrt{2}=( 3\sqrt{2}+2\sqrt{3} )-2( \sqrt{2}+\sqrt{3} )=\gamma\sqrt{6}-2\gamma=\frac{1}{2}\gamma^{3}-\frac{9}{2}\gamma
$$

を得る。$\sqrt{3}$は$\gamma-\sqrt{2}$を計算すればよい。

**問** 一般に$\gamma$から$\alpha, \beta$を求めるアルゴリズムはあるか？



## ガロアの基本定理

最初に代数体がガロア拡大となる特徴付けを行う。

**補題** $k=\mathbb{Q}$とする。代数体$K=k( \alpha )$について、以下は同値である。

- $K/k$はガロア拡大である。
- $K$は$\alpha$の最小多項式の根を全て含む。

従って$K/k$がガロア拡大のとき、$| \mathrm{Gal}( K/k ) |=\lbrack K : k \rbrack$が成り立つ。

（証明）まず$\alpha$の最小多項式を$p\in k\lbrack x \rbrack$として、$p$の$K$における相異な根全体を$\lbrace \alpha_{1}=\alpha, \dotsc, \alpha_{m} \rbrace$とする。このとき$m\le\mathrm{deg}( p )$である。写像$\alpha\mapsto\alpha_{i}$は中への同型$k( \alpha )\rightarrow k( \alpha )$を引き起こすが、その像$k( \alpha_{i} )\subset k( \alpha )$は$k( \alpha )$と同型なので、ベクトル空間としての次元を比較すると$k( \alpha_{i} )=k( \alpha )$が成り立つ。つまり$\alpha\mapsto\alpha_{i}$は自己同型になる。従って

$$
\mathrm{Aut}( k( \alpha )/k )=\lbrace \alpha\mapsto\alpha_{i} : i=1, \dotsc, m \rbrace
$$

が成り立つ。

$K/k$をガロア拡大とする。ここで

$$
f=\prod_{i=1}^{m}( x-\alpha_{i})=c_{0}+c_{1}x+\dotsb+c_{m}x^{m}\in K\lbrack x \rbrack
$$

を取ると、$\sigma\in\mathrm{Aut}( K/k )$について

$$
\lbrace \alpha_{1}^{\sigma}, \dotsc, \alpha_{m}^{\sigma} \rbrace=\lbrace \alpha_{1}, \dotsc, \alpha_{m} \rbrace
$$

が成り立つ。解と係数の関係より

$$
f^{\sigma}( x ):=c_{0}^{\sigma}+c_{1}^{\sigma}x+\dotsb+c_{m}^{\sigma}x^{m}=\prod_{i=1}^{m}( x-\alpha_{i}^{\sigma} )=\prod_{i=1}^{m}( x-\alpha_{i} )=f( x )
$$

となるから、$c_{i}^{\sigma}=c_{i}$を得る。これが任意の$\sigma\in\mathrm{Aut}( K/k )$について言えるから、

$$
c_{i}\in K^{\mathrm{Aut}( K/k )}=k
$$

となる。従って$f\in k\lbrack x \rbrack$であり、$f( \alpha )=0$より最小性から$f=p$でなければならない。つまり$K=k( \alpha )$は$p$の根を全て含む。

逆に$K$が$p$の根$\alpha_{1}=\alpha, \dotsc, \alpha_{n}$を全て含むとする。$\theta\in K^{\mathrm{Aut}( K/k )}$とする。まず$k$上の基底$1, \alpha, \dotsc, \alpha^{n-1}$を用いて

$$
\theta=c_{0}+c_{1}\alpha+\dotsb+c_{n-1}\alpha^{n-1}, \quad c_{i}\in k
$$

と表せる。ここで任意の$\sigma\in\mathrm{Aut}( K/k )$について

$$
\theta^{\sigma}=\theta=c_{0}+c_{1}\alpha^{\sigma}+\dotsb+c_{n-1}( \alpha^{\sigma} )^{n-1}
$$

が成り立つ。つまり$\alpha^{\sigma}$は$n-1$次以下の多項式

$$
c_{n-1}x^{n-1}+\dotsb+c_{1}x+c_{0}-\theta\in k\lbrack x \rbrack
$$

の根となるが、$\alpha^{\sigma}$は相異な$n$個の元を定めるため、この多項式は恒等的にゼロである。故に$\theta=c_{0}\in k$を得る。$\square$

**例** $\mathbb{Q}( \sqrt[3]{2} )/\mathbb{Q}$はガロア拡大ではない。なぜなら$\sqrt[3]{2}$の最小多項式は$x^{3}-2$であり、その根は$\sqrt[3]{2}, \omega\sqrt[3]{2}, \omega^{2}\sqrt[3]{2}$であるが、後ろの2つを$\mathbb{Q}( \sqrt[3]{2} )$は含まない。

**例** $\mathbb{Q}( \sqrt{2} )/\mathbb{Q}$はガロア拡大である。実際$\sqrt{2}$の最小多項式$x^{2}-2$の根は$\sqrt{2}, -\sqrt{2}\in\mathbb{Q}( \sqrt{2} )$を満たす。

次にガロアの基本定理と呼ばれる定理を示そう。

**定理** $k=\mathbb{Q}$とする。代数体$K:=k( \alpha )$について$K/k$はガロア拡大、$G:=\mathrm{Gal}( K/k )$とする。

- 中間体$M$について$K/M$はガロア拡大である。特に$\Psi( \Phi( M ) )=M$が成り立つ。
- ガロア群の部分群$H$について$\Phi( \Psi( H ) )=H$が成り立つ。

（証明）$M$を中間体とする。前節では本質的に$k$が$\mathbb{Q}$を含むことのみを用いていた。従って有限次拡大$K/M$もまた単拡大であることが分かる。そこで$K=M( \beta )$と表し、$\beta\in K$の$M$上の最小多項式を$q\in M\lbrack x \rbrack$として$pq$の分解体$E$を取る。このとき$q$は$E\lbrack x \rbrack$において一次の積

$$
q( x )=\prod_{j=1}^{m}( x-\beta_{j} )\in E\lbrack x \rbrack
$$

で表せる。すると$\beta\mapsto \beta_{j}$は中への同型$M( \beta )\rightarrow E$を定めるが、それは中への同型$K\rightarrow E$のことであるから、$\alpha\mapsto\alpha_{i}$のどれかになる。$K/k$はガロア拡大であるから$\alpha_{i}\in K$であり、それゆえ$\beta\mapsto\beta_{j}$の像は$K$に含まれる。特に$\beta_{j}\in K$である。故に$\mathrm{Aut}( K/M )$の元は拡大次数$m=\lbrack K : M \rbrack$と同じだけあることが分かり、補題の証明と同様にして$K/M$がガロア拡大であることが分かる。

$H$をガロア群の部分群とする。$\alpha$の$K^{H}$上の最小多項式を$f\in K^{H}\lbrack x \rbrack$とすると$\lbrack K : K^{H} \rbrack=\mathrm{deg}( f )$が成り立つ。ここで

$$
g( x ):=\prod_{\sigma\in H}( x-\alpha^{\sigma} )
$$

とおくと、各係数は$H$の作用で不変となるから$g\in K^{H}\lbrack x \rbrack$である。$g( \alpha )=0$より$f$は$g$を割り切る。従って

$$
\lbrack K : K^{H} \rbrack=\mathrm{deg}( f )\le\mathrm{deg}( g )=| H |
$$

を得る。$H\subset G_{K^{H}}$より群の位数を比較すると$H=G_{K^{H}}$が分かる。$\square$

**問** $K/k$がガロア拡大のとき、中間体$M$について$M/k$がガロア拡大となるのはどういうときか？



## ガロア群の計算例

最後に$K=\mathbb{Q}( \sqrt[3]{2}, \omega )$について、$\mathbb{Q}( \sqrt[3]{2}, \omega )/\mathbb{Q}$のガロア群$G$を計算して、ガロアの基本定理を検証しよう。

まず$\lbrack \mathbb{Q}( \sqrt[3]{2}, \omega ) : \mathbb{Q} \rbrack=6$なので$| G |=6$である。一方で$\sqrt[3]{2}$と$\omega$の$\mathbb{Q}$上の最小多項式は$x^{3}-2, x^{2}+x+1$だから、同型の候補となるのは$\sqrt[3]{2}\mapsto \sqrt[3]{2}, \omega\sqrt[3]{2}, \omega^{2}\sqrt[3]{2}$と$\omega\mapsto\omega, \omega^{2}$の組み合わせでちょうど6種類となる。つまりこの6個の同型がガロア群を定める。ここで

$$
\sigma:\left\lbrace \begin{aligned} \sqrt[3]{2} &\mapsto \omega\sqrt[3]{2} \\ \omega &\mapsto \omega \end{aligned}\right. , \quad \tau:\left\lbrace \begin{aligned} \sqrt[3]{2} &\mapsto \sqrt[3]{2} \\ \omega &\mapsto \omega^{2} \end{aligned}\right.
$$

とおくと、各々の同型は$\sigma$と$\tau$の積で表せる。表し方は複数あるが、

$$
\begin{aligned} \sigma^{3}&=\mathrm{id},& \tau^{2}&=\mathrm{id},& \sigma\tau&=\tau\sigma^{2} \end{aligned}
$$

という関係で同一視できる。これは3次対称群$S_{3}$と呼ばれるものと同型となる。

ガロアの基本定理に依れば、$\mathbb{Q}( \sqrt[3]{2}, \omega )$の中間体は、このガロア群$S_{3}$の部分群によって完全に決定される。$S_{3}$の部分群は良く知られており、位数2の部分群

$$
\langle \tau \rangle, \langle \tau\sigma \rangle, \langle \sigma\tau \rangle
$$

と、位数3の部分群

$$
\langle \sigma \rangle
$$

である。これに対応する中間体を計算し、表にまとめると次のようになる。

| 部分群$H$ | 中間体$K^{H}$ | $\lbrack K : K^{H} \rbrack=\vert H \vert$ |
|:-:|:-:|:-:|
| $\lbrace \mathrm{id} \rbrace$ | $\mathbb{Q}( \sqrt[3]{2}, \omega )$ | 1 |
| $\langle \tau \rangle$ | $\mathbb{Q}( \sqrt[3]{2} )$ | 2 |
| $\langle \tau\sigma \rangle$ | $\mathbb{Q}( \omega^{2}\sqrt[3]{2} )$ | 2 |
| $\langle \sigma\tau \rangle$ | $\mathbb{Q}( \omega\sqrt[3]{2} )$ | 2 |
| $\langle \sigma \rangle$ | $\mathbb{Q}( \omega )$ | 3 |
| $S_{3}$ | $\mathbb{Q}$ | 6 |

互いに逆の対応になっていることが分かるだろうか。