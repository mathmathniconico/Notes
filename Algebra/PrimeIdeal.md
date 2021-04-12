
# 素イデアルと整環




## 素イデアル

__定義__ $R$を環とする。真イデアル$P\subsetneq R$は以下の条件を満たすとする。

- $x, y\in R$について、$xy\in P$なら$x\in P$または$y\in P$が成り立つ。

このとき$P$を **素イデアル** （prime ideal）と呼び、環$R$の素イデアル全体を$\mathrm{Spec}R$と表す。

__定理__ （素イデアル対応定理）$I\subset R$をイデアルとする。このとき$I$を含む$R$の素イデアル全体と$R/I$の素イデアルは一対一に対応する。

（証明）イデアル対応定理より、素イデアル$J\subset R, K\subset R/I$について

$$
\begin{aligned}
\Phi(J)&=\lbrace a+I : a\in J \rbrace \subset R/I , \\
\Psi(K)&=\lbrace a\in R : a+I\in K \rbrace \subset R
\end{aligned}
$$

が素イデアルとなることを示せば良い。

$(a+I)(b+I)=ab+I \in\Phi(J)$とする。ある$x\in J$が存在して$ab+I=x+I$だから、$ab-x\in I\subset J$である。ここで$x\in J$より$J$がイデアルであることから$ab=(ab-x)+x\in J$を得る。ところで$J$は素イデアルだから$a\in J$または$b\in J$である。故に$a+I\in\Phi(J)$または$b+I\in\Phi(J)$を得る。

$ab\in\Psi(K)$とする。定義より$(a+I)(b+I)=ab+I\in K$である。$K$は素イデアルだから$a+I\in K$または$b+I\in K$が成り立ち、$a\in\Psi(K)$または$b\in\Psi(K)$を得る。$\square$




## 整環

__定義__ ゼロでない環$R$が以下を満たすとき **域** （domain）と呼ぶ。

- $a, b\in R$について$ab=0$なら$a=0$または$b=0$が成り立つ。

> $a, b\neq 0$であって$ab=0$のとき、$a$あるいは$b$を零因子と呼ぶ。特に単位的可換環が域のとき **整域** （integral domain）と呼ぶ。

__命題__ $I\subset R$をイデアルとする。TFAE

1. $I$は素イデアルである。
1. $R/I$は域である。

（証明）$I$を素イデアルとする。$\overline{a}\cdot\overline{b}=0$とすると、$ab\in I$より$a\in I$または$b\in I$が成り立つ。故に$\overline{a}=0$または$\overline{b}=0$である。

逆に$R/I$は整とする。$ab\in I$とすると$\overline{a}\cdot\overline{b}=\overline{ab}=0$である。故に$\overline{a}=0$または$\overline{b}=0$が成り立つ。故に$a\in I$または$b\in I$である。$\square$

__定義__ $R$を環とする。$ab=ac, a\neq 0$なら$b=c$が成り立つとき、$R$は **消去可能** （eliminable）であるという。

__命題__ $R$をゼロでない環とする。TFAE

1. $R$は域である。
1. $R$は消去可能である。

（証明）$R$は整とする。$ab=ac, a\neq 0$とすると$a(b-c)=0$より$b-c=0$となる。よって消去可能である。

逆に$R$は消去可能とする。$ab=0$とする。$a\neq 0$なら$ab=0=a\cdot 0$より消去可能性から$b=0$を得る。$\square$

> 域（domain）、整域（integral）という言葉は他でも多用されがちなので、別の良い方があるべきだと思う。