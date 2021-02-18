
# 普遍性

圏において、対象は他の対象との関連性によって記述される。その数学的定式化の一つが普遍性である。ここでは基本的な3つの例を挙げる。普遍性には常に双対概念が定義される。


## 終対象と始対象

既に終対象と始対象については述べたが、これらは普遍性の代表例である。

圏$\mathscr{C}$の終対象$T$は次の2条件を満たすものとして書ける。

- $T$は$\mathscr{C}$の対象である。
- $X$が$\mathscr{C}$の対象なら、唯一つの射$X\rightarrow T$が存在する。

ここで1つ目の条件は$T$についての条件を述べており、2つ目は$X$もまた同じ条件を満たすなら$T$への射が唯一つ存在することを述べている。

始対象$T$も同様に、次の2条件を満たすものとして書ける。

- $I$は$\mathscr{C}$の対象である。
- $X$が$\mathscr{C}$の対象なら、唯一つの射$I\rightarrow X$が存在する。

以上のように「ある条件を満たす集団において普遍的な何か」として定義されることを普遍性という。より丁寧に述べるなら、ある条件を満たすもの全体を圏とみなし、その圏における終対象や始対象を考えている。ただし基本的には終対象の方を考え、終対象と対を為す概念として「余」あるいは「コ」という接頭辞を付ける。この意味で始対象は「余終対象」と呼ぶべきかもしれない。


## 直積と余直積

$A, B\in\mathscr{C}$を対象とする。$A$と$B$の直積は次の普遍性で定義される。

- $A\prod B\in\mathscr{C}$は対象、$p\colon A\prod B\rightarrow A$および$q\colon A\prod B\rightarrow B$は射である。
- $X\in\mathscr{C}$が対象で$f\colon X\rightarrow A, g\colon X\rightarrow B$が射のとき、唯一つの射$h\colon X\rightarrow A\prod B$が存在して$f=p\circ h, g=q\circ h$を満たす。

つまり以下の圏を考えている。

- 対象は$X\in\mathscr{C}$と$f\colon X\rightarrow A, g\colon Y\rightarrow B$の3つ組$(X, f, g)$である。
- $(X, f, g)$および$(Y, a, b)$について、射$x\colon X\rightarrow Y$が$f=x\circ a, g=x\circ b$を満たすとき、これを射$(X, f, g)\rightarrow (Y, a, b)$とする。

直積はこの圏における終対象である。

> 上記の圏の始対象は普通考えない。この理由は自分もよく分かっていないが、覚え方はあり、普遍性は「経由点」として定義される。条件は射の始域であることなので、唯一つ決まる射$h$によって$A\prod B$を経由するのだから終対象である。（条件が対象であることのみの終対象や始対象には当てはまらないが。）

__定義__ $i\in I$について$A_{i}\in\mathscr{C}$を対象とする。$A_{i}$達の **直積** （product）は次の普遍性で定義される。

- $\prod_{i}A_{i}\in\mathscr{C}$は対象、$p_{j}\colon\prod_{i}A_{i}\rightarrow A_{j}$は射である。
- $X\in\mathscr{C}$が対象で$f_{j}\colon X\rightarrow A_{j}$が射のとき、唯一つの射$h\colon X\rightarrow\prod_{i}A_{i}$が存在して$f_{j}=p_{j}\circ h$を満たす。

特に$I$が有限集合のとき、**有限直積** （finite product）という。

直積の双対概念、つまり反対圏$\mathscr{C}^{\mathrm{op}}$における直積が余直積である。

__定義__ $i\in I$について$A_{i}\in\mathscr{C}$を対象とする。$A_{i}$達の **余直積** （coproduct）は次の普遍性で定義される。

- $\coprod_{i}A_{i}\in\mathscr{C}$は対象、$p_{j}\colon A_{j}\rightarrow \coprod_{i}A_{i}$は射である。
- $X\in\mathscr{C}$が対象で$f_{j}\colon A_{j}\rightarrow X$が射のとき、唯一つの射$h\colon \coprod_{i}A_{i}\rightarrow X$が存在して$f_{j}=p_{j}\circ h$を満たす。


## イコライザとコイコライザ










## pull-backとpush-forward



