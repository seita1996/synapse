---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/nosql-databases
---
## 1. [[NoSQL入門 MOC]]
   - **NoSQLとは**
      - [[NoSQLの定義 ("Not Only SQL", 非リレーショナルデータベース)]]
      - [[NoSQLが登場した背景 (インターネットの普及, ビッグデータ, Webスケールの要求)]]
      - `[[リレーショナルデータベース (RDB) の限界 (スキーマの柔軟性、水平スケーラビリティ)]]`
   - **NoSQLの利点**
      - `[[高いスケーラビリティ (水平分散 - Scale-out)]]`
      - `[[柔軟なデータモデル (スキーマレス、動的スキーマ)]]`
      - `[[高い可用性と耐障害性]]`
      - `[[特定のユースケースにおける高いパフォーマンス]]`
   - **NoSQLの課題**
      - `[[一貫性モデルの複雑さ (結果整合性)]]`
      - `[[標準化されたクエリ言語の欠如 (SQLのような)]]`
      - `[[トランザクション (ACID) サポートの制限]]`
      - `[[データモデリングの難しさ]]`
      - `[[エコシステムとツールの成熟度 (RDB比)]]`
   - **[[CAP定理 (CAP Theorem) MOC]]** (Eric Brewer)
      - `[[CAP定理の定義 (分散システムは3つのうち最大2つしか同時に保証できない)]]`
      - **[[一貫性 (Consistency - C)]]**
      - **[[可用性 (Availability - A)]]**
      - **[[分断耐性 (Partition Tolerance - P)]]** (現代の分散システムでは必須)
      - `[[CPシステム (一貫性と分断耐性)]]`
      - `[[APシステム (可用性と分断耐性)]]`
      - [[CAP定理のトレードオフとデータベース選択への影響]]
   - **[[BASE特性 (BASE Properties) MOC]]**
      - `[[BASE特性の定義 (結果整合性を重視するシステムの特性)]]`
      - `[[Basically Available (基本的に利用可能)]]`
      - `[[Soft State (状態は時間とともに変化しうる)]]`
      - `[[Eventually Consistent (最終的に一貫性がとれる)]]`
      - `[[ACID特性 (RDB) vs. BASE特性 (NoSQL)]]`
   - **[[結果整合性 (Eventual Consistency) MOC]]**
      - [[結果整合性の仕組みとレベル]]
   - **NoSQLデータベースの選択基準**

## 2. [[NoSQLデータベースの種類 (データモデルによる分類) MOC]]
   - **[[キーバリューストア (Key-Value Stores) MOC]]**
      - `[[キーバリューストアのデータモデル (単純なキーと値のペア)]]`
      - `[[キーバリューストアの特性 (シンプル、高速、高いスケーラビリティ)]]`
      - `[[主な操作 (Get, Put, Delete)]]`
      - `[[ユースケース (キャッシュ、セッション管理、設定情報保存)]]`
      - `[[代表的な製品 (Redis, Amazon DynamoDB, Riak)]]`
   - **[[ドキュメントデータベース (Document Databases) MOC]]**
      - `[[ドキュメントデータベースのデータモデル (JSON/BSON形式のドキュメント)]]`
      - `[[ドキュメントの構造 (ネストされたオブジェクト、配列)]]`
      - `[[ドキュメントデータベースの特性 (柔軟なスキーマ、豊富なクエリ機能)]]`
      - `[[クエリ言語 (ドキュメント内のフィールドに対するクエリ)]]`
      - `[[ユースケース (Webアプリケーション、コンテンツ管理、プロファイリング)]]`
      - `[[代表的な製品 (MongoDB, Couchbase, Amazon DocumentDB)]]`
   - **[[カラム指向データベース (Column-Family / Wide-Column Stores) MOC]]**
      - `[[カラム指向データベースのデータモデル (行キー、カラムファミリ、カラム)]]`
      - `[[カラム指向データベースの特性 (大量書き込み、高いスケーラビリティ、疎なデータ)]]`
      - `[[データ配置 (列指向ストレージとの違い)]]`
      - `[[ユースケース (大規模時系列データ、IoT、ログ分析)]]`
      - `[[代表的な製品 (Apache Cassandra, HBase, Google Cloud Bigtable)]]`
   - **[[グラフデータベース (Graph Databases) MOC]]**
      - `[[グラフデータベースのデータモデル (ノード、エッジ、プロパティ)]]`
      - `[[グラフデータベースの特性 (リレーションシップの高速なトラバース)]]`
      - `[[クエリ言語 (Cypher, Gremlinなど)]]`
      - `[[ユースケース (ソーシャルネットワーク、推薦エンジン、不正検知、ナレッジグラフ)]]`
      - `[[代表的な製品 (Neo4j, Amazon Neptune, JanusGraph)]]`
   - **[[(オプション) 時系列データベース (Time-Series Databases)]]** (InfluxDB, Prometheus)
   - **[[(オプション) 検索エンジンデータベース (Search Engine Databases)]]** (Elasticsearch, Apache Solr)

