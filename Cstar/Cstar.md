
# Cstar代数と準同型

__定義__ 代数$\mathcal{A}$が

$$
(A^{\ast})^{\ast}=A, (AB)^{\ast}=B^{\ast}A^{\ast}, (\lambda A+\mu B)^{\ast}=\overline{\lambda}A^{\ast}+\overline{\mu}B^{\ast}
$$

をみたす写像$\ast\colon\mathcal{A}\ni A\mapsto A^{\ast}\in\mathcal{A}$を持つとき$\ast$代数であるという。この写像$\ast$を対合（involution）と呼び、$\ast$代数を対合代数（involutive algebra）と呼ぶこともある。

特にノルム代数が$\ast$代数であり、対合に関するノルムの条件$\Vert A^{\ast} \Vert=\Vert A \Vert$を満たすときノルム$\ast$代数と呼ぶ。またBanach代数がノルム$\ast$代数であるときBanach$\ast$代数という。更にBanach$\ast$代数が$C^{\ast}$条件

$$
\Vert A^{\ast}A \Vert=\Vert A \Vert^{2}
$$

を満たすとき、$C^{\ast}$代数と呼ぶ。

__例__
- $\mathbb{C}$は通常の積と絶対値、共役により$C^{\ast}$代数となる。
- ヒルベルト空間$\mathcal{H}$上の有界線型作用素$\mathbb{B}(\mathcal{H})$は合成と作用素ノルム、随伴により$C^{\ast}$代数となる。

次に対合から定義される幾つかの有用なクラスを定める。これらのクラスは基本的なものであり、他にも様々な種類が考えられている。

__定義__ $\mathcal{A}$は$\ast$代数、$A\in\mathcal{A}$とする。

- $A^{\ast}=A$を満たすとき$A$は自己共役（self-adjoint）という。$A^{\ast}A=AA^{\ast}$を満たすとき$A$は正規（normal）という。
- 更に$\mathcal{A}$が単位的であれば、$A\in\mathcal{A}$が$A^{\ast}A=AA^{\ast}=I$を満たすとき$A$はユニタリー（unitary）という。
- $\Re A=\frac{A+A^{\ast}}{2}$を$A$の実部、$\Im A=\frac{A-A^{\ast}}{2i}$を$A$の虚部という。実部と虚部は自己共役であり$A=\Re A+i\Im A$を満たす。

> ヒルベルト空間上の線型作用素に対して$A^{\ast}A=I$であるとき等距離作用素、$AA^{\ast}=I$のとき余等距離作用素などと呼ぶこともある。従ってユニタリー条件の二つの等式は必ずしも両立する概念ではない。

単位的$\ast$代数において$I^{\ast}=I^{\ast}I=(I^{\ast}I)^{\ast}=(I^{\ast})^{\ast}=I$より$I^{\ast}=I$が成り立つ。また$A$が可逆であれば$A^{\ast}(A^{-1})^{\ast}=(A^{-1}A)^{\ast}=I^{\ast}=I$より$(A^{-1})^{\ast}=(A^{\ast})^{-1}$が分かる。このことから一般の元$A$に対して$\sigma(A^{\ast})=\overline{\sigma(A)}=\lbrace \overline{\lambda}\mid\lambda\in\sigma(A) \rbrace$が示される。

次の命題より、単位的$C^{\ast}$代数における正規元のスペクトル半径はノルムによってのみ決定され、所属する部分代数に依らないことが分かる。

