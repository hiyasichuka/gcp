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
  - ETL操作に使用。例えば、ストレージにファイルアップロードされると、クラウド関数がトリガーされ、コンテンツを変換してデータベースにアップロードすることができる
  - より簡単に使えるのがCloud Functions、柔軟性・拡張性がより高いのがCloud Run
  

- App Engine
  - PaaS
  - 自作アプリをGCP管理インフラに簡単にデプロイできる
  - AWSのElastic Beanstalkと同じ部類

### ストレージ

- Filestore
  - NoSQLクラウドデータベース 
- Cloud Storage
  - オブジェクトストレージ（AWS S3 ,Azure Blob Storageみたいなやつ） 

### データベース

- Bigtable
  - 最大99.999%の可用性で大規模な分析ワークロードにも運用ワークロードにも対応できるフルマネージドでスケーラブルな NoSQL データベース サービス。
  - Bigtable を使用すると、以下のすべてのタイプのデータを格納してクエリできます。
    * 時系列データ
    * マーケティング データ
    * 金融データ
    * IoT（モノのインターネット）データ
  - 大量の読み取りと書き込み用に最適化されており、アドホック分析には適していません。
- Datastore
  - アプリ開発を簡素化するように構築された NoSQLドキュメントデータベース。
  - BigQueryの外部データソースとしてはサポートされていない。
- Firestore
  - 柔軟でスケーラブルな NoSQL クラウド データベース
  - Datastoreの後継
- Memorystore
  - RedisとMemcached向けの、スケーラブルで安全かつ可用性の高いインメモリサービス
- Spanner
- SQL

### 統合

- API Gateway
- Cloud Scheduler
- Cloud Tasks
- Workflow

### ネットワーク

- VPC Network

### CI/CD

- Cloud Build
- Cloud Deploy
- Container Registry
- Artifact Registry
- Source Repositories

### ビッグデータ

- [Composer](https://cloud.google.com/composer)
  - Apache Airflowで構築された、フルマネージドのワークフローオーケストレーションサービス
  - Cloud Composerは、Apache Airflow で構築され、Python を使用して運用する、フルマネージドのワークフロー オーケストレーション サービス
  - GCPプロダクト※とのエンドツーエンドの統合により、ユーザーはパイプラインを自由かつ完全にオーケストレートできる
    - ※BigQuery、Dataflow、Dataproc、Datastore、Cloud Storage、Pub/Sub、AI Platform など
  - パイプラインがオンプレミスにあるか、複数のクラウドにまたがっているか、あるいは Google Cloud 内ですべて完結しているかにかかわらず、単一のオーケストレーションツールでワークフローを作成、スケジューリング、モニタリングできる
- Dataproc
  - Apache Spark、Apache Flink、Prestoをはじめ、30 以上のオープンソースやフレームワークを実行するための、フルマネージドでスケーラビリティの高いサービス
- Pub/Sub
- Dataflow
  - サーバーレスかつ高速で、費用対効果の高い、統合されたストリームデータ処理とバッチデータ処理を実現するサービス
- BigQuery
  - ビジネスのアジリティに対応して設計されたサーバーレスでスケーラビリティと費用対効果に優れたマルチクラウドデータウェアハウスです。
  - ANSI SQL を使用してペタバイト規模のデータを極めて高速に分析でき、運用のオーバーヘッドは発生しません。
  
- Data Catalog
- Data Fusion

# 試験ガイド

[Professional Data Engineer](https://cloud.google.com/certification/guides/data-engineer?hl=ja)
[Professional Cloud Developer](https://cloud.google.com/certification/guides/cloud-developer?hl=ja)


# エコシステム

- DataPrep
  - GCP 管理コンソールから、GUI 操作でデータの抽出、加工、ロードが簡単に行える、データプレパレーションツール
  - サーバーレスで、規模に関係なく稼働する。