## 3. [[MongoDB MOC]] (ドキュメントデータベース)

### 3.1. [[MongoDB入門 MOC]]
   - `[[MongoDBの概要と特徴 (柔軟なドキュメントモデル、高いスケーラビリティ、豊富なクエリ)]]`
   - **[[MongoDBのデータモデル]]**
      - `[[BSON (Binary JSON) フォーマット]]`
      - `[[データベース (Database), コレクション (Collection), ドキュメント (Document)]]`
      - `[[ドキュメント内の埋め込みドキュメントと配列]]`
      - `[[_idフィールドとObjectId]]`

### 3.2. [[MongoDBのクエリとデータ操作 MOC]]
   - **[[MongoDB Query Language (MQL)]]**
      - `[[CRUD操作 (Create, Read, Update, Delete)]]`
         - `[[`insertOne()`, `insertMany()`]]`
         - `[[`find()`, `findOne()`]]`
         - `[[`updateOne()`, `updateMany()`, `replaceOne()`]]`
         - `[[`deleteOne()`, `deleteMany()`]]`
      - **[[クエリセレクタ (Query Selectors)]]** (`$eq`, `$ne`, `$gt`, `$lt`, `$in`, `$and`, `$or`など)
      - **[[プロジェクション (Projection)]]** (返すフィールドの選択)
      - **[[更新演算子 (Update Operators)]]** (`$set`, `$unset`, `$inc`, `$push`, `$pull`など)
      - `[[`findAndModify`, `findOneAndUpdate`]]`
   - **[[インデックス (Indexes) MOC]]**
      - `[[インデックスの役割と重要性]]`
      - `[[シングルフィールドインデックス]]`
      - `[[複合インデックス (Compound Index)]]`
      - `[[マルチキーインデックス (Multikey Index)]]` (配列フィールド)
      - `[[テキストインデックス (Text Index)]]` (全文検索)
      - `[[地理空間インデックス (Geospatial Index)]]`
      - `[[インデックスの作成と管理 (`createIndex`, `getIndexes`)]]`
      - `[[クエリの実行計画 (`explain()`)]]`
   - **[[集計フレームワーク (Aggregation Framework) MOC]]**
      - `[[集計パイプラインの概念]]`
      - `[[主要なステージ (`$match`, `$group`, `$project`, `$sort`, `$limit`, `$unwind`, `$lookup`)]]`
      - `[[集計演算子 (`$sum`, `$avg`, `$max`, `$min`, `$push`など)]]`

### 3.3. [[MongoDBのアーキテクチャと運用 MOC]]
   - **[[レプリケーション (Replication) - レプリカセット (Replica Set) MOC]]**
      - `[[レプリカセットの構成 (プライマリ、セカンダリ)]]`
      - `[[自動フェイルオーバーと高可用性]]`
      - `[[読み取り設定 (Read Preference)]]`
   - **[[シャーディング (Sharding) MOC]]** (水平スケーラビリティ)
      - `[[シャーディングのアーキテクチャ (Shard, mongos, Config Server)]]`
      - `[[シャードキー (Shard Key) の選択]]`
      - `[[シャーディング戦略 (Ranged Sharding, Hashed Sharding)]]`
   - **[[書き込み懸念 (Write Concern) と読み取り懸念 (Read Concern)]]** (一貫性の調整)
   - **[[(オプション) トランザクション (Multi-document ACID Transactions)]]**
   - **MongoDBの管理とツール** (`mongosh`, `MongoDB Compass`, `MongoDB Atlas`)

