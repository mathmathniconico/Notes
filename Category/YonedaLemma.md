
# 米田の補題

> 米田の補題の証明はstraight forward、つまり「書いてみれば分かる」が、射が色々あるので混乱しやすい。ちなみにStacks Projectの証明はわずか3行である。

__補題__ （米田の補題）函手$h\colon\mathscr{C}\rightarrow\mathbf{Psh}(\mathscr{C})$について次が成り立つ。

- $h$は忠実充満である。
- $F\in\mathbf{Psh}(\mathscr{C}), U\in\mathscr{C}$とする。このとき$\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F)\rightarrow FU$を$ s\mapsto s_{U}(\mathrm{id}_{U})$で定める。これは自然な全単射となる。

<p align=center><img src="pics/yoneda_01.svg" height="100"></p>

> $h\colon\mathscr{C}\rightarrow\mathrm{Psh}(\mathscr{C})$が忠実充満ということは、射に関する$\mathscr{C}$の言葉が$\mathrm{Psh}(\mathscr{C})$の言葉に翻訳できることを意味する。後者の方が対象は多いため、構造的に豊かで調べやすい。また下の全単射により、$h_{U}$から$F$への自然変換は$FU$という集合の元に対応している。従って集合$FU$を調べることが$\mathrm{Psh}(\mathscr{C})$の射を調べることと実質的に同等となる。

（証明）まず$h$が忠実充満であることを示す。$U, V\in\mathscr{C}$及び自然変換$s\colon h_{U}\rightarrow h_{V}$を取る。$s_{U}\colon h_{U}(U)\rightarrow h_{V}(U)$について$\phi:=s_{U}(\mathrm{id}_{U})$と置く。自然変換$h\phi\colon h_{U}\rightarrow h_{V}$が$s$と一致することを示したい。$X\in\mathscr{C}$について$(h\phi)_{X}\colon h_{U}(X)\rightarrow h_{V}(X)$を考える。$\rho\in h_{U}(X)$に対し、$s$は自然変換だから以下の図式を可換とする。$(h\phi)_{X}(\rho)=\phi\circ\rho$に注意する。

<p align=center><img src="pics/yoneda_02.svg" height="100"></p>

よって$h\phi=s$が成り立つ。逆に$h\phi^{\prime}=s$なら$\phi=(h\phi^{\prime})_{U}(\mathrm{id}_{U})=s_{U}(\mathrm{id}_{U})$より一意性も従う。射の集合に全単射が存在するので、$h$は忠実充満である。

次に$F\in\mathbf{Psh}(\mathscr{C}), U\in\mathscr{C}$とする。$\xi\in FU$に対し自然変換$\Psi\xi\colon h_{U}\rightarrow F$を以下で定める。

- $X\in\mathscr{C}$について$(\Psi\xi)_{X}\colon h_{U}(X)\rightarrow FX$は$f\mapsto Ff(\xi)$とする。

$\Phi\xi$が自然変換であることは$F$が反変函手であることから従う。

さて$s\mapsto s_{U}(\mathrm{id}_{U})$と$\xi\mapsto\Psi\xi$は互いに全単射であることを示したい。$\xi=s_{U}(\mathrm{id}_{U})$に対して$\Phi\xi$は、$f\in h_{U}(X)$に対し

$$
(\Psi\xi)_{X}(f)=Ff(\xi)=Ff(s_{U}(\mathrm{id}_{U}))=s_{X}(h_{U}f(\mathrm{id}_{U})=s_{X}(f)
$$

を対応させる。（途中$s$が自然変換であることを用いた。）故に$\Psi\xi=s$である。逆に$s=\Psi\xi$なら

$$
s_{U}(\mathrm{id}_{U})=(\Psi\xi)_{U}(\mathrm{id}_{U})=F(\mathrm{id}_{U})(\xi)=\mathrm{id}_{FU}(\xi)=\xi
$$

より、確かに全単射である。

最後に対応が自然であることを示そう。$U, V\in\mathscr{C}$及び$F, G\in\mathrm{Psh}(\mathscr{C})$とする。$U\xleftarrow{\rho}V$及び自然変換$\eta\colon F\rightarrow G$について以下の図式が可換であることを示せばよい。簡単のため$\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F)$を$\lbrack h_{U}, F \rbrack$で表す。

