
# Microfacet理論

以下はまだ検討段階なので半分くらい妄想。あるいは既に考えられているとか、既存の理論で書けるかもしれない。



## はじめに

    Eric Heitz. Understanding the Masking-Shadowing Function in Microfacet-Based BRDFs.

を読んで、結構面白い事をやってると思ったので公理化できないかなと模索している。

どんな事かというと、平らな面（幾何学面）の表面に非常に細かい構造を考えて、その微細構造における光の反射を、例えば法線分布といった球面上での積分として計算する。このとき幾何学面というマクロな構造と、法線分布や遮蔽函数で表されるミクロな構造が両立するようなものを考える。

例えば$\lbrack 0, 1 \rbrack$の表面に正三角形を並べた図形を考えてみる。正三角形の辺の長さはなんでもいいが、この表面は折れ線（曲面）なので、この上の積分は実行できる。では一片の長さを無限に小さくしたものはどう考えるべきか。解析学的にはもちろん$\lbrack 0, 1 \rbrack$に収束する。しかしmicrofacet理論では微細な凹凸が残っていると考える。つまり$\frac{\pi}{6}$を向いてる面積が$1$で、$\frac{5}{6}\pi$を向いてる面積が$1$と考え、法線分布を

$$
D( \omega )=1\cdot\delta_{\frac{\pi}{6}}( \omega )+1\cdot\delta_{\frac{5}{6}\pi}( \omega )
$$

で与える。更に法線分布だけでは微細構造を決定しないと考えて、遮蔽函数$G( \omega_{0}, \omega)$を考慮する。$\omega_{0}$方向に$\omega$を向いた面がどれだけ遮蔽されるかを表す函数である。

正直なところ論文中の式変形は良く分からなくて、例えばSpatial-Statistical変換について$GL$の変換を$G$と$L$の変換の積にしているなど怪しい操作をしている。（準同型か？）しかし発想は面白くて、光の反射やらBRDFは分からなくても、エッセンスだけ取り出せば色々な分野にも応用できそうな気がする。

Microfacet理論の公理化に動機があるとすれば以下に挙げる通りだろう。

- 微細構造上での積分が非常に難しい。計算困難あるいは単純な式で表せない。
- 表面の特性は分かっていて、例えば法線分布や遮蔽函数で表される。
- 微細構造上の函数（例えば輝度）の積分を計算し、その定量的な評価を与えたい。

微細構造上の積分が可能な場合に、それと整合的であるべきか、あるいはそうでないかは分からない。



## 素朴な公理化

**定義** $\Omega=S^{n}$とする。集合$M$の$\Omega$-微細構造は以下のデータからなる。

- 法線分布を意味する$\Omega$上の測度$D$
- 各点における法線を意味する写像$\omega_{m}\colon M\rightarrow\Omega$
- $M$上の函数$g$について$\Omega$上の函数$\Psi g$が存在し、以下を満たす。

    1. $\Omega$上の函数$f$について$\Psi\lbrack f\circ\omega_{m} \rbrack=f$が成り立つ。
    2. 次の等式が成り立つ。

$$
\Psi g( \omega )=\frac{1}{D( \omega )}\int_{\Omega}\Psi\lbrack \delta_{\omega}( \omega_{m}( \cdot ) )g( \cdot ) \rbrack ( \eta )D( \eta )\mathrm{d}\eta
$$

定数函数$c$について$\Psi c=c$が成り立ち、論文中では$\Psi\lbrack GL \rbrack=\Psi G\Psi L$を用いたりしているので、$\Psi$は代数準同型とするのが良いのかもしれない。むしろ$G$の性質かもしれないが。

**例** $M$上の積分が存在する場合、

$$
\begin{aligned}
D( \omega ) &:= \int_{M} \delta_{\omega}( \omega_{M}( p ) )\mathrm{d}p, \\
\Psi g( \omega ) &:= \frac{1}{D( \omega )}\int_{M} \delta_{\omega}( \omega_{M}( p ) )g( p )\mathrm{d}p
\end{aligned}
$$

と定めればよい。実際、まず定義より

$$
D( \omega )=\int_{M}\delta_{\omega}( \omega_{m}( p ) )\mathrm{d}p
$$