## 4. [[Apache Cassandra MOC]] (カラム指向データベース)

### 4.1. [[Cassandra入門 MOC]]
   - `[[Cassandraの概要と特徴 (分散型、高い可用性と耐障害性、線形スケーラビリティ、チューニング可能な一貫性)]]`
   - **[[Cassandraのアーキテクチャ MOC]]**
      - `[[分散リング構造とノード]]`
      - `[[ゴシッププロトコル (Gossip Protocol)]]` (ノード間通信)
      - `[[スニッチ (Snitch)]]` (トポロジ認識)
      - `[[レプリケーション戦略 (Replication Strategy)]]` (SimpleStrategy, NetworkTopologyStrategy)
      - `[[パーティショナ (Partitioner)]]` (データの分散方法)
      - `[[マスターレスアーキテクチャ (リーダーなし)]]`

### 4.2. [[CassandraのデータモデルとCQL MOC]]
   - **[[Cassandraのデータモデル]]**
      - `[[キースペース (Keyspace)]]`
      - `[[テーブル (Table)]]`
      - **[[主キー (Primary Key)]]**
         - **[[パーティションキー (Partition Key)]]** (データの配置場所を決定)
         - **[[クラスタリングキー (Clustering Key)]]** (パーティション内でのソート順を決定)
      - `[[静的カラム (Static Columns)]]`
   - **[[CQL (Cassandra Query Language) MOC]]**
      - `[[SQLライクな構文]]`
      - `[[CRUD操作 (`INSERT`, `SELECT`, `UPDATE`, `DELETE`)]]`
      - `[[`WHERE`句の制約 (パーティションキーが必須)]]`
      - `[[バッチ操作 (`BATCH`)]]`
      - `[[軽量トランザクション (Lightweight Transactions - LWT)]]` (Compare-And-Set)
      - `[[(オプション) ユーザー定義型 (UDT), コレクション型 (list, set, map)]]`

### 4.3. [[Cassandraの内部動作と運用 MOC]]
   - **[[書き込みパス (Write Path)]]** (`Commit Log`, `Memtable`, `SSTable`)
   - **[[読み込みパス (Read Path)]]** (`Memtable`, `Row Cache`, `Key Cache`, `Bloom Filter`, `SSTable`)
   - **[[コンパクション (Compaction)]]** (SSTableのマージ)
   - **[[一貫性レベル (Consistency Level)]]**
      - `[[`ANY`, `ONE`, `QUORUM`, `LOCAL_QUORUM`, `EACH_QUORUM`, `ALL`など]]`
      - `[[書き込みと読み込みで異なる一貫性レベルを設定可能]]`
      - `[[一貫性とレイテンシのトレードオフ]]`
   - **[[Hinted Handoff と Read Repair]]** (ノード障害時のデータ一貫性維持)
   - **Cassandraの管理とツール** (`cqlsh`, `nodetool`, `DataStax Astra`)

## 5. [[Redis MOC]] (キーバリューストア / インメモリデータ構造サーバー)

### 5.1. [[Redis入門 MOC]]
   - `[[Redisの概要と特徴 (インメモリ、高速、豊富なデータ構造、単一スレッド)]]`
   - **[[Redisの主要なユースケース MOC]]**
      - `[[キャッシュ (Caching)]]`
      - `[[セッションストア (Session Store)]]`
      - `[[メッセージブローカー (Message Broker) / Pub/Sub]]`
      - `[[リアルタイム分析 (カウンター, ランキング)]]`
      - `[[キュー (Queue)]]`
      - `[[分散ロック (Distributed Lock)]]`

