
# メビウス函数の計算

### メビウス函数の例～自然数の通常の順序～

まず自然数の通常の順序$( \mathbb{N}_{0}, \le )$を考えよう。このincidence coalgebraを$N$とする。簡単のため、基底を$i\le j$について$e_{i, j}$と表す。

$N$のメビウス函数は定義に沿って計算すると

$$
\begin{aligned} \mu( e_{i, i} )&=1, \\ \mu( e_{i, i+1} )&=-\mu( e_{i+1, i+1} )=-1, \\ \mu( e_{i, i+2} )&=-( \mu( e_{i+2, i+2} )+\mu( e_{i+1, i+2} ) )=0, \\ \mu( e_{i, i+3} )&=-( \mu( e_{i+3, i+3} )+\mu( e_{i+2, i+3} )+\mu( e_{i+1, i+3} ) )=0, \\ \vdots & \end{aligned}
$$

と求めることができる。どうやら$e_{i, j}$のうち$j-i$が等しいもので同一の値を取るようだ。

$N$は余代数として大きすぎる。そこで部分加群$I=\langle e_{i, j}-e_{0, j-i} \rangle$を考えると、

$$
\begin{aligned}\Delta( e_{i, j}-e_{0, j-i} ) &= \sum_{i\le k\le j} e_{i, j}e_{k, j}-\sum_{i\le k\le j}e_{0, k-i}e_{k-i, j-i} \\ &=\sum_{i\le k\le j} \lbrace e_{i, k}( e_{k, j}-e_{0, j-k})+( e_{i, k}-e_{0, k-i} )e_{0, j-k}-e_{0, k-i}( e_{k-i, j-i}-e_{0, j-k} ) \rbrace \end{aligned}
$$

より$I$はイデアルとなる。（テンソル積の記号$\otimes$は省略した。）従って剰余余代数$N/I$を考えることができる。

剰余余代数$N/I$の双対代数を考えよう。$N/I$の代表元は$e_{0, n}$なので、これに対応する値$a_{n}$で双対の元は完全に決定される。従って$( N/I )^{\mathrm{dual}}$の元は数列$a=( a_{0}, a_{1}, a_{2}, \dotsc )$とみなせる。この同一視で$a, b\in ( N/I )^{\mathrm{dual}}$のconvolution積は

$$
( a\ast b )_{n}=( a\ast b )( \overline{e_{0, n}} )=\sum_{0\le k\le n}a( \overline{e_{0, k}} )b( \overline{e_{k, n}} )=\sum_{0\le k\le n}a( \overline{e_{0, k}} )b( \overline{e_{0, n-k}} )=\sum_{0\le k\le n}a_{k}b_{n-k}
$$

と表せるから、$( N/I )^{\mathrm{dual}}$は形式的冪級数環$R\lbrack\lbrack x \rbrack\rbrack$と$R$代数として同型である。

更にメビウス函数について$\mu( e_{i, j}-e_{0, j-i} )=0$である。つまり$\mu\in ( N/I )^{\mathrm{dual}}$は$N/I$のメビウス函数であり、$\mu=( 1, -1, 0, 0, \dotsc )$と同一視できる。形式的冪級数としては$1-x$に対応する。

メビウス反転に依れば、$N$上で$A=a\ast\mathfrak{z}$について$a=A\ast\mu$が成り立つ。つまり

$$
A( e_{i, j} )=\sum_{i\le k\le j}a( e_{i, k} )=\sum_{0\le n\le j-i}a_{n}=:A_{j-i}
$$

は$I$の剰余類上で一意的な値を取り、このとき

$$
a_{n}=A_{n}-A_{n-1}
$$

が成り立つ。



### メビウス函数の例～自然数の積順序～

次に自然数の積順序$( \mathbb{N}_{1}, \vert )$を考えよう。ここで$d\vert n$は$d$が$n$を割り切ることを指す。素因数分解の一意性より自然数$n$は素数$p_{1}, \dotsc, p_{r}$を用いて

$$
n=p_{1}^{n_{1}}\dotsm p_{r}^{n_{r}}
$$

と一意的に表せる。よって半順序集合として

$$
( \mathbb{N}_{1}, \vert )\cong\bigoplus_{p}( \lbrace p^{k} \rbrace, \vert )
$$

が成り立つ。更に$( \lbrace p^{k} \rbrace, \vert )$は半順序集合として$( \mathbb{N}_{0}, \le )$と同型である。故に$( \mathbb{N}_{1}, \vert )$のincidence coalgebraを$P$とすると、

$$
P\cong\bigoplus_{p}N_{p}
$$

