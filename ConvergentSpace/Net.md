
# 有向ネット

__定義__ 集合$A$上の関係$\le$は以下を満たすとする。

- $a\in A$について$a\le a$である。（反射性）
- $a, b, c\in A$について$a\le b, b\le c$なら$a\le c$である。（推移性）

このとき$\le$を$A$上の **前順序** （preorder）と呼び、組$(A, \le)$を前順序集合と呼ぶ。

__定義__ 前順序集合$(A, \le)$は以下を満たすとする。

- $a, b\in A$について、ある$c\in A$が存在して$a\le c, b\le c$となる。

このとき$(A, \le)$を **有向集合** （directed set）と呼ぶ。

> 例えば集合$X$上の空でない部分集合族$\mathscr{S}\subset 2^{X}, \neq\empty$について、$\mathscr{S}$上の前順序を$A\le B:\Leftrightarrow A\supset B$で定めることができる。このとき$\mathscr{S}$が有向であることと、$\mathscr{S}$がprefilterであることは同値となる。

__定義__ $X$を集合とする。有向集合$(A, \le)$から$X$への写像を **有向ネット** （directed net）あるいは単にネットと呼ぶ。ネットは$(x_{a}: a\in A)$や$x_{\bullet}\colon A\rightarrow X$などと表す。

> ネット全体は真クラスとなる！

さて、$X$上のネットを対象とする圏について考えたい。最も自然な射は何かという問いには所説あるが、サブネットという（クラス上の）関係によるthin categoryを考えるのが良い。サブネットにもいくつか考案されているが、Willard、Kelly、Aarnes-Andenaes(AA)の三つを紹介する。この順で関係が広くなり射の数が増える。特に重要な結果として、AAサブネットによる圏と$X$上のフィルターのなす圏が反変圏同値になる。従ってネット（真クラス）とフィルター（数学的対象）は互換可能である。

> このような圏同値を通した圏の数学的対象（特に束などの構造を伴うもの）への翻訳は個人的に興味がある。

特に解析学の分野においては、位相の議論をネットで行うことが多い。我々は既に収束空間を定義したので、ネットによる収束の定義がどのような条件を満たすとき収束空間を作るのか、それが位相的であるのはどういうときか、について考えていきたい。



## サブネット

__定義__ $x_{\bullet}=(x_{a}: a\in A)$を集合$X$上のネットとする。

- $x_{\ge p}:=\lbrace x_{a} : a\ge p \rbrace$を$x_{\bullet}$の **尾集合** （tail set）と呼ぶ。
- $S\subset X$について、$S$がある尾集合を含むとき$x_{\bullet}$に関して **等終** （eventual）という。
- $S\subset X$について、$S$が全ての尾集合と共通部分を持つとき$x_{\bullet}$に関して **共終** （cofinal）という。

> 定義より、$S$が等終なら共終である。

__命題__ $(x_{a}: a\in A)$を集合$X$上のネットとする。$S\subset X$とする。TFAE

- $S$は等終である。
- $X\setminus S$は共終でない。

（証明）ある$p\in A$について$x_{\ge p}\subset S$とする。$x_{\ge p}\cap (X\setminus S)=\emptyset$より$X\setminus S$は共終でない。逆も同様。$\square$

__命題__ $(x_{a}: a\in A)$を集合$X$上のネットとする。$S, T\subset X$とする。

- $S\subset T$とする。$S$が等終なら$T$も等終である。
- $S\subset T$とする。$S$が共終なら$T$も共終である。
- $S, T$が等終なら$S\cap T$も等終である。
- $S\cup T$が共終なら$S, T$の少なくとも一方は共終である。

（証明）上二つは明らか。

$x_{\ge p}\subset S, x_{\ge q}\subset T$とすると、ある$r$が存在して$p, q\le r$となるから$x_{\ge r}\subset x_{\ge p}\cap x_{\ge q}\subset S\cap T$を得る。

$S, T$が共終でないとすると、$X\setminus S, X\setminus T$は等終である。従って$(X\setminus S)\cap(X\setminus T)=X\setminus(S\cup T)$も等終である。つまり$S\cup T$は共終でない。$\square$

> 一般に$S_{1}, \dotsc, S_{n}\subset X$について、$S_{1}\cup\dotsb\cup S_{n}$が共終なら、ある$i$について$S_{i}$は共終である。

