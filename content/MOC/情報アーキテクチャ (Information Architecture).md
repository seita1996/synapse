---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/information-architecture
---
## 1. [[情報アーキテクチャ入門 MOC]]
   - **情報アーキテクチャとは何か**
      - [[情報アーキテクチャの定義 (情報を分かりやすくし、見つけやすくするための構造設計の技術と科学)]]
      - [[IAの目的 (ユーザビリティの向上、タスク達成の支援、コンテンツ価値の最大化)]]
      - `[[提唱者と主要書籍 (リチャード・ソウル・ワーマン, ピーター・モービル & ルイス・ローゼンフェルドの『シロクマ本』)]]`
   - **なぜIAが重要か**
      - `[[認知負荷の軽減]]`
      - `[[ユーザーの満足度と信頼の向上]]`
      - `[[ビジネス目標の達成支援 (コンバージョン率向上など)]]`
      - `[[コンテンツの持続可能性とスケーラビリティの確保]]`
   - **[[IAの3つのサークル (情報生態学) MOC]]**
      - **[[コンテキスト (Context)]]** (ビジネス目標、制約、文化、リソース)
      - **[[コンテンツ (Content)]]** (データ、ドキュメント、オブジェクト、メタデータ)
      - **[[ユーザー (Users)]]** (ターゲット層、ニーズ、情報探索行動)
      - `[[3つのサークルの重なりの中に最適なIAが存在する]]`
   - **IAと関連分野との関係**
      - `[[UXデザインにおけるIAの位置づけ]]`
      - `[[UIデザインとの違い (構造 vs. 表現)]]`
      - `[[コンテンツ戦略との連携]]`
      - `[[SEO (検索エンジン最適化) との関連]]`

## 2. [[情報アーキテクチャの構成要素 (4つのシステム) MOC]]

### 2.1. [[1. 組織化システム (Organization Systems) MOC]]
   - **組織化システムとは (情報のグループ化と分類の仕組み)**
   - **組織化スキーム (Organization Schemes)**
      - **[[厳密な組織化スキーム (Exact Organization Schemes)]]** (客観的、既知情報探索向け)
         - `[[アルファベット順 (Alphabetical)]]`
         - `[[時系列順 (Chronological)]]`
         - `[[地理的順 (Geographical)]]`
      - **[[曖昧な組織化スキーム (Ambiguous Organization Schemes)]]** (主観的、ブラウジング向け)
         - **[[トピック別 (Topical)]]**
         - **[[タスク指向 (Task-oriented)]]**
         - **[[オーディエンス別 (Audience-specific)]]**
         - `[[メタファー (Metaphor)]]` (注意が必要)
      - `[[ハイブリッドスキーム (複数のスキームの組み合わせ)]]`
   - **組織化の構造 (Organization Structures)**
      - **[[階層構造 (Hierarchy / Tree Structure)]]** (トップダウン)
         - `[[階層の幅と深さのバランス]]`
      - **[[データベースモデル / シーケンシャル構造]]** (ボトムアップ)
      - `[[ハイパーテキスト構造 (Hypertext)]]`
      - `[[(オプション) ファセット分類 (Faceted Classification)]]` (複数のフィルターで絞り込み)

### 2.2. [[2. ラベリングシステム (Labeling Systems) MOC]]
   - **ラベリングシステムとは (情報の表現方法、名前の付け方)**
   - **良いラベルの条件**
      - `[[ユーザーの語彙に合わせる]]`
      - `[[一貫性を保つ]]`
      - `[[明確で誤解を招かない]]`
      - `[[簡潔であること]]`
   - **ラベルの種類**
      - `[[ナビゲーションのラベル (リンクテキスト)]]`
      - `[[見出し (Headings)]]`
      - `[[インデックスタグ (Index Terms)]]`
      - `[[アイコンラベル]]`
   - **ラベリングシステムの設計プロセス**
      - `[[コンテンツ分析とユーザーリサーチから候補を抽出]]`
      - `[[競合サイトのラベリング調査]]`
      - `[[ユーザーテストによる検証]]`
   - **ラベリングのアンチパターン** (専門用語の乱用、一貫性のないラベルなど)

