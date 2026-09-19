# RoboCup JapanOpen @Space Challenge Website

このリポジトリは、**RoboCup JapanOpen @Space Challenge 公式Webサイト（GitHub Pages）**のコンテンツを管理するためのものです。

日本語版・英語版のトップページ、および年度別大会ページを収録しています。

## 公開サイトの構成

```text
/
├── index.html
├── styles.css
├── years/
│   ├── 2026.html
│   ├── 2027.html
│   └── template.html
├── en/
│   ├── index.html
│   └── years/
│       ├── 2026.html
│       ├── 2027.html
│       └── template.html
├── img/
└── docs/
    ├── 2025/
    └── 2026/
```

### 日本語版

* `index.html`

  * 公式トップページ
  * @Space Challengeの概要
  * 年度別大会ページ
  * ニュース
  * 論文・学会発表
  * 関連資料

* `years/2026.html`

  * RoboCup JapanOpen 2026 @Space Challenge 大会ページ
  * 大会概要
  * 競技内容
  * 参加登録
  * スケジュール
  * 競技結果
  * 運営体制
  * 参考情報

* `years/2027.html`

  * RoboCup JapanOpen 2027 @Space Challenge 大会ページ
  * 開催情報は決定次第更新

* `years/template.html`

  * 次年度以降の大会ページ作成用テンプレート

### 英語版

* `en/index.html`

  * 英語版トップページ

* `en/years/2026.html`

  * 2026年度大会ページ英語版

* `en/years/2027.html`

  * 2027年度大会ページ英語版

* `en/years/template.html`

  * 英語版年度ページ作成用テンプレート

### 共通ファイル

* `styles.css`

  * 日本語版・英語版で共通して使用するスタイルシート

* `img/`

  * Webサイト内で使用する画像

* `docs/`

  * 競技ルール、タイムテーブル、学会発表資料などのPDFファイル

## 新年度ページの追加方法

### 1. 日本語版

`years/template.html` をコピーし、例えば2028年度の場合は以下のファイルを作成します。

```text
years/2028.html
```

年度、開催日、会場、競技内容、スケジュール、結果などを更新します。

### 2. 英語版

`en/years/template.html` をコピーし、対応する英語版ページを作成します。

```text
en/years/2028.html
```

### 3. トップページへの追加

日本語版 `index.html` と英語版 `en/index.html` の年度別大会ページに、新年度のカードを追加します。

### 4. ナビゲーション・言語切替の確認

日本語版と英語版のページ間で、JA / ENリンクが正しく対応していることを確認します。

## ローカル確認

リポジトリのルートディレクトリで、以下のコマンドを実行します。

```bash
python3 -m http.server 8000
```

ブラウザで以下を開いて表示を確認します。

```text
http://localhost:8000/
```

英語版は以下から確認できます。

```text
http://localhost:8000/en/
```

年度別ページの例：

```text
http://localhost:8000/years/2026.html
http://localhost:8000/en/years/2026.html
```

ローカルファイルを直接 `file://` で開くのではなく、ローカルHTTPサーバー経由で確認することを推奨します。

## 更新時の確認項目

* 日本語版と英語版の内容が対応しているか
* 年度、開催日、会場等が正しいか
* ページ内ナビゲーションが正しく動作するか
* JA / EN切替リンクが正しいか
* 画像のパスが正しいか
* PDF等の資料リンクが正しいか
* PC・スマートフォンの両方でレイアウトが崩れていないか

## GitHub Pagesへの反映

変更内容を `main` ブランチへ反映すると、GitHub Pagesの設定に基づいて公開サイトへ反映されます。

公開前にローカル環境で表示・リンクを確認してください。

## 参考リンク

* [RoboCup @Space JP Website](https://robocupatspacejp.github.io/)
* [RoboCup JapanOpen](https://www.robocup.or.jp/)
