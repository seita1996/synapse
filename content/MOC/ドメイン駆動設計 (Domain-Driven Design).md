---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/domain-driven-design
---
## 1. [[DDD入門と基本原則 MOC]]
   - **DDDとは何か**
      - [[エリック・エヴァンスの『ドメイン駆動設計』の概要]]
      - [[DDDの定義 (複雑なドメインのモデル化を中心としたソフトウェア開発アプローチ)]]
      - [[DDDの核心的価値 (ドメインの深い理解、ビジネス価値との連携、進化する設計)]]
   - **なぜDDDか (DDDの必要性)**
      - [[ソフトウェアの複雑性の種類 (本質的複雑性と偶有的複雑性)]]
      - [[従来の開発アプローチの課題 (データ中心設計、貧血ドメインモデルなど)]]
      - [[DDDが解決しようとする問題]]
   - **DDDの構成要素 (概観)**
      - **[[ユビキタス言語 (Ubiquitous Language)]]**
      - **[[戦略的設計 (Strategic Design)]]**
      - **[[戦術的設計 (Tactical Design)]]**
   - **DDDの利点**
      - [[ドメイン専門家と開発者のコミュニケーション改善]]
      - [[ビジネスロジックの明確化と集約]]
      - [[保守性と拡張性の高いソフトウェアの実現]]
      - [[ドメイン知識のコードへの反映]]
      - [[テスト容易性の向上]]
   - **DDDが適しているプロジェクトとそうでないプロジェクト**
      - `[[DDDが有効なケース (複雑なドメイン、長期的なプロジェクト、ビジネス競争力の中核)]]`
      - `[[DDDが必ずしも必要でないケース (単純なCRUDアプリ、技術的複雑性が主体の問題)]]`
   - **DDD導入の課題と注意点**
      - [[学習コストの高さ]]
      - [[ドメイン専門家との密な連携の必要性]]
      - [[初期の設計オーバーヘッドの可能性]]
      - [[チーム全体の理解と合意形成]]

## 2. [[ユビキタス言語 (Ubiquitous Language) MOC]]
   - **ユビキタス言語とは**
      - [[ユビキタス言語の定義 (ドメイン専門家と開発者が共有し、プロジェクト全体で一貫して使用する言語)]]
      - [[ユビキタス言語の目的 (誤解の排除、ドメインモデルの正確な表現)]]
   - **ユビキタス言語の発見と育成**
      - [[ドメイン専門家との対話の重要性]]
      - [[用語集 (Glossary) の作成と維持]]
      - [[図やモデルを用いたコミュニケーション]]
      - [[コードにおけるユビキタス言語の反映 (クラス名、メソッド名、変数名)]]
      - [[継続的な洗練と進化]]
   - **ユビキタス言語の境界**
      - [[境界づけられたコンテキスト内での言語の一貫性]]
      - [[異なるコンテキスト間での用語の翻訳の必要性]]
   - **ユビキタス言語の失敗例とアンチパターン**
      - `[[技術用語の混入]]`
      - `[[開発者だけが理解できる言語]]`
      - `[[陳腐化する言語]]`
   - **ツールとプラクティス**
      - [[ドメインストーリーテリング (Domain Storytelling)]] (ユビキタス言語発見の一助)
      - [[イベントストーミング (EventStorming)]] (ユビキタス言語発見の一助)

