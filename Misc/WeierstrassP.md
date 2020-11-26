
# Weierstrassの$\wp$函数について

以下$\omega_{1}, \omega_{2}\in\mathbb{C}$は$\mathrm{Im}(\omega_{1}/\omega_{2})\gt 0$とする。


## 楕円函数

__定義__ $\mathbb{C}$上有理型な函数$f$が **楕円函数** （Elliptic Function）とは、二つの周期

$$
\begin{aligned}
f(z+2\omega_{1}) &=f(z), \\
f(z+2\omega_{2}) &=f(z)
\end{aligned}
$$

を持つことをいう。$\omega_{1}, \omega_{2}$を半周期といい、$m, n\in\mathbb{Z}$について$\Omega_{m,n}=2m\omega_{1}+2n\omega_{2}$と表す。その全体を$\Omega$と置く。

- 定数は楕円函数である。

楕円函数$f$が与えられたとき、点$t, t+2\omega_{1}, t+2\omega_{1}+2\omega_{2}, t+2\omega_{2}$で与えられる平行四辺形の領域を$\Delta$とする。このとき$\Delta$の境界$C$上には$f$の零点や極が無いものとする。

__命題__ 定数でない楕円函数$f$について以下が成り立つ。

- $\Delta$内部における$f$の極は有限個である。
- $\Delta$内部における$f$の零点は有限個である。
- $\Delta$内部における留数の和はゼロである。
- $f$は$\Delta$上で正則でない。

（証明）$\overline{\Delta}$は有界閉なので、もし$f$の極が$\Delta$内部に無限個存在すれば集積点を持つ。これは$f$が有理型であることに反する。零点の場合も$f$の零点は$1/f$の極であり、$1/f$が楕円函数であることから従う。

留数定理より

$$
\begin{aligned}
\sum_{a\in\Delta}\mathrm{Res}_{z=a}f(z) &=\frac{1}{2\pi\sqrt{-1}}\oint_{C}f(\zeta)\mathrm{d}\zeta \\
&=\left( \int_{t}^{t+2\omega_{1}}+\int_{t+2\omega_{1}}^{t+2\omega_{1}+2\omega_{2}}+\int_{t+2\omega_{1}+2\omega_{2}}^{t+2\omega_{2}}+\int_{t+2\omega_{2}}^{t}  \right)f(\zeta)\mathrm{d}\zeta
\end{aligned}
$$

となるが、周期性より積分の1番目と3番目、2番目と4番目が打ち消しあうのでゼロとなる。

$f$が$\Delta$上で正則なら$\overline{\Delta}$上で連続なので有界である。周期性より$\mathbb{C}$上で有界なのでLiouvilleの定理より$f$は定数となる。$\square$

__注意__ $f$を定数でない楕円函数とする。任意の$c\in\mathbb{C}$に対して、$f-c$もまた楕円函数である。ここで必要なら$\Delta$を少しずらすことで$\Delta$内部に$f-c$の零点が全て含まれるようにできる。このとき同様に有限個であることが分かるため、この意味で$f$の$c$点もまた$\Delta$内部で有限個である。

__命題__ $f$を定数でない楕円函数とする。$\Delta$内部における極と零点の重複込みの個数は一致し、一般に$c$点の重複込みの個数も一致する。更に$\Delta$内部における零点を重複込みで$a_{1}, \dotsc, a_{n}$とし、極を重複込みで$b_{1}, \dotsc, b_{n}$とすると、

$$
\sum_{i=1}^{n}a_{i}\equiv\sum_{i=1}^{n}b_{i} \mod{\Omega}
$$

が成り立つ。

（証明）偏角の原理を思い出す。$f$が$a$で$k$位なら$f(z)=(z-a)^{k}g(z)$と表せる。（$g$は$a$で正則で$g(a)\neq 0$を満たす。）このとき

$$
\frac{f^{\prime}(z)}{f(z)}=\frac{k}{z-a}+\frac{g^{\prime}(z)}{g(z)}
$$

