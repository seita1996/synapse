---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/aws-azure-gcp
---
## 1. [[クラウドコンピューティング入門 MOC]]
   - **クラウドコンピューティングとは**
      - [[クラウドコンピューティングの定義 (NISTによる5つの基本特性)]] (オンデマンドセルフサービス, 幅広いネットワークアクセス, リソースの共用, 迅速な伸縮性, 計測可能なサービス)
      - [[クラウドコンピューティングの利点 (俊敏性、弾力性、コスト効率、グローバル展開、イノベーション)]]
   - **[[サービスモデル (Service Models) MOC]]**
      - **[[IaaS (Infrastructure as a Service)]]** (仮想マシン、ストレージ、ネットワーク)
      - **[[PaaS (Platform as a Service)]]** (アプリケーション実行環境、データベース、開発ツール)
      - **[[SaaS (Software as a Service)]]** (エンドユーザー向けソフトウェア)
      - **[[FaaS (Function as a Service) / サーバーレスコンピューティング]]**
      - [[IaaS, PaaS, SaaSの比較と選択基準]]
   - **[[デプロイメントモデル (Deployment Models) MOC]]**
      - **[[パブリッククラウド (Public Cloud)]]**
      - **[[プライベートクラウド (Private Cloud)]]**
      - **[[ハイブリッドクラウド (Hybrid Cloud)]]**
      - **[[マルチクラウド (Multi-Cloud)]]**
   - **クラウドの主要な概念**
      - [[仮想化 (Virtualization) とハイパーバイザ]]
      - [[スケーラビリティ (Scalability - スケールアップ/ダウン vs. スケールアウト/イン)]]
      - [[可用性 (Availability) と信頼性 (Reliability)]]
      - [[耐障害性 (Fault Tolerance) と冗長性 (Redundancy)]]
      - [[弾力性 (Elasticity)]]
   - **[[クラウドの責任共有モデル (Shared Responsibility Model)]]**
      - [[クラウドプロバイダーとユーザーの責任範囲 (IaaS, PaaS, SaaSごとの違い)]]
   - **[[クラウドネイティブ (Cloud Native) の概念]]** (マイクロサービス、コンテナ、DevOps、CI/CD)

## 2. [[主要クラウドプロバイダーの比較 MOC]]
   - [[AWS vs. Azure vs. GCP: 概要と歴史、市場シェア]]
   - [[AWS vs. Azure vs. GCP: サービス名の対応表]]
   - [[AWS vs. Azure vs. GCP: 強みと弱み、主なターゲット市場]]
   - [[AWS vs. Azure vs. GCP: 料金体系の比較 (従量課金、リザーブドインスタンス、Savings Plans、コミットメント割引)]]
   - [[AWS vs. Azure vs. GCP: グローバルインフラストラクチャ (リージョン、アベイラビリティゾーン/ゾーン)]]
   - [[AWS vs. Azure vs. GCP: 管理コンソールとCLIの比較]]
   - [[AWS vs. Azure vs. GCP: コンプライアンスと認定]]
   - [[AWS vs. Azure vs. GCP: 無料利用枠の比較]]
   - [[マルチクラウド戦略におけるプロバイダー選択]]

## 3. [[Amazon Web Services (AWS) MOC]]

### 3.1. [[AWS入門と基本概念 MOC]]
   - [[AWSの概要と歴史]]
   - [[AWSアカウントの作成と管理]]
   - [[IAM (Identity and Access Management) の基本]] (詳細はセキュリティで)
   - [[AWSのグローバルインフラストラクチャ (リージョン, AZ, エッジロケーション)]]
   - [[AWS Management Console, AWS CLI, AWS SDKs]]

### 3.2. [[AWS コンピューティングサービス MOC]]
   - **[[Amazon EC2 (Elastic Compute Cloud) MOC]]**
      - `[[EC2インスタンスとは]]`
      - `[[インスタンスタイプファミリー (汎用, コンピューティング最適化, メモリ最適化, ストレージ最適化など)]]`
      - `[[Amazon Machine Image (AMI)]]`
      - `[[インスタンス購入オプション (オンデマンド, スポット, リザーブド, Savings Plans)]]`
      - `[[セキュリティグループ (Security Groups)]]`
      - `[[Elastic IPアドレス]]`
   - **[[Amazon EC2 Auto Scaling MOC]]** (自動スケーリング)
   - **[[Elastic Load Balancing (ELB) MOC]]** (ALB, NLB, GWLB)
   - **[[AWS Lambda MOC]]** (サーバーレスコンピューティング - FaaS)
      - `[[Lambda関数のトリガーと実行モデル]]`
      - `[[Lambdaのユースケースと制限]]`
   - **コンテナサービス**
      - `[[Amazon ECS (Elastic Container Service)]]` (コンテナオーケストレーション)
      - `[[Amazon EKS (Elastic Kubernetes Service)]]` (マネージドKubernetes)
      - `[[AWS Fargate]]` (サーバーレスコンテナエンジン)
      - `[[Amazon ECR (Elastic Container Registry)]]` (コンテナイメージリポジトリ)
   - `[[(オプション) AWS Elastic Beanstalk (PaaS)]]`
   - `[[(オプション) AWS Lightsail (簡易VPS)]]`

