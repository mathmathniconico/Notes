以下は基本的に$C^{\infty}$構造もとい滑らかな構造の話である。

## 座標をもつ空間の接ベクトル

$X$を$C^{\infty}$級の座標をもつ空間とする。座標写像$\phi_{\alpha}$に対して$\phi_{\alpha}(X)=U_{\alpha}$と表し、$x\in X$の像を$x_{\alpha}=(x_{\alpha}^{1}, \dotsc, x_{\alpha}^{n})$などと表す。

座標変換$\phi_{\alpha}\circ\phi_{\beta}^{-1}$は$U_{\beta}$から$U_{\alpha}$への$C^{\infty}$函数である。従って$C^{\infty}$函数$F^{1}, \dotsc, F^{n}$で

$$
\begin{aligned}
x_{\alpha}^{1} &=x_{\alpha}^{1}(x_{\beta}^{1}, \dotsc, x_{\beta}^{n})=F_{\alpha\beta}^{1}(x_{\beta}^{1}, \dotsc, x_{\beta}^{n}), & & \dotsc, & x_{\alpha}^{n} &=x_{\alpha}^{n}(x_{\beta}^{1}, \dotsc, x_{\beta}^{n})=F_{\alpha\beta}^{n}(x_{\beta}^{1}, \dotsc, x_{\beta}^{n})
\end{aligned}
$$

と表せる。このJacobi行列

$$
J(x_{\alpha}/x_{\beta})=\left(
\begin{matrix}
\frac{\partial x_{\alpha}^{1}}{\partial x_{\beta}^{1}} & \cdots & \frac{\partial x_{\alpha}^{1}}{\partial x_{\beta}^{n}} \\
\vdots & & \vdots \\
\frac{\partial x_{\alpha}^{n}}{\partial x_{\beta}^{1}} & \cdots & \frac{\partial x_{\alpha}^{n}}{\partial x_{\beta}^{n}}
\end{matrix}
\right)=\left(
\begin{matrix}
\frac{\partial F_{\alpha\beta}^{1}}{\partial x_{\beta}^{1}} & \cdots & \frac{\partial F_{\alpha\beta}^{1}}{\partial x_{\beta}^{n}} \\
\vdots & & \vdots \\
\frac{\partial F_{\alpha\beta}^{n}}{\partial x_{\beta}^{1}} & \cdots & \frac{\partial F_{\alpha\beta}^{n}}{\partial x_{\beta}^{n}}
\end{matrix}
\right)
$$

は$J(x_{\alpha}/x_{\beta})J(x_{\beta}/x_{\alpha})=J(x_{\alpha}/x_{\alpha})=I$より$U_{\beta}$上で可逆である。

$X$上の$C^{\infty}$函数族$C^{\infty}(X)$は座標の取り方に依らず定義されている。しかし変な話ではあるが、$f\in C^{\infty}(X)$に対して$f$の微分は定義されていない。そこで座標写像$\phi_{\alpha}$を取り、$f\circ\phi_{\alpha}^{-1}$を$U_{\alpha}$上の函数とみて、$x_{\alpha}$での値を単に$f(x_{\alpha})$と略記する。このとき各点での偏導関数は

$$
\frac{\partial f}{\partial x_{\alpha}^{1}}(x_{\alpha}), \dotsc, \frac{\partial f}{\partial x_{\alpha}^{n}}(x_{\alpha})
$$

と表せる。この値は座標写像の取り方に依存する。実際、座標写像$\phi_{\beta}$に対して

$$
\frac{\partial f}{\partial x_{\beta}^{1}}(x_{\beta}), \dotsc, \frac{\partial f}{\partial x_{\beta}^{n}}(x_{\beta})
$$

は一般に異なる値をとる。ただし座標変換があるので関係式

$$
\frac{\partial f}{\partial x_{\beta}^{j}}(x_{\beta})=\sum_{i=1}^{n}\frac{\partial x_{\alpha}^{i}}{\partial x_{\beta}^{j}}\frac{\partial f}{\partial x_{\alpha}^{i}}(x_{\alpha})
$$

は成立する。

