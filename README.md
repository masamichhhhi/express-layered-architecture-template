# express+typescriptで作るレイヤードアーキテクチャのテンプレート

## 構成
- controller: リクエストを受け取る。applicationに依存
- application: アプリケーションのビジネスロジック, domainに依存
- domain/model: ドメインモデル。判断・加工・計算のビジネスロジックはここ。
- domain/repository: infrastructureのインターフェースだけ定義する。
- infrastructure: DB接続などの実装はここ。domain/repositoryに依存する。

eslint
```bash
# 自動修正
$ npm run eslint -- --fix --ext '.js,.ts' ./src/**"
```