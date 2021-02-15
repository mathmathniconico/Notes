# 圏

小説やドラマの人物相関図を思い浮かべて欲しい。物語の主人公からは多くの矢印が出ているだろう。ヒロインとは相互に矢印があるはずだ。矢印を辿った先の結末には悪役が控えているかもしれない。一方で誰からも矢印のない謎の人物がいる。彼はきっと重要な役割を演じるはずだ。また続編では異なる相関図が描かれるだろう。あるいは別の物語では？　色々な図があれば、似ているかそうでないかを議論することができる。そこには幾何学が存在する。

圏論とは、私の感覚で言えば「点と矢印の幾何学」である。点は考えている「何か」を表しており、矢印は点と点の間にある関連性を表している。矢印は関連性を模式的に表したものだが、もちろん何でもよいという訳ではない。$A$が$B$と関連し、$B$が$C$と関連するなら、$A$が$C$に関連していなければならない。考え方は非常にシンプルであり、だからこそ応用範囲は幅広く、豊かな数学理論を展開することができる。

以下ではまず圏を定義し、最も基本的な概念である同型について述べる。抽象論が続くため例と一緒に紹介するべきだが、煩雑になってしまうので別に纏める。適宜参照して欲しい。




## 圏の定義、対象の同型

以下で構成される組$\mathscr{C}=(\mathrm{Ob}(\mathscr{C}), \mathrm{Mor}(\mathscr{C}), \mathrm{dom}, \mathrm{cod}, \circ )$を考える。

- $\mathrm{Ob}(\mathscr{C})$は **対象** （object）からなる集まりである。
- $\mathrm{Mor}(\mathscr{C})$は **射** （morphism）からなる集まりである。
- 射$f$について、$f$の **始域** （domain）と呼ばれる対象$\mathrm{dom}(f)$が唯一つ定まっている。
- 射$f$について、$f$の **終域** （codomain）と呼ばれる対象$\mathrm{cod}(f)$が唯一つ定まっている。
- 射$f, g$について、$\mathrm{cod}(f)=\mathrm{dom}(g)$のとき **合成** （composition）と呼ばれる射$g\circ f$が定義され、$\mathrm{dom}(g\circ f)=\mathrm{dom}(f), \mathrm{cod}(g\circ f)=\mathrm{cod}(g)$を満たす。

ここで記法に関するいくつかの注意点を述べる。

- $X$が$\mathscr{C}$の対象であることを$X\in\mathscr{C}$と略記する。
- 射$f$について、$\mathrm{dom}(f)=X, \mathrm{cod}(f)=Y$のとき$f\colon X\rightarrow Y$と書き、$f$は$X$から$Y$への射という。
- 対象$X, Y\in\mathscr{C}$について、$X$から$Y$への射全体を$\mathrm{Mor}_{\mathscr{C}}(X, Y)$で表す。添え字の$\mathscr{C}$は適宜省略される。

> $\mathrm{Mor}_{\mathscr{C}}(X, Y)$は$\mathscr{C}(X, Y)$と書く場合もある。この$\mathrm{Mor}_{\mathscr{C}}(X, Y)$たちは非交叉である。

__定義__ 上記の組$\mathscr{C}$が以下を満たすとき **圏**（category）と呼ぶ。何れも合成が定義される状況を考えている。

- 任意の対象$X$に対して恒等射$\mathrm{id}_{X}\in\mathrm{Mor}(X, X)$が存在し、射$f, g$について$\mathrm{id}_{X}\circ f=f, g\circ\mathrm{id}_{X}=g$が成り立つ。
- 射$f, g, h$について$(f\circ g)\circ h=f\circ(g\circ h)$が成り立つ。

> 「集まり」とやや曖昧な表現をしたのは、上記の定義は通常の数学、すなわち集合論の範疇に収まらないものだからである。数理論理的には$\mathrm{Ob}(\mathscr{C})$も$\mathrm{Mor}(\mathscr{C})$も真クラスであり、$\mathrm{dom}\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$や$\mathrm{cod}\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$はクラス間の写像となる。更に言えば対象や射そのものも集合である必要はない。もちろん「宇宙」を定義し、その中で圏論を展開することも可能（というよりもそれが正統）だが、このノートでは（私が分からないので）深入りせず、概念的な理解に留めることにする。

