
# 環上の加群

以下、$R$を単位的可換環とする。

__定義__ $(M, +, 0)$をアーベル群とする。演算$\colon R\times M\rightarrow M$は以下を満たすとする。

- $a\in R, x, y\in M$について$a\cdot(x+y)=a\cdot x+a\cdot y$が成り立つ。
- $a, b\in R, x\in M$について$(a+b)\cdot x=a\cdot x+b\cdot x$が成り立つ。
- $a, b\in R, x\in M$について$(ab)\cdot x=a\cdot(b\cdot x)$が成り立つ。
- $x\in M$について$1_{R}\cdot x=x$が成り立つ。

このとき$M$を$R$上の **加群** （module）、あるいは$R$加群や単に加群と呼ぶ。

$a\cdot x$は$ax$と略記する。一般に$(-a)\cdot x=-(ax)$が成り立つので$-ax$と略記する。$0_{R}\cdot x=0$である。

> 上記は$R$の可換性を除いた場合に左加群を定める。$(ab)x=a(bx)$を$(ab)x=b(ax)$に変えた場合は右加群と呼ばれるが、今は乗法について可換な環を考えているので同等になる。右加群の場合は演算を$\cdot\colon M\times R\rightarrow M$として$x\cdot (ab)=(x\cdot a)\cdot b$とする方が標準的だが、左右の違いは$R$の元が作用する順番が本質である。

- $\lbrace 0 \rbrace$は常に$R$加群となる。これを単に$0$と表す。
- 環$R$自身は$R$加群である。より一般に$R$のイデアル$I$も$R$加群である。
- ベクトル空間、あるいは線型空間は体上の加群のことである。ただしその性質は大きく異なる。




## 部分加群と合同関係

__定義__ $M$を$R$加群とする。部分群$N\subset M$が$M$の演算で$R$加群となるとき **部分加群** （submodule）と呼ぶ。このとき$N\lt M$と表す。

$R$加群はアーベル群だから、群としての同値関係や合同関係が同様に定義される。加群としての合同関係は$R$の作用を反映した形で定義される。

__定義__ $M$を$R$加群とする。$M$上の群としての合同関係$\theta$は以下を満たすとする。

- $a\in R, x, y\in M$について$x\theta y$なら$ax\theta ay$である。

このとき$\theta$を加群としての合同関係と呼び、全体を$\mathrm{Con}(M)$と表す。

__補題__ $M$を$R$加群、$N\subset M$とする。TFAE

1. $N$は部分加群である。
1. $\theta_{N}$は加群としての合同関係である。

（証明）$N\lt M$とする。$\theta_{N}$は群としての合同関係だから、$R$の作用に関する条件を示せば良い。$x\theta_{N}y$とする。$a\in R$について$ax-ay=a(x-y)$である。ここで$x-y\in N$かつ$N$は部分加群なので$a(x-y)\in N$となる。故に$ax\theta_{N}ay$を得る。

逆に$\theta_{N}$が加群としての合同関係とする。既に群の場合に示した通り、$N$は加法に関して$M$の部分群である。よって$R$の作用で閉じていることを示せば良い。$x\in N$とする。$x\theta_{N}0$だから、$a\in R$について仮定より$ax\theta_{N}0$となる。よって$ax\in N$を得る。$\square$




## 剰余加群と準同型定理

$M$を$R$加群、$\theta\in\mathrm{Con}(M)$を合同関係とする。$x\in M$の同値類$x/\theta$の全体$M/\theta$は

$$
\begin{aligned}
(x/\theta)+_{\theta}(y/\theta) &:=(x+y)/\theta \\
(a/\theta)\cdot_{\theta}(x/\theta) &:=(ax)/\theta
\end{aligned}
$$

により$R$加群となる。

> TODO




__定義__ $M, N$を$R$加群とする。写像$f\colon M\rightarrow N$が以下を満たすとき **準同型** （homomorphism）という。