<!--
\begin{Prop}
　$0$でない単位的\textup{C*}代数$\mathcal{C}$に対して次が成り立つ。
\begin{enumerate}
\item $||I||=1$である。つまり$0$でない\textup{C*}代数は常に規格化されている。
\item $A\in\mathcal{C}$が正規なら$r(A)=||A||$が成り立つ。
\end{enumerate}
\end{Prop}
\begin{Proof}
　(1) $||I||^{2}=||I^{*}I||=||I||$であるが、$I\neq 0$より$||I||\neq ||0||=0$つまり$||I||=1$を得る。
\\
　(2) \textup{C*}条件および正規性より$||A^{2^{n}}||^{2}=||(A^{2^{n}})^{*}(A^{2^{n}})||=||(A^{*})^{2^{n}}A^{2^{n}}||=||(A^{*}A)^{2^{n}}||$が成り立つ。
ここで一般に$(A^{*}A)^{*}=A^{*}A$であるから再び\textup{C*}条件より$||(A^{*}A)^{2^{n}}||=||(A^{*}A)^{2^{n-1}}||^{2}=\dotsb=||A^{*}A||^{2^{n}}=||A||^{2^{n+1}}$である。
故に$||A^{2^{n}}||^{\frac{1}{2^{n}}}=||A||$が成り立つので、$r(A)=\inf ||A^{2^{n}}||^{\frac{1}{2^{n}}}=||A||$が従う。
\end{Proof}

　更にスペクトル集合に関しては、次のことが分かる。

\begin{Prop}
　単位的\textup{C*}代数$\mathcal{C}$の元に対して次が成立する。
\begin{enumerate}
\item $U\in\mathcal{C}$がユニタリーであれば$\sigma(U)\subset\{\lambda\in\mathbb{C}\mid |\lambda|=1\}$が成立する。つまり単位円周上に含まれる。
\item $A\in\mathcal{C}$が自己共役であれば$\sigma(A)\subset [-||A||, ||A||]$が成り立つ。特に実数である。
\end{enumerate}
\end{Prop}
\begin{Proof}
　$\mathcal{C}=0$のときは$\sigma(0)=\emptyset$より明らか。
\\
　(1) $U^{*}U=I$より\textup{C*}条件より$1=||I||=||U^{*}U||=||U||^{2}$だから$||U||=1$を得る。故に$\lambda\in\sigma(U)$なら$|\lambda|\le 1$である。
逆に$\lambda^{-1}\in\sigma(U^{-1})=\sigma(U^{*})$であるが、$U^{*}$もユニタリーであるから$|\lambda^{-1}|\le 1$を得る。つまり$|\lambda|=1$が成り立つ。
\\
　(2) 実数$a, b\neq 0$と$\lambda=a+ib$に対し$A-\lambda I=b(b^{-1}(A-aI)-iI)$である。
$B=b^{-1}(A-aI)$と置くと、$B^{*}=\overline{b^{-1}}(A^{*}-\overline{a}I^{*})=b^{-1}(A-aI)=B$より$B$は自己共役となる。
このとき$B-iI$が可逆でないとすると、任意の実数$x$に対して$i(B-iI)=(iB-xI)+(x+1)I$より$x+1\in\sigma(iB-xI)$を得る。
$|x+1|\le||iB-xI||$であるから\textup{C*}条件より$(x+1)^{2}\le||iB-xI||^{2}=||(-iB^{*}-xI)(iB-xI)||=||B^{2}+x^{2}I||\le x^{2}+||B||^{2}$が成り立つ。
整理すると$1+2x\le||B||^{2}$が任意の$x$に対して成り立つことになり、これは矛盾する。
つまり$B-iI$は可逆であり、$A-\lambda I$も可逆となる。
故に$\sigma(A)\subset\mathbb{R}$が分かる。特に$r(A)\le||A||$より$\sigma(A)\subset [-||A||, ||A||]$が従う。
\end{Proof}

　これまでは代数という一つの対象と、その元について考察してきた。代数としての構造を深く理解するため、対象と対象との間にある関係について議論を深めよう。
それは圏論の用語を用いれば、射とは何かを考えるということである。