### 3.3. [[AWS ストレージサービス MOC]]
   - **[[Amazon S3 (Simple Storage Service) MOC]]** (オブジェクトストレージ)
      - `[[バケットとオブジェクト]]`
      - `[[S3ストレージクラス (Standard, Intelligent-Tiering, IA, Glacier)]]`
      - `[[バージョニングとライフサイクル管理]]`
      - `[[静的ウェブサイトホスティング]]`
      - `[[S3のセキュリティ (IAMポリシー, バケットポリシー, ACL, 暗号化)]]`
   - **[[Amazon EBS (Elastic Block Store) MOC]]** (EC2向けブロックストレージ)
      - `[[EBSボリュームタイプ (gp2/gp3, io1/io2, st1, sc1)]]`
      - `[[スナップショットとバックアップ]]`
   - `[[Amazon EFS (Elastic File System)]]` (NFSファイル共有サービス)
   - `[[Amazon FSx]]` (Windows/Lustre向けファイル共有)
   - `[[(オプション) AWS Storage Gateway]]` (ハイブリッドストレージ)

### 3.4. [[AWS ネットワーキングとコンテンツ配信 MOC]]
   - **[[Amazon VPC (Virtual Private Cloud) MOC]]**
      - `[[サブネット (パブリック, プライベート)]]`
      - `[[ルートテーブル]]`
      - `[[インターネットゲートウェイ (IGW) と NATゲートウェイ]]`
      - `[[ネットワークACL (NACLs) vs. セキュリティグループ]]`
      - `[[VPCピアリングとTransit Gateway]]`
   - **[[Amazon Route 53 MOC]]** (DNSサービス)
   - **[[Amazon CloudFront MOC]]** (CDNサービス)
   - `[[AWS Direct Connect]]` (専用線接続)

### 3.5. [[AWS データベースサービス MOC]]
   - **[[Amazon RDS (Relational Database Service) MOC]]** (マネージドリレーショナルDB)
      - `[[サポートされるエンジン (MySQL, PostgreSQL, MariaDB, Oracle, SQL Server, Aurora)]]`
      - `[[マルチAZによる高可用性]]`
      - `[[リードレプリカ]]`
   - **[[Amazon Aurora MOC]]** (クラウドネイティブRDB)
   - **[[Amazon DynamoDB MOC]]** (マネージドNoSQL - Key-Value/ドキュメント)
   - `[[Amazon ElastiCache]]` (インメモリキャッシュ - Redis, Memcached)
   - `[[Amazon Redshift]]` (データウェアハウス)
   - `[[(オプション) Amazon Neptune (グラフDB), Amazon DocumentDB (MongoDB互換)]]`

### 3.6. [[AWS AI/機械学習サービス MOC]]
   - `[[Amazon SageMaker]]` (MLプラットフォーム)
   - `[[AWSのAIサービス (Rekognition - 画像/動画分析, Polly - テキスト読み上げ, Lex - 対話ボット, Transcribe - 音声認識)]]`
   - `[[(オプション) Amazon Bedrock (生成AI)]]`

### 3.7. [[AWS 分析サービス MOC]]
   - `[[Amazon Athena]]` (S3データへのインタラクティブクエリ)
   - `[[Amazon EMR (Elastic MapReduce)]]` (ビッグデータ処理 - Spark, Hadoop)
   - `[[Amazon Kinesis]]` (リアルタイムデータストリーミング)
   - `[[Amazon OpenSearch Service (旧Elasticsearch Service)]]`
   - `[[AWS Glue]]` (ETLサービス)

### 3.8. [[AWS セキュリティ、ID、コンプライアンス MOC]]
   - `[[AWS IAM (Identity and Access Management)]]` (ユーザー、グループ、ロール、ポリシー)
   - `[[AWS KMS (Key Management Service)]]` (暗号化キー管理)
   - `[[AWS WAF & Shield]]` (Web Application Firewall, DDoS対策)
   - `[[AWS Secrets Manager]]` (シークレット管理)
   - `[[AWS Security Hub, Amazon GuardDuty, AWS Config]]` (セキュリティ監視・評価)

### 3.9. [[AWS 開発者ツールとDevOps MOC]]
   - `[[AWS CodeCommit]]` (Gitリポジトリ)
   - `[[AWS CodeBuild]]` (ビルドサービス)
   - `[[AWS CodeDeploy]]` (デプロイサービス)
   - `[[AWS CodePipeline]]` (CI/CDパイプライン)
   - `[[AWS CloudFormation]]` (Infrastructure as Code)
   - `[[AWS Cloud9]]` (クラウドIDE)

