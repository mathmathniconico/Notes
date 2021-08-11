
# バナッハ代数

__定義__ $\mathbb{C}$上の線型空間$\mathcal{A}$が結合的かつ双線型な積$\mathcal{A}\times\mathcal{A}\rightarrow\mathcal{A}$を持つとき代数あるいは多元環という。特にノルム空間が代数であり、積に関するノルムの条件

$$
\Vert AB \Vert\le\Vert A \Vert\cdot\Vert B \Vert
$$

を満たすときノルム代数と呼ぶ。特にバナッハ空間がノルム代数となるとき **バナッハ代数** （Banach algebra）と呼ぶ。

__定義__ 代数$\mathcal{A}$が積に関する単位元を持つとき代数$\mathcal{A}$は単位的であるという。特に単位元のノルムが$1$であるとき **規格化されている** （standardized）という。単位元は$I$や$I_{\mathcal{A}}$と表す。

- 単位的代数の単位元は一意的である。
- $0:=\lbrace 0 \rbrace$はバナッハ代数である。

__定義__ 単位的代数$\mathcal{A}$において$A\in\mathcal{A}$が可逆であるとは、ある元$B\in\mathcal{A}$が存在して$AB=BA=I$を満たすことをいう。このとき$B$は$A$に対して一意的に定まるので$A^{-1}$と書き、$A$の逆元という。可逆なことを特に **正則** （regular）とも呼び、全体を$\mathcal{R}$で表す。正則でないことを **特異** （singular）であると言い全体を$\mathcal{S}$と表す。それぞれ代数を明示して$\mathcal{R}_{\mathcal{A}}, \mathcal{S}_{\mathcal{A}}$とも表す。

__命題__ $\mathcal{B}$を単位的バナッハ代数、$A\in\mathcal{B}$とする。以下が成り立つ。

- $\Vert A \Vert\lt 1$なら$I-A$は可逆で$(I-A)^{-1}=\sum_{k=0}^{\infty}A^{k}$が成り立つ。右辺の無限和はノルム収束である。
- $\mathcal{R}\subset\mathcal{A}$は開集合である。
- $\mathcal{R}\ni A \mapsto A^{-1}\in\mathcal{R}$は連続である。

（証明）$B_{n}:=\sum_{k=0}^{n}A^{n}$とおくと、$\lbrace B_{n} \rbrace$はコーシー列となる。実際ノルムの三角不等式と積に関するバナッハ代数の条件から、$n\ge m$に対し$\Vert B_{n}-B_{m} \Vert=\Vert \sum_{k=m+1}^{n}A^{k} \Vert\le\sum_{k=m+1}^{n}\Vert A^{k} \Vert\le\sum_{k=m+1}^{n}\Vert A \Vert^{k}$であるから、$\Vert A \Vert\lt 1$より$0$に収束する。故に収束先$B=\lim B_{n}=\sum_{k=0}^{\infty}A^{k}$が存在する。後はこれが$I-A$の逆元を与えることを示せばよく、$\Vert I-(I-A)B \Vert=\lim\Vert I-(I-A)B_{n} \Vert=\lim\Vert A^{n} \Vert=0$であるから$(I-A)B=I$が分かる。逆も同様。

$A_{0}\in\mathcal{R}$の近傍が$\mathcal{R}$に含まれることを示せばよい。$\Vert A-A_{0} \Vert\lt\delta$とおく。$\Vert I-A_{0}^{-1}A \Vert=\Vert A_{0}^{-1}(A_{0}-A) \Vert\le\Vert A_{0}^{-1} \Vert \Vert A-A_{0} \Vert\lt\Vert A_{0}^{-1} \Vert\delta$より、$\delta=\Vert A_{0}^{-1} \Vert^{-1}$とすれば$\Vert I-A_{0}^{-1}A \Vert\lt 1$を得る。上の結果より$A_{0}^{-1}A\in\mathcal{R}$となるから$A=A_{0}A_{0}^{-1}A\in\mathcal{R}$より$A$は可逆。

