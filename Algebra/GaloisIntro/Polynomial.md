
# 多項式

## 多項式の剰余

$k$を体、$a_{0}, \dotsc, a_{n}\in k$とする。不定元$x$を用いて

$$
a_{n}x^{n}+a_{n-1}x^{n-1}+\dotsb+a_{1}x+a_{0}
$$

と表せる式を$k$上の**多項式**と呼び、その全体を$k\lbrack x \rbrack$で表す。特に$a_{n}\neq 0$のとき$n$を多項式の**次数**と呼び、多項式$f$について$\mathrm{deg}( f )$などと表す。ゼロ多項式の次数については$\mathrm{deg}( 0 )=-\infty$と定めておこう。

多項式同士も足し算や引き算、掛け算ができることに注意する。（このような構造を数学では**環**と呼ぶが、詳しくは別の機会に譲る。）ただし整数全体$\mathbb{Z}$と同じように、多項式同士の割り算を多項式の範囲で行うことはできないが、剰余を考えることはできる。

**定理** 多項式$f, g\in k\lbrack x \rbrack$について$g\neq 0$とする。このとき$q, r\in k\lbrack x \rbrack$が存在して

$$
f=qg+r, \quad \mathrm{deg}( r )\lt\mathrm{deg}( g )
$$

と表すことができる。更に$q, r$は一意的に決まる。

（証明）多項式$f, g$は

$$
\begin{aligned} f&= a_{n}x^{n}+\dotsb+a_{1}x+a_{0}, & a_{n}&\neq 0 \\ g &= b_{m}x^{m}+\dotsb+b_{1}x+b_{0}, & b_{m}&\neq 0 \end{aligned}
$$

と表せる。$n\lt m$なら$q=0, r=f$と置けばよい。$n\ge m$とする。ここで

$$
h:=f-\frac{a_{n}}{b_{m}}x^{n-m}g
$$

を考えると$\mathrm{deg}( h )\lt\mathrm{deg}( f )$となるから、帰納的にある多項式$q\in k\lbrack x \rbrack$を用いて$r:=f-qg$が$\mathrm{deg}( r )\lt\mathrm{deg}( g )$を満たすようにできる。

一意性を示すために$f=qg+r=q^{\prime}g+r^{\prime}$とする。$( q-q^{\prime} )g=( r^{\prime}-r )$より$q\neq q^{\prime}$なら

$$
\mathrm{deg}( (q-q^{\prime} )g )\ge\mathrm{deg}( g )\gt\mathrm{deg}( r^{\prime}-r )
$$

より矛盾する。よって$q=q^{\prime}$であり$r^{\prime}=r$である。$\square$

**例** $f=x^{2}+x+1, g=x+1$について$f=xg+1$より$q=x, r=1$である。

多項式の妙は**代入**という操作にあるが、これをきちんと述べるには少し準備が必要となる。なのでここで詳しくは述べないこととして、単に$x$を代入したい数で置き換える操作としておく。具体的には体の拡大$K/k$について、$k$上の多項式

$$
f=a_{n}x^{n}+\dotsb+a_{1}x+a_{0}\in k\lbrack x \rbrack
$$

に$\alpha\in K$を代入したものを

$$
f( \alpha ):=a_{n}\alpha^{n}+\dotsb+a_{1}\alpha+a_{0}\in K
$$

と表す。

定理の系として、因数定理と根の個数に関する不等式が得られる。

**系** $K/k$を体の拡大とする。$f\in k\lbrack x \rbrack, \alpha\in K$とする。以下は同値である。

- $f( \alpha )=0$である。
- $f$は$K\lbrack x \rbrack$の多項式として$x-\alpha$で割り切れる。つまり$q\in K\lbrack x \rbrack$を用いて$f=q( x-\alpha )$と表せる。

（証明）$x-\alpha$による余りを考えればよい。$\square$

$f( \alpha )=0$となる$\alpha\in K$を多項式$f$の$K$における**根**と呼ぶ。

**系** $K/k$を体の拡大とする。ゼロでない多項式$f\in k\lbrack x \rbrack, \neq 0$に対し、$f$の$K$における根は高々$\mathrm{deg}( f )$個である。