\begin{Def}
　$\mathcal{A}, \mathcal{B}$を代数、$\pi$を$\mathcal{A}$から$\mathcal{B}$への線型写像とする。
$\pi$が準同型\textup{:homomorphism}であるとは、任意の$A, B\in\mathcal{A}$に対して$\pi(AB)=\pi(A)\pi(B)$を満たすことを言う。
更に$\mathcal{A}, \mathcal{B}$が\textup{*}代数で、任意の$A\in\mathcal{A}$に対して$\pi(A^{*})=\pi(A)^{*}$を満たすとき、\textup{*}準同型\textup{:*-homomorphism}と言う。
それぞれ準同型が全単射であるとき同型\textup{:isomorphism}、\textup{*}同型\textup{:*-isomorphism}と呼ぶ。
\\
　ノルム代数$\mathcal{A}, \mathcal{B}$及び、準同型$\pi:\mathcal{A}\rightarrow\mathcal{B}$に対し、
$\pi$が等距離\textup{:isometric}であるとは、任意の$A\in\mathcal{A}$に対して$||\pi(A)||_{\mathcal{B}}=||A||_{\mathcal{A}}$を満たすことを言う。
\end{Def}

\begin{Rem}
　\textup{\textbf{Alg, Alg*, BanachAlg, BanachAlg*, C*}}及びその可換部分や単位的部分（\textup{\textbf{Comm.Alg, UnitalAlg}}等）は適切な対象\textup{:object}と射\textup{:morphism}により圏をなす。
\end{Rem}

\begin{Def}
　単位的な代数$\mathcal{A}, \mathcal{B}$と準同型$\pi:\mathcal{A}\rightarrow\mathcal{B}$に対して、
$\pi$が単位元を保つ\textup{:unit-preserving}とは、$\pi(I_{\mathcal{A}})=I_{\mathcal{B}}$を満たすことをいう。
\footnote{準同型は必ずしも単位元を保つとは限らない。これは$0$からの射を考えてみればすぐに分かる。ただし後に挙げる比較的重要な射に関しては大抵の場合に単位元を保つことを示すことができる。}
\end{Def}

　\textup{\textbf{BanachAlg}}等における線型位相空間としての圏との整合性、即ち準同型が有界\footnote{連続であることと同値であった。}であることは、たとえ単位元を保つことを仮定しても一般には従わない。
しかし単位的\textup{C*}代数のなす圏\textup{\textbf{C*}}においてはこの限りではなく、準同型性のみから有界性が従う。これは後述する。
単位元を保つ準同型に限れば、規格化された単位的\textup{Banach}代数の範疇で、次のように簡単に示すことができる。
一般の\textup{C*}代数において、準同型の有界性が示せるかは知らない。

\begin{Prop}
　単位的代数$\mathcal{A}, \mathcal{B}$と単位元を保つ準同型$\pi:\mathcal{A}\rightarrow\mathcal{B}$に対して逆元は逆元に写る。
特に$\mathcal{A}, \mathcal{B}$が\textup{Banach}代数で$\mathcal{B}$が規格化されているとき$||\pi||\le 1$つまり有界であり、更に$\mathcal{A}$も規格化されていれば$||\pi||=1$が成り立つ。
\end{Prop}
\begin{Proof}
　まず$A\in\mathcal{A}$が可逆とすると、$\pi(A^{-1})\pi(A)=\pi(A^{-1}A)=\pi(I_{\mathcal{A}})=I_{\mathcal{B}}$より$\pi(A^{-1})=\pi(A)^{-1}$が従う。
\\
　次に$\mathcal{B}$が規格化されているときに$\pi$の有界性を示す。$\pi=0$なら常に有界であるから$\pi\neq 0$としてよい。このとき$\mathcal{A}, \mathcal{B}\neq 0$である。
$A\in\mathcal{A}$に対し、$|\lambda|>||A||$とすると$A-\lambda I_{\mathcal{A}}\in\mathcal{R}_{\mathcal{A}}$である。
このとき$\pi(A)-\lambda I_{\mathcal{B}}=\pi(A-\lambda I_{\mathcal{A}})\in\mathcal{R}_{\mathcal{B}}$であるから、
$\mathcal{B}\neq 0$より$\pi(A)-\lambda I_{\mathcal{B}}\neq 0$すなわち$\pi(A)\neq \lambda I_{\mathcal{B}}$となる。
$\mathcal{B}$は規格化されているから、両辺のノルムを取ると$||\pi(A)||\neq ||\lambda I_{\mathcal{B}}||=|\lambda|\cdot||I_{\mathcal{B}}||=|\lambda|$が従う。
これが任意の$|\lambda|>||A||$に対して成り立つので$||\pi(A)||\le ||A||$を得る。つまり$||\pi||\le 1$を得る。
\\
　更に$\mathcal{A}$が規格化されているときは、$1=||I_{\mathcal{B}}||=||\pi(I_{\mathcal{A}})||\le ||\pi||\cdot ||I_{\mathcal{A}}||=||\pi||$から$||\pi||=1$が従う。
\end{Proof}

