
# ボレル可測

<!--
\subsection{位相空間と連続写像}
\begin{Def}{}{}
集合$ X $において$ \mathcal{O}\subset 2^{X} $が次の3条件を満たすとき、$ \mathcal{O} $は$ X $上の位相（topology）あるいは開集合系であるという。
\begin{EnumCond}
\item $ \emptyset\in\mathcal{O}, X\in\mathcal{O} $である。
\item $ U, V\in\mathcal{O} $なら$ U\cap V\in\mathcal{O} $である。
\item $ \lambda\in\Lambda $について$ U_{\lambda}\in\mathcal{O} $なら$ \bigcup_{\lambda\in\Lambda}U_{\lambda}\in\mathcal{O} $である。
\end{EnumCond}

このとき組$ ( X, \mathcal{O} ) $を位相空間といい、集合$ U\in\mathcal{O} $は（$ \mathcal{O} $-）開集合（open set）であるという。
\end{Def}

例えば$ \mathcal{O}=\lbrace \emptyset, X \rbrace $は包含関係における最小の位相を定め、密着位相（indiscrete topology）と呼ばれる。
また$ \mathcal{O}=2^{X} $は包含関係における最大の位相を定め、離散位相（discrete topology）と呼ばれる。この二つは自明（trivial）な位相とも呼ばれる。

位相は「近さ」の一般化であるとよく言われるが、上の定義だとその感覚が良く分からないだろう。
実は位相には同値な公理系が複数存在し、そのうちの一つに「近傍系」を利用するものがある。これを説明するために幾つかの用語を定義しよう。

\begin{Def}{}{}
$ ( X, \mathcal{O} ) $を位相空間とする。$ F\subset X $が$ X\backslash F\in\mathcal{O} $を満たすとき、（$ \mathcal{O} $-）閉集合（closed set）であるという。
\end{Def}

\begin{Exc}{}{}
位相空間$ ( X, \mathcal{O} ) $において、閉集合全体$ \mathfrak{A} $は以下を満たす。
\begin{EnumCond}
\item $ X\in\mathfrak{A}, \emptyset\in\mathfrak{A} $である。
\item $ F, G\in\mathfrak{A} $なら$ F\cup G\in\mathfrak{A} $である。
\item $ \lambda\in\Lambda $について$ F_{\lambda}\in\mathfrak{A} $なら$ \bigcap_{\lambda\in\Lambda}F_{\lambda}\in\mathfrak{A} $である。
\end{EnumCond}

逆にこれを満たす$ \mathfrak{A}\subset 2^{X} $に対し、$ \mathfrak{A} $を閉集合とする$ X $上の位相が唯一つ存在する。
\end{Exc}

\begin{Def}{}{}
$ ( X, \mathcal{O} ) $を位相空間、$ A\subset X $とする。$ x\in X $について以下を定める。
\begin{EnumCond}
\item ある開集合$ U\in\mathcal{O} $が存在して$ x\in U\subset A $が成り立つとき$ x $は$ A $の内点であるという。
$ A $の内点全体を$ A^{i} $あるいは$ A^{\circ} $で表し、$ A $の内部（interior）あるいは開核という。
\item $ x $が$ X\backslash A $の内点であるとき$ x $は$ A $の外点であるという。$ A $の外点全体を$ A^{e} $で表し、$ A $の外部（exterior）という。
\item $ x $が$ A $の内点でも外点でもないとき$ x $は$ A $の境界点であるという。$ A $の境界点全体を$ A^{f} $で表し、$ A $の境界（frontier）という。
\item 任意の開集合$ U\in\mathcal{O} $について$ x\in U $なら$ U\cap A\neq\emptyset $が成り立つとき$ x $は$ A $の触点であるという。
$ A $の触点全体を$ \overline{A} $あるいは$ A^{a} $で表し、$ A $の閉包（closure）という。
\end{EnumCond}
\end{Def}

$ A^{i} $は$ A $に含まれる最大の開集合であり、$ \overline{A} $は$ A $を含む最小の閉集合である。

写像$ i\colon A\mapsto A^{i} $を開核作用子、写像$ k\colon A\mapsto\overline{A} $を閉包作用子という。