### 2.3. [[3. ナビゲーションシステム (Navigation Systems) MOC]]
   - **ナビゲーションシステムとは (ユーザーが情報空間を移動するための手段)**
   - **ナビゲーションの種類**
      - **[[グローバルナビゲーション (Global Navigation)]]** (サイト全体で一貫して表示)
      - **[[ローカルナビゲーション (Local Navigation)]]** (特定のセクション内での移動)
      - **[[コンテキストナビゲーション (Contextual Navigation)]]** (関連コンテンツへのリンク)
      - `[[(オプション) 補足的ナビゲーション (Supplemental Navigation - サイトマップ, インデックス)]]`
   - **ナビゲーションのUIパターン**
      - `[[ナビゲーションバー (ヘッダーナビゲーション)]]`
      - `[[パンくずリスト (Breadcrumbs)]]`
      - `[[フッターナビゲーション (Fat Footer)]]`
      - `[[タブ (Tabs)]]`
      - `[[ドロップダウンメニュー / メガメニュー]]`
      - `[[サイドバーナビゲーション]]`
      - `[[ページネーション (Pagination)]]`
      - `[[関連リンク]]`
      - `[[ファセットナビゲーション (Faceted Navigation)]]`
   - **埋め込みナビゲーション (Embedded Navigation)**
      - `[[文中のハイパーリンク]]`
   - **良いナビゲーションの設計原則**
      - `[[現在地を示す]]`
      - `[[移動経路を示す]]`
      - `[[行き先を予測可能にする]]`
      - `[[一貫性を保つ]]`

### 2.4. [[4. 検索システム (Searching Systems) MOC]]
   - **検索システムとは (ユーザーがクエリを入力して情報を探す手段)**
   - **検索システムの構成要素**
      - `[[検索インターフェース (検索ボックス、検索ボタン)]]`
      - `[[クエリ言語 (Query Language)]]` (キーワード, ブーリアン演算, フレーズ検索など)
      - `[[検索アルゴリズムとインデックス]]`
      - `[[検索結果の表示 (Search Results)]]`
   - **良い検索システムの設計**
      - `[[検索ボックスの配置とデザイン]]`
      - `[[オートコンプリート / サジェスト機能]]`
      - `[[高度な検索機能]]`
      - `[[検索結果の順序付け (ランキング)]]`
      - `[[検索結果のスニペット表示]]`
      - `[[検索結果のフィルタリングとソート]]`
      - `[["検索結果がありません" ページの設計]]`
   - **検索ログ分析** (ユーザーのニーズ理解)

## 3. [[IAの設計プロセス MOC]]
   - **[[フェーズ1: リサーチとディスカバリー MOC]]**
      - `[[目的とスコープの定義]]`
      - `[[ステークホルダーインタビューの実施]]`
      - `[[ユーザーリサーチの実施 (インタビュー, ペルソナ作成)]]`
      - `[[競合分析]]`
      - `[[コンテンツインベントリとコンテンツ監査]]`
   - **[[フェーズ2: 戦略と構造設計 MOC]]**
      - `[[トップダウンアプローチ vs. ボトムアップアプローチ]]`
      - `[[組織化スキームと構造の決定]]`
      - `[[ラベリングシステムの開発]]`
      - `[[主要なナビゲーションパスの設計]]`
      - `[[カードソーティングの実施と分析]]`
      - `[[コンセプトモデル/メンタルモデルの作成]]`
   - **[[フェーズ3: ドキュメンテーションと実装 MOC]]**
      - `[[サイトマップの作成]]`
      - `[[ユーザーフロー図の作成]]`
      - `[[ワイヤーフレームの作成 (IAの視点から)]]`
      - `[[ナビゲーション仕様書の作成]]`
      - `[[コンテンツモデルとタクソノミーの定義]]`
      - `[[開発者やデザイナーとの連携]]`
   - **[[フェーズ4: 評価と改善 MOC]]**
      - `[[ツリーテストの実施]]`
      - `[[ユーザビリティテストによるナビゲーションの評価]]`
      - `[[クリックテスト / ファーストクリックテスト]]`
      - `[[アクセス解析データに基づく改善]]`
      - `[[IAの継続的なメンテナンス]]`

