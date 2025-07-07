---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/data-engineering
---
# [[データエンジニアリング MOC]]

## 1. [[データエンジニアリング入門 MOC]]
   - **データエンジニアリングとは**
      - [[データエンジニアリングの定義 (信頼性が高く効率的なデータパイプラインを構築・維持・管理する実践)]]
      - [[データエンジニアリングの目的 (分析や機械学習に利用可能なデータを、適切な形式で適切な場所に提供する)]]
      - [[なぜデータエンジニアリングが重要か (データ活用の土台、"Garbage In, Garbage Out"の防止)]]
   - **データエンジニアの役割と責任**
      - `[[データパイプラインの設計、構築、運用]]`
      - `[[データストレージシステムの管理]]`
      - `[[データ品質と信頼性の確保]]`
      - `[[スケーラビリティとパフォーマンスの最適化]]`
      - `[[データガバナンスとセキュリティの実践]]`
   - **関連職種との役割分担**
      - `[[データエンジニア vs. データアナリスト]]`
      - `[[データエンジニア vs. データサイエンティスト]]`
      - `[[データエンジニア vs. ソフトウェアエンジニア]]`
      - `[[データエンジニア vs. データベース管理者 (DBA)]]`
      - `[[アナリティクスエンジニアの登場]]`
   - **[[データライフサイクルとデータエンジニアリング MOC]]**
      - `[[データ生成 (Generation)]]`
      - `[[データ収集 (Collection / Ingestion)]]`
      - `[[データ処理 (Processing)]]`
      - `[[データ保存 (Storage)]]`
      - `[[データ管理 (Management)]]`
      - `[[データ分析 (Analysis)]]`
      - `[[データ可視化 (Visualization)]]`
   - **モダンデータエンジニアリングの原則**
      - `[[クラウドネイティブ]]`
      - `[[ELTパラダイムの採用]]`
      - `[[コードとしてのインフラ/パイプライン (IaC, Pipeline as Code)]]`
      - `[[自動化とテスト]]`
      - `[[分離とモジュール性 (Modern Data Stack)]]`
   - **データエンジニアリングの学習ロードマップ (例)**

## 2. [[データモデリング (Data Modeling) MOC]]
   - **データモデリングの重要性** (分析のしやすさ、パフォーマンス、保守性)
   - **データモデリングのレベル**
      - `[[概念データモデル (Conceptual Data Model)]]`
      - `[[論理データモデル (Logical Data Model)]]`
      - `[[物理データモデル (Physical Data Model)]] `
   - **リレーショナルデータベースのモデリング**
      - **[[正規化 (Normalization)]]** (第一〜第五正規形、ボイス・コッド正規形)
         - `[[正規化の目的 (データ冗長性の排除、更新時異常の防止)]]`
      - **[[非正規化 (Denormalization)]]**
         - `[[非正規化の目的 (クエリパフォーマンスの向上)]]`
         - `[[正規化と非正規化のトレードオフ]]`
   - **データウェアハウスのモデリング**
      - **[[スタースキーマ (Star Schema) MOC]]**
         - `[[ファクトテーブル (Fact Table)]]`
         - `[[ディメンションテーブル (Dimension Table)]]`
         - `[[スタースキーマの利点と欠点]]`
      - **[[スノーフレークスキーマ (Snowflake Schema) MOC]]**
         - `[[ディメンションテーブルの正規化]]`
         - `[[スノーフレークスキーマとスタースキーマの比較]]`
      - **[[ギャラクシースキーマ (Galaxy Schema / Fact Constellation)]]**
      - **[[ slowly changing dimensions (SCD) の種類と実装]]** (Type 1, 2, 3, 4, 6)
   - **[[データヴォールト (Data Vault) モデリング MOC]]**
      - `[[ハブ (Hub), リンク (Link), サテライト (Satellite)]]`
      - `[[データヴォールトの目的 (監査可能性、拡張性)]]`
   - **スキーマ定義と進化 (Schema Evolution)**
      - [[スキーマオンリード (Schema-on-Read) vs. スキーマオンライト (Schema-on-Write)]]
      - [[スキーマ変更への対応戦略]]

