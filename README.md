# リマインダー

iOS 風の TODO / リマインダーアプリ。リスト分けとポモドーロ式の集中モード付き。
React + Vite + Tailwind CSS で作られていて、データはブラウザの `localStorage` に保存されます。

## 開発

```bash
npm install
npm run dev
```

`http://localhost:5173` で開きます。

## ビルド

```bash
npm run build      # dist/ に出力
npm run preview    # ビルド結果をローカル確認
```

## GitHub Pages に公開する

このリポジトリには自動デプロイ用の GitHub Actions（`.github/workflows/deploy.yml`）が入っています。

1. このプロジェクトを GitHub リポジトリに push する（ブランチ名は `main`）
2. リポジトリの **Settings → Pages** を開く
3. **Build and deployment → Source** を **GitHub Actions** に設定
4. `main` に push するたびに自動でビルド＆公開されます

公開先は `https://<ユーザー名>.github.io/<リポジトリ名>/` です。
`vite.config.js` の `base` を `"./"` にしているので、リポジトリ名を問わずそのまま動きます。

## 主な機能

- リストごとの色分け・追加・削除（左スワイプで削除）
- タスクの追加 / 完了 / 削除、未完了・完了のフィルター
- 集中モード（ポモドーロ）: 25 分集中 → 5 分休憩、4 回ごとに 15 分の長い休憩
