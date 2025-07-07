---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/relational-databases
---
## 1. [[RDB入門とリレーショナルモデル MOC]]
   - **リレーショナルデータベース (RDB) とは**
      - [[RDBの定義 (リレーション(テーブル)に基づいてデータを構造化するデータベース)]]
      - [[RDBの歴史 (エドガー・F・コッドと「リレーショナルモデル」)]]
      - [[RDBMS (Relational Database Management System) の役割]]
      - [[RDBの利点 (データの一貫性・整合性の維持、柔軟なデータアクセス)]]
   - **リレーショナルモデルの基本概念**
      - **[[リレーション (Relation) / テーブル (Table)]]**
         - [[行 (Row) / タプル (Tuple) / レコード (Record)]]
         - [[列 (Column) / 属性 (Attribute) / フィールド (Field)]]
      - **[[ドメイン (Domain) / 型 (Type)]]** (属性が取りうる値の集合)
      - **[[次数 (Degree) と濃度 (Cardinality)]]**
      - [[リレーションの性質 (行の順序は無関係, 列の順序は無関係, 重複行は存在しない)]]
   - **[[キー (Keys) MOC]]**
      - `[[キーの役割 (行の一意性の保証、リレーション間の関連付け)]]`
      - **[[スーパーキー (Super Key)]]**
      - **[[候補キー (Candidate Key)]]**
      - **[[主キー (Primary Key - PK)]]**
         - `[[主キーの制約 (一意性、非NULL)]]`
      - **[[外部キー (Foreign Key - FK)]]**
         - `[[参照整合性 (Referential Integrity)]]`
         - `[[外部キー制約 (ON DELETE, ON UPDATE)]]`
      - **[[代理キー (サロゲートキー - Surrogate Key) vs. 自然キー (Natural Key)]]**
      - `[[(オプション) 代替キー (Alternate Key)]]`
      - `[[(オプション) 複合キー (Composite Key)]]`

## 2. [[リレーショナルデータモデリングと設計 MOC]]
   - **[[データベース設計のプロセス]]** (要求分析、概念設計、論理設計、物理設計)
   - **[[ERモデル (Entity-Relationship Model) MOC]]**
      - `[[エンティティ (Entity)]]`
      - `[[属性 (Attribute)]]`
      - `[[リレーションシップ (Relationship)]]`
      - `[[リレーションシップのカーディナリティ (1対1, 1対多, 多対多)]]`
      - **[[ER図 (ER Diagram - ERD) の書き方]]** (IE記法, IDEF1X記法など)
   - **[[正規化 (Normalization) MOC]]**
      - `[[正規化の目的 (データ冗長性の排除, 更新時異常の防止)]]`
      - **[[第一正規形 (1NF)]]** (属性の原子性)
      - **[[関数従属性 (Functional Dependency)]]**
         - `[[部分関数従属と完全関数従属]]`
         - `[[推移的関数従属]]`
      - **[[第二正規形 (2NF)]]** (部分関数従属の排除)
      - **[[第三正規形 (3NF)]]** (推移的関数従属の排除)
      - **[[ボイス・コッド正規形 (BCNF)]]**
      - `[[第4正規形 (4NF) と多値従属性 (Multivalued Dependency)]]` (概要)
      - `[[第5正規形 (5NF) と結合従属性 (Join Dependency)]]` (概要)
   - **[[非正規化 (Denormalization) MOC]]**
      - [[非正規化の目的 (クエリパフォーマンスの向上)]]
      - [[非正規化のトレードオフ (データ冗長性と更新時異常のリスク)]]
      - [[非正規化の具体的な手法]]
   - **インデックス設計** (詳細はパフォーマンスセクションで)

## 3. [[SQL (Structured Query Language) MOC]]

### 3.1. [[SQL入門 MOC]]
   - [[SQLの歴史と標準 (ANSI SQL)]]
   - [[SQLの方言 (PostgreSQL, MySQL, Oracle, SQL Serverなど)]]
   - **SQLの分類**
      - `[[データ定義言語 (DDL - Data Definition Language)]]`
      - `[[データ操作言語 (DML - Data Manipulation Language)]]`
      - `[[データ検索言語 (DQL - Data Query Language)]]`
      - `[[データ制御言語 (DCL - Data Control Language)]`
      - `[[トランザクション制御言語 (TCL - Transaction Control Language)]]`

