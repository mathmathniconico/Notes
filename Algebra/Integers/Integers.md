
# 整数

## 有理整数環

TODO: 整除、GCD、LCM、素数、互除法、基本定理

## 剰余環

合同、フェルマーの小定理、CRT


## 既約剰余類群

__命題__ $G$を有限集合とする。$G$上の演算$\cdot\colon G\times G\rightarrow G$は結合律を満たし、単位元$1_{G}\in G$が存在するとする。TFAE

- $(G, \cdot, 1_{G})$は群である。
- $a, b, c\in G$について$a\cdot b=a\cdot c$なら$b=c$である。（消去律）

（証明）上から下は明らか。$G$は有限集合なので$a\in G$について$\lbrace a^{n} : a=1, 2, \dotsc \rbrace$もまた有限集合である。従って$a^{n}=a^{m}$となる$n\gt m$を取れば

$$
a^{m}\cdot 1_{G}=a^{m}=a^{n}=a^{m}\cdot a^{n-m}
$$

より消去律から$a^{n-m}=1_{G}$を得る。特に$a\cdot a^{m-n-1}=a^{m-n-1}\cdot a=1_{G}$より$a$は逆元を持つ。$\square$

> この命題は有限集合が群であることを示すとき非常に有用である。

オイラーの定理

