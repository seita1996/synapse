---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/agile-principles
---
## 1. [[アジャイル入門 MOC]]
   - **アジャイルとは何か**
      - [[アジャイルの定義 (不確実性に対応し、価値を迅速かつ継続的に提供するための反復的・協調的なアプローチと考え方)]]
      - [[アジャイルは特定の方法論ではなく、マインドセットである]]
   - **アジャイルの歴史と背景**
      - `[[ウォーターフォールモデルの課題 (硬直性、手戻りコスト)]]`
      - `[[軽量なソフトウェア開発手法の台頭]]`
      - **[[2001年のアジャイルソフトウェア開発宣言の策定]]**
   - **アジャイル開発の全体像**
      - `[[経験主義の三本柱 (透明性, 検査, 適応)]]`
      - `[[反復 (Iteration) とインクリメント (Increment)]]`
      - `[[フィードバックループの重要性]]`
   - **アジャイルの主要な方法論 (概観)**
      - `[[スクラム (Scrum)]]`
      - `[[カンバン (Kanban)]]`
      - `[[エクストリームプログラミング (XP - Extreme Programming)]]`
      - `[[リーンソフトウェア開発 (Lean Software Development)]] `

## 2. [[アジャイルソフトウェア開発宣言 (The Agile Manifesto) MOC]]
   - **[[宣言の背景と署名者たち]]**
   - **[[アジャイル宣言の4つの価値 (The 4 Values) MOC]]**
      - `[["〜よりも (over)" の正しい解釈 (左側を重視するが、右側の価値も認める)]]`
      - ---
      - **[[価値1: プロセスやツールよりも個人と対話を (Individuals and interactions over processes and tools) MOC]]**
         - `[[価値1の解説: ツールやプロセスは人を助けるためにあるが、創造性や問題解決は人々の対話から生まれる]]`
         - `[[実践例: デイリースタンドアップ, ペアプログラミング, 対面での会話, チームでの意思決定]]`
         - `[[アンチパターン: ツールへの過度な依存, コミュニケーション不足, 形骸化したミーティング]]`
      - ---
      - **[[価値2: 包括的なドキュメントよりも動くソフトウェアを (Working software over comprehensive documentation) MOC]]**
         - `[[価値2の解説: 最終的な目標は動くソフトウェアであり、ドキュメントはそのための手段に過ぎない]]`
         - `[[実践例: 頻繁なデモ, ユーザーストーリー, 実行可能な仕様 (BDD), 自己文書化コード]]`
         - `[[アンチパターン: 過剰なドキュメント作成, ドキュメントと実装の乖離, 動かないソフトウェア]]`
         - `[[アジャイルにおけるドキュメントの適切な扱い方]]`
      - ---
      - **[[価値3: 契約交渉よりも顧客との協調を (Customer collaboration over contract negotiation) MOC]]**
         - `[[価値3の解説: 顧客は対立する相手ではなく、共に価値を創造するパートナーである]]`
         - `[[実践例: プロダクトオーナー/顧客のチームへの参加, 定期的なフィードバックセッション, ユーザーストーリーの共作]]`
         - `[[アンチパターン: 要求の厳格な固定化, 変更要求への抵抗, 契約を盾にした対立]]`
         - `[[アジャイル契約の考え方]]`
      - ---
      - **[[価値4: 計画に従うことよりも変化への対応を (Responding to change over following a plan) MOC]]**
         - `[[価値4の解説: 不確実な世界では、変化は避けられない。変化を脅威ではなく機会と捉える]]`
         - `[[実践例: 短いイテレーション, 継続的な優先順位見直し, バックログリファインメント, CI/CD]]`
         - `[[アンチパターン: 詳細すぎる長期計画への固執, 変更への抵抗, スコープクリープへの無策]]`
         - `[[アジャイルにおける計画の役割 (ロードマップ vs. 詳細計画)]]`

## 3. [[アジャイル宣言の背後にある12の原則 MOC]]

### 3.1. [[原則1: 顧客満足 (Customer Satisfaction) MOC]]
   - `[[原文: Our highest priority is to satisfy the customer through early and continuous delivery of valuable software.]]`
   - `[[解説: 顧客満足を最優先し、価値のあるソフトウェアを早く継続的に提供します。]]`
   - `[[実践: MVP (実用最小限の製品), 短いリリースサイクル, ユーザーフィードバックの収集と反映]]`
   - `[[関連プラクティス: 継続的デリバリー (CD), ユーザーストーリーマッピング]]`