となるが、$g^{\prime}(z)/g(z)$は$a$で正則なので$C_{a}$を$a$まわりの円周として

$$
k=\frac{1}{2\pi\sqrt{-1}}\oint_{C_{a}}\frac{f^{\prime}(z)}{f(z)}\mathrm{d}z
$$

となる。従って零点が$N$個、極が$M$個なら

$$
N-M=\frac{1}{2\pi\sqrt{-1}}\oint_{C}\frac{f^{\prime}(z)}{f(z)}\mathrm{d}z=0
$$

となり一致する。（$f^{\prime}/f$は楕円函数であり、最後の等式はその周期性より従う。）

同様に

$$
z\frac{f^{\prime}(z)}{f(z)}=(a+(z-a))\frac{f^{\prime}(z)}{f(z)}=\frac{ak}{z-a}+\mathrm{hol.}
$$

だから

$$
\begin{aligned}
\sum_{i=1}^{n}a_{i}-\sum_{i=1}^{n}b_{i} &=\frac{1}{2\pi\sqrt{-1}}\oint_{C}z\frac{f^{\prime}(z)}{f(z)}\mathrm{d}z \\
&=\frac{1}{2\pi\sqrt{-1}}\left\lbrace \int_{t}^{t+2\omega_{1}}+\int_{t+2\omega_{1}}^{t+2\omega_{1}+2\omega_{2}}+\int_{t+2\omega_{1}+2\omega_{2}}^{t+2\omega_{2}}+\int_{t+2\omega_{2}}^{t} \right\rbrace z\frac{f^{\prime}(z)}{f(z)}\mathrm{d}z \\
&=\frac{1}{2\pi\sqrt{-1}}\left\lbrace 2\omega_{1}\int_{t}^{t+2\omega_{2}}-2\omega_{2}\int_{t}^{t+2\omega_{1}} \right\rbrace\frac{f^{\prime}(z)}{f(z)}\mathrm{d}z
\end{aligned}
$$

となる。ここで$z$が線分$\lbrack t, t+2\omega_{i} \rbrack$上を動くとき、周期性より$f(z)$は原点周りを何週かして$f(t)$に戻ってくる。$f^{\prime}/f$の積分は$\mathrm{log}f$なので、その回数分$2\pi\sqrt{-1}$が現れる。結局

$$
\sum_{i=1}^{n}a_{i}-\sum_{i=1}^{n}b_{i}=2m\omega_{1}+2n\omega_{2}=\Omega_{m,n}\in\Omega
$$

となる。$\square$

__定義__ 楕円函数$f$について、$\Delta$内の極の重複込みの個数を$f$の位数と呼ぶ。

位数ゼロの楕円函数は定数である。また留数の和がゼロという性質から、定数でない楕円函数の位数は$2$以上となる。位数$2$の楕円函数を考えると、次のパターンがある。

- $1$箇所に$2$位の極を持ち、留数はゼロである。$\rightarrow \wp(z)$
- $2$箇所に$1$位の極を持ち、留数は互いに逆である。$\rightarrow \mathrm{sn}(z)$


## Weierstrassの$\wp$函数

函数$\wp(z)$を以下で定める。

$$
\wp(z):=\frac{1}{z^{2}}+\sum_{\omega\in\Omega}^{\prime}\left( \frac{1}{(z-\omega)^{2}}-\frac{1}{\omega^{2}} \right)
$$

ただし$\sum^{\prime}$はゼロを除く和とする。これは収束していて$\mathbb{C}$上有理型となる。$\Delta$内部の極は$z\equiv 0$のみで、位数は$2$、留数はゼロである。

__定義__ $\wp(z)$を **Wierstrassの$\wp$（ペー）函数** という。

$\omega_{1}=\pi/2, \omega_{2}\rightarrow\infty$とすると$\omega=2m\omega_{1}+2n\omega_{2}$に対して$n=0$の項だけが残り

