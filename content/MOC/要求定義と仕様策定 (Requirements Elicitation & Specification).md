---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/requirements-elicitation-and-specification
---
## 1. [[要求工学入門 MOC]]
   - **要求 (Requirement) とは何か**
      - [[要求の定義 (ユーザーのニーズやビジネス目標を達成するためにシステムが満たすべき条件や能力)]]
      - [[なぜ要求定義が重要か (プロジェクト失敗の最大の原因は要求の不備)]]
   - **[[要求工学 (Requirements Engineering) の定義とプロセス MOC]]**
      - `[[1. 要求引き出し (Elicitation)]]`
      - `[[2. 要求分析 (Analysis)]]`
      - `[[3. 要求仕様策定 (Specification)]]`
      - `[[4. 要求の妥当性確認 (Validation)]]`
      - `[[5. 要求管理 (Management)]]`
   - **良い要求の特性**
      - `[[明確性 (Unambiguous)]]`
      - `[[検証可能性 (Testable / Verifiable)]]`
      - `[[一貫性 (Consistent)]]`
      - `[[完全性 (Complete)]]`
      - `[[実現可能性 (Feasible)]]`
      - `[[優先順位付け可能 (Prioritized)]]`
      - `[[理解可能性 (Understandable)]]`
   - **[[ステークホルダー (Stakeholder) の特定と分析 MOC]]**
      - [[ステークホルダーとは (プロジェクトに関心を持つ全ての人々)]]
      - `[[主要なステークホルダーの種類 (ユーザー, 顧客, 経営者, 開発者, 法務, サポートなど)]]`
      - `[[ステークホルダー分析 (関心と影響力のマッピング)]]`
      - `[[ステークホルダーとの効果的なコミュニケーション]]`

## 2. [[要求引き出し (Requirements Elicitation) MOC]]
   - **要求引き出しの目的 (ステークホルダーの頭の中にあるニーズを明文化する)**
   - **要求引き出しの課題** (要求が不明確, 暗黙の要求, 対立する要求)
   - **主要な要求引き出しテクニック**
      - **[[インタビュー (Interviews) MOC]]**
         - `[[構造化、半構造化、非構造化インタビュー]]`
         - `[[効果的な質問技法 (オープンエンド, クローズドエンド, 5W1H)]]`
         - `[[インタビューの計画、実施、記録]]`
      - **[[ワークショップ (Workshops) MOC]]**
         - `[[ブレインストーミング]]`
         - `[[JAD (Joint Application Development) セッション]]`
      - **[[アンケート調査 (Questionnaires / Surveys) MOC]]**
         - `[[定量的データの収集]]`
         - `[[良いアンケートの設計]]`
      - **[[観察 (Observation) MOC]]**
         - `[[フィールドワーク / エスノグラフィ調査]]`
         - `[[文脈的調査 (Contextual Inquiry)]]`
         - `[[ユーザーの実際の行動から暗黙のニーズを発見]]`
      - **[[プロトタイピング (Prototyping) MOC]]**
         - `[[プロトタイプを通じた要求の具体化とフィードバック収集]]`
         - `[[ペーパープロトタイプからインタラクティブプロトタイプまで]]`
      - **[[シナリオとストーリーテリング (Scenarios and Storytelling) MOC]]**
         - `[[具体的な利用状況を物語として記述]]`
      - **[[ドキュメント分析 (Document Analysis)]]** (既存の仕様書、業務マニュアル、競合製品の分析)
      - **[[フォーカスグループ (Focus Groups)]]**
   - **テクニックの選択と組み合わせ**

## 3. [[要求分析と交渉 (Requirements Analysis and Negotiation) MOC]]
   - **要求分析の目的 (引き出した要求を整理・構造化し、矛盾や曖昧さを解消する)**
   - **要求のモデル化 (Requirements Modeling)**
      - **[[ユースケース (Use Cases) MOC]]**
         - `[[ユースケース図の作成 (アクター, ユースケース, 関係)]]`
         - `[[ユースケース記述 (基本フロー, 代替フロー, 例外フロー)]]`
      - **[[データモデリング (ER図など)]]** (データベース設計MOCと連携)
      - **[[状態遷移モデリング (状態遷移図)]]**
      - **[[プロセスマッピング (ビジネスプロセスモデリング - BPMNなど)]]**
   - **[[要求の優先順位付け (Prioritization) MOC]]**
      - `[[MoSCoW法 (Must, Should, Could, Won't)]]`
      - `[[KANOモデル (狩野モデル)]]` (当たり前品質, 一元的品質, 魅力的品質)
      - `[[重要度と緊急度のマトリクス]]`
      - `[[加重スコアリング (Weighted Scoring)]]`
   - **[[要求のコンフリクト解決と交渉 (Conflict Resolution and Negotiation)]]**
      - `[[ステークホルダー間の要求の対立]]`
      - `[[トレードオフ分析]]`
      - `[[交渉戦略]]`

