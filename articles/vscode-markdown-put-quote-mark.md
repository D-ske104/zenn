---
title: "VSCodeで複数行にMarkdownの引用符を付ける"
emoji: "🤞"
type: "tech" # tech: 技術記事 / idea: アイデア
topics: ["VSCode", "Markdown"]
published: false
---

## 目的

**Markdown**でテキストを書いているときに**複数行**に対してまとめて**引用符**を付けたい。

## 課題

私が使っているVSCode拡張機能にそういう機能がない。

## 方法

**選択範囲**に**マルチカーソル**を置く機能を使う。

### 手順

1. 対象のテキストをドラッグなどして**範囲選択**する。
2. `Shift + Alt + I` [^1] で選択範囲の行末に**マルチカーソル**を置く。
3. `Home` キーでマルチカーソルを**行頭に移動**させる。
4. **引用符** `>` を入力する。
5. おわり。

### 付録

![vscode-markdown-put-quote-mark.gif](/images/vscode-markdown-put-quote-mark.gif)[^2]

## 感想

最終的な結論に至るまで試行錯誤したけど、シンプルにマルチカーソルで解決してしまいました。

::::details あがいた記録

:::details 正規表現で置換する
@[gist](https://gist.github.com/D-ske104/c9e87b8207f9c0dda781cfd91503aeb6)
:::

::::

マルチカーソル便利。

この機会に**VSCodeのショートカットを一覧**したら結構ためになりました。

https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf

`Ctrl + Shift + K` で行の削除なんかは工程を減らせて結構便利ですね。

~~**Zenモード`Ctrl + K Z`は[Downwell](https://store.steampowered.com/app/360740/Downwell/?l=japanese)のプレイ画面にそっくり。**~~

ショートカットに割り当てられていないそのほかのコマンドも早めに一覧した方がそれ以降の作業効率が上がっていいでしょうね。

https://code.visualstudio.com/api/references/commands

[^1]: Visual Studio Code Keyboard shortcuts for Windows - https://code.visualstudio.com/shortcuts/keyboard-shortcuts-windows.pdf
[^2]: ウォッチャー | Vue.js - https://ja.vuejs.org/guide/essentials/watchers.html
