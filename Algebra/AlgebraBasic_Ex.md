
# 例示：群と環

以下に群と環に関する例を挙げる。ここでは簡易的な記述に留め、後で用いる場合に改めてきちんと定義する。






## 環とイデアルの例

__例__ 以下は全て単位的環である。

- 整数全体$\mathbb{Z}$は可換環である。特に **有理整数環** と呼ばれる。
- 有理数、実数、複素数の全体$\mathbb{Q}, \mathbb{R}, \mathbb{C}$は体である。
- 単位的可換環$R$について$R$係数の多項式全体$R\lbrack x \rbrack$は多項式の和と積で可換環となる。これを多項式環という。
- 単位的可換環$R$について$n$次正方行列全体$\mathrm{M}(n; R)$は行列の和と積で環となる。これを全行列環という。特に$n\ge 2$なら非可換である。
- アーベル群$G$の自己準同型（$G$から$G$への群の準同型）全体$\mathrm{End}(G)$は$(f+g)(x):=f(x)+g(x)$及び$(f\cdot g)(x):=f(g(x))$により環となる。ゼロはゼロ写像$0(x):=0$、イチは恒等写像$1(x):=x$である。これも一般に非可換である。
- $R$を単位的可換環、$G$を群とする。$G$の元を基底とした$k$上のベクトル空間$k\lbrack G \rbrack$は環になる。ここで乗法は$a, b\in k$及び$g, h\in G$について$ag\cdot bh:=ab(gh)$で定める。これを **群環** （group ring）という。一般に非可換である。

> TODO イデアルの例、準同型の例、体の例



## 素イデアルの例

- 例えば$R=\mathbb{Z}$について$p\in\mathbb{Z}$が素数であることと$p\mathbb{Z}$が素イデアルとなることは同値になる。特に$6\mathbb{Z}$は素イデアルでない。実際$2\cdot 3=6\in 6\mathbb{Z}$だが$2, 3\notin 6\mathbb{Z}$である。


整環でない例

$\mathbb{Z}$は整域である。一方で$\mathbb{Z}\times\mathbb{Z}$は成分毎の演算で環となるが、
例えば$(1, 0)(0, 1)=(0, 0)$となるため整域ではない。$6\mathbb{Z}$は素イデアルでない。
これは$\mathbb{Z}/6\mathbb{Z}$が整域でないことからも分かる。実際
\[ (2+6\mathbb{Z})(4+6\mathbb{Z})=8+6\mathbb{Z}=2+6\mathbb{Z}=(2+6\mathbb{Z})(1+6\mathbb{Z}) \]
しかし$4+6\mathbb{Z}\neq 1+6\mathbb{Z}$なので$2+6\mathbb{Z}$を消去できない。