が成り立つ。（ただし$N_{p}$は$N$のコピーとする。）定義域の直和は、双対を取ると直積になるので

$$
P^{\mathrm{dual}}\cong\prod_{p}N_{p}^{\mathrm{dual}}
$$

を得る。この同型により$\phi=( \phi_{p} )\in P^{\mathrm{dual}}$の値は、各基底$d=p_{1}^{k_{1}}\dotsm p_{r}^{k_{r}}\vert n$に関して

$$
\phi( d\vert n )=\phi_{p_{1}}( p_{1}^{k_{1}}\vert p_{1}^{n_{1}} )\dotsm\phi_{p_{r}}( p_{r}^{k_{r}}\vert p_{r}^{n_{r}} )=\phi_{p_{1}}( e_{k_{1}, n_{1}} )\dotsm\phi_{p_{r}}( e_{k_{r}, n_{r}} )
$$

と計算される。

次に$P^{\mathrm{dual}}$におけるconvolution積を観察する。$\phi=( \phi_{p} ), \psi=( \psi_{p} )\in P^{\mathrm{dual}}$に対して

$$
\begin{aligned} ( \phi\ast\psi )( d\vert n )&=\sum_{d\vert m\vert n}\phi( d\vert m )\psi( m\vert n ) \\ &=\sum_{k_{1}\le l_{1}\le n_{1}}\dotsb\sum_{k_{r}\le l_{r}\le n_{r}}\phi_{p_{1}}( e_{k_{1}, l_{1}} )\dotsm\phi_{p_{r}}( e_{k_{r}, l_{r}} )\psi_{p_{1}}( e_{l_{1}, n_{1}} )\dotsm\psi_{p_{r}}( e_{l_{r}, n_{r}} ) \\ &= \left( \sum_{k_{1}\le l_{1}\le n_{1}}\phi_{p_{1}}( e_{k_{1}, l_{1}} )\psi_{p_{1}}( e_{l_{1}, n_{1}} ) \right)\dotsm\left( \sum_{k_{r}\le l_{r}\le n_{r}}\phi_{p_{r}}( e_{k_{r}, l_{r}} )\psi_{p_{r}}( e_{l_{r}, n_{r}} ) \right) \\ &= ( \phi_{p_{1}}\ast\psi_{p_{1}} )( e_{k_{1}, n_{1}} )\dotsm( \phi_{p_{r}}\ast\psi_{p_{r}} )( e_{k_{r}, n_{r}} ) \end{aligned}
$$

より、$\phi\ast\psi=( \phi_{p}\ast\psi_{p} )$であることがわかる。故に$\phi_{p}^{\prime}=( \varepsilon, \dotsc, \varepsilon, \phi_{p}, \varepsilon, \dotsc )\in P^{\mathrm{dual}}$を、$N_{p}$に属す成分が$\phi_{p}$、それ以外の素数$q$について$N_{q}$に属す成分が$\varepsilon_{q}$となるような元とすると、

$$
\phi=\phi_{p_{1}}^{\prime}\ast\phi_{p_{2}}^{\prime}\ast\dotsb=:\bigodot_{p}\phi_{p}^{\prime}
$$

とconvolution積による分解が得られる。（厳密には、素数を小さい順に並べてた上で$r$番目までの素数$p( 1 ), \dotsc, p( r )$を固定し、$\phi_{p( 1 )}^{\prime}\ast\dotsm\ast\phi_{p( r )}^{\prime}$の極限として右辺を定義する。）この分解を**convolution分解**と呼ぶ。

以上を利用して$P$のメビウス函数を計算してみよう。$\mathfrak{z}\in P^{\mathrm{dual}}$は全ての$d\vert n$について$\mathfrak{z}( d\vert n )=1$だから、$\mathfrak{z}=( \mathfrak{z}_{p} )$は全ての$k_{i}\le n_{i}$について$\mathfrak{z}_{p}( e_{k_{1}, n_{i}} )=1$となる。$N_{p}^{\mathrm{dual}}$の単位元を$\varepsilon_{p}$とすれば$\varepsilon=( \varepsilon_{p} )$が$P^{\mathrm{dual}}$の単位元であることに注意すれば、$N_{p}$のメビウス函数を$\mu_{p}$として

$$
( \mathfrak{z}_{p} )\ast( \mu_{p} )=( \mathfrak{z}_{p}\ast\mu_{p} )=( \varepsilon_{p} )=\varepsilon
$$

を得る。従って$\mu:=( \mu_{p} )$が$P$のメビウス函数である。そこでconvolution分解を$\bigodot_{p}\mu_{p}^{\prime}$とおく。

