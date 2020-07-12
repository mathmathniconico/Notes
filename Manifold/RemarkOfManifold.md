
## 多様体の実現

__定義__ $C^{r}$多様体$M, N$において、写像$f\colon M\rightarrow N$が$C^{s}$級（$s\le r$）であるとは、$M, N$の局所座標系$\lbrace (U_{\alpha}, \phi_{\alpha}) \rbrace, \lbrace (V_{\beta}, \psi_{\beta}) \rbrace$について、$\psi_{\beta}\circ f\circ\phi_{\alpha}^{-1}$が$C^{s}$級函数であることをいう。

この定義は局所座標系の取り方に依らない。つまり$C^{r}$同値な開被覆をどのように選んでも$f$が$C^{s}$級であることは変わらない。故に多様体の$C^{r}$構造にのみ依存する性質であるため、多様体の間の写像として適切である。

$C^{r}$多様体$M, N$の間に同相写像$\Phi$が存在し、$\Phi$も$\Phi^{-1}$も上の意味で$C^{r}$級であるとき、$M$と$N$は$C^{r}$同相であるという。一般に$M$と$\Phi$によって同相な位相空間$X$は、$(\Phi(U_{\alpha}), \phi_{\alpha}\circ\Phi^{-1})$を局所座標とする$C^{r}$多様体となる。このとき明らかに$M$と$X$は多様体として$C^{r}$同相になる。

ここで問題となるのは、任意の多様体は、あるユークリッド一般曲面として実現可能かどうかである。つまり$\mathbb{R}^{L}$の中への$C^{r}$同相写像を与えることができるだろうか。

__事実__ （H.Whitney, 1936）多様体が高々可算個の局所座標で覆えるなら、そのような$n$次元$C^{r}$多様体は、十分大きな$L$に対して、$\mathbb{R}^{L}$内の$C^{r}$級曲面と$C^{r}$同相である。（より精密に$L=2n+1$でよいことと閉曲面であることを示した。更にWhitneyは1944年に$L=2n$でもよいことを示している。）

この結果により、抽象的な多様体の定義は不用に思えるかもしれない。しかし例えば実射影空間$P^{n}$の性質は、原点を通る直線全体からなるという幾何的性質に由来しているのであって、決して曲面として実現されるという事実によるものではない。つまり抽象化こそ本体であって、数学のあらゆる場面で適応可能な幅の広さこそが重要である。更にいえば、ひとたび抽象化されることでもっと広い概念の考察を可能にすることが数学の自由さであり、その立場において、もはやWhitneyの定理が成立するとは限らないのである。


## 可微分構造の一意性、実解析的多様体

以下$s\le r$とする。多様体の$C^{s}$構造は、局所座標の$C^{r}$性に依ることを以前注意として（言葉は少し違うが）触れた。今$M$を$C^{s}$多様体とする。局所座標系$\lbrace (U_{\alpha}, \phi_{\alpha}) \rbrace$の取り方は様々だが、次が成り立つと仮定する。

- $U_{\alpha}\cap U_{\beta}\neq\empty$のとき$\phi_{\beta}\circ\phi_{\alpha}^{-1}$は$C^{r}$級函数である。

このとき$M$は$C^{r}$級多様体としての構造を持つ。つまり$C^{s}$構造の中に、細分化された$C^{r}$構造が含まれていることを意味する。

ここで問題となるのは次の2つである。

- 任意の$C^{s}$構造には$C^{r}$構造が存在するか？
- もし存在するならその構造は一意的か？　つまり$C^{r}$同相なものになるか？

特に$r=\infty$のとき、これらの問題は1936年にWhitneyによって肯定的によって解かれている。（精密には多様体は可算個の局所座標で覆えるとし、$s\ge 1$である。$s=0$については存在も一意性も否定的であり、位相構造と可微分構造の本質的な差を見ることができる。）

ちなみに、$C^{\infty}$構造より一層細かい構造として、実解析的な同相写像を出発点とする$C^{\omega}$多様体がある。これについても$C^{\infty}$多様体の上に、唯一つの$C^{\omega}$構造が存在することが知られている。

> 可算個の局所座標で覆えることはもちろん、局所有限性などの条件が必要かもしれない。後で厳密な議論を行うと思う。


## 複素多様体

複素函数に関しては可微分性が解析性まで延長されるため、次のような定義が可能である。

__定義__  Hausdorff空間$M$について、$M$を覆う開集合の族$\lbrace U_{\lambda} : \lambda\in\Lambda \rbrace$が存在し、各$\lambda\in\Lambda$に対して$U_{\lambda}$から$\mathbb{C}^{n}$のある開集合への同相写像$\phi_{\lambda}$が存在して、$U_{\lambda}\cap U_{\mu}\neq\empty$のとき$\phi_{\mu}\circ\phi_{\lambda}^{-1}$が$\phi_{\lambda}(U_{\lambda}\cap U_{\mu})$から$\phi_{\mu}(U_{\lambda}\cap U_{\mu})$への複素解析的函数であるとする。このとき$M$を$n$次元複素多様体という。

