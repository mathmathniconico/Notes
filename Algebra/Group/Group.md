
# 群

群は数学のあらゆる場面に現れる、最も基本的な代数構造である。群はある数学的オブジェクトの自己同型を抽象化したものであり、一般にそのオブジェクトの対称性を記述すると考えられている。この論理を追うことは数学を学ぶ上で良い訓練になるが、抽象度が高いため理解が進まないこともあると思う。そういうときは様々な具体例を計算すると良い。必要に応じて具体的な群に関するページを設けるつもりなので、並行して読み進めて欲しい。

群の構造を記述する代表的な概念は二つある。一つは部分代数としての部分群、もう一つは合同関係としての正規部分群である。名前から察するように正規部分群は部分群でもあるが両者の出処は異なる。部分群はあくまでも元の群の部分的な構造を表しているのに対し、正規部分群は準同型定理を通して元の群としての性質を良く継承している。




## 群と部分群

__定義__ $G$を空でない集合とする。演算$\cdot\colon G\times G\rightarrow G$は以下を満たすとする。

- $a, b, c\in G$について$(a\cdot b)\cdot c=a\cdot(b\cdot c)$が成り立つ。（結合律）
- ある$1\in G$が存在して、どの$a\in G$についても$a\cdot 1=1\cdot a=a$が成り立つ。（単位元の存在）
- $a\in G$について、ある$b\in G$が存在して$a\cdot b=b\cdot a=1$が成り立つ。（逆元の存在）

このとき集合の組$(G, \cdot, 1)$を **群** （group）と呼ぶ。

群$G$と書くときは上記の組が想定されているものとする。演算は$\cdot_{G}$と表すこともあるが、明らかな場合は$a\cdot b$を$ab$と略記する。

- $1\in G$は一意的である。この意味で$1_{G}$と表し$G$の **単位元** （unit element）と呼ぶ。
- 上記の$b\in G$は一意的である。この意味で$a^{-1}$と表し$a$の **逆元** （inverse element）と呼ぶ。
- $G$が可換（$a, b\in G$について$ab=ba$）のとき **アーベル群** （abelian group）と呼ぶ。アーベル群の演算と単位元は$+$と$0$で表される。

__定義__ $G$を群とする。$H\subset G$が$G$の演算によって群になるとき **部分群** （subgroup）と呼ぶ。このとき$H\lt G$と表す。

__命題__ $H\lt G$を部分群とする。$H$の単位元および逆元は、$G$の単位元および逆元と一致する。

（証明）$1_{H}$の$G$における逆元を$x$とすると$1_{H}=(x1_{H})1_{H}=x(1_{H}1_{H})=x1_{H}=1_{G}$を得る。$a\in H$の$H$での逆元を$b$、$G$における逆元を$c$とすると、$b=b(ac)=(ba)c=c$を得る。$\square$

__定理__ （部分群の特徴付け）$G$を群、$H\subset G$は空でないとする。TFAE

1. $H$は$G$の部分群である。
1. $a, b\in H$に対し、$ab\in H$かつ$a^{-1}\in H$である。
1. $a, b\in H$に対し、$b^{-1}a\in H$である。

（証明）上から下は明らか。一番下を仮定して一番上を示そう。$a\in H$を取ると$1=a^{-1}a\in H$である。よって$b\in H$に対して$b^{-1}=b^{-1}1\in H$である。故に$a, b\in H$に対して$ab=(a^{-1})^{-1}b\in H$を得る。$H$は$G$の演算で閉じていて、単位元を持ち、逆元が存在する。以上より$H$は$G$の部分群である。$\square$

__定義__ $G$を群、$S\subset G$とする。$Z(S):=\lbrace a\in G : \forall s\in S, sa=as \rbrace$を$S$の **中心** （center）と呼ぶ。

__命題__ $G$を群、$S\subset G$とする。$S$の中心$Z(S)$は$G$の部分群である。

（証明）$1\in Z(S)$より空でない。$a, b\in Z(S)$とする。$s\in S$について$sab=asb=abs$より$ab\in Z(S)$、また$as=sa$より$s^{-1}a=as^{-1}$だから$a^{-1}\in Z(S)$である。特徴付けより$Z(S)$は$G$の部分群となる。$\square$

> 特に$Z(G)$はアーベル群である。実際$a, b\in Z(G)\subset G$より$ab=ba$が成り立つ。




## 合同関係と正規部分群

__定義__ $S$を空でない集合とする。$\theta\subset S\times S$を$S$上の **関係** （relation）と呼び、$(a, b)\in\theta$のことを$a\theta b$と表す。

