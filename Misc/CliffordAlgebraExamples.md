
# クリフォード代数の例

例えば$X=\mathbb{Z}$として通常の大小関係を考える。符号は$x\ge 0$のとき$r( x )=1$として、$x\lt 0$のとき$r( x )=-1$とする。以下このクリフォード代数$\mathrm{Clif}( \mathbb{Z}, R, r )$を$\mathrm{Clif}( R )_{\infty, \infty}$と表すことにする。このとき$p, q\ge 0$に対して

$$
e_{-q}, \dotsc, e_{-1}, e_{0}, e_{1}, \dotsc, e_{p-1}
$$

で生成される部分代数（あるいは$X=\lbrace -q, \dotsc, p-1 \rbrace$のクリフォード代数）を$\mathrm{Clif}( R )_{q, p}$で表す。以下$R=\mathbb{R}$として計算してみよう。

$i_{1}\lt\dotsb\lt i_{t}$および$I=\lbrace i_{1}, \dotsc, i_{t} \rbrace$のとき$e_{i_{1}}\dotsm e_{i_{t}}=r( I )e_{I}$である。

行列代数$\mathbb{M}_{n}( R )$を$R( n )$と表す。

**例** $\mathrm{Clif}( \mathbb{R} )_{0, 0}=\mathbb{R}$である。

**例** $\mathrm{Clif}( \mathbb{R} )_{0, 1}=\mathbb{R}\oplus\mathbb{R}e_{0}$の積構造は

$$
( a+be_{0} )( c+de_{0} )=( ac+bd )+( ad+bc )e_{0}
$$

である。これは全単射$a+be_{0}\mapsto ( a+b, a-b )\in \mathbb{R}^{2}$によって

$$
\begin{aligned} ( a+b, a-b )( c+d, c-d ) &= ( ( ac+bd )+( ad+bc ), ( ac+bd )-( ad+bc ) ) \\ &= ( ( a+b )( c+d ), ( a-b )( c-d ) ) \end{aligned}
$$

に翻訳されるので、結局代数として成分毎の積構造を持つ$\mathbb{R}^{2}$と同型である。

**例** $\mathrm{Clif}( \mathbb{R} )_{1, 0}=\mathbb{R}\oplus\mathbb{R}e_{-1}$の積構造は

$$
( a+be_{-1} )( c+de_{-1} )=( ac-bd )+( ad+bc )e_{-1}
$$

である。これは複素数$\mathbb{C}$に他ならない。つまり$a+be_{-1}\mapsto a+bi$と対応させればよい。

**例** $\mathrm{Clif}( \mathbb{R} )_{0, 2}=\mathbb{R}\oplus\mathbb{R}e_{0}\oplus\mathbb{R}e_{1}\oplus\mathbb{R}e_{0, 1}$の積構造は$e_{0, 1}=e_{0}e_{1}$に注意すると

| | $1$ | $e_{0}$ | $e_{1}$ | $e_{0, 1}$ |
|:-:|:-:|:-:|:-:|:-:|
| $1$ | $1$ | $e_{0}$ | $e_{1}$ | $e_{0, 1}$ |
| $e_{0}$ | $e_{0}$ | $1$ | $e_{0, 1}$ | $e_{1}$ |
| $e_{1}$ | $e_{1}$ | $-e_{0, 1}$ | $1$ | $-e_{0}$ |
| $e_{0, 1}$ | $e_{0, 1}$ | $-e_{1}$ | $e_{0}$ | $-1$ |

によって決まる。（積の順序は行が左、列が右とする。）天下りで恐縮だが

$$
\begin{aligned} 1 &\mapsto\left( \begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} \right), & e_{0} &\mapsto\left( \begin{matrix} 1 & 0 \\ 0 & -1 \end{matrix} \right), & e_{1} &\mapsto\left( \begin{matrix} 0 & 1 \\ 1 & 0 \end{matrix}\right), & e_{0, 1}& \mapsto\left( \begin{matrix} 0 & 1 \\ -1 & 0 \end{matrix} \right) \end{aligned}
$$