### 3.10. [[AWS 管理とガバナンス MOC]]
    - `[[Amazon CloudWatch]]` (モニタリング、ロギング、アラート)
    - `[[AWS CloudTrail]]` (APIコール監査)
    - `[[AWS Systems Manager]]` (運用管理)
    - `[[AWS Organizations]]` (複数アカウント管理)

## 4. [[Microsoft Azure MOC]]

### 4.1. [[Azure入門と基本概念 MOC]]
   - [[Azureの概要と歴史]]
   - [[Azureアカウントとサブスクリプション、管理グループ]]
   - [[Azure Resource Manager (ARM)]]
   - [[Azureのグローバルインフラストラクチャ (リージョン, アベイラビリティゾーン)]]
   - [[Azure Portal, Azure CLI, Azure PowerShell]]

### 4.2. [[Azure コンピューティングサービス MOC]]
   - `[[Azure Virtual Machines (VM)]]` (IaaS)
   - `[[Azure App Service]]` (PaaS - Webアプリ、モバイルバックエンド)
   - `[[Azure Functions]]` (サーバーレス - FaaS)
   - **コンテナサービス**
      - `[[Azure Kubernetes Service (AKS)]]`
      - `[[Azure Container Instances (ACI)]]`
      - `[[Azure Container Registry (ACR)]]`
   - `[[(オプション) Azure Spring Apps (Java), Azure Virtual Desktop]]`

### 4.3. [[Azure ストレージサービス MOC]]
   - `[[Azure Blob Storage]]` (オブジェクトストレージ)
   - `[[Azure Disk Storage]]` (VM向けブロックストレージ)
   - `[[Azure Files]]` (SMBファイル共有)
   - `[[(オプション) Azure NetApp Files, Azure Data Lake Storage]]`

### 4.4. [[Azure ネットワーキングサービス MOC]]
   - `[[Azure Virtual Network (VNet)]]`
   - `[[Azure Load Balancer]]`
   - `[[Azure Application Gateway]]`
   - `[[Azure DNS]]`
   - `[[Azure CDN]]`

### 4.5. [[Azure データベースサービス MOC]]
   - `[[Azure SQL Database]]` (マネージドSQL Server)
   - `[[Azure Cosmos DB]]` (マルチモデルNoSQLデータベース)
   - `[[Azure Database for PostgreSQL / MySQL / MariaDB]]`
   - `[[Azure Cache for Redis]]`
   - `[[Azure Synapse Analytics]]` (分析プラットフォーム)

### 4.6. [[Azure AI + 機械学習サービス MOC]]
   - `[[Azure Machine Learning]]` (MLプラットフォーム)
   - `[[Azure AI Services (旧Cognitive Services)]]` (Vision, Speech, Language, Decision)
   - `[[Azure OpenAI Service]]`

### 4.7. [[Azure DevOps MOC]]
   - `[[Azure Boards]]` (作業追跡)
   - `[[Azure Repos]]` (Gitリポジトリ)
   - `[[Azure Pipelines]]` (CI/CD)
   - `[[Azure Test Plans]]`
   - `[[Azure Artifacts]]`

### 4.8. [[Azure セキュリティとID管理 MOC]]
   - `[[Microsoft Entra ID (旧Azure Active Directory)]]`
   - `[[Azure Key Vault]]`
   - `[[Microsoft Defender for Cloud]]`

### 4.9. [[Azure 管理とガバナンス MOC]]
    - `[[Azure Monitor]]`
    - `[[Azure Resource Manager (ARM) Templates / Bicep]]` (IaC)
    - `[[Azure Policy]]` (ガバナンス)

## 5. [[Google Cloud Platform (GCP) MOC]]

### 5.1. [[GCP入門と基本概念 MOC]]
   - [[GCPの概要と歴史 (Googleの内部インフラがベース)]]
   - [[GCPのプロジェクトと階層構造]]
   - [[GCPのグローバルインフラストラクチャ (リージョン, ゾーン)]]
   - [[Google Cloud Console, gcloud CLI]]

### 5.2. [[GCP コンピューティングサービス MOC]]
   - `[[Google Compute Engine (GCE)]]` (IaaS)
   - `[[Google App Engine (GAE)]]` (PaaS)
   - `[[Google Cloud Functions]]` (サーバーレス - FaaS)
   - `[[Google Cloud Run]]` (サーバーレスコンテナ)
   - **コンテナサービス**
      - `[[Google Kubernetes Engine (GKE)]]`
      - `[[Google Artifact Registry]]`