### 3.2. [[原則2: 変化への歓迎 (Welcome Change) MOC]]
   - `[[原文: Welcome changing requirements, even late in development. Agile processes harness change for the customer's competitive advantage.]]`
   - `[[解説: 要求の変更は、たとえ開発の後半であっても歓迎します。変化を味方につける俊敏さが重要です。]]`
   - `[[実践: 短いイテレーション, プロダクトバックログの柔軟な管理, アーキテクチャの進化]]`
   - `[[関連プラクティス: 反復的開発, YAGNI原則, 進化するアーキテクチャ]]`

### 3.3. [[原則3: 頻繁なリリース (Frequent Delivery) MOC]]
   - `[[原文: Deliver working software frequently, from a couple of weeks to a couple of months, with a preference to the shorter timescale.]]`
   - `[[解説: 動くソフトウェアを、できるだけ短い時間間隔でリリースします。これによりフィードバックループが加速します。]]`
   - `[[実践: スクラムのスプリント, CI/CDパイプライン, カナリアリリース]]`
   - `[[関連プラクティス: CI/CD, DevOps, スプリント]]`

### 3.4. [[原則4: 協力 (Collaboration) MOC]]
   - `[[原文: Business people and developers must work together daily throughout the project.]]`
   - `[[解説: ビジネス側の人と開発者は、プロジェクトを通して毎日一緒に働かなければなりません。]]`
   - `[[実践: プロダクトオーナーの役割, デイリースクラム, チームへのビジネスゴールの共有]]`
   - `[[関連プラクティス: クロスファンクショナルチーム, 顧客開発]]`

### 3.5. [[原則5: 信頼とモチベーション (Trust and Motivation) MOC]]
   - `[[原文: Build projects around motivated individuals. Give them the environment and support they need, and trust them to get the job done.]]`
   - `[[解説: 意欲に満ちた人々を集め、環境と支援を与え、仕事が成し遂げられると信頼して任せます。]]`
   - `[[実践: 自己組織的なチーム, 心理的安全性, サーバントリーダーシップ, 権限委譲]]`
   - `[[関連プラクティス: 自己組織化, 心理的安全性, サーバントリーダーシップ]]`

### 3.6. [[原則6: フェイス・トゥ・フェイスの対話 (Face-to-face Conversation) MOC]]
   - `[[原文: The most efficient and effective method of conveying information to and within a development team is face-to-face conversation.]]`
   - `[[解説: 情報を伝える最も効率的で効果的な方法は、フェイス・トゥ・フェイスで話をすることです。]]`
   - `[[実践: デイリースタンドアップ, ペアプログラミング, ホワイトボードでのディスカッション, チームの物理的な配置]]`
   - `[[リモートワークにおけるこの原則の適用 (ビデオ会議, 仮想ホワイトボード)]]`

### 3.7. [[原則7: 動くソフトウェア (Working Software) MOC]]
   - `[[原文: Working software is the primary measure of progress.]]`
   - `[[解説: 動くソフトウェアこそが進捗の最も重要な尺度です。]]`
   - `[[実践: スプリントレビュー/デモ, 受け入れテスト駆動開発(ATDD), Doneの定義]]`
   - `[[アンチパターン: 進捗率(%)による報告, "90%完了"症候群]]`
   - `[[関連プラクティス: Doneの定義, 受け入れテスト]]`

### 3.8. [[原則8: 持続可能なペース (Sustainable Pace) MOC]]
   - `[[原文: Agile processes promote sustainable development. The sponsors, developers, and users should be able to maintain a constant pace indefinitely.]]`
   - `[[解説: アジャイル･プロセスは持続可能な開発を促進します。関係者は一定のペースを維持できなければなりません。]]`
   - `[[実践: 無理のないスプリント計画, 残業の常態化防止, ベロシティの安定化, 心理的安全性]]`
   - `[[アンチパターン: デスマーチ, バーンアウト]]`
   - `[[関連プラクティス: ベロシティ, Yesterday's Weather]]`

### 3.9. [[原則9: 技術的卓越性 (Technical Excellence) MOC]]
   - `[[原文: Continuous attention to technical excellence and good design enhances agility.]]`
   - `[[解説: 技術的卓越性と優れた設計に対する不断の注意が、機敏さを高めます。]]`
   - `[[実践: テスト駆動開発(TDD), リファクタリング, ペアプログラミング, コードレビュー, CI/CD, 設計原則(SOLID)]]`
   - `[[技術的負債とその返済]]`
   - `[[関連プラクティス: TDD, BDD, リファクタリング, CI, 設計原則]]`