ノルム位相による連続性を示すには点列連続性を示せば十分である。$\lbrace A_{n} \rbrace\subset\mathcal{R}, A\in\mathcal{R}$が$A_{n}\rightarrow A$を満たすとする。$A_{n}^{-1}\rightarrow A^{-1}$を示せばよい。$\Vert A_{n}^{-1}-A^{-1} \Vert\le\Vert (A^{-1}A_{n})^{-1}-I \Vert\Vert A^{-1} \Vert$であるが、$\Vert I-A^{-1}A_{n} \Vert\le\Vert A^{-1} \Vert\Vert A-A_{n} \Vert\rightarrow 0$より十分大きな$n$に対して$(A^{-1}A_{n})^{-1}=\sum_{k=0}^{\infty}(I-A^{-1}A_{n})^{k}$と表せるから、$\Vert A_{n}^{-1}-A^{-1} \Vert\le\Vert A^{-1} \Vert\Vert \sum_{k=1}^{\infty}(I-A^{-1}A_{n})^{k} \Vert\le\Vert A^{-1} \Vert\sum_{k=1}^{\infty} \Vert I-A^{-1}A_{n} \Vert^{k}$となる。ここで和は$k=1$からであることに注意すると$n\rightarrow\infty$のとき$0$に収束する。故に$A_{n}^{-1}\rightarrow A^{-1}$を得る。

__定義__ 単位的代数$\mathcal{A}$及び$A\in\mathcal{A}$に対し、$\rho(A)=\lbrace \lambda\in\mathbb{C} : A-\lambda I\in\mathcal{R}_{\mathcal{A}} \rbrace$を **レゾルベント** （resolvent）という。代数$\mathcal{A}$を明示して$\rho_{\mathcal{A}}(A)$と表すこともある。

$\sigma(A)=\mathbb{C}\backslash\rho_{\mathcal{A}}(A)$を **スペクトル** （spectrum）という。同様に代数$\mathcal{A}$を明示して$\sigma_{\mathcal{A}}(A)$と表すこともある。

$\lambda\in\rho(A)$に対し$(A-\lambda I)^{-1}\in\mathcal{A}$を対応させる写像を$A(\lambda)$と書き、レゾルベント関数という。

__命題__ $\mathcal{A}$を単位的代数とする。$A, B\in\mathscr{A}$とする。

- $\sigma(AB)\cup \lbrace 0  \rbrace=\sigma(BA)\cup \lbrace 0  \rbrace$が成り立つ。
- $A$が可逆なら$\sigma(A^{-1})=\sigma(A)^{-1}=\lbrace \lambda^{-1} : \lambda\in\sigma(A) \rbrace$が成り立つ。
- $\mu\in\mathbb{C}, \neq 0$に対して$\sigma(\mu A)=\mu\sigma(A)$が成り立つ。

