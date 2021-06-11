

# ハール測度

ルベーグ測度には平行移動不変性があるが、ハール測度はこの一般化にあたる。

__定義__ 位相空間$(X, \mathcal{O})$のコンパクト部分集合全体を$\mathcal{K}$と書く。集合函数$\lambda\colon\mathcal{K}\rightarrow\lbrack 0, \infty \rbrack$は以下を満たすとする。

- コンパクトな$K\subset X$について$\lambda (K)<\infty$であり、$\lambda (\emptyset)=0$である。
- コンパクトな$A, B\subset X$について、$A\subset B$なら$\lambda (A)\le\lambda (B)$を満たす。（単調性）
- コンパクトな$A, B\subset X$について、$\lambda (A\cup B)\le\lambda (A)+\lambda (B)$が成り立つ。（有限劣加法性）
- 上の状況で$A\cap B=\emptyset$なら等号が成り立つ。（有限加法性）

このとき$\lambda$を **容量** （content）と呼ぶ。

> コンパクト集合同士の和はコンパクト集合であった。

　容量から外測度に近い概念を定義することができる。

__定義__ $\lambda\colon\mathcal{K}\rightarrow \lbrack 0, \infty \rbrack$を位相空間$(X, \mathcal{O})$上の容量とする。$A\subset X$とする。

$$
\lambda_{\ast}(A):=\sup\lbrace \lambda (K) : K\in\mathcal{K}, K\subset A \rbrace
$$

を$A$の内部容量（inner content）と呼ぶ。

> $\lambda_{\ast}$は単調で、かつ$\lambda_{\ast}(\emptyset)=0$を満たす。位相空間にハウスドルフ性を認めれば$\mathcal{O}$上の可算劣加法性が従う。

__命題__ 位相空間$(X, \mathcal{O})$はハウスドルフ空間とする。このとき$\lambda_{\ast}$の$\mathcal{O}$への制限$\lambda_{\ast}\vert_{\mathcal{O}}$は可算劣加法的かつ有限加法的である。

（証明）まずハウスドルフ空間における事実として、コンパクトな$K\subset X$と開集合$U_{1}, U_{2}$について$K\subset U_{1}\cup U_{2}$とすると、あるコンパクトな$K_{j}\subset X$が存在して$K=K_{1}\cup K_{2}, K_{j}\subset U_{j}$が成り立つことが知られている。

$\mathcal{O}$上での可算劣加法性を示そう。$U_{n}\in\mathcal{O}$とする。コンパクトな$K\subset\bigcup U_{n}$について、ある有限集合$F\subset\mathbb{N}$により$K\subset\bigcup_{n\in F}U_{n}$と表せる。従って先の事実より、$K=\bigcup_{n\in F}K_{n}$を満たすコンパクトな$K_{n}\subset U_{n}$が存在する。$\lambda$の有限劣加法性と$\lambda_{\ast}$の定義より

$$
\lambda (K)\le\sum_{n\in F}\lambda (K_{n})\le\sum_{n\in F}\lambda_{\ast}(U_{n})\le\sum\lambda_{\ast}(U_{n})
$$

が成り立つ。左辺の上限を取れば$\lambda_{\ast}\left(\bigcup I_{n}\right)\le\sum\lambda_{\ast}(U_{n})$を得る。

$U_{1}, \dotsc, U_{n}\in\mathcal{O}$は互いに素とする。コンパクトな$K_{j}\subset U_{j}$を取ると、$K_{1}, \dotsc, K_{n}$は互いに素で、$\bigcup_{j=1}^{n}K_{j}$はコンパクトかつ$\bigcup_{j=1}^{n}K_{j}\subset\bigcup_{j=1}^{n}U_{j}$を満たす。$\lambda$の有限加法性より

$$
\sum_{j=1}^{n}\lambda (K_{j})=\lambda\left(\bigcup_{j=1}^{n}K_{j}\right)\le\lambda_{\ast}\left(\bigcup_{j=1}^{n}U_{j}\right)
$$

だから、左辺の上限を取れば$\sum_{j=1}^{n}\lambda_{\ast}(U_{j})\le\lambda_{\ast}\left(\bigcup_{j=1}^{n}U_{j}\right)$を得る。$\square$

