# 圏と函手

## 圏の定義

以下で構成される組$\mathscr{C}=(\mathrm{Ob}(\mathscr{C}), \mathrm{Mor}(\mathscr{C}), \mathrm{dom}, \mathrm{cod}, \circ )$を考える。

- $\mathrm{Ob}(\mathscr{C})$は集合である。この要素を **対象** （object）と呼ぶ。
- $\mathrm{Mor}(\mathscr{C})$は集合である。この要素を **射** （morphism）と呼ぶ。
- $\mathrm{dom}\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$は写像である。射$f$について$\mathrm{dom}(f)$を$f$の始域（domain）と呼ぶ。
- $\mathrm{cod}\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$は写像である。射$f$について$\mathrm{cod}(f)$を$f$の終域（codomain）と呼ぶ。
- $\mathrm{dom}(g)=\mathrm{cod}(f)$を満たす射$f, g$について合成（composition）と呼ばれる射$g\circ f$が定義され、$\mathrm{dom}(g\circ f)=\mathrm{dom}(f), \mathrm{cod}(g\circ f)=\mathrm{cod}(g)$を満たす。

集合のファイバー積を用いるなら、$\circ$は然るべき条件を満たす写像

$$
\circ\colon\mathrm{Mor}(\mathscr{C})\underset{\mathrm{dom}, \mathrm{Ob}(\mathscr{C}), \mathrm{cod}}{\times}\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Mor}(\mathscr{C})
$$

である。

- $X$が$\mathscr{C}$の対象であること（$X\in\mathrm{Ob}(\mathscr{C})$）を、省略して$X\in\mathscr{C}$と書く。
- 射$f\in\mathrm{Mor}(\mathscr{C})$について$\mathrm{dom}(f)=X, \mathrm{cod}(f)=Y$のとき、$f$は$X$から$Y$への射であるといい$f\colon X\rightarrow Y$と書く。
- 対象$X, Y\in\mathscr{C}$について、$X$から$Y$への射全体を$\mathrm{Mor}_{\mathscr{C}}(X, Y)$で表す。添え字の$\mathscr{C}$は適宜省略される。

- $\mathrm{Mor}(\mathscr{C})=\bigsqcup_{X, Y\in\mathscr{C}}\mathrm{Mor}(X, Y)$は非交叉和である。

> 圏の定義も色々あって、最後の非交叉性が成り立たない場合もあるが、それだと問題が起こるらしい。詳しくは知らない。

__定義__ 上記の組$\mathscr{C}$が以下を満たすとき **圏**（category）と呼ぶ。

- 任意の対象$X$について恒等射$\mathrm{id}_{X}\in\mathrm{Mor}(X, X)$が存在し、合成を定義できる射$f, g$について$\mathrm{id}_{X}\circ f=f, g\circ\mathrm{id}_{X}=g$が常に成り立つ。
- 合成を定義できる射$f, g, h$について$(f\circ g)\circ h=f\circ(g\circ h)$が成り立つ。

> 上の定義は一般に「小さい圏」と呼ばれるものの定義である。$\mathrm{Ob}(\mathscr{C})$が真クラス（従って$\mathrm{Mor}(\mathscr{C})$も真クラス）でも同様な概念を考察できるが、これは「大きな圏」と呼ばれる。その中でも任意の対象$X, Y$について$\mathrm{Mor}(X, Y)$が集合である場合は「局所的に小さい圏」と呼ぶ。しかし「大きな圏」を考慮すると「大きな圏の集まり」を議論する必要があり、それは数理論理学の範疇であり筆者も詳しくない。従って以下やこれ以外のノートにおいて単に「圏」と呼ぶときは基本的に「小さい圏」を考え、そうでない場合も記述を簡単にするための「言葉としての圏論」を扱う。あるいは「大きな圏」をリストとして挙げてしまうこともできる。例えば集合の圏$\mathbf{Sets}$、アーベル群の圏$\mathbf{Ab}$といったように、必要に応じて「大きな圏」をリストに加えてしまう。

- $\mathrm{id}_{X}$は一意的である。

__例__ 群$G$について圏$\circlearrowright^{G}$を以下で定める。