（証明）$f$に根$\alpha$があれば$x-\alpha$で割り切れるので次数を考えれば帰納的に示せる。$\square$

常に$\mathrm{deg}( f )$個あるわけではないことに注意しよう。

**例** $\mathbb{Q}( \sqrt{2} )/\mathbb{Q}$において、$f=x^{3}-2\in\mathbb{Q}\lbrack x \rbrack$の根は存在しない。$\mathbb{Q}( \sqrt{2} )$の元は$a, b\in\mathbb{Q}$として$a+b\sqrt{2}$と表せるので、

$$
f( a+b\sqrt{2} )=( a+b\sqrt{2} )^{3}-2=a^{3}+6ab^{2}-2+( 3a^{2}b+2b^{3} )\sqrt{2}
$$

となるが、これはゼロにならない。



## 剰余体と分解体

多項式$f\in k\lbrack x \rbrack, \neq 0$は最高次の係数が$1$のとき**モニック**であるという。また一次以上の多項式$g, h\in k\lbrack x \rbrack$を用いて$f=gh$と表せないとき、$f$は$k\lbrack x \rbrack$において**既約**であるという。

多項式は次数を持つので、任意の多項式は有限個の既約多項式の積で表せることに注意する。

**命題** 多項式の既約多項式による剰余全体は体となる。

（証明）$p\in k\lbrack x \rbrack$を既約多項式とする。$f\in k\lbrack x \rbrack, \neq 0$は$\mathrm{deg}( f )\lt\mathrm{deg}( p )$を満たすとする。このとき$p$の$f$による剰余を考えると$p=qf+r$と表せるが、$p$は既約だから$r\neq 0$である。$r\in k$なら$f$は可逆となるから、帰納的に$r$は可逆としてよい。つまり$s, t\in k\lbrack x \rbrack$が存在して$sr=tp+1$と表せる。

$$
sp=sqf+sr=sqf+tp+1 \Longleftrightarrow ( s-t )p=sqf+1
$$

だから$f$も可逆となる。$\square$

上記の体、つまり既約多項式$p\in k\lbrack x \rbrack$による剰余全体を$k\lbrack x \rbrack/( p )$と書き、$p$による**剰余体**と呼ぶ。特に$k\lbrack x \rbrack/( p )$は$k$の拡大体である。

**補題** $f\in k\lbrack x \rbrack$を$\mathrm{deg}( f )=n\gt 0$なる多項式とする。このときある体の拡大$K/k$が存在して、$f$は$K\lbrack x \rbrack$において$n$個の一次多項式の積として表せる。

（証明）$n$に関する帰納法で示す。$n=1$のとき、$f=ax+b$だから、$x=-\frac{b}{a}\in k$が解である。故に$K=k$とすればよい。$n\gt 0$のとき$f=gp$と既約多項式$p\in k\lbrack x \rbrack$と分解できる。体$E=k\lbrack x \rbrack/( p )$を考えれば$E/k$は体の拡大であって、剰余としての$x\in E$は多項式$p$の根である。これを改めて$\xi$と書き、不定元を$y$とすれば$p$は$E\lbrack y \rbrack$において$( y-\xi )$を因子に持つ。特に$f=( y-\xi )g$と分解できるので、帰納的に$1$次多項式の積で表せる体の拡大$K/k$が存在する。$\square$

多項式について、その根を全て含む体を**分解体**と呼ぶ。先の補題は、任意の多項式が分解体を持つことを述べている。




## 有限次拡大と最小多項式

多項式と関連して有限次拡大の性質を見ていく。

**命題** $K/k$は有限次拡大とする。このとき任意の$\alpha\in K$は、ある$k$上の多項式$f\in k\lbrack x \rbrack$の根である。

（証明）拡大次数を$n$とすると、

$$
1, \alpha, \alpha^{2}, \dotsc, \alpha^{n}
$$

は$k$上一次従属である。従って、ある$a_{0}, \dotsc, a_{n}\in k$が存在して

$$
a_{0}\cdot 1+a_{1}\alpha+\dotsb+a_{n}\alpha^{n}=0
$$

