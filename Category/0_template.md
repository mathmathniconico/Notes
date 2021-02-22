
# タイトル

あああ



## 見出し1


あああ


### 見出し1-1

あああ


### 見出し1-2

あああ



## 見出し2

<p align=center><img src="pics/category_01.svg" height="100"></p>

```latex {cmd}
\documentclass{standalone}
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
\begin{document}

\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[rrd, bend left, "v"] \arrow[rdd, bend right, "u"'] \arrow[rd, dashed, "h"] & & \\
& A\prod_{f, C, g}B \arrow[d, "p"'] \arrow[r, "q"] & B \arrow[d, "g"] \\
& A \arrow[r, "f"'] & C
\end{tikzcd}

\end{document}
```



<details>
<summary>LaTeXソース</summary>

```latex
% プリアンブル
\usepackage{amsmath, amssymb, mathrsfs}
\usepackage{tikz-cd}
```

```latex
% aaa.svg
\begin{tikzcd}[contains/.style = {phantom, "\ni", sloped}]
X \arrow[rrd, bend left, "v"] \arrow[rdd, bend right, "u"'] \arrow[rd, dashed, "h"] & & \\
& A\prod_{f, C, g}B \arrow[d, "p"'] \arrow[r, "q"] & B \arrow[d, "g"] \\
& A \arrow[r, "f"'] & C
\end{tikzcd}
```


</details>





<!--




-->
