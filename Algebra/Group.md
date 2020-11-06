
# 群

群は数学のあらゆる場面に現れる、最も基本的な代数構造である。群はある数学的オブジェクトの自己同型を抽象化したものであり、一般にそのオブジェクトの対称性を記述すると考えられている。この論理を追うことは数学を学ぶ上で良い訓練になるが、抽象度が高いため理解が進まないこともあると思う。そういうときは様々な具体例を計算すると良いので、可能ならばどこかに具体例のページを作りたい。

群の構造を記述する代表的な概念は二つある。一つは部分代数としての部分群、もう一つは合同関係としての正規部分群である。名前から察するように正規部分群は部分群でもあるが両者の出どころは異なる。部分群はあくまでも元の群の部分的な構造を表しているのに対し、正規部分群は準同型定理を通して元の群としての性質を良く表している。


## 群と部分群

__定義__ $G$を空でない集合とする。演算$\cdot\colon G\times G\rightarrow G$は以下を満たすとする。

- 結合的である。つまり$a, b, c\in G$について$(a\cdot b)\cdot c=a\cdot(b\cdot c)$が成り立つ。
- 単位元が存在する。ある$1\in G$が存在して、どの$a\in G$についても$a\cdot 1=1\cdot a=a$が成り立つ。この$1$を **単位元** （unit element）という。
- 逆元が存在する。$a\in G$について、ある$b\in G$が存在して$a\cdot b=b\cdot a=1$が成り立つ。この$b$を$a$の **逆元** （inverse element）という。

このとき集合の組$(G, \cdot, 1)$を **群** （group）と呼ぶ。

群$G$と書くときは上記の組が想定されているものとする。演算$\cdot$は$\cdot_{G}$と表すこともあるが、明らかな場合は$a\cdot b$を$ab$と略記する。

- 単位元は一意的である。実際$e\in G$も単位元の条件を満たすなら、$e=1e=1$である。この意味で単位元を$1_{G}$と表す。
- 逆元は一意的である。実際$c\in G$も逆元の条件を満たすなら、$c=c1=cab=1b=b$である。この意味で$a$の逆元を$a^{-1}$と表す。
- $1^{-1}=1$であり、$(ab)^{-1}=b^{-1}a^{-1}$である。

__定義__ 群$G$の演算が可換のとき、つまり$a, b\in G$について$ab=ba$が成り立つとき、$G$は **アーベル群** （arbelian group）という。

> アーベル群の場合、演算$\cdot$と単位元$1$は$+$と$0$で表されることが多い。

__例__ 以下に例を挙げるが、後でまたちゃんと定義する。

- $\mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}$は、加法に関してアーベル群となる。単位元は$0$で、$a$の逆元は$-a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$から原点を除いた集合$k^{\times}$は、乗法に関してアーベル群となる。単位元は$1$で、$a$の逆元は$1/a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$n$次正則行列全体$\mathrm{GL}(n; k)$は、行列の積に関して群となる。このような群を一般線型群という。
- 相異な$n$文字の置換（全単射）全体$S_{n}$は、写像の合成に関して群となる。これを$n$次対称群という。

__定義__ $G$を群とする。$H\subset G$が$G$の演算によって群になるとき **部分群** （subgroup）という。このとき$H\lt G$と表す。

__命題__ $H\lt G$を部分群とする。以下が成り立つ。

- $H$の単位元は$G$の単位元と一致する。
- $a\in H$のとき、$H$における$a$の逆元は、$G$における$a$の逆元と一致する。

（証明）$1_{H}$の$G$における逆元を$x$とする。$1_{G}=1_{H}x=x1_{H}$だから、$1_{H}=(x1_{H})1_{H}=x(1_{H}1_{H})=x1_{H}=1_{G}$を得る。

$a\in H$の$H$での逆元を$b$、$G$における逆元を$c$とする。$b=b(ac)=(ba)c=c$より従う。$\square$

__例__ 部分群の例を挙げる。

- $\mathbb{Z}\lt\mathbb{Q}\lt\mathbb{R}\lt\mathbb{C}$である。
- $\mathbb{T}_{1}=\lbrace z\in\mathbb{C} : \vert z \vert=1 \rbrace$は$\mathbb{C}^{\times}$の部分群である。これを$1$次元トーラスという。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$\mathrm{SL}(n; k):=\lbrace A\in\mathrm{GL}(n; k) : \mathrm{det}A=1 \rbrace$は$\mathrm{GL}(n; k)$の部分群である。これを特殊線型群という。
- 正方形でない長方形$R$を$R$自身に写す変換は$4$頂点の置換で表され、その全体$V$は$S_{4}$の部分群となる。これをクラインの$4$群という。

__定理__ （部分群の特徴付け）$G$を群、$H\subset G$は空でないとする。TFAE

1. $H$は$G$の部分群である。
1. $a, b\in H$に対し、$ab\in H$かつ$a^{-1}\in H$である。
1. $a, b\in H$に対し、$ba^{-1}\in H$である。

