
# 余代数の例

ここでは余代数$(C, \Delta\colon C\rightarrow C\otimes C, \epsilon\colon C\rightarrow R)$の例をいくつか挙げる。

以下$R$は単位的可換環とする。




## グラフ余代数の例

後できちんと定義するが、ある種の有向グラフに対して余代数を定義することができる。


### 頂点のみ

$S$を集合として、$RS:=\bigoplus_{s\in S}Rs$と置く。この上の余代数構造を

$$
\begin{aligned}
\Delta(s) &=s\otimes s, \\
\epsilon(s) &=1
\end{aligned}
$$

で定める。

これは$S$を頂点集合とする辺の無いグラフに対応している。


### 有向辺

$U_{2}:=Rg\oplus Rx\oplus Rh$の余代数構造を

$$
\begin{aligned}
\Delta(g) &=g\otimes g, & \Delta(x) &=g\otimes x+x\otimes h, & \Delta(h) &=h\otimes h, \\
\epsilon(g) &=1, & \epsilon(x) &=0, & \epsilon(h) &=1
\end{aligned}
$$

で定める。

これは$\lbrace p, q \rbrace$を頂点とするグラフに対応しており、対応する有向辺は$g=e_{pp}, x=e_{pq}, h=e_{qq}$である。


### 完全グラフ

$\mathbb{M}_{n}(R)$は$n$次正方行列全体とする。これは$(i, j)$成分が$1$でそれ以外が$0$の行列$e_{ij}$により生成される。このとき余代数構造を

$$
\begin{aligned}
\Delta(e_{ij}) &=\sum_{k}e_{ik}\otimes e_{kj}, \\
\epsilon(e_{ij}) &=\delta_{i, j}
\end{aligned}
$$

で定める。行列余代数と呼ばれる。

これは$\lbrace 1, \dotsc, n \rbrace$を頂点とする完全グラフに他ならない。




## グラフ余代数の剰余余代数の例

余代数には余イデアルという部分加群を定義でき、剰余加群もまた余代数となることが知られている。


### 微分作用素

$R\oplus R\partial$上の余代数構造を

$$
\begin{aligned}
\Delta(1) &=1\otimes 1, & \Delta(\partial) &=\partial\otimes 1+1\otimes\partial \\
\epsilon(1) &=1, & \epsilon(\partial) &=0
\end{aligned}
$$

で定める。

実際、例えば

$$
\begin{aligned}
( \Delta\otimes\mathrm{id} )\circ\Delta(\partial) &=( \Delta\otimes\mathrm{id} )( \partial\otimes 1+1\otimes\partial )=\Delta(\partial)\otimes 1+1\otimes 1\otimes\partial \\
&=\partial\otimes 1\otimes 1+1\otimes\partial\otimes 1+1\otimes 1\otimes\partial \\
&=\partial\otimes 1\otimes 1+1\otimes\Delta(\partial)=( \mathrm{id}\otimes\Delta )( \partial\otimes 1+1\otimes\partial ) \\
&=( \mathrm{id}\otimes\Delta )\circ\Delta(\partial)
\end{aligned}
$$

より一致する。

これは$U_{2}$の余イデアル$\langle h-g \rangle$による剰余余代数である。


### 三角余代数

$Rc\otimes Rs$上の余代数構造を

$$
\begin{aligned}
\Delta(c) &=c\otimes c-s\otimes s, & \Delta(s) &=s\otimes c+c\otimes s, \\
\epsilon(c) &= 1, & \epsilon(s) &= 0
\end{aligned}
$$

で定める。三角余代数と呼ばれる。

サイズ$2$の行列余代数$\mathbb{M}_{2}(R)$において$e_{11}=c, e_{12}=s, e_{21}=s^{\prime}, e_{22}=c^{\prime}$と置くと、$c-c^{\prime}, s+s^{\prime}$で生成される部分加群は余イデアルとなる。三角余代数はこの剰余余代数である。


## 自然数の加法構造に関する余代数

$\bigoplus_{n\ge 0}Rd_{n}$上の余代数構造を

$$
\begin{aligned}
\Delta(d_{n}) &=\sum_{i+j=n}d_{i}\otimes d_{j}, \\
\epsilon(d_{n}) &=\delta_{n, 0}
\end{aligned}
$$

で定める。実際$\sum_{i+j+k}d_{i}\otimes d_{j}\otimes d_{k}$に帰着されるので余代数であることが分かる。

自然数の集合$\mathbb{N}$に、大小関係が$i\le j$のとき$i\rightarrow j$となるようなグラフ構造を考える。この有向辺$e_{ij}$から生成されるグラフ余代数はとても大きなものだが、$e_{ij}-e_{0(j-i)}$で生成される部分加群は余イデアルであり、上記はその剰余余代数となる。特に$d_{n}=\overline{e_{0n}}$である。



## その他？


### divided power coalgebra

$\bigoplus_{n\ge 0}Rd_{n}$上の余代数構造を

$$
\begin{aligned}
\Delta(d_{n}) &=\sum_{k=0}^{n}\left(\begin{matrix} n \\ k \end{matrix}\right) d_{k}\otimes d_{n-k}, \\
\epsilon(d_{n}) &=\delta_{n, 0}
\end{aligned}
$$

で定める。divided power coalgebraと呼ばれる。

> ひょっとしたら上手く余イデアルを取れば実現できるかもしれないが、グラフ余代数としては実現できていない。

グラフの「重み」を$i\rightarrow k\rightarrow j$に対して$\gamma_{ikj}\in R$が以下を満たすとき定義する。

- $a\rightarrow b\rightarrow c\rightarrow d$について$\gamma_{abc}\gamma_{acd}=\gamma_{abd}\gamma_{bcd}$が成り立つ。
- $i\rightarrow j$について$\gamma_{iij}=\gamma_{ijj}=1$が成り立つ。

このとき

$$
\begin{aligned}
\Delta(e_{ij}) &=\sum_{i\rightarrow k\rightarrow j}\gamma_{ikj}e_{ik}\otimes e_{kj}, \\
\epsilon(e_{ij}) &=\delta_{i, j}
\end{aligned}
$$

は余代数を定める。（重み付きグラフ余代数と呼ぶ。）

divided power coalgebraは

$$
\gamma_{abc}=\frac{(c-a)!}{(b-a)!(c-b)!}
$$

による重み付きグラフ余代数である。