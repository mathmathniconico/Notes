
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

<p align=center><img src="pics/functor_01.svg" height="100"></p>

この図式が成り立つとき$t=(t_{X})_{X\in\mathscr{A}}$は自然であるという。圏論の文脈で「自然」というときは、だいたいこの意味である。

函手$F$に対して$(\mathrm{id}_{F})_{X}=\mathrm{id}_{FX}\colon FX\rightarrow FX$と定めると恒等自然変換$\mathrm{id}_{F}\colon F\rightarrow F$を定義することができる。また自然変換$t\colon F\rightarrow G, s\colon G\rightarrow H$に対し、$(s\circ t)_{X}=s_{X}\circ t_{X}\colon FX\rightarrow GX\rightarrow HX$と定めることで、自然変換の合成$s\circ t$を定義することができる。これらは圏の定義の恒等射の性質や合成の結合性を満たす。つまり函手を対象として自然変換を射とする圏を考えることができる。

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。以下で構成される圏を$\mathscr{A}$から$\mathscr{B}$への **函手圏** と呼び$\mathbf{Funct}(\mathscr{A}, \mathscr{B})$で表す。
- 対象は$\mathscr{A}$から$\mathscr{B}$への函手とする。
- 函手$F, G\colon\mathscr{A}\rightarrow\mathscr{B}$について、$F$から$G$への射は$F$から$G$への自然変換とする。

> 圏論の動機の一つに、元の概念を廃し、射によって対象間を記述するというものがある。この観点からすれば、二つの圏を測るのは「圏の圏」において同型を定める一つの函手ではなく、圏の間の函手全体つまり函手圏である。

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。函手$F\colon\mathscr{A}\rightarrow\mathscr{B}$が **圏同値** （equivalence）であるとは、ある函手$G\colon\mathscr{B}\rightarrow\mathscr{A}$が存在して$G\circ F\simeq\mathrm{id}_{\mathscr{A}}$と$F\circ G\simeq\mathrm{id}_{\mathscr{B}}$がそれぞれの函手圏において成り立つことをいう。このとき$\mathscr{A}$と$\mathscr{B}$は圏同値であるといい、$\mathscr{A}\approx\mathscr{B}$と表す。

$G\circ F\simeq\mathrm{id}_{\mathscr{A}}$は函手圏$\mathbf{Funct}(\mathscr{A}, \mathscr{A})$における同型である。即ち同型となる自然変換$t\colon G\circ F\rightarrow\mathrm{id}_{\mathscr{A}}$が存在する。言い換えると対象$X\in\mathscr{A}$に対して同型射$t_{X}\colon GFX\xrightarrow{\simeq} X$が存在して、$\rho\colon X\rightarrow Y$について$\rho\circ t_{X}=t_{Y}\circ GF\rho$が成り立つ。つまり以下の図式は可換である。

<p align=center><img src="pics/functor_02.svg" height="100"></p>


<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% functor_01.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[d, "\rho"'] & FX \arrow[r, "t_{X}"] \arrow[d, "F\rho"'] \arrow[dr, phantom, "\circlearrowright"] & GX \arrow[d, "G\rho"] \\
Y & FY \arrow[r, "t_{Y}"'] & GY
\end{tikzcd}
```

```latex
% functor_02.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[d, "\rho"'] & GFX \arrow[r, "t_{X}", "\simeq"'] \arrow[d, "GF\rho"'] \arrow[dr, phantom, "\circlearrowright"] & X \arrow[d, "\rho"] \\
Y & GFY \arrow[r, "\simeq", "t_{Y}"'] & Y
\end{tikzcd}
```

</details>