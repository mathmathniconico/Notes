
# フェルマーの小定理

Fermatの名を冠す定理は数あれど、最初に出会うのは小定理だろう。基本的な定理だけに応用も広く証明も様々だが、例の如くFermat自身のものは残っていないらしい。

__命題__ （フェルマーの小定理A）$p$を素数、$a$を$p$の倍数でない整数とする。このとき

$$
a^{p-1}\equiv 1\mod p
$$

が成り立つ。

（証明）$a\gt 0$は$p$の倍数でないとする。$a, 2a, \dotsc, (p-1)a$は法$p$で互いに異なるゼロでない元を与えている。従ってその積は

$$
(p-1)!a^{p-1}\equiv (p-1)!\mod{p}
$$

を満たす。$(p-1)!$は$p$と互いに素なので$a^{p-1}\equiv 1$でなければならない。$a\lt 0$のとき、$p=2$に対しては$a\equiv -a$より従い、奇素数$p$に対しては$p-1$が偶数なので$a^{p-1}=(-a)^{p-1}$より従う。$\square$

フェルマーの小定理は$a\equiv 0$の場合も含めると次のように書ける。

__命題__ （フェルマーの小定理B）$p$を素数、$a$を整数とする。このとき

$$
a^{p}\equiv a\mod p
$$

が成り立つ。

（証明）$a\gt 0$とする。二項展開を調べると$(x+y)^{p}\equiv x^{p}+y^{p}$が恒等的に成り立つことが分かる。よって

$$
a^{p}\equiv 1^{p}+(a-1)^{p}\equiv\dotsb\equiv a\mod{p}
$$

を得る。$a\le 0$のときは$a\equiv b$となる$b\gt 0$を考えればよい。$\square$




## coloringによる拡張

J.Petersenはcoloringと呼ばれる手法で小定理Bを次のように証明した。（1872）

（証明）$a\gt 0$とする。$p$個の箱を用意し、それらが円周上に並んでいるとする。これらを$a$色で塗り分けたい。色塗りの総数は$a^{p}$通りである。このうち全ての箱が同色となるのは$a$通りしかない。それ以外の塗り方は、$p$が素数なので、回転させると異なる塗り方になる。つまり$p$の倍数通りである。故に$a^{p}-a$は$p$の倍数である。先程と同様に$a\le 0$でも成り立つ。$\square$

coloringの方法は一般の有限群に拡張できる。

__定理__ $G$を有限群、$a\in\mathbb{Z}$とする。このとき

$$
\sum_{g\in G}a^{\vert G \vert/\mathrm{ord}g}\equiv 0\mod{\vert G \vert}
$$

が成り立つ。

（証明）$a\gt 0$とする。写像$G\rightarrow\lbrace 1, \dotsc, a \rbrace$を$G$の$a$色coloringと呼び、その全体を$X$とする。このとき作用$G\curvearrowright X$が$g\cdot\phi(h):=\phi(hg^{-1})$で定まる。ここで$g\in G$を固定すると、$\phi\in X$に対し以下は同値となる。

- $\phi\in X^{g}$である。つまり$g\cdot\phi=\phi$が成り立つ。
- $\phi$は任意の$h\in G$について$h\langle g \rangle$上一定値を取る。

従って$\phi$の任意性は$\langle g \rangle$の左剰余類につき$a$色となるから、

$$
\vert X^{g} \vert=a^{\vert G/\langle g \rangle \vert}=a^{(G : \langle g \rangle)}=a^{\vert G \vert/\mathrm{ord}g}
$$

となる。Cauchy-Frobenius countingより

$$
\frac{1}{\vert G \vert}\sum_{g\in G}\vert X^{g} \vert
$$

は定数だから命題の式が従う。先程と同様に$a\le 0$でも成り立つ。$\square$

__系__ （coloringによる拡張）$a$を整数、$m$を正の整数とする。このとき

$$
\sum_{d\vert m}\varphi\left(\frac{m}{d}\right)a^{d}=\sum_{k=1}^{m}a^{(k, m)}\equiv 0 \mod{m}
$$

が成り立つ。（ただし$(k, m)$は$k$と$m$の最小公倍数を表し、$\varphi$はオイラーのtotient函数とする。）

（証明）定理の$G$として$\mathbb{Z}/m\mathbb{Z}$を取る。$k=1, \dotsc, m$に対して$\mathrm{ord}\overline{k}=m/(k, m)$だから、右の式が成り立つ。$(k, m)=d$となる$k$の個数はちょうど$\varphi(m/d)$個なので左の等式が成り立つ。$\square$

