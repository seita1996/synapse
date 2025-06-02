---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/api-design
---
## 1. [[API設計入門 MOC]]
   - **APIとは何か**
      - [[API (Application Programming Interface) の定義と役割]]
      - [[APIの種類 (ライブラリAPI, OS API (システムコール), Web API)]]
      - [[内部API (Internal API) vs. 外部API (External/Public API) vs. パートナーAPI (Partner API)]]
   - **API設計の重要性**
      - [[なぜAPI設計が重要か (ソフトウェア間の連携、再利用性、モジュール性)]]
      - [[APIエコシステムとビジネス価値]]
      - [[開発者体験 (DX - Developer Experience) とAPI設計]]
   - **良いAPIの特性**
      - [[使いやすさ (Usability) / 学習しやすさ (Learnability)]]
      - [[分かりやすさ (Understandability) / 明確性 (Clarity)]]
      - [[発見しやすさ (Discoverability)]]
      - [[一貫性 (Consistency)]]
      - [[予測可能性 (Predictability)]]
      - [[柔軟性 (Flexibility) と拡張性 (Extensibility)]]
      - [[信頼性 (Reliability) と堅牢性 (Robustness)]]
      - [[効率性 (Efficiency) / パフォーマンス]]
      - [[セキュリティ (Security)]]
      - [[テスト容易性 (Testability)]]
      - [[保守性 (Maintainability)]]
   - **API設計の基本原則**
      - **[[API-First Design (APIファースト設計)]]**
         - [[APIファーストアプローチの利点と進め方]]
      - [[契約による設計 (Design by Contract) とAPI]]
      - [[関心の分離 (Separation of Concerns) とAPI設計]]
      - [[最小驚きの原則 (Principle of Least Astonishment) の適用]]
   - **APIの利用者と提供者**
      - [[APIコンシューマー (API Consumer) の視点]]
      - [[APIプロバイダー (API Provider) の視点]]
      - [[API利用者と提供者間のコミュニケーションとフィードバック]]

