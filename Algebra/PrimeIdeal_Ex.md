
# 単項イデアルの生成元が単元で移り合わない例について

マストドンの方である方と本読みをしているのだけど、その本に次の問題があった。

> 問題　環$R$において$(\alpha)=(\beta)\Leftrightarrow\exists\varepsilon\in U; \varepsilon\alpha=\beta$を証明せよ．

この本では、環とは単位的可換環のことであり、また$U$は単元全体を指す。つまり単項イデアルの生成元は互いに同伴であることを主張している。しかしながら、これは一般の環では恐らく成り立たない。この問題の書かれた節は整域を扱っているので、「整域$R$において」と修正するべきだとすぐ気づく。

証明は簡単で、右から左は明らか。逆は$\alpha=s\beta, \beta=t\alpha$となるから$\beta=ts\beta$つまり$(1-ts)\beta=0$を得る。$R$が整域なら$\beta\neq 0$のとき$ts=1$より$t, s$は単元となる。$\beta=0$のときも$\alpha=\beta=0$となるので単元$1$で移り合う。

このような修正はよくあることだが、しかし果たして反例はあるのだろうか？　となるのは当然である。


## 証明の反例

整域でない場合、上の証明が上手く働かない例を作ることができる。

例えば$\mathbb{Z}/42\mathbb{Z}$において$\alpha=12, \beta=18$を考える。このとき$(12)=(18)$である。しかし$12=3\times 18$かつ$18=12\times 12$であり、$s=3, t=12$とすると$ts=36\neq 1$となってしまう。

ただしこれは主張の反例ではない。例えば$12=17\times 18$かつ$18=5\times 12$であり、$s=17, t=5$とすると$ts=1$を得る。つまり単元の組を取れるという主張の反例としては不適である。


## 主張の反例

$(\alpha)=(\beta)$なら$\alpha=s\beta, \beta=t\alpha$と表せるから、これらが不定元となるような環を考える。つまり$\alpha, t, s$を不定元として、$\beta:=t\alpha$と定義する。すると$\alpha=s\beta=st\alpha$となるので、これが常に成り立っていればよい。

$K$を体として、$R=K\lbrack \alpha, s, t \rbrack/(\alpha-st\alpha)$と定める。このとき$\beta:=t\alpha$とすると$\alpha=st\alpha=s\beta$となる。また$(\alpha)=(st\alpha)=(s\beta)\subset(\beta)=(t\alpha)\subset(\alpha)$より$(\alpha)=(\beta)$が成り立つ。

__主張__ $\alpha, \beta$は単元で移り合わない。

ある$u$が存在して$\alpha=u\beta$が$R$において成り立つとする。このとき$\alpha-u\beta\in (\alpha-st\alpha)$より、ある$f$が存在して$\alpha-ut\alpha=f(\alpha-st\alpha)$を満たす。このとき$\alpha(1-ut-f+fst)=0$だから多項式環の整域性より$1-ut-f+fst=0$である。$u$について解きたいが$t$が邪魔なのでなんとかしたい。

$f=1-t(u-fs)$なので$g:=u-fs$とおくと$f=1-tg$となる。すると$u=(1-tg)s+g=(1-ts)g+s$を得る。ここでもし$u$が$R$において単元なら、ある$p, q$が存在して

$$
p\lbrack (1-ts)g+s \rbrack+q\lbrack \alpha-st\alpha \rbrack=1
$$

と表せる。$\alpha=0$を代入すると特に$p(s, t)\lbrack (1-ts)g(s, t)+s\rbrack=1$が成り立つ。しかし全次数を考えると左辺が$0$次になることはないので矛盾する。

また、ある$v$が存在して$\beta=v\alpha$が$R$において成り立つとする。このとき$t\alpha-v\alpha\in (\alpha-st\alpha)$より、ある$h$が存在して$t\alpha-v\alpha=h(\alpha-st\alpha)$を満たす。同様に$t-v=h(1-st)$だから、$v=-h(1-st)+t$を得る。残りの議論も同様に従う。


## 所感

整域でない場合に、イデアルの生成元に対する可移性のような概念は一般に考えられているのだろうか？