---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/value-stream-mapping
---
## 1. [[VSM入門とリーン思考 MOC]]
   - **バリューストリームマッピングとは**
      - [[VSMの定義 (製品やサービスが顧客に届くまでのプロセス全体を可視化し、価値の流れとムダを分析・改善する手法)]]
      - [[VSMの目的 (リードタイムの短縮, プロセス効率の向上, ムダの削減, 継続的改善)]]
      - [[なぜ「マッピング」が重要か (全体像の把握、共通認識の醸成、問題点の特定)]]
   - **[[リーン思考 (Lean Thinking) とVSMの関係 MOC]]**
      - `[[リーン思考の起源 (トヨタ生産方式 - TPS)]]`
      - **[[リーンの5つの原則]]**
         - `[[1. 価値の特定 (Specify Value)]]`
         - `[[2. バリューストリームの特定 (Identify the Value Stream)]]`
         - `[[3. フローの創造 (Create Flow)]]`
         - `[[4. プルシステムの確立 (Establish Pull)]]`
         - `[[5. 完璧の追求 (Pursue Perfection)]]`
      - `[[VSMはリーン原則を実践するためのツール]]`
   - **VSMの適用分野**
      - `[[製造業 (起源)]]`
      - `[[ソフトウェア開発とDevOps]]`
      - `[[オフィス業務・サービス業]]`
      - `[[ヘルスケア]]`
      - `[[サプライチェーンマネジメント]]`

## 2. [[VSMのコアコンセプト MOC]]
   - **[[価値 (Value)]]**
      - `[[顧客視点での価値の定義]]`
      - **[[価値創造活動 (Value-Added Activities)]]** (顧客が対価を払う活動)
      - **[[非価値創造活動 (Non-Value-Added Activities)]]** (ムダ)
         - `[[必要だが非価値創造な活動 (Type 1 Muda)]]` (例: 法規制対応)
         - `[[純粋なムダ (Type 2 Muda)]]`
   - **[[バリューストリーム (Value Stream)]]**
      - `[[バリューストリームの定義 (価値を届けるための一連の活動の流れ)]]`
      - `[[製品ファミリーの特定]]`
   - **[[フロー (Flow)]]**
      - `[[フローの定義 (作業や情報が淀みなく流れる状態)]]`
      - `[[フローを妨げる要因 (ボトルネック, 停滞)]]`
   - **[[プル (Pull)]]**
      - `[[プルシステムの定義 (後工程が必要なものを、必要な時に、必要なだけ引き取る)]]`
      - `[[プッシュシステムとの違い]]`
   - **[[ムダ (Waste / Muda) MOC]]**
      - `[[ムダの定義 (価値を生まない全ての活動)]]`
      - **[[トヨタ生産方式の7つのムダ (TIMWOOD)]]**
         - `[[1. 運搬のムダ (Transport)]]`
         - `[[2. 在庫のムダ (Inventory)]]`
         - `[[3. 動作のムダ (Motion)]]`
         - `[[4. 待ちのムダ (Waiting)]]`
         - `[[5. 過剰生産のムダ (Over-production)]]}`
         - `[[6. 過剰加工のムダ (Over-processing)]]`
         - `[[7. 不良・手直しのムダ (Defects)]]`
      - `[[(オプション) 8番目のムダ: 未活用の人材 (Skills / Non-utilized talent)]]`
      - **[[ソフトウェア開発における8つのムダ]]**
         - `[[部分的に完成した作業 (在庫)]]`
         - `[[余分な機能 (過剰生産)]]`
         - `[[再学習 (不良)]]`
         - `[[ハンドオフ (運搬)]]`
         - `[[タスクスイッチング (動作)]]`
         - `[[遅延 (待ち)]]`
         - `[[ゴールドプレーティング (過剰加工)]]`
         - `[[未活用のスキル]]`

## 3. [[VSMの実践プロセス MOC]]

### 3.1. [[ステップ1: 準備とスコープ定義 MOC]]
   - **VSMの目的と目標設定**
   - **対象となる製品ファミリーまたはプロセスの選定**
   - **チームの編成** (クロスファンクショナルなチームが理想)
   - **VSMワークショップの計画**
   - **スポンサーシップと関係者の巻き込み**