　ハウスドルフ空間上に容量が定まっているとき、その内部容量から外測度が構成できる。

__命題__ $(X, \mathcal{O})$をハウスドルフ空間、$\lambda$を容量とする。$A\subset X$に対し

$$
\widehat{\lambda}(A):=\inf\lbrace \lambda_{\ast}(U)\mid U\in\mathcal{O}, A\subset U \rbrace
$$

と定めれば、$\widehat{\lambda}$は外測度になる。

（証明）まず$\widehat{\lambda}|_{\mathcal{O}}=\lambda_{\ast}|_{\mathcal{O}}$であることを示す。$U\in\mathcal{O}$に対し$U$自身が$U$を含む開集合だから$\widehat{\lambda}(U)\le\lambda_{\ast}(U)$である。一方$\lambda_{\ast}$の単調性より、$O\in\mathcal{O}, U\subset O$に対し$\lambda_{\ast}(U)\le\lambda_{\ast}(O)$が成り立つ。故に$\lambda_{\ast}(U)\le\widehat{\lambda}(U)$である。特に$\widehat{\lambda}(\emptyset)=\lambda_{\ast}(\emptyset)=0$が分かる。

$\widehat{\lambda}$が単調であることは良い。可算劣加法性を示す。$A_{n}\subset X$について$\sum\widehat{\lambda}(A_{n})<\infty$とする。$\varepsilon>0$を取る。$\widehat{\lambda}$の定義から、適当な開集合$U_{n}$を取り$A_{n}\subset U_{n}$かつ

$$
\lambda_{\ast}(U_{n})\le\widehat{\lambda}(A_{n})+\frac{\varepsilon}{2^{n}}
$$

を満たすようにできる。このとき

$$
\begin{aligned}
\widehat{\lambda}\left(\bigcup A_{n}\right)
&\le\widehat{\lambda}\left(\bigcup U_{n}\right)=\lambda_{\ast}\left(\bigcup U_{n}\right) \\
&\le\sum\lambda_{\ast}(U_{n})\le\sum\widehat{\lambda}(A_{n})+\varepsilon
\end{aligned}
$$

となる。$\varepsilon$は任意だから可算劣加法性が成り立つ。$\square$

$\widehat{\lambda}$可測な集合全体を$\mathcal{M}_{\widehat{\lambda}}$とすれば、$\widehat{\lambda}:\mathcal{M}_{\widehat{\lambda}}\rightarrow \lbrack 0, \infty \rbrack$は測度となる。

__命題__ $(X, \mathcal{O})$はハウスドルフ空間、$\lambda\colon\mathcal{K}\rightarrow \lbrack 0, \infty \rbrack$は容量とする。$\mu\colon\mathscr{A}\rightarrow \lbrack 0, \infty \rbrack$は測度で$\sigma\lbrack \mathcal{O} \rbrack\subset\mathscr{A}$を満たすとする。このとき$\mu|_{\sigma\lbrack \mathcal{O} \rbrack}=\widehat{\lambda}|_{\sigma\lbrack \mathcal{O} \rbrack}$であれば、$A\in\sigma\lbrack \mathcal{O} \rbrack$は$\mu$外部正則であり、$U\in\mathcal{O}$は$\mu$内部正則になる。

> 一般のボレル集合が$\mu$内部正則になるとは限らない。

（証明）$A\in\sigma \lbrack \mathcal{O} \rbrack$に対し$\mu (A)=\widehat{\lambda}(A)=\inf_{A\subset O\in\mathcal{O}}\lambda_{\ast}(O)$である。ここで$\lambda_{\ast}(O)=\widehat{\lambda}(O)=\mu (O)$であるから、$A$は$\mu$-外部正則となる。

$U\in\mathcal{O}$に対し、$\mu (U)=\widehat{\lambda}(U)=\lambda_{\ast}(U)=\sup_{U\supset K\in\mathcal{K}}\lambda (K)$である。ここで$K\subset O\in\mathcal{O}$に対して$\lambda_{\ast}(O)$の定義により$\lambda (K)\le\lambda_{\ast}(O)$が成り立つ。右辺の下限を取れば$\lambda (K)\le\widehat{\lambda}(K)$が従う。よって$\mu (U)\le\sup_{U\supset K\in\mathcal{K}}\widehat{\lambda}(K)$を得るが、逆の不等号は明らかなので、$U$は$\mu$-内部正則となる。$\square$