## 2. [[APIスタイルとパラダイム MOC]]
   - **[[REST (Representational State Transfer) API設計 MOC]]**
      - [[RESTの定義と6つのアーキテクチャ制約]]
         - `[[クライアントサーバ (Client-Server)]]`
         - `[[ステートレス (Stateless)]]`
         - `[[キャッシュ可能 (Cacheable)]]`
         - `[[統一インターフェース (Uniform Interface)]]`
            - `[[リソースの識別 (Identification of resources - URI)]]`
            - `[[表現を通じたリソース操作 (Manipulation of resources through representations)]]`
            - `[[自己記述的メッセージ (Self-descriptive messages)]]`
            - `[[HATEOAS (Hypermedia as the Engine of Application State)]]`
         - `[[階層化システム (Layered System)]]`
         - `[[コードオンデマンド (Code-On-Demand - オプション)]]`
      - [[リソース (Resource) の概念とモデリング]]
      - [[表現 (Representation) の概念 (JSON, XMLなど)]]
      - `[[HTTPメソッドのセマンティクスとREST (GET, POST, PUT, DELETE, PATCHなど)]]` (詳細は後述)
      - `[[HTTPステータスコードの利用とREST]]` (詳細は後述)
      - [[REST APIの冪等性と安全性]]
      - [[Richardson Maturity Model (RMM) - RESTの成熟度レベル]] (Level 0-3)
      - [[REST API設計のベストプラクティスとアンチパターン]]
      - `[[具体的なREST API設計例 (例: ブログAPI, eコマースAPI)]]`
   - **[[GraphQL API設計 MOC]]**
      - [[GraphQLの定義と目的 (柔軟なデータ取得、単一エンドポイント)]]
      - [[GraphQLの主要な概念]]
         - `[[スキーマ定義言語 (SDL - Schema Definition Language)]]`
         - `[[型システム (Type System - Object, Scalar, Enum, Interface, Union, Input)]]`
         - `[[クエリ (Query)]]`
         - `[[ミューテーション (Mutation)]]`
         - `[[サブスクリプション (Subscription)]]` (リアルタイム更新)
         - `[[リゾルバ (Resolver)]]`
      - [[GraphQLとRESTの比較 (利点と欠点)]]
         - `[[オーバーフェッチとアンダーフェッチの問題解決]]`
      - [[GraphQLのベストプラクティス (スキーマ設計、エラー処理、ページネーション)]]
      - [[GraphQLクライアントライブラリ (Apollo, Relayなど)]]
      - `[[具体的なGraphQLスキーマ設計例]]`
   - **[[gRPC (gRPC Remote Procedure Calls) API設計 MOC]]**
      - [[gRPCの定義と目的 (高性能なRPCフレームワーク)]]
      - [[gRPCの主要な概念]]
         - `[[Protocol Buffers (Protobuf)によるインターフェース定義言語 (IDL)]]`
         - `[[サービス定義とメッセージ型]]`
         - `[[RPCの種類 (Unary, Server streaming, Client streaming, Bidirectional streaming)]]`
         - `[[HTTP/2ベースのトランスポート]]`
         - `[[コード生成]]`
      - [[gRPCとREST/GraphQLの比較]] (パフォーマンス、ストリーミング、型安全性)
      - [[gRPCのベストプラクティス (エラー処理、デッドライン、メタデータ)]]
      - [[gRPCの利用例 (マイクロサービス間通信、モバイルクライアント)]]
   - **[[WebSockets API設計 MOC]]**
      - [[WebSocketsの定義と目的 (双方向リアルタイム通信)]]
      - [[WebSocketsハンドシェイクとプロトコル]]
      - [[メッセージベース通信]]
      - [[WebSocketsの利用例 (チャットアプリ、リアルタイムゲーム、ライブ通知)]]
      - [[WebSocketsと他のリアルタイム技術 (ロングポーリング、SSE) との比較]]
   - **[[Webhook API設計 MOC]]** (リバースAPI)
      - [[Webhookの定義と目的 (イベント発生時の非同期通知)]]
      - [[Webhookの仕組み (HTTP POSTによるコールバック)]]
      - [[Webhook設計のベストプラクティス (セキュリティ、再試行、冪等性)]]
      - [[Webhookの利用例 (CI/CDパイプライン連携、外部サービス連携)]]
   - **[[(オプション) SOAP (Simple Object Access Protocol) API MOC]]** (概要、歴史、RESTとの比較)
      - [[XMLベース、WSDL、UDDI]]
   - **[[(オプション) RPC (Remote Procedure Call) スタイルのAPI設計 MOC]]** (一般的な概念、JSON-RPCなど)
   - **[[各APIスタイルの選択基準とトレードオフ]]**

## 3. [[API設計の一般原則とベストプラクティス MOC]]
   - **[[リソース指向設計 (Resource-Oriented Design)]]** (主にREST向け)
      - [[リソースの適切な粒度と命名]]
      - [[リソース間の関連性の表現]]
   - **[[APIの一貫性 (Consistency) MOC]]**
      - [[命名規則 (URI, パラメータ, フィールド)]]
      - [[データフォーマットの一貫性]]
      - [[エラーレスポンスの一貫性]]
      - [[振る舞いの一貫性]]
   - **[[予測可能性 (Predictability) と直感性]]**
      - [[APIの挙動が利用者の期待通りであること]]
   - **[[シンプルさと最小限の驚き (Simplicity and Principle of Least Astonishment)]]**
      - [[APIの学習コスト低減]]
      - [[不必要な複雑性の排除]]
   - **[[柔軟性と拡張性 (Flexibility and Extensibility)]]**
      - [[将来の変更に対応できる設計]]
      - [[後方互換性の考慮]]
   - **[[状態管理 (Statelessness vs. Stateful APIs)]]**
      - [[ステートレスAPIの利点 (スケーラビリティ、キャッシュ容易性)]]
      - [[ステートフルAPIが必要なケースと注意点]]
   - **[[冪等性 (Idempotency) の設計 MOC]]**
      - [[冪等な操作の定義 (何度実行しても結果が同じ)]]
      - [[HTTPメソッドと冪等性 (GET, PUT, DELETEは冪等)]]
      - [[冪等性を保証するための設計 (リクエストIDなど)]]
   - **[[APIエラー処理設計 MOC]]** (詳細は後述のセキュリティとエラー処理セクションで)
   - **[[APIパフォーマンス考慮事項 MOC]]**
      - [[ペイロードサイズの最適化 (必要なデータのみ返す、圧縮)]]
      - [[リクエスト数の削減 (バッチ処理、GraphQL)]]
      - [[キャッシュ戦略]] (詳細は後述)
      - [[非同期処理の活用]]
   - **[[APIセキュリティ設計 MOC]]** (詳細は後述のセキュリティセクションで)
   - **[[APIバージョニング戦略 MOC]]** (詳細は後述のバージョニングセクションで)
   - **[[APIドキュメンテーション MOC]]** (詳細は後述のドキュメンテーションセクションで)
   - **[[APIのテスト容易性設計]]**
   - **[[API開発者体験 (DX) の向上]]** (使いやすいSDK、分かりやすいエラー、豊富なドキュメント)

