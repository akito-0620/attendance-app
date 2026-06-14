# attendance-app

スマートフォン向けの出席管理 PWA（Progressive Web App）です。インストール不要でブラウザから利用でき、オフラインでも動作します。

## 機能

- 出席・欠席・遅刻などの状態を記録・管理
- iOS / Android 対応のモバイルファーストデザイン
- オフライン対応（Service Worker によるキャッシュ）
- ホーム画面へのインストール対応

## 使い方

### ブラウザで開く

`index.html` をブラウザで直接開くか、ローカルサーバーで配信します。

```bash
# Python の簡易サーバーを使う例
python -m http.server 8080
```

ブラウザで `http://localhost:8080` にアクセス。

### PWA としてインストール

スマートフォンのブラウザで開き、「ホーム画面に追加」からインストールするとアプリとして起動できます。

## ファイル構成

```
attendance-app/
├── index.html      # メインアプリ（UI・ロジック）
├── manifest.json   # PWA マニフェスト
└── sw.js           # Service Worker（オフライン対応）
```

## 技術スタック

- HTML / CSS / JavaScript（ビルド不要）
- PWA（Progressive Web App）
- Service Worker によるオフラインキャッシュ