$$
\frac{1}{z^{2}}+\sum_{m}^{\prime}\left( \frac{1}{(z-\pi m)^{2}}-\frac{1}{(\pi z)^{2}} \right)=\sum_{m=-\infty}^{\infty}\frac{1}{(z-\pi m)^{2}}-\frac{2}{\pi^{2}}\sum_{m=1}^{\infty}\frac{1}{m^{2}}=\frac{1}{\mathrm{sin}^{2}z}-\frac{1}{3}
$$

だから$\wp$函数は概ね$\mathrm{cosec}^{2}(z)$のようなものである。

$\wp$函数の微分は、項別微分して

$$
\wp^{\prime}(z)=-2\sum_{\omega}\frac{1}{(z-\omega)^{3}}
$$

と分かる。

__命題__ $\wp$函数に対して以下が成り立つ。

- $\wp^{\prime}(z)$は奇函数、$\wp(z)$は偶函数である。
- $\wp^{\prime}(z), \wp(z)$は共に楕円函数である。

（証明）$\wp^{\prime}(z)$について

$$
\wp^{\prime}(-z)=-2\sum\frac{1}{(-z-\omega)^{3}}=2\sum\frac{1}{(z-(-\omega))^{3}}=-\wp^{\prime}(z)
$$

より$\wp^{\prime}(z)$は奇函数である。同様に$\wp(z)$は偶関数である。

まず$wp^{\prime}(z)$について

$$
\wp^{\prime}(z+2\omega_{1})=-2\sum\frac{1}{(z+2\omega_{1}-\Omega_{m,n})^{3}}=-2\sum\frac{1}{(z-\Omega_{m-1,n})^{3}}=\wp^{\prime}(z)
$$

より楕円函数である。従って積分すると

$$
\wp(z+2\omega_{1})=\wp(z)+\mathrm{const.}
$$

となるが、$z=-\omega_{1}$と置けば偶関数より定数部分はゼロとなる。故に$\wp(z)$も楕円函数である。$\square$

__命題__ $\wp(z)$は

$$
\left( \frac{\mathrm{d}y}{\mathrm{d}z} \right)^{2}=4y^{3}-g_{2}y-g_{3}
$$

の解である。ただし

$$
\begin{aligned}
g_{2}&=60\sum^{\prime}\frac{1}{\omega^{4}}, & g_{3}&=140\sum^{\prime}\frac{1}{\omega^{6}}
\end{aligned}
$$

とする。

（証明）$\phi(z)=\wp(z)-1/z^{2}$は原点で正則な偶関数であるから$\phi(z)=a_{0}+a_{2}z^{2}+a_{4}z^{4}+\dotsb$と表せる。すると

$$
a_{0}=\phi(0)=\sum^{\prime}\left( \frac{1}{(-\omega)^{2}}-\frac{1}{\omega^{2}} \right)=0
$$

より$\wp(z)=z^{-2}+a_{2}z^{2}+a_{4}z^{4}+\dotsb$となる。頑張って計算すると

$$
\wp^{\prime}(z)^{2}-4\wp(z)^{3}+20a_{2}\wp(z)=-28a_{4}+\mathrm{higher.}
$$

となる。左辺は楕円函数なので右辺も楕円函数だから定数となる。あとは係数を計算すると

$$
\begin{aligned}
a_{2}=\frac{\phi^{(2)}(0)}{2!}&=3\sum^{\prime}\frac{1}{\omega^{4}}, & a_{4} &=5\sum^{\prime}\frac{1}{\omega^{6}}, & \dotsc &
\end{aligned}
$$

より目的の微分方程式を満たすことが分かる。$\square$

ちなみに

$$
\begin{aligned}
a_{2}&=\frac{g_{2}}{20}, & a_{4}&=\frac{g_{3}}{28}, & a_{6}&=\frac{g_{2}^{2}}{1200}, & a_{8}&=\frac{3g_{2}g_{3}}{6160}, & a_{10}&=\frac{g_{2}^{3}}{156000}+\frac{g_{3}^{2}}{10192}, & a_{12}&=\frac{g_{2}^{2}g_{3}}{184800}, & \dotsc &
\end{aligned}
$$

