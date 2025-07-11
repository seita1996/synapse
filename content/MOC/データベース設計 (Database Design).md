---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/database-design
---
## 1. [[データベース設計入門 MOC]]
   - **データベース設計とは**
      - [[データベース設計の定義 (効率的で一貫性があり、堅牢なデータ格納・アクセスを実現するための構造を設計するプロセス)]]
      - [[なぜデータベース設計が重要か (アプリケーションのパフォーマンス、データの整合性、将来の拡張性に直結)]]
      - [[良いデータベース設計と悪いデータベース設計]]
   - **データベース設計の3つのレベル (フェーズ)**
      - **[[概念設計 (Conceptual Design)]]** (ビジネス要件を抽象的なモデルに)
      - **[[論理設計 (Logical Design)]]** (特定のデータモデル(例:リレーショナル)にマッピング)
      - **[[物理設計 (Physical Design)]]** (特定のDBMS上での実装を定義)
   - **データベース設計のプロセス全体像**
      - `[[要求分析 → 概念設計 → 論理設計 → 物理設計 → 実装 → テスト → 運用・保守]]`
   - **データモデリングの重要性**
   - **設計原則**
      - `[[データ整合性 (Data Integrity) の確保]]`
      - `[[データ冗長性 (Data Redundancy) の最小化 (正規化)]]`
      - `[[パフォーマンスとスケーラビリティの考慮]]`
      - `[[柔軟性と拡張性の確保]]`
      - `[[セキュリティの考慮]]`

## 2. [[概念設計 (Conceptual Design) MOC]]
   - **概念設計の目的**
      - `[[ビジネス要件とデータ要件の理解と文書化]]`
      - `[[利害関係者 (ステークホルダー) とのコミュニケーションツール]]`
      - `[[データベースの全体像の把握]]`
   - **要求分析 (Requirements Analysis)**
      - `[[データ要件の収集 (どのようなデータを、どのように利用するか)]]`
      - `[[機能要件と非機能要件の洗い出し]]`
      - `[[ユーザーインタビューとドキュメント分析]]`
   - **[[ERモデル (Entity-Relationship Model) MOC]]**
      - **[[エンティティ (Entity) の特定]]** (システムが管理すべき「モノ」や「概念」)
      - **[[属性 (Attribute) の特定]]** (エンティティが持つ情報)
         - `[[単純属性 vs. 複合属性]]`
         - `[[単一値属性 vs. 多値属性]]`
         - `[[派生属性 (Derived Attribute)]]`
      - **[[リレーションシップ (Relationship) の特定]]** (エンティティ間の関連)
         - `[[リレーションシップの次数 (Degree)]]` (2項関係, 3項関係)
      - **[[カーディナリティ (Cardinality) / 多重度]]**
         - `[[1対1 (One-to-One)]]`
         - `[[1対多 (One-to-Many)]]`
         - `[[多対多 (Many-to-Many)]]`
      - **[[参加の制約 (Participation Constraints)]]** (全体参加 vs. 部分参加)
      - **[[弱エンティティ (Weak Entity)]]**
      - **[[特殊化 (Specialization) と汎化 (Generalization) / ISA関係]]** (サブクラスとスーパークラス)
         - `[[継承の表現]]`
   - **[[ER図 (ER Diagram - ERD) の作成 MOC]]**
      - `[[ER図の表記法 (チェン記法, IE記法/カラスの足記法, UMLクラス図)]]`
      - `[[良いER図を作成するためのヒント]]`
      - `[[ER図作成ツール (draw.io, Lucidchart, ERDPlusなど)]]`
   - **概念設計の成果物** (ER図、データディクショナリ)

