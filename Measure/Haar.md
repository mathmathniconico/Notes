

# ハール測度

ルベーグ測度には平行移動不変性がある。ハール測度はこの一般化にあたる。

__定義__ 位相空間$(X, \mathcal{O})$のコンパクト部分集合全体を$\mathcal{K}$と書くことにする。集合関数$\lambda:\mathcal{K}\rightarrow [0, \infty]$が以下の条件を満たすとき、容量あるいはコンテント\textup{(content)}と呼ぶ。

- 任意の$K\in\mathcal{K}$に対して$\lambda (K)<\infty$であり、$\lambda (\emptyset)=0$を満たす。
- 単調性が成り立つ。即ち$A, B\in\mathcal{K}, A\subset B$なら$\lambda (A)\le\lambda (B)$を満たす。
- 有限劣加法性が成り立つ。$A, B\in\mathcal{K}$なら$\lambda (A\cup B)\le\lambda (A)+\lambda (B)$が成り立つ。
- 有限加法性が成り立つ。つまり\textup{(iii)}で$A\cap B=\emptyset$なら等号が成り立つ。

> コンパクト集合同士の和はコンパクト集合であった。また$\mathcal{K}$が適当な集合演算で閉じてないので、これらの条件を纏めることはできない。

<!--

　容量から外測度に近い概念を定義することができる。

\begin{Def}
$\lambda:\mathcal{K}\rightarrow [0, \infty]$を位相空間$(X, \mathcal{O})$上の容量とする。$A\subset X$に対し、
\[ \lambda_{*}(A):=\sup\{\lambda (K)\mid K\in\mathcal{K}, K\subset A\} \]
を$A$の内部容量\textup{(inner content)}と呼ぶ。
\end{Def}

　$\lambda_{*}$は単調で、かつ$\lambda_{*}(\emptyset)=0$を満たす。
位相空間にハウスドルフ性を認めれば$\mathcal{O}$上の可算劣加法性が従う。

\begin{Prop}
位相空間$(X, \mathcal{O})$はハウスドルフ空間とする。
このとき$\lambda_{*}|_{\mathcal{O}}$は可算劣加法的かつ有限加法的である。
\end{Prop}
\begin{Proof}
まず位相空間論における事実から
$K\in\mathcal{K}, U_{1}, U_{2}\in\mathcal{O}$に対し$K\subset U_{1}\cup U_{2}$であるとする。
このとき$K_{j}\in\mathcal{K}$を$K=K_{1}\cup K_{2}, K_{j}\subset U_{j}$を満たすように取れる。

　$\mathcal{O}$上での可算劣加法性を示そう。$\{U_{n}\}\subset\mathcal{O}$とする。
$K\subset\bigcup U_{n}, K\in\mathcal{K}$に対してコンパクト性より有限集合$F\subset\mathbb{N}$が取れ、
$K\subset\bigcup_{n\in F}U_{n}$とできる。このとき先に述べた事実により$K_{n}\in\mathcal{K}$が存在して
$K=\bigcup_{n\in F}K_{n},\, K_{n}\subset U_{n}$を満たすようにできる。$\lambda$の有限劣加法性と$\lambda_{*}$の定義より
\[ \lambda (K)\le\sum_{n\in F}\lambda (K_{n})\le\sum_{n\in F}\lambda_{*}(U_{n})\le\sum\lambda_{*}(U_{n}) \]
が成り立つ。左辺の上限を取れば$\lambda_{*}\left(\bigcup I_{n}\right)\le\sum\lambda_{*}(U_{n})$を得る。

　互いに素な$U_{1}, \dotsc, U_{n}\in\mathcal{O}$を取る。$K_{j}\subset U_{j}, K_{j}\in\mathcal{K}$を取れば互いに素で、
$\bigcup_{j=1}^{n}K_{j}\in\mathcal{K}$かつ$\bigcup_{j=1}^{n}K_{j}\subset\bigcup_{j=1}^{n}U_{j}$を満たす。
\[ \sum_{j=1}^{n}\lambda (K_{j})=\lambda\left(\bigcup_{j=1}^{n}K_{j}\right)\le\lambda_{*}\left(\bigcup_{j=1}^{n}U_{j}\right) \]
だから、左辺の上限を取れば$\sum_{j=1}^{n}\lambda_{*}(U_{j})\le\lambda_{*}\left(\bigcup_{j=1}^{n}U_{j}\right)$を得る。
\end{Proof}

