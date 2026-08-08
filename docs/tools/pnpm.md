# pnpm

## 概要

パッケージマネージャをnpmからpnpmに移行した。ディスク効率(依存パッケージのハードリンク共有)と速度のメリットを取るため。

## インストール手順

Homebrewで導入済み(既にグローバルインストールされていた)。

```bash
brew install pnpm
```

## 移行手順(npm → pnpm)

```bash
rm -rf node_modules package-lock.json
pnpm install
```

`pnpm install`により`pnpm-lock.yaml`が生成される。`package.json`には利用バージョンを固定するため`packageManager`フィールドを追加した。

```json
{
  "packageManager": "pnpm@11.17.0"
}
```

## 設定・運用方針

- `package-lock.json`は削除し、`pnpm-lock.yaml`をコミット対象にする。
- `.gitignore`に`.pnpm-store`(ローカルキャッシュ)を追加している。
- `package.json`のscriptsはそのまま流用可能(`pnpm run <script>`または`pnpm <script>`で実行)。

## 使い方

```bash
pnpm install       # 依存関係インストール
pnpm <script名>     # package.jsonのscriptsを実行(runは省略可)
```

## 参考リンク

- [pnpm公式サイト](https://pnpm.io/)