## 3. [[論理設計 (Logical Design) MOC]]
   - **論理設計の目的**
      - `[[概念モデルを特定のデータモデル (例: リレーショナルモデル) に変換]]`
      - `[[DBMSに依存しないスキーマの設計]]`
   - **リレーショナルデータベースの論理設計**
      - **[[ERモデルからリレーショナルモデルへのマッピング]]**
         - `[[エンティティ → テーブル]]`
         - `[[属性 → 列 (カラム)]]`
         - `[[1対多リレーションシップ → 外部キー]]`
         - `[[1対1リレーションシップの扱い]]`
         - `[[多対多リレーションシップ → 関連テーブル (中間テーブル)]]`
         - `[[弱エンティティのマッピング]]`
         - `[[汎化/特殊化のマッピング戦略]]`
      - **[[正規化 (Normalization) MOC]]** (再掲・設計プロセスとして)
         - `[[正規化の目的と更新時異常 (挿入・更新・削除異常)]]`
         - `[[関数従属性の分析]]`
         - **[[第一正規形 (1NF) への変換]]** (繰り返しグループの排除)
         - **[[第二正規形 (2NF) への変換]]** (部分関数従属の排除)
         - **[[第三正規形 (3NF) への変換]]** (推移的関数従属の排除)
         - **[[ボイス・コッド正規形 (BCNF) への変換]]**
         - [[正規化の利点とパフォーマンスのトレードオフ]]
      - **[[非正規化 (Denormalization) の検討]]**
         - `[[非正規化を適用するケース (パフォーマンス要件)]]`
         - `[[非正規化の手法 (冗長な列の追加、テーブルのマージなど)]]`
   - **NoSQLデータベースの論理設計 (データモデリング)**
      - **[[クエリ駆動モデリング (Query-Driven Modeling)]]** (再掲)
      - `[[ドキュメントデータベースのモデリング (埋め込み vs. 参照)]]`
      - `[[キーバリューストアのキー設計]]`
      - `[[カラム指向データベースのパーティションキー/クラスタリングキー設計]]`
      - `[[グラフデータベースのノードとエッジの設計]]`
   - **論理設計の成果物** (テーブル定義書、リレーションシップ定義、正規化されたスキーマ)

## 4. [[物理設計 (Physical Design) MOC]]
   - **物理設計の目的**
      - `[[論理スキーマを特定のRDBMS/NoSQLシステム上に実装]]`
      - `[[パフォーマンス、ストレージ効率、セキュリティなどを考慮した物理的構成の決定]]`
   - **[[データ型 (Data Types) の選択 MOC]]**
      - `[[特定のDBMSが提供するデータ型の選択]]` (例: `INT` vs. `BIGINT`, `VARCHAR` vs. `TEXT`)
      - `[[ストレージサイズとパフォーマンスへの影響]]`
      - `[[固定長 vs. 可変長]]`
      - `[[適切な日付・時刻型の選択]]`
   - **[[インデックス設計 (Index Design) MOC]]**
      - `[[インデックスの役割と仕組み (B-Treeなど)]]` (再掲)
      - **[[どの列にインデックスを作成すべきか]]**
         - `[[主キーとユニークキー]]`
         - `[[外部キー]]`
         - `[[WHERE句で頻繁に使用される列]]`
         - `[[JOIN句で使用される列]]`
         - `[[ORDER BY句で使用される列]]`
      - **[[複合インデックス (Composite Index) の設計]]**
         - `[[列の順序の重要性]]`
      - **[[カバリングインデックス (Covering Index)]]**
      - [[インデックスの貼りすぎによる弊害 (更新パフォーマンスの低下)]]
      - `[[インデックスのメンテナンス (`REINDEX`など)]]`
   - **[[パーティショニング (Partitioning) MOC]]**
      - `[[パーティショニングの目的 (大規模テーブルの管理性・パフォーマンス向上)]]`
      - `[[水平パーティショニング (Horizontal Partitioning) / シャーディング]]`
         - `[[レンジパーティショニング]]`
         - `[[リストパーティショニング]]`
         - `[[ハッシュパーティショニング]]`
      - `[[垂直パーティショニング (Vertical Partitioning)]]`
   - **[[ビュー (Views) の物理的設計]]**
      - `[[マテリアライズドビュー (Materialized Views)]]`
   - **[[ファイル編成とストレージパラメータ]]**
      - `[[テーブルスペースの設計]]`
      - `[[物理的なデータ配置の考慮]]`
   - **[[制約 (Constraints) の実装]]**
      - `[[データベースレベルでの制約とアプリケーションレベルでの制約]]`
   - **[[物理設計の成果物]]** (DDLスクリプト, ストレージ設定, インデックス定義)

