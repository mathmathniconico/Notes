
# 環

群は数学的オブジェクトの対称性を表すとされるが、環は幾何学的オブジェクトである。ある環から出る環の準同型は一種の幾何学的表出であり、それらを束ねることで元の環の幾何学的情報を得ることができるとされる。これによってどの程度元の環を復元できるかは興味のあるところだろう。

環についても群と同様に部分代数と合同関係という二つの概念を考えることができる。部分代数には部分環が対応し、合同関係にはイデアルが対応する。




## 環と部分環

__定義__ $(R, +, 0)$をアーベル群とする。演算$\cdot\colon R\times R\rightarrow R$は以下を満たすとする。

- $a, b, c\in R$について$(a\cdot b)\cdot c=a\cdot(b\cdot c)$が成り立つ。（結合律）
- $a, b, c\in R$について$a\cdot(b+c)=a\cdot b+a\cdot c$及び$(a+b)\cdot c=a\cdot c+b\cdot c$が成り立つ。（$+$に関する両側分配性）

このとき集合の組$(R, +, \cdot, 0)$を **環** （ring）と呼ぶ。

環$R$と書くときは上記の組が想定されているものとする。$+$を加法、$\cdot$を乗法と呼ぶ。$a\in R$の加法逆元を$-a$と表し、乗法$a\cdot b$は$ab$と略記する。数の$0$と区別するために$0_{R}$という記号も用いるが、本文ではゼロと呼ぶ。

- $a\in R$について$a0=0a=0$が成り立つ。
- $a, b\in R$について$(-a)b=a(-b)=-(ab)$が成り立つ。特に$(-a)(-b)=ab$である。

__定義__ $R$を環とする。

- 乗法単位元が存在するとき、$R$は **単位的** （unitary）という。乗法単位元は一意的であり$1_{R}$と表す。本文ではイチと呼ぶ。
- ゼロとイチが等しいとき$R=\lbrace 0 \rbrace$となるが、これを **ゼロ環** と呼ぶ。
- $Z(R)=\lbrace z\in R : \forall a\in R, az=za \rbrace$を$R$の **中心** （center）と呼ぶ。
- $Z(R)=R$のとき **可換** （commutative）という。そうでないとき **非可換** （non-commutative）という。

__定義__ $R$を環とする。$S\subset R$が$R$の演算によって環になるとき **部分環** （subring）という。このとき$S\lt R$と表す。

> 環$R$が単位的であっても、その部分環$S\lt R$が単位的とは限らない。例えば$2\mathbb{Z}\lt\mathbb{Z}$は部分環だが、$1\notin 2\mathbb{Z}$である。また部分環が単位的であっても、群の場合と異なりイチが一致するとは限らない。

- 中心$Z(R)$は$R$の部分環である。




## 合同関係とイデアル

__定義__ $R$を環、$S\subset R$とする。このとき関係$a\theta_{S}b$を$b-a\in S$で定める。

> この定義はアーベル群$(R, +, 0)$に関する$\theta_{S}$と同等である。従って部分群の場合と比較すると、部分環$S\lt R$に対しては$\theta_{S}$が同値関係となることが分かる。一方で同値関係$\theta_{S}$からは$S$が加法に関して部分群であることは言えるものの、一般に$S$が部分環とは限らない。

__定義__ $R$を環、$\theta$を$R$上の同値関係とする。以下が成り立つとき$\theta$を **合同関係** （congruence relation）と呼び、全体を$\mathrm{Con}(R)$と表す。

- $a\theta b$なら$(-a)\theta(-b)$である。
- $a\theta a^{\prime}, b\theta b^{\prime}$なら$(a+b)\theta(a^{\prime}+b^{\prime})$である。
- $a\theta a^{\prime}, b\theta b^{\prime}$なら$(ab)\theta(a^{\prime}b^{\prime})$である。

__定義__ $R$を環、$I\subset R$は空でないとする。$I$が以下の条件を満たすとき **イデアル** （ideal）と呼ぶ。

- $a, b\in I$に対し$b-a\in I$が成り立つ。
- $r\in R$及び$a\in I$に対し$ra\in I$及び$ar\in I$が成り立つ。

$R$でないイデアルを **真イデアル** （proper ideal）と呼ぶ。

__補題__ $R$を環、$I\subset R$とする。TFAE

1. $I$はイデアルである。
1. $\theta_{I}$は合同関係である。

（証明）$I$をイデアルとする。$I$は空でなく、加法はアーベル群だから$\theta_{I}$は加法に関する合同関係となる。よって乗法に関する条件を示せばよい。$a\theta_{I}b, c\theta_{I}d$とする。$b-a\in I, d-c\in I$だからイデアルの条件より$(b-a)c, b(d-c)\in I$である。よって

$$
bd-ac=b(d-c)+(b-a)c\in I
$$

となり$ac\theta_{I}bd$を得る。

$\theta_{I}$を合同関係とする。$\theta_{I}$は加法に関する合同関係でもあるから$I$は空でなく、$a, b\in I$に対して$b-a\in I$が成り立つ。$r\in R, a\in I$とすると、$a\in I$より$0\theta_{I}a$である。また$r\theta_{I}r$だから、$0\theta_{I}ra$及び$0\theta_{I}ar$を得る。故に$ra, ar\in I$である。$\square$




## 剰余環と準同型定理

