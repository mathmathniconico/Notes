
# ネーター加群


## 部分加群の生成


<!--
$ R $-加群$ M $の部分加群$ N_{i}\subset M $が与えられているとする。添え字$ i\in I $は有限個でも無限個でも構わない。
\begin{EnumCond}
\item $ N_{i} $の元による有限和全体を$ \sum_{i\in I} N_{i} $で表し$ N_{i} $達の和という。
\item $ N_{i} $の共通部分$ \bigcap_{i\in I} N_{i} $を$ N_{i} $達の交叉という。
\end{EnumCond}

それぞれ$ M $の部分加群となるが、特に$ I=\lbrace 1, 2, \dotsc, n \rbrace $が有限集合のとき、
$ N_{1}+\dotsb+N_{n} $や$ N_{1}\cap\dotsb\cap N_{n} $と書くこともある。

例えば$ M=\mathbb{Z} $を$ \mathbb{Z} $-加群として考えると、
$ 4\mathbb{Z}+6\mathbb{Z}=2\mathbb{Z}, 4\mathbb{Z}\cap 6\mathbb{Z}=12\mathbb{Z} $が成り立つ。

\begin{Def}{加群の生成}{}
$ S\subset M $に対し、$ S $を含む$ M $の部分加群のうちで最小のものを、
$ S $により生成された$ M $の部分加群と呼び、$ \langle S \rangle_{M} $と表す。つまり
\[ \langle S \rangle_{M}:=\bigcap_{S\subset N\subset M\mathrm{:submod.}}N \]
と定める。
\end{Def}

ここで一般的な慣習として、環$ R $の部分集合$ X\subset R $及び、$ R $-加群$ M $の部分集合$ Y $に対して
\[ XY:=\left\lbrace \sum_{\mathrm{finite}}x_{i}y_{i} \middle| x_{i}\in X, y_{i}\in Y \right\rbrace \]
と定める。つまり$ X $の元と$ Y $の元の有限和全体を指すことにする。（単に積だけではなくて、有限和を取ることが一般的な記法と異なるので注意。）

\begin{Thm}{}{}
$ R $-加群$ M $の部分集合$ S $に対し$ \langle S \rangle_{M}=RS $が成り立つ。
\end{Thm}

（証明）$ S\subset RS $かつ$ RS\subset M $は部分加群だから、定義より$ \langle S \rangle_{M}\subset RS $は言える。
逆に部分加群$ N\subset M $が$ S\subset N $であるとすると、$ RS\subset N $が従う。
よって$ RS\subset \bigcap N=\langle S \rangle_{M} $を得る。$ \square $

$ RS $の元の$ S $による表示は一意的であるとは限らない。実際$ M=\mathbb{Z} $として、$ S=\lbrace 4, 6 \rbrace $と置く。
このとき$ \langle S \rangle_{\mathbb{Z}}=2\mathbb{Z} $だが、
\[ 2=(-1)\cdot 4+1\cdot 6=2\cdot 4+(-1)\cdot 6 \]
であり、表示方法が複数あることが分かる。


\subsection{ネーター加群とネーター環}
数学において、何らかの有限性を持つということは重宝される。
（手で数える程度なら）紙に書き下すことができるし、少し多くても（ある程度は）コンピューターで計算もできる。
人類は有限の世界に生きているのだから、本質的に有限しか認識できないと主張する人もいる。
良く分からない環を表現したものが加群なのだから、そこに有限性を仮定したくなる気持ちも分かるだろう。

$ M=\langle S \rangle_{M}=RS $のとき、$ S $を$ M $の生成系という。
特に生成系として有限集合が取れるとき、$ M $は\index{ゆうげんせいせいかぐん@有限生成加群}有限生成
（\index{finitely generated module}finitely generated）という。

例えば$ \mathbb{Q} $は$ \mathbb{Z} $-加群として有限生成ではない。しかし$ \mathbb{Q} $-加群としては有限生成である。

さて、定義は簡単なのだが、実は有限生成はとても厄介な概念であり、大きな誤解の危険を孕んでいる。
\begin{centering}有限生成な加群の部分加群は有限生成だろうか？\end{centering}

答えは否で、ここでは挙げないが反例がある。つまり、せっかく有限生成な加群を用意しても、うかつに部分加群を考えることができないということになる。
コンピューターに計算させようとして、永遠にプログラムが止まらないなんてことが起こり得てしまう。これはマズいので次の性質が肝になる。

\begin{Def}{}{}
加群$ M $は部分加群が常に有限生成（特に$ M $自身も有限生成）であるとき、
\index{ねーたーかぐん@ネーター加群}ネーター加群（\index{noetherian module}noetherian module）と言う。
\footnote{ドイツの女性数学者Emmy Noetherに由来する。とんでもなく凄い人。}特に環$ R $が$ R $-加群としてネーター加群であるとき
\index{ねーたーかん@ネーター環}ネーター環（\index{noetherian ring}noetherian ring）という。
\end{Def}

上の定義を見て「ずるい」と思ったらその感覚は正しい。別の定義との同値性を示すのが一般的だが、簡単のためにあえて上の方法を採用した。
ネーター女史の貢献もその同値性にあるのだが、今はこの定義のまま進もうと思う。

例えば体$ k $のイデアルは$ \lbrace 0 \rbrace, k $のみだからネーター環である。では$ \mathbb{Z} $はネーター環だろうか？