（証明）上から下は明らか。一番下を仮定して一番上を示そう。$H$は空でないから$a\in H$が取れる。$1=aa^{-1}\in H$より$1\in H$である。よって$b\in H$に対して$b^{-1}=1b^{-1}\in H$である。故に$a, b\in H$に対して$ab=a(b^{-1})^{-1}\in H$を得る。$H$は$G$の演算で閉じていて、単位元を持ち、逆元が存在する。以上より$H$は$G$の部分群である。$\square$


## 正規部分群と合同関係

__定義__ $S$を空でない集合とする。$\theta\subset S\times S$を$S$上の **関係** （relation）という。$(a, b)\in\theta$のことを$a\theta b$と表す。

__定義__ 関係$\theta$が以下を満たすとき$\theta$を **同値関係** （equivaliance relation）という。

- 反射的である。つまり$a\theta a$である。
- 対称的である。つまり$a\theta b$なら$b\theta a$である。
- 推移的である。つまり$a\theta b, b\theta c$なら$a\theta c$である。

> 同値関係は等号の性質の一部を抜き出したものである。従って「等しい」という関係$=$も同値関係である。ただし等号はどのような操作でも等しいという強い性質を持つので、同値関係はそれより弱い概念である。

__定義__ $G$を群、$H\subset G$とする。このとき関係$a\theta_{H}b$を$ba^{-1}\in H$で定める。

__命題__ $G$を群、$H\subset G$とする。TFAE

1. $H$は$G$の部分群である。
1. $\theta_{H}$は同値関係である。

（証明）$H$を部分群とする。$a\in G$に対し、$aa^{-1}=1\in H$より$a\theta_{H}a$を得る。また$a\theta_{H}b$なら$ba^{-1}\in H$だから$ab^{-1}=(ba^{-1})^{-1}\in H$より$b\theta_{H}a$を得る。更に$a\theta_{H}b, b\theta_{H}c$なら$ba^{-1}, cb^{-1}\in H$だから$ca^{-1}=(cb^{-1})(ba^{-1})\in H$より$a\theta_{H}c$を得る。

逆に$\theta_{H}$を同値関係とする。$1\in G$について反射性より$1\theta_{H}1$である。よって$1\in H$だから$H$は空でない。次に$a, b\in H$とする。$1\theta_{H}a, 1\theta_{H}b$より対称性と推移性から$a\theta_{H}b$を得る。故に$ba^{-1}\in H$である。特徴付けより$H$は$G$の部分群である。$\square$

__定義__ $G$を群、$\theta$を$G$上の同値関係とする。以下が成り立つとき$\theta$を **合同関係** （congruence relation）といい、全体を$\mathrm{Con}(G)$と表す。

- $a\theta b$なら$a^{-1}\theta b^{-1}$である。
- $a\theta a^{\prime}, b\theta b^{\prime}$なら$ab\theta a^{\prime}b^{\prime}$である。

__定義__ $N\lt G$を部分群とする。全ての$x\in G$に対して$x^{-1}Nx\subset N$が成り立つとき **正規部分群** （normal subgroup）という。

> 正規部分群の定義は等号（$x^{-1}Nx=N$）でも良い。実際$N$が正規部分群なら$x^{-1}$について$xNx^{-1}\subset N$より$N\subset x^{-1}Nx$が成り立つ。

- アーベル群において、部分群は正規部分群である。

__補題__ $G$を群、$N\subset G$は空でないとする。TFAE

1. $N$は正規部分群である。
1. $\theta_{N}$は合同関係である。

（証明）$N$を正規部分群とする。$\theta_{N}$が同値関係であることは良い。$a\theta_{N}b$とする。$b\theta_{N}a$より$ab^{-1}\in N$である。$x=a$に対して仮定より

$$
b^{-1}a=a^{-1}(ab^{-1})a\in N
$$

より$a^{-1}\theta_{N}b^{-1}$が従う。また$a\theta_{N}b, c\theta_{N}d$とすると、$ba^{-1}, dc^{-1}\in N$である。$dc^{-1}$について、$x=a^{-1}$に対して仮定より$a(dc^{-1})a^{-1}\in N$である。ここで$ba^{-1}\in N$を左から掛けて$bdc^{-1}a^{-1}\in N$を得る。故に$ac\theta_{N}bd$である。

逆に$\theta_{N}$を合同関係とする。$N$が部分群であることは良い。$y\in N$とすると$1\theta_{N}y$である。一方$x^{-1}\theta_{N}x^{-1}$だから合同関係の定義より$x^{-1}\theta_{N}x^{-1}y$である。つまり$x^{-1}y(x^{-1})^{-1}\in N$より$N$は正規部分群である。$\square$


## 剰余群と準同型定理

$G$を群、$\theta\in\mathrm{Con}(G)$を合同関係とする。$a\in G$に対してその同値類を$a/\theta:=\lbrace b\in G : a\theta b \rbrace$で表し、その全体を$G/\theta:=\lbrace a/\theta : a\in G \rbrace$とする。このとき$G/\theta$上の演算$\cdot_{\theta}$を

$$
(a/\theta)\cdot_{\theta}(b/\theta):=ab/\theta
$$

