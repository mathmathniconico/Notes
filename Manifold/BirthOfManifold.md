
## 多様体

$\mathbb{R}^{n}$と局所的に同相な貼合わせとして多様体を定義したい。そのためには少なくとも各点のまわりの位相構造がきちんと分離されているべきだろう。そうでなければ例えば点列の収束先が一意に決まらなかったりして、解析的に扱い辛くなり、曲線や曲面概念の抽象化とはいえない。従って以下考える多様体はHausdorff空間とする。

__定義__ Hausdorff空間$M$において、開集合の族$\lbrace U_{\lambda} : \lambda\in\Lambda \rbrace$が以下の条件を満たすとき、$C^{r}$級の開被覆であるという。

- $M=\bigcup_{\lambda\in\Lambda}U_{\lambda}$である。
- $U_{\lambda}$は$C^{r}$級の座標をもつ空間である。
- $U_{\lambda}\cap U_{\mu}\neq\empty$のとき、それぞれの座標写像は$U_{\lambda}\cap U_{\mu}$上の座標写像として互いに$C^{r}$同値である。

__定義__ $C^{r}$級の開被覆$\lbrace U_{\alpha} : \alpha\in A \rbrace$と$\lbrace V_{\beta} : \beta\in B \rbrace$が以下の条件を満たすとき$C^{r}$同値であるという。

- $U_{\alpha}\cap V_{\beta}\neq\empty$のとき、それぞれの座標写像は$U_{\alpha}\cap V_{\beta}\neq\empty$上の座標写像として互いに$C^{r}$同値である。

座標をもつ空間においては、座標写像と$C^{r}$同値なものを同一視して$C^{r}$構造を定めた。$S^{1}$の例では、こうした構造の貼合わせを考えたが、開被覆の$C^{r}$同値を定義した今となっては、もはや不要な議論である。

Hausdorff空間$M$上に、ひとたび$C^{r}$級の開被覆$\lbrace U_{\lambda} : \lambda\in\Lambda \rbrace$（と座標写像の族$\lbrace \phi_{\lambda} \rbrace$）が与えられれば、$M$上の$C^{s}$級（$s\le r$）写像$f$を$f\circ \phi_{\lambda}^{-1}$が$C^{s}$級であることをもって定義できる。これまでの議論と同様に、写像が$C^{s}$級であることは、同値な$C^{r}$級の開被覆の選び方に依らず決まる。

ここで少し厄介な事情を垣間見ることが出来る。上では$C^{r}$級の開被覆より、$C^{s}$級の写像族が決まっている。写像の可微分性は開被覆の可微分性に依存する、このことを少し心に留めておこう。

以上を良くある書き方で纏めておく。

__定義__ Hausdorff空間$M$について、$M$を覆う開集合の族$\lbrace U_{\lambda} : \lambda\in\Lambda \rbrace$が存在し、各$\lambda\in\Lambda$に対して$U_{\lambda}$から$\mathbb{R}^{n}$のある開集合への同相写像$\phi_{\lambda}$が存在して、$U_{\lambda}\cap U_{\mu}\neq\empty$のとき$\phi_{\mu}\circ\phi_{\lambda}^{-1}$が$\phi_{\lambda}(U_{\lambda}\cap U_{\mu})$から$\phi_{\mu}(U_{\lambda}\cap U_{\mu})$への$C^{r}$級函数であるとする。このとき$M$上の$C^{r}$級の写像族は$C^{r}$同値な$C^{r}$級の開被覆の取り方に依らず決まる。これを$M$の$C^{r}$構造と呼び、この構造にのみ関係する性質を取り扱うとき、$M$を$n$次元$C^{r}$多様体（manifold）という。

__定義__ 上の記号で$U_{\lambda}$あるいは$( U_{\lambda}, \phi_{\lambda} )$を局所座標、その全体を局所座標系という。$\phi_{\beta}\circ\phi_{\alpha}^{-1}$は座標変換と呼ばれる。


## 多様体の例：ユークリッド空間の一般曲面

