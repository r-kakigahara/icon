# icon

社内アプリで使うアイコン・画像の公開置き場。
Google Chat Webhook のアバターなど、**インターネット公開 URL が必要な画像**をここで管理する。

## URL の使い方

ファイルは raw URL で直接参照できる:

```
https://raw.githubusercontent.com/r-kakigahara/icon/main/<フォルダ>/<ファイル名>
```

例: `https://raw.githubusercontent.com/r-kakigahara/icon/main/nipo/nipo-avatar-c-poko.png`

## 運用ルール

- アプリ・用途ごとにフォルダを切る (`nipo/` など)
- **画像を差し替えるときはファイル名を変える** (Google 側にキャッシュされるため、同名上書きでは反映されないことがある)
- `.png` が配信用 (アバターは 512×512 正方形・円形トリミング前提)、`.svg` は編集用マスター
- 公開リポジトリなので、社外秘情報を含む画像は置かない

## 収録一覧

### nipo/ — NIPO (製造2部 日報システム)

Google Chat「NIPO からのお知らせ」Webhook アバター候補。円形クロップ・36px 表示前提で設計。

| ファイル | 内容 |
|---|---|
| `nipo-avatar-a-n.png` | 案A: ブランド N マーク (Editorial Light / Zinc-900 + 白N) |
| `nipo-avatar-b-n-dot.png` | 案B: N マーク + 通知ドット (#06b6d4) |
| `nipo-avatar-c-poko.png` | 案C: サポートドローン「ポコ」(アプリ内 PokoFace 準拠) |
| `nipo-avatar-d-face.png` | 案D: ポコ顔スクリーンのクローズアップ |

### zairyou/ — 材料管理システム (製造1部)

Google Chat「材料管理システム」Webhook アバター候補。円形クロップ・36px 表示前提で設計。背景色はアプリのアクセント色 `#0E7DA8`。文字は Noto Sans JP Black (OFL) をアウトライン化しており、`.svg` の表示にフォントは不要。

| ファイル | 内容 |
|---|---|
| `zairyou-avatar-a-zairyou.png` | 案A (推奨): 「材料」2文字。24px でも読める |
| `zairyou-avatar-b-bag.png` | 案B: 材料袋 + 「材」。袋の形が分かるのは 48px 以上 |
| `zairyou-avatar-c-zai.png` | 案C: 「材」1文字 |

### shukka/ — 出荷管理ボード (生産管理部)

Google Chat「出荷管理ボード」Webhook アバター候補。円形クロップ・36px 表示前提で設計。背景はアプリアイコンと同じ紺〜青のグラデーション (`#1e3a5f` → `#1a56db`)。

| ファイル | 内容 |
|---|---|
| `shukka-avatar-a-truck-board.png` | 案A (推奨): MIETA+ の4枚タイルを荷台に積んだトラック。24px でもトラックと分かる |
| `shukka-avatar-b-truck.png` | 案B: 白いトラックだけ |
| `shukka-avatar-c-shukka.png` | 案C: 「出荷」2文字 (Noto Sans JP Black をアウトライン化)。材料管理の案A と形が似る |
| `shukka-avatar-d-mieta.png` | 案D: アプリアイコンと同じ MIETA+ シンボル。出荷の意味は形から読めない |

### chokusetsu-shogo/ — 監視アラート君 (直接出荷照合)

Google Chat「監視アラート君（直接出荷照合）」Webhook アバター候補。円形クロップ・36px 表示前提で設計。他のアイコンが青・水色・紺なので、警告色の黄と赤で一目で区別できるようにしている。文字は Noto Sans JP Black (OFL) をアウトライン化。

| ファイル | 内容 |
|---|---|
| `shogo-avatar-a-siren-shogo.png` | 案A (推奨): 目のある赤色回転灯 + 「照合」。36px でも回転灯と文字が読める |
| `shogo-avatar-b-siren.png` | 案B: 目のある赤色回転灯だけ。最も目立つが、照合の意味は形から読めない |
| `shogo-avatar-c-shogo-alert.png` | 案C: 赤地に「照合」+ 警告バッジ。材料管理の案A と構成が似る |
| `shogo-avatar-d-barcode-alert.png` | 案D: 警告三角 + バーコード。文字なし。36px ではバーコードが細かくなる |