## 3. [[戦略的設計 (Strategic Design) MOC]]
   - **戦略的設計の目的 (大規模システムの構造化、チーム間の連携)**
   - **[[ドメイン (Domain) とサブドメイン (Subdomain) MOC]]**
      - **[[コアドメイン (Core Domain)]]** (ビジネスの競争優位性を生み出す中核部分)
      - **[[支援サブドメイン (Supporting Subdomain)]]** (コアを支援するが、独自性は低い)
      - **[[汎用サブドメイン (Generic Subdomain)]]** (一般的で、外部ソリューションが利用可能な部分)
      - [[サブドメインの識別方法]]
      - [[各サブドメインへの投資戦略]]
   - **[[境界づけられたコンテキスト (Bounded Context) MOC]]**
      - [[境界づけられたコンテキストの定義 (特定のドメインモデルが明確な境界を持つ範囲)]]
      - [[ユビキタス言語の適用範囲としてのコンテキスト]]
      - [[モデルの一貫性と独立性の保証]]
      - **境界づけられたコンテキストの識別方法**
         - `[[組織構造との関連]]`
         - `[[言語的な境界]]`
         - `[[チームの境界]]`
      - **境界づけられたコンテキストの利点**
         - `[[モデルの単純化と集中]]`
         - `[[チームの自律性向上]]`
         - `[[明確なインターフェース定義]]`
      - **境界づけられたコンテキストの設計原則**
         - `[[コンテキストのサイズ (大きすぎず、小さすぎず)]]`
         - `[[明示的な境界の定義]]`
   - **[[コンテキストマップ (Context Map) MOC]]**
      - [[コンテキストマップの定義 (境界づけられたコンテキスト間の関係性を視覚化する図)]]
      - [[コンテキストマップの目的 (システム全体の理解、連携戦略の明確化)]]
      - **コンテキストマップにおける連携パターン**
         - **[[共有カーネル (Shared Kernel)]]**
            - `[[共有カーネルの定義と適用ケース]]`
            - `[[利点とリスク (密結合)]]`
         - **[[顧客/供給者 (Customer/Supplier Development Teams)]]**
            - `[[顧客/供給者の定義と関係性]]`
            - `[[上流 (Upstream) と下流 (Downstream)]]`
            - `[[利点と調整コスト]]`
         - **[[順応者 (Conformist)]]**
            - `[[順応者の定義と適用ケース]]`
            - `[[利点とリスク (供給者への依存)]]`
         - **[[腐敗防止層 (Anticorruption Layer - ACL)]]**
            - `[[ACLの定義と目的 (外部モデルからの保護)]]`
            - `[[AdapterパターンやFacadeパターンの利用]]`
            - `[[利点と実装コスト]]`
         - **[[公開ホストサービス (Open Host Service - OHS)]]**
            - `[[OHSの定義と目的 (安定したプロトコルによるサービス公開)]]`
         - **[[公開言語 (Published Language)]]**
            - `[[公開言語の定義 (コンテキスト間での共通データ形式)]] (例: JSON Schema, Protocol Buffers)`
         - **[[分離した道 (Separate Ways)]]**
            - `[[連携しない、または最小限の連携]]`
         - **[[大きな泥だんご (Big Ball of Mud)]]** (アンチパターンとしての認識)
      - [[コンテキストマップの作成とメンテナンス]]