## 4. [[Web API設計の詳細 (主にHTTPベース) MOC]]

### 4.1. [[URI設計 (URI Design) MOC]]
   - [[URIの構造 (スキーム, ホスト, パス, クエリ, フラグメント)]]
   - [[リソース指向のURI設計]]
      - [[名詞の使用 (複数形推奨)]]
      - [[階層構造の表現]]
      - [[具体的なリソースとコレクションリソース]]
   - [[URI設計のベストプラクティス]]
      - [[小文字の使用]]
      - [[ハイフン (`-`) vs. アンダースコア (`_`)]]
      - [[末尾スラッシュ (`/`) の扱い]]
      - [[ファイル拡張子を含めない]]
      - [[CRUD操作をURIに含めない (HTTPメソッドで表現)]]
   - `[[URI設計の例]]`

### 4.2. [[HTTPメソッドの適切な利用 MOC]]
   - **[[GET]]**: リソースの取得 (安全、冪等)
   - **[[POST]]**: リソースの新規作成、またはサブリソースの作成、他のメソッドで表現できない操作 (冪等でない)
   - **[[PUT]]**: リソースの完全な更新または作成 (冪等)
   - **[[DELETE]]**: リソースの削除 (冪等)
   - **[[PATCH]]**: リソースの部分的な更新 (冪等であるべきだが、実装による)
   - **[[HEAD]]**: GETと同様だがレスポンスボディなし (メタデータ取得) (安全、冪等)
   - **[[OPTIONS]]**: リソースがサポートするメソッドの取得 (CORS) (安全、冪等)
   - [[メソッドの安全性と冪等性の理解と適用]]

### 4.3. [[HTTPステータスコードの適切な利用 MOC]]
   - **カテゴリ別ステータスコード**
      - `[[1xx: 情報 (Informational)]]` (Continue, Switching Protocols)
      - `[[2xx: 成功 (Successful)]]`
         - `[[200 OK]]`
         - `[[201 Created]]`
         - `[[202 Accepted]]`
         - `[[204 No Content]]`
      - `[[3xx: リダイレクション (Redirection)]]`
         - `[[301 Moved Permanently]]`
         - `[[302 Found / 303 See Other / 307 Temporary Redirect]]`
         - `[[304 Not Modified]]`
      - `[[4xx: クライアントエラー (Client Error)]]`
         - `[[400 Bad Request]]`
         - `[[401 Unauthorized]]` (認証失敗)
         - `[[403 Forbidden]]` (認可失敗)
         - `[[404 Not Found]]`
         - `[[405 Method Not Allowed]]`
         - `[[406 Not Acceptable]]`
         - `[[409 Conflict]]`
         - `[[415 Unsupported Media Type]]`
         - `[[422 Unprocessable Entity]]` (バリデーションエラー)
         - `[[429 Too Many Requests]]` (レート制限)
      - `[[5xx: サーバエラー (Server Error)]]`
         - `[[500 Internal Server Error]]`
         - `[[502 Bad Gateway]]`
         - `[[503 Service Unavailable]]`
         - `[[504 Gateway Timeout]]`
   - [[エラーレスポンスボディとの連携]] (詳細はエラー処理設計で)

