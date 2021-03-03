
# 例示：群




## 巡回群

> TODO




## 対称群

__定義__ $X$を集合とする。写像$f\colon X\rightarrow X$が全単射のとき、$f$を$X$上の **置換** （permutation）と呼び、その全体を$\mathrm{Sym}X$と表す。

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


### 三次対称群$S_{3}$

三次対称群$S_{3}:=\mathrm{Sym}\lbrace 1, 2, 3 \rbrace$を具体的に書き下してみよう。

$S_{3}$の元を巡回置換で表示し、1列目を$\tau$、1行目を$\sigma$としたときの$\tau\circ\sigma$を表にした。

$$
\begin{matrix}
(1) & (2\,3) & (1\,2) & (1\,2\,3) & (1\,3\,2) & (1\,3) \\
(2\,3) & (1) & (1\,3\,2) & (1\,3) & (1\,2) & (1\,2\,3) \\
(1\,2) & (1\,2\,3) & (1) & (2\,3) & (1\,3) & (1\,3\,2) \\
(1\,2\,3) & (1\,2) & (1\,3) & (1\,3\,2) & (1) & (2\,3) \\
(1\,3\,2) & (1\,3) & (2\,3) & (1) & (1\,2\,3) & (1\,2) \\
(1\,3) & (1\,3\,2) & (1\,2\,3) & (1\,2) & (2\,3) & (1) \\
\end{matrix}
$$





## 自己同型群

Aut G

内部自己同型群 Inn G


## 群と部分群の例

__例__ 以下は群の例である。

- $\mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}$は、加法に関してアーベル群となる。単位元は$0$で、$a$の逆元は$-a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$から原点を除いた集合$k^{\times}$は、乗法に関してアーベル群となる。単位元は$1$で、$a$の逆元は$1/a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$n$次正則行列全体$\mathrm{GL}(n; k)$は、行列の積に関して群となる。このような群を一般線型群という。

__例__ 以下は部分群の例である。

- $\mathbb{Z}\lt\mathbb{Q}\lt\mathbb{R}\lt\mathbb{C}$である。
- $\mathbb{T}_{1}=\lbrace z\in\mathbb{C} : \vert z \vert=1 \rbrace$は$\mathbb{C}^{\times}$の部分群である。これを$1$次元トーラスという。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$\mathrm{SL}(n; k):=\lbrace A\in\mathrm{GL}(n; k) : \mathrm{det}A=1 \rbrace$は$\mathrm{GL}(n; k)$の部分群である。これを特殊線型群という。
- 正方形でない長方形$R$を$R$自身に写す変換は$4$頂点の置換で表され、その全体$V$は$S_{4}$の部分群となる。これをクラインの$4$群という。

> TODO 合同関係と正規部分群の例、準同型と同型の例