### 3.2. [[データ定義言語 (DDL) MOC]]
   - **[[データベースとスキーマの操作]]**
      - `[[CREATE DATABASE / SCHEMA]]`
      - `[[DROP DATABASE / SCHEMA]]`
   - **[[テーブルの操作]]**
      - `[[CREATE TABLE]]`
         - **[[データ型 (Data Types)]]** (INTEGER, VARCHAR, CHAR, TEXT, NUMERIC, REAL, DATE, TIMESTAMPなど、RDBMSごとの違い)
         - **[[制約 (Constraints)]]**
            - `[[NOT NULL]]`
            - `[[UNIQUE]]`
            - `[[PRIMARY KEY]]`
            - `[[FOREIGN KEY]]`
            - `[[CHECK]]`
            - `[[DEFAULT]]`
      - `[[ALTER TABLE]]` (列の追加/削除/変更、制約の追加/削除)
      - `[[DROP TABLE]]`
      - `[[TRUNCATE TABLE]]`
   - **[[ビュー (View) の操作]]**
      - `[[CREATE VIEW]]`
      - `[[DROP VIEW]]`
      - [[ビューの利点 (単純化、セキュリティ)]]
   - **[[インデックス (Index) の操作]]**
      - `[[CREATE INDEX]]`
      - `[[DROP INDEX]]`

### 3.3. [[データ操作言語 (DML) MOC]]
   - **[[`INSERT` 文]]**
      - `[[単一行の挿入]]`
      - `[[複数行の挿入]]`
      - `[[SELECT結果の挿入 (`INSERT INTO ... SELECT ...`)]]`
   - **[[`UPDATE` 文]]**
      - `[[WHERE句による更新対象の指定]]`
   - **[[`DELETE` 文]]**
      - `[[WHERE句による削除対象の指定]]`
      - `[[DELETE vs. TRUNCATE vs. DROP]]`
   - **[[(オプション) `MERGE` 文 (UPSERT)]]**

