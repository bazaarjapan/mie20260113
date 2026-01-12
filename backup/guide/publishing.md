# 公開（GitHub Pages）

このサイトは **GitHub Actions** で MkDocs をビルドし、**GitHub Pages** にデプロイします。

## 1) リポジトリ設定
GitHub のリポジトリ画面で以下を設定します。
- `Settings` → `Pages`
- `Build and deployment` → `Source`: `GitHub Actions`

## 2) 公開URL（補足）
公開URLは通常 `https://<org-or-user>.github.io/<repo>/` になります。

このリポジトリの場合は `https://bazaarjapan.github.io/mie20260113/` です。

`mkdocs.yml` の `site_url` はこのURLに合わせて更新してください。

## 3) 公開のトリガー
`main` ブランチへ push すると、`.github/workflows/deploy-pages.yml` が走って自動公開されます。
