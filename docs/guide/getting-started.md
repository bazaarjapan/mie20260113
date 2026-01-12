# 使い始める

## ページ構成（おすすめ）
- 目的（Goal）
- 前提（Prerequisites）
- 手順（Steps）
- 期待される結果（Expected output）
- よくあるエラー（Troubleshooting）

## 章の追加方法
1. `docs/guide/` などに `*.md` を追加
2. `mkdocs.yml` の `nav:` に追加（サイドバーの順序が決まります）

例:

```yaml
nav:
  - ガイド:
      - 新しい章: guide/new-chapter.md
```