複素多様体$M$は

$$
(x_{1}+\sqrt{-1}y_{1}, \dotsc, x_{n}+\sqrt{-1}y_{n})\mapsto (x_{1}, y_{1}, \dotsc, x_{n}, y_{n})
$$

を通して$2n$次元の$C^{\infty}$多様体としての構造を持つ。

例えば実射影空間を定義したときと同様にして、$\mathbb{C}^{n+1}\backslash\lbrace 0 \rbrace$の元の比$\lbrack z_{1} : \dotsb : z_{n+1} \rbrack$により複素射影空間$P^{n}(\mathbb{C})$を定義できる。

複素構造の存在や実現可能性は、実の場合と比べて易しくない。例えば偶数次元の球面$S^{2n}(n\ge 1, n\neq 3)$には複素構造が存在しない。コンパクトな複素多様体は（1点などの自明な場合を除いて）$\mathbb{C}^{L}$の中に複素解析的に埋め込めるとは限らない。$\mathbb{C}^{n}$と位相的には同相でも定数函数しか正則函数が存在しないような複素構造も知られている。


### 多様体の複素化

> あまり自信がないが、この本は実多様体のみを扱うので基本気にしなくていいはず。

$M$を$C^{\infty}$多様体とすると、先程述べた通り実解析的な構造が本質的に唯一つ定まる。つまり適当な（局所有限な）局所座標系$\lbrace (U_{\alpha}, \phi_{\alpha}) \rbrace$を取ると、座標変換$\phi_{\beta\alpha}=\phi_{\beta}\circ\phi_{\alpha}^{-1}$が実解析函数となるように取れる。従って解析接続が可能で、$\phi_{\alpha}(U_{\alpha}\cap U_{\beta})$の$\mathbb{C}^{n}$における近傍上で定義された複素解析函数$\phi_{\beta\alpha}^{\mathbb{C}}$に一意的に拡張できる。

これらを糊として貼り合わせたいのだが、定義域がバラバラだと上手く行かない。しかし$M$は局所有限なので、任意の$p\in M$に対して$p$の開近傍$O$を取ることができて、$O\cap U_{\alpha}\neq\empty$なる$\alpha$は有限個である。そこで$O$上で考えると、適当な正の連続関数$\varepsilon$が取れて、

$$
\begin{aligned}
\phi_{\alpha}(O\cap U_{\alpha})^{\mathbb{C}} &:=\lbrace (x_{i}+\sqrt{-1}y_{i})\in\mathbb{C}^{n} : x\in\phi_{\alpha}(O\cap U_{\alpha}), \vert y_{i} \vert\lt\varepsilon(x) \rbrace, \\
\phi_{\alpha}(O\cap U_{\alpha}\cap U_{\beta})^{\mathbb{C}} &:=\phi_{\alpha}(O\cap U_{\alpha})^{\mathbb{C}}\cap\lbrace (x_{i}+\sqrt{-1}y_{i})\in\mathbb{C}^{n} : x\in\phi_{\alpha}(O\cap U_{\alpha}\cap U_{\beta}) \rbrace
\end{aligned}
$$

としたときに、$\phi_{\beta\alpha}^{\mathbb{C}}$が$\phi_{\alpha}(O\cap U_{\alpha}\cap U_{\beta})^{\mathbb{C}}$上の複素解析函数となる。解析接続の一意性より座標変換の性質から$\phi_{\gamma\beta}^{\mathbb{C}}\circ\phi_{\beta\alpha}^{\mathbb{C}}=\phi_{\gamma\alpha}^{\mathbb{C}}$が成り立つ。特に$\phi_{\alpha\beta}^{\mathbb{C}}\circ\phi_{\beta\alpha}^{\mathbb{C}}=\mathrm{id}$であり、$\phi_{\alpha\beta}^{\mathbb{C}}$は複素解析的な同相写像であることが分かる。

さて、全ての$p\in M$と$O\cap U_{\alpha}\neq\empty$なる$\alpha$についての直和$\bigsqcup \phi_{\alpha}(O\cap U_{\alpha})^{\mathbb{C}}$を考える。座標変換$\phi_{\alpha\beta}^{\mathbb{C}}$で移り合う点同士を同一視したものを$M^{\mathbb{C}}$とすると、$M^{\mathbb{C}}$は$\overline{\phi_{\alpha}(O\cap U_{\alpha})^{\mathbb{C}}}$を局所座標とする複素多様体となる。これを$M$の複素化という。