と順次$g_{2}, g_{3}$によって求めていくことができる。具体的には$\wp$函数は$g_{2}$と$g_{3}$によって決まる。

__注意__ 逆に$y=\wp(u(z))$が解なら$(\wp^{\prime})^{2}\dot{u}^{2}=4\wp^{3}-g_{2}\wp-g_{3}=(\wp^{\prime})^{2}$より$\dot{u}^{2}=1$だから$u=\pm z+\alpha$となる。よって$y=\wp(\pm z+\alpha)=\wp(z\pm\alpha)$を得る。従って一般解は$\wp(z+\alpha)$である。

__注意__ $(\wp^{\prime})^{2}=4\wp^{3}-g_{2}\wp-g_{3}$を更に微分すると$2\wp^{\prime}\wp^{(2)}=12\wp^{2}\wp^{\prime}-g_{2}\wp^{\prime}$だから

$$
\begin{aligned}
\wp^{(2)}&=6\wp^{2}-\frac{g_{2}}{2}, & \wp^{(3)}&=12\wp\wp^{\prime} 
\end{aligned}
$$

を得る。特に$\wp$はパンルヴェＩ（$y^{(2)}=6y^{2}+t$）の$t\rightarrow -g_{2}/2$における自励極限であることが分かる。


## $\wp$函数の加法定理

$\wp^{\prime}(z)$は$z\equiv 0$に$3$位の極を持つから、同じ数の零点が$\Delta$内部に存在する。まず奇函数だから$\wp^{\prime}(z+2\omega_{1})=\wp^{\prime}(z)$に$z=-\omega_{1}$を代入して$\wp^{\prime}(\omega_{1})=0$を得る。同様に$\wp^{\prime}(\omega_{2})=\wp^{\prime}(\omega_{1}+\omega_{2})=0$である。つまり$\omega_{1}, \omega_{2}, \omega_{1}+\omega_{2}$が$\wp^{\prime}(z)$の零点を与える。以下この点での$\wp(z)$の値を

$$
\begin{aligned}
e_{1}&=\wp(\omega_{1}), & e_{2}&=\wp(\omega_{2}), & e_{3}&=\wp(\omega_{1}+\omega_{2})
\end{aligned}
$$

とする。

__命題__ 以下が成り立つ。

- $e_{1}, e_{2}, e_{3}$は互いに異なる。
- $4y^{3}-g_{2}y-g_{3}=4(y-e_{1})(y-e_{2})(y-e_{3})$が成り立つ。

（証明）互いに異なることは$f(z):=\wp(z)-e_{r}$を考えればよい。実際$f^{\prime}(z)=\wp^{\prime}(z)$より$f(\omega_{r})=f^{\prime}(\omega_{r})=0$だから、$\omega_{r}$は$f$の少なくとも$2$位の零点となる。しかし$f$の位数は$2$だからこれ以上の零点はなく、即ち$e_{1}$は$e_{2}, e_{3}$と異なることが分かる。他も同様である。

$\wp^{\prime}(z)^{2}=4\wp(z)^{3}-g_{2}\wp(z)-g_{3}$に$z=\omega_{1}, \omega_{2}, \omega_{1}+\omega_{2}$を代入すると$4e_{r}^{3}-g_{2}e_{r}-g_{3}=0$を得る。これらが互いに異なる所与の多項式の根であることが分かるので、最高次係数を合わせると命題の式が成り立つ。$\square$

更に解と係数の関係より

$$
\begin{aligned}
e_{1}+e_{2}+e_{3}&=0, & e_{1}e_{2}+e_{2}e_{3}+e_{3}e_{1}&=-\frac{g_{2}}{4}, & e_{1}e_{2}e_{3}&=\frac{g_{3}}{4}
\end{aligned}
$$

を得る。また$(e_{1}+e_{2}+e_{3})^{2}, (e_{1}+e_{2}+e_{3})^{3}, (e_{1}-e_{2})(e_{2}-e_{3})(e_{3}-e_{1})$等を計算すると