$R$を環、$\theta\in\mathrm{Con}(R)$を合同関係とする。群の場合と同様に$a\in R$の同値類$a/\theta$を考えると、その全体$R/\theta$は

$$
\begin{aligned}
(a/\theta)+_{\theta}(b/\theta) &:=(a+b)/\theta \\
(a/\theta)\cdot_{\theta}(b/\theta) &:=ab/\theta \\
\end{aligned}
$$

によって環となる。群の場合と同様にゼロは$0/\theta$で$a/\theta$の加法逆元は$(-a)/\theta$である。特に$R$が単位的のとき$1/\theta$が$R/\theta$の乗法単位元となる。

__定理__ $R$を環とする。以下が成り立つ。

- $I\subset R$をイデアルとする。$\theta_{I}$は$R$上の合同関係であり$I=0/\theta_{I}$が成り立つ。
- $\theta\in\mathrm{Con}(G)$を合同関係とする。$I:=0/\theta$は$R$のイデアルであり、$\theta=\theta_{I}$が成り立つ。

（証明）$I$をイデアルとする。補題より$\theta_{I}$は合同関係である。$I=0/\theta_{I}$は明らか。

$\theta$を合同関係とする。群の場合の結果から、$I$は加法に関して部分群であり$\theta=\theta_{I}$が成り立つ。補題より$I$はイデアルである。$\square$

以上より合同関係とイデアルの間に一対一の対応が成り立つ。この意味で$R/\theta_{I}$のことを$R/I$と表す。また$a/\theta=a+I$であるから、こちらの表記も用いる。

> 群の場合と同様に包含を保つ束としての同型を与えている。対角集合$\Delta=\lbrace (a, a) : a\in R \rbrace$について$0/\Delta=\lbrace 0 \rbrace$であり、全体集合$\nabla=\lbrace (a, b) : a, b\in R \rbrace$について$0/\nabla=R$となる。

__定義__ $I\subset R$をイデアルとする。上記の環$R/I$を$R$の$I$による **剰余環** （residue class ring）という。

__定理__ （イデアル対応定理）$I\subset R$をイデアルとする。このとき$I$を含む$R$のイデアルと$R/I$のイデアルは一対一に対応する。

（証明）$J\subset R$に対し$\Phi(J):=\lbrace a+I : a\in J \rbrace$とする。また$K\subset R/I$に対し$\Psi(K):=\lbrace a\in R : a+I\in K \rbrace$とする。$J, K$がイデアルなら$\Phi(J), \Psi(K)$もイデアルであり、更に$\Psi(\Phi(J))=J$かつ$\Phi(\Psi(K))=K$が成り立つ。$\square$

> 剰余環$R/I$の構造は$I$より大きい部分の構造を完全に記述する。素朴だがこの対応関係は非常に興味深い。更にこの対応は包含関係を保つ。即ち$J_{1}\subset J_{2}$なら$\Phi(J_{1})\subset\Phi(J_{2})$であり、$K_{1}\subset K_{2}$なら$\Psi(K_{1})\subset\Psi(K_{2})$が成り立つ。




## 準同型と準同型定理

__定義__ $R, R^{\prime}$を環とする。写像$f\colon R\rightarrow R^{\prime}$が以下を満たすとき **準同型** （homomorphism）という。

- $a, b\in R$について$f(a+b)=f(a)+f(b)$が成り立つ。
- $a, b\in R$について$f(ab)=f(a)f(b)$が成り立つ。

__定義__ $R, R^{\prime}$を環とする。二つの準同型$f\colon R\rightarrow R^{\prime}, g\colon R^{\prime}\rightarrow R$が存在して$g\circ f=\mathrm{id}_{R}$かつ$f\circ g=\mathrm{id}_{R^{\prime}}$を満たすとき$R$と$R^{\prime}$は **同型** （isomorphic）であるといい、$R\simeq R^{\prime}$と表す。

- 環の準同型$f$について、同型を与えることと$f$が全単射であることは同値である。

環の準同型$f\colon R\rightarrow R^{\prime}$に対しても群の場合と同様に核と像を定義することができる。ただし核は加法単位元の逆像なので

$$
\mathrm{Ker}f=\lbrace a\in R : f(a)=0 \rbrace
$$

である。環の準同型は積の構造を保つから核や像は部分環で、更に$\Delta_{f}:=\lbrace (x, y) : f(x)=f(y) \rbrace$が$R$上の合同関係となるから$0/\Delta_{f}=\mathrm{Ker}f$が成り立つ。故に$\mathrm{Ker}f$はイデアルである。準同型定理も同様に成り立つ。

__定理__ （準同型定理）$f\colon R\rightarrow R^{\prime}$を環の準同型とする。このとき環としての同型

$$
R/\mathrm{Ker}f\simeq\mathrm{Im}f
$$

が成り立つ。

> 準同型の合成は準同型であり、恒等写像も準同型である。これらは射の条件を満たし環の圏$\mathbf{Rng}$を定める。対象のクラスを単位的環に制限し、更に準同型を単位元を保つ（$f(1)=1$）ものに制限することで、単位的環の圏$\mathbf{Ring}$を定めることができる。更に対象のクラスを単位的可換環に制限したものを単位的可換環の圏$\mathbf{commRing}$と表す。どちらも準同型定理が同様に成り立つ。