と対応させると、代数としての同型を与える。従って行列代数$\mathbb{R}( 2 )$と同型である。なお上記は対角成分がちょうど$\mathrm{Clif}( \mathbb{R} )_{0, 1}$になるように定義した。

**例** $\mathrm{Clif}( \mathbb{R} )_{1, 1}=\mathbb{R}\oplus\mathbb{R}e_{-1}\oplus\mathbb{R}e_{0}\oplus\mathbb{R}e_{-1, 0}$の積構造は、$e_{-1, 0}=e_{-1}e_{0}$に注意すると、

| | $e_{-1}$ | $e_{0}$ | $e_{-1, 0}$ |
|:-:|:-:|:-:|:-:|
| $e_{-1}$ | $-1$ | $e_{-1, 0}$ | $-e_{0}$ |
| $e_{0}$ | $-e_{-1, 0}$ | $1$ | $-e_{-1}$ |
| $e_{-1, 0}$ | $e_{0}$ | $e_{-1}$ | $1$ |

である。並び替えて

| | $e_{-1, 0}$ | $e_{0}$ | $e_{-1}$ |
|:-:|:-:|:-:|:-:|
| $e_{-1, 0}$ | $1$ | $e_{-1}$ | $e_{0}$ |
| $e_{0}$ | $-e_{-1}$ | $1$ | $-e_{-1, 0}$ |
| $e_{-1}$ | $-e_{0}$ | $e_{-1, 0}$ | $-1$ |

とすれば$\mathrm{Clif}( \mathbb{R} )_{0, 2}$の右下と同等である。よって

$$
\begin{aligned} 1 &\mapsto\left( \begin{matrix} 1 & 0 \\ 0 & 1 \end{matrix} \right) , & e_{-1, 0} &\mapsto\left( \begin{matrix} 1 & 0 \\ 0 & -1 \end{matrix} \right), & e_{0} &\mapsto\left( \begin{matrix} 0 & 1 \\ 1 & 0 \end{matrix}\right), & e_{-1} &\mapsto\left( \begin{matrix} 0 & 1 \\ -1 & 0 \end{matrix} \right) \end{aligned}
$$

と対応させれば$\mathbb{R}( 2 )$と同型になる。

今後の為にもう少し状況を詳しく見ておこう。$\alpha+\beta e_{-1}+\gamma e_{0}+\delta e_{-1, 0}$は上の対応によって

$$
\left( \begin{matrix} \alpha+\delta & \gamma+\beta \\ \gamma-\beta & \alpha-\delta \end{matrix} \right)
$$

に写る。

TODO

**例** $\mathrm{Clif}( \mathbb{R} )_{2, 0}=\mathbb{R}\oplus\mathbb{R}e_{-2}\oplus\mathbb{R}e_{-1}\oplus\mathbb{R}e_{-2, -1}$の積構造は、$e_{-2, -1}=e_{-2}e_{-1}$に注意すると

| | $e_{-2}$ | $e_{-1}$ | $e_{-2, -1}$ |
|:-:|:-:|:-:|:-:|
| $e_{-2}$ | $-1$ | $e_{-2, -1}$ | $-e_{-1}$ |
| $e_{-1}$ | $-e_{-2, -1}$ | $-1$ | $e_{-2}$ |
| $e_{-2, -1}$ | $e_{-1}$ | $-e_{-2}$ | $-1$ |

である。ここで

$$
\begin{aligned} e_{-1}&\mapsto i, & e_{-2, -1}&\mapsto j, & e_{-2}&\mapsto k \end{aligned}
$$

とすれば$i^{2}=j^{2}=k^{2}=-1$かつ$ij=k, jk=i, ki=j, ijk=-1$となる。よって四元数$\mathbb{H}$と同型になる。

ここまでの分類をまとめると、次の表になる。

| $\mathbb{R}$ | $p=0$ | $1$ | $2$ | $3$ |
|:-:|:-:|:-:|:-:|:-:|
| $q=0$ | $\mathbb{R}$ | $\mathbb{R}^{2}$ | $\mathbb{R}( 2 )$ | ? |
| $1$ | $\mathbb{C}$ | $\mathbb{R}( 2 )$ | ? | ? |
| $2$ | $\mathbb{H}$ | ? | ? | ? |
| $3$ | ? | ? | ? | ? |