\begin{Exc}{}{}
位相空間$ ( X, \mathcal{O} ) $において、開核作用子は$ A, B\subset X $について以下を満たす。
\begin{EnumCond}
\item $ i( X )=X $である。
\item $ i( A )\subset A $である。
\item $ i( A\cap B )=i( A )\cap i( B ) $である。
\item $ i( i( A ) )=i( A ) $である。
\end{EnumCond}

逆にこれを満たす写像$ i $に対し、$ i( A ) $を$ A $の内部とする$ X $上の位相が唯一つ存在する。
\end{Exc}

\begin{proof}
（ヒント）$ \mathcal{O}:=\lbrace U : i( U )=U \rbrace $とすればよい。$ \square $
\end{proof}

\begin{Exc}{クラトウスキイの公理系}{}
位相空間$ ( X, \mathcal{O} ) $において、閉包作用子は$ A, B\subset X $について以下を満たす。
\begin{EnumCond}
\item $ k( \emptyset )=\emptyset $である。
\item $ k( A )\supset A $である。
\item $ k( A\cup B )=k( A )\cup k( B ) $である。
\item $ k( k( A ) )=k( A ) $である。
\end{EnumCond}

逆にこれを満たす写像$ k $に対し、$ k( A ) $を$ A $の閉包とする$ X $上の位相が唯一つ存在する。
\end{Exc}

\begin{proof}
（ヒント）$ \mathcal{O}:=\lbrace U : k( X\backslash U )=X\backslash U \rbrace $とすればよい。$ \square $
\end{proof}

\begin{Def}{}{}
$ ( X, \mathcal{O} ) $を位相空間、$ a\in X $とする。$ N\subset X $が$ a\in N^{i} $を満たすとき、$ a $の近傍（neighborhood）であるという。
$ a $の近傍全体を$ \mathfrak{N}( a ) $で表し、$ a $の近傍系という。
\end{Def}

\begin{Exc}{ハウスドルフの公理系}{}
位相空間$ ( X, \mathcal{O} ) $において、近傍系は$ a\in X $について以下を満たす。
\begin{EnumCond}
\item $ X\in\mathfrak{N}( a ) $であり、$ N\in\mathfrak{N}( a ) $なら$ a\in N $である。
\item $ N, M\in\mathfrak{N}( a ) $なら$ N\cap M\in\mathfrak{N}( a ) $である。
\item $ N\in\mathfrak{N}( a ) $であり、$ N\subset M $なら$ M\in\mathfrak{N}( a ) $である。
\item $ N\in\mathfrak{N}( a ) $について、ある$ M\in\mathfrak{N}( a ) $が存在し、任意の$ b\in M $について$ N\in\mathfrak{N}( b ) $が成り立つ。
\end{EnumCond}

逆にこれを満たす写像$ a\mapsto\mathfrak{N}( a ) $に対し、$ \mathfrak{N}( a ) $を$ a $の近傍系とする$ X $上の位相が唯一つ存在する。 
\end{Exc}

\begin{proof}
（ヒント）$ \mathcal{O}:=\lbrace N : a\in N \Rightarrow N\in\mathfrak{N}( a ) \rbrace $とすればよい。$ \square $
\end{proof}

次に連続写像を定義する。

\begin{Def}{}{}
$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $を位相空間、$ a\in X $とする。写像$ f\colon X\rightarrow Y $が
\[ N\in\mathfrak{N}( f( a ) )\Rightarrow f^{-1}( N )\in\mathfrak{N}( a ) \]
を満たすとき、$ f $は$ a $において連続（continuous）であるという。
\end{Def}

\begin{Prop}{}{}
$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $を位相空間とする。写像$ f\colon X\rightarrow Y $に関して以下は同値である。
\begin{EnumEquiv}
\item 任意の$ a\in X $において$ f $は連続である。
\item $ U\subset Y $が$ \mathcal{O}_{Y} $-開集合なら$ f^{-1}( U )\subset X $は$ \mathcal{O}_{X} $-開集合である。
\item $ F\subset Y $が$ \mathcal{O}_{Y} $-閉集合なら$ f^{-1}( F )\subset X $は$ \mathcal{O}_{X} $-閉集合である。
\item 任意の$ A\subset X $に対し$ f( \overline{A} )\subset\overline{f( A )} $が成り立つ。
\end{EnumEquiv}
\end{Prop}

\begin{proof}
（証明）略。$ \square $
\end{proof}

