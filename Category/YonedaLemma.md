
# 米田の補題

__補題__ （米田の補題）函手$h\colon\mathscr{C}\rightarrow\mathbf{Psh}(\mathscr{C})$について次が成り立つ。

- $h$は忠実充満である。
- $F\in\mathbf{Psh}(\mathscr{C}), U\in\mathscr{C}$とする。$\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F)\rightarrow FU$を$s\mapsto s_{U}(\mathrm{id}_{U})$で定める。この対応は自然な全単射である。

<p align=center><img src="pics/yoneda_01.svg" width="300"/></p>

$h\colon\mathscr{C}\rightarrow\mathrm{Psh}(\mathscr{C})$が忠実充満ということは、射に関する$\mathscr{C}$での議論と$\mathrm{Psh}(\mathscr{C})$での議論は「同じ」とみなせる。後者の方が構造的には豊かであり、対象も多く、調べやすい。また二つ目の全単射により、$h_{U}$から$F$への自然変換は$FU$の元に対応している。

（証明）











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

以上より圏$\mathscr{C}$における直積の存在が、圏$\mathrm{Psh}(\mathscr{C})$における$F$の表現可能性として翻訳することができた。







## コード置き場

```latex {cmd}
\documentclass{standalone}
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
\begin{document}

\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F) \arrow[r] \arrow[d, contains] & FU \arrow[d, contains] \\
s \arrow[r, mapsto] & s_{U}(\mathrm{id}_{U})
\end{tikzcd}

\end{document}
```


```latex
\usepackage{amsmath, amssymb, mathrsfs}

\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
\mathrm{Mor}_{\mathrm{Psh}(\mathscr{C})}(h_{U}, F) \arrow[r] \arrow[d, contains] & FU \arrow[d, contains] \\
s \arrow[r, mapsto] & s_{U}(\mathrm{id}_{U})
\end{tikzcd}
```
