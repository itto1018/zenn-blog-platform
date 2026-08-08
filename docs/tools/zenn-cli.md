# Zenn CLI

## 概要

Zennに記事・本を投稿するためのローカル執筆環境を作るために導入。ローカルでMarkdownを書き、`zenn preview`で確認してからZennのWeb版エディタに貼り付けて投稿する運用にしている。

## インストール手順

```bash
pnpm init
pnpm add zenn-cli
pnpm exec zenn init
```

> 初期構築時はnpmで導入したが、その後pnpmに移行した。移行手順は[pnpm.md](./pnpm.md)を参照。

`zenn init` によって以下が生成される。

- `articles/` — 記事の格納先
- `books/` — 本の格納先
- `.gitignore`(node_modulesなど)
- `README.md`(zenn-cliのデフォルト説明)

`package.json` には以下のスクリプトを追加している。

```json
{
  "scripts": {
    "preview": "zenn preview",
    "new:article": "zenn new:article",
    "new:book": "zenn new:book"
  }
}
```

## 設定・運用方針

- `articles/` `books/` は内容の変更が頻繁なため、**Git管理対象外**にしている(`.gitignore`で`/articles/*` `/books/*`を無視し、`.gitkeep`でディレクトリ構造のみ保持)。
- 記事はZennのWeb版エディタで直接投稿する運用のため、GitHub連携による自動デプロイは現時点では未使用。
  - 自動デプロイを使う場合は`.gitignore`から`articles/` `books/`を外し、[Zennのデプロイ設定](https://zenn.dev/dashboard/deploys)からリポジトリを連携する。
- リポジトリ名は `zenn-blog-platform`(GitHub: https://github.com/itto1018/zenn-blog-platform)。

## 使い方

```bash
pnpm new:article   # 新しい記事を作成
pnpm new:book      # 新しい本を作成
pnpm preview       # http://localhost:8000 でプレビュー
```

## 参考リンク

- [📘 Zenn CLIの使い方](https://zenn.dev/zenn/articles/zenn-cli-guide)
- [📘 Markdown記法一覧](https://zenn.dev/zenn/articles/markdown-guide)