\begin{Def}
　$\mathcal{A}$を代数とする。$\mathcal{A}$の部分空間$\mathcal{I}$が$\mathcal{A}\mathcal{I}\subset\mathcal{I}$を満たすとき左イデアル\textup{:left ideal}と言う。
同様に$\mathcal{I}\mathcal{A}\subset\mathcal{I}$を満たすとき右イデアル\textup{:right ideal}と言う。
左イデアルかつ右イデアルのとき、両側イデアル\textup{:two-sided ideal}と言う。
\\
　$\{0\}, \mathcal{A}$は両側イデアルとなる。これを自明\textup{:trivial}な両側イデアルと言う。両側イデアルが自明でないとき、非自明\textup{:non-trivial}であると言う。
\end{Def}

\begin{Rem}
　準同型$\pi:\mathcal{A}\rightarrow\mathcal{B}$の核$\Ker\pi\subset\mathcal{A}$は両側イデアルとなる。
\\
　両側イデアル$\mathcal{I}, \mathcal{J}, \mathcal{I}_{\lambda}(\lambda\in\Lambda)$に対し、
$\mathcal{I}\cap\mathcal{J}, \bigcup_{\lambda\in\Lambda}\mathcal{I}_{\lambda}$は両側イデアルになる。
\end{Rem}

\begin{Def}
　ノルム代数$\mathcal{A}$の両側イデアルがノルム位相において閉集合であるとき、両側閉イデアル\textup{:two-sided closed ideal}、あるいは単にイデアル\textup{:ideal}と呼ぶ。
\end{Def}

\begin{Prop}
　\textup{Banach}代数$\mathcal{B}$とイデアル$\mathcal{I}\subset\mathcal{B}$に対して、
商空間$\mathcal{B}/\mathcal{I}$は\textup{Banach}代数となる。
\end{Prop}
\begin{Proof}
　$A, B\in\mathcal{B}$の同値類を$[A], [B]$で表せば、自然なノルム$||[A]||=\inf\{||A+Q||\mid Q\in\mathcal{I}\}$により$\mathcal{B}/\mathcal{I}$が\textup{Banach}空間になることはよい。
そこで積を$[A]\cdot [B]=[AB]$と定めれば、$||[AB]||=\inf\{||AB+Q||\mid Q\in\mathcal{I}\}\le\inf\{||A+Q_{1}||\cdot ||A+Q_{2}||\mid Q_{1}, Q_{2}\in\mathcal{I}\}=||[A]||\cdot||[B]||$
より積に関するノルムの条件を満たすことが分かる。故に商空間$\mathcal{B}/\mathcal{I}$は\textup{Banach}代数である。
\end{Proof}

\begin{Rem}
　$\mathcal{B}$が可換なら$\mathcal{B}/\mathcal{I}$も可換となる。
\\
　$\mathcal{B}$が単位的なら$\mathcal{B}/\mathcal{I}$も単位的であり、その単位元は$I_{\mathcal{B}/\mathcal{I}}=[I_{\mathcal{B}}]$である。
すなわち商写像は単位元を保つ準同型である。
\end{Rem}