となる。$f=a_{0}+a_{1}x+\dotsb+a_{n}x^{n}\in k\lbrack x \rbrack$と置けば$f( \alpha )=0$より$\alpha$は$f$の根である。$\square$

$\alpha$を根とする多項式のうち、次数が最小でモニックなものを$\alpha$の$k$上の**最小多項式**と呼ぶ。

**命題** 最小多項式は既約である。

（証明）有限次拡大$K/k$において、$\alpha\in K$の最小多項式を$f\in k\lbrack x \rbrack$とする。もし一次以上の多項式$g, h\in k\lbrack x \rbrack$に対し$f=gh$と書けるなら、

$$
0=f( \alpha )=g( \alpha )h( \alpha )
$$

より、$g( \alpha )=0$または$h( \alpha )=0$となる。これは次数の最小性に矛盾する。$\square$

**命題** $K/k$を有限次拡大とする。$\alpha\in K$の$k\lbrack x \rbrack$における最小多項式を$f$とする。多項式$g\in k\lbrack x \rbrack$について$g( \alpha )=0$のとき$f$は$g$を割り切る。

（証明）定理より$g=qf+r$となる$q, r\in k\lbrack x \rbrack$が存在するが、$\alpha$を代入すると$r( \alpha )=0$を得る。$\mathrm{deg}( r )\lt\mathrm{deg}( f )$より、$r=0$でなければならない。$\square$

上記の2つの命題より最小多項式の判定法が得られる。すなわち、既約かつモニックな多項式の根は、その根の最小多項式である。つまり最小多項式は自分自身の根の最小多項式になっている。

**例** $\mathbb{Q}( \sqrt{2} )/\mathbb{Q}$において$x^{2}-2$は$\sqrt{2}$の最小多項式である。実際$( \sqrt{2} )^{2}-2=0$であり、$\sqrt{2}\notin\mathbb{Q}$より既約である。

**例** $\mathbb{Q}( \sqrt[3]{2} )/\mathbb{Q}$において$x^{3}-2$は$\sqrt[3]{2}$の最小多項式である。これも$\sqrt[3]{2}\notin\mathbb{Q}$より既約性が分かる。

拡大$K/k$において、体$k$を含み、$S\subset K$を含む最小の体を$k( S )$などと表す。特に$S=\lbrace \alpha \rbrace$が唯一つの元であるとき$k( \alpha )$と書き$k( \alpha )/k$は**単拡大**と呼ぶ。

有限次単拡大は、ベクトル空間としての基底が生成元の冪で取れるという性質を持つ。

**命題** $K/k$は有限次拡大とする。$\alpha\in K$について最小多項式の次数を$n$とすると

$$
k( \alpha )=k\lbrack \alpha \rbrack=\lbrace a_{0}+a_{1}\alpha+\dotsb+a_{n-1}\alpha^{n-1} : a_{0}, \dotsc, a_{n-1}\in k \rbrace
$$

が成り立ち

$$
1, \alpha, \alpha^{2}, \dotsc, \alpha^{n-1}
$$

はベクトル空間$k( \alpha )$の$k$上の基底となる。従って$n$は$k( \alpha )/k$の拡大次数と一致する。

（証明）$\alpha$の最小多項式を$p$とする。すると$p( \alpha )=0$より$\alpha^{n}$は$1, \alpha, \dotsc, \alpha^{n-1}$の線形結合で書ける。よって

$$
k\lbrack \alpha \rbrack=\lbrace a_{0}+a_{1}\alpha+\dotsb+a_{n-1}\alpha^{n-1} : a_{0}, \dotsc, a_{n-1}\in k \rbrace
$$

と表せる。$k\lbrack \alpha \rbrack\subset k( \alpha )$は自明であり、逆も$k\lbrack \alpha \rbrack\cong k\lbrack x \rbrack/( p )$が剰余体（$\cong$については後述するが、$\alpha$を不定元とする多項式と思えば同じとみなせるということ）であることから$k( \alpha )$の最小性より従う。一次独立性は$p$の最小性より従う。$\square$