もう少し詳しく議論するために方向微分を考える。$U_{\alpha}$上の$\xi_{\alpha}=(\xi_{\alpha}^{1}, \dotsc, \xi_{\alpha}^{n})$方向への微分を取る操作

$$
\left.\sum_{i=1}^{n}\xi_{\alpha}^{i}\frac{\partial}{\partial x_{\alpha}^{i}}\right\vert_{x}\colon f\mapsto \sum_{i=1}^{n}\xi_{\alpha}^{i}\frac{\partial f}{\partial x_{\alpha}^{i}}(x_{\alpha})
$$

を考える。もし全ての$f\in C^{\infty}(X)$に対して、$U_{\alpha}$上の$\xi_{\alpha}$方向への微分と、$U_{\beta}$上の$\eta_{\beta}$方向への微分が一致しているなら、

$$
\sum_{i=1}^{n}\xi_{\alpha}^{i}\frac{\partial f}{\partial x_{\alpha}^{i}}(x_{\alpha})=\sum_{j=1}^{n}\eta_{\beta}^{j}\frac{\partial f}{\partial x_{\beta}^{j}}(x_{\beta})=\sum_{i=1}^{n}\sum_{j=1}^{n}\eta_{\beta}^{j}\frac{\partial x_{\alpha}^{i}}{\partial x_{\beta}^{j}}\frac{\partial f}{\partial x_{\alpha}^{i}}(x_{\alpha})
$$

が成り立つ。逆に

$$
\xi_{\alpha}^{i}=\sum_{j=1}^{n}\frac{\partial x_{\alpha}^{i}}{\partial x_{\beta}^{j}}\eta_{\beta}^{j}
$$

が成り立てば2つの方向微分は一致する。この条件は簡単に$\xi_{\alpha}=J(x_{\alpha}/x_{\beta})\eta_{\beta}$と表せる。

> 記号の乱用が気になる人もいるかもしれないが面倒なので許してほしい。

$\xi_{\alpha}=(\xi_{\alpha}^{1}, \dotsc, \xi_{\alpha}^{n})\in\mathbb{R}^{n}$に対して方向微分

$$
\xi_{\alpha}^{1}\left.\frac{\partial}{\partial x_{\alpha}^{1}}\right\vert_{x}+\dotsb+\xi_{\alpha}^{n}\left.\frac{\partial}{\partial x_{\alpha}^{n}}\right\vert_{x}
$$

を考え、全体を$T_{x}(\phi_{\alpha})$とすると$n$次元の線型空間となる。そこで$\xi_{\alpha}$に対応する元もまた$\xi_{\alpha}$と表すことにする。ここで$\xi_{\alpha}=J(x_{\alpha}/x_{\beta})\eta_{\beta}$の関係にある$\xi_{\alpha}\in T_{x}(\phi_{\alpha}), \eta_{\beta}\in T_{x}(\phi_{\beta})$を同一視すれば$\bigcup_{\alpha}T_{x}(\phi_{\alpha})$上の同値関係であり、同値類全体を$T_{x}(X)$と表す。すると$J(x_{\alpha}/x_{\beta})$は線型同型であるから$T_{x}(X)$もまた$n$次元の線型空間となる。これを$x$における **接空間** 、その元を **接ベクトル** と呼ぶ。

$\xi\in T_{x}(X)$をとると、座標写像$\phi_{\alpha}$について$T_{x}(\phi_{\alpha})$における代表元$\xi_{\alpha}$が一意に定まる。ここで$f\in C^{\infty}(X)$について

$$
\xi(f):=\sum_{i=1}^{n}\xi_{\alpha}^{i}\frac{\partial f}{\partial x_{\alpha}^{i}}(x_{\alpha})
$$

と定めると、右辺の値は座標写像の取り方に依らず確定し、以下を満たす。

- $\xi(af+bg)=a\xi(f)+b\xi(g)$が成り立つ。（$a, b\in\mathbb{R}, f,g\in C^{\infty}(X)$）
- $\xi(fg)=\xi(f)g(x)+\xi(g)f(x)$が成り立つ。（$f,g\in C^{\infty}(X)$）

これらは座標写像を用いずに述べられるので、実は逆にこの性質を満たすものとして接空間を定めることが出来る。

