
# 普遍性

圏において、対象は他の対象との関連性によって記述される。その数学的定式化の一つが普遍性である。



## 普遍性を持つ対象

既に終対象と始対象については述べたが、これらは普遍性の代表例である。

圏$\mathscr{C}$の終対象$T$は次の2条件を満たすものとして書ける。

- $T$は$\mathscr{C}$の対象である。
- $X$が$\mathscr{C}$の対象なら、唯一つの射$X\rightarrow T$が存在する。

<p align=center><img src="pics/universality_terminal.svg" height="20"></p>

ここで1つ目の条件は$T$についての条件を述べており、2つ目は$X$もまた同じ条件を満たすなら$T$への射が唯一つ存在することを述べている。

始対象$T$も同様に、次の2条件を満たすものとして書ける。

- $I$は$\mathscr{C}$の対象である。
- $X$が$\mathscr{C}$の対象なら、唯一つの射$I\rightarrow X$が存在する。

<p align=center><img src="pics/universality_initial.svg" height="20"></p>

以上のように、ある条件を満たす集団において普遍的な「唯一つの射」によって特徴付けられることを普遍性という。循環的だが、ある条件を満たすもの全体を圏とみなし、その圏における終対象や始対象のことを普遍性と呼ぶ。基本的には終対象の方を考え、始対象は反対圏の終対象であるから、終対象と対を為す概念として「余」あるいは「コ」という接頭辞を付ける。この意味で始対象は「余終対象」と呼ぶべきかもしれない。

代表的なものを以下に3つ挙げよう。


### 直積と余直積

$A, B\in\mathscr{C}$を対象とする。$A$と$B$の直積は次の普遍性で定義される。

- $A\prod B\in\mathscr{C}$は対象、$p\colon A\prod B\rightarrow A$および$q\colon A\prod B\rightarrow B$は射である。
- $X\in\mathscr{C}$が対象で$f\colon X\rightarrow A, g\colon X\rightarrow B$が射のとき、唯一つの射$h\colon X\rightarrow A\prod B$が存在して$f=p\circ h, g=q\circ h$を満たす。

<p align=center><img src="pics/universality_2prod.svg" height="100"></p>

つまり以下の圏を考えている。

- 対象は$X\in\mathscr{C}$と$f\colon X\rightarrow A, g\colon Y\rightarrow B$の3つ組$(X, f, g)$である。
- $(X, f, g)$および$(Y, a, b)$について、射$x\colon X\rightarrow Y$が$f=x\circ a, g=x\circ b$を満たすとき、これを射$(X, f, g)\rightarrow (Y, a, b)$とする。

直積はこの圏における終対象である。

> 上記の圏の始対象は普通考えない。この理由は自分もよく分かっていないが、覚え方はあり、普遍性は「経由点」として定義される。条件は射の始域であることなので、唯一つ決まる射$h$によって$A\prod B$を経由するのだから終対象である。（条件が対象であることのみの終対象や始対象には当てはまらないが。）

より多くの直積についても同様に定める。

__定義__ $i\in I$について$A_{i}\in\mathscr{C}$を対象とする。$A_{i}$達の **直積** （direct product）は次の普遍性で定義される。

- $\prod_{i\in I}A_{i}\in\mathscr{C}$は対象、$p_{j}\colon\prod_{i\in I}A_{i}\rightarrow A_{j}$は射である。
- $X\in\mathscr{C}$が対象で$f_{j}\colon X\rightarrow A_{j}$が射のとき、唯一つの射$h\colon X\rightarrow\prod_{i\in I}A_{i}$が存在して$f_{j}=p_{j}\circ h$を満たす。

<p align=center><img src="pics/universality_prod.svg" height="120"></p>

特に$I$が有限集合のとき、**有限直積** （finite product）という。

__定義__ $i\in I$について$A_{i}\in\mathscr{C}$を対象とする。$A_{i}$達の **余直積** （direct coproduct）は次の普遍性で定義される。