## 4. [[要求仕様策定 (Requirements Specification) MOC]]
   - **仕様策定の目的 (分析・合意された要求を明確かつ一貫性のある形式で文書化する)**
   - **仕様書の読者 (開発者, テスター, PM, ステークホルダー)**
   - **[[ソフトウェア要求仕様書 (SRS - Software Requirements Specification) MOC]]** (伝統的アプローチ)
      - `[[SRSの標準的な構成 (IEEE 830など)]]`
         - `[[1. 序論 (目的, スコープ, 用語定義)]]`
         - `[[2. 全体概要 (製品の全体像, 機能, ユーザー特性, 制約)]]`
         - `[[3. 詳細な要求 (機能要件, 非機能要件, 外部インターフェース要件)]]`
      - `[[良いSRSの書き方]]`
   - **[[アジャイル開発における仕様策定 MOC]]**
      - **[[ユーザーストーリー (User Stories) MOC]]**
         - [[ユーザーストーリーの形式 (`As a <user role>, I want <goal> so that <reason>`)]]
         - `[[INVESTモデル (Independent, Negotiable, Valuable, Estimable, Small, Testable)]]`
         - `[[受け入れ基準 (Acceptance Criteria)]]`
         - `[[ユーザーストーリーマッピング]]`
      - `[[フィーチャー (Features) とエピック (Epics)]]`
      - **[[プロダクトバックログ (Product Backlog)]]** (生きた仕様書)
   - **[[ユースケース記述 (Use Case Specification) MOC]]** (再掲・文書化として)
   - **視覚的な仕様記述**
      - `[[ワイヤーフレームとモックアップ]]`
      - `[[プロトタイプ]]`
      - `[[UML (Unified Modeling Language) ダイアグラム]]` (ユースケース図, アクティビティ図, シーケンス図, 状態マシン図など)
   - **仕様書の言語**
      - `[[自然言語の曖昧さを避ける工夫]]`
      - `[[専門用語集 (Glossary) の作成]]` (ユビキタス言語と連携)

## 5. [[要求の妥当性確認 (Requirements Validation) MOC]]
   - **妥当性確認の目的 (仕様化された要求がステークホルダーの真のニーズを満たしているか確認する)**
   - **妥当性確認と検証 (Validation vs. Verification)**
      - `[[Validation: 正しいものを作っているか (Are we building the right thing?)]]`
      - `[[Verification: それを正しく作っているか (Are we building the thing right?)]]`
   - **妥当性確認のテクニック**
      - **[[レビューとインスペクション]]**
         - `[[ウォークスルー]]`
         - `[[技術的レビュー]]`
         - `[[形式的インスペクション]]`
      - **[[プロトタイピングによる確認]]**
      - **[[テストケースの早期作成]]**
      - **[[シミュレーション]]**
      - **[[ユーザーによる受け入れテスト (UAT)]]** (最終段階での妥当性確認)

## 6. [[要求管理 (Requirements Management) MOC]]
   - **要求管理の目的 (プロジェクトライフサイクル全体を通して要求への変更を管理する)**
   - **要求管理の主要な活動**
      - **[[要求のベースライン設定]]**
      - **[[変更管理 (Change Management)]]**
         - `[[変更要求の受付と影響分析]]`
         - `[[変更管理委員会 (CCB - Change Control Board)]]`
         - `[[変更の承認プロセス]]`
      - **[[トレーサビリティ (Traceability) の確保]]**
         - `[[要求トレーサビリティマトリクス]]`
         - `[[前方トレーサビリティ (要求→設計→実装→テスト)]]`
         - `[[後方トレーサビリティ (テスト→設計→要求)]]`
      - `[[バージョニングと履歴管理]]`
   - **要求管理ツール** (JIRA, Confluence, Doorsなど)

## 7. [[要求の種類 MOC]]