<p align=center><img src="pics/yoneda_03.svg" height="200"></p>

底面は$\eta$が自然変換であることから可換となる。

左の側面の可換性を示す。$\lbrack h_{U}, F \rbrack\rightarrow\lbrack h_{V}, F \rbrack$は以下の写像$s\mapsto\widetilde{s}$である。

- $X\in\mathscr{C}$について$\widetilde{s}_{X}\colon h_{V}(X)\xrightarrow{(h\rho)_{X}} h_{U}(X)\xrightarrow{s_{X}}FX$である。つまり$f\in h_{V}(X)$について$\widetilde{s}_{X}(f)=s_{X}(\rho\circ f)$である。

一方$\xi=F\rho(s_{U}(\mathrm{id}_{U}))\in FV$に対応する自然変換$\Psi\xi\colon h_{V}\rightarrow F$は、$f\in h_{V}(X)$を

$$
(\Psi\xi)_{X}(f)=Ff(\xi)=Ff(F\rho(s_{U}(\mathrm{id}_{U})))=F(\rho\circ f)(s_{U}(\mathrm{id}_{U}))=\Psi(s_{U}(\mathrm{id}_{U}))(\rho\circ f)=s_{X}(\rho\circ f)=\widetilde{s}_{X}(f)
$$

に写す。よって$\Phi\xi=\widetilde{s}$であり図式は可換になる。右の側面も同様である。

背面の可換性を示す。$\lbrack h_{U}, F \rbrack\rightarrow \lbrack h_{U}, G \rbrack$は以下の写像$s\mapsto\widehat{s}$である。

- $X\in\mathscr{C}$について$\widehat{s}_{X}\colon h_{U}(X)\xrightarrow{s_{X}}FX\xrightarrow{\eta_{X}}GX$である。

従って$\widehat{s}_{U}(\mathrm{id}_{U})=\eta_{U}(s_{U}(\mathrm{id}_{U}))$より図式は可換となる。正面も同様である。

以上より天面の可換性も従う。$\square$


## 直積対象と米田の補題

$A, B\in\mathscr{C}$の直積を例に取り、その定義が正統なものであることを確認しよう。

まず$h_{A}, h_{B}$の「直積」として$F=h_{A}\times h_{B}\in\mathrm{Psh}(\mathscr{C})$を以下で定める。

- $X\in\mathscr{C}$に対し$FX=h_{A}(X)\times h_{B}(X)$とする。
- $\rho\colon X\leftarrow Y$に対し$F\rho\colon FX\rightarrow FY$を$(f, g)\mapsto(f\circ\rho, g\circ\rho)$で定める。

補題によれば$U\in\mathscr{C}$に対して自然な全単射

$$
\Phi_{U}\colon\mathrm{Mor}(h_{U}, F)\rightarrow h_{A}(U)\times h_{B}(U)
$$

が存在する。右辺から$\xi=(p, q)$を取れるとして、対応する自然変換$\Phi_{U}^{-1}\xi$を考える。それは$X\in\mathscr{C}$について

$$
(\Phi_{U}^{-1}\xi)_{X}\colon h_{U}(X)\rightarrow h_{A}(X)\times h_{B}(X)
$$

という射から構成され、$\rho\in h_{U}(X)$を$F\rho(\xi)=(p\circ\rho, q\circ\rho)$に写す。

直積$A\prod B$と射影$\pi_{A}, \pi_{B}$が存在する場合を考える。$X\in\mathscr{C}$及び$f\colon X\rightarrow A, g\colon X\rightarrow B$に対し、ある$k\in h_{A\prod B}(X)$が唯一つ存在して$\pi_{A}\circ k=f, \pi_{B}\circ k=g$を満たす。この写像$\Psi_{X}\colon (f, g)\mapsto k$は$\xi=(\pi_{A}, \pi_{B})$としたときの$(\Phi_{A\prod B}^{-1}\xi)_{X}$の逆を与えている。従って$\Phi_{A\prod B}^{-1}\xi\in\mathrm{Mor}(h_{A\prod B}, F)$と$\Psi\in\mathrm{Mor}(F, h_{A\prod B})$によって$\mathrm{Psh}(\mathscr{C})$における同型$F\simeq h_{A\prod B}$を得る。つまり$F$は表現可能である。

