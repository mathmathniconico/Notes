
# 圏の定義

以下で構成される組$\mathscr{C}=(\mathrm{Ob}(\mathscr{C}), \mathrm{Mor}(\mathscr{C}), s, t, \circ )$を考える。

- $\mathrm{Ob}(\mathscr{C})$は集合である。この要素を **対象** （object）と呼ぶ。
- $\mathrm{Mor}(\mathscr{C})$は集合である。この要素を **射** （morphism）と呼ぶ。
- $s\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$は写像である。射$f$について$s(f)$を$f$の始域（domain）と呼ぶ。
- $t\colon\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Ob}(\mathscr{C})$は写像である。射$f$について$t(f)$を$f$の終域（codomain）と呼ぶ。
- $t(f)=s(g)$を満たす射$f, g$について合成（composition）と呼ばれる射$g\circ f$が定義され、$s(g\circ f)=s(f), t(g\circ f)=t(g)$を満たす。

集合のファイバー積を用いるなら、$\circ$は然るべき条件を満たす写像

$$
\circ\colon\mathrm{Mor}(\mathscr{C})\underset{t, \mathrm{Ob}(\mathscr{C}), s}{\times}\mathrm{Mor}(\mathscr{C})\rightarrow\mathrm{Mor}(\mathscr{C})
$$

である。

- $x$が$\mathscr{C}$の対象であること（$x\in\mathrm{Ob}(\mathscr{C})$）を、省略して$x\in\mathscr{C}$と書く。
- 射$f\in\mathrm{Mor}(\mathscr{C})$について$s(f)=x, t(f)=y$のとき、$f$は$x$から$y$への射であるといい$f\colon x\rightarrow y$と書く。
- 対象$x, y\in\mathscr{C}$について、$x$から$y$への射全体を$\mathrm{Mor}_{\mathscr{C}}(x, y)$で表す。添え字の$\mathscr{C}$は適宜省略される。

- $\mathrm{Mor}(\mathscr{C})=\bigsqcup_{x, y\in\mathscr{C}}\mathrm{Mor}(x, y)$は非交叉和である。

> 圏の定義も色々あって、最後の非交叉性が成り立たない場合もあるが、それだと問題が起こるらしい。詳しくは知らない。

__定義__ 上記の組$\mathscr{C}$が以下を満たすとき **圏**（category）と呼ぶ。

- 任意の対象$x$について恒等射$\mathrm{id}_{x}\in\mathrm{Mor}(x, x)$が存在し、合成を定義できる射$f, g$について$\mathrm{id}_{x}\circ f=f, g\circ\mathrm{id}_{x}=g$が常に成り立つ。
- 合成を定義できる射$f, g, h$について$(f\circ g)\circ h=f\circ(g\circ h)$が成り立つ。

> 上の定義は一般に「小さい圏」と呼ばれるものの定義である。$\mathrm{Ob}(\mathscr{C})$が真クラス（従って$\mathrm{Mor}(\mathscr{C})$も真クラス）でも同様な概念を考察できるが、これは「大きな圏」と呼ばれる。その中でも任意の対象$x, y$について$\mathrm{Mor}(x, y)$が集合である場合は「局所的に小さい圏」と呼ぶ。しかし「大きな圏」を考慮すると「大きな圏の集まり」を議論する必要があり、それは数理論理学の範疇であり筆者も詳しくない。従って以下やこれ以外のノートにおいて単に「圏」と呼ぶときは基本的に「小さい圏」を考え、そうでない場合も記述を簡単にするための「言葉としての圏論」を扱う。
>
> あるいは「大きな圏」のリストを挙げてしまう方法もある。集合の圏$\mathbf{Sets}$、アーベル群の圏$\mathbf{Ab}$、群の圏$\mathbf{Grp}$、群$G$の作用する集合の圏$G\mathbf{sets}$、環$R$上の加群の圏$\mathbf{Mod}_{R}$、体$k$上のベクトル空間の圏$\mathbf{Vect}_{k}$、環の圏$\mathbf{Ring}$、スキームの圏$\mathbf{Sch}$、位相空間の圏$\mathbf{Top}$、位相空間$X$上の前層の圏$\mathbf{Psh}(X)$と層の圏$\mathbf{Sh}(X)$、更に$X$上のアーベル群の前層の圏$\mathbf{PAb}(X)$と$X$上のアーベル群の層の圏$\mathbf{Ab}(X)$、圏$\mathscr{C}$から$\mathbf{Sets}$への函手の圏$\mathbf{Sets}^{\mathscr{C}}=\mathbf{Funct}(\mathscr{C}, \mathbf{Sets})$、$\mathscr{C}$上の前層の圏$\mathbf{Psh}(\mathscr{C})=\mathbf{Funct}(\mathscr{C}^{op}, \mathbf{Sets})$、$\mathscr{C}$上の層の圏$\mathbf{Sh}(\mathscr{C})$などが挙げられる。他にも使う場合は、ここに加えて行けばよい。

- $\mathrm{id}_{x}$は一意的である。

__定義__ 射$f\colon x\rightarrow y$が **同型** （isomorphism）であるとは、ある$g\colon y\rightarrow x$が存在して$g\circ f=\mathrm{id}_{x}, f\circ g=\mathrm{id}_{y}$が成り立つことをいう。このとき$x$と$y$は同型といい、$x\simeq y$と表す。

- $f$が同型のとき、上の$g$もまた同型であり、更に$g$は一意に定まる。これを$f^{-1}$と表し、$f$の逆（inverse）と呼ぶ。

__例__ 全ての射が同型であるときgroupoid（群っぽい）という。例えば群$G$は、$\lbrace \ast \rbrace$を対象の集合、$G$を射の集合とするgroupoidとなる。あるいは射の集合が恒等射のみからなる圏もgroupoidである。

__定義__ 圏$\mathscr{A}, \mathscr{B}$について、$\mathscr{A}$と$\mathscr{B}$の積という圏$\mathscr{A}\times\mathscr{B}$を以下で定める。

- 対象の集合は$\mathrm{Ob}(\mathscr{A}\times\mathscr{B}):=\mathrm{Ob}(\mathscr{A})\times\mathrm{Ob}(\mathscr{B})$とする。
- 射の集合は$\mathrm{Mor}_{\mathscr{A}\times\mathscr{B}}((x, y), (z, w)):=\mathrm{Mor}_{\mathscr{A}}(x, z)\times\mathrm{Mor}_{\mathscr{B}}(y, w)$とする。


## 函手

__定義__ $\mathscr{A}, \mathscr{B}$は圏とする。$\mathscr{A}$から$\mathscr{B}$への **函手** （functor）$F\colon\mathscr{A}\rightarrow\mathscr{B}$は以下で構成される。

- 対象$x\in\mathscr{A}$について対象$Fx\in\mathscr{B}$が定義されている。
- 対象$x, y\in\mathscr{A}$及び射$f\in\mathrm{Mor}_{\mathscr{A}}(x, y)$について射$Ff\in\mathrm{Mor}_{\mathscr{B}}(Fx, Fy)$が定義されている。
- 以上は全て射の合成と恒等射に関してcompatibleである。つまり$F(f\circ g)=Ff\circ Fg$であり、$F\mathrm{id}_{x}=\mathrm{id}_{Fx}$である。

> 函手は写像の組として書くこともできる。

- 函手は同型を保存する。つまり$x\simeq y$なら$Fx\simeq Fy$である。