### 3.2. [[ステップ2: 現状のバリューストリームマップ作成 (Current State Mapping) MOC]]
   - **プロセスの「現地現物」での観察 (Go See / Gemba Walk)**
   - **プロセスのステップを右から左へ（顧客から上流へ）書き出す**
   - **各プロセスのデータボックスに指標を記入** (詳細は指標セクションで)
      - `[[サイクルタイム (C/T)]]`
      - `[[切替時間 (C/O)]]`
      - `[[アップタイム (Uptime)]]`
      - `[[在庫数 (Inventory)]]`
   - **情報フローの描き方** (手動情報、電子情報)
   - **マテリアル/成果物のフローの描き方**
      - `[[プッシュ矢印 (`→`)]]`
   - **リードタイムラダー (Lead Time Ladder) の作成**
      - `[[プロセスタイム (付加価値時間) と待ち時間の分離]]`
      - `[[総リードタイムと総プロセスタイムの計算]]`
   - **現状マップの完成と共有**

### 3.3. [[ステップ3: 現状の分析と問題特定 MOC]]
   - **現状マップの分析**
      - `[[ムダの特定 (7つ+1のムダの観点から)]]`
      - `[[ボトルネックの特定 (サイクルタイムが最も長いプロセス)]]`
      - `[[フローが停滞している箇所の特定 (長い待ち時間)]]`
      - `[[プロセスのばらつきの特定]]`
   - **[[改善の機会の特定 (カイゼンバースト)]]**
   - **根本原因分析 (Root Cause Analysis)**
      - `[[なぜなぜ5回 (Five Whys)]]` (再掲・VSM文脈)
      - `[[魚の骨図 (Fishbone Diagram)]]`
   - **[[プロセスサイクル効率 (Process Cycle Efficiency - PCE) の計算]]**
      - `[[PCE = (総プロセスタイム / 総リードタイム) * 100]]`

### 3.4. [[ステップ4: 将来のあるべき姿マップ作成 (Future State Mapping) MOC]]
   - **将来の状態に関するビジョンの設定**
   - **リーン原則に基づいた改善アイデアの適用**
      - **[[継続的なフローの設計]]**
         - `[[プロセスの結合]]`
         - `[[セルの形成 (Cellular Manufacturing)]]`
      - **[[プルシステムの導入]]**
         - `[[スーパーマーケット (Supermarket)]]` (後工程のための在庫置き場)
         - `[[カンバン (Kanban)]]` (引き取りの合図)
      - **[[タクトタイム (Takt Time) の計算]]**
         - `[[タクトタイム = (利用可能な稼働時間) / (顧客需要)]]`
      - **[[ペースメーカープロセス (Pacemaker Process) の設定]]**
         - `[[顧客に最も近い、連続的なフローで生産をスケジューリングできる単一のポイント]]`
      - **[[生産の平準化 (Heijunka)]]**
         - `[[量の平準化と種類の平準化]]`
   - **将来のあるべき姿マップの描画**

### 3.5. [[ステップ5: 実施計画の作成と実行 MOC]]
   - **現状から将来への移行計画**
      - `[[具体的な改善項目 (カイゼン) のリストアップと優先順位付け]]`
   - **実施計画の作成**
      - `[[各改善項目の担当者、期限、評価指標を設定]]`
      - `[[バリューストリームループ (Value Stream Loops) による分割]]`
   - **PDCAサイクルによる継続的改善**
      - `[[Plan (計画) → Do (実行) → Check (評価) → Act (改善)]]`
   - **バリューストリームマネージャーの役割**
   - **定期的なレビューとマップの更新**

## 4. [[VSMの記号と指標 MOC]]

### 4.1. [[VSMの主要な記号 (Icons) MOC]]
   - **プロセスの記号**
      - `[[プロセスボックス]]`
      - `[[顧客/サプライヤー]]`
      - `[[データボックス]]`
   - **マテリアル/成果物の記号**
      - `[[在庫 (Inventory)]]` (三角)
      - `[[プッシュ矢印 (Push Arrow)]]`
      - `[[スーパーマーケット (Supermarket)]]`
      - `[[プル (Pull)]]` (引き取りカンバン)
      - `[[FIFOレーン]]`
      - `[[出荷 (Shipment)]]`
   - **情報の記号**
      - `[[手動情報フロー]]`
      - `[[電子情報フロー]]`
      - `[[カンバンポスト]]`
      - `[[Go See (現地現物)]]`
      - `[[生産管理/スケジューリング]]`
   - **一般的な記号**
      - `[[カイゼンバースト (Kaizen Burst)]]`
      - `[[オペレーター]]`
      - `[[タイムライン (Lead Time Ladder)]]`