\begin{Def}
　代数$\mathcal{A}$及び両側イデアル$\mathcal{I}\subsetneq\mathcal{A}$に対し、次を定める。
\begin{enumerate}
\item $\mathcal{I}$が素\textup{:prime}であるとは、任意の$A, B\in\mathcal{A}$に対し、$AB\in\mathcal{I}$なら$A\in\mathcal{I}$または$B\in\mathcal{I}$が成り立つことをいう。
$\mathcal{A}$の素な両側イデアル全体を$\Prime(\mathcal{A})$で表す。
\item $\mathcal{I}$が極大\textup{:maximal}であるとは$\mathcal{I}$を含む非自明な両側イデアルが存在しないことを言う。$\mathcal{A}$の極大な両側イデアル全体を$\Max(\mathcal{A})$で表す。
\end{enumerate}
\end{Def}

\begin{Prop}
　代数$\mathcal{A}$に対し、$\Max(\mathcal{A})$は$\Prime(\mathcal{A})$の部分集合となる。
\end{Prop}
\begin{Proof}
　$\mathcal{I}\in\Max(\mathcal{A})$に対し、$AB\in\mathcal{I}, A\notin\mathcal{I}$とする。
このとき$\mathcal{J}=\{CA+D\mid C\in\mathcal{A}, D\in\mathcal{I}\}$は$\mathcal{I}$を真に含む両側イデアルとなる。
極大性から$\mathcal{J}=\mathcal{A}$であり、ある$C\in\mathcal{A}, D\in\mathcal{I}$により$CA+D=I$を満たす。
両辺に右から$B$をかけると$CAB+DB=B$となり、$AB, D\in\mathcal{I}$より左辺は$\mathcal{I}$に属する。つまり$B\in\mathcal{I}$を得る。
これは$\mathcal{I}$が素であることを意味する。
\end{Proof}

\begin{Lem}
　単位的\textup{Banach}代数$\mathcal{B}$の極大な両側イデアルは両側閉イデアルであり、それを極大イデアルと呼ぶことができる。また全体でない両側イデアルに対し、それを含む極大イデアルは必ず存在する。
\end{Lem}
\begin{Proof}
　極大な両側イデアルを$\mathcal{I}\in\Max(\mathcal{B})$とする。これが閉集合であることを示す。
まず$\mathcal{I}$の閉包$\overline{\mathcal{I}}$が両側イデアルであることを示す。$A\in\mathcal{B}, B\in\overline{\mathcal{I}}$に対し、$B$に収束する$\mathcal{I}$の列$\{B_{n}\}\subset\mathcal{I}$を取る。
$||AB_{n}-AB||\le||A||\cdot||B_{n}-B||\rightarrow 0$より$AB_{n}\in\mathcal{I}$だから$AB\in\overline{\mathcal{I}}$が従う。つまり$\overline{\mathcal{I}}$は左イデアルである。逆も同様。
\footnote{ここまで$\mathcal{B}$が単位的であることを用いていない。}
次に$\mathcal{I}=\overline{\mathcal{I}}$を示す。$||I-A||<1$なら$A\in\mathcal{R}_{\mathcal{B}}$である。
$A\in\mathcal{I}$とすると任意の$B\in\mathcal{B}$に対し$B=BA^{-1}A\in\mathcal{I}$より$\mathcal{I}=\mathcal{B}$となるので$\mathcal{I}$が極大イデアルであることに矛盾する。
故に$A\notin\mathcal{I}$であり、$\mathcal{I}\cap\{A\mid ||I-A||<1\}=\emptyset$である。
つまり$I\notin\overline{\mathcal{I}}$であるから$\overline{\mathcal{I}}\neq\mathcal{B}$が従い、極大性から$\mathcal{I}=\overline{\mathcal{I}}$を得る。故に$\mathcal{I}$は両側閉イデアル。
\\
　次に$\mathcal{I}\subsetneq\mathcal{B}$を両側イデアルとする。$\mathcal{I}$を含む両側イデアル$\mathcal{J}\subsetneq\mathcal{B}$の全体を考えれば、包含関係により帰納的半順序集合となる。
従って\textup{Zorn}の補題（選択公理）により極大元を取ることができる。これが求める極大イデアルとなる。
\end{Proof}