$$
\begin{aligned}
g_{2}&=2(e_{1}^{2}+e_{2}^{2}+e_{3}^{2}), & g_{3}&=\frac{4}{3}(e_{1}^{3}+e_{2}^{3}+e_{3}^{3}), & g_{2}^{3}-27g_{3}^{2}&=16(e_{1}-e_{2})^{2}(e_{2}-e_{3})^{2}(e_{3}-e_{1})^{2}
\end{aligned}
$$

を得る。

__定理__ $u+v+w\equiv 0$に対し

$$
\left\vert \begin{matrix}
\wp(u) & \wp^{\prime}(u) & 1 \\
\wp(v) & \wp^{\prime}(v) & 1 \\
\wp(w) & \wp^{\prime}(w) & 1
\end{matrix} \right\vert = 0
$$

が成り立つ。

（証明）$\wp(u), \wp(v), \wp(w)$は互いに異なるとしてよい。連立方程式

$$
\begin{aligned}
a\wp(u)+b &= \wp^{\prime}(u), \\
a\wp(v)+b &= \wp^{\prime}(v)
\end{aligned}
$$

の根$a, b$を取り、$f(z):=a\wp(z)+b-\wp^{\prime}(z)$とする。$f$は原点に$3$位の極を持つ位数$3$の楕円函数である。よって$u, v$それと$w^{\prime}$という零点が存在する。楕円函数の性質より零点と極の和は$\mod\Omega$で一致する。よって$u+v+w^{\prime}\equiv 0+0+0$だから$w\equiv w^{\prime}$となる。つまり$w$もまた$f$の零点である。$a, b$を消去すれば定理の式を得る。$\square$

__系__ （加法定理、倍各公式）一般の$u, v$に対して

$$
\wp(u+v)=\frac{1}{4}\left\lbrace \frac{\wp^{\prime}(u)-\wp^{\prime}(v)}{\wp(u)-\wp(v)} \right\rbrace^{2}-\wp(u)-\wp(v)
$$

が成り立つ。特に$v\rightarrow u$とすれば

$$
\wp(2u)=\frac{1}{4}\left\lbrace \frac{\wp^{(2)}(u)}{\wp^{\prime}(u)} \right\rbrace^{2}-2\wp(u)
$$

が成り立つ。

（証明）$u+v+w\equiv 0$とする。定理の証明の$a, b$について

$$
\begin{aligned}
g(z)&=(a\wp(z)+b)^{2}-\wp^{\prime}(z)^{2} \\
&=-4\wp(z)^{3}+a^{2}\wp(z)^{2}+(2ab+g_{2})\wp(z)+b^{2}+g_{3}
\end{aligned}
$$

とおくと、$g(u)=g(v)=g(w)=0$より$\wp(u), \wp(v), \wp(w)$は

$$
-4t^{3}+a^{2}t^{2}+(2ab+g_{2})t+b^{2}g_{3}=0
$$

の解である。解と係数の関係より

$$
\wp(u)+\wp(v)+\wp(w)=\frac{a^{2}}{4}=\frac{1}{4}\left\lbrace \frac{\wp^{\prime}(u)-\wp^{\prime}(v)}{\wp(u)-\wp(v)} \right\rbrace^{2}
$$

だが、$\wp(w)=\wp(-u-v)=\wp(u+v)$より求める式を得る。$\square$


## 逆関数$\wp^{-1}$について

__定義__ 函数$w(z)$に対し、

$$
\lbrace w; z \rbrace := \left\lbrace \frac{w^{(2)}}{w^{\prime}} \right\rbrace^{\prime}-\frac{1}{2}\left\lbrace \frac{w^{(2)}}{w^{\prime}} \right\rbrace^{2}=\frac{w^{(3)}}{w^{\prime}}-\frac{3}{2}\left( \frac{w^{(2)}}{w^{\prime}} \right)^{2}
$$

を **Schwarz微分** という。