　ハウスドルフ空間上に容量が定まっているとき、その内部容量から外測度が構成できる。

\begin{Prop}
$(X, \mathcal{O})$をハウスドルフ空間、$\lambda$を容量とする。$A\subset X$に対し
\[ \widehat{\lambda}(A):=\inf\{\lambda_{*}(U)\mid U\in\mathcal{O}, A\subset U\} \]
と定めれば、$\widehat{\lambda}$は外測度になる。
\end{Prop}
\begin{Proof}
まず$\widehat{\lambda}|_{\mathcal{O}}=\lambda_{*}|_{\mathcal{O}}$であることを示す。
$U\in\mathcal{O}$に対し$U$自身が$U$を含む開集合だから$\widehat{\lambda}(U)\le\lambda_{*}(U)$である。
一方$\lambda_{*}$の単調性より、$O\in\mathcal{O}, U\subset O$に対し$\lambda_{*}(U)\le\lambda_{*}(O)$が成り立つ。
故に$\lambda_{*}(U)\le\widehat{\lambda}(U)$である。
特に$\widehat{\lambda}(\emptyset)=\lambda_{*}(\emptyset)=0$が分かる。

　$\widehat{\lambda}$が単調であることは良い。故に可算劣加法性を示す。
このとき$\{A_{n}\}\subset 2^{X}$に対し、$\sum\widehat{\lambda}(A_{n})<\infty$と仮定して良い。
$\varepsilon>0$を取る。$\widehat{\lambda}$の定義から、適当な開集合$U_{n}$を、$A_{n}\subset U_{n}$かつ
\[ \lambda_{*}(U_{n})\le\widehat{\lambda}(A_{n})+\frac{\varepsilon}{2^{n}} \]
を満たすように取れる。このとき
\begin{align*}
\widehat{\lambda}\left(\bigcup A_{n}\right)
&\le\widehat{\lambda}\left(\bigcup U_{n}\right)=\lambda_{*}\left(\bigcup U_{n}\right) \\
&\le\sum\lambda_{*}(U_{n})\le\sum\widehat{\lambda}(A_{n})+\varepsilon
\end{align*}
となる。$\varepsilon$は任意だから可算劣加法性が成り立つ。
\end{Proof}

　$\widehat{\lambda}$-可測な集合全体を$\mathcal{M}_{\widehat{\lambda}}$とすれば、
$\widehat{\lambda}:\mathcal{M}_{\widehat{\lambda}}\rightarrow [0, \infty]$は測度となる。

\begin{Prop}
$(X, \mathcal{O})$はハウスドルフ空間、$\lambda:\mathcal{K}\rightarrow [0, \infty]$は容量とする。
$\mu:\mathscr{A}\rightarrow [0, \infty]$は測度で$\sigma[\mathcal{O}]\subset\mathscr{A}$を満たすとする。
このとき$\mu|_{\sigma[\mathcal{O}]}=\widehat{\lambda}|_{\sigma[\mathcal{O}]}$であれば、
$A\in\sigma[\mathcal{O}]$は$\mu$-外部正則であり、$U\in\mathcal{O}$は$\mu$-内部正則になる。
\footnote{一般のボレル集合が$\mu$-内部正則になるとは限らない。}
\end{Prop}
\begin{Proof}
$A\in\sigma[\mathcal{O}]$に対し$\mu (A)=\widehat{\lambda}(A)=\inf_{A\subset O\in\mathcal{O}}\lambda_{*}(O)$である。
ここで$\lambda_{*}(O)=\widehat{\lambda}(O)=\mu (O)$であるから、$A$は$\mu$-外部正則となる。
また$U\in\mathcal{O}$に対し、$\mu (U)=\widehat{\lambda}(U)=\lambda_{*}(U)=\sup_{U\supset K\in\mathcal{K}}\lambda (K)$である。
ここで$K\subset O\in\mathcal{O}$に対して$\lambda_{*}(O)$の定義により$\lambda (K)\le\lambda_{*}(O)$が成り立つ。
右辺の下限を取れば$\lambda (K)\le\widehat{\lambda}(K)$が従う。
よって$\mu (U)\le\sup_{U\supset K\in\mathcal{K}}\widehat{\lambda}(K)$を得るが、逆の不等号は明らかなので、
$U$は$\mu$-内部正則となる。
\end{Proof}

