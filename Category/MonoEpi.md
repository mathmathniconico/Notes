
# モノ射とエピ射



## 定義

__定義__ 射$f\colon A\rightarrow B$について以下は同値である。このとき$f$は **モノ射** （monomorphism）であるという。

- 任意の射$g, h\colon X\rightarrow A$に対し、$f\circ g=f\circ h$なら$g=h$が成り立つ。
- 図式$f\circ\mathrm{id}_{A}=f\circ\mathrm{id}_{A}$はカルテシアンである。つまり

<p align=center><img src="pics/mono_01.svg" height="100"></p>

はファイバー積である。

（証明）上を仮定する。$u\colon X\rightarrow A, v\colon X\rightarrow A$は$f\circ u=f\circ v$を満たすとする。仮定より$u=v$だから$u\colon X\rightarrow A$は図式を可換とする。

<p align=center><img src="pics/mono_02.svg" height="160"></p>

一方で$h\colon X\rightarrow A$が図式を可換とするなら$u=\mathrm{id}_{A}\circ h=h$でなければならない。従ってファイバー積の普遍性を満たす。$\square$

モノ射の双対概念がエピ射である。

__定義__ 射$f\colon A\rightarrow B$に対し、以下は同値である。このとき$f$は **エピ射** （epimorphism）であるという。

- 任意の射$g, h\colon B\rightarrow X$に対し、$g\circ f=h\circ f$なら$g=h$が成り立つ。
- 図式$\mathrm{id}_{B}\circ f=\mathrm{id}_{B}\circ f$はコカルテシアンである。つまり

<p align=center><img src="pics/epi_01.svg" height="100"></p>

は余ファイバー積である。

明らかに、同型はモノかつエピである。しかし逆は一般に成り立たない。



## 基本的性質

__命題__　以下が成り立つ。

- モノ射の合成はモノ射である。つまり$f\colon A\rightarrow B, g\colon B\rightarrow C$をモノ射とすると$g\circ f$もモノ射である。
- $f, g\colon A\rightarrow B$のイコライザ$e\colon E\rightarrow A$はモノ射である。
- モノ射はpull-backで保たれる。従って右随伴で保たれる。

（証明）$\square$

> TODO: split/retract, external axiom of choice, subobject classifier, image factorization



## 四つの視点

あまり意識されることはないが、個人的に重要だと思う視点を書いておく。

__定義__ $\mathcal{K}$は圏$\mathscr{C}$の対象からなる部分クラスとする。

- $X\in \mathcal{K}$について$X$へのモノ射を集めて$S\mathcal{K}$と書く。これを$\mathcal{K}$の下部（Substruction）という。
- $X\in \mathcal{K}$について$X$へのエピ射を集めて$A\mathcal{K}$と書く。これを$\mathcal{K}$の類似（Analogous）という。
- $X\in \mathcal{K}$について$X$からのモノ射を集めて$E\mathcal{K}$と書く。これを$\mathcal{K}$の拡大（Extension）という。
- $X\in \mathcal{K}$について$X$からのエピ射を集めて$H\mathcal{K}$と書く。これを$\mathcal{K}$の相同（Homologous）という。

特に$\mathcal{K}$が$X\in\mathscr{C}$のみからなるとき、下部と類似は$\mathscr{C}/X$の部分圏であり、拡大と相同は$\mathscr{C}^{\mathrm{op}}/X$の部分圏である。

> これは普遍代数を意識した用語だが、もちろん一般的ではないので他所で使わないこと。

数学で現れる様々な概念は、上記あるいはそのサブクラスに関わることが多い。

- 下部の例：部分群、部分空間、部分対象
- 類似の例：層、ファイバーバンドル
- 拡大の例：体の拡大、埋め込み
- 相同の例：合同関係、商



<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% mono_01.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
A \arrow[r, "\mathrm{id}_{A}", "="'] \arrow[d, "=", "\mathrm{id}_{A}"'] & A \arrow[d, "f"] \\
A \arrow[r, "f"'] & B
\end{tikzcd}
```

```latex
% mono_01.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[rdd, bend right, "u"'] \arrow[rrd, bend left, "v"] \arrow[rd, "h"] & & \\
& A \arrow[r, "\mathrm{id}_{A}", "="'] \arrow[d, "=", "\mathrm{id}_{A}"'] & A \arrow[d, "f"] \\
& A \arrow[r, "f"'] & B
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
A \arrow[d, "f"'] \arrow[r, "f"] & B \arrow[d, "\mathrm{id}_{B}", "="'] \\
B \arrow[r, "=", "\mathrm{id}"'] & B
\end{tikzcd}

\end{document}
```
-->