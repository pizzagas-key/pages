# 音MAD 月別流行レポート

ニコニコ動画の「音MAD」タグ付き動画（2007年〜）を月ごとに集計し、
その月に急増したタグ（バーストスコア）から「何が流行ったのか」を
素材・曲・イベントに分けてまとめた静的HTMLレポートです。

## 閲覧方法

### GitHub Pages（推奨）

リポジトリの **Settings → Pages → Build and deployment** で
`Deploy from a branch` / ブランチ `main` / フォルダ `/ (root)` を選んで保存すると、
数分後に次のURLで閲覧できます。

```
https://pizzagas-key.github.io/pages/nico-report/
```

### Pages を使わない場合

raw.githack.com 経由でも表示できます。

- https://raw.githack.com/pizzagas-key/pages/main/nico-report/index.html

## 内容

| ファイル | 内容 |
|---|---|
| `index.html` | 目次（年ごとのリンク） |
| `2007.html` 〜 `2026.html` | 各年の月別レポート。要約文・急上昇タグの実データ表（素材/原曲/その他に分割表記）・再生数上位動画（1位は埋め込みプレイヤー、2〜5位はサムネイルカード） |

タグはニコニコ大百科に記事が存在するものにリンクを設定しています。

## データについて

- 出典: [ニコニコ動画スナップショット検索API v2](https://snapshot.search.nicovideo.jp/api/v2/snapshot/video/contents/search)
- 再生数・順位は収集時点（2026年6月）のスナップショットです
- バーストスコア = 当月件数 ÷ (過去6ヶ月平均 + 3)
- 2024年6月中旬〜8月上旬はニコニコ動画のサービス停止期間のためデータがありません
- 生成: otomad-tag-stats プロジェクト（ローカル）の `export_report.py` による自動生成