　上記の$\mu$を、$\lambda$により誘導された測度とも言う。この測度は以下の意味で$\mathcal{K}$により特徴付けられる。

\begin{Prop}
$(X, \mathcal{O}), (Y, \mathcal{T})$をハウスドルフ空間、$h:X\rightarrow Y$は同相写像とする。
$\lambda, \gamma$を$X, Y$上の容量として、これらにより誘導された測度を
$\mu:\mathcal{A}\rightarrow [0, \infty], \nu:\mathcal{B}\rightarrow [0, \infty]$とする。
任意のコンパクト集合$K\Subset X$に対して$\gamma (h(K))=\lambda (K)$が成り立つとする。
このとき$A\in\sigma[\mathcal{O}]$に対して$\nu (h(A))=\mu (A)$が成り立つ。
\end{Prop}
\begin{Proof}
以下$\mathcal{O}, \mathcal{T}$のコンパクト集合全体を$\mathcal{K}, \mathcal{L}$で表す。
まず$U\in\mathcal{O}$に対して
\begin{align*}
\{\lambda (K)\mid K\in\mathcal{K}, K\subset U\}&=\{\gamma (h(K))\mid K\in\mathcal{K}, K\subset U\} \\
&=\{\gamma (L)\mid L=h(K), K\in\mathcal{K}, K\subset U\} \\
&=\{\gamma (L)\mid L\in\mathcal{L}, L\subset h(U)\}
\end{align*}
が成り立つので$\lambda_{*}(U)=\gamma_{*}(h(U))$が従う。次に$A\subset X$に対して
\begin{align*}
\{\lambda_{*}(U)\mid U\in\mathcal{O}, A\subset U\}&=\{\gamma_{*}(h(U))\mid U\in\mathcal{O}, A\subset U\} \\
&=\{\gamma_{*}(V)\mid V=h(U), U\in\mathcal{O}, A\subset U\} \\
&=\{\gamma_{*}(V)\mid V\in\mathcal{T}, h(A)\subset V\}
\end{align*}
が成り立つので$\widehat{\lambda}(A)=\widehat{\gamma}(h(A))$が成り立つ。
特に$A\in\sigma[\mathcal{O}]\subset\mathscr{A}$なら$h(A)\in\sigma[\mathcal{T}]\subset\mathscr{B}$であるから、
\[ \mu (A)=\widehat{\lambda}(A)=\widehat{\gamma}(h(A))=\nu (h(A)) \]
を得る。
\end{Proof}

　局所コンパクトな位相群が容量を持つことを示そう。その前に、位相群におけるコンパクト集合の性質に触れておく。

\begin{Lem}
$G$を位相群、$K\Subset G$はコンパクトであるとする。$K\subset U$なる開集合$U$に対し、$1$の開近傍$V$を取り、
$KV=\{xy\mid x\in K, y\in V\}\subset U$とできる。
\end{Lem}
\begin{Proof}
$x\in K$に対し$W_{x}:=x^{-1}U$とおくと$x\in U$より$W_{x}$は$1$の開近傍となる。
そこで$1$の開近傍$V_{x}\subset W_{x}$を$V_{x}V_{x}\subset W_{x}$となるように取る。
このとき$\{x V_{x}\mid x\in K\}$は$K$の開被覆となるから、コンパクト性より$x_{1}, \dotsc, x_{n}\in K$を取り
$K\subset\bigcup_{j=1}^{n}x_{j}V_{x_{j}}$と表せる。$V:=\bigcap_{j=1}^{n}V_{x_{j}}$と定めると$1$の開近傍である。
このとき$x\in K$に対し$x\in x_{j}V_{x_{j}}$となる$x_{j}$が取れるので、
\[ xV\subset x_{j}V_{x_{j}}V\subset x_{j}V_{x_{j}}V_{x_{j}}\subset x_{j}W_{x_{j}}=U \]
を得る。
\end{Proof}