## 4. [[戦術的設計 (Tactical Design) - ビルディングブロック MOC]]
   - **戦術的設計の目的 (境界づけられたコンテキスト内のドメインモデルを豊かに表現する要素群)**
   - **[[エンティティ (Entity) MOC]]**
      - [[エンティティの定義 (識別子によって区別され、ライフサイクルを持つオブジェクト)]]
      - [[エンティティの識別子 (Identity)]] (人工キー vs. 自然キー)
      - [[エンティティの可変性 (Mutable)]]
      - [[エンティティの振る舞い (Behavior)]]
      - [[エンティティのライフサイクル管理 (生成、永続化、削除)]]
      - [[エンティティの設計原則]]
      - `[[エンティティの例 (顧客、注文、商品)]]`
   - **[[値オブジェクト (Value Object - VO) MOC]]**
      - [[値オブジェクトの定義 (属性の集まりで、識別子を持たず、不変なオブジェクト)]]
      - [[値オブジェクトの不変性 (Immutability)]]
      - [[値オブジェクトの等価性 (属性値による比較)]]
      - [[値オブジェクトの振る舞い (副作用のない操作)]]
      - [[値オブジェクトの利点 (表現力向上、副作用の排除、テスト容易性)]]
      - [[値オブジェクトの設計原則 (小さく、凝集性が高い)]]
      - `[[値オブジェクトの例 (金額、住所、日付範囲、色)]]`
      - [[エンティティの属性としての値オブジェクト]]
   - **[[ドメインサービス (Domain Service) MOC]]**
      - [[ドメインサービスの定義 (特定のエンティティや値オブジェクトに属さないドメインロジック)]]
      - [[ドメインサービスの役割 (複数のエンティティをまたがる操作、ドメイン固有の計算)]]
      - [[ステートレスな振る舞い]]
      - [[ドメインサービスとアプリケーションサービスの違い]]
      - `[[ドメインサービスの例 (送金サービス、商品推薦サービス)]]`
   - **[[集約 (Aggregate) MOC]]**
      - [[集約の定義 (強い関連性を持つエンティティと値オブジェクトのまとまり、一貫性境界)]]
      - **[[集約ルート (Aggregate Root - AR)]]**
         - `[[集約ルートの役割 (集約への唯一のアクセスポイント、不変条件の維持)]]`
         - `[[集約ルートはグローバルな識別子を持つエンティティ]]`
      - **[[集約の設計原則とルール]]**
         - `[[集約内のオブジェクトは集約ルートを通じてのみアクセスされる]]`
         - `[[集約ルートは集約全体の不変条件を維持する責任を持つ]]`
         - `[[集約はトランザクション境界となる (一貫性の単位)]]`
         - `[[他の集約への参照は、集約ルートの識別子によって行う]]`
         - `[[集約は小さく保つ]]`
      - [[集約の利点 (一貫性の保証、複雑性の管理)]]
      - `[[集約の例 (注文(AR)と注文明細、ブログ投稿(AR)とコメント)]]`
      - [[集約の設計の難しさ (境界の決定)]]
   - **[[リポジトリ (Repository) パターン MOC]]**
      - [[リポジトリの定義 (集約の永続化と再構築を抽象化するインターフェース)]]
      - [[リポジトリの目的 (ドメインモデルと永続化技術の分離)]]
      - [[リポジトリのインターフェース (コレクションのような振る舞い)]] (例: `add`, `remove`, `findById`, `findAll`)
      - [[リポジトリの実装 (具体的なORMやDBアクセス)]]
      - [[リポジトリと集約の関係 (通常、集約ルートごとにリポジトリが存在)]]
      - [[リポジトリとDAO (Data Access Object) の違い]]
      - [[リポジトリの設計上の考慮事項 (トランザクション管理、クエリの柔軟性)]]
   - **[[ファクトリ (Factory) パターン MOC]] (DDDにおける)**
      - [[ファクトリの定義 (複雑なオブジェクトや集約の生成責任を持つ)]]
      - [[ファクトリの目的 (オブジェクト生成ロジックのカプセル化、クライアントコードの単純化)]]
      - [[エンティティ、値オブジェクト、集約の生成におけるファクトリの利用]]
      - [[静的ファクトリメソッド vs. ファクトリクラス]]
      - [[ドメイン知識を含むファクトリ]]
      - `[[ファクトリの例 (注文ファクトリ、ユーザーアカウントファクトリ)]]`
   - **[[ドメインイベント (Domain Event) MOC]]**
      - [[ドメインイベントの定義 (ドメイン内で発生した重要な出来事を表すオブジェクト)]]
      - [[ドメインイベントの命名 (過去形)]]
      - [[ドメインイベントに含める情報 (発生時刻、関連IDなど)]]
      - [[ドメインイベントの不変性]]
      - **ドメインイベントの利用**
         - `[[集約間の疎結合な連携]]`
         - `[[副作用の分離 (例: 通知メール送信)]]`
         - `[[イベントソーシングの基盤]]`
         - `[[監査ログ]]`
      - **ドメインイベントの発行と購読**
         - `[[イベントディスパッチャ (Event Dispatcher) / メディエータ (Mediator)]]`
         - `[[イベントハンドラ (Event Handler / Subscriber)]]`
         - `[[同期的処理 vs. 非同期的処理]]`
      - `[[ドメインイベントの例 (注文確定イベント、ユーザー登録イベント)]]`
   - **[[モジュール (Module / Package) MOC]]** (DDDにおける)
      - [[モジュールの定義 (関連性の高いドメインオブジェクト群をまとめる単位)]]
      - [[モジュールの目的 (高凝集・疎結合の促進、モデルの可読性向上)]]
      - [[モジュールの命名 (ユビキタス言語に基づく)]]
      - [[モジュール間の依存関係]]

