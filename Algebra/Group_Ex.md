
# 例示：群




## 巡回群

> TODO




## 対称群

__定義__ $X$を集合とする。写像$\sigma\colon X\rightarrow X$が全単射のとき、$\sigma$を$X$上の **置換** （permutation）と呼び、その全体を$\mathrm{Sym}X$と表す。

$\mathrm{Sym}X$は写像の合成によって群となる。

> このとき作用$\mathrm{Sym}X\curvearrowright X$が$\sigma\cdot x:=\sigma(x)$により定まる。群演算は$(\tau\sigma)\cdot x=(\tau\circ\sigma)(x)=\tau(\sigma(x))=\tau\cdot(\sigma\cdot x)$であり左から作用している。

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




### 三次対称群$S_{3}$

三次対称群$S_{3}:=\mathrm{Sym}\lbrace 1, 2, 3 \rbrace$の元を具体的に書き下してみよう。写像としての記法の下段を並べると全部で6種類あり

$$
123, 132, 213, 231, 312, 321
$$

から成る。それぞれを巡回置換で表せば

$$
(1), (2\enspace 3), (1\enspace 2), (1\enspace 2\enspace 3), (1\enspace 3\enspace 2), (1\enspace 3)
$$

となる。

次に乗積表を求めてみる。乗積表とは1列目を$\tau$、1行目を$\sigma$としたときの$\tau\sigma=\tau\circ\sigma$を表にしたものである。

$$
\begin{matrix}
(1) & (2\enspace 3) & (1\enspace 2) & (1\enspace 2\enspace 3) & (1\enspace 3\enspace 2) & (1\enspace 3) \\
(2\enspace 3) & (1) & (1\enspace 3\enspace 2) & (1\enspace 3) & (1\enspace 2) & (1\enspace 2\enspace 3) \\
(1\enspace 2) & (1\enspace 2\enspace 3) & (1) & (2\enspace 3) & (1\enspace 3) & (1\enspace 3\enspace 2) \\
(1\enspace 2\enspace 3) & (1\enspace 2) & (1\enspace 3) & (1\enspace 3\enspace 2) & (1) & (2\enspace 3) \\
(1\enspace 3\enspace 2) & (1\enspace 3) & (2\enspace 3) & (1) & (1\enspace 2\enspace 3) & (1\enspace 2) \\
(1\enspace 3) & (1\enspace 3\enspace 2) & (1\enspace 2\enspace 3) & (1\enspace 2) & (2\enspace 3) & (1) \\
\end{matrix}
$$

部分群の構造は次のようになる。$(1)$と$S_{3}$の他に、位数$2$の部分群が$3$つと、位数$3$の部分群が$1$つある。

<p align=center><img src="pics/sym3_subgroups.svg" height="200"></p>




### 四次対称群$S_{4}$

- 正方形でない長方形$R$を$R$自身に写す変換は$4$頂点の置換で表され、その全体$V$は$S_{4}$の部分群となる。これをクラインの$4$群という。

## 自己同型群

Aut G

内部自己同型群 Inn G


## その他の基本的な例

- $\mathbb{Z}\lt\mathbb{Q}\lt\mathbb{R}\lt\mathbb{C}$は加法に関してアーベル群である。単位元は$0$で、$a$の逆元は$-a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$から原点を除いた集合$k^{\times}$は、乗法に関してアーベル群となる。単位元は$1$で、$a$の逆元は$1/a$である。
- $\mathbb{T}_{1}=\lbrace z\in\mathbb{C} : \vert z \vert=1 \rbrace\lt\mathbb{C}^{\times}$は部分群であり、これを$1$次元トーラスという。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$n$次正則行列全体$\mathrm{GL}(n; k)$は、行列の積に関して群となる。このような群を一般線型群という。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$\mathrm{SL}(n; k):=\lbrace A\in\mathrm{GL}(n; k) : \mathrm{det}A=1 \rbrace$は$\mathrm{GL}(n; k)$の部分群である。これを特殊線型群という。



<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% sym3_subgroups.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& & S_{3} & \\
& & & (1\enspace 2\enspace 3), (1\enspace 3\enspace 2) \arrow[lu, dash] \\
(2\enspace 3) \arrow[rruu, dash] & (1\enspace 2) \arrow[ruu, dash] & (1\enspace 3) \arrow[uu, dash] & \\
& & (1) \arrow[llu, dash] \arrow[lu, dash] \arrow[u, dash] \arrow[ruu, dash] &
\end{tikzcd}
```


</details>


