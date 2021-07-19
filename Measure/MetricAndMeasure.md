
# 距離空間と測度

以下$(X, \rho)$は距離空間とする。また$A\subset X$に対し$A$の直径を

$$
\vert A \vert=\textrm{diam}(A):=\sup\lbrace \rho (x, y)\mid x, y\in A \rbrace
$$

で表す。

__定義__ $\mu$を$X$上の外測度とする。任意の$A, B\subset X$について、$\rho (A, B):=\inf\lbrace \rho (x, y)\mid x\in A, y\in B \rbrace\gt 0$なら$\mu (A\sqcup B)=\mu (A)+\mu (B)$が成り立つとき **距離外測度** （metric outer measure）であるという。

__命題__ $\mu$を距離外測度とする。以下が成り立つ。

- $A_{n}\nearrow A$が$\rho (A_{n}, A\setminus A_{n+1})\gt 0$を満たすとき$\mu (A)=\sup\mu (A_{n})$が成り立つ。
- ボレル集合は$\mu$可測である。即ち$\sigma\lbrack \mathcal{O}_{\rho} \rbrack\subset\mathcal{M}_{\mu}$が成り立つ。

（証明）$B_{1}:=A_{1}, B_{m}:=A_{m}\setminus A_{m-1}$と置くと$A_{n}=\bigsqcup_{m=1}^{n}B_{m}, A=\bigsqcup B_{m}$が成り立つ。ここで$\mu$は外測度だから、単調性及び可算劣加法性より

$$
\sum_{m=1}^{n}\mu (B_{m})=\mu (A_{n})\le\mu (A)\le\sum\mu (B_{m})
$$

が成り立つ。このとき左辺の上限を取れば$\sup\mu (A_{n})=\mu (A)$を得る。

$F\subset X$を閉集合とする。$n\in\mathbb{N}$に対して

$$
U_{n}:=\left\lbrace x\in X\setminus F\mid \rho (x, F)\gt\frac{1}{n}\right\rbrace
$$

と定めると$U_{n}\nearrow X\setminus F$となる。任意の$E\subset X$に対して$\rho (E\cap U_{n}, E\cap F)\gt 0$を満たす。$\mu$は距離外測度だから

$$
\mu (E\cap U_{n})+\mu (E\cap F)=\mu ((E\cap U_{n})\sqcup (E\cap F))\le\mu(E)
$$

が成り立つが、$E\cap U_{n}\nearrow E\setminus F$は先の条件を満たしているので

$$
\mu (E\setminus F)+\mu (E\cap F)\le\mu (E)
$$

を得る。即ち$F$は$\mu$可測となる。$\mu$可測集合全体は$\sigma$加法族なので、$\sigma\lbrack \mathcal{O}_{\rho} \rbrack\subset\mathcal{M}_{\mu}$が従う。$\square$

距離外測度は以下のようにして構成できる。$\mathscr{E}\subset 2^{X}$は空集合を含むとする。$\delta\gt 0$とする。以下の文脈において$\mathscr{C}\subset\mathscr{E}$が$A\subset X$の$\mathscr{E}$による$\delta$被覆であるとは、$\mathscr{C}$が高々可算集合かつ$A\subset\bigcup_{C\in\mathscr{C}}C$であり、また任意の$C\in\mathscr{C}$に対して$\vert C \vert\le\delta$を満たすことを意味するものとする。

集合関数$\tau\colon\mathscr{E}\rightarrow\lbrack 0, \infty \rbrack$は$\tau (\emptyset)=0$を満たすとする。$\delta\gt 0$及び$A\subset X$に対し、$A$の$\delta$被覆$\mathscr{C}\subset\mathscr{E}$に関する$\sum_{C\in\mathscr{C}}\tau(C)$の下限を$\mu_{\delta}(A)$と定める。つまり

$$
\mu_{\delta}(A):=\inf\left\lbrace \sum_{C\in\mathscr{C}}\tau (C) : \mathscr{C}\subset\mathscr{E}\textup{は$A$の$\delta$被覆}\right \rbrace
$$

と定める。そして$\mu (A):=\sup_{\delta}\mu_{\delta}(A)$と置く。

<!--
\begin{Prop}
$\mu$は距離外測度となる。
\end{Prop}
\begin{Proof}
$\delta$-被覆はつまり直径が$\delta$以下の集合全体による被覆だから、$\mu_{\delta}$は外測度になる。
従って$A, B\subset X, A\subset B, \{A_{n}\}\subset 2^{X}$に対して
\[ \mu_{\delta}(\emptyset)=0, \mu_{\delta}(A)\le\mu_{\delta}(B),
\mu_{\delta}\left(\bigcup A_{n}\right)\le\sum\mu_{\delta}(A_{n}) \]
が成り立つ。$\delta$の上限を取れば、$\mu$は外測度になる。

　$A, B\subset X$は$\rho (A, B)>0$を満たすとする。このとき
\[ \delta:=\frac{\rho (A, B)}{3} \]
とすると、$A\sqcup B$の$\delta$-被覆$\mathscr{C}$に対して$A, B$の部分$\delta$-被覆$\mathscr{C}_{A}, \mathscr{C}_{B}$を互いに素に取れる。このとき
\[ \mu_{\delta}(A)+\mu_{\delta}(B)\le\sum_{C\in\mathscr{C}_{A}}\tau (C)+\sum_{C\in\mathscr{C}_{B}}\tau (C)
\le\sum_{C\in\mathscr{C}}\tau (C) \]
が成り立つ。従って右辺の下限を取れば
\[ \mu_{\delta}(A)+\mu_{\delta}(B)\le\mu_{\delta}(A\sqcup B)\le\mu (A\sqcup B) \]
を得る。左辺の上限を取れば$\mu (A)+\mu (B)\le\mu (A\sqcup B)$が従う。逆は明らか。
\end{Proof}

\begin{Def}
特に$\alpha\ge 0$に対して$\mathscr{E}=2^{X}, \tau (A):=|A|^{\alpha}$としたとき
$\mu_{\delta}, \mu$をそれぞれ$\mathcal{H}_{\delta}^{\alpha}, \mathcal{H}^{\alpha}$と書く。
$\mathcal{H}^{\alpha}$により生成される測度を$\alpha$-次元ハウスドルフ測度\textup{($\alpha$-dimensional Hausdorff measure)}と呼ぶ。
\end{Def}

\begin{Rem}
$\alpha\ge 0, \delta>0$及び$A\subset X$に対し
\[ P_{\delta}^{\alpha}(A):=\sup\left\{\sum |B_{n}|^{\alpha}\mid
B_{n}=B(x_{n}; r_{n}), x_{n}\in A, r_{n}\le\delta, B_{i}\cap B_{j}=\emptyset\right\} \]
と定める。つまり$A$の点を中心とする半径$\delta$以下の互いに素な閉球全体を考え、その直径の$\alpha$乗の和の上限を取る。
このとき集合関数$P_{0}^{\alpha}:2^{X}\rightarrow [0, \infty]$を$A\subset X$に対し
\[ P_{0}^{\alpha}(A):=\inf_{\delta}P_{\delta}^{\alpha}(A) \]
と定め、この関数により生成される外測度
\[ P^{\alpha}(A):=\inf\left\{\sum_{C\in\mathscr{C}} P_{0}^{\alpha}(C)\mid
\mathscr{C}\subset 2^{X}\textup{は$A$の被覆}\right\} \]
を$\alpha$-次元パッキング測度\textup{($\alpha$-dimensional packing measure)}と呼ぶ。
\end{Rem}

-->