# zenn-blog-platform

Zennに記事・本を投稿するためのローカル執筆環境（プラットフォーム）です。[zenn-cli](https://github.com/zenn-dev/zenn-editor/tree/canary/packages/zenn-cli)を使用しています。

このリポジトリではツール構成（`package.json`など）のみをGit管理しており、`articles/` `books/` 配下のコンテンツ自体は`.gitignore`で追跡対象外にしています（ディレクトリ構造のみ`.gitkeep`で保持）。記事は内容の変更が頻繁なため、Gitでの履歴管理はせずZennのWeb版エディタで直接投稿する運用です。

## セットアップ

```bash
npm install
```

## 使い方

### 新しい記事を作成

```bash
npm run new:article
```

`articles/` 配下にランダムなslugのMarkdownファイルが生成されます（Git管理対象外）。

### 新しい本を作成

```bash
npm run new:book
```

`books/` 配下に生成されます（Git管理対象外）。

### プレビュー

```bash
npm run preview
```

`http://localhost:8000` でプレビューできます。

## 投稿方法

1. `npm run new:article` でローカルに下書きを作成
2. `npm run preview` で確認しながら執筆
3. 完成したら[Zennのダッシュボード](https://zenn.dev/dashboard)から記事を貼り付けて公開

> GitHub連携による自動デプロイを使う場合は、`articles/` `books/` を`.gitignore`から外して追跡対象にした上で、[Zennのデプロイ設定](https://zenn.dev/dashboard/deploys)からこのリポジトリを連携してください。

## 参考

* [📘 Zenn CLIの使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)
* [📘 Markdown記法一覧](https://zenn.dev/zenn/articles/markdown-guide)