\begin{Def}{}{}
上の4条件の何れか（従って全て）を満たすとき、$ f $は位相空間$ ( X, \mathcal{O}_{X} ) $から$ ( Y, \mathcal{O}_{Y} ) $への連続写像という。
\end{Def}

連続写像の合成は連続写像であり、恒等写像は連続写像である。故に位相空間と連続写像は圏の対象と射を定める。これを位相空間の圏といい圏$ \mathbf{Top} $と記す。




\subsection{ボレル集合族}
\begin{Def}{}{}
位相空間$ ( X, \mathcal{O} ) $に対し、位相により生成される$ \sigma $-加法族$ \sigma\lbrack \mathcal{O} \rbrack $をボレル集合族と呼ぶ。
特に$ \sigma\lbrack \mathcal{O} \rbrack $-可測であることをボレル可測であるという。
\end{Def}

ボレル集合族は、位相が明らかな場合は$ \mathscr{B}_{X} $や$ \mathscr{B}( X ) $などと記すこともある。

位相空間$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $に対し、連続写像$ f\colon X\rightarrow Y $は$ \mathcal{O}_{Y} $-開集合を$ \mathcal{O}_{X} $-開集合に引き戻す。
従って$ f $は可測空間$ ( X, \sigma\lbrack \mathcal{O}_{X} \rbrack ) $から$ ( Y, \sigma\lbrack \mathcal{O}_{Y} \rbrack ) $への可測函数を定め、
更にこれは圏$ \mathbf{Top} $から圏$ \mathbf{meas} $への函手を定める。この函手をボレル函手と呼ぶことにする。

位相も$ \sigma $-加法族と同様に、直接指定されて表されるという状況はあまり多くなく、大抵は基本となる集合族が位相を「生成」していると考える。「生成」の方法はいくつかあるが、ここでは開基というものを紹介しよう。

\begin{Def}{}{}
$ ( X, \mathcal{O} ) $を位相空間、$ \mathcal{B}\subset\mathcal{O} $とする。
任意の開集合$ U\in\mathcal{O} $に対し、ある$ \mathcal{B}_{0}\subset\mathcal{B} $が存在して$ U=\cup\mathcal{B}_{0} $と表せるとき、
$ \mathcal{B} $は位相$ \mathcal{O} $の開基（open basis）であるという。
\end{Def}

言い換えれば、任意の開集合$ U\in\mathcal{O} $及び$ x\in U $に対し、適当な$ B\in\mathcal{B} $を取れば$ x\in B\subset U $が成り立つようにできる。

\begin{Rem}{}{}
集合族$ \mathfrak{A}\subset 2^{X} $について$ \mathfrak{A} $が空でないときは
\begin{align*}
\cup\mathfrak{A}&=\bigcup_{A\in\mathfrak{A}}A,& \cap\mathfrak{A}&=\bigcap_{A\in\mathfrak{A}}A
\end{align*}
と定め、
\begin{align*}
\cup\emptyset&=\emptyset, & \cap\emptyset&=X
\end{align*}
と定める。
\end{Rem}

通常の位相を持ったユークリッド空間$ \mathbb{R} $の開基としては、例えば開区間全体がある。当然開集合全体も開基であり、位相については様々な開基を考えることが出来る。しかし、開基が定める位相は次の命題より一意的である。

\begin{Prop}{}{}
$ X $を集合、$ \mathcal{B}\subset 2^{X} $とする。次は同値である。
\begin{EnumEquiv}
\item $ \mathcal{B} $はある位相の開基である。
\item 次の2条件を満たす。
	\begin{EnumCond}
 	\item $ X=\cup\mathcal{B} $である。
	\item $ B_{1}, B_{2}\in\mathcal{B} $及び$ x\in B_{1}\cap B_{2} $について、ある$ B\in\mathcal{B} $が存在して$ x\in B\subset B_{1}\cap B_{2} $を満たす。
	\end{EnumCond}
\end{EnumEquiv}

このとき$ \mathcal{B} $を開基とする位相は一意的である。
\end{Prop}