> 次の命題は計算すれば示せる。

__命題__ 以下が成り立つ。

- $ad-bc\neq 0$なら$\lbrace w; z \rbrace=\lbrace (aw+b)/(cw+d); z \rbrace$が成り立つ。
- $\lbrace w; z \rbrace=0$は、$w=(az+b)/(cw+d)$と表せることと同値である。
- $\lbrace w; z \rbrace+(w^{\prime})^{2}\lbrace z; w \rbrace=0$が成り立つ。

__補題__ 二階の微分方程式

$$
\frac{\mathrm{d}^{2}v}{\mathrm{d}z^{2}}+\frac{1}{2}Q(z)v=0
$$

の解を$a, b$とする。$w=b/a$とすると$\lbrace w; z \rbrace=Q(z)$が成り立つ。

（証明）$aw=b$を逐次微分すると

$$
\begin{aligned}
aw &= b, \\
a^{\prime}w+aw^{\prime} &= b^{\prime}, \\
a^{(2)}w+2a^{\prime}w^{\prime}+aw^{(2)} &= b^{(2)}, \\
a^{(3)}w+3a^{(2)}w^{\prime}+3a^{\prime}w^{(2)}+aw^{(3)} &= b^{(3)}
\end{aligned}
$$

となる。よって

$$
\begin{aligned}
\frac{w^{(3)}}{w^{(2)}}=\frac{aw^{(3)}}{aw^{(2)}} &= \frac{b^{(3)}}{aw^{(2)}}-3\frac{a^{\prime}}{a}-3\frac{a^{(2)}}{a}\frac{w^{\prime}}{w^{(2)}}-\frac{a^{(3)}}{a}\frac{w}{w^{(2)}}, \\
\frac{w^{(2)}}{w^{\prime}}=\frac{aw^{(2)}}{aw^{\prime}} &= \frac{b^{(2)}}{aw^{\prime}}-2\frac{a^{\prime}}{a}-\frac{a^{(2)}}{a}\frac{w}{w^{\prime}}
\end{aligned}
$$

となるから、

$$
\begin{aligned}
\frac{w^{(3)}}{w^{(2)}}-\frac{3}{2}\frac{w^{(2)}}{w^{\prime}}=\frac{b^{(3)}}{aw^{(2)}}-\frac{3}{2}\frac{b^{(2)}}{aw^{\prime}}-3\frac{a^{(2)}}{a}\frac{w^{\prime}}{w^{(2)}}+\frac{3}{2}\frac{a^{(2)}}{a}\frac{w}{w^{\prime}}-\frac{a^{(3)}}{a}\frac{w}{w^{(2)}}
\end{aligned}
$$

を得る。故に

$$
\begin{aligned}
\frac{w^{(3)}}{w^{\prime}}-\frac{3}{2}\left( \frac{w^{(2)}}{w^{\prime}} \right)^{2} &= \frac{w^{(2)}}{w^{\prime}}\left( \frac{w^{(3)}}{w^{(2)}}-\frac{3}{2}\frac{w^{(2)}}{w^{\prime}} \right) \\
&= \frac{b^{(3)}}{aw^{\prime}}-\frac{3}{2}\frac{b^{(2)}w^{(2)}}{a(w^{\prime})^{2}}-3\frac{a^{(2)}}{a}+\frac{3}{2}\frac{a^{(2)}}{a}\frac{ww^{(2)}}{(w^{\prime})^{2}}-\frac{a^{(3)}}{a}\frac{w}{w^{\prime}}　\\
&=\frac{1}{aw^{\prime}}(b^{(3)}-a^{(3)}w)-\frac{3w^{(2)}}{2a(w^{\prime})^{2}}(b^{(2)}-a^{(2)}w)-3\frac{a^{(2)}}{a}
\end{aligned}
$$

だが、$a, b$は微分方程式の解なので

