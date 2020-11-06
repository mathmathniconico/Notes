
# 環上の加群

## 環上の加群と準同型

__定義__ $R$を環とする。次を満たす集合の組$(M, +, \cdot, 0)$を$R$上の **加群** （module）あるいは単に$R$加群という。

- 加法$+\colon M\times M\rightarrow M$及び$0\in M$はアーベル群の構造を定める。
- スカラー倍$\cdot R\times M\rightarrow M$は以下を満たす。
	- $a\in R$及び$x, y\in M$について$a\cdot(x+y)=a\cdot x+a\cdot y$が成り立つ。
	- $a, b\in R$及び$x\in M$について$(a+b)\cdot x=a\cdot x+b\cdot x$が成り立つ。
	- $a, b\in R$及び$x\in M$について$(ab)\cdot x=a\cdot(b\cdot x)$が成り立つ。
	- $x\in M$について$1\cdot x=x$が成り立つ。

$R$加群$M$と書くときは上記の組が想定されているものとする。スカラー倍$a\cdot x$は$ax$と略記する。一般に$(-a)\cdot x=-(ax)$が成り立つので$-ax$と略記する。

> 厳密には左加群と呼ばれるものの定義である。$(ab)x=a(bx)$を$(ab)x=b(ax)$に変えた場合は右加群と呼ばれるが、今は乗法について可換な環を考えているので同等になる。右加群の場合は、スカラー倍を$\cdot\colon M\times R\rightarrow M$として$x\cdot (ab)=(x\cdot a)\cdot b$とする方が一般的かもしれない。

- 環$R$自身は$R$加群である。より一般に$R$のイデアル$I$も$R$加群である。
- $\alpha\in\mathbb{Z}$について$\alpha\mathbb{Z}$は$\mathbb{Z}$のイデアルである。
- ベクトル空間、あるいは線型空間は体上の加群のことである。ただし性質は大きく異なるので別に扱う方が筋は良い。

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