### 4.4. [[リクエスト/レスポンスヘッダ設計 MOC]]
   - **標準HTTPヘッダの活用**
      - `[[Content-Type]]` (リクエスト/レスポンスボディのメディアタイプ)
      - `[[Accept]]` (クライアントが受け入れ可能なメディアタイプ)
      - `[[Authorization]]` (認証情報)
      - `[[Cache-Control, ETag, Last-Modified, Expires]]` (キャッシュ制御)
      - `[[Location]]` (リソース作成時やリダイレクト時)
      - `[[User-Agent]]`
      - `[[Allow]]` (サポートするHTTPメソッド)
      - `[[Content-Length]]`
      - `[[Content-Encoding]]` (gzipなど)
      - `[[Link]]` (HATEOAS, ページネーション)
   - **カスタムヘッダ (`X-`プレフィックスなど)**
      - [[カスタムヘッダの利用シーンと注意点]]

### 4.5. [[データフォーマット (Data Formats) MOC]]
   - **[[JSON (JavaScript Object Notation)]]**
      - [[JSONの構文とデータ型]]
      - [[JSONの利点 (軽量、可読性、多くの言語でサポート)]]
      - [[JSON設計のベストプラクティス (命名規則: snake_case vs. camelCase)]]
   - **[[XML (Extensible Markup Language)]]**
      - [[XMLの構文と特徴 (タグ、属性、スキーマ)]]
      - [[XMLの利点と欠点 (冗長性、強力なスキーマ定義)]]
      - [[JSON vs. XML]]
   - **[[Protocol Buffers (Protobuf)]]**
      - [[Protobufのスキーマ定義 (.protoファイル)]]
      - [[Protobufの利点 (効率的なシリアライズ、型安全性、後方互換性)]]
      - [[gRPCとの連携]]
   - **[[(オプション) MessagePack, Apache Avro, Apache Thrift]]**
   - **[[Content Negotiation (コンテントネゴシエーション)]]** (`Accept`ヘッダと`Content-Type`ヘッダによるフォーマット選択)

### 4.6. [[ペイロード設計 (Payload Design) MOC]]
   - **リクエストボディ設計**
      - [[POST, PUT, PATCHリクエストのボディ構造]]
      - [[入力バリデーションの考慮]]
   - **レスポンスボディ設計**
      - [[成功レスポンスとエラーレスポンスの構造]]
      - [[データ構造の一貫性]]
      - [[エンベロープ (Envelope) の利用是非]] (例: `data`フィールドでラップする)
      - [[必要な情報のみを含める (オーバーフェッチの回避)]]
      - [[関連リソースの埋め込み (Embedding) vs. リンク (Linking)]]
      - [[Null値の扱い]]
      - [[日付と時刻のフォーマット (ISO 8601推奨)]]
   - **命名規則の重要性** (フィールド名)

### 4.7. [[ページネーション (Pagination) MOC]]
   - [[なぜページネーションが必要か (大量データの効率的な配信)]]
   - **ページネーションの種類**
      - `[[オフセットベースページネーション (Offset-based / Page-based)]]` (`page`, `limit` / `offset`, `limit`)
         - [[利点と欠点 (データ追加/削除時の問題)]]
      - `[[カーソルベースページネーション (Cursor-based / Keyset-based)]]`
         - [[利点と欠点 (高パフォーマンス、安定性)]]
   - [[ページネーション情報のレスポンスへの含め方]] (`Link`ヘッダ、レスポンスボディ内)

### 4.8. [[フィルタリング (Filtering) MOC]]
   - [[クエリパラメータによるリソースのフィルタリング]] (例: `?status=active&type=admin`)
   - [[フィルタリングパラメータの設計と命名]]
   - [[複雑なフィルタリング条件の表現方法]]

### 4.9. [[ソート (Sorting) MOC]]
   - [[クエリパラメータによる結果のソート]] (例: `?sort_by=name&order=asc`)
   - [[複数キーによるソート]]
   - [[デフォルトのソート順]]

### 4.10. [[検索 (Searching) MOC]]
   - [[部分一致検索、全文検索のAPI設計]]
   - [[検索クエリパラメータの設計]] (例: `?q=keyword`)

### 4.11. [[レート制限 (Rate Limiting) とスロットリング (Throttling) MOC]]
   - [[レート制限の目的 (APIの保護、公平な利用)]]
   - [[レート制限の方式 (固定ウィンドウ、スライディングウィンドウ、トークンバケット、リーキーバケット)]]
   - [[レート制限情報のクライアントへの通知]] (`X-RateLimit-Limit`, `X-RateLimit-Remaining`, `X-RateLimit-Reset`ヘッダ, `429 Too Many Requests`ステータス)

