# Obsidian

## 概要

学習目的のメモ管理ツールとして導入。ローカルのMarkdownファイル+双方向リンク+グラフビューで、学んだ内容同士のつながりを可視化しながら蓄積できる(Zettelkasten的な使い方)。

Vaultはこのリポジトリ内の`vault/`に置き、「学習メモをObsidianで育てて、記事化できそうなものだけ`articles/`にコピーして清書する」という2段階の運用を想定している。

## インストール手順

Homebrew caskで導入。

```bash
brew install --cask obsidian
```

## 設定・運用方針

- Vaultはリポジトリ直下の`vault/`に配置し、学習メモもリポジトリで一緒に管理する。
- Vaultを開くには、Obsidian起動後のダイアログで **Open folder as vault** を選び、リポジトリ内の`vault/`を指定する。
- `.obsidian/`の設定はGit管理するが、ウィンドウ配置など環境ごとに変わる`workspace.json` `workspace-mobile.json`や、ゴミ箱の`.trash/`は`.gitignore`で追跡対象外にしている。

## 参考リンク

- [Obsidian公式サイト](https://obsidian.md/)
- [Obsidian Help](https://help.obsidian.md/)
