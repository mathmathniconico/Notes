
# 代数と余代数

「代数」という用語は多義的であるが、ここでは単位的可換環上の加群であって、その作用と両立する双線型かつ結合的な積を持ち、更に単位元を持つものを考える。これは加群の圏において圏論的に記述することができ、その双対概念として余代数を定義できる。

> 「環上の多元環」と呼ばれることもあるが、単位的可換環$R$を明示して「$R$代数」と呼ぶのが一番安全かもしれない。

以下$R$は単位的可換環とする。




## 代数（環上の多元環）

まずは標準的な定義を復習しておく。

__定義__ $A$を$R$加群とする。演算$\cdot\colon A\times A\rightarrow A$は以下を満たすとする。

- 両側分配的である。つまり$a, b, c\in A$について$(a+b)\cdot c=a\cdot c+b\cdot c$及び$a\cdot (b+c)=a\cdot b+a\cdot c$が成り立つ。
- $R$の作用と両立する。つまり$a, b\in A, r\in R$について$(ra)\cdot b=r(a\cdot b)=a\cdot (rb)$が成り立つ。
- 結合的である。つまり$a, b, c\in A$について$a\cdot (b\cdot c)=(a\cdot b)\cdot c$が成り立つ。
- 両側単位元を持つ。つまり$1_{A}\in A$が存在して、$a\in A$について$1_{A}\cdot a=a=a\cdot 1_{A}$が成り立つ。

このとき$A$を$R$上の代数、あるいは$R$代数と呼ぶ。

> 要するに$A$もまた環であって、単位元を保つ環準同型$f\colon R\rightarrow A$が与えられていると思ってよい。ただし$A$には$ra:=f(r)a$によって$R$の作用が入るが、$B$の積と両立するためには$f(R)$が$A$の中心$Z(A)$に含まれていなければならない。（つまり任意の$A$の元と可換でなければならない。）故に$R$代数全体はスライス圏$\mathbf{Ring}^{\mathrm{op}}/R$の部分圏となる。

これを圏論的に書き直してみよう。まず演算を写像$m\colon A\times A\rightarrow A$で表す。上2つの条件は$m$が$R$双線型であることを意味している。するとテンソル積の普遍性より加群の準同型$\overline{m}\colon A\otimes A\rightarrow A$が誘導される。逆に$\overline{m}$が与えられれば$A\times A\rightarrow A\otimes A$と合成して上2つの条件を満たす$m$が得られるため、この対応は一対一である。

次に$u\colon R\rightarrow A$を$r\mapsto r\cdot 1_{A}$と置く。このとき次が成り立つ。

- $\overline{m}\circ( \overline{m}\otimes\mathrm{id}_{A} )=\overline{m}\circ( \mathrm{id}_{A}\otimes\overline{m} )$が成り立つ。つまり以下の図式は可換である。

<p align=center><img src="pics/coalgebra_alg1.svg" height="150"></p>

- $\overline{m}\circ( u\otimes\mathrm{id}_{A} ), \overline{m}\circ( \mathrm{id}_{A}\otimes u )$が自明な同型と等しい。つまり以下の図式は可換である。

<p align=center><img src="pics/coalgebra_alg2.svg" height="100"></p>

> $R\otimes A\rightarrow A$は$r\otimes a\mapsto ra$によって与えられる。逆は$a\mapsto 1\otimes a$である。$A\otimes R\rightarrow A$についても同様だが、$A$は「左加群」なので$a\otimes r\mapsto ra$である。（$R$は可換環であることに注意せよ。）

逆に$u\colon R\rightarrow A$が上の図式を満たすとき、$\overline{m}$から誘導される$m$は結合的となり、また$u(1_{R})$は$m$に関する両側単位元となる。

__定義__ $A$を$R$加群とする。加群の準同型$\overline{m}\colon A\otimes A\rightarrow A, u\colon R\rightarrow A$は上の図式を満たすとする。このとき組$(A, \overline{m}, u)$を **代数** （algebra）と呼ぶ。




## 余代数

代数の双対概念が余代数である。

__定義__ $C$を$R$加群とする。加群の準同型$\Delta\colon C\rightarrow C\otimes C, \epsilon\colon C\rightarrow R$は以下を満たすとする。

- $(\Delta\otimes\mathrm{id}_{C})\circ\Delta=( \mathrm{id}_{C}\otimes\Delta )\circ\Delta$が成り立つ。つまり以下の図式は可換である。

<p align=center><img src="pics/coalgebra_def1.svg" height="150"></p>

- $( \epsilon\otimes\mathrm{id}_{C} )\circ\Delta, ( \mathrm{id}_{C}\otimes\epsilon )\circ\Delta$が自明な同型と等しい。つまり以下の図式は可換である。

<p align=center><img src="pics/coalgebra_def2.svg" height="100"></p>

このとき組$(C, \Delta, \epsilon)$を **余代数** （coalgebra）と呼ぶ。























<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% coalgebra_alg1.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& A\otimes A\otimes A \arrow[ld, "\overline{m}\otimes\mathrm{id}_{A}"'] \arrow[rd, "\mathrm{id}_{A}\otimes\overline{m}"] & \\
A\otimes A \arrow[rd, "\overline{m}"'] & & A\otimes A \arrow[ld, "\overline{m}"] \\
& A &
\end{tikzcd}
```

```latex
% coalgebra_alg2.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& A\otimes A \arrow[d, "\overline{m}"] & \\
R\otimes A \arrow[ru, "u\otimes\mathrm{id}_{A}"] \arrow[r, "\simeq"'] & A & A\otimes R \arrow[lu, "\mathrm{id}_{A}\otimes u"'] \arrow[l, "\simeq"]
\end{tikzcd}
```

```latex
% coalgebra_def1.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& C\otimes C\otimes C & \\
C\otimes C \arrow[ru, "\Delta\otimes\mathrm{id}_{C}"] & & C\otimes C \arrow[lu, "\mathrm{id}_{C}\otimes\Delta"'] \\
& C \arrow[lu, "\Delta"] \arrow[ru, "\Delta"'] &
\end{tikzcd}
```

```latex
% coalgebra_def2.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& C\otimes C \arrow[ld, "\epsilon\otimes\mathrm{id}_{C}"'] \arrow[rd, "\mathrm{id}_{C}\otimes\epsilon"] & \\
R\otimes C & C \arrow[u, "\Delta"] \arrow[l, "\simeq"] \arrow[r, "\simeq"'] & C\otimes R
\end{tikzcd}
```

</details>




```latex {cmd}
\documentclass{standalone}
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
\begin{document}

\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
& A\otimes A \arrow[d, "\overline{m}"] & \\
R\otimes A \arrow[ru, "u\otimes\mathrm{id}_{A}"] \arrow[r, "\simeq"'] & A & A\otimes R \arrow[lu, "\mathrm{id}_{A}\otimes u"'] \arrow[l, "\simeq"]
\end{tikzcd}

\end{document}
```


