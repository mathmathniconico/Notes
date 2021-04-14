
## 基本被覆定理

> 以下はVitaliの被覆補題とも呼ばれている。

__補題__ $\mathscr{F}$を空でない集合族とする。各$F\in\mathscr{F}$について正の数$r(F)\gt 0$が与えられており、$d:=\mathrm{sup}\lbrace r(F) : F\in\mathscr{F} \rbrace\lt\infty$とする。$c\lt 1$とする。このとき以下を満たす部分集合族$\mathscr{G}\subset\mathscr{F}$が存在する。

- $\mathscr{G}$は非交叉である。つまり任意の$A, B\in\mathscr{G}$について$A\cap B\neq\emptyset$である。
- 任意の$F\in\mathscr{F}$に対し、ある$V\in\mathscr{G}$が存在して$c\cdot r(F)\le r(V)$かつ$V\cap F\neq\emptyset$が成り立つ。

（証明）Zornの補題による。まず集合$\Omega$を以下の条件を満たす$\omega\subset\mathscr{F}$の全体とする。

- $\omega$は非交叉である。
- $F\in\mathscr{F}$について$\omega^{F}:=\lbrace V\in\omega : V\cap F\neq\emptyset \rbrace$が空でないなら、$c\cdot r(F)\le r(V)$を満たす$V\in\omega^{F}$が存在する。

$\Omega$が空でないことを示そう。$d$は上限なので、適当な$V_{n}\in\mathscr{F}$が存在して$r(V_{n})\nearrow d\gt 0$となる。このときある$n$について$r(V_{n})\ge c\cdot d$が成り立つ。そこで$\omega_{n}:=\lbrace V_{n} \rbrace$とおく。$\omega_{n}$が非交叉なのは明らか。$F\in\mathscr{F}$について$\omega_{n}^{F}\neq\emptyset$とする。このとき$c\cdot r(F)\le c\cdot d\le r(V_{n})$である。故に$\omega_{n}\in\Omega$である。

$\Omega$は包含関係で半順序集合となるが、帰納的であることを示そう。$\tau\subset\Omega$を全順序部分集合とする。$\omega_{\tau}:=\bigcup_{\omega\in\tau}\omega$とおく。$\omega_{\tau}$が非交叉なのは明らか。$F\in\mathscr{F}$について$\omega_{\tau}^{F}\neq\emptyset$とする。このときある$W\in\omega_{\tau}$が存在して$W\cap F\neq\emptyset$となるが、$\omega_{\tau}$の定義よりある$\omega\in\tau$について$W\in\omega$であり$\omega^{F}\neq\emptyset$が分かる。$\omega\in\Omega$より$c\cdot r(F)\le r(V)$を満たす$V\in\omega^{F}$が存在する。特に$V\in\omega_{\tau}^{F}$より$\omega_{\tau}\in\Omega$を得る。つまり$\omega_{\tau}$は$\tau$の上界を与えているので$\Omega$は帰納的である。

Zornの補題より極大元$\mathscr{G}\in\Omega$が存在する。これが題意を満たすことを背理法により示そう。ある$F\in\mathscr{F}$が存在して、任意の$W\in\mathscr{G}$について$F\cap W=\emptyset$と仮定する。このとき

$$
\mathscr{G}^{\perp}:=\lbrace G\in\mathscr{F} : \forall W\in\mathscr{G}, G\cap W=\emptyset \rbrace
$$

は空でない。更に$\lbrace r(G) : G\in\mathscr{G}^{\perp} \rbrace$は有界なので、$G_{0}\in\mathscr{G}^{\perp}$を、任意の$G\in\mathscr{G}^{\perp}$に対して$c\cdot r(G)\le r(G_{0})$を満たすように取れる。$\mathscr{H}:=\mathscr{G}\cup\lbrace G_{0} \rbrace$とおく。これは$\mathscr{G}$より真に大きい非交叉な集合族である。$A\in\mathscr{F}$について$\mathscr{H}^{A}\neq\emptyset$とする。

- $W\in\mathscr{H}^{A}$を$W\in\mathscr{G}$として取れる場合、$W\in\mathscr{G}^{A}\neq\emptyset$だから$\mathscr{G}\in\Omega$の条件より$c\cdot r(A)\le r(V)$を満たす$V\in\mathscr{G}^{A}$が存在する。特に$V\in\mathscr{H}^{A}$だから$\mathscr{H}\in\Omega$である。
- $G_{0}\in\mathscr{H}^{A}$かつ任意の$W\in\mathscr{G}$について$W\notin\mathscr{H}^{A}$とする。このとき$A\in\mathscr{G}^{\perp}$だから$G_{0}$の取り方より$c\cdot r(A)\le r(G_{0})$が成り立つ。故に$\mathscr{H}\in\Omega$である。

以上は$\mathscr{G}$の極大性に矛盾する。従って任意の$F\in\mathscr{F}$について$\mathscr{G}^{F}\neq\emptyset$である。$\mathscr{G}\in\Omega$より$c\cdot r(F)\le r(V)$を満たす$V\in\mathscr{G}^{F}$が存在する。$\square$

__系__ $X$を距離空間とする。$\mathscr{F}$をボール（開か閉は問わない）からなる集合とし、$B\in\mathscr{F}$について半径$r(B)$は上に有界とする。$\varepsilon\gt 0$とする。このときある$\mathscr{G}\subset\mathscr{F}$が存在して$\bigcup\mathscr{F}\subset\bigcup (3+\varepsilon)\mathscr{G}$を満たす。