である。従って$\Omega$上の函数$f$について

$$
\begin{aligned}
\Psi\lbrack f\circ \omega_{m} \rbrack( \omega ) &= \frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )f( \omega_{m}( p ) )\mathrm{d}p \\
&=\frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )\mathrm{d}p\cdot f( \omega ) \\
&=f( \omega )
\end{aligned}
$$

を得る。また

$$
\begin{aligned}
&\frac{1}{D( \omega )}\int_{M}\Psi\lbrack \delta_{\omega}( \omega_{m}( \cdot ) )g( \cdot ) \rbrack( \eta )D( \eta )\mathrm{d}\eta \\
&=\frac{1}{D( \omega )}\int_{\Omega}\frac{1}{D( \eta )}\int_{M}\delta_{\eta}( \omega_{m}( p ) )\delta_{\omega}( \omega_{m}( p ) )g( p )\mathrm{d}p\cdot D( \eta )\mathrm{d}\eta \\
&=\frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )g( p )\left( \int_{\Omega}\delta_{\eta}( \omega_{m}( p ) )\mathrm{d}\eta \right)\mathrm{d}p \\
&=\frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )g( p )\mathrm{d}p \\
&=\Psi g( \omega )
\end{aligned}
$$

より条件を満たす。

**注意** 積分の交換はあまり重要ではない。というのも函数の集合を誤魔化して書いているので、交換できる$g$についてのみ考えている。また$\Omega=S^{n}$も本質的に重要ではない。$D( \omega )=0$となるような$\omega$も考えていない。最終的にはきちんと書くべきところだが、現時点では柔軟に考える。



## 微細構造上の積分

公理化のためには$\Psi$についてより多くの例と検証が必要だと思う。今のままでは、上の等式は$\omega_{m}$に依るので非常に扱い辛い。というのも、三角形の例でも分かるように、微細構造は曲面でないものを考えたい。よって各点を取ってその法線を求めるということが原理的に難しい。個人的には法線分布と遮蔽函数などが表面特性を表すと思っているので、各点の法線という表現をしたくない。$M$上の積分がないときに積分っぽいものを考えることができる、というのがmicrofacet理論の目指すべき方向性ではないだろうか。

**定義** $\Omega^{\prime}\subset\Omega$について$M^{\prime}=\lbrace p\in M : \omega_{M}( p )\in\Omega^{\prime} \rbrace$とする。$M$上の函数$g$の$M^{\prime}$における積分を

$$
\int^{\Psi}_{M^{\prime}}g( p )\mathrm{d}p:=\int_{\Omega^{\prime}}\Psi g( \eta )D( \eta )\mathrm{d}\eta
$$

で定める。

**例** $M$上の積分があるときは一致する。実際

$$
\begin{aligned}
\int^{\Psi}_{M^{\prime}}g( p )\mathrm{d}p &=\int_{\Omega^{\prime}}\Psi g( \eta )D( \eta )\mathrm{d}\eta \\
&= \int_{\Omega^{\prime}}\frac{1}{D( \omega )}\int_{M}\delta_{\eta}( \omega_{m}( p ) )g( p )\mathrm{d}p\cdot D( \eta )\mathrm{d}\eta \\
&=\int_{M}\left( \int_{\Omega^{\prime}}\delta_{\eta}( \omega_{m}( p ) )\mathrm{d}\eta \right)g( p )\mathrm{d}p \\
&=\int_{M^{\prime}}g( p )\mathrm{d}p
\end{aligned}
$$

である。

**命題** 以下が成り立つ。

$$
\begin{aligned}
& \int^{\Psi}_{M^{\prime}}\mathrm{d}p=\int_{\Omega^{\prime}}D( \eta )\mathrm{d}\eta, \\
& \int^{\Psi}_{M}f( \omega_{m}( p ) )\mathrm{d}p =\int_{\Omega}\Psi\lbrack f\circ\omega_{m} \rbrack( \eta )D( \eta )\mathrm{d}\eta=\int_{\Omega}f( \eta )D( \eta )\mathrm{d}\eta, \\
& \Psi g( \omega )=\frac{1}{D( \omega )}\int_{\Omega}\Psi\lbrack \delta_{\omega}( \omega_{m}( \cdot ) )g( \cdot ) \rbrack( \eta )D( \eta )\mathrm{d}\eta=\frac{1}{D( \omega )}\int^{\Psi}_{M}\delta_{\omega}( \omega_{m}( p ) )g( p )\mathrm{d}p.
\end{aligned}
$$