（証明）$\lambda\notin\sigma(AB)\lbrace 0 \rbrace$とすると、$AB-\lambda I$は可逆である。$C=(AB-\lambda I)^{-1}$と置く。$C(AB-\lambda I)=I=(AB-\lambda I)C$より、$CAB=\lambda C+I=ABC$が成り立つ。今$(BA-\lambda I)(BCA-I)=B(ABC)A-BA-\lambda BCA+\lambda I=\lambda I$であり、また$(BCA-I)(BA-\lambda I)=B(CAB)A-\lambda BCA-BA+\lambda I=\lambda I$である。$\lambda\neq 0$だから$(BA-\lambda I)^{-1}=\lambda^{-1}(BA-\lambda I$が分かる。つまり$\lambda\notin\sigma(BA)\cup\lbrace 0 \rbrace$を得る。逆も同様。

$A$が可逆なら$0\notin\sigma(A)$に注意すれば、$A-\lambda I=-\lambda A(A^{-1}-\lambda^{-1}I)$及び$A^{-1}-\lambda^{-1}I=-\lambda^{-1}A^{-1}(A-\lambda I)$より分かる。

三つ目は$\mu A-\lambda I=\mu(A-\frac{\lambda}{\mu}I)$より従う。$\square$

定義空間を$\mathbb{C}$とするバナッハ空間（代数？）値の関数論は、絶対値をノルムに変更することで複素数値の関数論と平行に議論できる。故にコーシーの積分定理、リュービルの定理などがバナッハ空間値の関数に対しても成立する。

__命題__ $\mathcal{B}$を単位的バナッハ代数、$A\in\mathcal{B}$とする。

- $\sigma(A)\subset \lbrace \lambda\in\mathbb{C} : \vert \lambda \vert\le\Vert A \Vert \rbrace$が成り立つ。
- $\sigma(A)$はコンパクトである。
- レゾルベント等式$A(\lambda)-A(\mu)=(\lambda-\mu)A(\lambda)A(\mu)$が成り立つ。
- レゾルベント関数$A(\lambda)$は解析的である。

（証明）
$\vert \lambda \vert\gt\Vert A \Vert$とすると$\Vert \frac{1}{\lambda}A \Vert=\frac{1}{\vert \lambda \vert}\Vert A \Vert\lt 1$だから、先に示した命題より$I-\frac{1}{\lambda}A$は可逆。だから$A-\lambda I\in\mathcal{R}$より$\lambda\in\rho(A)$が従う。

有界性が示されたので、$\sigma(A)\subset\mathbb{C}$が閉集合であることを示せばよい。$A\mapsto A^{-1}$は$\mathcal{R}$上連続であるため、$\rho(A)\subset\mathbb{C}$は開集合である。

$A(\lambda)-A(\mu)=A(\lambda)(A-\mu I -(A-\lambda I))A(\mu)=(\lambda-\mu)A(\lambda)A(\mu)$である。

$\mu\in\rho(A)$に対し、レゾルベント等式より

$$
\lim_{\rho(A)\ni\lambda\rightarrow\mu}\frac{A(\lambda)-A(\mu)}{\lambda-\mu}=A(\mu)^{2}
$$

が従うから連続微分可能である。更に無限回連続微分可能が従うので解析的である。$\square$

__定理__ $\mathcal{B}$を単位的バナッハ代数とする。$\mathcal{B}\neq 0$のとき$A\in\mathcal{B}$について$\sigma(A)$は空でない。また$\mathcal{B}=0$のとき$\sigma_{0}(0)$は空となる。

（証明）まず$\mathcal{B}\neq 0$なら$0\neq I$に注意しておく。まず$\sigma(A)=\emptyset$なら任意の有界線型汎関数$\varphi\in\mathcal{B}^{*}$に対して$\varphi(A(\lambda))$が整関数になることを示す。

$\lambda_{0}\in\rho(A)$に対し、$\vert \lambda-\lambda_{0} \vert\lt\delta$とする。$B=(\lambda-\lambda_{0})A(\lambda_{0})$は$\Vert B \Vert\lt\delta\Vert (A-\lambda_{0}I)^{-1} \Vert$より、$\delta=\Vert (A-\lambda_{0})^{-1} \Vert^{-1}$とおけば$\Vert B \Vert\lt 1$が従うので、級数展開$(I-B)^{-1}=\sum_{k=0}^{\infty}B^{k}$を得る。$I-B=(A-\lambda_{0}I-(\lambda-\lambda_{0})I)A(\lambda_{0})=(A-\lambda I)A(\lambda_{0})$より、$(I-B)^{-1}=(A-\lambda_{0}I)A(\lambda)$が従う。故に級数展開$A(\lambda)=\sum_{k=0}^{\infty}(\lambda-\lambda_{0})^{k}A(\lambda_{0})^{k+1}$を得る。そして$\varphi$の有界性から$\varphi( A(\lambda) )=\sum_{k=0}^{\infty}\varphi( A(\lambda_{0})^{k+1} )(\lambda-\lambda_{0})^{k}$の右辺が絶対収束することが示される。

この級数展開は任意の$\lambda_{0}\in\rho(A)=\mathbb{C}$におけるテイラー展開を与えていることから$\varphi(A(\lambda))$が整関数であることが分かる。ところが$\vert \lambda \vert\rightarrow\infty$のとき$-\frac{1}{\lambda}A\rightarrow 0$であるから$\Vert A(\lambda) \Vert\le\Vert (-\lambda(I-\frac{1}{\lambda}A))^{-1} \Vert=\vert \lambda \vert^{-1}\Vert (I-\frac{1}{\lambda}A)^{-1} \Vert\rightarrow 0$となる。故に$\vert \varphi(A(\lambda)) \vert\le\Vert \varphi \Vert\Vert A(\lambda) \Vert\rightarrow 0$であり、$\varphi(A(\lambda))$は有界となる。リュービルの定理から定数であることが従い、先ほどの収束の議論より$\varphi(A(\lambda))$は恒等的に$0$となる。これは矛盾する。

> 実は$\mathcal{B}$上の有界線型汎関数が十分豊富に存在することを示す必要がある。ハーン・バナッハの定理等から$\mathcal{B}\hookrightarrow\mathcal{B}^{\ast\ast}$が従うので、任意の$\varphi\in\mathcal{B}^{\ast}$に対し$\tilde{A(\lambda)}(\varphi)=\varphi(A(\lambda))\equiv 0$が成り立ち$\mathcal{B}=0$を得る。

<!--
　次の系は明快だが重要な結果である。

\begin{Cor}[Gelfand-Mazurの定理]
　$\mathcal{B}$を単位的\textup{Banach}代数で、体つまり$\mathcal{R}=\mathcal{B}\backslash \lbrace 0  \rbrace$とする。
このとき$\mathcal{B}=\mathbb{C}I$が成り立つ。
\end{Cor}
\begin{Proof}
　仮定より$\mathcal{B}\neq 0$に注意する。任意の元$A\in\mathcal{B}$に対して定理より$\sigma(A)$は空でないから、ある元$\lambda\in\sigma(A)$が存在して$A-\lambda I\in\mathcal{S}$を満たす。
ところが$\mathcal{S}= \lbrace 0  \rbrace$であるから$A=\lambda I$を得る。故に$\mathcal{B}\subset\mathbb{C}I$が成り立つ。逆も明白である。
\end{Proof}

\begin{Lem}[スペクトル写像定理（多項式版）]
　$\mathcal{B}$を単位的\textup{Banach}代数、$A$を$\mathcal{B}$の元、$p(\zeta)\in\mathbb{C}[\zeta]$を多項式とする。
このとき$p(\sigma(A))=\sigma(p(A))$が成り立つ。ただし$p(A)$は$\zeta$を$A$で置き換えた、$\mathcal{B}$における演算の下で定義される$\mathcal{B}$の元を意味する。
\end{Lem}
\begin{Proof}
　$p$は$1$次以上としてよい。$\lambda\in\mathbb{C}$に対し、$\lambda_{k}\in\mathbb{C}$により$p(\zeta)-\lambda=a\prod_{k=1}^{n}(\zeta-\lambda_{k})$と因数分解しておく。
このとき$p(A)-\lambda I=a\prod_{k=1}^{n}(A-\lambda_{k}I)$である。$A-\lambda I$の形の元達は互いに可換であることに注意する。
\\
　($\subset$) $\lambda\in p(\sigma(A))$とすると、$\lambda=p(\mu)$なる$\mu\in\sigma(A)$が存在する。
$0=p(\mu)-\lambda=a\prod_{k=1}^{n}(\mu-\lambda_{k})$より、ある$k$が存在して$\mu=\lambda_{k}$を満たす。
$\mu\in\sigma(A)$より、 $A-\lambda_{k}I$は可逆でない。 ここでもし$p(A)-\lambda I$が可逆なら $I=(a(p(A)-\lambda I)^{-1}\prod_{j\neq k}(A-\lambda_{j}I))(A-\lambda_{k}I)$より
$A-\lambda_{k}I$が可逆でないことに反するから$p(A)-\lambda I$は可逆でない。故に$\lambda\in\sigma(p(A))$となる。
\\
　($\supset$) $\lambda\in\sigma(p(A))$とすると$p(A)-\lambda I=\prod_{k=1}^{n}(A-\lambda_{k}I)$は可逆でないから、ある$k$が存在して$A-\lambda_{k}I$は可逆でない。
故に$\lambda_{k}\in\sigma(A)$であり、$p(\lambda_{k})-\lambda=0$より$\lambda=p(\lambda_{k})$が従う。つまり$\lambda\in p(\sigma(A))$が成り立つ。
\end{Proof}

　ここでは多項式$p$に対する元$A$の代入を考えたが、一般の関数$f$に対する代入も考えたくなるのは自然である。
近似定理などを用いて、多項式の極限として定める方法などを考えることができるが、対象となる$f$や$A$の範疇に問題が生じる。
後の節において、この問題に対する一つの回答を示す。
\\
　与えられたスペクトル集合を持つ元が存在するかという逆問題は、興味深い問題だがきっと難しいだろう。自分は詳しくない。

\begin{Fact}[Banach-Steinhausの定理（または一様有界性定理）の系]
　$\mathcal{B}$を\textup{Banach}代数、$E\subset\mathcal{B}$は空でないとする。
任意の有界線型汎関数$\varphi\in\mathcal{B}^{*}$に対し$ \lbrace |\varphi(A)| :  A\in E  \rbrace$が有界ならば、$\sup \lbrace ||A|| :  A\in E  \rbrace<\infty$が成り立つ。
\end{Fact}
\begin{Proof}
　元々の定理は\textup{Baire}のカテゴリー定理により示される。更に選択公理を用いて\textup{Hahn-Banach}の定理などが示され、$\mathcal{B}\hookrightarrow\mathcal{B}^{**}$を得る。この事実は以上より従う。
\end{Proof}

\begin{Thm}
　$\mathcal{B}$を$0$でない単位的\textup{Banach}代数とする。$A\in\mathcal{B}$に対し、以下の値が存在して、
\[ \lim_{n}||A^{n}||^{\frac{1}{n}}=\inf_{n}||A^{n}||^{\frac{1}{n}}=\sup \lbrace |\lambda| : \lambda\in\sigma(A)  \rbrace \]
が成り立つ。
\end{Thm}
\begin{Proof}
　自然数$m$を固定し、$n$に対して$0\le k<m$を用いて$n=mj+k$と表す。このとき積に関するノルムの条件から$||A^{n}||^{\frac{1}{n}}\le||A^{m}||^{\frac{j}{n}}||A^{k}||^{\frac{1}{n}}$が成り立つ。
そこで$n\rightarrow\infty$をすると$\frac{j}{n}\rightarrow\frac{1}{m}, \frac{1}{n}\rightarrow 0$より$\limsup||A^{n}||^{\frac{1}{n}}\le||A^{m}||^{\frac{1}{m}}$が従う。
これが任意の$m$に対して成立するから$\limsup||A^{n}||^{\frac{1}{n}}\le\inf||A^{m}||^{\frac{1}{m}}$を得る。
つまり$\lim ||A^{n}||^{\frac{1}{n}}$が存在して$\lim ||A^{n}||^{\frac{1}{n}}=\inf ||A^{n}||^{\frac{1}{n}}$が分かる。
\\
　$\lambda\in\sigma(A)$とすると補題より$\lambda^{n}\in\sigma(A^{n})$であるから$|\lambda|^{n}=|\lambda^{n}|\le||A^{n}||$を得る。
任意の$n$に対して言えるので$|\lambda|\le\inf ||A^{n}||^{\frac{1}{n}}$が従い、$sup \lbrace |\lambda| : \lambda\in\sigma(A)  \rbrace\le\inf ||A^{n}||^{\frac{1}{n}}$を得る。
\\
　逆は関数論の議論が必要となる。背理法により示す。今$\sup \lbrace |\lambda| : \lambda\in\sigma(A)  \rbrace<\inf ||A^{n}||^{\frac{1}{n}}$を仮定すると、実数の連続性から間に実数$a$が存在する。
この$a$に対して$E= \lbrace \frac{1}{a^{n}}A^{n}  \rbrace$とおく。今$|\lambda|>\inf||A^{n}||^{\frac{1}{n}}=\lim ||A^{n}||^{\frac{1}{n}}$とすると、
$\lim ||\left(\frac{1}{\lambda}A\right)^{n}||^{\frac{1}{n}}=\frac{1}{|\lambda|}\lim ||A^{n}||^{\frac{1}{n}}<1$より、
\textup{Cauchy}の判定法から$\sum_{k=0}^{\infty}||\left(\frac{1}{\lambda}A\right)^{k}||<+\infty$は絶対収束する。
故に$\sum_{k=0}^{\infty}\frac{1}{\lambda^{k}}A^{k}$はノルム収束し、展開式から$-\lambda A(\lambda)$に一致する。
$A(\lambda)$は$\rho(A)$上解析的なので、この収束半径は$\sup \lbrace |\lambda| : \lambda\in\sigma(A)  \rbrace$まで拡張できる。
\footnote{原点周りの円環領域$\sup \lbrace |\lambda| : \lambda\in\sigma(A)  \rbrace<r<\infty$におけるLaurent展開とみてもいいし、無限遠周りのTaylor展開と見ても良い。いずれにせよ一価正則性から解析接続が可能。}
故に$\lambda=a$を展開式に代入ができて$A(a)=-\frac{1}{a}\sum_{k=0}^{\infty}\frac{1}{a^{k}}A^{k}$が成り立つ。
ここで任意の有界線型汎関数$\varphi\in\mathcal{B}^{*}$に対し$\varphi(A(a))=-\frac{1}{a}\sum_{k=0}^{\infty}\frac{1}{a^{k}}\varphi(A^{k})$が線型性と連続性から従うので
$\sup |\varphi\left(\frac{1}{a^{k}}A^{k}\right)| <\infty$となる。先に述べた事実から$\sup ||\frac{1}{a^{k}}A^{k}||<\infty$であるからこれを$\alpha$と置くと、
$\inf ||A^{n}||^{\frac{1}{n}}\le\lim\alpha^{\frac{1}{n}}\cdot a=a<\inf ||A^{n}||^{\frac{1}{n}}$となり、これは矛盾する。
\end{Proof}

\begin{Def}
　この値を$r(A)$と書き、$A$のスペクトル半径\textup{:spectral radius}と呼ぶ。
\end{Def}

　最後に述べた定理は一見単純に見えるが、関数論などを用いた極めて精密な議論により得られた結果である。
ここから$r(A)\le ||A||$はすぐに従うが、その逆は一般に成り立たない。


\subsection*{例}\addcontentsline{toc}{subsection}{例}
　まずは単位的可換\textup{Banach}代数の例を挙げよう。
\begin{enumerate}
\item $0, \mathbb{C}$は単位的可換\textup{Banach}代数である。特に$\mathbb{C}$は規格化されている。
\item $n\le 2$に対し$\mathbb{C}^{n}$にノルムとして$\max$ノルムを取り、積を成分毎の積として定めれば、規格化された単位的可換\textup{Banach}代数となる。このとき単位元は$(1, \dotsc, 1)$である。
\item コンパクトハウスドルフ空間$X$上の連続写像全体$C(X)$は$\sup$ノルム（$\max$ノルム）及び、各点における積により単位的可換\textup{Banach}代数になる。$X\neq\emptyset$であれば規格化されている。
\item 局所コンパクトハウスドルフ空間$X$上の有界連続写像全体$C_{b}(X)$は$\sup$ノルム及び、各点における積により可換\textup{Banach}代数になる。$X\neq\emptyset$であれば規格化されている。
\end{enumerate}

\begin{Rem}
$0=C(\emptyset), \mathbb{C}=C( \lbrace *  \rbrace), \mathbb{C}^{n}=C( \lbrace *_{1}, \dotsc, *_{n}  \rbrace)$である。
$X$がコンパクトハウスドルフ空間であれば$C(X)=C_{b}(X)$である。
\end{Rem}

　次に非単位的な可換\textup{Banach}代数の例を挙げる。
局所コンパクトハウスドルフ空間$X$上の

\begin{enumerate}
\item $\mathcal{B}$を\textup{Banach}空間とし、その上の有界線型作用素全体$\mathbb{B}(\mathcal{B})$は規格化された単位的\textup{Banach}代数であるが、非可換となる。
ただし積は合成、ノルムは作用素ノルムとして与えられ、このとき単位元は$\textup{id}_{\mathcal{B}}$である。
\end{enumerate}

\begin{Rem}
　$n\le 2$に対し$\mathbb{C}^{n\times n}$には$\max$ノルムとは別の\textup{Banach}代数の構造が入る。
つまり$n\times n$行列は$\mathbb{C}^{n}$上の有界線型作用素とみなせるから、$\mathbb{B}(\mathbb{C}^{n})$の意味で規格化された単位的\textup{Banach}代数の構造が入る。
これを行列代数\textup{:matrix algebra}と言い、$\mathbb{M}_{n}(\mathbb{C})$で表す。
\end{Rem}

%\\
%　$L^{1}(\mathbb{R})$を\textup{Lebesgue}可測な$\mathbb{R}$上の実数値関数
%$f$で$||f||_{L^{1}(\mathbb{R})}:=\int_{\mathbb{R}} |f|\textup{d}\mu <\infty$
%を満たすもの全体とすると非単位的な\textup{Banach}代数となる。このときノルムは$L^{1}$ノルム、積は合成積
%\[ f*g(x)=\int_{\mathbb{R}} f(y)g(x-y) \textup{d}\mu \]
%として与えられる。

-->