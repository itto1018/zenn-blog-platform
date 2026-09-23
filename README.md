# zenn-blog-platform

Zennに記事・本を投稿するためのローカル執筆環境（プラットフォーム）です。[zenn-cli](https://github.com/zenn-dev/zenn-editor/tree/canary/packages/zenn-cli)を使用しています。

このリポジトリではツール構成（`package.json`など）、ツール導入手順（`docs/`）、学習メモ用のObsidian Vault（`vault/`）をGit管理しており、`articles/` `books/` `drafts/` 配下のコンテンツ自体は`.gitignore`で追跡対象外にしています（ディレクトリ構造のみ`.gitkeep`で保持）。記事は内容の変更が頻繁なため、Gitでの履歴管理はせずZennのWeb版エディタで直接投稿する運用です。

## セットアップ

```bash
pnpm install
```

## 使い方

### 新しい記事を作成

```bash
pnpm new:article
```

`articles/` 配下にランダムなslugのMarkdownファイルが生成されます（Git管理対象外）。

### 新しい本を作成

```bash
pnpm new:book
```

`books/` 配下に生成されます（Git管理対象外）。

### プレビュー

```bash
pnpm preview
```

`http://localhost:8000` でプレビューできます。

## 投稿方法

1. `pnpm new:article` でローカルに下書きを作成
2. `pnpm preview` で確認しながら執筆
3. 完成したら[Zennのダッシュボード](https://zenn.dev/dashboard)から記事を貼り付けて公開

> GitHub連携による自動デプロイを使う場合は、`articles/` `books/` を`.gitignore`から外して追跡対象にした上で、[Zennのデプロイ設定](https://zenn.dev/dashboard/deploys)からこのリポジトリを連携してください。

## ディレクトリ構成

| パス | 内容 | Git管理 |
| --- | --- | --- |
| `articles/` | Zennの記事（`pnpm new:article`で生成） | 対象外 |
| `books/` | Zennの本（`pnpm new:book`で生成） | 対象外 |
| `drafts/` | 記事化する前の下書き・資料置き場 | 対象外 |
| `docs/` | このプロジェクトに導入したツールの導入手順 | 対象 |
| `vault/` | 学習メモ用のObsidian Vault（[詳細](docs/obsidian.md)） | 対象 |

## ドキュメント

このプロジェクトに導入したツールの導入手順は `docs/` にまとめています。

* [Zenn CLI](docs/zenn_cli.md)
* [pnpm](docs/pnpm.md)
* [Obsidian](docs/obsidian.md)

## 参考

* [📘 Zenn CLIの使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)
* [📘 Markdown記法一覧](https://zenn.dev/zenn/articles/markdown-guide)