前節でも述べたように、$P$もまた余代数として大きすぎる。そこでイデアル

$$
I:=\left\langle d\vert n-1\vert\frac{n}{d} \right\rangle
$$

による剰余余代数$P/I$を考える。$P/I$の基底の代表元は$1\vert n$なので、これに対応する値$\alpha( n )$で双対代数の元は完全に決定される。従って$( P/I )^{\mathrm{dual}}$は数論的函数$\alpha\colon\mathbb{N}_{1}\rightarrow R$全体とみなせる。この同一視で$\alpha, \beta\in ( P/I )^{\mathrm{dual}}$のconvolution積は

$$
( \alpha\ast\beta )_{n}=( \alpha\ast\beta )( \overline{1\vert n} )=\sum_{1\vert d\vert n}\alpha( \overline{1\vert d} )\beta( \overline{d\vert n} )=\sum_{1\vert d\vert n}\alpha( \overline{1\vert d} )\beta\left( \overline{1\vert\frac{n}{d}} \right)=\sum_{1\vert d\vert n}\alpha( d )\beta\left( \frac{n}{d} \right)
$$

と表せる。これは数論的函数におけるconvolution積に他ならない。更に$\alpha\in( P/I )^{\mathrm{dual}}$をDirichlet級数

$$
\sum_{n=1}^{\infty}\frac{\alpha( n )}{n^{s}}
$$

に対応させれば、convolution積$\alpha\ast\beta$は級数の積に対応する。

さて、メビウス函数は$I$上でゼロなので$( P/I )^{\mathrm{dual}}$の元と見なせる。$\mu( 1 )=1$であり、$n=p_{1}^{n_{1}}\dotsm p_{r}^{n_{r}}$について

$$
\mu( n )=\mu( \overline{1\vert n} )=\mu( 1\vert n )=\mu_{p_{1}}( e_{0, n_{1}} )\dotsm\mu_{p_{r}}( e_{0, n_{r}} )
$$

は$n_{p}\ge 2$なる$p$があれば$\mu( n )=0$である。一方で$n_{1}=\dotsb=n_{r}=1$のときは$\mu( n )=( -1 )^{r}$である。従って$\mu$は良く知られた（数論的函数の）メビウス函数に他ならない。よってDirichlet級数はリーマンのゼータ函数を用いて

$$
\frac{1}{\zeta( s )}=\sum_{n=1}^{\infty}\frac{\mu( n )}{n^{s}}
$$

と表せる。一方、$\mu_{p}^{\prime}$も$I$上でゼロなので$( P/I )^{\mathrm{dual}}$の元と見なせる。よってconvolution分解は$( P/I )^{\mathrm{dual}}$においても意味を持つ。$\mu_{p}^{\prime}( n )$は$n=1$のとき$1$、$n=p$のとき$-1$であり、それ以外はゼロとなる。だから$\mu_{p}^{\prime}$のDirichlet級数は

$$
1-\frac{1}{p^{s}}
$$

であり、convolution分解によって

$$
\frac{1}{\zeta( s )}=\prod_{p}\left( 1-\frac{1}{p^{s}} \right)
$$

が従う。これはオイラー積表示に他ならない。



## 補足

オイラー積表示の右辺は厳密には

$$
\lim_{r\rightarrow\infty}\prod_{m=1}^{r}\left( 1-\frac{1}{p( m )^{s}} \right)
$$

と表すべきものなので、Dirichlet級数として意味を持つのは極限の中身、つまり$\mu_{p( 1 )}^{\prime}\ast\dotsb\ast\mu_{p( r )}^{\prime}$に対応するDirichlet級数である。極限は、これが$\mu$のDirichlet級数の有限項を近似しているという意味での極限なので、上記のオイラー積表示が意味を持つためには、Dirichlet級数の空間に適切な収束概念を定義する必要がある。この収束概念が、函数としての収束を表すかは分からない。いずれにせよ、上記のオイラー積表示は形式的なものなので、正しく意味を持っているかは不明なことに注意するべきだろう。とはいえ函数論的な議論でオイラー積は厳密に証明できたはずなので、あまり心配には及ばないかもしれない。

ところで$I_{p}=\langle e_{k_{p}, n_{p}}-e_{0, n_{p}-k_{p}} \rangle$とすると$I=\bigoplus_{p}I_{p}$であることに注意して

$$
P/I\cong\bigoplus_{p} N_{p}/I_{p}
$$

が分かる。よって

$$
( P/I )^{\mathrm{dual}}\cong\prod_{p}( N_{p}/I_{p} )^{\mathrm{dual}}
$$

が成り立つ。この表示に何か意味はあるだろうか。