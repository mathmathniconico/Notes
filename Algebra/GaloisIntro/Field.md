
# 体とその拡大

## はじめに

本稿では、代数体のガロア理論を解説する。ガロア理論というと、決闘で死亡した逸話のある数学者エヴァリスト・ガロアの発想を基にした理論であり、体の代数拡大とその自己同型群に関する対応関係を記述する。現代ではそれに端を発して多種多様なガロア理論が研究されているが、本稿ではより内容を絞って代数体（厳密には有限次代数体）のクラスでガロア理論を解説する。

理由は2つあって、一つはガロア理論が純代数的であるために難解で、理論は追えても理解が進まない人（私）がいる。代数体を用いれば複雑な議論を大幅に省略することができるので、理解の助けになれば良いと思う。もう一つはガロア理論の先の展開を考えた時に、代数体は充分過ぎる程に豊かな構造を持つからである。代数体はそれ自体が高度な研究対象なのである。

前提知識としては、集合論の基本的な記号や用語、ベクトル空間の初歩（特に基底などに関する知識）、行列演算を含めた代数的操作くらいだろうか。



## 体の例

加減乗除の四則演算ができる集合を体と呼ぶ。具体例を挙げた方が分かり易いだろう。

**例** $\mathbb{Q}, \mathbb{R}, \mathbb{C}$は標準的な加減乗除で体となる。

**例** $\sqrt{2}\notin\mathbb{Q}$について

$$
\mathbb{Q}( \sqrt{2} ):=\lbrace a+b\sqrt{2} : a, b\in\mathbb{Q} \rbrace
$$

は体である。足し算と引き算、それに掛け算ができることは明らかである。残るは割り算だが、これはゼロ以外に逆元が存在することを示せば良い。$a, b\in\mathbb{Q}$について$a^{2}-2b^{2}\neq 0$に注意すると

$$
( a+b\sqrt{2} )\left(\frac{a-b\sqrt{2}}{a^{2}-2b^{2}}\right)=1
$$

が成り立ち、確かに$\mathbb{Q}( \sqrt{2} )$の元はゼロを除き可逆である。

**例** $\sqrt[3]{2}\notin\mathbb{Q}$について

$$
\mathbb{Q}( \sqrt[3]{2} )=\lbrace a+b\sqrt[3]{2}+c\sqrt[3]{4} : a, b, c\in\mathbb{Q} \rbrace
$$

は体である。これも同様に

$$
( a+b\sqrt[3]{2}+c\sqrt[3]{4} )( x+y\sqrt[3]{2}+z\sqrt[3]{4} )=1
$$

を$x, y, z$について解くことで逆元を計算することができる。上記は

$$
\left( \begin{matrix} a & 2c & 2b \\ b & a & 2c \\ c & b & a \end{matrix} \right)\left( \begin{matrix} x \\ y \\ z \end{matrix} \right)=\left( \begin{matrix} 1 \\ 0 \\ 0 \end{matrix} \right)
$$

と表せるので、

$$
f( a, b, c ):=\mathrm{det}\left( \begin{matrix} a & 2c & 2b \\ b & a & 2c \\ c & b & a \end{matrix} \right)=a^{3}+2b^{3}+4c^{3}-6abc
$$

が$a=b=c=0$以外のゼロ点を持たないことを示せば良い。

$f( a, b, c )=0$とする。このとき任意の$\lambda\in\mathbb{Q}$について$f( \lambda a, \lambda b, \lambda c )=0$だから、$a, b, c$は共通因子を持たない整数としてよい。すると$a^{3}$は偶数でなければならないから、$a$も偶数である。$a=2a^{\prime}$とすれば

$$8( a^{\prime} )^{3}+2b^{3}+4c^{3}-12a^{\prime}bc=0\Longleftrightarrow b^{3}+2c^{3}+4( a^{\prime} )^{3}-6bca^{\prime}=0$$

より、これを繰り返して$b=2b^{\prime}, c=2c^{\prime}$と表せることが分かる。$a, b, c$は共通因子を持たないので、$( a, b, c )=( 0, 0, 0 )$でなければならない。以上により$\mathbb{Q}( \sqrt[3]{2} )$の元はゼロを除き可逆である。

**例** $\omega:=-\frac{1}{2}+\frac{\sqrt{3}}{2}\sqrt{-1}\in\mathbb{C}$について

$$
\mathbb{Q}( \omega ):=\lbrace a+b\omega : a, b\in\mathbb{Q} \rbrace
$$

