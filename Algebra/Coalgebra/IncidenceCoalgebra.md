
# Incidence Colgebra

## Incidence Coalgebra

小さい圏とは、以下の4つのデータからなる。

- objectの集合$C_{0}$
- morphismの集合$C_{1}$
- 写像$s, t\colon C_{1}\rightarrow C_{0}$及びそのfiber積における合成写像$\circ\colon C_{1}\times_{C_{0}}C_{1}\rightarrow C_{1}$
- 各objectに対する恒等写像$1\colon C_{0}\rightarrow C_{1}$

ここで合成写像は$C_{1}\times_{C_{0}}C_{1}=\lbrace ( g, f ) : s( g )=t( f ) \rbrace$の元$( g, f )$に対して$g\circ f$を対応させる。つまり$s$は定義域を対応させ、$t$は値域を対応させる。以下$x\in C_{0}$について$1( x )$のことを$1_{x}$と表記する。

またこれらのデータは以下の関係を持つ。ただし$f, g, h\in C_{1}, x, y\in C_{0}$は適切なものを考える。

- $s( g\circ f )=s( f ), t( g\circ f )=t( g )$
- $s( 1_{x} )=x, t( 1_{x} )=x$
- $( h\circ g )\circ f=h\circ( g\circ f )$
- $1_{y}\circ f=f=f\circ 1_{x}$

このとき上記の組を**小さい圏**（small category）と呼ぶ。

可換環$R$について、morphismを基底とする$R$上の自由加群$C$を考える。ここに写像$\Delta\colon C\rightarrow C\otimes C$及び$\varepsilon\colon C\rightarrow R$を、$f\in C_{1}$に対して線型に以下で定める。

$$
\begin{aligned} \Delta( f )&:=\sum_{h\circ g=f}g\otimes h, & \varepsilon( f )&:=\left\lbrace\begin{aligned} &1 & &\text{if }f=1_{x} \\ &0 & &\text{otherwise} \end{aligned}\right. \end{aligned}
$$

ここで$\Delta$がwell-definedであるためには、任意の$f$で$h\circ g=f$なる$( h, g )$は有限個でなければならない。小さい圏がこの条件を満たすとき、**局所有限**（locally finite）と言う。

**命題**
局所有限な小さい圏において、上記の$( C, \Delta, \varepsilon )$は余代数となる。

（証明）余代数の定義を検証すればよい。$\mathrm{id}\otimes\Delta\circ\Delta=\Delta\otimes\mathrm{id}\circ\Delta$は次のように示される。

$$
\mathrm{id}\otimes\Delta\circ\Delta( f )=\mathrm{id}\otimes\Delta\left( \sum_{h\circ g=f}g\otimes h \right)=\sum_{h\circ g=f}g\otimes\left( \sum_{v\circ u=h} u\otimes v \right)=\sum_{v\circ u\circ g=f}g\otimes u\otimes v
$$

より、右辺は$v\circ u\circ g=f$なる三つ組$( v, u, g )$に関する和である。$\Delta\otimes\mathrm{id}\circ\Delta$も同様なので等しい。

また$\mathrm{id}\otimes\varepsilon\circ\Delta( f )=f\otimes 1$は以下のように示される。$1_{x}\circ g=f$なら$g=1_{x}\circ g=f$より$x=t( f )$であるから、

$$
\mathrm{id}\otimes\varepsilon\circ\Delta( f )=\mathrm{id}\otimes\varepsilon\left( \sum_{h\circ g=f}g\otimes h \right)=\sum_{h\circ g=f}g\otimes\varepsilon( h )=f\otimes\varepsilon( 1_{t( f )} )=f\otimes 1
$$

が従う。$\varepsilon\circ\mathrm{id}\circ\Delta( f )=1\otimes f$も同様である。$\square$

上記の余代数$( C, \Delta, \varepsilon )$を**incidence coalgebra**と呼ぶ。隣接余代数という翻訳もあるが、馴染みが薄いので英語で表記する。



## Incidence Algebra

一般に余代数と代数のpairingを考えることでconvolution代数を定義できるが、特に代数として$R$自身をとることで、余代数$C$の双対代数（dual algebra of coalgebra）を考えることができる。つまり$\mathrm{Hom}_{R}( C, R )=:C^{\mathrm{dual}}$が次のconvolution積で代数となる。$\phi, \psi\in C^{\mathrm{dual}}$のconvolution積は、$f\in C_{1}$に対して線型に

$$
( \phi\ast\psi )( f ):=\sum_{h\circ g=f}\phi( g )\psi( h )
$$

で定義される。単位元は$\varepsilon$である。特にincidence coalgebraの双対代数を**incidence algebra**と呼ぶ。

例えば任意の$f\in C_{1}$について$\mathfrak{z}( f )=1$となる写像がある。（基底に対して$1$を取るだけで、恒等的に$1$というわけではない。）



## Incidence Coalgebraの剰余余代数について

Incidence coalgebraの剰余余代数に、上記の議論を拡張する。$( C, \Delta, \varepsilon )$を余代数、$N\subset C$をイデアルとする。$R$加群の系列

$$
0\rightarrow N\rightarrow C\rightarrow C/N\rightarrow 0
$$

は完全なので、双対を取ると

$$
( 0\leftarrow )N^{\mathrm{dual}}\leftarrow C^{\mathrm{dual}}\leftarrow ( C/N )^{\mathrm{dual}}\leftarrow 0
$$

は完全になる。特に$( C/N )^{\mathrm{dual}}$は$C^{\mathrm{dual}}$に自然に埋め込める。よって$\phi$が$N$上で恒等的にゼロ（$\phi\in\mathrm{Ker}( C^{\mathrm{dual}}\rightarrow N^{\mathrm{dual}}$）なら、$\phi$は$( C/N )^{\mathrm{dual}}$の元（$\phi\in\mathrm{Im}( ( C/N )^{\mathrm{dual}}\rightarrow C^{\mathrm{dual}}$）とみなせる。


## 補足

Khripchenko, Novikovは上記のアナロジーでfinitary incidence algebraを導入している。こちらは$C$に局所有限性を仮定せず、代わりに$C^{\mathrm{dual}}$にpath finiteness（これは私の造語）を仮定する。つまり$s( f ), t( f )$を結ぶpathに含まれる射$g$について$\phi( g )\neq 0$となるものが有限個であるとする。（論文ではposetに対して論じているのでこの翻訳が正しいかは要検証。）局所有限性が無いので$C$そのものは余代数の構造を持たないが、$C^{\mathrm{dual}}$の方は代数構造を持つという主張だ。

一般に代数$A$に対してその双対余代数$A^{\mathrm{dual}}$を定義できる場合がある。しかし恐らくfinaitary incidence algebraに対して定義できる場合は、それがincidence algebraである必要があると思われる。そしてその双対余代数は、元々の余代数と同型であるだろう。