**例** $\mathrm{Clif}( \mathbb{R} )_{3, 0}$は

$$
\begin{aligned} &1, & &e_{-3}, & &e_{-2}, & &e_{-1}, & &e_{-3, -2}, & &e_{-3, -1}, & &e_{-2, -1}, & &e_{-3, -2, -1} \end{aligned}
$$

を基底とするベクトル空間である。この積構造は次のようになる。ただし対角成分以外で可換な場合は下線を引いた。

|  | $e_{-3}$ | $e_{-2}$ | $e_{-1}$ | $e_{-3, -2}$ | $e_{-3, -1}$ | $e_{-2, -1}$ | $e_{-3, -2, -1}$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $e_{-3}$ | $-1$ | $e_{-3, -2}$ | $e_{-3, -1}$ | $-e_{-2}$ | $-e_{-1}$ | $\underline{e_{-3, -2, -1}}$ | $\underline{-e_{-2, -1}}$ |
| $e_{-2}$ | $-e_{-3, -2}$ | $-1$ | $e_{-2, -1}$ | $e_{-3}$ | $\underline{-e_{-3, -2, -1}}$ | $-e_{-1}$ | $\underline{e_{-3, -1}}$ |
| $e_{-1}$ | $-e_{-3, -1}$ | $-e_{-2, -1}$ | $-1$ | $\underline{e_{-3, -2, -1}}$ | $e_{-3}$ | $e_{-2}$ | $\underline{-e_{-3, -2}}$ |
| $e_{-3, -2}$ | $e_{-2}$ | $-e_{-3}$ | $\underline{e_{-3, -2, -1}}$ | $-1$ | $e_{-2, -1}$ | $-e_{-3, -1}$ | $\underline{-e_{-1}}$ |
| $e_{-3, -1}$ | $e_{-1}$ | $\underline{-e_{-3, -2, -1}}$ | $-e_{-3}$ | $-e_{-2, -1}$ | $-1$ | $e_{-3, -2}$ | $\underline{e_{-2}}$ |
| $e_{-2, -1}$ | $\underline{e_{-3, -2, -1}}$ | $e_{-1}$ | $-e_{-2}$ | $e_{-3, -1}$ | $-e_{-3, -2}$ | $-1$ | $\underline{-e_{-3}}$ |
| $e_{-3, -2, -1}$ | $\underline{-e_{-2, -1}}$ | $\underline{e_{-3, -1}}$ | $\underline{-e_{-3, -2}}$ | $\underline{-e_{-1}}$ | $\underline{e_{-2}}$ | $\underline{-e_{-3}}$ | $1$ |

$\mathbb{R}, \mathbb{C}, \mathbb{H}$と続くから八元数$\mathbb{O}$と予想したくなるが、クリフォード代数は結合的なので八元数ではない。$\mathbb{H}^{2}$と当たりを付けて、

$$
\begin{aligned} e_{-1}&\mapsto( i, i ), & e_{-2, -1}&\mapsto( j, j ), & e_{-2}&\mapsto( k, k ) \end{aligned}
$$

と仮定する。残りの基底$( i, -i ), ( j, -j ), ( k, -k ), ( 1, -1 )$の対応を調べればよい。まず$e_{-3, -2, -1}$は全ての基底と可換である。上記の基底でこのような性質を持つのは$( 1, -1 )$しかないので$e_{-3, -2, -1}\mapsto( 1, -1 )$である。すると$e_{-2}, e_{-1}, e_{-2, -1}$との積より、符号に注意して

$$
\begin{aligned} e_{-3, -1}&\mapsto( k, -k ), & e_{-3, -2}&\mapsto -( i, -i ), & e_{-3}&\mapsto -( j, -j ) \end{aligned}
$$

が分かる。実際に計算してみると次の表になる。

