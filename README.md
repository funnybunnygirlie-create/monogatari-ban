# 物語盤（MONOGATARI-BAN）

小説の構想を付箋で並べるボードアプリ。ダークテーマ・単一HTMLの静的サイト（バックエンドなし）。
保存はブラウザの `localStorage`＋任意で Google Drive（アプリ専用フォルダ）に同期します。

## ローカルで動かす

```bash
python -m http.server 5173
```

ブラウザで `http://localhost:5173` を開く。

## Google Drive 同期の設定

`index.html` 冒頭の `GOOGLE_CLIENT_ID` に、Google Cloud で作成した OAuth クライアントID を設定します。
スコープは `drive.appdata`（アプリ専用の隠しフォルダ）のみ。公開URLは Google Cloud の
「承認済み JavaScript 生成元」に登録する必要があります。

## ファイル

- `index.html` … 本体（これが公開される）
- `novel-board.html` … 元のプロトタイプ（参考用）