$$
\begin{aligned}
\frac{a^{(2)}}{a} &= -\frac{1}{2}Q, \\
b^{(2)}-a^{(2)}w &= -\frac{1}{2}Q(b-aw)=0, \\
b^{(3)}-a^{(3)}w &= -\frac{1}{2}Q^{\prime}(b-aw)-\frac{1}{2}Q(b^{\prime}-aw^{\prime})=-\frac{1}{2}Qaw^{\prime}
\end{aligned}
$$

が成り立つ。これを代入すると

$$
\lbrace w; z \rbrace=\frac{w^{(3)}}{w^{\prime}}-\frac{3}{2}\left( \frac{w^{(2)}}{w^{\prime}} \right)^{2} = Q
$$

を得る。$\square$

今$y=\wp(z)$は

$$
(y^{\prime})^{2}=4(y-e_{1})(y-e_{2})(y-e_{3})
$$

を満たしていた。微分して上の式で両辺をそれぞれ割ると

$$
2\frac{y^{(2)}}{y^{\prime}}=\sum_{r=1}^{3}\frac{y^{\prime}}{y-e_{r}}
$$

となる。更に$2y^{\prime}$で割り、もう一度微分すると

$$
\frac{y^{(3)}(y^{\prime})^{2}-2(y^{(2)})^{2}y^{\prime}}{(y^{\prime})^{4}}=-\frac{1}{2}\sum_{r=1}^{3}\frac{y^{\prime}}{(y-e_{r})^{2}}
$$

より

$$
\frac{y^{(3)}}{(y^{\prime})^{3}}-\frac{2(y^{(2)})^{2}}{(y^{\prime})^{4}}=-\frac{1}{2}\sum_{r=1}^{3}\frac{1}{(y-e_{r})^{2}}
$$

を得る。

__定理__ $\mathbb{P}^{1}$上多価な函数$z=\wp^{-1}(y)$は、$2$階の微分方程式

$$
\frac{\mathrm{d}^{2}v}{\mathrm{d}y}+\left\lbrack \frac{1}{4}\sum_{r=1}^{3}\frac{1}{(y-e_{r})^{2}}-\frac{1}{16}\left( \sum_{r=1}^{3}\frac{1}{y-e_{r}} \right)^{2} \right\rbrack v=0
$$

の解$v_{1}, v_{2}$の比$v_{2}/v_{1}$と等しい。

（証明）補題より$\lbrace z; y \rbrace$を計算すればよい。

$$
\begin{aligned}
\lbrace z; y \rbrace &=-\frac{1}{(y^{\prime})^{2}}\lbrace y; z \rbrace=-\frac{y^{(3)}}{(y^{\prime})^{3}}+\frac{3}{2}\frac{(y^{(2)})^{2}}{(y^{\prime})^{4}} \\
&=-\frac{1}{2}\frac{(y^{(2)})^{2}}{(y^{\prime})^{4}}+\frac{1}{2}\sum_{r=1}^{3}\frac{1}{(y-e_{r})^{2}} \\
&=\frac{1}{2}\sum_{r=1}^{3}\frac{1}{(y-e_{r})^{2}}-\frac{1}{8}\left( \sum_{r=1}^{3}\frac{1}{y-e_{r}} \right)^{2}
\end{aligned}
$$

より示される。$\square$

この微分方程式は$e_{1}, e_{2}, e_{3}$に第一種特異点を持ち、従って確定特異点である。また$y=1/t$の変数変換で$y=\infty$も確定特異点であることが分かるため、これは$e_{1}, e_{2}, e_{3}, \infty$に特異点を持つFuchs型微分方程式になる。


## あとがき

ちょっと雑だけど、古いノートを突貫工事で補いつつテキスト化してみた。楕円函数やより一般にabel函数のノートにするには圧倒的に知識も内容も足りないので、いつか勉強してきっちり理解した上でちゃんと書きたい。

参考文献：高木とかWhittaker-Watsonとか

mathlogには分割して投稿した。
- [Weierstrassのペー函数（１）](https://mathlog.info/articles/781)
- [Weierstrassのペー函数（２）](https://mathlog.info/articles/812)