は体である。同じように$a, b\in\mathbb{Q}$について

$$
\mathrm{det}\left( \begin{matrix} a & -b \\ b & a-b \end{matrix}\right)=a^{2}+b^{2}-ab
$$

が$a=b=0$以外のゼロ点を持たないことを示せば良い。$a$について解くと判別式は$-3b^{2}$だから$b\neq 0$が実数の範囲を動くとき$a\notin\mathbb{R}$となる。$b=0$のとき$a=0$が従うので、$\mathbb{Q}( \omega )$の元はゼロを除き可逆である。

**例** $\omega, \sqrt[3]{2}$について

$$
\mathbb{Q}( \omega, \sqrt[3]{2} ):=\lbrace a+b\sqrt[3]{2}+c\sqrt[3]{4}+d\omega+e\omega\sqrt[3]{2}+f\omega\sqrt[3]{4} : a, b, c, d, e, f\in\mathbb{Q} \rbrace
$$

は体である。これは一見大変そうに見えるが、

$$
\mathbb{Q}( \omega, \sqrt[3]{2} )=\lbrace a+b\omega : a, b\in\mathbb{Q}( \sqrt[3]{2} ) \rbrace
$$

であることに注意すれば、$a^{2}+b^{2}-ab$が$a, b\in\mathbb{Q}( \sqrt[3]{2} )$の範囲でゼロ点を持たないことを示せばよい。しかし$a^{2}+b^{2}-ab$の非自明なゼロ点は実数でない。従って$\mathbb{Q}( \omega, \sqrt[3]{2} )$の元はゼロを除き可逆である。


## 体の拡大

2つの体$k, K$について、$k\subset K$かつ互いの演算が一致しているとき、**体の拡大**と呼び$K/k$で表す。このとき$K$を$k$の拡大体とか、$k$を$K$の基礎体などという。また$k\subset M\subset K$が体の拡大を定めているとき、$M$を拡大$K/k$の中間体と呼ぶ。

**例** $\mathbb{Q}( \sqrt{2} )/\mathbb{Q}$は体の拡大である。$\mathbb{Q}( \sqrt[3]{2} ), \mathbb{Q}( \omega )$は拡大$\mathbb{Q}( \sqrt[3]{2}, \omega )/\mathbb{Q}$の中間体である。

ガロア理論は体の拡大に関する理論だが、その起源は代数方程式の解法にある。代数方程式というのは

$$
a_{n}x^{n}+a_{n-1}x^{n-1}+\dotsb+a_{1}x+a_{0}=0
$$

の形をした方程式であり、既知の変数$a_{1}, \dotsc, a_{n}$に対して未知の変数$x$を求める問題が古くから考えられてきた。ここで「求める」というのは代数的に解くということである。すなわち上記の左辺を上手く変形し、別の変数で置き換えるなどして簡単な方程式に帰着させて解く。

**例**
カルダノの方法で$x^{3}+3px-q=0$を解いてみよう。体積$y$の立方体の内部に、端を揃えて体積$z$の立方体を描こう。重なりが無い部分は、小さな立方体と3つの直方体に分けることが出来る。小さな立方体の一辺を$x$、重なりが無い部分の体積を$q$、そして直方体の体積を$px$と置けば、$x^{3}=q-3px$を満たし、特に$x=\sqrt[3]{y}-\sqrt[3]{z}$が求まる。従ってこのような立方体の組、つまり

$$
\begin{aligned} y-z&=q, & yz&=p^{3} \end{aligned}
$$

を満たす$y, z$が分かれば良い。$(y+z)^{2}=q^{2}+4p^{3}$だから、$x^{3}+3px-q=0$の解を求める問題は、2次方程式

$$
t^{2}-\sqrt{q^{2}+4p^{3}}\cdot t+p^{3}=0
$$

を解くことに帰着される。

4次方程式も同様に解くことが出来たため、高次の代数方程式であっても次数を1つずつ下げていけば解を求めることができるだろう、という楽観が生まれたが、それが見事に打ち破られることになるのはご存知のことだと思う。

さて、例のように低次の代数方程式に帰着させると、その係数はより複雑なものとなる。$p, q$が住む世界（体）に、$q^{2}+4p^{3}$の二乗根を加え、更に$y, z$の三乗根を加える、という積み上げを考えることになる。式変形は係数の加減乗除で行われるので、この積み上げは体の枠組みで考えるのが自然である。これが体の拡大を考える理由である。



## 拡大次数の連鎖律