- $\mathrm{Ob}(\circlearrowright^{G})=\lbrace \ast \rbrace$として$\mathrm{Mor}(\ast, \ast)=G$とする。
- 射の合成は$g\circ f=gf$とする。

単位元は恒等射であり、演算の結合性より合成の結合性も成り立つ。この圏には名前は付いていないが、単対象圏の一種である。

次に同型を定義する。「何を等しいと思うか」は数学の様々な場面で重要な概念だが、圏論においては恒等射によって特徴付けられる。

__定義__ 射$f\colon X\rightarrow Y$が **同型** （isomorphism）であるとは、ある$g\colon Y\rightarrow X$が存在して$g\circ f=\mathrm{id}_{X}, f\circ g=\mathrm{id}_{Y}$が成り立つことをいう。このとき$X$と$Y$は同型といい、$X\simeq Y$と表す。

- $f$が同型のとき、上の$g$もまた同型であり、更に$g$は一意に定まる。これを$f^{-1}$と表し、$f$の逆（inverse）と呼ぶ。
- 全ての射が同型であるときgroupoid（群っぽい）という。群$G$について$\circlearrowright^{G}$はgroupoidである。

__定義__ 圏$\mathscr{A}, \mathscr{B}$について、$\mathscr{A}$と$\mathscr{B}$の積という圏$\mathscr{A}\times\mathscr{B}$を以下で定める。

- 対象の集合は$\mathrm{Ob}(\mathscr{A}\times\mathscr{B}):=\mathrm{Ob}(\mathscr{A})\times\mathrm{Ob}(\mathscr{B})$とする。
- 射の集合は$\mathrm{Mor}_{\mathscr{A}\times\mathscr{B}}((X, Y), (Z, W)):=\mathrm{Mor}_{\mathscr{A}}(X, Z)\times\mathrm{Mor}_{\mathscr{B}}(Y, W)$とする。


## 函手、自然変換、圏同値

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。$\mathscr{A}$から$\mathscr{B}$への **函手** （functor）$F\colon\mathscr{A}\rightarrow\mathscr{B}$は以下で構成される。

- 対象$X\in\mathscr{A}$について対象$FX\in\mathscr{B}$が定義されている。
- 対象$X, Y\in\mathscr{A}$及び射$f\colon X\rightarrow Y$について射$Ff\colon FX\rightarrow FY$が定義されている。写像$f\mapsto Ff$を$F_{X, Y}$で表す。
- 以上は全て射の合成と恒等射に関してcompatibleである。つまり$F(f\circ g)=Ff\circ Fg$であり、$F\mathrm{id}_{X}=\mathrm{id}_{FX}$である。

> 函手は、対象の間の写像と射の間の写像の組として書くこともできる。

- 函手は同型を保存する。つまり$X\simeq Y$なら$FX\simeq FY$である。

例えば対象も射も同じものを対応させることで恒等函手$\mathrm{id}_{\mathscr{C}}\colon\mathscr{C}\rightarrow\mathscr{C}$を定義できる。また函手$F\colon\mathscr{A}\rightarrow\mathscr{B}$と函手$G\colon\mathscr{B}\rightarrow\mathscr{C}$について、函手の合成$G\circ F\colon\mathscr{A}\rightarrow\mathscr{C}$を定義することができる。これらは圏の定義の恒等射の性質や合成の結合性を満たす。つまり厳密には圏ではないものの、圏を対象とみなし函手を射とみなした、いわば「圏の圏」を考えることができる。ここでの「同型」について考えてみよう。

__定義__ 圏$\mathscr{A}, \mathscr{B}$について、函手$F\colon\mathscr{A}\rightarrow\mathscr{B}$及び函手$G\colon\mathscr{B}\rightarrow\mathscr{A}$が$G\circ F=\mathrm{id}_{\mathscr{A}}$及び$F\circ G=\mathrm{id}_{\mathscr{B}}$を満たすとき、$\mathscr{A}$と$\mathscr{B}$は圏同型といい、$\mathscr{A}\simeq\mathscr{B}$と表す。

> しかし圏同型は条件として強すぎる。というのも圏同型は、対象と対象の間に完全な一対一の対応を要請し、また函手の間にも完全な一対一の対応を要請する。これは射の中身は別として合成という名の操作が恒等射でさえあれば良いという対象間の同型とは異なり、集合において全単射を構成するようなものであり、とても窮屈な概念である。実際に実用上も圏同型が言えることは殆ど無く、一方で同型でない圏が「同じように見える」ことに真の価値がある。

