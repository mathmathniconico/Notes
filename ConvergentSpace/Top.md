
# 位相





__補題__ （開近傍による開集合の特徴付け）$(X, \mathcal{O})$を位相空間、$U\subset X$とする。TFAE

1. $U\in\mathcal{O}$である。
1. 任意の$x\in U$に対し、ある$V\in\mathcal{O}$が存在して$x\in V\subset U$である。

（証明）$U\in\mathcal{O}$なら$V$として$U$を取ればよい。逆は$x\in X$に対して$S_{x}:=\lbrace V\in\mathcal{O} : x\in V\subset U \rbrace$と置くと、仮定より$S_{x}\neq\emptyset$である。つまり$\exists V_{x}\in S_{x}$だが、集合$\lbrace V_{x} : x\in X \rbrace$を取りたい。ここで選択公理を使っても良いが、実は$V_{x}:=\cup S_{x}$と指定してしまえば必要ない。このとき$V_{x}\in\mathcal{O}$であり$x\in V_{x}\subset U$が成り立つ。従って$U=\bigcup_{x\in X}V_{x}\in\mathcal{O}$である。$\square$