### 4.12. [[キャッシュ戦略 (Caching Strategies) MOC]]
   - **HTTPキャッシュ**
      - `[[Cache-Control` ヘッダ (`public`, `private`, `no-cache`, `no-store`, `max-age`)]]
      - `[[Expires` ヘッダ]]
      - `[[ETag` ヘッダと条件付きリクエスト (`If-None-Match`)]]
      - `[[Last-Modified` ヘッダと条件付きリクエスト (`If-Modified-Since`)]]
   - [[クライアントサイドキャッシュ、プロキシキャッシュ、サーバサイドキャッシュ]]
   - [[キャッシュ無効化戦略 (Cache Invalidation)]]

### 4.13. [[HATEOAS (Hypermedia as the Engine of Application State) MOC]]
   - [[HATEOASの定義と目的 (APIの自己発見性、クライアントとサーバの疎結合)]]
   - [[レスポンスに次の操作や関連リソースへのリンクを含める]]
   - [[`Link`ヘッダやレスポンスボディ内でのリンク表現 (HAL, JSON Hyper-Schema, Sirenなど)]]
   - [[HATEOASの利点と実装の複雑性]]

### 4.14. [[国際化 (i18n) と地域化 (l10n) の考慮]]
   - `[[Accept-Language` ヘッダによる言語指定]]
   - `[[Content-Language` ヘッダによるレスポンス言語指定]]
   - [[日付、時刻、数値、通貨フォーマットの地域化]]

## 5. [[APIセキュリティ MOC]]
   - **[[認証 (Authentication) MOC]]**
      - `[[Basic認証]]` (非推奨)
      - `[[APIキー (API Keys)]]`
      - **[[OAuth 2.0 / OpenID Connect (OIDC) MOC]]**
         - `[[OAuth 2.0のロール (Resource Owner, Client, Authorization Server, Resource Server)]]`
         - `[[OAuth 2.0のフロー (Authorization Code, Implicit (非推奨), Client Credentials, Resource Owner Password Credentials (非推奨))]]`
         - `[[アクセストークンとリフレッシュトークン]]`
         - `[[OIDCと認証レイヤー]]`
      - **[[JSON Web Token (JWT) MOC]]**
         - `[[JWTの構造 (Header, Payload, Signature)]]`
         - `[[JWTの利用シナリオと注意点]]`
      - `[[(オプション) mTLS (Mutual TLS)]]`
   - **[[認可 (Authorization) MOC]]**
      - [[認証されたユーザー/クライアントが何をしてよいかを決定]]
      - **[[ロールベースアクセス制御 (RBAC - Role-Based Access Control)]]**
      - **[[属性ベースアクセス制御 (ABAC - Attribute-Based Access Control)]]**
      - [[OAuth 2.0におけるスコープ (Scopes)]]
   - **入力検証 (Input Validation)**
      - [[全てのクライアント入力を検証する (パラメータ、ヘッダ、ボディ)]]
      - [[データ型、フォーマット、長さ、範囲の検証]]
      - [[インジェクション攻撃対策 (SQLインジェクション、XSSなど)]]
   - **出力エンコーディング (Output Encoding)**
      - [[コンテキストに応じた適切なエンコーディング (HTML, JavaScript, URL)]]
   - **機密データの扱い**
      - [[ペイロードやログにおける機密情報のマスキングまたは暗号化]]
      - [[PCI DSS, HIPAAなどのコンプライアンス要件]]
   - **[[TLS/SSLによる通信暗号化 (HTTPSの強制)]]**
   - **[[OWASP API Security Top 10 とその対策 MOC]]**
      - `[[API1:2023 Broken Object Level Authorization]]`
      - `[[API2:2023 Broken Authentication]]`
      - `[[API3:2023 Broken Object Property Level Authorization]]`
      - `[[API4:2023 Unrestricted Resource Consumption]]`
      - `[[API5:2023 Broken Function Level Authorization]]`
      - `[[API6:2023 Unrestricted Access to Sensitive Business Flows]]`
      - `[[API7:2023 Server Side Request Forgery (SSRF)]]`
      - `[[API8:2023 Security Misconfiguration]]`
      - `[[API9:2023 Improper Inventory Management]]`
      - `[[API10:2023 Unsafe Consumption of APIs]]`
   - **[[(オプション) APIキーのローテーションと管理]]**
   - **[[(オプション) シークレット管理 (Secret Management)]]**