\begin{proof}
（証明）位相$ \mathcal{O} $が$ \mathcal{B} $を開基とするなら、
\[ \mathcal{O}=\lbrace \cup\mathfrak{A} : \mathfrak{A}\subset\mathcal{B} \rbrace \]
という等式を満たさなければならない。一意性はこれより明らか。また下の2条件を満たすとき、この等式で定めた$ \mathcal{O} $は位相を定め、$ \mathcal{B} $はその開基となる。上から下も簡単。$ \square $
\end{proof}

さて位相空間$ ( X, \mathcal{O} ) $の開基$ \mathcal{B} $について考えるとき、当然問題となってくるのは、
開基により生成される$ \sigma $-加法族$ \sigma\lbrack \mathcal{B} \rbrack $と、位相により生成される$ \sigma $-加法族$ \sigma\lbrack \mathcal{O} \rbrack $との関係である。
もちろん$ \sigma\lbrack \mathcal{B} \rbrack\subset\sigma\lbrack \mathcal{O} \rbrack $は成り立つが、これは必ずしも一致するとは限らない。

\begin{Def}{}{}
$ ( X, \mathcal{O} ) $を位相空間とする。位相$ \mathcal{O} $が、高々可算個の開集合からなる開基を持つとき、第2可算公理を満たすという。
\end{Def}

\begin{Lem}{}{}
位相空間$ ( X, \mathcal{O} ) $は第2可算公理を満たし、開基$ \mathcal{B} $はその可算開基を含むとする。
このとき$ \sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathcal{B} \rbrack $が成り立つ。
\end{Lem}

\begin{proof}
（証明）開集合$ U\in\mathcal{O} $について、$ \mathcal{B} $は可算開基$ \mathcal{B}^{\prime} $を含むので、
$ \mathcal{B}^{\prime}_{0}\subset\mathcal{B}^{\prime} $を取り$ U=\cup\mathcal{B}^{\prime}_{0} $と表せる。
このとき$ O\in\sigma\lbrack \mathcal{B} \rbrack $を得るから、最小性より$ \sigma\lbrack \mathcal{O} \rbrack\subset\sigma\lbrack \mathcal{B} \rbrack $が従う。$ \square $
\end{proof}




\subsection{積位相空間とボレル集合族}
位相空間に対しても積を考えることが出来る。我々は可測空間において有限積しか今の所は考えていないので、位相空間においても同様に有限積のみを考えることにする。

\begin{Def}{}{}
$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $を位相空間とする。
\[ \mathcal{O}_{X}\times\mathcal{O}_{Y}=\lbrace U\times V : U\in\mathcal{O}_{X}, V\in\mathcal{O}_{Y} \rbrace\subset 2^{X\times Y} \]
は開基の2条件を満たし、ある一意的な位相$ \mathcal{O}\subset 2^{X\times Y} $の開基となる。
この位相を箱型積位相（box product topology）と呼び、$ ( X\times Y, \mathcal{O} ) $を箱型積位相空間という。
\end{Def}

実は、任意の添え字を持つ位相空間の族について、その直積集合上に積位相と呼ばれる位相を定めることができ、これを積位相空間、あるいは単に積空間と呼ぶ。
このとき積空間と各成分への射影は普遍性を満たし、圏$ \mathbf{Top} $における積対象となる。積空間の位相は一般的に箱型積位相とは異なるものだが、添え字集合が有限のときには一致する。
従って上で定めた箱型積位相空間$ ( X\times Y, \mathcal{O} ) $は、積空間であり、$ ( X, \mathcal{O}_{X} ) $と$ ( Y, \mathcal{O}_{Y} ) $の積対象でもある。
これより、以下では「箱型」という用語は省略して述べる。

\begin{Prop}{}{}
$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $を位相空間とする。
$ \mathcal{B}_{X}, \mathcal{B}_{Y} $を$ \mathcal{O}_{X}, \mathcal{O}_{Y} $の開基とすれば、$ \mathcal{B}_{X}\times\mathcal{B}_{Y} $は積位相の開基となる。

特に$ \mathcal{B}_{X}, \mathcal{B}_{Y} $が可算のとき、$ \mathcal{B}_{X}\times\mathcal{B}_{Y} $も可算である。故に有限積は第2可算公理を保つ。
\end{Prop}

\begin{proof}
（証明）開基の2条件が成り立つことを示せば良い。$ \square $
\end{proof}