> 特に$m=p$を素数とすると、$\varphi(p)=p-1, \varphi(1)=1$だから$(p-1)a+a^{p}\equiv 0$よりフェルマーの小定理Bを得る。




## オイラーの定理

> TODO:



## メビウス函数による拡張

> TODO:






<!--


# ニュートン多項式が満たす性質
対称式というものは厄介な存在で、出会った時はその重要性に気付かず、後で忘失して後悔する人も多いのではないだろうか（自分だけかも）。そういえば「基本対称式で全ての対称式が書き下せる」という定理は「知ってるようで知らない命題」の一つかもしれない。Newton多項式に関する性質もその一つである。

** 命題 **
$\theta\_{1}, \dotsc, \theta\_{D}$に対し$s\_{i}:=\theta\_{1}^{i}+\dotsb+\theta\_{D}^{i}$と置く。また多項式$P(x)$及び$a\_{1}, \dotsc, a\_{D}$を

<center>$\begin{align*} P(x) &:=(x-\theta_{1})\dotsm (x-\theta_{D}) \\ &=x^{D}-a_{1}x^{D-1}-\dotsb-a_{D-1}x-a_{D} \end{align*}$</center>

により定める。このとき$k>D$に対して$a\_{k}=0$と定めれば、任意の$n$に対して

<center>$s_{n}=a_{1}s_{n-1}+\dotsb+a_{n-1}s_{1}+na_{n}$</center>

が成り立つ。

$s\_{n}$のことを$n$次ニュートン多項式という。上記はこの漸化式を与えているとみなすことができる。

（証明）$n=D$のとき、$P(\theta\_{1})=\dotsb=P(\theta\_{D})=0$より、$D$本の式を足し合わせることで

<center>$s_{D}-a_{1}s_{D-1}-\dotsb-a_{D-1}s_{1}-Da_{D}=0$</center>

を得る。よって正しい。実は示すのはこれだけでよい。

$D\lt n$のときは変数を増やして今の結果を用いる。

<center>$\begin{align*} Q(x) &=(x-\theta_{1})\dotsm(x-\theta_{D})(x-\theta_{D+1})\dotsm(x-\theta_{n}) \\ &=x^{n}-b_{1}x^{n-1}-\dotsm-b_{n} \end{align*}$</center>

とおくと、$t\_{i}:=\theta\_{1}^{i}+\dotsb+\theta\_{D}^{i}+\theta\_{D+1}^{i}+\dotsb+\theta\_{n}^{i}$に対して

<center>$t_{n}-b_{1}t_{n-1}-\dotsb-b_{n-1}t_{1}-nb_{n}=0$</center>

が成り立つ。ここで$\theta\_{D+1}=\dotsb=\theta\_{n}=0$を代入すれば$t\_{i}=s\_{i}, b\_{i}=a\_{i}$を得るので、命題の式が成り立つことが分かる。

$D\gt n$のときは$s\_{n}-a\_{1}s\_{n-1}-\dotsb-s\_{n-1}s\_{1}$と$na\_{n}$を比較して一致を示す。両方とも$\lbrace \theta\_{i} \rbrace$に関して$n$次の項のみを持ち、任意の項$\theta\_{i\_{1}}\dotsm\theta\_{i\_{n}}$に対して係数を調べれば、現れない$\theta\_{j}$に$0$を代入することで上の場合に帰着できる。これが一致することは既に示したので全体としても一致し、結局$s\_{n}-a\_{1}s\_{n-1}-\dotsb-s\_{n-1}s\_{1}=na\_{n}$を得る。$\square$

（複素解析を用いた証明）複素変数$z$を導入して少し計算すれば、適当な領域で次の等式を得る。

<center>$\displaystyle D+\sum_{n=1}^{\infty}s_{n}z^{n}=\sum_{j=1}^{D}\frac{1}{1-\theta_{j}z}=\frac{P^{\prime}(z^{-1})}{zP(z^{-1})}.$</center>

右辺の分母を掃って

<center>$\displaystyle \begin{align*} \left( D+\sum_{n=1}^{\infty}s_{n}z^{n}\right)& \left( 1-a_{1}z-a_{2}z^{2}-\dotsb-a_{D}z^{D}\right) \\ &=D-(D-1)a_{1}z-(D-2)a_{2}z^{2}-\dotsb-2a_{D-2}z^{D-2}-a_{D-1}z^{D-1} \end{align*}$</center>