で定めることができる。実際、合同関係の定義よりwell-definedである。このとき$G/\theta$は群となる。単位元は$1/\theta$であり、$a/\theta$の逆元は$a^{-1}/\theta$である。

__定理__ $G$を群とする。以下が成り立つ。

- $N\lhd G$を正規部分群とする。$\theta_{N}$は$G$上の合同関係であり$N=1/\theta_{N}$が成り立つ。
- $\theta\in\mathrm{Con}(G)$を合同関係とする。$N:=1/\theta$は$G$の正規部分群であり、$\theta=\theta_{N}$が成り立つ。

（証明）$N$を正規部分群とする。補題より$\theta_{N}$は合同関係である。$N=1/\theta_{N}$は明らか。

$\theta$を合同関係とする。$a\theta b$とすると、反射性より$a^{-1}\theta a^{-1}$だから$1\theta ba^{-1}$である。故に$ba^{-1}\in N$だから$a\theta_{N}b$を得る。逆も同様なので$\theta=\theta_{N}$が成り立つ。補題より$N$は正規部分群である。$\square$

以上より正規部分群と合同関係の間に一対一の対応が成り立つ。この意味で$G/\theta_{N}$のことを$G/N$と表す。また$a/\theta=aN$であるから、こちらの表記も用いる。

__定義__ $N\lhd G$を正規部分群とする。上記の群$G/N$を$G$の$N$による **剰余群** （residue class group）という。

> 更に包含を保つ束としての同型を与えている。対角集合$\Delta=\lbrace (a, a) : a\in G \rbrace$について$1/\Delta=\lbrace 1 \rbrace$であり、全体集合$\nabla=\lbrace (a, b) : a, b\in G \rbrace$について$1/\nabla=G$となる。

__定義__ $G, G^{\prime}$を群とする。写像$f\colon G\rightarrow G^{\prime}$が以下を満たすとき **準同型** （homomorphism）という。

- $a, b\in G$について$f(ab)=f(a)f(b)$が成り立つ。

> 準同型の合成は準同型であり、恒等写像も準同型である。これらは射の条件を満たすため、群の圏$\mathbf{Grp}$が定まる。対象としてアーベル群に制限することでアーベル群の圏$\mathbf{Ab}$も定まる。

__命題__ 準同型$f\colon G\rightarrow G^{\prime}$について以下が成り立つ。

- $f(1)=1$である。
- $f(a^{-1})=f(a)^{-1}$である。

（証明）$f(1)=f(1\cdot 1)=f(1)f(1)$より、左から$f(1)^{-1}$を掛ければよい。

$1=f(1)=f(aa^{-1})=f(a)f(a^{-1})$より、逆元の一意性から従う。$\square$

__定義__ $G, G^{\prime}$を群とする。二つの準同型$f\colon G\rightarrow G^{\prime}, g\colon G^{\prime}\rightarrow G$が存在して$g\circ f=\mathrm{id}_{G}$かつ$f\circ g=\mathrm{id}_{G^{\prime}}$を満たすとき$G$と$G^{\prime}$は **同型** （isomorphic）であるといい、$G\simeq G^{\prime}$と表す。

- 群の準同型$f$について、同型を与えることと$f$が全単射であることは同値である。

__定義__ $f\colon G\rightarrow G^{\prime}$を群の準同型とする。次を定義する。

- $\mathrm{Ker}f:=\lbrace a\in G : f(a)=1 \rbrace$を$f$の **核** （kernel）という。
- $\mathrm{Im}f:=f(G)=\lbrace f(a) : a\in G \rbrace$を$f$の **像** （image）という。

__命題__ $f\colon G\rightarrow G^{\prime}$を群の準同型とする。$\Delta_{f}:=\lbrace (x, y) : f(x)=f(y) \rbrace$は$G$上の合同関係であり、$1/\Delta_{f}=\mathrm{Ker}f$が成り立つ。

（証明）合同関係であることは明らか。$x\in 1/\Delta_{f}$なら$1\Delta_{f}x$より$f(x)=f(1)=1$である。故に$x\in\mathrm{Ker}f$となる。逆も同様である。$\square$

$\mathrm{Ker}f\subset G, \mathrm{Im}f\subset G^{\prime}$はそれぞれ部分群である。特に$\mathrm{Ker}f$は正規部分群である。

__定理__ （準同型定理）$f\colon G\rightarrow G^{\prime}$を群の準同型とする。このとき同型

$$
G/\mathrm{Ker}f\simeq\mathrm{Im}f
$$

が成り立つ。

（証明）$a/\Delta_{f}$に対して$f(a)$を対応させる写像はwell-definedな準同型であり、全単射である。$\square$

> アーベル群の部分群は正規部分群だから、準同型$f\colon G\rightarrow G^{\prime}$に対して、核や余核$\mathrm{Cok}f:=G^{\prime}/\mathrm{Im}f$が常に定義できる。更に準同型定理より余像$\mathrm{Coim}f:=G/\mathrm{Ker}f$と像の同型が成り立つ。これらは圏論的な意味を持つため、$\mathbf{Ab}$はアーベル圏になる。