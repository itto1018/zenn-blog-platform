# Obsidian

## 概要

学習目的のメモ管理ツールとして導入。ローカルのMarkdownファイル+双方向リンク+グラフビューで、学んだ内容同士のつながりを可視化しながら蓄積できる(Zettelkasten的な使い方)。

このリポジトリ(zenn-blog-platform)とは直接連携しないが、「学習メモをObsidianで育てて、記事化できそうなものだけ`articles/`にコピーして清書する」という2段階の運用を想定している。

## インストール手順

Homebrew caskで導入。

```bash
brew install --cask obsidian
```

`/Applications/Obsidian.app` にインストールされ、CLIバイナリ `obsidian-cli` が `/opt/homebrew/bin/obsidian` にリンクされる。

## 設定・運用方針

- Vaultは特定プロジェクトに紐づけず、複数プロジェクト共通で使えるように配置する。
  - 場所: `/Users/itto/Development/Obsidian/`
- Vault自体は本リポジトリ(zenn-blog-platform)には含めない。学習メモと投稿用記事のリポジトリを分離するため。
- Vault初回作成はGUI操作が必要。Obsidian起動後のダイアログで **Open folder as vault** を選び、上記ディレクトリを指定する。

## 参考リンク

- [Obsidian公式サイト](https://obsidian.md/)
- [Obsidian Help](https://help.obsidian.md/)