> $C^{r}(X)$級の方向微分として定義すると厳密には一致しない。

まとめると、方向微分という素朴な対象から作用素（函数空間からの写像）としての接ベクトル・接空間という概念に至った。ここまでくれば多様体上に拡張することはたやすい。


## 多様体上の接空間と接バンドル

$C^{\infty}$多様体$M$について、以下を満たす写像$\xi\colon C^{\infty}(M)\rightarrow\mathbb{R}$を$x\in M$における接ベクトルという。

- $\xi(af+bg)=a\xi(f)+b\xi(g)$が成り立つ。（$a, b\in\mathbb{R}, f,g\in C^{\infty}(X)$）
- $\xi(fg)=\xi(f)g(x)+\xi(g)f(x)$が成り立つ。（$f,g\in C^{\infty}(X)$）

$x$における接ベクトル全体を$T_{x}(M)$と書き、$x$における接空間という。局所座標を一つ取れば座標を持つ空間となるから、接ベクトルはある方向微分として表すことができる。よって$T_{x}(M)$は$n$次元線型空間であることが分かる。

こうして接空間$T_{x}(M)$を沢山並べることができるが、お互いに全く関係がないというわけではない。$x, y\in M$が同じ局所座標$(U_{\alpha}, \phi_{\alpha})$に含まれているとする。$\phi_{\alpha}(x)=(x_{\alpha}^{1}, \dotsc, x_{\alpha}^{n})$とすると、

$$
\begin{aligned}
\left\lbrace \left.\frac{\partial}{\partial x_{\alpha}^{1}}\right\vert_{x}, \dotsc, \left.\frac{\partial}{\partial x_{\alpha}^{n}}\right\vert_{x} \right\rbrace &\subset T_{x}(M), & \left\lbrace \left.\frac{\partial}{\partial x_{\alpha}^{1}}\right\vert_{y}, \dotsc, \left.\frac{\partial}{\partial x_{\alpha}^{n}}\right\vert_{y} \right\rbrace\subset T_{y}(M)
\end{aligned}
$$

はそれぞれの基底を与えている。従って$\xi_{\alpha}=(\xi_{\alpha}^{1}, \dotsc, \xi_{\alpha}^{n})\in\mathbb{R}^{n}$が与えられたとき、接ベクトルの同一視によって$\xi_{\alpha}$は$T_{x}(M)$においては

$$
\xi_{\alpha}^{1}\left.\frac{\partial}{\partial x_{\alpha}^{1}}\right\vert_{x}+\dotsb+\xi_{\alpha}^{n}\left.\frac{\partial}{\partial x_{\alpha}^{n}}\right\vert_{x}\in T_{x}(M)
$$

を表し、$T_{y}(M)$においては

$$
\xi_{\alpha}^{1}\left.\frac{\partial}{\partial x_{\alpha}^{1}}\right\vert_{ｙ}+\dotsb+\xi_{\alpha}^{n}\left.\frac{\partial}{\partial x_{\alpha}^{n}}\right\vert_{ｙ}\in T_{ｙ}(M)
$$

を表す。言い換えると$U_{\alpha}$上で各接空間$T_{x}(M)$の元を一斉に成分表示できる。この意味で

$$
T(M)\vert U_{\alpha}:=\bigcup_{x\in U_{\alpha}}T_{x}(M)\longleftrightarrow U_{\alpha}\times\mathbb{R}^{n}
$$

という一対一の対応が得られる。

$x\in U_{\alpha}\cap U_{\beta}$のとき、上記の対応によって$\xi\in T_{x}(M)$は$\mathbb{R}^{n}$の元として2通りの表現を持つことになる。これを$\xi_{\alpha}, \xi_{\beta}\in\mathbb{R}^{n}$とすると、座標変換から

$$
\xi_{\alpha}^{i}=\sum_{j}^{n}\frac{\partial x_{\alpha}^{j}}{\partial x_{\beta}^{i}}\xi_{\beta}^{j}
$$

を満たすことが分かる。

この概念はより一般的なベクトル・バンドルの立場から見た方が明快なので、ここでは述べない。