を得る。あとは$z^{n}$の係数を比較すれば良い。実際$n\gt D$のとき$s\_{n}-a\_{1}s\_{n-1}-\dotsb-a\_{D}s\_{n-D}=0$となるが、$k>D$で$a\_{k}=0$より命題の式を得る。$n=D$のときは$s\_{D}-a\_{1}s\_{D-1}-\dotsb-a\_{D-1}s\_{1}-Da\_{D}=0$を得る。$n\lt D$のときは左辺が$s\_{n}-a\_{1}s\_{n-1}-\dotsb-a\_{n-1}s\_{1}-Da\_{n}$となるが、右辺は$-(D-n)a\_{n}$なのでやはり正しい。$\square$

# Partition-coloring

$a\_{1}, a\_{2}, a\_{3}, \dotsc$は自然数とする。これらはパレットを表していて、$j$番目のパレットには$a\_{j}$色がある。次に$n$個の箱を用意し、先ほどと同様に円周上に並べておく。これらを色で塗り分けたいのだが、少し条件を加える。箱の間に区切り（partition）を置き、その間に$j$個の箱が並ぶなら$j$番目のパレットから一色を選び、その色でその$j$個の箱を塗る。つまり$a\_{j}$通りの選択肢がある。このルールの下での色塗り（$n$-ptn-colと呼ぶことにする）の総数を$s^{\ast}\_{n}$と置く。

** 定理 **
$s^{\ast}\_{n}$は

<center>$s^{\ast}_{n}=a_{1}s^{\ast}_{n-1}+\dotsb+a_{n-1}s^{\ast}_{1}+na_{n}$</center>

及び

<center>$\displaystyle \sum_{d\vert n}s^{\ast}_{d}\mu\left(\frac{n}{d}\right)\equiv 0\mod n$</center>

を満たす。

（証明）箱に$B\_{0}, \dotsc, B\_{n-1}$とラベルを貼る。$B\_{0}$から数えて一番最初の区割りを$B\_{t}, \dotsc, B\_{t+u-1}$とする。この$u$個の箱を除くと、$u\lt n$なら$(n-u)$-ptn-colに帰着できる。また逆に$n-u$個の場合から$u$個の箱を（最初の区切りに）挿入することで$n$-ptn-colを作れる。この対応は一対一なので、$u=n$の場合（$na\_{n}$通りの色分け方（区切り位置もあるので$n$倍されている））も入れて漸化式を作ると

<center>$\displaystyle s^{\ast}_{n}=\sum_{u=1}^{n-1}a_{u}s^{\ast}_{n-u}+na_{n}$</center>

を得る。これは一つ目の式である。

次に$r\_{n}$を$n$-ptn-colで、自明な回転を除き全て異なる塗り方になるものの総数とする。この定義から$r\_{n}$が$n$の倍数であることは直ぐわかる。$n$-ptn-colは、$d\vert n$に対し$d$回転で初めて同じ塗り方になるものを含むが、これらは自明な回転を除き全て異なる塗り方になる$d$-ptn-colを$\frac{n}{d}$回繰り返すことで得られるため、その総数は$r\_{d}$個である。よって

<center>$\displaystyle s^{\ast}_{n}=\sum_{d\vert n}r_{d}$</center>

が成り立つ。ここで$\mathrm{M\ddot{o}bius}$の反転公式を用いると、二番目の式

<center>$\displaystyle r_{n}=\sum_{d\vert n}s^{\ast}_{d}\mu\left(\frac{n}{d}\right)\equiv 0 \mod n$</center>

を得る。$\square$

反転公式様様である。

# 一般化されたフェルマーの小定理

さて、$s\_{n}$及び$s^{\ast}\_{n}$の漸化式を見比べると、$a\_{i}\gt 0$なら$s\_{n}=s^{\ast}\_{n}$であることが分かる。更に

<center>$\displaystyle \sum_{d\vert n}s_{d}\mu\left(\frac{n}{d}\right)\equiv 0\mod n$</center>

も直ちに従う。一般の$a\_{i}$に対しては$a\_{i}=a\_{i}^{+}-k\_{i}n, a\_{i}^{+}\gt 0$と置けば、$a\_{i}^{+}$に対する結果より従う。この結果は始めに表で挙げた式を含んでいる。

    -->

## 参考文献
    [1] C.J.Smith. A Coloring Proof of a Generalisation of Fermat's Little Theorem.
    [2] I.M.Isaacs, M.R.Pournaki. Generalizations of Fermat's Little Theorem via Group Theory. The Mathematical Association of America, Monthly 112, October 2005, pp.734-740.
