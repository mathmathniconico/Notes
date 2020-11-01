
# 素イデアルと整域

__素イデアル__$\mathfrak{p}\subsetneq R$を真イデアルとする。$xy\in\mathfrak{p}$なら$x\in\mathfrak{p}$または$y\in\mathfrak{p}$が成り立つとき$\mathfrak{p}$を **素イデアル** （prime ideal）という。

- 例えば$R=\mathbb{Z}$について$p\in\mathbb{Z}$が素数であることと$p\mathbb{Z}$が素イデアルとなることは同値になる。特に$6\mathbb{Z}$は素イデアルでない。実際$2\cdot 3=6\in 6\mathbb{Z}$だが$2, 3\notin 6\mathbb{Z}$である。

> 整数における素数と同様に、素イデアルは環論における血肉に相当し、様々な場面で中心的な役割を果たす。まずその一例を挙げよう。

__定理__ （素イデアル対応定理）$I\subset R$をイデアルとする。このとき$I$を含む$R$の素イデアル全体と$R/I$の素イデアルは一対一に対応する。


（証明）イデアル対応定理（定理\ref{th:IdealCorrespondence}があるので$J\subset R, \overline{K}\subset R/I$を素イデアルとして、
\begin{align*}
	\Phi(J)&=\lbrace a+I \mid a\in J \rbrace \subset R/I , \\
	\Psi(\overline{K})&=\lbrace a\in R \mid a+I\in\overline{K} \rbrace \subset R
\end{align*}
が素イデアルとなることを示せば良い。

$(a+I)(b+I)=ab+I \in\Phi(J)$とする。
ここで$\Phi(J)$の定義から直ちに$ab\in J$としてしまうと突っ込まれてマスハラ
\footnote{mathematical harassmentの略。数学に従事する者は日々これと戦っている。
あえて突っ込ませて反撃して黙らせるという高等技術も存在する。「いやその指摘はおかしいですよね」}を受ける。
この式はある$x\in J$が存在して$ab+I=x+I$が成り立つことを示している。
よって$ab-x\in I\subset J$であり、$x\in J$と$J$がイデアルであることから$ab=(ab-x)+x\in J$が従う。
ところで$J$は素イデアルだったから$a\in J$または$b\in J$である。故に$a+I\in\Phi(J)$または$b+I\in\Phi(J)$を得る。

$ab\in\Psi(\overline{K})$とする。
このときは$\Psi(\overline{K})$の定義から$(a+I)(b+I)=ab+I\in\overline{K}$が言える。
$\overline{K}$は素イデアルだったから$a+I\in\overline{K}$または$b+I\in\overline{K}$が成り立つが、
これは$a\in\Psi(\overline{K})$または$b\in\Psi(\overline{K})$を示している。$\square$

$R$の素イデアル全体を$\mathrm{Spec}R$と表す。


\subsection{整域}
イデアルがあったら取りあえず割ってみるのをお勧めする。素イデアルによる剰余環では何が成り立つだろうか。
$\mathfrak{p}\subset R$を素イデアルとし、$R/\mathfrak{p}$の元について、
\[ (x+\mathfrak{p})(y+\mathfrak{p})=0+\mathfrak{p} \]
が成り立つとする。このとき$xy\in\mathfrak{p}$だが、
$\mathfrak{p}$は素イデアルなので$x\in\mathfrak{p}$または$y\in\mathfrak{p}$が言える。
つまり$x+\mathfrak{p}=0+\mathfrak{p}$または$y+\mathfrak{p}=0+\mathfrak{p}$が成り立つ。
換言すれば、掛けてゼロになるなら、いずれか一方がゼロであることが分かる。
逆にゼロでない元同士の積はゼロとはならない。このような環を\index{せいいき@整域}整域（\index{integral domain}integral domain）という。
\footnote{この命名は紛らわしい。後で元が整（integral）とか整閉整域（integrally closed integral domain）とか出てくる。
更にdomainはdomainで色々な場面で使われる。しかし今更変えられないのでどうしようもない。}

\begin{Prop}{}{}
$I \subset R$をイデアルとする。このとき以下は同値となる。
\begin{EnumEquiv}
	\item$I$は素イデアル。
	\item$R/I$は整域。
\end{EnumEquiv}
\end{Prop}
（証明）上の議論より$I$が素イデアルなら$R/I$が整域であることが分かる。逆に$R/I$が整域とし、$ab\in I$とする。
$(a+I)(b+I)=ab+I=0+I$だから、$R/I$の整域性より$a+I=0+I$または$b+I=0+I$が従う。
故に$a\in I$または$b\in I$となる。$\square$

\begin{Def}{}{}
$ab=ac, a\neq 0$なら$b=c$が成り立つとき、\index{しょうきょかのう@消去可能}消去可能（\index{eliminable}eliminable）であるという。
\end{Def}

\begin{Prop}{}{}
環$R$に対し、以下は同値となる。
\begin{EnumEquiv}
\item$R$は整域である。
\item$R$は消去可能である。
\end{EnumEquiv}
\end{Prop}
（証明）簡単。$\square$

$\mathbb{Z}$は整域である。一方で$\mathbb{Z}\times\mathbb{Z}$は成分毎の演算で環となるが、
例えば$(1, 0)(0, 1)=(0, 0)$となるため整域ではない。$6\mathbb{Z}$は素イデアルでない。
これは$\mathbb{Z}/6\mathbb{Z}$が整域でないことからも分かる。実際
\[ (2+6\mathbb{Z})(4+6\mathbb{Z})=8+6\mathbb{Z}=2+6\mathbb{Z}=(2+6\mathbb{Z})(1+6\mathbb{Z}) \]
しかし$4+6\mathbb{Z}\neq 1+6\mathbb{Z}$なので$2+6\mathbb{Z}$を消去できない。

