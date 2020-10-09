# 読み方

- ブラウザの拡張機能を使う（Chrome系のブラウザの場合）
    1. [github-math-display](https://chrome.google.com/webstore/detail/github-math-display/cgolaobglebjonjiblcjagnpmdmlgmda)（[GitHub](https://github.com/AaronCQL/katex-github-chrome-extension)）

- VSCodeで見る
    1. このリポジトリをダウンロードして[VSCode](https://code.visualstudio.com)でプレビューする。以下のプラグインが必要。
    1. [Markdown+Math](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)（[GitHub](https://github.com/goessner/mdmath)）
    数式をプレビューできるプラグイン。
    1. [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)（[GitHub](https://github.com/shd101wyy/vscode-markdown-preview-enhanced)）
    数式をプレビューできる多機能で強力なプラグイン。
        - `enableScriptExecution`を`true`に設定すればmarkdown内のコードを実行できる。
        - 可換図式の描画にはLaTeXエンジン（[TeXLive](https://www.tug.org/texlive/)）と[pdf2svg](https://github.com/jalios/pdf2svg-windows)が必要。
        - 環境変数の編集前に必ずバックアップを取ること。
        - 出力された一時ファイルのsvgを保存する方法が分からない。

[参考資料](/References.md)

# 可換環論

準備中

# 収束空間論

過去に作ったノートに穴が結構あったので修正しつつ移植中。CCSあたりの証明をもっとシンプルにしたい。

1. フィルターと収束空間の基礎

    1. [フィルターとprefilter](/ConvergentSpace/Filter.md)
    1. [フィルターの大小（Wedge積とVel積）](/ConvergentSpace/FinerCoarser.md)
    1. [フィルター射（始フィルターと終フィルター）](/ConvergentSpace/InitialFinal.md)
    1. [収束空間と連続射](/ConvergentSpace/Conv.md)
    1. [Continuous Convergence Structure](/ConvergentSpace/CCS.md)

1. 収束空間と位相空間
    1. [収束空間の位相構造](/ConvergentSpace/FilterOpenTopology.md)
    1. 位相空間の収束構造
    1. [超フィルター](/ConvergentSpace/UltraFilter.md)

# 圏論

- [圏の定義](/Category/Category.md)
- [米田の補題](/Category/YonedaLemma.md)

# 多様体ノート

志賀浩二「多様体論」（岩波基礎数学選書）を底本とした多様体のノート。序章で多様体論の概要について述べ、精密な議論は後の章で行う。底本はファイバーバンドルからドラーム理論、サードの定理まで書いてあるが、そこまでこのノートが続くかは不明。

1. 序章

    1. [座標をもつ空間](/Manifold/CoordinatedSpace.md)
    1. [曲線と曲面概念の拡張](/Manifold/WhatIsManifold.md)
    1. [多様体の誕生](/Manifold/BirthOfManifold.md)
    1. [多様体に関する諸注意](/Manifold/RemarkOfManifold.md)
    1. [接ベクトルと接バンドル](/Manifold/Tangent.md)

1. 多様体論


# 執筆環境

- VSCodeでmarkdownを書く。
- Markdown+Mathでインライン数式をハイライトする。
- Markdown Preview Enhancedでプレビューする。図式のプレビューとしても用いる。
- [Tex2img](https://tex2img.tech)で図式等のsvgを生成。

## 筆者について

- [arXiv探訪](https://arxiv.hatenablog.com) ブログ
- [マストドン](https://mathtod.online/@mathmathniconico) 数式が書けるツイッターみたいなSNS
- [エッセイ2020](/Essay/Essay2020.md)