\begin{Def}{}{}
\[ 0\rightarrow M^{\prime}\xrightarrow{f}M\xrightarrow{g}M^{\prime\prime}\rightarrow 0 \]
を$ R $-加群の完全系列とする。このように$ 0 $に挟まれた三つの完全系列を
\index{たんかんぜんれつ@短完全列}短完全列（\index{short exact sequence}short exact sequence）と呼ぶ。
\end{Def}

\begin{Thm}{}{}
上の条件下において、以下は同値となる。
\begin{EnumEquiv}
\item $ M $はネーター加群である。
\item $ M^{\prime}, M^{\prime\prime} $はネーター加群である。
\end{EnumEquiv}
\end{Thm}

（証明）$ M $がネーター加群であると仮定しよう。$ N^{\prime}\subset M^{\prime} $を部分加群とする。
まず$ f(N^{\prime})\subset M $は部分加群だから、ネーター性より有限生成、
よって$ f(N^{\prime})=R\lbrace x_{1}, \dotsc, x_{n}\rbrace $と書ける。
ここで$ f(x^{\prime}_{i})=x_{i} $となる元$ x^{\prime}_{i}\in N^{\prime} $を取っておく。
これらが$ N^{\prime} $を生成することを示そう。$ x^{\prime}\in N^{\prime} $とすると、適当な$ a_{i}\in R $を用いて
\[ \displaystyle f(x^{\prime})=\sum_{i=1}^{n}a_{i}x_{i}=f\left(\sum_{i=1}^{n}a_{i}x^{\prime}_{i}\right) \]
と表すことが出来る。$ f $は単射だったから
$ x^{\prime}=\sum a_{i}x^{\prime}_{i}\in R\lbrace x^{\prime}_{1}, \dotsc, x^{\prime}_{n}\rbrace $を得る。
逆は$ x^{\prime}_{i}\in N^{\prime} $であることから明らかだろう。故に$ M^{\prime} $はネーター加群である。

次に$ N^{\prime\prime}\subset M^{\prime\prime} $を部分加群とする。$ g^{-1}(N^{\prime\prime})\subset M $は部分加群である。
再びネーター性より有限生成、よって$ g^{-1}(N^{\prime\prime})=R\lbrace y_{1}, \dotsc, y_{m} \rbrace $と書ける。
$ y^{\prime\prime}\in N^{\prime\prime} $に対し、$ g $は全射だったから$ g(y)=y^{\prime\prime} $となる$ y\in M $を取ることが出来る。
今$ y\in g^{-1}(N^{\prime\prime}) $より、適当な$ b_{j}\in R $を用いて$ y=\sum_{j=1}^{m}b_{j}y_{j} $と表すことが出来る。
\[ \displaystyle y^{\prime\prime}=g(y)=g\left( \sum_{j=1}^{m}b_{j}y_{j} \right)=\sum_{j=1}^{m}b_{j}g(y_{j}) \]
だから、$ N^{\prime\prime}\subset R\lbrace g(y_{1}), \dotsc, g(y_{m}) \rbrace $が従う。
やはり逆も明らかなので、$ M^{\prime\prime} $がネーター加群であることが分かる。

最後に$ M^{\prime}, M^{\prime\prime} $をネーター加群と仮定して、部分加群$ N\subset M $が有限生成であることを示そう。まずネーター性より
\[ f^{-1}(N)=R\lbrace x^{\prime}_{1}, \dotsc, x^{\prime}_{n} \rbrace, g(N)=R\lbrace y^{\prime\prime}_{1}, \dotsc, y^{\prime\prime}_{m} \rbrace \]
と表すことができる。ここで$ y_{j}\in N $を$ g(y_{j})=y^{\prime\prime}_{j} $となるように取っておく。
$ z\in N $に対して、$ g(z)=\sum b_{j}y^{\prime\prime}_{j} $と表せる。
$ z-\sum b_{j}y_{j}\in \mathrm{Ker}g=\mathrm{Im}f $だから、$ z-\sum b_{j}y_{j}=\sum a_{i}f(x^{\prime}_{i}) $と表せる。
故に$ z=\sum b_{j}y_{j}+\sum a_{i}f(x^{\prime}_{i}) $を得る。ここから
\[ N=R\lbrace y_{1}, \dotsc, y_{m}, f(x^{\prime}_{1}), \dotsc, f(x^{\prime}_{n}) \rbrace \]
は直ぐに従う。$ \square $

\begin{Exc}{}{}
\[ 0\rightarrow M^{\prime}\xrightarrow{f}M\xrightarrow{g}M^{\prime\prime}\rightarrow 0 \]
を$ R $-加群の完全系列とする。このとき以下が成り立つことを証明せよ。逆も成り立つだろうか？
\begin{EnumCond}
\item $ M $が有限生成なら$ M^{\prime\prime} $も有限生成である。
\item $ M^{\prime}, M^{\prime\prime} $が有限生成なら$ M $も有限生成である。
\end{EnumCond}
\end{Exc}


\subsection{この節のまとめ}
部分加群に対する二つの演算$ \sum_{i\in I }N_{i}, \bigcap_{i\in I}N_{i} $を導入し、それを用いて生成という概念を紹介した。
生成系として有限集合が取れるとき有限生成であるというが、一般に有限生成加群の部分加群は有限生成とは限らない。
この条件を満たす加群をEmmy Noetherに由来してネーター加群という。ネーター加群は完全系列に対して良く振舞う。

-->