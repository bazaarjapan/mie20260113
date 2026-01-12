# 画像の扱い

## 置き場所
画像は `docs/assets/images/` に置きます。

例:
- `docs/assets/images/login.png`
- `docs/assets/images/step-01.png`

## Markdown から参照する
同一階層のページから参照する例:

```md
![](assets/images/step-01.png)
```

`docs/guide/` 配下のページから参照する例:

```md
![](../assets/images/step-01.png)
```

## 命名ルール（おすすめ）
- 小文字 + ハイフン区切り: `step-01.png`
- 手順番号を入れる（並び替えに強くする）: `setup-01.png`, `setup-02.png`