\begin{Def}
　代数$\mathcal{A}$に対し、恒等的に$0$でない準同型$\chi:\mathcal{A}\rightarrow\mathbb{C}$を$\mathcal{A}$の指標\textup{:character}という。
$\mathcal{A}$の指標全体を$\Delta(\mathcal{A})$で表す。これを$\mathcal{A}$の構造空間\textup{:structure space}や指標空間\textup{:character space}、スペクトル\textup{:spectrum}などと呼ぶ。
\footnote{普通、可換Banach代数の上に指標や構造空間を定義する。しかし定義するだけなら単位的代数の上にもできるはず。以降の命題も可換性の仮定は必要だろうか。}
\end{Def}

\begin{Rem}
　単位的代数の指標は単位元を保つ準同型である。それは恒等的に$0$でなく、また$\mathbb{C}$が整域であることから分かる。
また$\Delta(0)=\emptyset$である。
\end{Rem}

\begin{Thm}
　$\mathcal{B}$を単位的\textup{Banach}代数とする。$\chi\in\Delta(\mathcal{B})$に対して$\Ker\chi\in\Max(\mathcal{B})$を対応させる写像は全単射となる。
\end{Thm}
\begin{Proof}
　$\mathcal{B}=0$のとき、どちらも空集合なので正しい。$\mathcal{B}\neq 0$とする。
\\
　指標は恒等的に$0$でないから$\Ker\chi$が$\mathcal{B}$でない両側イデアルとなることはよい。$\Ker\chi\subsetneq\mathcal{J}$を両側イデアルとすると、ある$A\in\mathcal{J}\backslash\Ker\chi$が存在する。
$\chi(A)\neq 0$より、$\lambda=\chi(A)^{-1}$と置くと$\lambda\chi(A)=1$が成り立つ。$\lambda=\lambda\chi(I)=\chi(\lambda I)$より、$\chi(\lambda A)=\chi(\lambda I)\chi(A)=\lambda\chi(A)=1$が従う。
そこで$\chi(I)=\chi(\lambda A)$より$B=I-\lambda A\in\Ker\chi\subset\mathcal{J}$を得る。$I=B+\lambda A\in\mathcal{J}$より$\mathcal{J}=\mathcal{B}$が従う。
故に$\Ker\chi\in\Max(\mathcal{B})$が従う。
\\
　単射性を示す。$\chi_{1}(A)\neq\chi_{2}(A)$とする。$B=A-\chi_{1}(A)I$と置けば$B\in\Ker\chi_{1}\backslash\Ker\chi_{2}$より$\Ker\chi_{1}\neq\Ker\chi_{2}$が従う。
\\
　全射性を示す。$\mathcal{I}\in\Max(\mathcal{B})$を取る。補題より$\mathcal{I}$はイデアルだから、$\mathcal{B}/\mathcal{I}$は\textup{Banach}代数となる。
任意の$A\in\mathcal{B}\backslash\mathcal{I}$に対して、$\mathcal{J}=\{AB+C\mid B\in\mathcal{B}, C\in\mathcal{I}\}$とおく。
$\mathcal{J}\subset\mathcal{B}$は両側イデアルとなり、$A\in\mathcal{J}$より$\mathcal{I}\subsetneq\mathcal{J}$を得る。
極大性より$\mathcal{J}=\mathcal{B}$だから、ある$B\in\mathcal{B}, C\in\mathcal{I}$が存在して$AB+C=I$を満たす。
これを商写像で写すと$[A][B]=[I]$であるから、$[A]$は可逆となる。つまり$\mathcal{B}/\mathcal{I}$は体。
\textup{Gelfand-Mazur}の定理より、$\mathcal{B}/\mathcal{I}\cong\mathbb{C}$故に、商写像$\pi:\mathcal{B}\rightarrow\mathcal{B}/\mathcal{I}\cong\mathbb{C}$は指標となる。
$\Ker\pi=\mathcal{I}$だから、全射性が従う。
\end{Proof}