## 6. [[APIのバージョニング MOC]]
   - [[なぜAPIバージョニングが必要か (破壊的変更からの保護、クライアントの移行期間)]]
   - **[[非破壊的変更と破壊的変更の区別]]**
      - [[非破壊的変更の例 (新しいエンドポイント/フィールドの追加、オプションパラメータの追加)]]
      - [[破壊的変更の例 (エンドポイント/フィールドの削除・リネーム、必須パラメータの追加、データ型の変更、認証方法の変更)]]
   - **[[バージョニング戦略 (Versioning Strategies) MOC]]**
      - **[[URIパスによるバージョニング (`/v1/resource`)]]** (最も一般的)
         - [[利点と欠点]]
      - **[[クエリパラメータによるバージョニング (`?version=1`)]]**
         - [[利点と欠点]]
      - **[[カスタムリクエストヘッダによるバージョニング (`X-API-VERSION: 1`)]]**
         - [[利点と欠点]]
      - **[[Acceptヘッダによるバージョニング (メディアタイプバージョニング - `Accept: application/vnd.example.v1+json`)]]**
         - [[利点と欠点 (RESTの原則に忠実)]]
   - [[バージョニングのベストプラクティス]]
      - [[可能な限り破壊的変更を避ける]]
      - [[明確なバージョニングポリシーを持つ]]
      - [[古いバージョンのサポート期間と廃止通知]]
   - [[バージョニングしない戦略 (継続的進化 - 例: GraphQL)]] (課題と対策)

## 7. [[APIドキュメンテーション MOC]]
   - **APIドキュメンテーションの重要性** (開発者体験、採用促進)
   - **良いAPIドキュメントの構成要素**
      - [[概要と導入 (APIの目的、利用開始方法)]]
      - [[認証方法の説明]]
      - [[エンドポイントの一覧と詳細 (HTTPメソッド、URI、パラメータ、ヘッダ)]]
      - [[リクエスト/レスポンスのデータ構造と例]]
      - [[エラーコードとエラーメッセージの一覧]]
      - [[レート制限とクォータ]]
      - [[バージョニングポリシー]]
      - [[SDKとクライアントライブラリの情報]]
      - [[チュートリアルとユースケース例]]
      - [[用語集]]
      - [[サポートと連絡先]]
   - **[[API仕様フォーマット (API Specification Formats) MOC]]**
      - **[[OpenAPI Specification (OAS) / Swagger MOC]]**
         - [[OASの構造 (YAML/JSON)]]
         - [[OASの利点 (ドキュメント自動生成、コード自動生成、テスト自動生成)]]
         - [[Swagger Editor, Swagger UI, Swagger Codegen]]
      - **[[RAML (RESTful API Modeling Language)]]** (概要と比較)
      - **[[API Blueprint]]** (Markdownベース - 概要と比較)
   - **[[インタラクティブなAPIドキュメントの提供]]** ("Try it out"機能)
   - **ドキュメントの自動生成と手動記述のバランス**
   - **ドキュメントのバージョニングとメンテナンス**
   - **APIドキュメントホスティングツール** (Stoplight, ReadMe, Postman Docsなど)

## 8. [[APIテスト MOC]]
   - **APIテストの重要性と目的**
   - **APIテストの種類**
      - **[[APIユニットテスト]]** (個々のエンドポイントや機能のテスト)
      - **[[API統合テスト]]** (複数のAPIコンポーネント間の連携テスト)
      - **[[API契約テスト (Contract Testing)]]**
         - `[[コンシューマ駆動契約テスト (Consumer-Driven Contract Testing - CDC)]]`
         - `[[Pact, Spring Cloud Contractなどのツール]]`
      - **[[API End-to-End (E2E) テスト]]**
      - **[[APIパフォーマンステスト (負荷テスト、ストレステスト)]]**
      - **[[APIセキュリティテスト]]** (脆弱性スキャン、ペネトレーションテスト)
      - **[[APIユーザビリティテスト]]** (ドキュメントやSDKの使いやすさ)
   - **APIテスト戦略**
      - [[テストピラミッドとAPIテスト]]
      - [[テストデータの管理]]
   - **APIテストツール**
      - `[[Postman / Newman]]`
      - `[[RestAssured (Java)]]`
      - `[[Requests (Python) + PyTest]]`
      - `[[Jest / Supertest (JavaScript)]]`
      - `[[k6, JMeter (パフォーマンステスト)]]`
   - **[[モック (Mock) とスタブ (Stub) の利用]]**
   - **APIテストの自動化とCI/CDパイプラインへの統合**