> 上記の$\mu$を、$\lambda$により誘導された測度とも言う。この測度は以下の意味で$\mathcal{K}$により特徴付けられる。

__命題__ $(X, \mathcal{O}), (Y, \mathcal{T})$をハウスドルフ空間、$h\colon X\rightarrow Y$は同相写像とする。$\lambda, \gamma$を$X, Y$上の容量として、これらにより誘導された測度を$\mu\colon \mathcal{A}\rightarrow \lbrack 0, \infty \rbrack, \nu\colon \mathcal{B}\rightarrow \lbrack 0, \infty \rbrack$とする。任意のコンパクト集合$K\Subset X$に対して$\gamma (h(K))=\lambda (K)$が成り立つとする。このとき$A\in\sigma\lbrack \mathcal{O} \rbrack$に対して$\nu (h(A))=\mu (A)$が成り立つ。

（照明）以下$\mathcal{O}, \mathcal{T}$のコンパクト集合全体を$\mathcal{K}, \mathcal{L}$で表す。まず$U\in\mathcal{O}$に対して

$$
\begin{aligned}
\lbrace \lambda (K)\mid K\in\mathcal{K}, K\subset U \rbrace&=\lbrace \gamma (h(K))\mid K\in\mathcal{K}, K\subset U \rbrace \\
&=\lbrace \gamma (L)\mid L=h(K), K\in\mathcal{K}, K\subset U \rbrace \\
&=\lbrace \gamma (L)\mid L\in\mathcal{L}, L\subset h(U) \rbrace
\end{aligned}
$$

が成り立つので$\lambda_{\ast}(U)=\gamma_{*}(h(U))$が従う。次に$A\subset X$に対して

$$
\begin{aligned}
\lbrace \lambda_{\ast}(U)\mid U\in\mathcal{O}, A\subset U \rbrace&=\lbrace \gamma_{*}(h(U))\mid U\in\mathcal{O}, A\subset U \rbrace \\
&=\lbrace \gamma_{*}(V)\mid V=h(U), U\in\mathcal{O}, A\subset U \rbrace \\
&=\lbrace \gamma_{*}(V)\mid V\in\mathcal{T}, h(A)\subset V \rbrace
\end{aligned}
$$

が成り立つので$\widehat{\lambda}(A)=\widehat{\gamma}(h(A))$が成り立つ。特に$A\in\sigma\lbrack \mathcal{O} \rbrack\subset\mathscr{A}$なら$h(A)\in\sigma\lbrack \mathcal{T} \rbrack\subset\mathscr{B}$であるから、

$$
\mu (A)=\widehat{\lambda}(A)=\widehat{\gamma}(h(A))=\nu (h(A))
$$

を得る。$\square$

<!--
　局所コンパクトな位相群が容量を持つことを示そう。その前に、位相群におけるコンパクト集合の性質に触れておく。

\begin{Lem}
$G$を位相群、$K\Subset G$はコンパクトであるとする。$K\subset U$なる開集合$U$に対し、$1$の開近傍$V$を取り、
$KV=\lbrace xy\mid x\in K, y\in V \rbrace\subset U$とできる。
\end{Lem}
\begin{Proof}
$x\in K$に対し$W_{x}:=x^{-1}U$とおくと$x\in U$より$W_{x}$は$1$の開近傍となる。
そこで$1$の開近傍$V_{x}\subset W_{x}$を$V_{x}V_{x}\subset W_{x}$となるように取る。
このとき$\lbrace x V_{x}\mid x\in K \rbrace$は$K$の開被覆となるから、コンパクト性より$x_{1}, \dotsc, x_{n}\in K$を取り
$K\subset\bigcup_{j=1}^{n}x_{j}V_{x_{j}}$と表せる。$V:=\bigcap_{j=1}^{n}V_{x_{j}}$と定めると$1$の開近傍である。
このとき$x\in K$に対し$x\in x_{j}V_{x_{j}}$となる$x_{j}$が取れるので、
\\lbrack  xV\subset x_{j}V_{x_{j}}V\subset x_{j}V_{x_{j}}V_{x_{j}}\subset x_{j}W_{x_{j}}=U \ \rbrack
を得る。
\end{Proof}