圏を集合論の範疇で考えることは有益である。

> 写像$f\colon B\rightarrow A, g\colon C\rightarrow A$について、ファイバー積$B\underset{f, A, g}{\times}C$とは、集合$\lbrace ( b, c )\in B\times C : f(b)=g(c) \rbrace$のことである。

__定義__ $\mathrm{Ob}(\mathscr{C}), \mathrm{Mor}(\mathscr{C})$を集合、$\mathrm{dom}, \mathrm{cod}\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$は写像とする。更に$\circ$は然るべき条件を満たす写像

$$
\circ\colon\mathrm{Mor}(\mathscr{C})\underset{\mathrm{dom}, \mathrm{Ob}(\mathscr{C}), \mathrm{cod}}{\times}\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Mor}(\mathscr{C})
$$

とする。このとき集合の組$\mathscr{C}$を **小さい圏** （small category）と呼ぶ。

> 小さい圏においては全てが集合なので、心が落ち着くかと思う。従って基本的には小さい圏を考えればよいが、「言葉としての圏論」を目指すにはやや不足がある。例えば集合を対象、写像を射とする圏$\mathbf{Set}$を考える。集合全体は集合でないため、$\mathrm{Ob}(\mathbf{Set})$やそれを含む$\mathrm{Mor}(\mathbf{Set})$は集合でない。$\mathbf{Set}$を扱えないのは余りにも不便だ。しかし我々は対象全体には興味がなく、点と点の関連性、すなわち射に興味があることを思い出そう。であるならば、射について語ることが可能なら十分である。

__定義__ $\mathscr{C}$を圏とする。任意の対象$X, Y$に対して$\mathrm{Mor}_{\mathscr{C}}(X, Y)$が集合のとき、$\mathscr{C}$は **局所的に小さい** （locally small）という。そうでないときは **大きい** （big）という。

圏を定義したので、次にその圏における「等しい」という概念について考える。射つまり関連性によって対象を記述するというのが圏論的な考え方である。故にどのような対象を同じものとしてみなすか、もまた射の言葉で記述される。

__命題__ 恒等射$\mathrm{id}_{X}$は一意的である。

（証明）$i, j\colon X\rightarrow X$が恒等射の性質を満たすなら、$i=i\circ j=j$より等しい。$\square$

__定義__ 射$f\colon X\rightarrow Y$が **同型** （isomorphism）であるとは、ある$g\colon Y\rightarrow X$が存在して$g\circ f=\mathrm{id}_{X}, f\circ g=\mathrm{id}_{Y}$が成り立つことをいう。このとき$X$と$Y$は同型といい、$X\simeq Y$と表す。このとき$g$もまた同型であり、更に一意的である。そこで$g$を$f^{-1}$と表し$f$の **逆** （inverse）と呼ぶ。




## 反対圏、積の圏、スライス圏

ここでは与えられた圏から別の圏を作る方法を3つ紹介する。これらは基本的なものだが、圏論において重要な役割を担う。

__定義__ $\mathscr{C}$を圏とする。圏$\mathscr{C}^{\mathrm{op}}$を以下で定める。これを$\mathscr{C}$の **反対圏** （opposite category）と呼ぶ。

- 対象は$\mathscr{C}$の対象とする。つまり$\mathrm{Ob}(\mathscr{C}^{\mathrm{op}})=\mathrm{Ob}(\mathscr{C})$である。
- $X, Y\in\mathscr{C}$とする。$f\colon X\leftarrow Y$が$\mathscr{C}$における射のとき、$f^{\mathrm{op}}\colon X\rightarrow Y$と表して$\mathscr{C}^{\mathrm{op}}$における$X$から$Y$への射とする。つまり$\mathrm{Mor}_{\mathscr{C}^{\mathrm{op}}}(X, Y)=\mathrm{Mor}_{\mathscr{C}}(Y, X)$である。

__定義__ $\mathscr{A}, \mathscr{B}$を圏とする。圏$\mathscr{A}\times\mathscr{B}$を以下で定める。これを$\mathscr{A}$と$\mathscr{B}$の **積の圏** （product of categories）と呼ぶ。