最も基本的な多様体としてユークリッド空間の一般曲面を定義する。

$\mathbb{R}^{L}$上で定義された$L-n$個の函数$f_{1}, \dotsc, f_{L-n}$は$C^{r}$級とする。これらの零点集合を

$$
M:=\lbrace x=(x_{1}, \dotsc, x_{L}) : f_{1}(x)=\dotsb=f_{L-n}(x)=0 \rbrace
$$

とおき、以下を仮定する。

- $r\ge 1$である。
- $M$の各点においてJacobi行列（$(L-n)\times L$行列）

    $$
    \left\lbrack
    \begin{matrix}
    \frac{\partial f_{1}}{\partial x_{1}} & \cdots & \frac{\partial f_{1}}{\partial x_{L}} \\
    \vdots & \ddots & \vdots \\
    \frac{\partial f_{L-n}}{\partial x_{1}} & \cdots & \frac{\partial f_{L-n}}{\partial x_{L}}
    \end{matrix}
    \right\rbrack
    $$

    の階数が$L-n$である。

$M$上の点$P_{0}$において、仮定よりJacobi行列の右側$L-n$次正方行列の行列式はゼロでない。陰関数定理より$P_{0}$の$M$における開近傍$U(P_{0})$及び、$\mathbb{R}^{n}$上の$C^{r}$級函数$g_{1}, \dotsc, g_{L-n}$が存在して、

$$
U(P_{0})=\lbrace (x_{1}, \dotsc, x_{n}, g_{1}(x), \dotsc, g_{L-n}(x) ) : x=(x_{1}, \dotsc, x_{n})\in\mathrm{proj}( U(P_{0}) ) \rbrace
$$

と表せる。ただし$\mathrm{proj}$は$\mathbb{R}^{L}$の最初の$n$成分への射影とする。

$U(P_{0})$はこの射影を座標写像とする座標をもつ空間であり、更に座標写像は互いに$C^{r}$同値である。故に$M$は$n$次元$C^{r}$多様体である。


## 多様体の例：実射影空間

$\mathbb{R}^{n+1}$の原点を通る直線全体を$P^{n}$とする。原点を通る直線上の点は定数倍で移り合うことで特徴付けられるから、$\mathbb{R}^{n+1}\backslash\lbrace 0 \rbrace$の元$x, y$に対して$t\neq 0$によって$y=tx$となるとき$x\sim y$と定めると$\sim$は同値関係となる。要するに原点と点$x\neq 0$を通る直線は、各成分の比$\lbrack x_{1} : \dotsb : x_{n+1} \rbrack$によって表される。この対応により

$$
P=(\mathbb{R}^{n+1}\backslash\lbrace 0 \rbrace)/\sim
$$

とみなせるので、$P^{n}$に商位相を入れることができる。この位相がHausdorff空間となることは、2点を分離する放射状の開集合を考えれば明らかである。

ここで$U_{i}:=\lbrace \lbrack x_{1} : \dots : x_{n+1} \rbrack : x_{i}\neq 0 \rbrace$とおく。$U_{i}$から$\mathbb{R}^{n}$への写像$\phi_{i}$を

$$
\phi_{i}(\lbrack x_{1} : \dots : x_{n+1} \rbrack):=\left( \frac{x_{1}}{x_{i}}, \dotsc, \frac{x_{i-1}}{x_{i}}, \frac{x_{i+1}}{x_{i}}, \dotsc, \frac{x_{n+1}}{x_{i}} \right)
$$

によって定めると、これは位相同型であるから$U_{i}$は座標をもつ空間となる。$P^{n}=U_{1}\cup\dotsb\cup U_{n+1}$であり、$\phi_{j}\circ\phi_{i}^{-1}$は$C^{\infty}$級であるため、$P^{n}$は$n$次元$C^{\infty}$多様体である。

__注意__ 一般に原点を通る$d$次元平面全体の集合にも$C^{\infty}$多様体としての構造を入れることが出来る。これをGrassmann多様体という。このように直観が働きにくい対象も数学的に扱えるのが多様体を考える一つの利点でもある。
