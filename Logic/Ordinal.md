
# 順序数

## 順序数の基本的性質

__定義__ $z$を集合とする。

- 集合$y$について、$y\in z$なら$y\subset z$であるとき$z$は **推移的** という。
- $z$が推移的で、かつ$\in$でwell-orderedのとき **順序数** （ordinal number）という。
- 順序数全体のクラスを$\mathrm{ON}$で表す。

> $0:=\emptyset$は順序数である。後で示すが$\mathrm{ON}$は真クラスである。

__補題__ 順序数$\alpha$について、$z\in\alpha$なら$z$も順序数である。

（証明）$\alpha$は推移的なので$z\subset\alpha$である。従って$z$はwell-orderedである。$y\in z$とする。まず$y\in z\subset\alpha$だから、$\alpha$の推移性より$y\subset\alpha$である。すると$x\in y$について$x\in y\subset\alpha$だから、結局$x, y, z\in\alpha$を得る。$\alpha$は$\in$でwell-orderedより、特に$\in$は推移的関係である。故に$x\in y\in z$より$x\in z$が従う。以上より$y\subset z$を得る。$\square$

> 標語的には$\mathrm{ON}$は推移的であるといえる。

__補題__ 順序数$\alpha, \beta$について$\alpha\cap\beta$も順序数である。

（証明）$\alpha\cap\beta\subset\alpha$より$\alpha\cap\beta$はwell-orderedである。$y\in\alpha\cap\beta$について$y\in\alpha$より$y\subset\alpha$である。同様に$y\subset\beta$より$y\subset\alpha\cap\beta$である。$\square$

__補題__ 順序数$\alpha, \beta$についてTFAE

1. $\alpha\subset\beta$である。
1. $\alpha\in\beta$または$\alpha=\beta$である。

（証明）$\alpha=\beta$のときは明白。$\alpha\in\beta$のとき、$\beta$の推移性より$\alpha\subset\beta$を得る。

$\alpha\subset\beta$とする。$\alpha\neq\beta$のとき、$X:=\beta\backslash\alpha\neq\emptyset$だから整列性より最小元$\xi\in X$が取れる。$\mu\in\xi$とすると、$\xi\in\beta$だから$\beta$の推移性より$\mu\in\beta$である。$\mu\in X$なら最小性に反すので$\mu\notin X$である。故に$\mu\in\alpha$が従う。逆に$\mu\in\alpha$とすると、$\alpha\subset\beta$より$\mu\in\beta$である。ところで$\lbrace \mu, \xi \rbrace\subset\beta$は$\in$で整列されているので$\mu\in\xi$か$\xi=\mu$か$\xi\in\mu$が成り立つ。$\xi=\mu$は$\mu\in\alpha$より$\xi\notin\alpha$に矛盾する。$\xi\in\mu$も$\mu\in\alpha$と$\alpha$の推移性より$\xi\in\mu\subset\alpha$となり矛盾する。以上より$\mu\in\xi$である。よって$\alpha=\xi\in\beta$を得る。$\square$

__定理__ 順序数$\alpha, \beta, \gamma$について以下が成り立つ。

- $\alpha\in\beta$かつ$\beta\in\gamma$なら$\alpha\in\gamma$である。
- $\alpha\notin\alpha$である。
- $\alpha\in\beta$または$\beta\in\alpha$または$\alpha=\beta$が成り立つ。
- 順序数からなる空でない集合は$\in$最小元を持つ。

（証明）$\alpha\in\beta$かつ$\beta\in\gamma$とする。$\gamma$の推移性より$\alpha\in\beta\subset\gamma$である。

$\alpha$は$\in$でwell-orderedである。故に$x\in\alpha$なら$x\notin x$である。$\alpha\in\alpha$なら$\alpha\notin\alpha$となり矛盾する。故に$\alpha\notin\alpha$である。

