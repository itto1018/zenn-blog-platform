# it-blog-zenn

Zennに記事・本を投稿するためのコンテンツリポジトリです。[zenn-cli](https://github.com/zenn-dev/zenn-editor/tree/canary/packages/zenn-cli)を使用しています。

## セットアップ

```bash
npm install
```

## 使い方

### 新しい記事を作成

```bash
npm run new:article
```

`articles/` 配下にランダムなslugのMarkdownファイルが生成されます。

### 新しい本を作成

```bash
npm run new:book
```

### プレビュー

```bash
npm run preview
```

`http://localhost:8000` でプレビューできます。

## Zennとの連携（GitHub連携）

1. このリポジトリをGitHubにpushする
2. [Zennのデプロイ設定](https://zenn.dev/dashboard/deploys)からこのリポジトリを連携する
3. `main`ブランチにpushすると自動的に記事が公開されます

記事のfront matterで `published: true` にすると公開されます。

## 参考

* [📘 Zenn CLIの使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)
* [📘 Markdown記法一覧](https://zenn.dev/zenn/articles/markdown-guide)
