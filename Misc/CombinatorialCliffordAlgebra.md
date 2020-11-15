
# 組合せ論的クリフォード代数

クリフォード代数（Clifford Algebra）あるいはヘステネス（Hestenes）の幾何代数（Geometric Algebra）は通常、二次形式を伴うベクトル空間の普遍性で定義され、具体的にはテンソル代数の商代数として構成される。しかしArthanは半順序集合の集合演算によるcombinatorialな構成法を提案した。本稿ではこれに従い、やや一般的な枠組みで組合せ論的クリフォード代数を定義する。

## 組合せ論的クリフォード代数

$X$を集合、$R$は単位的可換環とする。**符号**と呼ばれる任意の写像$r\colon X\rightarrow R$をとる。$X$の有限部分集合全体を$\mathbb{F}$とする。各$I\in\mathbb{F}$について記号$e_{I}$を用意する。このとき自由$R$加群

$$
\mathrm{Clif}( X, R, r ):=\bigoplus_{I\in\mathbb{F}}Re_{I}
$$

に代数構造を定めたい。$e_{\emptyset}$の係数をスカラーと呼ぶ。

クリフォード代数の特徴は自乗するとスカラーであることなので、各基底$e_{I}$同士の積は

$$
e_{I}e_{J}:=\sigma( I, J )e_{I\triangle J}
$$

によって定められるべきだろう。積は$R$双線型かつ結合的なので

$$
\begin{aligned} ( e_{I}e_{J} )e_{K}=\sigma( I, J )e_{I\triangle J}e_{K}=\sigma( I, J )\sigma( I\triangle J, K )e_{( I\triangle J )\triangle K}, \\ e_{I}( e_{J}e_{K} )=e_{I}\sigma( J, K )e_{J\triangle K}=\sigma( I, J\triangle K )\sigma( J, K )e_{I\triangle( J\triangle K )} \end{aligned}
$$

が成り立つ。対称差は結合的だから、結局

$$
\sigma( I, J )\sigma( I\triangle J, K )=\sigma( I, J\triangle K )\sigma( J, K )
$$

が成り立てばよい。逆にこのような$\sigma\colon\mathbb{F}\times\mathbb{F}\rightarrow R$が与えられれば、

$$
\left( \sum\lambda_{I}e_{I} \right)\left( \sum\mu_{J}e_{J} \right):=\sum\lambda_{I}\mu_{J}\sigma( I, J )e_{I\triangle J}
$$

によって$\mathrm{Clif}( X, R, r )$は結合代数となる。

以下$F\in\mathbb{F}$について

$$
r( F )=\left\lbrace\begin{aligned} &\prod_{x\in F}r( x ) & &\text{if } F\neq\emptyset \\ &1 & &\text{if }F=\emptyset \end{aligned}\right.
$$

と置く。



### Arthanの構成法

$( X, \le )$を半順序集合とする。$I, J\in\mathbb{F}$に対し、

$$
\tau( I, J ):=\vert \lbrace ( i, j ) \in I\times J : i\gt j \rbrace \vert
$$

と置く。このとき$\mod{2}$で

$$
\begin{aligned} \tau( I\triangle J, K ) &= \tau( I, K )+\tau( J, K )-2\tau( I\cap J, K ) \\ &\equiv \tau( I, K )+\tau( J, K ) \end{aligned}
$$

であり、同様に

$$
\tau( I, J\triangle K )\equiv\tau( I, J )+\tau( I, K )
$$

が成り立つ。よって

$$
\begin{aligned} \tau( I, J )+\tau( I\triangle J, K ) &\equiv \tau( I, J )+\tau( I, K )+\tau( J, K ) \\ &\equiv\tau( I, J\triangle K )+\tau( J, K ) \end{aligned}
$$

が成り立つ。そこで

$$
\sigma( I, J ):=r( I\cap J )( -1 )^{\tau( I, J )}
$$

と定めれば、

$$
\sigma( I, J )\sigma( I\triangle K, K )=\sigma( I, J\triangle K )\sigma( J, K )
$$

が成り立つ。実際$\prod r( x )$の部分は

$$
( I\cap J )\sqcup( ( I\triangle J )\cap K )=( I\cap ( J\triangle K ) )\sqcup( J\cap K )
$$

より左右で等しい。

略記として$e_{\emptyset}:=1, e_{\lbrace x \rbrace}=e_{x}$と表すのが便利である。

こうして半順序集合の**クリフォード代数**$\mathrm{Clif}( X, R, r )$が構成される。



## クリフォード代数の対称性

$\mathrm{Clif}( X, R, r )$をクリフォード代数とする。以下は簡単に示すことが出来る。

- $e_{x}^{2}=e_{x}e_{x}=r( x )$である。
- $x, y\in X$が比較可能なら$e_{x}e_{y}=-e_{y}e_{x}$である。
- $x, y\in X$が比較不可能なら$e_{x}e_{y}=e_{y}e_{x}$である。

**補題** $I, J\in\mathbb{F}$について

$$
\tau( J, I )\equiv\tau( I, I )+\tau( J, J )+\tau( I\triangle J, I\triangle J )+\tau( I, J )
$$

が成り立つ。

（証明）$\tau$の関係式

$$
\tau( I, J )+\tau( I\triangle J, K )\equiv\tau( I, J\triangle K )+\tau( J, K )
$$

