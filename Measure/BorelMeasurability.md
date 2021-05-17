
# ボレル集合族

__定義__ 位相空間$( X, \mathcal{O} )$に対し、位相により生成される$\sigma$-加法族$\sigma\lbrack \mathcal{O} \rbrack$をボレル集合族と呼ぶ。特に$\sigma\lbrack \mathcal{O} \rbrack$可測であることをボレル可測であるという。

ボレル集合族は、位相が明らかな場合は$\mathscr{B}_{X}$や$\mathscr{B}( X )$などと記すこともある。

> 位相空間$( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$に対し、連続写像$f\colon X\rightarrow Y$は$\mathcal{O}_{Y}$開集合を$\mathcal{O}_{X}$開集合に引き戻す。従って$f$は可測空間$( X, \sigma\lbrack \mathcal{O}_{X} \rbrack )$から$( Y, \sigma\lbrack \mathcal{O}_{Y} \rbrack )$への可測函数を定め、更にこれは圏$\mathbf{Top}$から圏$\mathbf{meas}$への函手を定める。この函手をボレル函手と呼ぶことにする。

生成された位相との関わりを見ていく。$( X, \mathcal{O} )$を位相空間とし、$\mathcal{B}$をその開基とする。開基と位相のそれぞれにより生成される$\sigma$加法族$\sigma\lbrack \mathcal{B} \rbrack$と$\sigma\lbrack \mathcal{O} \rbrack$の関係はどうなるだろうか。定義より$\sigma\lbrack \mathcal{B} \rbrack\subset\sigma\lbrack \mathcal{O} \rbrack$となるが、必ずしも一致するとは限らない。

__補題__ 位相空間$( X, \mathcal{O} )$は第2可算公理を満たし、開基$\mathcal{B}$はその可算開基を含むとする。このとき$\sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathcal{B} \rbrack$が成り立つ。

（証明）開集合$U\in\mathcal{O}$について、$\mathcal{B}$は可算開基$\mathcal{B}^{\prime}$を含むので、$\mathcal{B}^{\prime}_{0}\subset\mathcal{B}^{\prime}$を取り$U=\cup\mathcal{B}^{\prime}_{0}$と表せる。このとき$O\in\sigma\lbrack \mathcal{B} \rbrack$を得るから、最小性より$\sigma\lbrack \mathcal{O} \rbrack\subset\sigma\lbrack \mathcal{B} \rbrack$が従う。$\square$


<!--


\subsection{積位相空間とボレル集合族}
位相空間に対しても積を考えることが出来る。我々は可測空間において有限積しか今の所は考えていないので、位相空間においても同様に有限積のみを考えることにする。

\begin{Def}{}{}
$( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間とする。
\[ \mathcal{O}_{X}\times\mathcal{O}_{Y}=\lbrace U\times V : U\in\mathcal{O}_{X}, V\in\mathcal{O}_{Y} \rbrace\subset 2^{X\times Y} \]
は開基の2条件を満たし、ある一意的な位相$\mathcal{O}\subset 2^{X\times Y}$の開基となる。
この位相を箱型積位相（box product topology）と呼び、$( X\times Y, \mathcal{O} )$を箱型積位相空間という。
\end{Def}

実は、任意の添え字を持つ位相空間の族について、その直積集合上に積位相と呼ばれる位相を定めることができ、これを積位相空間、あるいは単に積空間と呼ぶ。
このとき積空間と各成分への射影は普遍性を満たし、圏$\mathbf{Top}$における積対象となる。積空間の位相は一般的に箱型積位相とは異なるものだが、添え字集合が有限のときには一致する。
従って上で定めた箱型積位相空間$( X\times Y, \mathcal{O} )$は、積空間であり、$( X, \mathcal{O}_{X} )$と$( Y, \mathcal{O}_{Y} )$の積対象でもある。
これより、以下では「箱型」という用語は省略して述べる。

\begin{Prop}{}{}
$( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$を位相空間とする。
$\mathcal{B}_{X}, \mathcal{B}_{Y}$を$\mathcal{O}_{X}, \mathcal{O}_{Y}$の開基とすれば、$\mathcal{B}_{X}\times\mathcal{B}_{Y}$は積位相の開基となる。

特に$\mathcal{B}_{X}, \mathcal{B}_{Y}$が可算のとき、$\mathcal{B}_{X}\times\mathcal{B}_{Y}$も可算である。故に有限積は第2可算公理を保つ。
\end{Prop}

\begin{proof}
（証明）開基の2条件が成り立つことを示せば良い。$\square$
\end{proof}

位相空間$( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$について、$\mathcal{B}_{X}, \mathcal{B}_{Y}$をその開基、$( X\times Y, \mathcal{O} )$をその積空間とする。このとき
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
位相空間$( X, \mathcal{O}_{X} ), ( Y, \mathcal{O}_{Y} )$は第2可算公理を満たし、$\mathcal{B}_{X}, \mathcal{B}_{Y}$はその可算開基とする。積位相を$\mathcal{O}$とすれば、
\[ \sigma\lbrack \mathcal{O} \rbrack=\sigma\lbrack \mathcal{B}_{X}\times\mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{B}_{X} \rbrack\otimes\sigma\lbrack \mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack \]
が成り立つ。
\end{Thm}

\begin{proof}
（証明）補題より$\sigma\lbrack \mathcal{B}_{X} \rbrack=\sigma\lbrack \mathcal{O}_{X} \rbrack, \sigma\lbrack \mathcal{B}_{Y} \rbrack=\sigma\lbrack \mathcal{O}_{Y} \rbrack$
及び$\sigma\lbrack \mathcal{B}_{X}\times\mathcal{B}_{Y} \rbrack = \sigma\lbrack \mathcal{O} \rbrack$が成り立つ。
従って上の議論から$\sigma\lbrack \mathcal{O} \rbrack\subset\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack$となるため、逆を示せば良い。

$f\colon X\times Y\rightarrow X, g\colon X\times Y\rightarrow Y$を射影とする。このとき積位相の定義より$f, g$は連続写像となるから、可測写像でもある。
従って普遍性より、唯一つの可測写像$h\colon ( X\times Y, \sigma\lbrack \mathcal{O} \rbrack )\rightarrow ( X\times Y, \sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack )$が存在して、図式を可換にする。
このとき$h$は定め方より恒等写像となるが、可測性より$\sigma\lbrack \mathcal{O}_{X} \rbrack\otimes\sigma\lbrack \mathcal{O}_{Y} \rbrack \subset \sigma\lbrack \mathcal{O} \rbrack$を得る。$\square$
\end{proof}

定理の示すところは、可算開基を持つ位相空間について、積位相空間のボレル集合族は、ボレル集合族の積$\sigma$-加法族である、ということであり、
ボレル集合族の表記に倣えば$\mathscr{B}_{X\times Y}=\mathscr{B}_{X}\otimes\mathscr{B}_{Y}$が成り立つということを意味している。
この意味でボレル函手は有限積に関して自然に振舞うことが分かる。

\end{document}

-->