### 4.2. [[VSMの主要な指標 (Metrics) MOC]]
   - **時間に関する指標**
      - **[[サイクルタイム (C/T - Cycle Time)]]** (1つの製品/タスクを完了させる時間)
      - **[[リードタイム (L/T - Lead Time)]]** (注文から納品までの総時間)
      - **[[プロセスタイム (P/T - Process Time) / 付加価値時間 (Value-Added Time)]]**
      - **[[切替時間 (C/O - Changeover Time)]]**
      - **[[タクトタイム (Takt Time)]]**
   - **品質と効率に関する指標**
      - **[[アップタイム (Uptime)]]** (設備やシステムが稼働している時間の割合)
      - **[[在庫 (Inventory)]]** (仕掛品 - WIP)
      - **[[初回通過率 (First Time Yield - FTY) / 直行率]]**
      - **[[プロセスサイクル効率 (PCE - Process Cycle Efficiency)]]**

## 5. [[ソフトウェア開発とDevOpsにおけるVSM MOC]]
   - **DevOpsバリューストリーム** (アイデアから顧客価値提供、フィードバックまで)
   - **ソフトウェア開発における「ムダ」の再定義**
      - `[[部分的に完成したコード (在庫)]]`
      - `[[不要な機能 (過剰生産)]]`
      - `[[バグ (不良)]]`
      - `[[チーム間のハンドオフ (運搬)]]`
      - `[[タスクスイッチング (動作)]]`
      - `[[承認待ち、ビルド待ち (待ち)]]`
      - `[[過剰なプロセス、手作業 (過剰加工)]]`
      - `[[サイロ化によるスキルの未活用]]`
   - **現状マップの作成 (ソフトウェア開発版)**
      - `[[プロセスの洗い出し (企画→設計→開発→テスト→リリース→運用)]]`
      - `[[各プロセスのリードタイムとプロセスタイムの計測]]`
      - `[[ツールチェーンの可視化]]`
   - **将来のあるべき姿の設計 (ソフトウェア開発版)**
      - `[[CI/CDパイプラインによるフローの改善]]`
      - `[[カンバンボードによるWIP制限とプルシステムの実現]]`
      - `[[自動化による手作業の削減]]`
      - `[[フィードバックループの高速化]]`
   - **DevOpsにおける主要指標**
      - `[[デプロイ頻度 (Deployment Frequency)]]`
      - `[[変更のリードタイム (Lead Time for Changes)]]`
      - `[[変更失敗率 (Change Failure Rate)]]`
      - `[[平均修復時間 (MTTR - Mean Time to Restore Service)]]` (DORAメトリクス)

## 6. [[VSMの利点と課題 MOC]]
   - **VSMの利点**
      - `[[プロセス全体の可視化と共通理解]]`
      - `[[ムダとボトルネックの体系的な特定]]`
      - `[[データに基づいた改善活動]]`
      - `[[顧客価値への集中]]`
      - `[[組織の壁を越えたコラボレーション促進]]`
   - **VSMの課題と導入の難しさ**
      - `[[経営層のコミットメントが必要]]`
      - `[[データの収集と測定が困難な場合がある]]`
      - `[[現状維持への抵抗]]`
      - `[[一度きりのイベントで終わってしまうリスク]]`
      - `[[非線形なプロセス (創造的作業など) への適用]]`

## 7. [[関連する手法との連携 MOC]]
   - `[[カンバン (Kanban) とVSM]]` (プルシステムとWIP制限)
   - `[[スクラム (Scrum) とVSM]]` (スプリントごとのプロセス改善)
   - `[[シックスシグマ (Six Sigma) とVSM]]` (ばらつきの削減)
   - `[[制約理論 (TOC - Theory of Constraints) とVSM]]` (ボトルネックの集中改善)
   - `[[デザイン思考 (Design Thinking) とVSM]]` (顧客価値の定義)

## 8. [[VSMのためのツールとリソース MOC]]
   - **デジタル作図ツール**
      - `[[Miro, Mural]]` (オンラインホワイトボード)
      - `[[Lucidchart, draw.io]]` (ダイアグラムツール)
      - `[[専用VSMソフトウェア]]`
   - **物理的なワークショップのためのツール**
      - `[[ホワイトボード、付箋、マーカー]]`
   - **主要な書籍** (『Learning to See』(邦題:『見える化』手法)など)
   - **オンラインリソースとコミュニティ**