　$G$を局所コンパクトハウスドルフ位相群とする。
$K\Subset G$をコンパクトな部分集合、$V\subset G$は内点を持つとする。即ち$V^{\circ}\neq\emptyset$であるとする。
このとき$\{gV^{\circ}\mid g\in G\}$は$K$の開被覆となるから、有限個の$g_{1}, \dotsc, g_{n}\in G$を選び
$K\subset\bigcup_{j=1}^{n}gV^{\circ}$とできる。このような被覆が存在する$n$の内、最小のものを$\#(K:V)$で表す。

　以下$G$のコンパクト集合全体を$\mathcal{K}$、$1$の開近傍全体を$\mathcal{U}$で表す。
$G$は局所コンパクトであるから、$1$のコンパクト近傍$K_{0}$が存在する。\footnote{位相群の位相は$1$の近傍系で記述できた。}
そこで$U\in\mathcal{U}$に対し、写像$\lambda_{U}:\mathcal{K}\rightarrow [0, \infty]$を
\[ \lambda_{U}(K):=\frac{\#(K:U)}{\#(K_{0}:U)} \]
で定める。ここで$K_{0}$は近傍だから$\#(K_{0}:U)\neq 0$となることに注意する。

　このとき$0\le\lambda_{U}(K)\le\#(K:K_{0})<\infty$が成り立つ。実際$\#(K:U)\le\#(K:K_{0})\#(K_{0}:U)$を示せばよいが、
これは被覆を考えれば明らかである。故に$\lambda_{U}$は
\[ \Lambda:=\prod_{K\in\mathcal{K}}[0, \#(K:K_{0})] \]
の元と見なせる。この$\Lambda$はチコノフの定理によりコンパクトである。\footnote{選択公理を用いている。}
$V\in\mathscr{U}$に対し、
\[ \Lambda (V):=\overline{\{\lambda_{U}\mid U\in\mathscr{U}, U\subset V\}} \]
と定める。もし$\{\Lambda (V)\mid V\in\mathscr{U}\}$が有限交叉性を持てば、
$\Lambda$がコンパクトであることから
\[ \bigcap_{V\in\mathscr{U}}\Lambda (V)\neq\emptyset \]
が従う。

　実際に$V_{1}, \dotsc, V_{n}\in\mathscr{U}$を取れば、$V:=\bigcap_{j=1}^{n}V_{j}\in\mathscr{U}$であり、
$\lambda_{V}\in\bigcap_{j=1}^{n}\Lambda (V_{j})$となるから$\{\Lambda (V)\mid V\in\mathscr{U}\}$は有限交叉性を持つ。
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
この写像は$\{\lambda_{U}\mid U\in\mathscr{U}\}$上で非負であるから、$\Lambda (V)$上でも非負となる。
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
$G$を局所コンパクトハウスドルフ位相群とする。ボレル集合体を$\mathscr{B}(G)=\sigma[\mathcal{O}]$と書く。
以下を満たす測度$\mu:\mathscr{B}(G)\rightarrow [0, \infty]$が存在する。
\begin{itemize}
\item[\textup{(i)}] $G$のコンパクト集合全体$\mathcal{K}$上で有限値を取る。つまり$K\in\mathcal{K}$なら$\mu (K)<\infty$を満たす。
\item[\textup{(ii)}] $\mu$は外部正則である。
\item[\textup{(iii)}] 開集合$O\in\mathcal{O}$は$\mu$-内部正則である。
\item[\textup{(iv)}] 左移動で不変である。つまり任意の$A\in\mathscr{B}$に対して$\mu (gA)=\mu (A)$が成り立つ。
\end{itemize}
\end{Thm}
\begin{Proof}
$\lambda$を上で得た容量とする。このとき$\sigma[\mathcal{O}]\subset\mathcal{M}_{\widehat{\lambda}}$が成り立つ。
$U\in\mathcal{O}$が$\widehat{\lambda}$-可測であることを示せばよい。$A\subset G$及び$\varepsilon>0$を取る。
$\widehat{\lambda}(A)=\inf_{A\subset U\in\mathcal{O}}\lambda_{*}(O)$であるから、ある$O\in\mathcal{O}$が存在して
\[ A\subset O, \lambda_{*}(O)\le\widehat{\lambda}(A)+\frac{\varepsilon}{3} \]
を満たすように取れる。ここで$O\cap U$は開集合だから
$\widehat{\lambda}(O\cap U)=\lambda_{*}(O\cap U)=\sup_{O\cap U\supset K\in\mathcal{K}}\lambda (K)$である。
よってある$K\in\mathcal{K}$が存在して
\[ K\subset O\cap U, \widehat{\lambda}(O\cap U)-\frac{\varepsilon}{3}\le\lambda (K) \]
を満たすように取れる。更に$O\backslash K$も開集合だから、同様にして$L\in\mathcal{K}$を
\[ L\subset O\backslash K, \widehat{\lambda}(O\backslash K)-\frac{\varepsilon}{3}\le\lambda (L) \]
を満たすように取れる。$K\subset U$より$O\backslash U\subset O\backslash K$となり、また$K\cap L=\emptyset$であるから、
\begin{align*}
\widehat{\lambda}(A\cap U)+\widehat{\lambda}(A\backslash U)-\frac{2}{3}\varepsilon
&\le\widehat{\lambda}(O\cap U)+\widehat{\lambda}(O\backslash U)-\frac{2}{3}\varepsilon \\
&\le\lambda (K)+\widehat{\lambda}(O\backslash K)-\frac{\varepsilon}{3} \\
&\le\lambda (K)+\lambda (L)=\lambda (K\sqcup L)\\
&\le\lambda_{*}((O\cap U)\cup (O\backslash K))=\lambda_{*}(O) \\
&\le\widehat{\lambda}(A)+\frac{\varepsilon}{3}
\end{align*}
となる。つまり
\[ \widehat{\lambda}(A\cap U)+\widehat{\lambda}(A\backslash U)\le\widehat{\lambda}(A)+\varepsilon \]
であるから、$\varepsilon$が任意に取れたので$U$は$\widehat{\lambda}$-可測となる。

　以上により$\mu:=\widehat{\lambda}|_{\sigma[\mathcal{O}]}$が求める測度となる。後は$\mathcal{K}$上で有限値を取ることを示せばよい。
$K\in\mathcal{K}$を取る。$x\in K$に対しコンパクトな近傍$K_{x}$を取れるが、このとき$\{K_{x}^{\circ}\}$は$K$の開被覆となる。
$K$はコンパクトだから有限個の$K_{1}, \dotsc, K_{n}$を取り、$K\subset\bigcup_{j=1}^{n}K_{j}^{\circ}$とできる。
このとき$L:=\bigcup_{j=1}^{n}K_{j}$とすれば$K\subset L^{\circ}\subset L$が従う。故に
\[ \widehat{\lambda}(K)\le\lambda_{*}(L^{\circ})\le\lambda_{*}(L)=\lambda (L)<\infty \]
を得る。
\end{Proof}

\begin{Def}
定理の条件を満たす測度を左不変ハール測度\textup{(left-invariant Haar measure)}と呼ぶ。
条件\textup{(iv)}を以下の\textup{(iv$^{\prime}$)}に変えた条件を満たす測度を右不変ハール測度と呼ぶ。
\begin{itemize}
\item[\textup{(iv$^{\prime}$)}] 右移動で不変である。つまり$A\in\mathscr{B}$に対して$\mu (Ag)=\mu (A)$が成り立つ。
\end{itemize}
両方の条件を満たす測度を両側不変ハール測度と呼ぶ。
\end{Def}



-->