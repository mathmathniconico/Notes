
# 余代数のイデアルと剰余余代数

## 剰余余代数

$R$を可換環、$( C, \Delta, \varepsilon )$を余代数とする。$C$は$R$加群なので、部分加群$N\subset C$に対して剰余加群$C/N$を考えることができる。

$C/N$はいつ自然な余代数の構造を持つだろうか。

まず双線型写像$C\times C\rightarrow C/N\otimes C/N$から、テンソル積の普遍性より線型写像

$$
\pi\colon C\otimes C\rightarrow C/N\otimes C/N
$$

が誘導される。よって$\pi\circ\Delta\colon C\rightarrow C/N\otimes C/N$の商が取れればよい。つまり

$$
N\subset\mathrm{Ker}( \pi\circ\Delta )\Longleftrightarrow\Delta( N )\subset\mathrm{Ker}( \pi )
$$

が成り立てばよく、このとき商写像$\overline{\Delta}\colon C/N\rightarrow C/N\otimes C/N$が定義される。また$\overline{\varepsilon}\colon C/N\rightarrow R$を自然に定義するには$\varepsilon( N )=0$でなければならない。

纏めよう。部分加群$N\subset C$が以下の二条件を満たすとき**イデアル**と言う。

- $\Delta( N )\subset\mathrm{Ker}( \pi )$
- $\varepsilon( N )=0$

**命題** $( C, \Delta, \varepsilon )$を余代数、$N\subset C$をイデアルとする。このとき$( C/N, \overline{\Delta}, \overline{\varepsilon} )$は余代数である。

（証明）$x\in N$について$\Delta( x )=\sum_{i=1}^{n}a_{i}\otimes b_{i}$とする。また

$$
\begin{aligned} \Delta( a_{i} )&=\sum_{j_{i}=1}^{m_{i}}u_{j_{i}}\otimes v_{j_{i}}, & \Delta( b_{i} )&=\sum_{k_{i}=1}^{l_{i}}p_{k_{i}}\otimes q_{k_{i}} \end{aligned}
$$

とする。余代数の定義より

$$
\begin{aligned} \mathrm{id}\otimes\Delta( \Delta( x ) ) &= \sum_{i=1}^{n}a_{i}\otimes\sum_{j_{i}=1}^{m_{i}}u_{j_{i}}\otimes v_{j_{i}}=\sum_{i=1}^{n}\sum_{j_{i}=1}^{m_{i}}a_{i}\otimes u_{j_{i}}\otimes v_{j_{i}} \\ &= \Delta\otimes\mathrm{id}( \Delta( x ) )=\sum_{i=1}^{n}\sum_{k_{i}=1}^{l_{i}}p_{k_{i}}\otimes q_{k_{i}}\otimes b_{i} \end{aligned}
$$

が成り立つ。従って$C\times C\times C\rightarrow C/N\otimes C/N\otimes C/N$を考えれば

$$
\sum_{i=1}^{n}\sum_{j_{i}=1}^{m_{i}}\overline{a_{i}}\otimes\overline{u_{j_{i}}}\otimes\overline{v_{j_{i}}}=\sum_{i=1}^{n}\sum_{k_{i}=1}^{l_{i}}\overline{p_{k_{i}}}\otimes\overline{q_{k_{i}}}\otimes\overline{b_{i}}
$$

より$\mathrm{id}\otimes\overline{\Delta}\circ\overline{\Delta}( \overline{x} )=\overline{\Delta}\otimes\mathrm{id}\circ\overline{\Delta}( \overline{x} )$が成り立つ。

$\overline{\varepsilon}$についても同様である。実際

$$
\mathrm{id}\otimes\varepsilon\circ\Delta( x )=\sum_{i=1}^{n}a_{i}\otimes\varepsilon( b_{i} )=x\otimes 1
$$

より、$C\times R\rightarrow C/N\otimes R$を考えれば

$$
\mathrm{id}\otimes\overline{\varepsilon}\circ\overline{\Delta}( \overline{x} )=\sum_{i=1}^{n}\overline{a_{i}}\otimes\overline{\varepsilon}( \overline{b_{i}} )=\sum_{i=1}^{n}\overline{a_{i}}\otimes\varepsilon( b_{i} )=\overline{x}\otimes 1
$$

を得る。もう一方も同様である。$\square$

上記の余代数$( C/N, \overline{\Delta}, \overline{\varepsilon} )$を**剰余余代数**（quotient coalgebra）と呼ぶ。



## 補足

他の本だとイデアルの条件は$\Delta( N )\subset C\otimes N+N\otimes C$となっていることがあるが、ややミスリードがある。というのも一般的な状況ではあるが、反例に近い例がある。

可換環$R$上の加群$M, N$の部分加群$M^{\prime}, N^{\prime}$について