まずは部分列の類推よりサブネットを考える。$x\colon A\rightarrow X$をネットとする。$B\subset A$は前順序集合となるから、これが有向集合となればよい。$a, b\in B$とする。$A$は有向集合だから、ある$c\in A$が存在して$a, b\le c$となる。そこで$c\le d$となる$d\in B$が存在すれば、$B$もまた有向集合となる。そのためには、任意の$c\in A$について$c\le d$なる$d\in B$が存在すればよい。ところで$A$自身は恒等写像$\mathrm{id}\colon A\rightarrow A$により$A$上のネットを定めるが、上記は$\mathrm{id}_{\ge c}\cap B\neq\emptyset$と書き換えられる。すなわち$B$は$\mathrm{id}$に対して共終である。

__定義__ $(A, \le)$を有向集合とする。ネット$\mathrm{id}\colon A\rightarrow A$に関して以下を定める。

- ネット$\mathrm{id}$の尾集合を **尾部分集合** と呼び$A_{\ge p}=\lbrace a\in A : a\ge p \rbrace$などと表す。
- ネット$\mathrm{id}$に関して共終な部分集合を$A$の **共終部分集合** と呼ぶ。同様に **等終部分集合** も定める。

__定義__ $x\colon A\rightarrow X$をネットとする。$B\subset A$は共終部分集合とする。すなわち任意の$a\in A$に対して、ある$b\in B$が存在して$a\le b$を満たすとする。このとき$x$の$B$への制限$x\restriction_{B}$を **共終サブネット** （cofinal subnet）と呼び、$x\restriction_{B}\le_{c}x$と表す。

ネット全体において、共終サブネットという関係は非常に狭いものとなる。実際上の例で$A$のコピー$A^{\prime}$を用意すると、$B$は$A^{\prime}$に含まれないため、共終サブネットとはならない。そこで、$A$の共終部分集合の上への順序保存写像が与えられている状況も考慮することにする。

__定義__ $x\colon A\rightarrow X, y\colon B\rightarrow X$をネットとする。$\phi\colon B\rightarrow A$は以下を満たすとする。

- $\phi$は単調である。つまり$b, b^{\prime}\in B$について$b\le b^{\prime}$なら$\phi(b)\le\phi(b^{\prime})$が成り立つ。
- $\phi(B)\subset A$は共終部分集合となる。つまり任意の$a\in A$に対して、ある$b\in B$が存在して$a\le\phi(b)$が成り立つ。特に$\phi(B_{\ge b})\subset A_{\ge a}$である。
- $x\circ\phi=y$である。つまり任意の$b\in B$について$x_{\phi(b)}=y_{b}$が成り立つ。

このとき$y$は$x$の **Willardサブネット** であるといい、$y\le_{w}x$と表す。

これで良さそうに思えるが、まだサブネットの本質には至らない。ネットにおいて重要なのは値域の並びと先の方での動き（共終性）であるため、単調性は外しても良い。

__定義__ Willardサブネットの一番目の単調性を外した条件を満たすとき **Kellyサブネット** といい、$y\le_{k}x$と表す。

__例__ （[KellyサブネットだがWillardサブネットでない例](https://math.stackexchange.com/questions/1126609/different-definitions-of-subnet)）$n\in\mathbb{N}$に対し$x_{n}=2^{-n}$と定める。また$n$が偶数のとき$y_{n}=2^{-(n+1)}$、奇数のとき$y_{n}=2^{-(n-1)}$と定める。

| $n$ | $0$ | $1$ | $2$ | $3$ | $4$ | $5$ |
|-|-|-|-|-|-|-|
| $x_{n}$ | $2^{0}$ | $2^{-1}$ | $2^{-2}$ | $2^{-3}$ | $2^{-4}$ | $2^{-5}$ |
| $y_{n}$ | $2^{-1}$ | $2^{0}$ | $2^{-3}$ | $2^{-2}$ | $2^{-5}$ | $2^{-4}$ |

ここで$n$が偶数のとき$\phi(n)=n+1$、奇数のとき$\phi(n)=n-1$と定めると、$x_{\phi(n)}=y_{n}$を満たす。また隣接する二項を入れ替えたに過ぎないので$\phi(\mathbb{N})\subset\mathbb{N}$は共終である。従って$y\le_{k}x$だが、$\phi$は単調ではないので$y\le_{w}x$ではない。