__定義__ $F, G\colon \mathscr{A}\rightarrow\mathscr{B}$を函手とする。$F$から$G$への **自然変換** （natural transformation）$t\colon F\rightarrow G$は以下で構成される。

- 対象$X\in\mathscr{A}$について射$t_{X}\colon FX\rightarrow GX$が定義されている。
- 対象$X, Y\in\mathscr{A}$及び射$\rho\colon X\rightarrow Y$に対し$G\rho\circ t_{X}=t_{Y}\circ F\rho$が成り立つ。つまり以下の図式は可換となる。

<p align=center><img src="pics/category_01.svg" height="100"></p>

この図式が成り立つとき$t=(t_{X})_{X\in\mathscr{A}}$は自然であるという。圏論の文脈で「自然」というときは、だいたいこの意味である。

函手$F$に対して$(\mathrm{id}_{F})_{X}=\mathrm{id}_{FX}\colon FX\rightarrow FX$と定めると恒等自然変換$\mathrm{id}_{F}\colon F\rightarrow F$を定義することができる。また自然変換$t\colon F\rightarrow G, s\colon G\rightarrow H$に対し、$(s\circ t)_{X}=s_{X}\circ t_{X}\colon FX\rightarrow GX\rightarrow HX$と定めることで、自然変換の合成$s\circ t$を定義することができる。これらは圏の定義の恒等射の性質や合成の結合性を満たす。つまり函手を対象として自然変換を射とする圏を考えることができる。

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。以下で構成される圏を$\mathscr{A}$から$\mathscr{B}$への **函手圏** と呼び$\mathbf{Funct}(\mathscr{A}, \mathscr{B})$で表す。
- 対象は$\mathscr{A}$から$\mathscr{B}$への函手とする。
- 函手$F, G\colon\mathscr{A}\rightarrow\mathscr{B}$について、$F$から$G$への射は$F$から$G$への自然変換とする。

> 圏論の動機の一つに、元の概念を廃し、射によって対象間を記述するというものがある。この観点からすれば、二つの圏を測るのは「圏の圏」において同型を定める一つの函手ではなく、圏の間の函手全体つまり函手圏である。

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。函手$F\colon\mathscr{A}\rightarrow\mathscr{B}$が **圏同値** （equivalence）であるとは、ある函手$G\colon\mathscr{B}\rightarrow\mathscr{A}$が存在して$G\circ F\simeq\mathrm{id}_{\mathscr{A}}$と$F\circ G\simeq\mathrm{id}_{\mathscr{B}}$がそれぞれの函手圏において成り立つことをいう。このとき$\mathscr{A}$と$\mathscr{B}$は圏同値であるといい、$\mathscr{A}\approx\mathscr{B}$と表す。

$G\circ F\simeq\mathrm{id}_{\mathscr{A}}$は函手圏$\mathbf{Funct}(\mathscr{A}, \mathscr{A})$における同型である。即ち同型となる自然変換$t\colon G\circ F\rightarrow\mathrm{id}_{\mathscr{A}}$が存在する。言い換えると対象$X\in\mathscr{A}$に対して同型射$t_{X}\colon GFX\xrightarrow{\simeq} X$が存在して、$\rho\colon X\rightarrow Y$について$\rho\circ t_{X}=t_{Y}\circ GF\rho$が成り立つ。つまり以下の図式は可換である。

<p align=center><img src="pics/category_02.svg" height="100"></p>


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
X \arrow[d, "\rho"'] & FX \arrow[r, "t_{X}"] \arrow[d, "F\rho"'] \arrow[dr, phantom, "\circlearrowright"] & GX \arrow[d, "G\rho"] \\
Y & FY \arrow[r, "t_{Y}"'] & GY
\end{tikzcd}
```

```latex
% category_02.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[d, "\rho"'] & GFX \arrow[r, "t_{X}", "\simeq"'] \arrow[d, "GF\rho"'] \arrow[dr, phantom, "\circlearrowright"] & X \arrow[d, "\rho"] \\
Y & GFY \arrow[r, "\simeq", "t_{Y}"'] & Y
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



