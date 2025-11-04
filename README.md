# BookManager(書籍管理アプリ)

### なぜこのアプリを作成したのか？
- 書籍を紙や電子で購入していると自分の手持ちの本を忘れてしまうことがある。
- このアプリに登録することで自分が今まで購入した本の表紙の一覧で確認することができる。→間違えて同じ本を買わないで済む
- 本を読んだ感想やメモも同時に保存しておくことができる。

### 概要
- 書籍を一括管理できるWebアプリ
- ユーザーごとに書籍の登録とメモが可能

### 機能一覧
-   ログイン機能 
-   Google Books API を用いた書籍検索機能
-   Markdown形式の読書記録登録・編集・削除
-   表紙画像付きの書籍一覧表示
-   SQLite3によるローカルDB管理

### デモ動画
[![](http://markdown-videos-api.jorgenkh.no/youtube/lPSApYnldCg)](https://youtu.be/lPSApYnldCg)

### BookManager_仕様書
- [仕様書](BookManager_仕様書.pdf)

### 製作期間と製作時期
- 大学の講義内で期末課題として製作
- 実装期間１週間

### 使用技術・言語・ライブラリ
- HTML
- CSS
- JavaScript
- Node.js...21.5.0
- Prisma（SQLite3）...5.8.1
- Express...4.17.1
- Markdown-it

### 特徴や工夫点
- GoogleBooksAPIを使用することで書籍の表紙画像を表示することができるようにした
- メモはMarkdown記法で書き込みが可能

### 問題点や今後の展望
- 書籍の一覧性を向上させるためにUIの見直しが必要
- GoogleBooksAPIだけでは取得できる書籍の量が少ないため、別の書籍データ取得用APIを費用することで網羅率を上げたい
- MVCモデル学習のためにLaravelでプログラムを置き換えたい

---

## 実行方法

### 1\. リポジトリのクローン

```bash
git clone https://github.com/yourusername/bookmanager.git
cd bookmanager
```

### 2\. 依存関係のインストール

```bash
npm install
```

### 3\. データベースのセットアップ

PrismaでSQLiteデータベースを作成します。

```bash
npx prisma migrate dev --name init
```

デフォルトで `prisma/schema.prisma` の設定に基づき、`dev.db` が生成されます。

### 4\. 開発サーバーの起動

```bash
npm start
```

もしくは

```bash
node src/index.js
```

ブラウザで以下のURLを開きます：  
http://localhost:3000

---

## ディレクトリ構成

```csharp
BookManager/
├── src/
│   ├── controllers/     # ロジック制御
│   ├── routes/          # ルーティング
│   ├── views/           # EJSテンプレート
│   ├── index.js         # エントリーポイント
│   └── prisma/          # DBスキーマ設定
├── public/              # 静的ファイル（CSS/画像など）
├── package.json
└── README.md
```

---


    
