
# 例示：群




__例__ 以下は群の例である。

- $\mathbb{Z}, \mathbb{Q}, \mathbb{R}, \mathbb{C}$は、加法に関してアーベル群となる。単位元は$0$で、$a$の逆元は$-a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$から原点を除いた集合$k^{\times}$は、乗法に関してアーベル群となる。単位元は$1$で、$a$の逆元は$1/a$である。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$n$次正則行列全体$\mathrm{GL}(n; k)$は、行列の積に関して群となる。このような群を一般線型群という。
- 相異な$n$文字の置換（全単射）全体$S_{n}$は、写像の合成に関して群となる。これを$n$次対称群という。







## 部分群の例

__例__ 以下は部分群の例である。

- $\mathbb{Z}\lt\mathbb{Q}\lt\mathbb{R}\lt\mathbb{C}$である。
- $\mathbb{T}_{1}=\lbrace z\in\mathbb{C} : \vert z \vert=1 \rbrace$は$\mathbb{C}^{\times}$の部分群である。これを$1$次元トーラスという。
- $k=\mathbb{Q}, \mathbb{R}, \mathbb{C}$について$\mathrm{SL}(n; k):=\lbrace A\in\mathrm{GL}(n; k) : \mathrm{det}A=1 \rbrace$は$\mathrm{GL}(n; k)$の部分群である。これを特殊線型群という。
- 正方形でない長方形$R$を$R$自身に写す変換は$4$頂点の置換で表され、その全体$V$は$S_{4}$の部分群となる。これをクラインの$4$群という。

> TODO 合同関係と正規部分群の例、準同型と同型の例



大事な部分群の例を挙げておこう。$ g\in G, S\subset G $に対し次を定める。
\begin{EnumCond}
\item $ \langle g \rangle:=\lbrace g^{n} \mid n\in\mathbb{Z} \rbrace $を$ g $により生成される
\index{じゅんかいぐん@巡回群}巡回群（\index{cyclic group}cyclic group）という。
\item $ \mathrm{Z}(S):=\lbrace x\in G \mid \forall s\in S, xs=sx \rbrace $を$ S $の
\index{ちゅうしんかぐん@中心化群}中心化群（\index{centralizer group}centralizer group）という。
\item $ \mathrm{N}(S):= \lbrace x\in G \mid xS=Sx \rbrace $を$ S $の
\index{せいきかぐん@正規化群}正規化群（\index{normalizer group}normalizer group）という。
\end{EnumCond}
このとき$ \langle g \rangle $の濃度を$ g $の\index{いすう@位数}位数（\index{order}order）
といい$ \mathrm{ord}g $と表す。このとき$ \langle 1 \rangle\subset\langle g \rangle\subset G $を考えれば、
指数の性質より$ \mathrm{ord}g $は$ \sharp G $を割る。巡回群はアーベル群である。

\begin{Prop}{}{}
部分群$ H\lt G $に対し次が成り立つ。
\begin{EnumCond}
\item $ H\lhd G \Longleftrightarrow \mathrm{N}(H)=G $が成り立つ。
\item $ H\lhd \mathrm{N}(H) $が成り立つ。
\item $ \mathrm{Z}(G)\lhd G $が成り立つ。
\end{EnumCond}
\end{Prop}

$ \mathrm{Z}(G) $は$ G $の\index{ちゅうしん@中心}中心（\index{center}center）と呼ばれ、しばしばこれを求めることが重要な問となる。

群においても準同型、同型を定義することができる。$ f:G\rightarrow H $が群の\index{じゅんどうけい@準同型}準同型
（\index{homomorphism}homomorphism）であるとは、$ f(ab)=f(a)f(b) $を満たすことをいう。
単位元が単位元に対応し、また逆元の像が逆元となる。このとき$ f $の像$ \mathrm{Im}f $及び核$ \mathrm{Ker}f $は$ H, G $の部分群となり、
特に核は正規部分群となる。従って準同型定理$ \mathrm{Im}f\cong_{\mathrm{grp}} G/\mathrm{Ker}f $が成り立つ。同様に群の完全系列
\[ 1\rightarrow\mathrm{Ker}f\rightarrow G\xrightarrow{f} H\rightarrow\mathrm{Cok}f\rightarrow 1 \]
も成り立つ。特にこの系列に対しては、元の位数を交互に逆数をとることで$ 1 $となることに注意する。

群$ G $から$ G $自身への同型全体は恒等写像$ \mathrm{id}:x\mapsto x $を単位元とする群を為す。これを$ \mathrm{Aut}G $と表し$ G $の
\index{じこどうけいぐん@自己同型群}自己同型群（\index{automorphism group}automorphism group）と呼ぶ。
加えて$ a\in G $に対し$ \sigma_{a}:x\mapsto axa^{-1} $と定めると同型となる。
特にその全体は$ \mathrm{Aut}G $の部分群となるため、これを\index{ないぶじこどうけいぐん@内部自己同型群}内部自己同型群
（\index{inner automorphism group}inner automorphism group）と呼び$ \mathrm{Inn}G $で表す。
全射準同型$ G\rightarrow \mathrm{Inn}G: a\mapsto \sigma_{a} $を考えればその核は$ G $の中心となる。
故に群としての同型$ G/\mathrm{Z}(G)\cong_{\mathrm{grp}} \mathrm{Inn}G $を得る。