|  | $( -j, j )$ | $( k, k )$ | $( i, i )$ | $( -i, i )$ | $( k, -k )$ | $( j, j )$ | $( 1, -1 )$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $( -j, j )$ | $-1$ | $( -i, i )$ | $( k, -k )$ | $-( k, k )$ | $-( i, i )$ | $( 1, -1 )$ | $-( j, j )$ |
| $( k, k )$ | $-( i, -i )$ |  |  | $( -j, j )$ | $-( 1, -1 )$ |  | $( k, -k )$ |
| $( i, i )$ | $-( k, -k )$ |  |  | $( 1, -1 )$ | $( -j, j )$ |  | $-( -i, i )$ |
| $( -i, i )$ | $( k, k )$ | $-( -j, j )$ | $( 1, -1 )$ | $-1$ | $( j, j )$ | $-( k, -k )$ | $-( i, i )$ |
| $( k, -k )$ | $( i, i )$ | $-( 1, -1 )$ | $-( -j, j )$ | $-( j, j )$ | $-1$ | $( -i, i )$ | $( k, k )$ |
| $( j, j )$ | $( 1, -1 )$ |  |  | $( k, -k )$ | $-( -i, i )$ |  | $-( -j, j )$ |
| $( 1, -1 )$ | $-( j, j )$ | $( k, -k )$ | $-( -i, i )$ | $-( i, i )$ | $( k, k )$ | $-( -j, j )$ | $1$ |

穴の部分は$\mathrm{Clif}( \mathbb{R} )_{2, 0}$と同様なので省略した。確かに上に挙げた二つの表は一致しており、故に$\mathrm{Clif}( \mathbb{R} )_{3, 0}\cong\mathbb{H}^{2}$が分かる。

**例** $\mathrm{Clif}( \mathbb{R} )_{2, 1}$は

$$
\begin{aligned} &1, & &e_{-2}, & &e_{-1}, & &e_{0}, & &e_{-2, -1}, & &e_{-2, 0}, & &e_{-1, 0}, & &e_{-2, -1, 0} \end{aligned}
$$

を基底とするベクトル空間である。この積構造は次のようになる。

|  | $e_{-2}$ | $e_{-1}$ | $e_{0}$ | $e_{-2, -1}$ | $e_{-2, 0}$ | $e_{-1, 0}$ | $e_{-2, -1, 0}$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $e_{-2}$ | $-1$ | $e_{-2, -1}$ | $e_{-2, 0}$ | $-e_{-1}$ | $-e_{0}$ | $\underline{e_{-2, -1, 0}}$ | $\underline{-e_{-1, 0}}$ |
| $e_{-1}$ | $-e_{-2, -1}$ | $-1$ | $e_{-1, 0}$ | $e_{-2}$ | $\underline{-e_{-2, -1, 0}}$ | $-e_{0}$ | $\underline{e_{-2, 0}}$ |
| $e_{0}$ | $-e_{-2, 0}$ | $-e_{-1, 0}$ | $1$ | $\underline{e_{-2, -1, 0}}$ | $-e_{-2}$ | $-e_{-1}$ | $\underline{e_{-2, -1}}$ |
| $e_{-2, -1}$ | $e_{-1}$ | $-e_{-2}$ | $\underline{e_{-2, -1, 0}}$ | $-1$ | $e_{-1, 0}$ | $-e_{-2, 0}$ | $\underline{-e_{0}}$ |
| $e_{-2, 0}$ | $e_{0}$ | $\underline{-e_{-2, -1, 0}}$ | $e_{-2}$ | $-e_{-1, 0}$ | $1$ | $-e_{-2, -1}$ | $\underline{-e_{-1}}$ |
| $e_{-1, 0}$ | $\underline{e_{-2, -1, 0}}$ | $e_{0}$ | $e_{-1}$ | $e_{-2, 0}$ | $e_{-2, -1}$ | $1$ | $\underline{e_{-2}}$ |
| $e_{-2, -1, 0}$ | $\underline{-e_{-1, 0}}$ | $\underline{e_{-2, 0}}$ | $\underline{e_{-2, -1}}$ | $\underline{-e_{-1}}$ | $\underline{-e_{-1}}$ | $\underline{e_{-2}}$ | $-1$ |

