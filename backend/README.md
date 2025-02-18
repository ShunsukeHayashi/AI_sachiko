# バックエンド

幸子（サーチコネクション）のバックエンドアプリケーション

## 技術スタック

- Node.js
- Express.js
- Elasticsearch
- Redis (キャッシュ)

## ディレクトリ構造

```
src/
  ├── api/          - APIルートハンドラ
  ├── config/       - 設定ファイル
  ├── services/     - ビジネスロジック
  ├── models/       - データモデル
  ├── utils/        - ユーティリティ関数
  └── middleware/   - ミドルウェア
```

## セットアップ

```bash
# 依存関係のインストール
npm install

# 開発サーバーの起動
npm run dev

# テストの実行
npm test

# リントの実行
npm run lint
```

## 環境変数

`.env`ファイルを作成し、以下の環境変数を設定してください：

```
PORT=3000
ELASTICSEARCH_URL=http://localhost:9200
REDIS_URL=redis://localhost:6379
NODE_ENV=development
```

## 開発ガイドライン

- コードスタイルはESLintとPrettierに従う
- ユニットテストは必須
- APIドキュメントはSwagger/OpenAPIで管理