順序数$\delta=\alpha\cap\beta$を考える。$\delta\subset\alpha$より「$\delta\in\alpha$または$\delta=\alpha$」が成り立つ。もし$\delta=\alpha$なら$\alpha\subset\beta$であり、従って「$\alpha\in\beta$または$\alpha=\beta$」を得る。$\delta\subset\beta$の場合も同様なので、結局「$\delta\in\alpha$かつ$\delta\in\beta$」の場合が残る。しかし$\delta\in\alpha\cap\beta\in\delta$となり矛盾するのでそのようなことは起こらない。

$X\neq\emptyset$を順序数からなる集合（$y\in X$なら$y$は順序数ということ）とする。$X$は空でないので順序数$\alpha\in X$を取る。$\alpha\cap X\subset\alpha$は$\in$で整列されているので最小元$\xi\in\alpha\cap X$を取る。$\xi$は$X$の$\in$最小元である。実際$\beta\in X$について「$\alpha\in\beta$か$\alpha=\beta$か$\beta\in\alpha$」であるが、前二つは$\xi\in\beta$となり、$\beta\in\alpha$のときは最小性より「$\xi=\beta$か$\xi\in\beta$」となる。$\square$

> 標語的には$\mathrm{ON}$は$\in$でwell-orderedといえる。この意味で順序数$\alpha, \beta$について$\alpha\lt\beta$は$\alpha\in\beta$の略記とする。また$\alpha\leqq\beta$も$\alpha\in\beta\vee\alpha=\beta$の略記とする。

__系__ （Burali-Fortiのパラドクス）全ての順序数を含む集合は存在しない。つまり$\mathrm{ON}$は真クラスである。

（証明）$X$は全ての順序数を含むとすると、特に$\mathrm{ON}$は集合となる。このとき標語的に述べたことを思い出せば$\mathrm{ON}$は順序数となる。しかし$\mathrm{ON}\in\mathrm{ON}$となるので定理に矛盾する。$\square$


## 後続型順序数と極限順序数

集合$x$の後者（successor）は$S(x):=x\cup\lbrace x \rbrace$により定義される。

__命題__ 順序数$\alpha$について$S(\alpha)$は順序数であり、$\alpha$より次に大きな順序数である。

（証明）$y\in S(\alpha)$とする。$y=\alpha$のとき$y=\alpha\subset S(\alpha)$は明らか。$y\in\alpha$のときは$\alpha$の推移性より$y\subset\alpha\subset S(\alpha)$となる。よって$S(\alpha)$は推移的である。$\emptyset\neq X\subset S(\alpha)$とする。$Y:=X\backslash\lbrace \alpha \rbrace\subset\alpha$について$Y\neq\emptyset$なら$\alpha$の整列性より$\in$最小元$\xi$が存在する。$\xi\in\alpha$より$\xi$は$X$の最小元である。$Y=\emptyset$なら$Y=\lbrace \alpha \rbrace$であり、$\alpha$が最小元である。以上より$S(\alpha)$は順序数である。

順序数$\gamma$について$\alpha\lt\gamma$とする。$\alpha\in\gamma$より$\alpha\subset\gamma$である。よって$S(\alpha)\subset\gamma$だから、補題より$S(\alpha)\in\gamma$または$S(\alpha)=\gamma$である。つまり$S(\alpha)\le\gamma$である。逆に$\gamma\lt S(\alpha)$とすると、$\gamma\in\alpha$または$\gamma=\alpha$が成り立つから$\gamma\le\alpha$である。$\square$

__命題__ 順序数$\beta$について以下を定める。

- ある順序数$\alpha$が存在して$\beta=S(\alpha)$のとき、$\beta$は **後続型順序数** と呼ぶ。
- $\beta\neq 0$かつ後続型順序数でないとき、$\beta$は **極限順序数** と呼ぶ。
- $\alpha\le\beta$なる順序数$\alpha$が$0$か後続型順序数のとき、$\beta$は **有限順序数** あるいは **自然数** と呼ぶ。