今度は$1, e_{-1}$が生成する部分代数$\mathrm{Clif}( \mathbb{R} )_{1, 0}\cong\mathbb{C}$に$e_{-2}, e_{0}$を添加したものと考えられる。従って$\mathbb{C}( 2 )$と予想できる。そこで虚数単位$h$をとり、基底として

$$
\left( \begin{matrix} 1 & \\ & 1 \end{matrix} \right), \left( \begin{matrix} 1 & \\ & -1 \end{matrix} \right), \left( \begin{matrix} & 1 \\ 1 & \end{matrix} \right), \left( \begin{matrix} & 1 \\ -1 & \end{matrix} \right), \left( \begin{matrix} h & \\ & h \end{matrix} \right), \left( \begin{matrix} h & \\ & -h \end{matrix} \right), \left( \begin{matrix} & h \\ h & \end{matrix} \right), \left( \begin{matrix} & h \\ -h & \end{matrix} \right)
$$

をとる。それぞれ$1, A, B, C, D, E, F, G$とおいて計算すると

|  | $A$ | $B$ | $C$ | $D$ | $E$ | $F$ | $G$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $A$ | $1$ | $C$ | $B$ | $E$ | $D$ | $G$ | $F$ |
| $B$ | $-C$ | $1$ | $-A$ | $F$ | $-G$ | $D$ | $-E$ |
| $C$ | $-B$ | $A$ | $-1$ | $G$ | $-F$ | $E$ | $-D$ |
| $D$ | $E$ | $F$ | $G$ | $-1$ | $-A$ | $-B$ | $-C$ |
| $E$ | $D$ | $G$ | $F$ | $-A$ | $-1$ | $-C$ | $-B$ |
| $F$ | $-G$ | $D$ | $-E$ | $-B$ | $C$ | $-1$ | $A$ |
| $G$ | $-F$ | $E$ | $-D$ | $-C$ | $B$ | $-A$ | $1$ |

となる。まず可換性より$e_{-2, -1, 0}\mapsto G$が分かる。全ての符号が正で揃っているので、$e_{-1, 0}\mapsto A$と仮定しよう。$e_{-1, 0}e_{-2}=e_{-2, -1, 0}$より$AX=D$を解いて$X=E$を得る。従って$e_{-2}\mapsto E$とする。$e_{-2, -1, 0}$との積でマイナスの符号が付くのは$e_{-2}, e_{-2, -1}, e_{-2, 0}, e_{-2, -1, 0}$であり、$D$との積でマイナスの符号が付くのは$E, F, G, D$である。よって$F, G$は$e_{-2, -1}, e_{-2, 0}$のいずれかである。対角成分を見ると$e_{-2, -1}\mapsto F, e_{-2, 0}\mapsto G$でなければならない。同様に$e_{-1}\mapsto C, e_{0}\mapsto B$が分かる。この対応が正しいことは、ちゃんと計算してみれば分かる。

| $e_{-2}$ | $e_{-1}$ | $e_{0}$ | $e_{-2, -1}$ | $e_{-2, 0}$ | $e_{-1, 0}$ | $e_{-2, -1, 0}$ |
|:-:|:-:|:-:|:-:|:-:|:-:|:-:|:-:|
| $\left( \begin{matrix} h & \\ & -h \end{matrix} \right)$ | $\left( \begin{matrix} & 1 \\ -1 & \end{matrix} \right)$ | $\left( \begin{matrix} & 1 \\ 1 & \end{matrix} \right)$ | $\left( \begin{matrix} & h \\ h & \end{matrix} \right)$ | $\left( \begin{matrix} & h \\ -h & \end{matrix} \right)$ | $\left( \begin{matrix} & 1 \\ -1 & \end{matrix} \right)$ | $\left( \begin{matrix} h & \\ & h \end{matrix} \right)$ |

従って$\mathrm{Clif}( \mathbb{R} )_{2, 1}\cong\mathbb{C}( 2 )$が成り立つ。

TODO

良く知られた符号$( -, -, -, + )$のミンコフスキー空間は$\mathrm{Clif}( \mathbb{R} )_{3, 1}$に埋め込まれる。（空間成分の符号が負、時間成分の符号が正）



## 補足

天下りではない、もっと見通しの良い計算があると思うのだが、よく分からない。