## 5. [[DDDとアーキテクチャ MOC]]
   - **DDDを支えるアーキテクチャスタイル**
      - **[[レイヤードアーキテクチャ (Layered Architecture) とDDD]]**
         - `[[ドメイン層の分離と重視]]`
         - `[[アプリケーション層、インフラストラクチャ層との連携]]`
      - **[[ヘキサゴナルアーキテクチャ (Hexagonal Architecture / Ports and Adapters) とDDD]]**
         - `[[ドメインモデルの外部依存からの隔離]]`
         - `[[ポート (インターフェース) とアダプタ]]`
      - **[[オニオンアーキテクチャ (Onion Architecture) とDDD]]**
         - `[[依存関係の方向 (外側から内側へ)]]`
         - `[[ドメインモデルが中心]]`
      - **[[クリーンアーキテクチャ (Clean Architecture) とDDD]]**
         - `[[関心の分離と依存ルール]]`
         - `[[エンティティ、ユースケース、インターフェースアダプタ、フレームワーク＆ドライバ]]`
      - **[[CQRS (Command Query Responsibility Segregation) とDDD]]**
         - `[[コマンドモデルとクエリモデルの分離]]`
         - `[[集約とコマンド処理の親和性]]`
         - `[[クエリモデルの最適化]]`
      - **[[イベントソーシング (Event Sourcing) とDDD]]**
         - `[[状態変更をドメインイベントのシーケンスとして永続化]]`
         - `[[集約の状態再構築]]`
         - `[[イベントソーシングの利点と課題]]`
   - **アプリケーションサービス (Application Service)**
      - [[アプリケーションサービスの役割 (ユースケースの調整、トランザクション制御、ドメインオブジェクトの呼び出し)]]
      - [[アプリケーションサービスは薄く保つ]]
      - [[アプリケーションサービスとドメインサービスの違い]]
   - **インフラストラクチャサービス (Infrastructure Service)**
      - [[永続化、メッセージング、外部API連携などの技術的関心事]]

## 6. [[DDDの実践とテクニック MOC]]
   - **ドメインモデリングの進め方**
      - [[ドメイン専門家との協調モデリング]]
      - **[[イベントストーミング (EventStorming) MOC]]**
         - `[[イベントストーミングの概要と目的 (ドメイン知識の可視化、共通理解の形成)]]`
         - `[[イベントストーミングの進め方 (ドメインイベント、コマンド、アクター、集約、ポリシーなど)]]`
         - `[[ビッグピクチャーイベントストーミングとデザインレベルイベントストーミング]]`
      - **[[ドメインストーリーテリング (Domain Storytelling) MOC]]**
         - `[[ドメインストーリーテリングの概要と目的 (具体的なシナリオを通じたドメイン理解)]]`
         - `[[ピクトグラムとアノテーションを用いたストーリー記述]]`
      - [[コンテキストマッピングのワークショップ]]
      - [[モデルの視覚化 (UML、ホワイトボード)]]
      - [[継続的なリファクタリングとモデルの進化]]
   - **モデル貧血症 (Anemic Domain Model) アンチパターン**
      - [[データコンテナとしてのオブジェクトと、手続き的なサービス]]
      - [[ドメインロジックの欠如]]
      - [[リッチなドメインモデルとの対比]]
   - **ドメインモデルのテスト**
      - [[ユニットテスト (エンティティ、値オブジェクト、ドメインサービス)]]
      - [[集約の不変条件のテスト]]
      - [[リポジトリのテスト (モックまたはインメモリDB)]]
   - **チーム体制とコミュニケーション**
      - [[DDDとアジャイル開発]]
      - [[ドメイン専門家のプロジェクトへの関与]]

## 7. [[DDDの進化と関連する考え方 MOC]]
   - **DDDとマイクロサービスアーキテクチャ**
      - [[境界づけられたコンテキストとマイクロサービスの境界]]
      - [[マイクロサービスにおける集約とイベント]]
   - **リアクティブDDD (Reactive DDD)**
   - **関数型DDD (Functional DDD)**
      - [[不変性、純粋関数とDDDビルディングブロック]]
   - **最新のDDDに関する書籍やコミュニティ**
   - **DDDディストルド (DDD Distilled - Vaughn Vernon)** (より軽量なアプローチ)