を思い出そう。$K\mapsto I$として

$$
\tau( I, J )+\tau( I\triangle J, J )\equiv\tau( I, I\triangle J )+\tau( J, I )\quad( \heartsuit )
$$

が成り立つ。$K\mapsto J$として

$$
\tau( I, J )+\tau( I\triangle J, J )\equiv\tau( J, J )
$$

だが、$I$と$J$を交換すると

$$
\tau( J, I )+\tau( I\triangle J, I )\equiv\tau( I, I )\quad( \diamondsuit )
$$

が成り立つ。$K\mapsto I\triangle J$として

$$
\tau( I, J )+\tau( I\triangle J, I\triangle J )\equiv\tau( I, I )+\tau( J, I\triangle J )
$$

だが、やはり$I$と$J$を交換すると

$$
\tau( J, I )+\tau( I\triangle J, I\triangle J )\equiv\tau( J, J )+\tau( I, I\triangle J )\quad( \spadesuit )
$$

が成り立つ。

$( \heartsuit ), ( \diamondsuit ), ( \spadesuit )$を辺々足し合わせると

$$
\tau( I, J )+\tau( I\triangle J, I\triangle J )\equiv\tau( I, I )+\tau( J, J )+\tau( J, I )
$$

を得る。ここで$a\equiv -a$に注意すれば求める式を得る。$\square$

補題より交換の式が分かる。

**系** $I, J\in\mathbb{F}$について

$$
e_{J}e_{I}=( -1 )^{\tau( I, I )+\tau( J, J )+\tau( I\triangle J, I\triangle J )}e_{I}e_{J}
$$

が成り立つ。

**定義** クリフォード代数上の三種類の対称性を次を線型に拡張して定める。

- $e_{I}^{\mathrm{inv}}:=( -1 )^{\vert I \vert}e_{I}$をinvolutionという。
- $e_{I}^{\mathrm{rev}}:=( -1 )^{\tau( I, I )}e_{I}$をreversionという。
- $e_{I}^{\mathrm{conj}}:=( e_{I}^{\mathrm{inv}} )^{\mathrm{rev}}=( e_{I}^{\mathrm{rev}} )^{\mathrm{inv}}$をconjugationと呼ぶ。

なおinvolutionとreversionは$( -1 )$を何回か書けるだけなので可換になる。

覚えにくいが、inversionは「基底の向きを変える」演算であり、reversionは「積の順序を変える」演算である。これを端的に表したのが次の命題である。

**命題** $I, J\in\mathbb{F}, x\in X$について以下が成り立つ。

- $( e_{I}e_{J} )^{\mathrm{inv}}=e_{I}^{\mathrm{inv}}e_{J}^{\mathrm{inv}}$が成り立つ。特に$e_{x}^{\mathrm{inv}}=-e_{x}$である。
- $( e_{I}e_{J} )^{\mathrm{rev}}=e_{J}^{\mathrm{rev}}e_{I}^{\mathrm{rev}}$が成り立つ。特に$e_{x}^{\mathrm{rev}}=e_{x}$である。

つまり$A, B\in\mathrm{Clif}( X, R, r )$について

$$
\begin{aligned} ( AB )^{\mathrm{inv}}&=A^{\mathrm{inv}}B^{\mathrm{inv}}, & ( AB )^{\mathrm{rev}}&=B^{\mathrm{rev}}A^{\mathrm{rev}} \end{aligned}
$$

が成り立つ。

（証明）involutionについては

$$
\begin{aligned} ( e_{I}e_{J} )^{\mathrm{inv}} &= ( \sigma( I, J )e_{I\triangle J} )^{\mathrm{inv}}=( -1 )^{\vert I\triangle J \vert}\sigma( I, J )e_{I\triangle J} \\ &= ( -1 )^{\vert I \vert+\vert J \vert-2\vert I\cap J\vert}e_{I}e_{J} \\ &= ( -1 )^{\vert I \vert}e_{I}( -1 )^{\vert J \vert}e_{J} \\ &= e_{I}^{\mathrm{inv}}e_{J}^{\mathrm{inv}} \end{aligned}
$$

より分かる。また定義より$e_{x}^{\mathrm{inv}}=( -1 )e_{x}=-e_{x}$である。

reversionについては交換の式を示したので

$$
\begin{aligned} ( e_{I}e_{J} )^{\mathrm{rev}} &= ( \sigma( I, J )e_{I\triangle J} )^{\mathrm{rev}}=( -1 )^{\tau( I\triangle J, I\triangle J )}e_{I}e_{J} \\ &= ( -1 )^{\tau( I\triangle J, I\triangle J )}( -1 )^{\tau( I, I )+\tau( J, J )+\tau( I\triangle J, I\triangle J )}e_{J}e_{I} \\ &=( -1 )^{\tau( J, J )}e_{J}( -1 )^{\tau( I, I )}e_{I} \\ &=e_{J}^{\mathrm{rev}}e_{I}^{\mathrm{rev}} \end{aligned}
$$

より分かる。また定義より$e_{x}^{\mathrm{rev}}=( -1 )^{0}e_{x}=e_{x}$である。$\square$




## 参考文献

    R.D.Arthan. A Minimalist Construction of the Geometric Algebra. arXiv:math/0607190v2 [math.RA] 9 Jul 2006.