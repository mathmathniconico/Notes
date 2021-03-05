
# 対称群

__定義__ $X$を集合とする。写像$\sigma\colon X\rightarrow X$が全単射のとき、$\sigma$を$X$上の **置換** （permutation）と呼び、その全体を$\mathrm{Sym}X$と表す。

$\mathrm{Sym}X$は写像の合成によって群となる。

> $\sigma\in\mathrm{Sym}X, x\in X$について$\sigma\cdot x:=\sigma(x)$と定めると、$(\tau\sigma)\cdot x=(\tau\circ\sigma)(x)=\tau(\sigma(x))=\tau\cdot(\sigma\cdot x)$であり、左からの作用$\mathrm{Sym}X\curvearrowright X$を定める。

__定義__ $S_{n}:=\mathrm{Sym}\lbrace 1, \dotsc, n \rbrace$を$n$次の **対称群** （symmetric group）と呼ぶ。


対称群の元の記法はいくつか流儀があるが、上の行を下の行に対応させる写像としての記法を採用する。つまり$\sigma\in S_{n}$は

$$
\sigma=\left\lbrack \begin{matrix} 1 & 2 & \cdots & n \\ \sigma(1) & \sigma(2) & \cdots & \sigma(n) \end{matrix} \right\rbrack
$$

と表す。写像の合成は

$$
\begin{aligned}
\tau\sigma &=\left\lbrack \begin{matrix} 1 & 2 & \cdots & n \\ \tau(1) & \tau(2) & \cdots & \tau(n) \end{matrix} \right\rbrack\left\lbrack \begin{matrix} 1 & 2 & \cdots & n \\ \sigma(1) & \sigma(2) & \cdots & \sigma(n) \end{matrix} \right\rbrack \\
&=\left\lbrack \begin{matrix} 1 & 2 & \cdots & n \\ \tau(\sigma(1)) & \tau(\sigma(2)) & \cdots & \tau(\sigma(n)) \end{matrix} \right\rbrack
\end{aligned}
$$

となる。

__定義__ $\sigma\in S_{n}$とする。ある$1\le i_{1}, \dotsc, i_{k}\le n$が存在して、$j\neq i_{s}$なら$\sigma(j)=j$であり

$$
\begin{aligned}
\sigma(i_{1})&=i_{2}, & &\dotsc, & \sigma(i_{k-1})&=i_{k}, & \sigma(i_{k})&=i_{1}
\end{aligned}
$$

が成り立つとする。このとき$\sigma$を **巡回置換** （cycle）と呼び、

$$
\sigma=(i_{1}\enspace i_{2}\enspace\dotsc\enspace i_{k})
$$

と表す。$k$を$\sigma$の **長さ** （length）と呼ぶ。長さ$2$の巡回置換を **互換** （transposition）と呼び、更に$(i\enspace i+1)$の形のものを **隣接互換** （adjacent transposition）と呼ぶ。

__命題__ 任意の置換は巡回置換の積で表せる。

（証明）$n$に関する帰納法で示す。$n=1$のときは明らか。$\sigma\in S_{n}$は巡回置換でないとしてよい。$T:=\lbrace \sigma^{k}(1) : k\ge 0 \rbrace$とすると、ある$0\lt k\lt n$で$\sigma^{k}(1)=1$となる。このような最小の$k$を取る。$\tau:=(1\enspace\sigma(1)\enspace\dotsc\enspace\sigma^{k-1}(1))$とすると、$\tau^{-1}\sigma$は$T$を変えないので$S_{n-k}$の元とみなして良い。帰納法の仮定より$\tau^{-1}\sigma$は巡回置換の積で表せるから、左から$\tau$を掛ければ$\sigma$も巡回置換の積で表せる。$\square$

__命題__ 任意の置換は互換の積で表せる。

（証明）先の命題より任意の巡回置換に対して示せば良い。$(i_{1}\enspace\dotsc\enspace i_{k})=(i_{1}\enspace i_{2})\dotsm(i_{k-1}\enspace i_{k-2})(i_{k}\enspace i_{k-1})$より従う。$\square$

__命題__ 任意の置換は隣接互換の積で表せる。

（証明）先の命題より任意の互換に対して示せば良い。$i\lt j$について

$$
(i\enspace j)=(i\enspace i+1)\dotsm(j-2\enspace j-1)(j-1\enspace j)(j-2\enspace j-1)\dotsm(i\enspace i+1)
$$

より従う。$\square$

> 上記は$s_{i}=(i\enspace i+1)$（$1\le i\le n-1$）が$S_{n}$の生成元であることを示している。これらは組紐関係式
>
> $$
> \begin{aligned}
> s_{i}^{2}&=1, & s_{i}s_{j}&=s_{j}s_{i}\quad(\vert i-j \vert\ge 2), & s_{i}s_{i+1}s_{i}&=s_{i+1}s_{i}s_{i+1}
> \end{aligned}
> $$
>
> を満たし、逆にこのような関係式を満たす$s_{i}$により生成される群は$S_{n}$と同型となる。ちなみに例えば$(1\enspace 2), \dotsc, (1\enspace n)$の$n$個の互換や、$(1\enspace 2), (1\enspace\dotsc\enspace n)$の$2$個の巡回置換などによっても$S_{n}$は生成される。










