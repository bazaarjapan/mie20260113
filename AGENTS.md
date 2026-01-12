# Repository Guidelines

## 概要
このリポジトリは研修資料などの **Markdown ドキュメント** を管理します。現状は `*.md` のみで、アプリ実装やビルド成果物は含みません。
Purpose: keep training materials editable, reviewable, and easy to export.

## Project Structure & Module Organization
- ルート: ドキュメント本体（例: `三重県生成AI活用研修.md`）
- 追加する場合の推奨:
  - `assets/`: 画像・図・配布素材（`assets/images/` など）
  - `drafts/`: 下書き（公開前の原稿）
  - `templates/`: 章立てや見出しテンプレート

## Build, Test, and Development Commands
このリポジトリには専用のビルド/テスト基盤はありません（`package.json` / `Makefile` 等なし）。
- ローカル確認: エディタの Markdown Preview を利用（例: VS Code のプレビュー）
- 任意の出力（導入済みの場合）:
  - PDF 変換: `pandoc .\\三重県生成AI活用研修.md -o .\\out.pdf`
  - Lint: `markdownlint-cli2 "**/*.md"`（導入時のみ）

## Coding Style & Naming Conventions
- 記法: 見出しは `##` から段階的に、箇条書きは `-` か `*` のどちらかに統一
- 文章: 1段落は短く、結論→補足の順で記述（研修カリキュラムは「目的/手順/成果物」を明示）
- コード/コマンド/製品名: `...` で囲んで誤読を防止
- ファイル名: 日付や用途が分かる名前を推奨（例: `20260113_研修カリキュラム.md`）

## Content Guidelines
- Use clear sections: Goal / Agenda / Hands-on / Output / Q&A
- Write assumptions explicitly: audience, timebox, prerequisites, accounts needed
- Prefer concrete examples: prompt samples, inputs, expected outputs, fallback options
- Keep terminology consistent: the same tool name and the same Japanese label throughout

## Testing Guidelines
テストコードはありません。代わりに、以下をレビュー観点として扱います。
- Markdown 崩れ（見出し階層、リスト入れ子、空行）
- リンク切れ、固有名詞の表記ゆれ、機密情報の混入
Quick checklist: headings ok / links ok / dates ok / copyable commands ok.

## Commit & Pull Request Guidelines
このフォルダは現時点で Git 管理されていないため、履歴から規約を抽出できません。Git 管理する場合は以下を推奨します。
- コミット: Conventional Commits（例: `docs: add Suno AI section` / `docs: fix typos`）
- PR: 変更目的、影響範囲（対象 `.md`）、レンダリング確認（スクリーンショットが必要なら添付）を記載

## Security & Configuration Tips
- 個人情報（氏名、電話、メール、住所）や API keys / tokens を本文に含めない
- 外部サービスの利用手順は「公式ヘルプへの誘導 + 最小限の操作説明」を優先（仕様変更に強くする）
- 画像は相対パスで参照（例: `assets/images/banner.png`）し、出典とライセンスを明記

## Agent-Specific Instructions
- 生成物は日本語を基本とし、外部仕様（ツール名・コマンド）は原語のまま正確に記載してください。
- このサイトの文書は、全体的に柔らかめのトーンで統一してください。