逆に$F$が$U\in\mathscr{C}$によって表現可能としよう。同型を$s\colon h_{U}\xrightarrow{\simeq}F$とする。$s\in\mathrm{Mor}(h_{U}, F)$より

$$
(p, q):=\Phi_{U}(s)=s_{U}(\mathrm{id}_{U})\in h_{A}(U)\times h_{B}(U)
$$

と置く。$X\in\mathscr{C}$及び$f\colon X\rightarrow A, g\colon X\rightarrow B$に対し、$s_{X}\colon h_{U}(X)\rightarrow h_{A}(X)\times h_{B}(X)$は全単射だから$k:=s_{X}^{-1}(f, g)\in h_{U}(X)$とする。

$$
(f, g)=s_{X}(k)=Fk(s_{U}(\mathrm{id}_{U}))=Fk(p, q)=(p\circ k, q\circ k)
$$

より$k$は図式を可換とし、また一意的であることも分かる。従って$U$及び$p, q$は$A$と$B$の直積であることがわかる。

以上より圏$\mathscr{C}$における直積の存在が、圏$\mathrm{Psh}(\mathscr{C})$における$F$の表現可能性に翻訳できることが分かった。


<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% yoneda_01.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F) \arrow[r] \arrow[d, contains] & FU \arrow[d, contains] \\
s \arrow[r, mapsto] & s_{U}(\mathrm{id}_{U})
\end{tikzcd}
```

```latex
%yoneda_02.dvg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
U \arrow[d, leftarrow, "\rho"'] & h_{U}(U) \arrow[r, "s_{U}"] \arrow[d, "h_{U}\rho"'] \arrow[dr, phantom, "\circlearrowright"] & h_{V}(U) \arrow[d, "h_{V}\rho"] & & \mathrm{id}_{U} \arrow[r, mapsto] \arrow[d, mapsto] & s_{U}(\mathrm{id}_{U})=\phi \arrow[d, mapsto] \\
X & h_{U}(X) \arrow[r, "s_{X}"'] & h_{V}(X) & & \mathrm{id}_{U}\circ\rho=\rho \arrow[r, mapsto] & s_{X}(\rho)=\phi\circ\rho=(h\phi)_{X}(\rho)
\end{tikzcd}
```

```latex
%yoneda_03.dvg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
\lbrack h_{U}, F \rbrack \arrow[rr] \arrow[dr] \arrow[dd, leftrightarrow] & & \lbrack h_{U}, G \rbrack \arrow[dr] \arrow[dd, leftrightarrow] & \\
& \lbrack h_{V}, F \rbrack \arrow[rr] \arrow[dd, leftrightarrow] & & \lbrack h_{V}, G \rbrack \arrow[dd, leftrightarrow] \\
FU \arrow[rr, "\eta_{U}"', near end] \arrow[dr, "F\rho"'] & & GU \arrow[dr, "G\rho"] & \\
& FV \arrow[rr, "\eta_{V}"'] & & GV
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
\lbrack h_{U}, F \rbrack \arrow[rr] \arrow[dr] \arrow[dd, leftrightarrow] & & \lbrack h_{U}, G \rbrack \arrow[dr] \arrow[dd, leftrightarrow] & \\
& \lbrack h_{V}, F \rbrack \arrow[rr] \arrow[dd, leftrightarrow] & & \lbrack h_{V}, G \rbrack \arrow[dd, leftrightarrow] \\
FU \arrow[rr, "\eta_{U}"', near end] \arrow[dr, "F\rho"'] & & GU \arrow[dr, "G\rho"] & \\
& FV \arrow[rr, "\eta_{V}"'] & & GV
\end{tikzcd}

\end{document}
```
-->