　$G$を局所コンパクトハウスドルフ位相群とする。
$K\Subset G$をコンパクトな部分集合、$V\subset G$は内点を持つとする。即ち$V^{\circ}\neq\emptyset$であるとする。
このとき$\lbrace gV^{\circ}\mid g\in G \rbrace$は$K$の開被覆となるから、有限個の$g_{1}, \dotsc, g_{n}\in G$を選び
$K\subset\bigcup_{j=1}^{n}gV^{\circ}$とできる。このような被覆が存在する$n$の内、最小のものを$\#(K:V)$で表す。

　以下$G$のコンパクト集合全体を$\mathcal{K}$、$1$の開近傍全体を$\mathcal{U}$で表す。
$G$は局所コンパクトであるから、$1$のコンパクト近傍$K_{0}$が存在する。\footnote{位相群の位相は$1$の近傍系で記述できた。}
そこで$U\in\mathcal{U}$に対し、写像$\lambda_{U}:\mathcal{K}\rightarrow \lbrack 0, \infty \rbrack$を
\\lbrack  \lambda_{U}(K):=\frac{\#(K:U)}{\#(K_{0}:U)} \ \rbrack
で定める。ここで$K_{0}$は近傍だから$\#(K_{0}:U)\neq 0$となることに注意する。

　このとき$0\le\lambda_{U}(K)\le\#(K:K_{0})<\infty$が成り立つ。実際$\#(K:U)\le\#(K:K_{0})\#(K_{0}:U)$を示せばよいが、
これは被覆を考えれば明らかである。故に$\lambda_{U}$は
\\lbrack  \Lambda:=\prod_{K\in\mathcal{K}}\lbrack 0, \#(K:K_{0}) \rbrack \ \rbrack
の元と見なせる。この$\Lambda$はチコノフの定理によりコンパクトである。\footnote{選択公理を用いている。}
$V\in\mathscr{U}$に対し、
\\lbrack  \Lambda (V):=\overline{\lbrace \lambda_{U}\mid U\in\mathscr{U}, U\subset V \rbrace} \ \rbrack
と定める。もし$\lbrace \Lambda (V)\mid V\in\mathscr{U} \rbrace$が有限交叉性を持てば、
$\Lambda$がコンパクトであることから
\\lbrack  \bigcap_{V\in\mathscr{U}}\Lambda (V)\neq\emptyset \ \rbrack
が従う。

　実際に$V_{1}, \dotsc, V_{n}\in\mathscr{U}$を取れば、$V:=\bigcap_{j=1}^{n}V_{j}\in\mathscr{U}$であり、
$\lambda_{V}\in\bigcap_{j=1}^{n}\Lambda (V_{j})$となるから$\lbrace \Lambda (V)\mid V\in\mathscr{U} \rbrace$は有限交叉性を持つ。
つまり$\lambda\in\bigcap_{V\in\mathscr{U}}\Lambda (V)$が取れる。
\footnote{ここまでハウスドルフ性は用いていない。しかし$\lambda$が容量であることを示すのに必要となる。}

\begin{Prop}
上記の$\lambda\in\bigcap_{V\in\mathscr{U}}\Lambda (V)$は容量である。
\end{Prop}
\begin{Proof}
(i)　まず$\lambda\in\Lambda$より$\lambda (K)<\infty$が任意の$K\in\mathcal{K}$が成り立つ。
特に$K=\emptyset$のとき、$\#(\emptyset:K_{0})=0$だから$\Lambda$の$\emptyset\in\mathcal{K}$成分は一点になる。
つまり$\lambda (\emptyset)=0$を得る。

　(ii)　$K_{1}, K_{2}\in\mathcal{K}$が$K_{1}\subset K_{2}$を満たすとする。$U\in\mathscr{U}$に対し
$\#(K_{1}:U)\le\#(K_{2}:U)$より$\lambda_{U}(K_{1})\le\lambda_{U}(K_{2})$は明らか。
そこで$f\in\Lambda$に対し$f(K_{2})-f(K_{1})$を対応させる写像$\Lambda\rightarrow\mathbb{R}$は、射影と差の合成なので連続写像となる。
この写像は$\lbrace \lambda_{U}\mid U\in\mathscr{U} \rbrace$上で非負であるから、$\Lambda (V)$上でも非負となる。
よって$\lambda (K_{2})-\lambda (K_{1})\ge 0$を得る。

　(iii)　$K_{1}, K_{2}\in\mathcal{K}$を取る。$U\in\mathscr{U}$に対し、$U$による$K_{1}$の被覆と$K_{2}$の被覆を合わせると
$K_{1}\cup K_{2}$の被覆となるから$\#(K_{1}\cup K_{2}:U)\le\#(K_{1}:U)+\#(K_{2}:U)$となる。
つまり$\lambda_{U}(K_{1}\cup K_{2})\le\lambda_{U}(K_{1})+\lambda_{U}(K_{2})$が分かる。
(ii)と同様に考えれば$\lambda (K_{1}\cup K_{2})\le\lambda (K_{1})+\lambda (K_{2})$が従う。

　(iv)　$K_{1}\cap K_{2}=\emptyset$とする。このとき$G$はハウスドルフ空間だから、互いに素な開集合$U_{1}, U_{2}$を取り
$K_{1}\subset U_{1}, K_{2}\subset U_{2}$とできる。補題より$K_{1}V_{1}\subset U_{1}, K_{2}V_{2}\subset U_{2}$なる
$1$の開近傍$V_{1}, V_{2}$が取れる。そこで$V:=V_{1}\cap V_{2}$と置くと、$K_{1}V\cap K_{2}V=\emptyset$である。
$U\in\mathscr{U}$が$U\subset V^{-1}$を満たすとする。このとき$K_{1}U^{-1}\cap K_{2}U^{-1}=\emptyset$であるが、
$\lambda_{U}(K_{1}\sqcup K_{2})=\lambda_{U}(K_{1})+\lambda_{U}(K_{2})$となる。
実際$n:=\#(K_{1}\sqcup K_{2}:U)$と置き、$K_{1}\sqcup K_{2}\subset\bigcup_{j=1}^{n}g_{j}U$となる被覆を取る。
ここで$g_{j}U\cap K_{1}, g_{j}U\cap K_{2}\neq\emptyset$なら$g_{j}\in K_{1}U^{-1}\cap K_{2}U^{-1}$となるから矛盾する。
従って$g_{j}U$は$K_{1}, K_{2}$の一方のみとしか交わらない。よって$\#(K_{1}:U)+\#(K_{2}:U)\le\#(K_{1}\sqcup K_{2}:U)$が分かる。
結局$f\in\Lambda$に対し$f(K_{1})+f_(K_{2})-f(K_{1}\sqcup K_{2})$を対応させる連続写像は
$\Lambda(V^{-1})$上で恒等的に$0$となり、よって$\lambda (K_{1}\sqcup K_{2})=\lambda (K_{1})+\lambda (K_{2})$を得る。
\end{Proof}

\begin{Thm}
$G$を局所コンパクトハウスドルフ位相群とする。ボレル集合体を$\mathscr{B}(G)=\sigma\lbrack \mathcal{O} \rbrack$と書く。
以下を満たす測度$\mu:\mathscr{B}(G)\rightarrow \lbrack 0, \infty \rbrack$が存在する。
\begin{itemize}
\item\lbrack \textup{(i)} \rbrack $G$のコンパクト集合全体$\mathcal{K}$上で有限値を取る。つまり$K\in\mathcal{K}$なら$\mu (K)<\infty$を満たす。
\item\lbrack \textup{(ii)} \rbrack $\mu$は外部正則である。
\item\lbrack \textup{(iii)} \rbrack 開集合$O\in\mathcal{O}$は$\mu$-内部正則である。
\item\lbrack \textup{(iv)} \rbrack 左移動で不変である。つまり任意の$A\in\mathscr{B}$に対して$\mu (gA)=\mu (A)$が成り立つ。
\end{itemize}
\end{Thm}
\begin{Proof}
$\lambda$を上で得た容量とする。このとき$\sigma\lbrack \mathcal{O} \rbrack\subset\mathcal{M}_{\widehat{\lambda}}$が成り立つ。
$U\in\mathcal{O}$が$\widehat{\lambda}$-可測であることを示せばよい。$A\subset G$及び$\varepsilon>0$を取る。
$\widehat{\lambda}(A)=\inf_{A\subset U\in\mathcal{O}}\lambda_{\ast}(O)$であるから、ある$O\in\mathcal{O}$が存在して
\\lbrack  A\subset O, \lambda_{\ast}(O)\le\widehat{\lambda}(A)+\frac{\varepsilon}{3} \ \rbrack
を満たすように取れる。ここで$O\cap U$は開集合だから
$\widehat{\lambda}(O\cap U)=\lambda_{\ast}(O\cap U)=\sup_{O\cap U\supset K\in\mathcal{K}}\lambda (K)$である。
よってある$K\in\mathcal{K}$が存在して
\\lbrack  K\subset O\cap U, \widehat{\lambda}(O\cap U)-\frac{\varepsilon}{3}\le\lambda (K) \ \rbrack
を満たすように取れる。更に$O\backslash K$も開集合だから、同様にして$L\in\mathcal{K}$を
\\lbrack  L\subset O\backslash K, \widehat{\lambda}(O\backslash K)-\frac{\varepsilon}{3}\le\lambda (L) \ \rbrack
を満たすように取れる。$K\subset U$より$O\backslash U\subset O\backslash K$となり、また$K\cap L=\emptyset$であるから、
\begin{align*}
\widehat{\lambda}(A\cap U)+\widehat{\lambda}(A\backslash U)-\frac{2}{3}\varepsilon
&\le\widehat{\lambda}(O\cap U)+\widehat{\lambda}(O\backslash U)-\frac{2}{3}\varepsilon \\
&\le\lambda (K)+\widehat{\lambda}(O\backslash K)-\frac{\varepsilon}{3} \\
&\le\lambda (K)+\lambda (L)=\lambda (K\sqcup L)\\
&\le\lambda_{\ast}((O\cap U)\cup (O\backslash K))=\lambda_{\ast}(O) \\
&\le\widehat{\lambda}(A)+\frac{\varepsilon}{3}
\end{align*}
となる。つまり
\\lbrack  \widehat{\lambda}(A\cap U)+\widehat{\lambda}(A\backslash U)\le\widehat{\lambda}(A)+\varepsilon \ \rbrack
であるから、$\varepsilon$が任意に取れたので$U$は$\widehat{\lambda}$-可測となる。

　以上により$\mu:=\widehat{\lambda}|_{\sigma\lbrack \mathcal{O} \rbrack}$が求める測度となる。後は$\mathcal{K}$上で有限値を取ることを示せばよい。
$K\in\mathcal{K}$を取る。$x\in K$に対しコンパクトな近傍$K_{x}$を取れるが、このとき$\lbrace K_{x}^{\circ} \rbrace$は$K$の開被覆となる。
$K$はコンパクトだから有限個の$K_{1}, \dotsc, K_{n}$を取り、$K\subset\bigcup_{j=1}^{n}K_{j}^{\circ}$とできる。
このとき$L:=\bigcup_{j=1}^{n}K_{j}$とすれば$K\subset L^{\circ}\subset L$が従う。故に
\\lbrack  \widehat{\lambda}(K)\le\lambda_{\ast}(L^{\circ})\le\lambda_{\ast}(L)=\lambda (L)<\infty \ \rbrack
を得る。
\end{Proof}

\begin{Def}
定理の条件を満たす測度を左不変ハール測度\textup{(left-invariant Haar measure)}と呼ぶ。
条件\textup{(iv)}を以下の\textup{(iv$^{\prime}$)}に変えた条件を満たす測度を右不変ハール測度と呼ぶ。
\begin{itemize}
\item\lbrack \textup{(iv$^{\prime}$)} \rbrack 右移動で不変である。つまり$A\in\mathscr{B}$に対して$\mu (Ag)=\mu (A)$が成り立つ。
\end{itemize}
両方の条件を満たす測度を両側不変ハール測度と呼ぶ。
\end{Def}



-->