# Google Cloud Platform

## サービス一覧


### コンピューティング

- Compute Engine
  - いわゆるEC2やAzureVMと同じコンピューティングリソース

- Kubernetes Engine
  - k8sクラスタをワンクリックするだけですぐに作業を開始できる
  - さらに最大 15,000 ノードまでスケールアップ可能
  - マルチゾーンクラスタとリージョンクラスタを含む高可用性のコントロールプレーンを活用できる
  - コンテナ イメージの脆弱性スキャンやデータ暗号化などがデフォルトで組み込まれた安全設計

- VMware Engine
  - すでに構築済のオンプレVMwareアプリケーションをモダナイズするときに使う

### サーバレス

- Cloud Run
  - コンテナベースのサーバーレスコンピューディングサービス
  - 自作コンテナを、Googleのサーバー上で良しなに動かすことができる
  - http(s) のWebサイト/APIを手軽に作れる
  - 自動でスケーリングしてくれる

- Cloud Functions
  - 必要に応じて必要な機能だけ呼び出すことができる
  - イベントを起点としてサーバーサイドロジックを実行する
  - サーバー管理不要、従量課金、イベント駆動
  - より簡単に使えるのがCloud Functions、柔軟性・拡張性がより高いのがCloud Run

- App Engine
  - PaaS
  - 自作アプリをGCP管理インフラに簡単にデプロイできる
  - AWSのElastic Beanstalkと同じ部類

### ストレージ

Filestore
Cloud Storage
Data Transfer

### データベース

Bigtable
Datastore
Firestore
Memorystore
Spanner
SQL

### 統合

API Gateway
Cloud Scheduler
Cloud Tasks
Workflow

### ネットワーク

VPC Network
その他諸々

### CI/CD

Cloud Build
Cloud Deploy
Container Registry
Artifact Registry
Source Repositories

### ビッグデータ

Composer
Dataproc
Pub/Sub
Dataflow
BigQuery
Data Catalog
Data Fusion

# 試験ガイド

[Professional Data Engineer](https://cloud.google.com/certification/guides/data-engineer?hl=ja)
[Professional Cloud Developer](https://cloud.google.com/certification/guides/cloud-developer?hl=ja)
