# 読み方

- ブラウザの拡張機能を使う（Chrome系のブラウザの場合）
    1. [github-math-display](https://chrome.google.com/webstore/detail/github-math-display/cgolaobglebjonjiblcjagnpmdmlgmda)（[GitHub](https://github.com/AaronCQL/katex-github-chrome-extension)）

- VSCodeで見る
    1. このリポジトリをダウンロードして[VSCode](https://code.visualstudio.com)でプレビューする。以下のプラグインが必要。
    1. [Markdown+Math](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)（[GitHub](https://github.com/goessner/mdmath)）
    数式をプレビューできるプラグイン。
    1. [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)（[GitHub](https://github.com/shd101wyy/vscode-markdown-preview-enhanced)）
    数式をプレビューできる多機能で強力なプラグイン。



# 数理論理学

- [順序数](/Logic/Ordinal.md)


# 圏論

- [圏論について](/Category/AboutMyCat.md)
- [圏](/Category/Category.md)
- [例示：圏](/Category/Category_Ex.md)
- [普遍性](/Category/Universality.md)
- 例示：普遍性
- [函手](/Category/Functor.md)
- [忠実充満函手と部分圏](/Category/Subcategory.md)
- 前層の圏
- [米田の補題](/Category/YonedaLemma.md)
- 極限と余極限
- 随伴
- [モノ射とエピ射](/Category/MonoEpi.md)

# 代数学

## 可換環論

- [群](/Algebra/Group.md)
- [例示：群](Algebra/Group_Ex.md)
- [環](/Algebra/Ring.md)
- [素イデアルと整環](/Algebra/PrimeIdeal.md)
- [環上の加群](/Algebra/Module.md)
- [例示：群・環・加群](/Algebra/AlgebraBasic_Ex.md)
- ネーター加群
- 多項式環
- 自由加群
- ヒルベルトの基底定理
- 環上の代数と次数付き環
- 斉次イデアルとクルルの交叉定理
- [群の作用](/Algebra/GroupAction.md)


## ガロア理論入門

- [体とその拡大](/Algebra/GaloisIntro/Field.md)
- [多項式](/Algebra/GaloisIntro/Polynomial.md)
- [ガロア拡大](/Algebra/GaloisIntro/GaloisExtension.md)
- [代数体のガロア理論](/Algebra/GaloisIntro/GaloisTheory.md)

## 余代数

- [代数と余代数](/Algebra/Coalgebra/Coalgebra.md)
- [例示：余代数](/Algebra/Coalgebra/Coalgebra_Ex.md)
- 余代数の準同型
- [余代数のイデアルと剰余余代数](/Algebra/Coalgebra/QuotientCoalgebra.md)
- [Incidence余代数](/Algebra/Coalgebra/IncidenceCoalgebra.md)
- [半順序集合のIncidence Algebra](/Algebra/Coalgebra/PosetIncidenceAlgebra.md)
- [メビウス函数の計算](/Algebra/Coalgebra/MobiusFunction.md)


# 収束空間論

過去に作ったノートに穴が結構あったので修正しつつ移植中。CCSあたりの証明をもっとシンプルにしたい。

1. 位相空間の基礎
    1. [位相](/ConvergentSpace/Top.md)

1. フィルター付き空間の基礎

    1. [フィルターとprefilter](/ConvergentSpace/Filter.md)
    1. [Wedge積とVel積](/ConvergentSpace/WedgeVel.md)
    1. [始フィルターと終フィルター](/ConvergentSpace/InitialFinal.md)

1. 収束空間の基礎
    1. [収束空間と連続射](/ConvergentSpace/Conv.md)
    1. [Continuous Convergence Structure](/ConvergentSpace/CCS.md)
    1. [収束空間の位相構造（隣接位相）](/ConvergentSpace/FilterOpenTopology.md)
    1. [位相空間の収束構造（位相収束構造）](/ConvergentSpace/TopologicalConv.md)
    1. [例：反射的有向グラフ](/ConvergentSpace/ReflexiveDirectedGraph.md)

1. 収束空間における位相概念
    1. [超フィルター](/ConvergentSpace/UltraFilter.md)


# その他

- [Microfacet理論](/Misc/Microfacet.md)
- [組合せ論的クリフォード代数](/Misc/CombinatorialCliffordAlgebra.md)
- [クリフォード代数の例](/Misc/CliffordAlgebraExamples.md)
- [ワイエルシュトラスのペー函数](/Misc/WeierstrassP.md)
- [距離空間とリプシッツ写像](/Misc/LipschitzMap.md)


# 多様体のノート

志賀浩二「多様体論」（岩波基礎数学選書）を底本とした多様体のノート。序章で多様体論の概要について述べ、精密な議論は後の章で行う。底本はファイバーバンドルからドラーム理論、サードの定理まで書いてある。

1. 序章

    1. [座標をもつ空間](/Manifold/CoordinatedSpace.md)
    1. [曲線と曲面概念の拡張](/Manifold/WhatIsManifold.md)
    1. [多様体の誕生](/Manifold/BirthOfManifold.md)
    1. [多様体に関する諸注意](/Manifold/RemarkOfManifold.md)
    1. [接ベクトルと接バンドル](/Manifold/Tangent.md)

1. 多様体論


# このリポジトリについて

勉強ノートなので命題の並びや証明は底本の影響が大きい。

- [参考文献](/References.md)

## 著者

- [arXiv探訪](https://arxiv.hatenablog.com) ブログ
- [マストドン](https://mathtod.online/@mathmathniconico) 数式が書けるツイッターみたいなSNS

### エッセイ

主にマストドンでトゥートした一部を抜粋

- 2020年 [その1](/Essay/Essay2020_1.md)、[その2](/Essay/Essay2020_2.md)
- 2021年 [その1](/Essay/Essay2021_1.md)

## 執筆環境

- VSCodeでmarkdownを書く。
- Markdown+Mathでインライン数式をハイライトする。
- Markdown Preview Enhancedでプレビューする。図式のプレビューとしても用いる。
- [Tex2img](https://tex2img.tech)で図式等のsvgを生成。
- GitHub Desktopで公開。

Markdown Preview Enhancedは数式をプレビューできるVSCodeのプラグイン。

- `enableScriptExecution`を`true`に設定すればmarkdown内のコードを実行できる。
- 可換図式の描画にはLaTeXエンジン（[TeXLive](https://www.tug.org/texlive/)と[pdf2svg](https://github.com/jalios/pdf2svg-windows)が必要。
- 環境変数の編集前に必ずバックアップを取ること。
- 出力された一時ファイルのsvgを保存する方法が分からない。
- 微妙に動作が不安定で、表示が更新されずVSCodeを閉じないと復活しないときがある。