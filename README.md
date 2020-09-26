# 読み方

- ブラウザの拡張機能を使う（Chrome系のブラウザの場合）
    1. [github-math-display](https://chrome.google.com/webstore/detail/github-math-display/cgolaobglebjonjiblcjagnpmdmlgmda)（[GitHub](https://github.com/AaronCQL/katex-github-chrome-extension)）
    一番手軽。

- VSCodeで見る
    1. このリポジトリをクローンorダウンロードして、各markdownをプレビューする。以下のプラグインが必要。
    1. [Markdown+Math](https://marketplace.visualstudio.com/items?itemName=goessner.mdmath)（[GitHub](https://github.com/goessner/mdmath)）
    数式をプレビューできるシンプルなプラグイン。更にmarkdownの数式をハイライトしてくれる。

    1. [Markdown Preview Enhanced](https://marketplace.visualstudio.com/items?itemName=shd101wyy.markdown-preview-enhanced)（[GitHub](https://github.com/shd101wyy/vscode-markdown-preview-enhanced)）
    多機能かつ強力なプラグイン。プレビューだけでなく、コードの実行も可能。LaTeXも動かすことができ、TikZ-cdを用いて可換図式を表示することもできるのだが、以下の問題がある。
        - markdownの数式をハイライトしてくれない。（Markdown+Mathと併用可能）
        - コードの実行には設定の`enableScriptExecution`を`true`にする必要がある。（注意：セキュリティ上のリスクあり）
        - 可換図式の描画にはLaTeXエンジン（最新の[TeXLive](https://www.tug.org/texlive/)で良い）と[pdf2svg](https://github.com/jalios/pdf2svg-windows)が必要。特に後者は環境変数を自分で設定する必要がある。（注意：環境変数は編集前に必ずバックアップを取ること）
        - 出力されたsvgは一時ファイルだが、その保存方法が分からない。可能ならリンクを挿入することでGitHub上でも見れるようになるのだが。

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