## 4. [[IA設計のための主要な手法とテクニック MOC]] (再掲・集約)
   - **[[コンテンツインベントリ (Content Inventory) とコンテンツ監査 (Content Audit) MOC]]**
      - `[[インベントリの作成方法 (スプレッドシートなど)]]`
      - `[[監査の評価軸 (ROT - Redundant, Obsolete, Trivial)]]`
   - **[[カードソーティング (Card Sorting) MOC]]**
      - `[[カードソーティングの定義と目的 (ユーザーのメンタルモデルを理解する)]]`
      - **[[オープンカードソーティング]]** (ユーザーが自由にグループ化)
      - **[[クローズドカードソーティング]]** (事前に定義されたカテゴリに分類)
      - `[[ハイブリッドカードソーティング]]`
      - `[[カードソーティングの実施手順と分析方法 (類似度マトリクス, デンドログラム)]]`
      - `[[オンラインカードソーティングツール (OptimalSortなど)]]`
   - **[[ツリーテスト (Tree Testing / Reverse Card Sorting) MOC]]**
      - `[[ツリーテストの定義と目的 (IAの構造の有効性を検証する)]]`
      - `[[ツリーテストの実施手順と分析方法 (成功率, 直接性, 所要時間)]]`
      - `[[オンラインツリーテストツール (Treejackなど)]]`
   - **[[ユーザーフロー (User Flow) とタスク分析 (Task Analysis) MOC]]**
      - `[[ユーザーが特定の目標を達成するためのステップを可視化]]`
   - **[[サイトマップ (Sitemap) MOC]]**
      - `[[サイトマップの種類 (視覚的サイトマップ, XMLサイトマップ)]]`
      - `[[サイトマップの作成方法とツール]]`
   - **[[ワイヤーフレーム (Wireframe) MOC]]** (IAの視点から)
      - `[[ページレベルでのIAの具体化]]`
      - `[[ナビゲーション要素とコンテンツの配置]]`

## 5. [[IAの成果物 (Deliverables) MOC]]
   - `[[競合分析レポート]]`
   - `[[ユーザーリサーチレポート (ペルソナ, ジャーニーマップ)]]`
   - `[[コンテンツインベントリ/監査スプレッドシート]]`
   - `[[カードソーティング/ツリーテスト結果レポート]]`
   - `[[サイトマップ]]`
   - `[[ユーザーフロー図 / タスクフロー図]]`
   - `[[ワイヤーフレーム / プロトタイプ]]`
   - `[[ナビゲーション仕様書]]`
   - `[[コンテンツモデル / タクソノミー定義書]]`
   - `[[ラベリング仕様書]]`

## 6. [[IAの原則とベストプラクティス MOC]]
   - **Peter Morville の UX Honeycomb** (Useful, Usable, Desirable, Findable, Accessible, Credible, Valuable)
   - **Abby Covert の 10 Principles of IA**
   - **8つの情報アーキテクチャの原則 (by Dan Brown)**
      - `[[オブジェクトの原則 (Principle of Objects)]]`
      - `[[選択の原則 (Principle of Choices)]]`
      - `[[開示の原則 (Principle of Disclosure)]]`
      - `[[模範の原則 (Principle of Exemplars)]]`
      - `[[フロントドアの原則 (Principle of Front Doors)]]`
      - `[[多重分類の原則 (Principle of Multiple Classification)]]`
      - `[[フォーカスナビゲーションの原則 (Principle of Focused Navigation)]]`
      - `[[成長の原則 (Principle of Growth)]]`
   - **その他のベストプラクティス**
      - `[[ユーザーの言語を使う]]`
      - `[[一貫性を保つ]]`
      - `[[認知負荷を減らす]]`
      - `[[コンテキストを提供する]]`
      - `[[失敗からの回復を容易にする]]`

## 7. [[様々なコンテキストにおけるIA MOC]]
   - `[[大規模WebサイトのIA]]`
   - `[[eコマースサイトのIA]]` (ファセットナビゲーションの重要性)
   - `[[モバイルアプリケーションのIA]]` (画面サイズの制約)
   - `[[エンタープライズシステム / イントラネットのIA]]`
   - `[[音声ユーザーインターフェース (VUI) のIA]]`
   - `[[オムニチャネル体験におけるIA]]`

## 8. [[IAのためのツールとリソース MOC]]
   - **マインドマッピングツール** (XMind, MindMeister)
   - **ダイアグラム作成ツール** (draw.io, Lucidchart, Miro, FigJam)
   - **カードソーティング/ツリーテストツール** (Optimal Workshop)
   - **ワイヤーフレーム/プロトタイピングツール** (Figma, Sketch, Adobe XD)
   - **主要な書籍、ブログ、コミュニティ**