__定義__ 空でない関係$\theta$が以下を満たすとき$\theta$を **同値関係** （equivaliance relation）と呼ぶ。

- $a\in S$について$a\theta a$である。（反射律）
- $a, b\in S$について$a\theta b$なら$b\theta a$である。（対称律）
- $a, b, c\in S$について$a\theta b, b\theta c$なら$a\theta c$である。（推移律）

__定義__ $G$を群、$H\subset G$とする。このとき関係$a\theta_{H}b$を$b^{-1}a\in H$で定める。

__命題__ $G$を群、$H\subset G$とする。TFAE

1. $H$は$G$の部分群である。
1. $\theta_{H}$は同値関係である。

（証明）$H$を部分群とする。$1=1^{-1}1\in H$より$\theta_{H}$は空でない。$a\in G$について$a^{-1}a=1\in H$より$a\theta_{H}a$を得る。また$a\theta_{H}b$なら$a^{-1}b=(b^{-1}a)^{-1}\in H$より$b\theta_{H}a$を得る。更に$a\theta_{H}b, b\theta_{H}c$なら$c^{-1}a=(c^{-1}b)(b^{-1}a)\in H$より$a\theta_{H}c$を得る。

逆に$\theta_{H}$を同値関係とする。$1\in G$について反射性より$1\theta_{H}1$である。よって$1=1^{-1}1\in H$だから$H$は空でない。次に$a, b\in H$とする。$a\theta_{H}1, b\theta_{H}1$だから、対称律と推移律より$a\theta_{H}b$を得る。従って特徴付けより$H$は$G$の部分群である。$\square$

__定義__ $G$を群、$H\lt G$を部分群とする。$\theta_{H}$による同値類を **左剰余類** （left coset）と呼び全体を$G/H$で表す。$a\in G$の同値類は$\overline{a}:=\lbrace b\in G : a\theta_{H}b \rbrace=aH$である。

__定義__ $G$を群、$\theta$を$G$上の同値関係とする。以下が成り立つとき$\theta$を **合同関係** （congruence relation）と呼び、全体を$\mathrm{Con}(G)$と表す。

- $a, b\in G$について、$a\theta b$なら$a^{-1}\theta b^{-1}$である。
- $a, b, c, d\in G$について、$a\theta b, c\theta d$なら$ac\theta bd$である。

__定義__ $N\lt G$を部分群とする。どの$x\in G$に対しても$xNx^{-1}\subset N$であるとき$N$を **正規部分群** （normal subgroup）と呼び$N\lhd G$と表す。

> $x$として$x^{-1}$を取れば$x^{-1}Nx\subset N$より$N\subset xNx^{-1}$が成り立つ。従って包含は等号でも良い。

- $Z(G)$は$G$の正規部分群である。
- アーベル群の部分群は常に正規部分群である。

__補題__ $G$を群、$N\subset G$とする。TFAE

1. $N$は正規部分群である。
1. $\theta_{N}$は合同関係である。

（証明）$N$を正規部分群とする。$\theta_{N}$が同値関係であることは良い。$a\theta_{N}b$とする。反射律より$b\theta_{N}a$だから$ba^{-1}=a(a^{-1}b)a^{-1}\in aNa^{-1}\subset N$より$a^{-1}\theta_{N}b^{-1}$が従う。次に$a\theta_{N}b, c\theta_{N}d$とすると、$c^{-1}(b^{-1}a)c\in c^{-1}Nc\subset N$だから、$d^{-1}c\in N$を左から掛けて$d^{-1}b^{-1}ac\in N$を得る。故に$ac\theta_{N}bd$である。

逆に$\theta_{N}$を合同関係とする。$N$が部分群であることは良い。$y\in N$とすると$y\theta_{N}1$である。一方$x^{-1}\theta_{N}x^{-1}$だから合同関係の定義より$yx^{-1}\theta_{N}x^{-1}$である。つまり$xyx^{-1}\in N$より$N$は正規部分群である。$\square$

> $Z(G)$に対応する合同関係$a\theta_{Z(G)}b$は、任意の$x\in G$について$axa^{-1}=bxb^{-1}$であることと同値となる。




## 剰余群

$G$を群、$\theta\in\mathrm{Con}(G)$を合同関係とする。$a\in G$に対してその同値類を$a/\theta:=\lbrace b\in G : a\theta b \rbrace$で表し、その全体を$G/\theta:=\lbrace a/\theta : a\in G \rbrace$とする。このとき$G/\theta$上の演算$\cdot_{\theta}$を