位相空間$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $について、$ \mathcal{B}_{X}, \mathcal{B}_{Y} $をその開基、$ ( X\times Y, \mathcal{O} ) $をその積空間とする。このとき
\[ \sigma\lbrack \mathcal{B}_{X}\times\mathcal{B}_{Y} \rbrack \subset \sigma\lbrack \mathcal{B}_{X}\times Y\cup X\times\mathcal{B}_{Y} \rbrack \subset \sigma\lbrack \mathcal{O}_{X}\times Y\cup X\times\mathcal{O}_{Y} \rbrack \subset \sigma\lbrack \mathcal{O} \rbrack \]
が成り立つ。ここで
\begin{align*}
\sigma\lbrack \mathcal{B}_{X} \rbrack\otimes\sigma\lbrack \mathcal{B}_{Y} \rbrack &:= \sigma\left\lbrack \sigma\lbrack \mathcal{B}_{X} \rbrack\times Y\cup X\times\sigma\lbrack \mathcal{B}_{Y} \rbrack \right\rbrack = \sigma\left\lbrack \sigma\lbrack \mathcal{B}_{X} \rbrack\times\sigma\lbrack \mathcal{B}_{Y} \rbrack \right\rbrack, \\
\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack &:= \sigma\left\lbrack \sigma\lbrack \mathcal{O}_{X} \rbrack\times Y\cup X\times\sigma\lbrack \mathcal{O}_{Y} \rbrack \right\rbrack = \sigma\left\lbrack \sigma\lbrack \mathcal{O}_{X} \rbrack\times\sigma\lbrack \mathcal{O}_{Y} \rbrack \right\rbrack
\end{align*}
が成り立つので、
\begin{align*}
\sigma\lbrack \mathcal{B}_{X}\times Y\cup X\times\mathcal{B}_{Y} \rbrack &\subset \sigma\lbrack \mathcal{B}_{X} \rbrack\otimes\sigma\lbrack \mathcal{B}_{Y} \rbrack, \\
\sigma\lbrack \mathcal{O}_{X}\times Y\cup X\times\mathcal{O}_{Y} \rbrack &\subset \sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack
\end{align*}
も成り立つ。

ここで興味があるのは、これらの包含関係が「いつ」等号となるかという疑問である。この一つの答えを、我々は第2可算公理の文脈で得ることが出来る。

\begin{Thm}{}{}
位相空間$ ( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} ) $は第2可算公理を満たし、$ \mathcal{B}_{X}, \mathcal{B}_{Y} $はその可算開基とする。積位相を$ \mathcal{O} $とすれば、
\[ \sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathcal{B}_{X}\times\mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{B}_{X} \rbrack\otimes\sigma\lbrack \mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack \]
が成り立つ。
\end{Thm}

\begin{proof}
（証明）補題より$ \sigma\lbrack \mathcal{B}_{X} \rbrack=\sigma\lbrack \mathcal{O}_{X} \rbrack, \sigma\lbrack \mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{O}_{Y} \rbrack $
及び$ \sigma\lbrack \mathcal{B}_{X}\times\mathcal{B}_{Y} \rbrack = \sigma\lbrack \mathcal{O} \rbrack $が成り立つ。
従って上の議論から$ \sigma\lbrack \mathcal{O} \rbrack\subset\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack $となるため、逆を示せば良い。

$ f\colon X\times Y\rightarrow X, g\colon X\times Y\rightarrow Y $を射影とする。このとき積位相の定義より$ f, g $は連続写像となるから、可測写像でもある。
従って普遍性より、唯一つの可測写像$ h\colon ( X\times Y, \sigma\lbrack \mathcal{O} \rbrack )\rightarrow ( X\times Y, \sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack ) $が存在して、図式を可換にする。
このとき$ h $は定め方より恒等写像となるが、可測性より$ \sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack \subset \sigma\lbrack \mathcal{O} \rbrack $を得る。$ \square $
\end{proof}

定理の示すところは、可算開基を持つ位相空間について、積位相空間のボレル集合族は、ボレル集合族の積$ \sigma $-加法族である、ということであり、
ボレル集合族の表記に倣えば$ \mathscr{B}_{X\times Y}=\mathscr{B}_{X}\otimes\mathscr{B}_{Y} $が成り立つということを意味している。
この意味でボレル函手は有限積に関して自然に振舞うことが分かる。

\end{document}

-->