### 5.2. [[Redisのデータ構造 MOC]]
   - **[[Strings]]** (文字列、数値、ビットマップ)
   - **[[Lists]]** (両端キュー、スタック)
   - **[[Hashes]]** (オブジェクトのフィールド格納)
   - **[[Sets]]** (一意な要素の集合)
   - **[[Sorted Sets]]** (スコア付きのソートされた集合、ランキングやリーダーボードに利用)
   - **[[Streams]]** (ログ形式のデータ構造、Kafkaライク)
   - **[[HyperLogLogs]]** (巨大な集合の濃度を推定)
   - **[[Geospatial Indexes]]** (地理空間データ)
   - `[[各データ構造の主要コマンド]]`

### 5.3. [[Redisの機能と運用 MOC]]
   - **[[永続化 (Persistence) MOC]]**
      - `[[RDB (Redis Database) - スナップショット方式]]`
      - `[[AOF (Append-Only File) - ログ追記方式]]`
      - `[[RDBとAOFの比較と選択]]`
   - **[[レプリケーション (Replication) MOC]]**
      - `[[マスター/スレーブ構成]]`
      - `[[非同期レプリケーション]]`
   - **[[高可用性 (High Availability) - Redis Sentinel MOC]]**
      - `[[マスターノードの監視と自動フェイルオーバー]]`
   - **[[スケーラビリティ - Redis Cluster MOC]]**
      - `[[データのシャーディング]]`
      - `[[マスターレスアーキテクチャ]]`
   - **[[トランザクション (`MULTI`, `EXEC`, `WATCH`)]]**
   - **[[Pub/Sub (Publish/Subscribe) MOC]]**
   - **[[Luaスクリプティング]]** (アトミックな複合操作)
   - **[[Redisのメモリ管理]]**
   - **Redisの管理とツール** (`redis-cli`, `RedisInsight`)

## 6. [[NoSQLデータモデリング MOC]]
   - **RDBモデリングとの違い (正規化 vs. 非正規化)**
   - **[[クエリ駆動モデリング (Query-Driven Modeling)]]** (アプリケーションのアクセスパターンを先に考える)
   - **[[非正規化 (Denormalization) とデータ重複]]**
   - **[[埋め込み (Embedding) vs. 参照 (Referencing)]]** (1対多、多対多関係の表現)
      - `[[ドキュメントデータベースにおける埋め込みと参照]]`
   - **キー設計の重要性**
      - `[[キーバリューストアにおけるキー設計]]`
      - `[[カラム指向データベースにおけるパーティションキーとクラスタリングキーの設計]]`
   - **集約 (Aggregates) の事前計算**
   - **インデックス戦略** (セカンダリインデックスなど)
   - **データモデリングのアンチパターン**

## 7. [[NoSQLデータベースの選択と利用 MOC]]
   - **プロジェクト要件に基づくデータベース選択**
      - `[[データモデルの適合性]]`
      - `[[読み書きのパターンとパフォーマンス要件]]`
      - `[[一貫性の要件 (強整合性 vs. 結果整合性)]]`
      - `[[スケーラビリティと可用性の要件]]`
      - `[[運用コストとチームのスキルセット]]`
   - **[[ポリグロットパーシステンス (Polyglot Persistence) MOC]]**
      - `[[複数のデータベースを適材適所で使い分けるアプローチ]]`
      - `[[マイクロサービスアーキテクチャとポリグロットパーシステンス]]`
   - **NoSQLデータベースの移行戦略**
   - **NoSQLデータベースの監視とチューニング**

## 8. [[NoSQLの将来とトレンド MOC]]
   - **[[NewSQLデータベースとの関係]]**
   - **[[マルチモデルデータベース (Multi-model Databases)]]**
   - **[[サーバーレスNoSQLデータベース]]** (DynamoDB On-Demandなど)
   - **[[クラウドネイティブデータベース]]**
   - **[[トランザクションサポートの強化]]**
   - **[[AI/MLワークロードとNoSQL]]**