$$
(a/\theta)\cdot_{\theta}(b/\theta):=ab/\theta
$$

で定める。（合同関係の定義よりwell-definedである。）このとき$G/\theta$は群となる。単位元は$1/\theta$であり、$a/\theta$の逆元は$a^{-1}/\theta$である。

__定理__ $G$を群とする。以下が成り立つ。

- $N\lhd G$を正規部分群とする。$\theta_{N}$は$G$上の合同関係であり$N=1/\theta_{N}$が成り立つ。
- $\theta\in\mathrm{Con}(G)$を合同関係とする。$N:=1/\theta$は$G$の正規部分群であり、$\theta=\theta_{N}$が成り立つ。

（証明）$N$を正規部分群とすると補題より$\theta_{N}$は合同関係である。$N=1/\theta_{N}$は明らか。

$\theta$を合同関係とする。$a\theta b$とすると$b^{-1}\theta b^{-1}$と$b\theta a$より$1\theta b^{-1}a$である。故に$b^{-1}a\in 1/\theta=N$だから$a\theta_{N}b$を得る。逆も同様なので$\theta=\theta_{N}$が成り立つ。補題より$N$は正規部分群である。$\square$

以上より正規部分群と合同関係の間に一対一の対応が成り立つ。特に$G/\theta_{N}=G/N$である。従って$a/\theta_{N}=aN$である。

> 更にこの対応は、包含を保つ束としての同型を与えている。対角集合$\Delta=\lbrace (a, a) : a\in G \rbrace$について$1/\Delta=\lbrace 1 \rbrace$であり、全体集合$\nabla=\lbrace (a, b) : a, b\in G \rbrace$について$1/\nabla=G$となる。

__定義__ $N\lhd G$を正規部分群とする。群$G/N$を$G$の$N$による **剰余群** （residue class group）と呼ぶ。




## 準同型と準同型定理

__定義__ $G, G^{\prime}$を群とする。写像$f\colon G\rightarrow G^{\prime}$が以下を満たすとき **準同型** （homomorphism）と呼ぶ。

- $a, b\in G$について$f(ab)=f(a)f(b)$が成り立つ。

> 準同型$f$について$f(1)=1$及び$f(a^{-1})=f(a)^{-1}$が成り立つ。このように準同型は演算の構造を保存する。

__定義__ $G, G^{\prime}$を群とする。二つの準同型$f\colon G\rightarrow G^{\prime}, g\colon G^{\prime}\rightarrow G$が存在して$g\circ f=\mathrm{id}_{G}$かつ$f\circ g=\mathrm{id}_{G^{\prime}}$を満たすとき$G$と$G^{\prime}$は **同型** （isomorphic）であるといい、$G\simeq G^{\prime}$と表す。

- 群の準同型$f$について、同型を与えることと$f$が全単射であることは同値である。

__定義__ $f\colon G\rightarrow G^{\prime}$を群の準同型とする。次を定義する。

- $\mathrm{Ker}f:=\lbrace a\in G : f(a)=1 \rbrace$を$f$の **核** （kernel）と呼ぶ。
- $\mathrm{Im}f:=f(G)=\lbrace f(a) : a\in G \rbrace$を$f$の **像** （image）と呼ぶ。

> $\mathrm{Ker}f\subset G, \mathrm{Im}f\subset G^{\prime}$はそれぞれ部分群だが、次の命題より特に核は正規部分群であることが分かる。

__命題__ $f\colon G\rightarrow G^{\prime}$を群の準同型とする。$\Delta_{f}:=\lbrace (x, y) : f(x)=f(y) \rbrace$は$G$上の合同関係であり、$1/\Delta_{f}=\mathrm{Ker}f$が成り立つ。

（証明）合同関係であることは明らか。$x\in 1/\Delta_{f}$なら$1\Delta_{f}x$より$f(x)=f(1)=1$である。故に$x\in\mathrm{Ker}f$となる。逆も同様である。$\square$

__定理__ （準同型定理）$f\colon G\rightarrow G^{\prime}$を群の準同型とする。このとき同型

$$
G/\mathrm{Ker}f\simeq\mathrm{Im}f
$$

が成り立つ。

（証明）$a/\Delta_{f}$に対して$f(a)$を対応させる写像はwell-definedな準同型であり、全単射である。$\square$

> 準同型の合成は準同型であり、恒等写像も準同型である。これらは射の条件を満たし群の圏$\mathbf{Grp}$を定める。対象のクラスをアーベル群に制限することでアーベル群の圏$\mathbf{Ab}$も定まる。$\mathbf{Ab}$はアーベル圏の代表例である。