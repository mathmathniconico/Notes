# 圏の例

我々が今何について考えているのか、その間の関連性をどのように記述しているのかは、圏を指定することで明らかとなる。この意味で圏は一つの議論領域であり、理論を俯瞰的に捉える大きな枠組みを我々に与えてくれる。

以下はこのノートで基本的に詳しく扱わない圏のリストである。前提知識としては$\mathbf{Set}$と$\mathbf{Top}$が何かくらいを知っていれば問題ない。




## 小さい圏の例

### 半順序集合

$X$を集合、$\le$を二項関係とする。組$(X, \le)$が以下を満たすとき **半順序集合** （partially ordered set, poset）と呼ぶ。$x, y, z\in X$とする。

- $x\le x$である。（反射律）
- $x\le y$かつ$y\le z$なら$x\le z$である。（推移律）
- $x\le y$かつ$y\le x$なら$x=y$である。（反対称律）

$(X, \le)$を半順序集合とする。以下で圏を定める。

- 対象は$x\in X$とする。
- $x, y\in X$とする。$x\le y$のときに限り射$x\rightarrow y$を定める。

この圏において、対象$x, y$が同型とは$x=y$のことである。

> 圏とみなすには反対称律は必要ない。つまり前順序（preorder, quasi-order）集合も圏とみなせる。

__例__ 自然数$\mathbb{N}$において、関係$a\vert b$を「$a$が$b$を割り切る」とする。このとき$(\mathbb{N}, \vert)$は半順序集合となる。$0$や$1$、最小公倍数や最大公約数はどういう対象か考えよ。

__例__ 集合$X$に対して、$P(X):=2^{X}$を$X$の部分集合全体とする。$P(X)$は包含関係$\subset$により半順序集合$(P(X), \subset)$を定める。$\emptyset$や$X$自身、$A, B\subset X$について$A\cap B$や$A\cup B$はどういう対象か考えよ。包含関係を$\supset$で入れるとどうか。


### モノイド

$M$を集合、$\cdot\colon M\times M\rightarrow M$を二項演算とする。組$(M, \cdot)$が以下を満たすとき **モノイド** （monoid）と呼ぶ。$a, b, c\in M$とする。

- $a\cdot(b\cdot c)=(a\cdot b)\cdot c$が成り立つ。（結合律）
- ある$1_{M}\in M$が存在して$a\cdot 1_{M}=1_{M}\cdot a=a$が成り立つ。（単位元の存在）

$(M, \cdot)$をモノイドとする。圏$\overrightarrow{M}$を以下で定める。

- 対象は一つとする。つまり$\mathrm{Ob}=\lbrace \ast \rbrace$とする。
- 射は$M$の元とする。つまり$\mathrm{Mor}(\ast, \ast)=M$とする。ただし射の合成を$a\circ b:=a\cdot b$と定める。

> $a\circ b:=b\cdot a$と定める流儀と、どちらが良いのかは場合による。

このとき恒等射は$\mathrm{id}_{\ast}=1_{M}$である。

__定義__ 圏$\mathscr{C}$は、全ての射が同型のときgroupoidという。

- 群$G$について圏$\overrightarrow{G}$はgroupoidである。

> 名前が似ているがモノイド圏、あるいはモノイダル圏と呼ばれる概念が存在する。一応異なるものなので注意すること。


### 全ての行列が成す圏

有用かどうかは知らないが、変わり種に次のような圏もある。

- 対象は非負整数$n\ge 1$とする。
- 非負整数$m, n\ge 1$について$M$を適当な成分（例えば体や単位的可換環）の$m\times n$行列（$m$行$n$列）とする。このとき$M\colon n\rightarrow m$と表して射とみなす。

$n\times l$行列$N\colon l\rightarrow n$と$m\times n$行列$M\colon n\rightarrow m$の合成は$M\circ N:=MN\colon l\rightarrow n$によって定義される。

各対象$n$の恒等射は単位行列$E_{n}$である。




## 局所的に小さい圏の例

### 集合と写像の圏

$\mathbf{Set}$

$G\mathbf{Set}$

### 位相空間と連続写像の圏

$\mathbf{Top}$

$\mathbf{HTop}$

__例__ $C^{\infty}$多様体と$C^{\infty}$写像の圏

### 代数と準同型の圏

__例__ 群と群準同型の圏$\mathbf{Grp}$

__例__ 単位的環と単位元を保つ環準同型の圏$\mathbf{Ring}$

__例__ $R$加群とその準同型の圏$\mathbf{Mod}_{R}$


### その他

$\mathbf{Conv}$

$\mathbf{Prob}$