## 9. [[APIライフサイクル管理 MOC]]
   - **APIライフサイクルのフェーズ**
      - **[[1. 計画と設計 (Planning and Design)]]** (要件定義、スタイル選択、仕様策定)
      - **[[2. 開発と実装 (Development and Implementation)]]**
      - **[[3. テストと検証 (Testing and Validation)]]**
      - **[[4. デプロイと公開 (Deployment and Publication)]]** (APIゲートウェイ、開発者ポータル)
      - **[[5. 運用と監視 (Operation and Monitoring)]]**
         - `[[APIモニタリング (可用性、パフォーマンス、エラーレート)]]`
         - `[[APIロギング (リクエスト/レスポンスログ、監査ログ)]]`
         - `[[APIアナリティクス (利用状況分析)]]`
      - **[[6. バージョン管理と進化 (Versioning and Evolution)]]**
      - **[[7. 廃止 (Deprecation and Retirement)]]** (通知、移行期間、シャットダウン)
   - **[[APIゲートウェイ (API Gateway) の役割 MOC]]**
      - [[リクエストルーティング、レート制限、認証/認可、キャッシュ、ロギング、モニタリング、リクエスト/レスポンス変換]]
      - [[代表的なAPIゲートウェイ製品 (AWS API Gateway, Apigee, Kong, Tykなど)]]
   - **[[API開発者ポータル (API Developer Portal)]]** (ドキュメント、APIキー管理、アナリティクス提供)
   - **APIガバナンス (API Governance)**
      - [[API設計標準とガイドラインの策定と遵守]]
      - [[APIレビュープロセス]]
      - [[APIカタログとインベントリ管理]]

## 10. [[API設計アンチパターン MOC]]
   - **リソース設計のアンチパターン**
      - `[[チャッティAPI (Chatty API) / 細かすぎるリソース]]`
      - `[[ゴッドAPI (God API / Monolithic API Endpoint) / 粗すぎるリソース]]`
      - `[[動詞を使ったURI (`/getUsers`, `/createUser`)]]`
      - `[[URIにコンテキストを含めすぎる (`/tenant/123/department/456/employee/789`)]]`
   - **リクエスト/レスポンス設計のアンチパターン**
      - `[[一貫性のない命名規則やデータフォーマット]]`
      - `[[不必要なデータの公開 (オーバーフェッチ)]]`
      - `[[必要なデータが一度に取得できない (アンダーフェッチ)]]`
      - `[[レスポンスエンベロープの乱用]]`
   - **HTTP利用のアンチパターン**
      - `[[不適切なHTTPメソッドの使用 (例: GETで状態変更)]]`
      - `[[不適切なHTTPステータスコードの使用 (例: エラーなのに200 OK)]]`
      - `[[全てのエラーを200 OKで返し、ボディでエラー内容を伝える]]`
   - **エラー処理のアンチパターン**
      - `[[貧弱なエラー報告 (情報不足、不明瞭)]]`
      - `[[スタックトレースなどの機密情報をそのまま返す]]`
   - **バージョニングのアンチパターン**
      - `[[バージョニングの欠如]]`
      - `[[頻繁すぎる破壊的変更]]`
      - `[[多数のバージョンを永続的にサポート]]`
   - **ドキュメンテーションのアンチパターン**
      - `[[ドキュメントが存在しない、または不十分]]`
      - `[[ドキュメントが古く、現状と乖離している]]`
   - **セキュリティのアンチパターン**
      - `[[認証/認可の不備]]`
      - `[[入力検証の欠如]]`
      - `[[HTTPS未使用]]`