## 3. [[データ収集とインジェスト (Data Collection and Ingestion) MOC]]
   - **データインジェストのパターン**
      - `[[バッチインジェスト (Batch Ingestion)]]`
      - `[[マイクロバッチインジェスト (Micro-batch Ingestion)]]`
      - `[[ストリーミングインジェスト (Streaming Ingestion)]]`
   - **データソース別の収集方法**
      - `[[リレーショナルデータベースからのデータ収集]]`
         - `[[JDBC/ODBC経由のバッチ取得]]`
         - **[[CDC (Change Data Capture) MOC]]** (Debezium, Maxwell's demonなど)
      - `[[Web APIからのデータ取得]]`
      - `[[ファイル (CSV, JSON, XML, Log) のインジェスト]]`
      - `[[イベントストリームのインジェスト (Kafka, Kinesisなど)]]`
   - **データインジェストツール**
      - `[[Fluentd / Fluent Bit]]` (ログ収集)
      - `[[Apache Sqoop]]` (Hadoopエコシステム)
      - `[[SaaSベースのデータインテグレーションツール]]`
         - `[[Fivetran]]`
         - `[[Stitch]]`
         - `[[Airbyte]]` (オープンソース)
   - **データインジェスト層の設計** (スケーラビリティ、耐障害性、監視)

## 4. [[ETL / ELT パイプライン MOC]]
   - **[[ETL (Extract, Transform, Load) MOC]]**
      - `[[ETLのプロセスフロー (抽出→変換→ロード)]]`
      - `[[ETLの伝統的なアーキテクチャとツール (Informatica, Talendなど)]]`
      - `[[ETLのユースケースと課題]]`
   - **[[ELT (Extract, Load, Transform) MOC]]**
      - `[[ELTのプロセスフロー (抽出→ロード→変換)]]`
      - `[[ELTが主流になった背景 (クラウドDWHの台頭)]]`
      - **[[dbt (data build tool) MOC]]**
         - `[[dbtの役割 (データウェアハウス内でのT(変換)に特化)]]`
         - `[[SQLベースのデータ変換、テスト、ドキュメンテーション]]`
         - `[[アナリティクスエンジニアリングとdbt]]`
   - **[[ETL vs. ELT の比較 MOC]]**
      - `[[処理場所 (中間サーバ vs. DWH)]]`
      - `[[データ量と柔軟性]]`
      - `[[ツールとスキルセット]]`
   - **[[リバースETL (Reverse ETL) MOC]]**
      - `[[DWHから業務システム (Salesforce, Marketoなど) へのデータ同期]]`
   - **データパイプラインの設計**
      - `[[冪等性 (Idempotency) の確保]]`
      - `[[エラーハンドリングと再試行ロジック]]`
      - `[[依存関係の管理]]`
      - `[[モニタリングとアラート]]`
   - **[[(オプション) Apache NiFiによるデータフロー自動化]]**

## 5. [[データストレージとウェアハウジング MOC]]

### 5.1. [[データウェアハウス (DWH - Data Warehouse) MOC]]
   - [[DWHの定義と目的 (分析目的で統合・整理された時系列データのリポジトリ)]]
   - **DWHの4つの特性 (S.I.T.V)**
      - `[[主題指向 (Subject-Oriented)]]`
      - `[[統合 (Integrated)]]`
      - `[[時系列 (Time-Variant)]]`
      - `[[不揮発性 (Non-Volatile)]]`
   - **クラウドデータウェアハウス**
      - `[[Amazon Redshift MOC]]`
      - `[[Google BigQuery MOC]]`
      - `[[Snowflake MOC]]`
      - `[[クラウドDWHの特徴 (コンピューティングとストレージの分離、スケーラビリティ)]]`
   - **DWHのアーキテクチャ** (インプレス、エンタープライズ、データマート)

### 5.2. [[データレイク (Data Lake) MOC]]
   - [[データレイクの定義と目的 (構造化・半構造化・非構造化データをそのままの形式で保存するリポジトリ)]]
   - **データレイクの特性**
      - `[[スキーマオンリード (Schema-on-Read)]]`
      - `[[高い柔軟性とスケーラビリティ]]`
   - **データレイクの課題**
      - `[["データスワンプ (Data Swamp)"化のリスク]]`
      - `[[データガバナンスとセキュリティの複雑性]]`
   - **データレイクの構築** (AWS S3, Azure Data Lake Storage, Google Cloud Storage)

### 5.3. [[データレイクハウス (Data Lakehouse) MOC]]
   - [[データレイクハウスの定義 (データレイクの柔軟性とDWHの管理機能・性能を両立)]]
   - **データレイクハウスを支える技術**
      - `[[オープンなテーブルフォーマット (Delta Lake, Apache Iceberg, Apache Hudi)]]`
         - `[[ACIDトランザクション、タイムトラベル、スキーマ進化の実現]]`
      - `[[クエリエンジン (Spark, Trino/Presto)]]`
   - `[[Databricks Lakehouse Platformの概要]]`
   - `[[SnowflakeのUnistoreとデータレイクハウス]]`

### 5.4. [[データストレージのファイルフォーマット MOC]]
   - **行指向フォーマット**
      - `[[CSV, TSV, JSON]]` (可読性、柔軟性)
   - **列指向フォーマット (カラムナフォーマット)**
      - **[[Apache Parquet MOC]]**
      - **[[Apache ORC (Optimized Row Columnar) MOC]]**
      - `[[列指向フォーマットの利点 (分析クエリの高速化、高い圧縮率)]]`
   - **[[Apache Avro MOC]]** (スキーマ埋め込み、行指向、スキーマ進化に強い)
   - **フォーマット選択の基準**

## 6. [[データ処理システム MOC]]

### 6.1. [[バッチ処理 (Batch Processing) MOC]]
   - [[バッチ処理の定義 (データをまとめて一括処理)]]
   - **[[Apache Spark MOC]]**
      - `[[Sparkのアーキテクチャ (Driver, Executor, Cluster Manager)]]`
      - `[[RDD (Resilient Distributed Dataset)]]`
      - `[[DataFrame と DataSet API]]`
      - `[[遅延評価 (Lazy Evaluation) とDAG (有向非巡回グラフ)]]`
      - `[[Spark SQL]]`
      - `[[PySpark (Python API)]]`
   - **[[Hadoop MapReduce MOC]]** (歴史的意義と基本概念)
      - `[[MapperとReducer]]`

### 6.2. [[ストリーム処理 (Stream Processing) MOC]]
   - [[ストリーム処理の定義 (データを発生と同時に継続的に処理)]]
   - **ストリーム処理の基本概念**
      - `[[イベント時間 (Event Time) vs. 処理時間 (Processing Time)]]`
      - `[[ウィンドウ処理 (Tumbling, Sliding, Session Windows)]]`
      - `[[ウォーターマーク (Watermarks)]]` (遅延データの扱い)
      - `[[状態管理 (Stateful Streaming)]]`
   - **ストリーム処理フレームワーク**
      - **[[Apache Spark Structured Streaming MOC]]** (マイクロバッチ)
      - **[[Apache Flink MOC]]** (ネイティブストリーム処理)
      - **[[Apache Kafka Streams MOC]]** (Kafkaと統合されたライブラリ)
   - **ストリーム処理のユースケース** (リアルタイムモニタリング、不正検知、リアルタイム推薦)

### 6.3. [[データ処理アーキテクチャ MOC]]
   - **[[ラムダアーキテクチャ (Lambda Architecture)]]**
      - `[[バッチ層、スピード層、サービング層]]`
      - `[[利点と複雑性]]`
   - **[[カッパアーキテクチャ (Kappa Architecture)]]**
      - `[[ストリーム処理に一本化]]`
      - `[[ラムダアーキテクチャとの比較]]`

## 7. [[ワークフローオーケストレーション MOC]]
   - [[オーケストレーションの必要性 (複雑なデータパイプラインの管理)]]
   - **[[Apache Airflow MOC]]**
      - `[[Airflowのコアコンセプト (DAG, Operator, Sensor, Hook, XCom)]]`
      - `[[PythonによるDAG定義]]`
      - `[[Airflowのアーキテクチャ (Scheduler, Webserver, Executor, Worker)]]`
   - **モダンなオーケストレーションツール**
      - `[[Prefect MOC]]`
      - `[[Dagster MOC]]` (データアウェアなオーケストレータ)
   - **[[(オプション) Luigi, Argo Workflows]]**
   - **オーケストレーションツールの選定基準**

## 8. [[データ品質とガバナンス MOC]]

### 8.1. [[データ品質 (Data Quality) MOC]]
   - **データ品質の6つの側面**
      - `[[完全性 (Completeness)]]`
      - `[[一意性 (Uniqueness)]]`
      - `[[適時性 (Timeliness)]]`
      - `[[妥当性 (Validity)]]`
      - `[[正確性 (Accuracy)]] `
      - `[[一貫性 (Consistency)]]`
   - [[データプロファイリングツールの活用]]
   - **[[データ品質テストと監視]]**
      - `[[dbt tests]]`
      - `[[Great Expectations]]`
      - `[[パイプラインへのテスト組み込み]]`

### 8.2. [[データガバナンス (Data Governance) MOC]]
   - [[データガバナンスの定義と目的]]
   - [[データスチュワードシップと役割分担]]
   - **[[メタデータ管理とデータカタログ]]**
      - `[[技術的メタデータ、ビジネスメタデータ、運用メタデータ]]`
      - `[[データカタログツール (Amundsen, DataHub, Alation, Collibra)]]`
   - **[[データリネージ (Data Lineage)]]**
      - `[[データリネージの重要性 (トレーサビリティ、影響分析)]]`
   - **[[アクセスコントロールとデータセキュリティ]]**
   - **[[データプライバシーと法規制 (GDPR, CCPA)]]** (再掲・データエンジニアリング文脈)

## 9. [[データエンジニアリングのインフラとツール MOC]] (再掲・集約)
   - **[[クラウドデータプラットフォームの活用]]** (AWS, GCP, Azureの主要サービス)
   - **[[コンテナ化 (Docker) とオーケストレーション (Kubernetes)]]** (データパイプラインでの利用)
   - **プログラミング言語**
      - `[[SQL (データエンジニアリングにおける最重要言語)]]`
      - `[[Python (スクリプティング、PySpark, Airflowなど)]]`
      - `[[JVM言語 (Java, Scala) (Spark, Flink, Kafkaなど)]]`
   - **[[Infrastructure as Code (IaC) for Data Platforms]]** (Terraform)
   - **[[CI/CD for Data Pipelines (DataOps) MOC]]**
      - `[[データパイプラインのテスト (ユニット、インテグレーション)]]`
      - `[[ステージング環境の構築]]`
      - `[[パイプラインの自動デプロイ]]`

## 10. [[モダンデータスタック (The Modern Data Stack) MOC]]
   - [[モダンデータスタックの概念 (ELT中心、クラウドネイティブ、分離・専門化されたツール群)]]
   - **構成要素の例**
      - `[[データインジェスト: Fivetran, Airbyte]]`
      - `[[データウェアハウス: Snowflake, BigQuery, Redshift]]`
      - `[[データ変換: dbt]]`
      - `[[BI/分析: Looker, Tableau, Power BI]]`
      - `[[リバースETL: Census, Hightouch]]`
      - `[[オーケストレーション: Airflow, Prefect, Dagster]]`
   - [[モダンデータスタックの利点と課題]]

## 11. [[データエンジニアリングのベストプラクティスとアンチパターン MOC]]
   - **ベストプラクティス**
      - `[[コードとして全てを管理する (SQL, パイプライン定義, IaC)]]`
      - `[[テストを徹底する]]`
      - `[[ドキュメントを整備する]]`
      - `[[モニタリングとアラートを設定する]]`
      - `[[スケーラビリティを考慮して設計する]]`
      - `[[コストを意識する]]`
   - **アンチパターン**
      - `[[データスワンプの構築]]`
      - `[[過度な最適化または最適化の欠如]]`
      - `[[テストとモニタリングの軽視]]`
      - `[[パイプラインの過度な複雑化 ("スパゲッティパイプライン")]]`
      - `[[セキュリティとガバナンスの無視]]`

## 12. [[データエンジニアリングの将来とトレンド MOC]]
   - **[[Data Mesh MOC]]**
      - `[[Data Meshの4つの原則 (ドメイン指向の所有権, 製品としてのデータ, セルフサービスデータプラットフォーム, フェデレーション計算ガバナンス)]]`
   - **[[ストリーミング処理の普及とリアルタイム分析]]**
   - **[[アナリティクスエンジニアリングの台頭]]**
   - **[[MLOpsとDataOpsの統合]]**
   - **[[データエンジニアの役割のさらなる進化]]**