## 幾何学面との両立

幾何学面の持つマクロな構造は、微細構造を無視したときの法線$\omega_{g}$で決定される。三角形の例であれば、$\lbrack 0, 1 \rbrack$が幾何学面であり、その面は$\frac{\pi}{2}$方向を向いている。微細構造の法線$\omega_{m}( p )$はむしろ$\omega_{g}$に対する回転で表すべきだろう。現時点では平らな面しか考えていないが、いずれ曲率を伴う多様体の一部と見なすのが自然である。つまりマクロな構造といっても局所的なもので、大域的なマクロ構造！　は別にある。このとき多様体の座標変換に応じて、その回転が両立するように定義すべきかもしれない。いずれにせよそれを考えるのは時期尚早だが。

$G( \omega_{0}, p )$は、点$p\in M$が$\omega_{0}$方向に遮蔽されているか否かを表す二値函数とする。このとき$\omega_{0}$方向への投射面積は$M$上の面積が存在するとき、

$$
\int_{M}G( \omega_{0}, p )\langle \omega_{m}( p ), \omega_{0} \rangle\mathrm{d}p=\int^{\Psi}_{M}G( \omega_{0}, p )\langle \omega_{m}( p ), \omega_{0} \rangle\mathrm{d}p
$$

で表される。ここで$\langle \cdot, \cdot \rangle$は正にクランプした（負はゼロにする）内積である。右辺を計算すると

$$
\begin{aligned}
&\int_{\Omega}\Psi\lbrack G( \omega_{0}, \cdot )\langle \omega_{m}( \cdot ), \omega_{0} \rangle \rbrack( \eta )D( \eta )\mathrm{d}\eta \\
&=\int_{\Omega}\frac{1}{D( \eta )}\int_{M}\delta_{\eta}( \omega_{m}( p ) )G( \omega_{0}, p )\langle \omega_{m}( p ), \omega_{0} \rangle\mathrm{d}p\cdot D( \eta )\mathrm{d}\eta \\
&=\int_{\Omega}\frac{1}{D( \eta )}\int_{M}\delta_{\eta}( \omega_{m}( p ) )G( \omega_{0}, p )\mathrm{d}p\langle \eta, \omega_{0} \rangle D( \eta )\mathrm{d}\eta \\
&=\int_{\Omega}\Psi G( \eta )\langle \eta, \omega_{0} \rangle D( \eta )\mathrm{d}\eta
\end{aligned}
$$

となる。この$\Psi G$は

$$
\begin{aligned}
\vert \Psi G( \omega_{0}, \omega )\vert &= \left\vert \frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )G( \omega_{0}, p )\mathrm{d}p \right\vert \\ &\le \frac{1}{D( \omega )}\int_{M}\delta_{\omega}( \omega_{m}( p ) )\mathrm{d}p \\
&=1
\end{aligned}
$$

より、$\Psi G( \omega_{0}, \omega )\in\lbrack 0, 1 \rbrack$を満たす。

さて、微細構造は微細なのだから、マクロな視点から見れば投射面積に影響を与えない。従って、上の積分は幾何学面の面積

$$
\mathrm{cos}\theta_{0}
$$

と一致するだろう。（$\theta_{0}$は$\omega_{0}$と$\omega_{g}$の成す角。）故に遮蔽函数を次のように定義できる。

**定義** $0\le H( \omega_{0}, \omega )\le 1$が任意の$\omega_{0}$について

$$
\int_{\Omega}H( \omega_{0}, \eta )\langle \eta, \omega_{0} \rangle D( \eta )\mathrm{d}\eta=\mathrm{cos}\theta_{0}=\omega_{g}\cdot\omega_{0}
$$

を満たすとき、遮蔽函数と呼ぶ。