### 5.3. [[GCP ストレージサービス MOC]]
   - `[[Google Cloud Storage (GCS)]]` (オブジェクトストレージ)
   - `[[Persistent Disk]]` (GCE向けブロックストレージ)
   - `[[Filestore]]` (NFSファイル共有)

### 5.4. [[GCP ネットワーキングサービス MOC]]
   - `[[Virtual Private Cloud (VPC)]]`
   - `[[Cloud Load Balancing]]`
   - `[[Cloud DNS]]`
   - `[[Cloud CDN]]`

### 5.5. [[GCP データベースサービス MOC]]
   - `[[Cloud SQL]]` (マネージドMySQL, PostgreSQL, SQL Server)
   - **[[Cloud Spanner]]** (グローバル分散RDB)
   - **[[Cloud Bigtable]]** (カラム指向NoSQL)
   - **[[Firestore]]** (ドキュメントNoSQL)
   - `[[Memorystore]]` (インメモリキャッシュ - Redis, Memcached)
   - **[[BigQuery]]** (サーバーレスデータウェアハウス)

### 5.6. [[GCP AIと機械学習サービス MOC]]
   - **[[Vertex AI]]** (統合MLプラットフォーム)
   - `[[BigQuery ML]]` (SQLによるML)
   - `[[AI Building Blocks (Vision AI, Speech-to-Text, Natural Language AIなど)]]`
   - `[[(オプション) Googleの生成AIモデル (Geminiなど)]]`

### 5.7. [[GCP データ分析サービス MOC]]
   - `[[BigQuery]]` (再掲)
   - `[[Dataproc]]` (Spark, Hadoop)
   - `[[Dataflow]]` (ストリーム/バッチ処理)
   - `[[Pub/Sub]]` (メッセージング)

### 5.8. [[GCP セキュリティとID管理 MOC]]
   - `[[Cloud Identity and Access Management (IAM)]]`
   - `[[Cloud Key Management Service (KMS)]]`
   - `[[Secret Manager]]`
   - `[[Security Command Center]]`

### 5.9. [[GCP 開発者ツールと運用 MOC]]
   - `[[Cloud Source Repositories]]` (Gitリポジトリ)
   - `[[Cloud Build]]` (CI/CD)
   - `[[Cloud Code]]` (IDEプラグイン)
   - `[[Operations Suite (旧Stackdriver)]]` (Cloud Monitoring, Cloud Logging)
   - `[[Deployment Manager / Terraform]]` (IaC)

## 6. [[クラウドネイティブ技術 (横断的トピック) MOC]]
   - **[[コンテナ化 (Docker)]]** (再掲、クラウド文脈での重要性)
   - **[[コンテナオーケストレーション (Kubernetes)]]** (再掲、クラウド文脈での重要性)
   - **[[サービスメッシュ (Service Mesh) MOC]]** (Istio, Linkerd)
   - **[[サーバーレスコンピューティング]]** (再掲、FaaSとBaaS)
   - **[[Infrastructure as Code (IaC) MOC]]**
      - `[[Terraformによるマルチクラウド管理]]`
      - `[[プロバイダー固有ツール (CloudFormation, ARM) との比較]]`
   - **[[CI/CD in the Cloud MOC]]** (各プロバイダーのDevOpsツールの活用)

## 7. [[マルチクラウドとハイブリッドクラウド MOC]]
   - **[[マルチクラウド戦略]]** (利点、課題、ユースケース)
   - **[[ハイブリッドクラウド戦略]]** (利点、課題、ユースケース)
   - **管理プレーン**
      - `[[Google Anthos]]`
      - `[[Azure Arc]]`
      - `[[AWS Outposts]]`
   - **相互接続とデータ連携**

## 8. [[クラウドのコスト管理 (FinOps) MOC]]
   - [[クラウドコストの可視化と分析]]
   - [[コスト最適化戦略]]
      - `[[リソースのサイジング]]`
      - `[[不要リソースの停止・削除]]`
      - `[[予約インスタンス/Savings Plansの活用]]`
      - `[[スポットインスタンスの活用]]`
      - `[[オートスケーリングの適切な設定]]`
      - `[[ストレージ階層の最適化]]`
   - [[予算設定とアラート]]
   - [[タグ付け戦略 (Tagging Strategy)]]
   - [[FinOpsの文化とプロセス]]

## 9. [[クラウドセキュリティ (横断的トピック) MOC]]
   - [[責任共有モデルの再確認]]
   - [[アイデンティティとアクセス管理 (IAM) のベストプラクティス]]
   - [[ネットワークセキュリティ (VPC, ファイアウォール, セキュリティグループ)]]
   - [[データ保護と暗号化 (転送中、保存時)]]
   - [[インシデント対応とロギング、モニタリング]]
   - [[コンプライアンスとガバナンス]]
   - [[クラウドセキュリティポスチャ管理 (CSPM)]]