$K/k$を体の拡大とする。このとき$K$は$k$上のベクトル空間と見なすことができる。$k$上のベクトル空間としての次元を拡大$K/k$の**拡大次数**と呼び、$\lbrack K : k \rbrack$で表す。拡大次数が有限のものを**有限次拡大**と呼ぶ。

**例** $1, \sqrt{2}$は$\mathbb{Q}$上一次独立で

$$
\mathbb{Q}( \sqrt{2} )=\lbrace a+b\sqrt{2} : a, b\in\mathbb{Q} \rbrace
$$

なので$\lbrack \mathbb{Q}( \sqrt{2} ) : \mathbb{Q} \rbrack=2$である。

**例** $1, \sqrt[3]{2}, \sqrt[3]{4}$は$\mathbb{Q}$上一次独立で

$$
\mathbb{Q}( \sqrt[3]{2} )=\lbrace a+b\sqrt[3]{2}+c\sqrt[3]{4} : a, b, c\in\mathbb{Q} \rbrace
$$

なので$\lbrack \mathbb{Q}( \sqrt[3]{2} ) : \mathbb{Q} \rbrack=3$である。

**例** $1, \omega$は$\mathbb{Q}( \sqrt[3]{2} )$上一次独立で

$$
\mathbb{Q}( \sqrt[3]{2}, \omega )=\lbrace a+b\omega : a, b\in\mathbb{Q}( \sqrt[3]{2} ) \rbrace
$$

なので$\lbrack \mathbb{Q}( \sqrt[3]{2}, \omega ) : \mathbb{Q}( \sqrt[3]{2} ) \rbrack=2$である。

**例** $1, \sqrt[3]{2}, \sqrt[3]{4}, \omega, \omega\sqrt[3]{2}, \omega\sqrt[3]{4}$は$\mathbb{Q}$上一次独立で

$$
\mathbb{Q}( \sqrt[3]{2}, \omega )=\lbrace a+b\sqrt[3]{2}+c\sqrt[3]{4}+d\omega+e\omega\sqrt[3]{2}+f\omega\sqrt[3]{4} : a, b, c, d, e, f\in\mathbb{Q} \rbrace
$$

なので$\lbrack \mathbb{Q}( \sqrt[3]{2}, \omega ) : \mathbb{Q} \rbrack=6$である。



**例** $\mathbb{R}$の$\mathbb{Q}$上のベクトル空間としての基底はハメル基底などと呼ばれ、無限集合であることが知られている。つまり$\lbrack \mathbb{R} : \mathbb{Q} \rbrack=\infty$である。

このように体の拡大はベクトル空間の特殊な例であるが、ただ単に積の定まったベクトル空間というだけでなく、その積構造がベクトル空間の構造に反映される。その一つが次に示す拡大次数に対する連鎖律である。

**命題** $K/M/k$を拡大の列とする。拡大次数について

$$
\lbrack K : k \rbrack = \lbrack K : M \rbrack\cdot\lbrack M : k \rbrack
$$

が成り立つ。

（証明）$K/M$および$M/k$について、それぞれの基底を$\lbrace \alpha_{i} \rbrace, \lbrace \beta_{j} \rbrace$と置く。このとき$\lbrace \alpha_{i}\beta{j} \rbrace$が$K/k$の基底となる。実際、一次独立性のみ示してみよう。有限個の$c_{ij}\in k$について$\sum c_{ij}\alpha_{i}\beta_{j}=0$とする。$i$で括ると$\sum_{i}( \sum_{j}c_{ij}\beta_{j} )\alpha_{i}$となる。$\alpha_{i}$の係数は$M$の元だから、$\lbrace \alpha_{i} \rbrace$の一次独立性より$\sum_{j}c_{ij}\beta_{j}=0$が従う。更に$\lbrace \beta_{j} \rbrace$の一次独立性から$c_{ij}=0$が従う。$\square$

**例** 拡大の列$\mathbb{Q}( \sqrt[3]{2}, \omega )/\mathbb{Q}( \sqrt[3]{2} )/\mathbb{Q}$を考えると

$$
\lbrack \mathbb{Q}( \sqrt[3]{2}, \omega ) : \mathbb{Q} \rbrack=6=2\cdot 3=\lbrack \mathbb{Q}( \sqrt[3]{2}, \omega ) : \mathbb{Q}( \sqrt[3]{2} ) \rbrack\cdot\lbrack \mathbb{Q}( \sqrt[3]{2} ) : \mathbb{Q} \rbrack
$$

となる。