- 対象はそれぞれの対象の組とする。つまり$A\in\mathscr{A}, B\in\mathscr{B}$について$(A, B)\in\mathscr{A}\times\mathscr{B}$とする。
- 射もそれぞれの射の組とする。つまり$\mathscr{A}$の射$f\colon A\rightarrow X$と$\mathscr{B}$の射$g\colon B\rightarrow Y$によって$(f, g)\colon (A, B)\rightarrow (X, Y)$を$\mathscr{A}\times\mathscr{B}$の射とする。

__定義__ $\mathscr{C}$を圏、$X\in\mathscr{C}$とする。圏$\mathscr{C}/X$を以下で定める。これを$\mathscr{C}$の$X$上の **スライス圏** （slice of category）と呼ぶ。

- 対象は$A\in\mathscr{C}$と$f\colon A\rightarrow X$の組$(A, f)$である。
- $f\colon A\rightarrow X, g\colon B\rightarrow X$とする。射$h\colon A\rightarrow B$が$g\circ h=f$を満たすとき、これをスライス圏における射$h\colon (A, f)\rightarrow (B, g)$とする。

<p align=center><img src="pics/category_01.svg" height="100"></p>

> $X$上のスライス圏は$X$への射全体のことであり、「$X$の上方の対象から成る圏」とも言われる。同様に$X$から出る射を考えることで「下方の対象から成る圏」を考えることもできるが、これは反対圏のスライス圏$\mathscr{C}^{\mathrm{op}}/X$のことである。




## 射のみを用いた圏の定義

> 参考：[single-sorted definition of a category](https://ncatlab.org/nlab/show/single-sorted+definition+of+a+category) in nLab.

対象$X$を恒等射$\mathrm{id}_{X}$と同一視することで、圏を射の言葉で記述することができる。まず次の状況を考える。

- $\mathscr{A}$は射からなる集まりである。
- $s, t\colon\mathscr{A}\rightarrow\mathscr{A}$は対応とする。それぞれsource、targetと呼ぶ。
- 射の合成$g\circ f$は$sg=tf$のときのみ定義される。

以下を満たす組$(\mathscr{A}, s, t, \circ)$を考える。$f, g, h$は射とする。合成は等式の一方が定義されるなら他方も定義されることに注意する。

- $ssf=sf=tsf, ttf=tf=stf$が成り立つ。
- $s(g\circ f)=sf, t(g\circ f)=tg$が成り立つ。
- $f\circ sf=f, tf\circ f=f$が成り立つ。
- $(h\circ g)\circ f=h\circ(g\circ f)$が成り立つ。

このとき上記は圏と同等である。

まず射$x$に対して$sx=x$と$tx=x$は同値である。実際$sx=x$なら$tx=t(sx)=sx=x$であり、逆も同様である。このとき$x\in\mathrm{Ob}$と書く。

__命題__ $x$を射とする。TFAE

- $x\in\mathrm{Ob}$である。
- 任意の射$f, g$に対し、合成が定義できるなら$f\circ x=f$及び$x\circ g=g$が成り立つ。

（証明）$x\in\mathrm{Ob}$とする。$f\circ x$が定義できるなら$sf=tx=x$となる。故に$f\circ x=f\circ sf=f$となる。$x\circ g$に対しても同様に$x=sx=tg$より$x\circ g=tg\circ g=g$を得る。

逆に$x$が下の条件を満たすとする。$sx=t(sx)$より$x\circ sx$は定義できるので$x\circ sx=x$が成り立つ。仮定より$x\circ sx=sx$だから$sx=x$である。$\square$

下は恒等射としての性質であり、この意味で対象と恒等射は同一視される。




<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% category_01.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
A \arrow[dr, "f"'] \arrow[rr, "h"] &  \arrow[d, phantom, "\circlearrowright"] & B \arrow[dl, "g"] \\
& X &
\end{tikzcd}
```

</details>

<!--
```latex {cmd}
\documentclass{standalone}
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
\begin{document}

\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[d, "\rho"'] & GFX \arrow[r, "t_{X}", "\simeq"'] \arrow[d, "GF\rho"'] \arrow[dr, phantom, "\circlearrowright"] & X \arrow[d, "\rho"] \\
Y & GFY \arrow[r, "\simeq", "t_{Y}"'] & Y &
\end{tikzcd}

\end{document}
```
-->



