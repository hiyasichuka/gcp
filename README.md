# Google Cloud Platform

## サービス一覧

### コンピューティング

- Compute Engine
  - いわゆるEC2やAzureVMと同じコンピューティングリソース

- Kubernetes Engine
  - k8sクラスタをワンクリックするだけですぐに作業を開始できる
  - さらに最大 15,000 ノードまでスケールアップ可能
  - マルチゾーンクラスタとリージョンクラスタを含む高可用性のコントロールプレーンを活用できる
  - コンテナイメージの脆弱性スキャンやデータ暗号化などがデフォルトで組み込まれた安全設計

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
  - データは「ドキュメント」に格納し、それが「コレクション」にまとめられます。
  - ドキュメント＝JSONのイメージ
  - コレクション＝コンテナのイメージ
  - コレクションにはドキュメントだけが含まる。コレクションに値を持つ生のフィールドを直接含めることはできず、他のコレクションを含めることもできない

- Cloud Storage
  - オブジェクトストレージ（AWS S3 ,Azure Blob Storageみたいなやつ） 

### データベース

- BigTable
  - [マネージド（＝サーバレスではない）](https://cloud.google.com/blog/ja/topics/developers-practitioners/serverless-vs-fully-managed-whats-difference)
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
  - サーバレス（サーバー管理が不要で 個別のインスタンスを見る必要なし）
- SQL
  - マネージド（一部作業が必要）

### 統合

- API Gateway
- Cloud Scheduler
- Cloud Tasks
- Workflow

### ネットワーク

- VPC Network

### CI/CD

- Cloud Build
 - サーバーレス CI / CD プラットフォーム
- Cloud Deploy
 - GKE、Cloud Run、Anthos に継続的デリバリー
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
  - マネージド（サーバレスではない）
  - Apache Spark、Apache Flink、Prestoをはじめ、30 以上のオープンソースやフレームワークを実行するための、フルマネージドでスケーラビリティの高いサービス
- Dataperp
  - GCP 管理コンソールから、GUI操作でデータの抽出、加工、ロードが簡単に行える、データプレパレーションツール
  - サーバーレスで、規模に関係なく稼働する。
- Pub/Sub
  - パブリッシャー/サブスクライバーの略で、これを使用するとサービスが100ミリ秒程度のレイテンシで非同期に通信できる
  - データを取り込んで配布するためのストリーミング分析とデータ統合パイプラインに使用される
  - CloudStorageに画像を保存して、Pub/Sub経由でFunctionのパターンもある
- Dataflow
  - サーバーレスかつ高速で、費用対効果の高い、統合されたストリームデータ処理とバッチデータ処理を実現するサービス
  - Apache Beam PubsubIOを使用している場合、DataflowはデフォルトでこのIDを使用してメッセージの重複除去を実行できる
  - そのため、このような Pub/Sub からの同じメッセージの再配信に起因する重複は、Dataflow で除外できます
- BigQuery
  - サーバレス
  - ビジネスのアジリティに対応して設計されたサーバーレスでスケーラビリティと費用対効果に優れたマルチクラウドデータウェアハウスです。
  - ANSI SQL を使用してペタバイト規模のデータを極めて高速に分析でき、運用のオーバーヘッドは発生しません。
- Data Catalog
  - フルマネージドでスケーラビリティの高いデータ検出およびメタデータ管理サービス
- Data Fusion
  - データパイプラインを迅速に構築し管理するための、フルマネージデータ統合サービス
  - データのクレンジング、準備、ブレンド、転送、変換を行う 

# 試験ガイド

[Associate Cloud Engineer](https://cloud.google.com/learn/certification/cloud-engineer?hl=ja)
[Professional Data Engineer](https://cloud.google.com/certification/guides/data-engineer?hl=ja)
[Professional Cloud Developer](https://cloud.google.com/certification/guides/cloud-developer?hl=ja)