### 3.4. [[データ検索言語 (DQL) / SELECT文 MOC]]
   - **[[`SELECT` 文の基本構造]]**
      - `[[SELECT句 (列の選択, `*`, `DISTINCT`, 別名(AS))]]`
      - `[[FROM句 (テーブルの指定)]]`
   - **[[`WHERE` 句 (行のフィルタリング)]]**
      - `[[比較演算子 (`=`, `!=`, `<`, `>`など)]]`
      - `[[論理演算子 (`AND`, `OR`, `NOT`)]]`
      - `[[`BETWEEN` ... `AND` ...]]`
      - `[[`IN` (...) / `NOT IN` (...)]]`
      - `[[`LIKE` (ワイルドカード: `%`, `_`)]]`
      - `[[`IS NULL` / `IS NOT NULL`]]`
   - **[[`ORDER BY` 句 (結果のソート)]]**
      - `[[ASC` (昇順), `DESC` (降順)]]`
      - `[[複数列によるソート]]`
   - **[[`LIMIT` / `OFFSET` 句 (結果行数の制限とページネーション)]]** (`FETCH FIRST`などの方言も)
   - **[[集約関数 (Aggregate Functions) MOC]]**
      - `[[COUNT()]]`
      - `[[SUM()]]`
      - `[[AVG()]]`
      - `[[MAX()]]`
      - `[[MIN()]]`
   - **[[`GROUP BY` 句 (データのグループ化)]]**
      - [[集約関数との組み合わせ]]
   - **[[`HAVING` 句 (グループ化後のフィルタリング)]]**
      - `[[WHERE` と `HAVING` の違い]]
   - **[[結合 (JOIN) MOC]]**
      - `[[INNER JOIN]]` (内部結合)
      - `[[LEFT JOIN (LEFT OUTER JOIN)]]` (左外部結合)
      - `[[RIGHT JOIN (RIGHT OUTER JOIN)]]` (右外部結合)
      - `[[FULL OUTER JOIN]]` (完全外部結合)
      - `[[CROSS JOIN]]` (交差結合)
      - `[[自己結合 (Self Join)]]`
      - `[[USING` 句と `ON` 句]]
   - **[[集合演算子 (Set Operators) MOC]]**
      - `[[UNION` と `UNION ALL]]`
      - `[[INTERSECT]]`
      - `[[EXCEPT` / `MINUS]]`
   - **[[サブクエリ (Subquery) MOC]]**
      - `[[スカラーサブクエリ]]`
      - `[[複数行サブクエリ (`IN`, `ANY`, `ALL`)]]`
      - `[[相関サブクエリ (Correlated Subquery)]]`
      - `[[`EXISTS` 演算子]]`
   - **[[共通テーブル式 (CTE - Common Table Expressions) / `WITH` 句 MOC]]**
      - [[再帰的CTE]]
   - **[[ウィンドウ関数 (Window Functions) MOC]]**
      - `[[ウィンドウ関数の構文 (`OVER`句)]]`
      - `[[`PARTITION BY`, `ORDER BY`, `ROWS/RANGE` フレーム]]`
      - `[[集約ウィンドウ関数 (`SUM`, `AVG`など)]]`
      - `[[ランキング関数 (`ROW_NUMBER`, `RANK`, `DENSE_RANK`)]]`
      - `[[オフセット関数 (`LAG`, `LEAD`)]]`
   - **[[CASE式 (条件分岐)]]**
   - **[[(オプション) ピボットテーブル (PIVOT)]]**

### 3.5. [[データ制御言語 (DCL) とトランザクション制御言語 (TCL) MOC]]
   - **[[`GRANT`]]** (権限付与)
   - **[[`REVOKE`]]** (権限剥奪)
   - **[[`COMMIT`]]** (トランザクションの確定)
   - **[[`ROLLBACK`]]** (トランザクションの取り消し)
   - **[[`SAVEPOINT`]]** (部分的なロールバック)

## 4. [[トランザクション管理 MOC]]
   - **[[トランザクションの定義と目的]]** (All or Nothing)
   - **[[ACID特性 MOC]]**
      - **[[原子性 (Atomicity)]]** (全て実行されるか、全く実行されないか)
      - **[[一貫性 (Consistency)]]** (トランザクション前後でデータベースの整合性が保たれる)
      - **[[独立性 (Isolation) / 分離性]]** (複数のトランザクションが互いに影響しない)
      - **[[永続性 (Durability)]]** (コミットされた変更は失われない)
   - **[[トランザクション分離レベル (Isolation Levels) MOC]]**
      - `[[READ UNCOMMITTED]]`
         - `[[ダーティリード (Dirty Read) の可能性]]`
      - `[[READ COMMITTED]]`
         - `[[ノンリピータブルリード (Non-repeatable Read / Fuzzy Read) の可能性]]`
      - `[[REPEATABLE READ]]`
         - `[[ファントムリード (Phantom Read) の可能性]]`
      - `[[SERIALIZABLE]]`
   - **[[ロック (Locking) MOC]]**
      - `[[共有ロック (Shared Lock / Read Lock)]]`
      - `[[排他ロック (Exclusive Lock / Write Lock)]]`
      - `[[ロックの粒度 (行ロック、テーブルロック)]]`
      - **[[2相ロック (Two-Phase Locking - 2PL)]]**
   - **[[デッドロック (Deadlock) MOC]]**
      - `[[デッドロックの発生条件]]`
      - `[[デッドロックの検出と解消]]`
   - **[[(オプション) 多版型同時実行制御 (MVCC - Multi-Version Concurrency Control)]]** (PostgreSQL, Oracleなど)

## 5. [[データベースのパフォーマンスと最適化 MOC]]
   - **[[インデックス (Index) MOC]]**
      - [[インデックスの役割 (データ検索の高速化)]]
      - **[[B-Treeインデックス (B木/B+木インデックス)]]** (最も一般的)
      - **[[ハッシュインデックス]]**
      - `[[(オプション) 全文検索インデックス]]`
      - `[[(オプション) 空間インデックス (R-treeなど)]]`
      - `[[複合インデックス (Composite Index)]]`
      - `[[カバリングインデックス (Covering Index)]]`
      - `[[インデックスの利点と欠点 (検索速度 vs. 更新/挿入/削除のオーバーヘッド)]]`
      - `[[効果的なインデックスの設計戦略]]`
   - **[[クエリの実行計画 (Query Execution Plan) MOC]]**
      - `[[実行計画とは (クエリ実行の内部的な手順)]]`
      - `[[`EXPLAIN` / `EXPLAIN ANALYZE`コマンドの使い方]]`
      - `[[実行計画の読み方 (スキャン方法: フルテーブルスキャン vs. インデックススキャン, 結合アルゴリズム: Nested Loop Join, Hash Join, Merge Join)]]`
   - **[[クエリチューニング]]**
      - `[[インデックスの活用]]`
      - `[[`WHERE`句の改善 (SARGableな条件)]]`
      - `[[`JOIN`の最適化]]`
      - `[[サブクエリの最適化]]`
   - **データベースの統計情報** (オプティマイザが実行計画を立てるために使用)
   - **マテリアライズドビュー (Materialized View)**
   - **パーティショニング (Partitioning)** (大規模テーブルの分割)
   - **コネクションプーリング (Connection Pooling)**

## 6. [[主要なRDBMSの実装 MOC]]

### 6.1. [[PostgreSQL MOC]]
   - [[PostgreSQLの歴史と特徴 (高機能、拡張性、標準SQL準拠)]]
   - **PostgreSQLのアーキテクチャ** (プロセスベースアーキテクチャ)
   - **PostgreSQLのデータ型** (JSON/JSONB, 配列型, hstore, 幾何データ型など豊富な型)
   - **PostgreSQLの高度な機能**
      - `[[MVCC (多版型同時実行制御)]]`
      - `[[テーブル継承]]`
      - `[[外部データラッパー (FDW - Foreign Data Wrappers)]]`
      - `[[豊富なインデックス種類 (GIN, GiSTなど)]]`
      - `[[高度なトランザクション制御]]`
   - **PostgreSQLの管理と運用**
      - `[[主要な設定ファイル (`postgresql.conf`, `pg_hba.conf`)]]`
      - `[[バックアップとリカバリ (`pg_dump`, `pg_restore`)]]`
      - `[[レプリケーション (ストリーミングレプリケーション)]]`
      - `[[VACUUM` と `ANALYZE`]]`
   - **PostgreSQLのエコシステム** (`pgAdmin`, `psql`コマンドラインツール)

### 6.2. [[MySQL MOC]]
   - [[MySQLの歴史と特徴 (Webでの圧倒的実績、高速性、シンプルさ)]]
   - **MySQLのアーキテクチャ** (スレッドベースアーキテクチャ)
   - **[[ストレージエンジン MOC]]**
      - `[[InnoDB]]` (トランザクション対応、行レベルロック、デフォルト)
      - `[[MyISAM]]` (トランザクション非対応、テーブルレベルロック、高速読み取り)
      - `[[その他のストレージエンジン (Memory, Archive 등)]]`
   - **MySQLの機能**
      - `[[レプリケーション (マスター/スレーブ、グループレプリケーション)]]`
      - `[[MySQLのクラスタリングソリューション (InnoDB Cluster, Percona XtraDB Cluster)]]`
   - **MySQLの管理と運用**
      - `[[主要な設定ファイル (`my.cnf`)]]`
      - `[[バックアップとリカバリ (`mysqldump`)]]`
      - `[[ユーザー管理]]`
   - **MySQLのエコシステム** (`MySQL Workbench`, `mysql`コマンドラインツール)
   - **MySQLとMariaDBの関係**

### 6.3. [[PostgreSQL vs. MySQL MOC]]
   - `[[アーキテクチャとパフォーマンス特性の比較]]`
   - `[[機能とSQL標準準拠度の比較]]`
   - `[[ライセンスとコミュニティの比較]]`
   - `[[ユースケースに応じた選択]]`

## 7. [[データベースの管理と運用 MOC]]
   - **[[データベースのインストールと設定]]**
   - **[[バックアップとリカバリ戦略]]**
      - `[[フルバックアップ、差分バックアップ、増分バックアップ]]`
      - `[[ポイントインタイムリカバリ (PITR)]]`
   - **[[高可用性 (High Availability - HA) とレプリケーション]]**
      - `[[アクティブ/パッシブ構成とアクティブ/アクティブ構成]]`
      - `[[同期レプリケーションと非同期レプリケーション]]`
   - **[[シャーディング (Sharding)]]** (水平分割によるスケーラビリティ)
   - **[[ユーザー管理とセキュリティ]]**
      - `[[認証と認可]]`
      - `[[ロールベースアクセス制御 (RBAC)]]`
      - `[[データの暗号化 (転送中、保存時)]]`
   - **[[データベースモニタリング]]** (パフォーマンス、リソース使用率、エラー)

## 8. [[RDBと他のデータベースモデルの比較 MOC]]
   - **[[RDB vs. NoSQLデータベース]]**
      - `[[スキーマ (固定 vs. 柔軟)]]`
      - `[[一貫性モデル (ACID vs. BASE)]]`
      - `[[スケーラビリティ (垂直 vs. 水平)]]`
      - `[[クエリ言語 (SQL vs. 各種API)]]`
      - `[[ユースケースの比較]]`
   - **[[RDB vs. グラフデータベース]]**
   - **[[RDB vs. 時系列データベース]]**
   - **ポリグロットパーシステンス (Polyglot Persistence)** (複数のDBを使い分けるアプローチ)

## 9. [[RDBの将来とトレンド MOC]]
   - **[[NewSQLデータベース (VoltDB, CockroachDB, TiDBなど)]]** (SQLの利便性とNoSQLのスケーラビリティの両立)
   - **[[クラウドネイティブRDBMS (AWS Aurora, Google Cloud Spannerなど)]]**
   - **[[HTAP (Hybrid Transactional/Analytical Processing)]]**
   - **[[サーバーレスデータベース]]**
   - **[[データベースの自動化とAIOps]]**