- $\coprod_{i}A_{i\in I}\in\mathscr{C}$は対象、$p_{j}\colon A_{j}\rightarrow \coprod_{i\in I}A_{i}$は射である。
- $X\in\mathscr{C}$が対象で$f_{j}\colon A_{j}\rightarrow X$が射のとき、唯一つの射$h\colon \coprod_{i\in I}A_{i}\rightarrow X$が存在して$f_{j}=h\circ p_{j}$を満たす。

<p align=center><img src="pics/universality_coprod.svg" height="120"></p>


### イコライザとコイコライザ

__定義__ $f, g\colon A\rightarrow B$を射とする。$f$と$g$の **イコライザ** （equalizer）は次の普遍性で定義される。

- $E(f, g)\in\mathscr{C}$は対象、$e\colon E(f, g)\rightarrow A$は射であり、$f\circ e=g\circ e$を満たす。
- $X\in\mathscr{C}$が対象で射$x\colon X\rightarrow A$が$f\circ x=g\circ x$を満たすとき、唯一つの射$h\colon X\rightarrow E(f, g)$が存在して$x=e\circ h$を満たす。

<p align=center><img src="pics/universality_equalizer.svg" height="100"></p>

__定義__ $f, g\colon A\rightarrow B$を射とする。$f$と$g$の **コイコライザ** （coequalizer）は次の普遍性で定義される。

- $Q(f, g)\in\mathscr{C}$は対象、$q\colon B\rightarrow Q(f, g)$は射であり$q\circ f=q\circ g$を満たす。
- $X\in\mathscr{C}$が対象で$x\colon B\rightarrow X$が$x\circ f=x\circ g$を満たすとき、唯一つの射$h\colon Q(f, g)\rightarrow X$が存在して$x=h\circ q$を満たす。

<p align=center><img src="pics/universality_coequalizer.svg" height="100"></p>

> イコライザは等化子、コイコライザは余等化子とも呼ばれる。$E(f, g)$や$Q(f, g)$という記号は一般的でないので注意すること。


### ファイバー積と余ファイバー積

__定義__ $f\colon A\rightarrow C, g\colon B\rightarrow C$を射とする。$f$と$g$の **ファイバー積** （fiber product）は次の普遍性で定義される。

- $A\underset{f, C, g}{\prod}B\in\mathscr{C}$は対象、$p\colon A\underset{f, C, g}{\prod}B\rightarrow A$及び$q\colon A\underset{f, C, g}{\prod}B\rightarrow B$は射であり、$f\circ p=g\circ q$を満たす。
- $X\in\mathscr{C}$が対象で射$u\colon X\rightarrow A, v\colon X\rightarrow B$が$f\circ u=g\circ v$を満たすとき、唯一つの射$h\colon X\rightarrow A\underset{f, C, g}{\prod}B$が存在して$u=p\circ h, v=q\circ h$を満たす。

<p align=center><img src="pics/universality_fiberprod.svg" height="160"></p>

__定義__ $f\colon C\rightarrow A, g\colon C\rightarrow B$を射とする。$f$と$g$の **余ファイバー積** （fiber coproduct）は次の普遍性で定義される。

- $A\underset{f, C, g}{\coprod}B\in\mathscr{C}$は対象、$p\colon A\rightarrow A\underset{f, C, g}{\coprod}B$及び$q\colon B\rightarrow A\underset{f, C, g}{\coprod}B$は射であり、$p\circ f=q\circ g$を満たす。
- $X\in\mathscr{C}$が対象で射$u\colon A\rightarrow X, v\colon B\rightarrow X$が$u\circ f=v\circ g$を満たすとき、唯一つの射$h\colon A\underset{f, C, g}{\coprod}B\rightarrow X$が存在して$u=h\circ p, v=h\circ q$を満たす。

<p align=center><img src="pics/universality_fibercoprod.svg" height="160"></p>

> ファイバー積は **引き戻し** （pull-back）、余ファイバー積は **押し出し** （push-forward）とも呼ばれる。それぞれ射が明らかな場合は、$f, g$を省略して$A\prod_{C}B$や$A\coprod_{C}B$と表すこともあるが、いずれにせよ直積の記号と被るので紛らわしい。そこで図式に以下のような名前を付けることで解決することが多い。

__定義__ 圏$\mathscr{C}$において以下の図式を考える。