## 5. [[特定の要件のためのデータベース設計 MOC]]
   - **[[パフォーマンスのための設計 MOC]]**
      - `[[クエリパフォーマンスの最適化を意識した設計]]`
      - `[[非正規化の戦略的利用]]`
      - `[[キャッシュ戦略とデータベース設計]]`
   - **[[スケーラビリティのための設計 MOC]]**
      - `[[水平スケール vs. 垂直スケール]]`
      - `[[シャーディング戦略の設計]]`
      - `[[ステートレスアプリケーションとの親和性]]`
   - **[[高可用性と耐障害性のための設計 MOC]]**
      - `[[レプリケーション (Replication) の設計]]`
      - `[[フェイルオーバークラスタの設計]]`
      - `[[バックアップとリカバリ戦略]]`
   - **[[セキュリティのための設計 MOC]]**
      - **[[データベースセキュリティの原則]]**
      - `[[ユーザー、ロール、権限の設計 (DCL)]]`
      - `[[ビューによるアクセス制御]]`
      - `[[データの暗号化 (転送中、保存時)]]`
      - `[[監査ログの設計]]`
   - **[[データウェアハウス (DWH) の設計 MOC]]** (再掲・設計プロセスとして)
      - `[[スタースキーマとスノーフレークスキーマの設計]]`
      - `[[ETL/ELTプロセスを考慮した設計]]`
      - `[[SCD (Slowly Changing Dimensions) の設計]]`
   - **[[時系列データの設計 MOC]]**
   - **[[地理空間データの設計 MOC]]**

## 6. [[データベースのライフサイクルとベストプラクティス MOC]]
   - **[[データベースのリファクタリング (Database Refactoring) MOC]]**
      - `[[リファクタリングの必要性と課題]]`
      - `[[代表的なリファクタリングパターン]]`
   - **[[スキーマ変更とデータマイグレーション (Schema Evolution and Data Migration) MOC]]**
      - `[[マイグレーションの戦略 (ビッグバン vs. 段階的)]]`
      - `[[マイグレーションツール (Flyway, Liquibase, Alembicなど)]]`
      - `[[ゼロダウンタイムマイグレーション]]`
   - **[[データベースのドキュメンテーション]]**
      - `[[データディクショナリ (Data Dictionary) / データ定義書]]`
      - `[[ER図の維持管理]]`
      - `[[ドキュメント自動生成ツール]]`
   - **[[バージョン管理 (Version Control) for Databases]]**
      - `[[スキーマ定義とマイグレーションスクリプトのGit管理]]`
   - **[[データベース設計のアンチパターン MOC]]**
      - `[[不適切な主キーの選択 (例: 変更されうる自然キー)]]`
      - `[[インデックスの乱用または不足]]`
      - `[[過度な正規化 / 不適切な非正規化]]`
      - `[[データ型を大きく取りすぎる (`VARCHAR(255)`の乱用など)]]`
      - `[[EAV (Entity-Attribute-Value) パターンの誤用]]`
      - `[[一つのテーブルに全てを詰め込む (God Table)]]`
      - `[[ロジックをデータベースに寄せすぎる (複雑なストアドプロシージャ)]]`
   - **[[(オプション) ORM (Object-Relational Mapper) 利用時の設計考慮事項]]**
      - `[[N+1問題と対策]]`
      - `[[ORMが生成するSQLの意識]]`

## 7. [[データベース設計ツール MOC]]
   - **モデリング/ER図作成ツール**
      - `[[draw.io (diagrams.net)]]`
      - `[[Lucidchart]]`
      - `[[ERDPlus]]`
      - `[[Figma (FigJam)]]`
      - `[[Miro]]`
      - `[[ER/Studio]]`
      - `[[ERwin Data Modeler]]`
      - `[[MySQL Workbench]]`
      - `[[pgModeler]]`
   - **スキーマ管理/マイグレーションツール**
      - `[[Flyway]]`
      - `[[Liquibase]]`
      - `[[Alembic]]`
      - `[[dbt]]` (データ変換層でのモデリング)
   - **データベースクライアント/管理ツール**
      - `[[DBeaver]]`
      - `[[DataGrip]]`
      - `[[pgAdmin (PostgreSQL)]]`
      - `[[MySQL Workbench]]` (再掲)