$$
\pi\colon M\otimes N\rightarrow M/M^{\prime}\otimes N/N^{\prime}
$$

の核を考えたい。実は$R=k$が体であるなら

$$
\mathrm{Ker}( \pi )=M^{\prime}\otimes N+M\otimes N^{\prime}
$$

が成り立つ。しかし$R$が体でないときは、そもそも$M^{\prime}\otimes N$や$M\otimes N^{\prime}$は、$M\otimes N$に含まれるとは限らない。

例えば$R=\mathbb{Z}, M=\mathbb{Z}, N=\mathbb{Z}/2\mathbb{Z}$とする。更に$M^{\prime}=2\mathbb{Z}, N^{\prime}=0$とする。

- $M\otimes N=\mathbb{Z}\otimes( \mathbb{Z}/2\mathbb{Z} )$の元は$n\otimes 1$の線型和となるが、$3\otimes 1=1\otimes 1+2\otimes 1=1\otimes 1$のように計算ができる。従ってゼロでない元は$1\otimes 1$しかない。
- $M^{\prime}\otimes N=2\mathbb{Z}\otimes( \mathbb{Z}/2\mathbb{Z} )$の元は同様に$2\otimes 1$しかない。
- $M\otimes N^{\prime}=0$である。

このように、そもそも部分加群でない場合がある。

何が問題であったかというと、包含$M^{\prime}\rightarrow M$から誘導される$\alpha\colon M^{\prime}\otimes N\rightarrow M\otimes N$が単射とは限らないことにある。$R=k$が体の場合は平坦性より単射になる。あるいはベクトル空間の場合は基底が取れるので、テンソル積が、元の基底のテンソルを基底とするベクトル空間であることからも従う。$N^{\prime}\rightarrow N$から誘導される$\beta\colon M\otimes N^{\prime}\rightarrow M\otimes N$についても同様なことが言える。

一般の$R$に戻ると、$\mathrm{Im}( \alpha )+\mathrm{Im}( \beta )\subset\mathrm{Ker}( \pi )$は明白だが、実は逆の包含も次のように示される。まず双線型写像

$$
M/M^{\prime}\times N/N^{\prime}\rightarrow M\otimes N/( \mathrm{Im}( \alpha )+\mathrm{Im}( \beta ) )
$$

はwell-definedである。実際$x\in M, y\in N$及び$m\in M^{\prime}, n\in N^{\prime}$について

$$
( x+m )\otimes( y+n )=x\otimes y+x\otimes n+m\otimes y+m\otimes n
$$

より$\overline{x+m}\otimes\overline{y+n}=\overline{x}\otimes\overline{y}$を得る。従ってテンソル積の普遍性より

$$
M/M^{\prime}\otimes N/N^{\prime}\xrightarrow{f} M\otimes N/( \mathrm{Im}( \alpha )+\mathrm{Im}( \beta ) )\xrightarrow{g} M\otimes N/\mathrm{Ker}( \pi )\xrightarrow{\cong}M/M^{\prime}\otimes N/N^{\prime}
$$

を得る。生成元の対応を見ると$\overline{x}\otimes\overline{y}\mapsto\overline{x}\otimes\overline{y}$なので恒等写像である。故に上の$f$は単射である。また$f$の全射性も$M\otimes N$の生成元を見れば明らかなので$f$は同型となる。よって$g$も同型となり、結局

$$
\mathrm{Im}( \alpha )+\mathrm{Im}( \beta )=\mathrm{Ker}( \pi )
$$

であることが分かる。

先の例では$2\mathbb{Z}\otimes( \mathbb{Z}/2\mathbb{Z} )\rightarrow\mathbb{Z}\otimes( \mathbb{Z}/2\mathbb{Z} )$は恒等的にゼロだから、$\mathrm{Im}( \alpha )=0$となる。また$N^{\prime}=0$より$\mathrm{Im}( \beta )=0$である。ところで

$$
M\otimes N=\mathbb{Z}\otimes( \mathbb{Z}/2\mathbb{Z} )=\lbrace 0, 1\otimes 1 \rbrace=( \mathbb{Z}/2\mathbb{Z} )\otimes( \mathbb{Z}/2\mathbb{Z} )=M/M^{\prime}\otimes N/N^{\prime}
$$

より、確かに$\mathrm{Ker}( \pi )=\mathrm{Im}( \alpha )+\mathrm{Im}( \beta )$である。

**注意** イデアルの条件は

- $\Delta( N )\subset\overline{N\otimes C}+\overline{C\otimes N}$
- $\varepsilon( N )=0$

としてよい。ただし

$$
\begin{aligned} \overline{N\otimes C}&:=\mathrm{Im}( \alpha ), & \overline{C\otimes N}&:=\mathrm{Im}( \beta ) \end{aligned}
$$

は先に述べた$\alpha, \beta$より定まるものとする。