- $x, y\in M$について$f(x+y)=f(x)+f(y)$が成り立つ。
- $a\in R, x\in M$について$f(ax)=af(x)$が成り立つ。

また準同型$f\colon M\rightarrow N$に対し以下を定める。

- $\mathrm{Ker}f:=\lbrace x\in M : f(x)=0 \rbrace$を$f$の核（kernel）という。
- $\mathrm{Im}f:=\lbrace f(x) : x\in M$を$f$の像（image）という。

特に$f(0)=0$だから$\mathrm{Ker}f, \mathrm{Im}f\neq\emptyset$である。$\mathrm{Ker}f=\lbrace 0 \rbrace$と$f$が単射であることは同値であり、$\mathrm{Im}f=N$と$f$が全射であることは同値となる。

> 環$R$上の加群と準同型は加群の圏$\mathbf{Mod}_{R}$を作る。これはアーベル圏の代表例であり重要な圏である。$\mathbf{Mod}_{R}$は環$R$を完全に決定することが知られており、この意味で加群は環の外部表現といえる。なお非可換環の場合にはもっと深い理論がある。

__定義__ $M, N$を$R$加群とする。二つの準同型$f\colon M\rightarrow N, g\colon N\rightarrow M$が存在して$g\circ f=\mathrm{id}_{M}$かつ$f\circ g=\mathrm{id}_{N}$を満たすとき$M$と$N$は **同型** （isomorphic）であるといい、$M\simeq N$と表す。

- 準同型について同型と全単射であることは同値である。

__定義__ $R$加群$M$の部分集合が$M$の演算で$R$加群となるとき、部分加群という。

- 準同型$f\colon M\rightarrow N$について$\mathrm{Ker}f\subset M, \mathrm{Im}f\subset N$は部分加群である。
- 単射準同型$f\colon M\rightarrow N$について同型$M\simeq f(M)\subset N$によって$M$を$N$の部分加群とみなすことがある。
- 環$R$の$R$加群としての部分加群はイデアルのことに他ならない。

$R$加群$M$の部分加群$N$について$x+N:=\lbrace x+y : y\in N \rbrace$を集めた集合

$$
M/N:=\lbrace x+N : x\in M \rbrace
$$

に自然な$R$加群の構造を$(x+N)+(y+N):=(x+y)+N$及び$a\cdot(x+N):=ax+N$で定めることができる。

__定義__ 上記の$R$加群$M/N$を **剰余加群** と呼ぶ。

__定理__ （準同型定理）$f\colon M\rightarrow N$を$R$加群の間の準同型とする。$M/\mathrm{Ker}f\simeq\mathrm{Im}f$が成り立つ。

（証明）$\overline{f}\colon M/\mathrm{Ker}f\rightarrow\mathrm{Im}f$を$f(x+M):=f(x)$で定める。このとき$\overline{f}$は準同型かつ全単射である。$\square$

- $\mathrm{Cok}f:=N/\mathrm{Im}f$を$f$の **余核** （cokernel）という。
- $\mathrm{Coim}f:=M/\mathrm{Ker}f$を$f$の **余像** （coimage）という。

> 準同型定理は$\mathrm{Coim}f\simeq\mathrm{Im}f$と表せる。

__定義__ $R$加群$M_{i}$及び準同型$f_{i}\colon M_{i}\rightarrow M_{i+1}$の組を加群の **系列** （sequence）と呼ぶ。

$$
\dotsb\rightarrow M_{i-1}\xrightarrow{f_{i-1}}M_{i}\xrightarrow{f_{i}}M_{i+1}\rightarrow\dotsb
$$

この系列において$\mathrm{Im}f_{i}=\mathrm{Ker}f_{i+1}$が常に成り立つとき、系列は **完全** （exact）であるという。

準同型$f\colon M\rightarrow N$について以下が成り立つ。

- $f$が単射であるとは$0\rightarrow M\xrightarrow{f}N$が完全であることに他ならない。
- $f$が全射であるとは$M\xrightarrow{f}N\rightarrow 0$が完全であることに他ならない。