### 3.10. [[原則10: シンプルさ (Simplicity) MOC]]
   - `[[原文: Simplicity--the art of maximizing the amount of work not done--is essential.]]`
   - `[[解説: シンプルさ（ムダなく作れる量を最大限にすること）は不可欠です。]]`
   - `[[実践: YAGNI (You Ain't Gonna Need It) 原則, MVP, シンプルな設計の選択]]`
   - `[[アンチパターン: ゴールドプレーティング (過剰品質), 将来のための過剰な設計]]`
   - `[[関連プラクティス: YAGNI, MVP, KISS原則]]`

### 3.11. [[原則11: 自己組織化 (Self-organizing Teams) MOC]]
   - `[[原文: The best architectures, requirements, and designs emerge from self-organizing teams.]]`
   - `[[解説: 最良のアーキテクチャ・要求・設計は、自己組織的なチームから生み出されます。]]`
   - `[[実践: チームによるタスク割り当てと見積もり, チームでの設計決定, 権限委譲]]`
   - `[[マイクロマネジメントの弊害]]`
   - `[[関連プラクティス: スクラムチーム, プランニングポーカー]]`

### 3.12. [[原則12: 振り返りと改善 (Retrospection and Adaptation) MOC]]
   - `[[原文: At regular intervals, the team reflects on how to become more effective, then tunes and adjusts its behavior accordingly.]]`
   - `[[解説: チームは、どうすればもっと効果的になれるかを定期的に振り返り、それに基づいて自分たちのやり方を調整します。]]`
   - **[[レトロスペクティブ (ふりかえり) の実践]]**
      - `[[レトロスペクティブの目的と重要性]]`
      - `[[レトロスペクティブの進め方 (KPT, Fun/Done/Learn, Starfishなど)]]`
      - `[[心理的安全性の確保]]`
      - `[[アクションアイテムの創出と追跡]]`
   - `[[継続的改善 (Kaizen) の精神]]`

## 4. [[アジャイル原則の実践と応用 MOC]]
   - **[[アジャイル原則とスクラム MOC]]**
      - `[[スクラムの各イベント (スプリント計画, デイリースクラム, スプリントレビュー, レトロスペクティブ) と原則の対応]]`
      - `[[スクラムの3つの役割 (PO, SM, 開発者) と原則の対応]]`
      - `[[スクラムの成果物 (プロダクトバックログ, スプリントバックログ, インクリメント) と原則の対応]]`
   - **[[アジャイル原則とカンバン MOC]]**
      - `[[カンバンのプラクティス (可視化, WIP制限, フロー管理) と原則の対応]]`
   - **[[アジャイル原則とエクストリームプログラミング (XP) MOC]]**
      - `[[XPのプラクティス (ペアプログラミング, TDD, CIなど) と原則の対応]]`
   - **原則をチームに導入する方法**
   - **原則の遵守度を測るための自己評価**

## 5. [[アジャイルマインドセット MOC]]
   - **[[Doing Agile vs. Being Agile の違い MOC]]** (プラクティスの実践 vs. 価値と原則の体現)
   - **アジャイルマインドセットを構成する要素**
      - `[[経験主義 (Empiricism)]]` (再掲)
      - `[[リーン思考 (Lean Thinking)]]` (ムダの排除)
      - `[[グロースマインドセット (Growth Mindset)]]` (学習と成長)
      - `[[サーバントリーダーシップ (Servant Leadership)]]`
      - `[[心理的安全性 (Psychological Safety)]]`
   - **チームと組織におけるアジャイルマインドセットの醸成**

## 6. [[アジャイル原則への批判とよくある誤解 MOC]]
   - `[[「アジャイルは計画が不要」という誤解 → 継続的な計画と適応]]`
   - `[[「アジャイルはドキュメントが不要」という誤解 → 価値のあるドキュメントを適切な量だけ]]`
   - `[[「アジャイルは規律が不要でカオスだ」という誤解 → 高い自己規律が求められる]]`
   - `[[「アジャイルは設計をしない」という誤解 → 創発的設計と継続的リファクタリング]]`
   - `[[大規模プロジェクトやミッションクリティカルなシステムへの適用の難しさという批判とそれに対する反論/アプローチ]]`
   - `[[アジャイルの商業化と形骸化 (カーゴカルトアジャイル)]]`

## 7. [[関連リソース MOC]]
   - **主要な書籍** (『アジャイルソフトウェア開発宣言』, 『Clean Agile』, 『エクストリームプログラミング』など)
   - **主要な提唱者とブログ** (Kent Beck, Martin Fowler, Robert C. Martinなど)
   - **関連コミュニティとカンファレンス** (Agile Alliance, Scrum Alliance, Agile Japanなど)