　構造空間がスペクトルと呼ばれる理由は単位的\textup{Banach}代数において次の対応が存在するためである。

\begin{Cor}
　単位的\textup{Banach}代数$\mathcal{B}$及び$A\in\mathcal{B}$に対して、
\begin{enumerate}
\item $\sigma(A)=\{\chi(A)\mid \chi\in\Delta(\mathcal{B})\}$が成り立つ。
\item $\mathcal{B}$が$0$でなければ不等式$|\chi(A)|\le r(A)\le ||A||$が成り立つ。
\end{enumerate}
\end{Cor}
\begin{Proof}
　(1) $\mathcal{B}=0$なら両方とも空集合なので$0$でないとしてよい。
$\lambda\in\sigma(A)$を取ると、$A-\lambda I\in\mathcal{S}$より$A-\lambda I$を含む極大イデアル$\mathcal{J}$が存在する。
先の命題から対応する指標$\chi$を取れば、$\chi(A-\lambda)=0$すなわち$\chi(A)=\lambda\chi(I)=\lambda$を得る。
逆に$\chi(A)=\lambda$なる$\lambda$に対し、$A-\lambda I\in\Ker\chi$であり、再び先の命題により$\Ker\chi$は極大イデアルだから
$A-\lambda I\in\mathcal{S}$が従う。つまり$\lambda\in\sigma(A)$を得る。
\\
　(2) $r(A)\le ||A||$は既に示した。$\chi(A)\in\sigma(A)$より$|\chi(A)|\le r(A)$となる。
\end{Proof}

　\textup{*}代数の指標が\textup{*}準同型、つまり対合を保存するかどうかは圏論的にも気になる所である。
次の命題では単位的\textup{C*}代数に対してそれが従うことを示す。

\begin{Cor}
　単位的\textup{C*}代数$\mathcal{C}$において、指標$\chi$は対合を保存する。
すなわち任意の$A\in\mathcal{C}$に対して$\chi(A^{*})=\overline{\chi(A)}$が成り立つ。
\end{Cor}
\begin{Proof}
$\chi(A^{*}A)$は自己共役だから$\chi(A^{*})\chi(A)\in\sigma(A^{*}A)\subset\mathbb{R}$である。
つまりある実数$r$により$\chi(A^{*})=r\overline{\chi(A)}$と表せる。
また$A+A^{*}$は自己共役だから$\chi(A)+\chi(A^{*})=\chi(A+A^{*})\in\sigma(A+A^{*})\subset\mathbb{R}$である。
ここで実数$a, b$を用いて$\chi(A)=a+ib$と表せば$\chi(A)+r\overline{\chi(A)}=a(1+r)+ib(1-r)\in\mathbb{R}$が従う。
$b\neq 0$なら$1-r=0$より$r=1$を得る。つまり$\chi(A^{*})=\overline{\chi(A)}$である。
一方$b=0$なら$i(A-A^{*})$が自己共役だから$\chi(A)-\chi(A^{*})=a(1-r)$は実数である。
$a\neq 0$なら同様に$\chi(A^{*})=\overline{\chi(A)}$を得る。
$a=0$のとき$\chi(A)=0$だから、$\chi(A^{*})=0=\overline{\chi(A)}$が分かる。
\end{Proof}

-->