### 7.1. [[機能要件 (Functional Requirements) MOC]]
   - [[機能要件の定義 (システムが「何をするか」)]]
   - `[[特定の入力に対するシステムの振る舞い]]`
   - `[[業務プロセスとルール]]`
   - `[[認証と認可のルール]]`
   - `[[レポートとデータ出力]]`
   - `[[機能要件の記述方法 (ユースケース, ユーザーストーリーなど)]]`

### 7.2. [[非機能要件 (Non-Functional Requirements - NFRs) / 品質特性 MOC]]
   - [[非機能要件の定義 (システムが「どのように動作するか」、品質や制約)]]
   - **主要な非機能要件のカテゴリ**
      - **[[性能 (Performance)]]**
         - `[[応答時間 (Response Time)]]`
         - `[[スループット (Throughput)]]`
         - `[[リソース使用率 (CPU, Memory)]]`
      - **[[可用性 (Availability)]]**
         - `[[稼働率 (Uptime - 例: 99.99%)]]`
         - `[[平均故障間隔 (MTBF), 平均修復時間 (MTTR)]]`
      - **[[信頼性 (Reliability)]]**
      - **[[スケーラビリティ (Scalability)]]** (拡張性)
      - **[[セキュリティ (Security)]]**
         - `[[認証, 認可, 暗号化, 監査ログなど]]`
      - **[[ユーザビリティ (Usability)]]** (使いやすさ)
      - **[[保守性 (Maintainability)]]**
      - **[[移植性 (Portability)]]**
      - `[[(オプション) 相互運用性 (Interoperability)]]`
      - `[[(オプション) コンプライアンスと法規制]]`
   - [[非機能要件の定量化と検証可能性]]

### 7.3. [[その他の要求分類 MOC]]
   - **[[ビジネス要件 (Business Requirements)]]** (高レベルな目標)
   - **[[ユーザー要件 (User Requirements)]]** (ユーザーがシステムで達成したいこと)
   - **[[システム要件 (System Requirements)]]** (機能要件と非機能要件の詳細)
   - **[[制約条件 (Constraints)]]** (技術的、予算的、時間的な制約)

## 8. [[開発手法と要求 MOC]]

### 8.1. [[アジャイル開発における要求の扱い MOC]]
   - `[[要求の進化と継続的な発見]]`
   - **[[プロダクトバックログ (Product Backlog)]]**
      - `[[生きた要求文書としてのバックログ]]`
      - `[[バックログリファインメント (グルーミング)]]`
   - **[[ユーザーストーリーと受け入れ基準]]** (再掲)
   - **[[スプリント計画と要求の具体化]]**
   - **[[ステークホルダーとの頻繁なコミュニケーション]]**

### 8.2. [[ウォーターフォール開発における要求定義 MOC]]
   - `[[要求定義フェーズの重要性]]`
   - `[[ベースライン化と厳格な変更管理]]`
   - `[[詳細なソフトウェア要求仕様書 (SRS) の作成]]`
   - `[[ウォーターフォールにおける要求定義の課題]]` (手戻りコストの大きさ)

## 9. [[要求定義・仕様策定のベストプラクティスとアンチパターン MOC]]
   - **ベストプラクティス**
      - `[[早期から全てのステークホルダーを巻き込む]]`
      - `[[視覚的なモデルを多用する]]`
      - `[[専門用語集を作成し、共通言語を確立する]]`
      - `[[要求に優先順位を付ける]]`
      - `[[要求を検証可能にする]]`
      - `[[変更を歓迎し、管理するプロセスを持つ]]`
   - **アンチパターン**
      - `[[不完全な要求引き出し]]`
      - `[[ゴールドプレーティング (Gold Plating - 過剰品質)]]`
      - `[[スコープクリープ (Scope Creep - 要求の際限ない追加)]]`
      - `[[分析麻痺 (Analysis Paralysis)]]`
      - `[[曖昧で検証不可能な要求]]`
      - `[[ユーザーの不在]]`
      - `[[要求とソリューションの混同]]`

## 10. [[ツールとリソース MOC]]
   - **要求管理ツール**
      - `[[JIRA, Trello, Asana]]` (アジャイル向け)
      - `[[Confluence, Notion]]` (ドキュメント管理)
      - `[[IBM DOORS, Jama Connect]]` (大規模/厳格なプロジェクト向け)
   - **モデリング/ダイアグラムツール**
      - `[[draw.io, Lucidchart, Miro]]`
      - `[[UMLモデリングツール]]`
   - **プロトタイピングツール**
      - `[[Figma, Sketch, Adobe XD]]`
   - **主要な書籍、標準 (IEEE 830など)、コミュニティ**
