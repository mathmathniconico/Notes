
# 素イデアルと整環




## 素イデアル

__定義__ $P\subsetneq R$を真イデアルとする。$P$が以下の条件を満たすとき **素イデアル** （prime ideal）と呼ぶ。

- $x, y\in R$について、$xy\in P$なら$x\in P$または$y\in P$が成り立つ。

$R$の素イデアル全体を$\mathrm{Spec}R$と表す。

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

<!--

__定義__ $R$を環とする。

- $a\in R$が零因子であるとは、あるゼロでない$b\in R$が存在して$ab=0$または$ba=0$を満たすことをいう。
- ゼロ以外の零因子を持たない環を **整環** （integral ring）という。
- 特に単位的可換環が整環であるとき、 **整域** （integral domain）という。

__命題__ $I\subset R$をイデアルとする。TFAE

1. $I$は素イデアルである。
1. $R/I$は整環である。

（証明）

$\square$

__定義__ $R$を環とする。$ab=ac, a\neq 0$なら$b=c$が成り立つとき、$R$は **消去可能** （eliminable）であるという。

__命題__ $R$を環とする。TFAE

1. $R$は整環である。
1. $R$は消去可能である。

（証明）

$\square$






## 可除環

- $R^{\times}:=\lbrace 

- $R$を単位的可換環とする。$R^{\times}=R\backslash\lbrace 0 \rbrace$について$(R^{\times}, \cdot, 1)$がアーベル群となるとき、$R$は **体** （field）という。

-->