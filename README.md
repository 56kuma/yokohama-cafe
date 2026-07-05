# yokohama-cafe

横浜駅・東神奈川エリアの赤ちゃん連れで行きやすいカフェ・レストランをまとめた静的サイトです。

- `index.html` 1ファイルだけの自己完結型（外部依存なし）
- モバイルファーストのカードレイアウト
- ダークモード対応（OSの設定に自動追従）

## Cloudflare Pages への公開方法

1. [Cloudflare ダッシュボード](https://dash.cloudflare.com/) → **Workers & Pages** → **Create** → **Pages** → **Connect to Git**
2. このリポジトリ（`56kuma/yokohama-cafe`）を選択
3. ビルド設定は以下の通り（静的HTMLのみなのでビルド不要）
   - **Framework preset**: None
   - **Build command**: （空欄）
   - **Build output directory**: `/`
4. **Save and Deploy** で公開完了

以降は `main` ブランチにプッシュするたびに自動でデプロイされます。

### CLI で公開する場合（Wrangler）

```sh
npx wrangler pages deploy . --project-name=yokohama-cafe
```
