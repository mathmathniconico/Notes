
# 巡回群

__定義__ $G$を群とする。$S\subset G$を含む最小の部分群を$\langle S \rangle$と表し、$S$が **生成** （generate）する部分群あるいは$S$によって生成される部分群という。

- $\langle S \rangle$は$S$を含む部分群の共通部分として表される。

__定義__ $G$を群とする。$g\in G$が生成する部分群

$$
\langle g \rangle:=\langle \lbrace g \rbrace \rangle=\lbrace g^{n} : n\in\mathbb{Z} \rbrace
$$

について、$\mathrm{ord}g:=\vert \langle g \rangle \vert$を$g$の **位数** （order）と呼ぶ。$G=\langle g \rangle$と表されるとき$G$を **巡回群** （cyclic group）と呼び、$g$を$G$の **生成元** （generator）と呼ぶ。

- 巡回群はアーベル群である。

__例__ 以下に巡回群の例を挙げる。

- $\mathbb{Z}$は加法により巡回群となる。生成元は$1$である。
- 整数$m$について$m\mathbb{Z}\subset\mathbb{Z}$は加法に関する正規部分群となる。この剰余群$\mathbb{Z}/m\mathbb{Z}$は巡回群である。生成元は$1+m\mathbb{Z}$である。
- $\mu_{m}:=\lbrace z\in\mathbb{C}^{\times} : z^{m}=1 \rbrace$は乗法に関する巡回群となる。生成元は$\xi_{m}:=e^{2\pi i/m}$である。

