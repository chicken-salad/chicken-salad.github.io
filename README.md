# chicken-salad.github.io

有里 勇輝 (Yuki Arisato) の個人ポートフォリオサイト。
東京都立駒込病院 初期研修医、東京大学医学部附属病院 感染症内科 届け出研究員、Quadka 共同創業者としての経歴と業績を、学術エディトリアル調のデザインで公開する単一ページサイト。

## 構成

```
.
├── index.html   — サイト本体（CSS / JavaScript はすべて inline）
└── README.md    — このファイル
```

外部依存は Google Fonts のみ（Fraunces / Manrope / JetBrains Mono / Noto Serif JP / Noto Sans JP）。
ビルドプロセス・サーバーサイド処理は一切なし。

## ページ構成

- **Hero** — 氏名・所属・タグライン・コンタクトリンク
- **01 / Profile** — 経歴の概要
- **02 / Career** — 時系列の歩み
- **03 / Highlights** — 主な受賞・実績
- **04 / Publications** — 査読付き論文・学会発表

## デプロイ（GitHub Pages）

### 1. リポジトリ作成

GitHub で `chicken-salad.github.io` という名前のリポジトリを新規作成（既に存在する場合はそこにファイルを置く）。

### 2. ファイルを push

```bash
git init
git add index.html README.md
git commit -m "Initial site"
git branch -M main
git remote add origin https://github.com/chicken-salad/chicken-salad.github.io.git
git push -u origin main
```

### 3. GitHub Pages を有効化

リポジトリの **Settings → Pages** で `Branch: main / (root)` を選択して保存。
数十秒〜数分後、`https://chicken-salad.github.io/` で公開される。

### 4. (オプション) 独自ドメイン

`Settings → Pages → Custom domain` にドメインを入力すると、リポジトリ直下に `CNAME` ファイルが生成される。レジストラ側で DNS 設定（A レコード4本、または www に対する CNAME）が必要。
完了後 `Enforce HTTPS` を有効化する。

## カスタマイズ

| 何を変えたいか | どこを編集するか |
|---|---|
| 配色 | `<style>` 冒頭の `:root { --bg, --ink, --accent ... }` |
| フォント | `:root` の `--serif`, `--sans`, `--mono` |
| 経歴を追加 | `<section id="career">` 内に `.timeline-item` を追加 |
| 論文を追加 | `<section id="publications">` 内の対応する `<ol class="pub-list">` に `<li>` を追加 |
| 連絡先 | `.hero-cta` と `footer .links` の2箇所 |
| メタ情報 (SEO) | `<head>` 内の `<title>`, `<meta description>`, `og:*` |

## 連絡先

- Email: yukiarigamerusa@gmail.com
- X: [@yoshi_NOTCH2](https://x.com/yoshi_NOTCH2)
- GitHub: [chicken-salad](https://github.com/chicken-salad)