<p align=center><img src="pics/universality_cartesian.svg" height="100"></p>

- $(A, f, g)$が$p$と$q$のファイバー積であるとき、図式は **カルテシアン** （cartesian）であるという。
- $(D, p, q)$が$f$と$g$の余ファイバー積であるとき、図式は **コカルテシアン** （cocartesian）であるという。



## 普遍性を持つ圏

__命題__ 以上に述べた普遍性により定義されるもの（終対象、始対象、直積、余直積、イコライザ、コイコライザ、ファイバー積、余ファイバー積）はそれぞれ同型を除いて一意的である。

（証明）終対象や始対象に関する一意性の証明と同様である。普遍性を満たすものが複数あれば、普遍性より互いに「唯一つの射」が定まり、それらの合成は自分自身への「唯一つの射」となる。恒等射もまた自分自身への「唯一つの射」であることから両者は一致し、故に普遍性を満たすもの同士は同型となる。$\square$

圏$\mathscr{C}$に対して、以上の概念が常に定義されるとき、$\mathscr{C}$はその普遍性を持つという。例えば終対象が存在する圏は、終対象を持つという。任意の直積が存在するとき、$\mathscr{C}$は直積を持つという。添え字集合の範囲限定して、有限個の直積が存在するとき、$\mathscr{C}$は有限直積を持つという。可算個の場合も同様とする。

> TODO








<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% universality_terminal.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[r, dashed, "\exists 1"] & T
\end{tikzcd}
```

```latex
% universality_initial.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
I \arrow[r, dashed, "\exists 1"] & T
\end{tikzcd}
```

```latex
% universality_2prod.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& X \arrow[ld, "\circlearrowright", "f"'] \arrow[rd, "g", "\circlearrowright"'] \arrow[d, dashed, "h"] & \\
A & A\prod B \arrow[l, "p"] \arrow[r, "q"'] & B
\end{tikzcd}
```

```latex
% universality_prod.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[rd, "f_{j}", "\circlearrowright"'] \arrow[d, dashed, "h"'] & \\
\displaystyle \prod_{i\in I}A_{i} \arrow[r, "p_{j}"'] & A_{j}
\end{tikzcd}
```

```latex
% universality_coprod.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X & \\
\displaystyle \coprod_{i\in I}A_{i} \arrow[u, dashed, "h"] & A_{j} \arrow[l, "p_{j}"] \arrow[lu, "\circlearrowright", "f_{j}"']
\end{tikzcd}
```

```latex
% universality_equalizer.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
E(f, g) \arrow[r, "e"] & A \arrow[r, shift left, "f"] \arrow[r, shift right, "g"'] & B \\
X \arrow[u, dashed, "h"] \arrow[ru, "\circlearrowright", "x"'] & &
\end{tikzcd}
```

```latex
% universality_coequalizer.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
A \arrow[r, shift left, "f"] \arrow[r, shift right, "g"'] & B \arrow[r, "q"] \arrow[rd, "\circlearrowright", "x"'] & Q(f, g) \arrow[d, dashed, "h"] \\
& & X
\end{tikzcd}
```

```latex
% universality_fiberprod.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[rrd, bend left, "v"] \arrow[rdd, bend right, "u"'] \arrow[rd, dashed, "h"] & & \\
& A\prod_{f, C, g}B \arrow[d, "p"'] \arrow[r, "q"] & B \arrow[d, "g"] \\
& A \arrow[r, "f"'] & C
\end{tikzcd}
```

```latex
% universality_fibercoprod.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
C \arrow[d, "f"'] \arrow[r, "g"] & B \arrow[d, "q"] \arrow[rdd, bend left, "v"] & \\
A \arrow[r, "p"'] \arrow[rrd, bend right, "u"'] & \displaystyle A\coprod_{f, C, g}B \arrow[rd, dashed, "h"] & \\
& & X
\end{tikzcd}
```

```latex
% universality_cartesian.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
A \arrow[d, "f"'] \arrow[r, "g"] & B \arrow[d, "q"] \\
C \arrow[r, "p"'] & D
\end{tikzcd}
```

</details>
