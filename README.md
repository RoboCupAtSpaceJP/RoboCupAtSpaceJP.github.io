# RoboCup@Space Website

このリポジトリは、**RoboCup@Space公式Webサイト（GitHub Pages）**のコンテンツを管理するためのものです。

## 公開サイトの構成

- `index.html`
  - 公式トップページ（概要、ニュース、大会ページへの導線）
- `styles.css`
  - 共通スタイル
- `years/2026.html`
  - 2026年度大会ページ（ルール・結果・スケジュール）
- `years/template.html`
  - 次年度ページ作成用テンプレート
- `img/robocup_space.jpg`
  - RoboCup@Spaceロゴ

## 使い方

1. `years/template.html` をコピーして `years/2027.html` のように新年度ページを作成
2. `index.html` の「年度別大会ページ」に新しいカードを追加
3. GitHub Pagesに反映（`main`ブランチ公開設定）


## ローカル確認

以下のコマンドでローカルサーバーを起動して確認できます。

```bash
python3 -m http.server 8000
```

ブラウザで `http://localhost:8000` を開いて表示確認してください。

## 参考リンク

- [RoboCup Japan Official Website](https://www.robocup.or.jp/)
- [RoboCup@Space Community (Discord)](https://discord.gg/nCs4AzANwt)
