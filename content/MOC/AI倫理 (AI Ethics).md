---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/ai-ethics
---
## 1. [[AI倫理入門 MOC]]
   - **AI倫理とは何か**
      - [[AI倫理の定義 (AIの開発・利用に関する道徳的原則と価値の研究)]]
      - [[なぜAI倫理が不可欠か (社会への影響、信頼の構築、リスク回避)]]
      - [[AI倫理の歴史的背景と議論の変遷]]
   - **AIが社会に与える影響**
      - [[AIのポジティブな影響 (医療、科学、生産性向上など)]]
      - [[AIのネガティブな影響とリスク (差別、失業、監視、自律兵器など)]]
   - **AI倫理の主要な原則 (概観)**
      - [[人間中心性 (Human-Centricity)]]
      - [[公平性 (Fairness)]]
      - [[透明性と説明可能性 (Transparency & Explainability)]]
      - [[堅牢性と安全性 (Robustness & Safety)]]
      - [[プライバシー (Privacy)]]
      - [[アカウンタビリティ (Accountability)]]
   - **ステークホルダーとその責任**
      - `[[開発者・研究者の倫理的責任]]`
      - `[[企業の倫理的責任 (CSR, ガバナンス)]]`
      - `[[政策立案者・政府の役割]]`
      - `[[利用者のリテラシーと責任]]`

## 2. [[公平性 (Fairness) in AI MOC]]

### 2.1. [[アルゴリズムのバイアス (Algorithmic Bias) MOC]]
   - **アルゴリズムバイアスの定義 (人間の偏見を反映・増幅する体系的な誤り)**
   - **バイアスの源泉**
      - **[[データバイアス (Data Bias)]]**
         - `[[サンプリングバイアス (Sampling Bias)]]`
         - `[[歴史的バイアス (Historical Bias)]]`
         - `[[選択バイアス (Selection Bias)]]`
         - `[[測定バイアス (Measurement Bias)]`
      - **[[モデルバイアス (Model Bias / Algorithmic Bias)]]**
         - `[[アルゴリズム選択によるバイアス]]`
         - `[[特徴量選択によるバイアス]]`
      - **[[人間のバイアス (Human Bias)]]**
         - `[[確証バイアス (Confirmation Bias)]]`
         - `[[暗黙のバイアス (Implicit Bias)]]`
         - `[[アノテーションバイアス (Annotation Bias)]]`
   - `[[バイアスがもたらす社会的な害 (採用、融資、司法判断における差別など)]]`
   - `[[バイアスの事例研究 (COMPAS, Amazon採用AIなど)]]`

### 2.2. [[公平性の定義と指標 (Definitions and Metrics of Fairness) MOC]]
   - [[公平性の定義の難しさ (トレードオフの存在)]]
   - **個人レベルの公平性 (Individual Fairness)**
      - `[[「類似した個人は類似した扱いを受けるべき」という原則]]`
   - **グループごとの公平性 (Group Fairness)**
      - `[[人口統計学的パリティ (Demographic Parity / Statistical Parity)]]`
      - `[[機会の均等 (Equal Opportunity)]]`
      - `[[均等オッズ (Equalized Odds)]]`
      - `[[(オプション) 条件付き公平性 (Conditional Fairness)]]`
   - `[[各公平性指標間のトレードオフ (例: 適合率パリティ vs. 再現率パリティ)]]`
   - `[[公平性のコンテキスト依存性]]`

### 2.3. [[バイアスの検出と緩和手法 MOC]]
   - **バイアスの検出**
      - `[[データセットの分析と可視化]]`
      - `[[公平性指標の計測]]`
      - `[[バイアス監査ツール (AI Fairness 360, Fairlearnなど)]]`
   - **バイアス緩和技術**
      - **[[前処理 (Pre-processing)]]**
         - `[[リサンプリング (Oversampling/Undersampling)]]`
         - `[[リウェイティング (Reweighting)]]`
      - **[[学習中処理 (In-processing)]]**
         - `[[正則化項による制約]]`
         - `[[敵対的学習 (Adversarial Debiasing)]]`
      - **[[後処理 (Post-processing)]]**
         - `[[分類しきい値の調整]]`
         - `[[キャリブレーション (Calibration)]]`

## 3. [[透明性と説明可能性 (Transparency and Explainability) MOC]]

### 3.1. [[透明性の原則 (Principle of Transparency) MOC]]
   - [[AIシステムにおける透明性の定義 (システムの仕組みや意思決定プロセスが理解可能であること)]]
   - **透明性のレベル**
      - `[[モデルの透明性 (ホワイトボックス vs. ブラックボックス)]]`
      - `[[データの透明性 (使用データ、前処理)]]`
      - `[[アルゴリズムの透明性]]`
   - [[透明性が求められる理由 (信頼、監査、デバッグ、責任追跡)]]
   - `[[モデルカード (Model Cards)]]`
   - `[[データセットのためのデータシート (Datasheets for Datasets)]]`

### 3.2. [[説明可能なAI (Explainable AI - XAI) MOC]]
   - **[[XAIの定義と目的 (AIモデルの予測や決定の理由を人間が理解できる形で提示する技術)]]**
   - **[[解釈可能性 (Interpretability) vs. 説明可能性 (Explainability)]]**
   - **XAIの技術分類**
      - **[[モデル固有の説明手法 (Model-Specific Methods)]]**
         - `[[線形モデルの係数]]`
         - `[[決定木の可視化]]`
         - `[[アテンションメカニズムの可視化 (Transformerなど)]]`
         - `[[CAM / Grad-CAM (CNN向け)]]`
      - **[[モデル非依存の説明手法 (Model-Agnostic Methods)]]**
         - **[[LIME (Local Interpretable Model-agnostic Explanations)]]** (局所的な線形近似)
         - **[[SHAP (SHapley Additive exPlanations)]]** (ゲーム理論に基づく貢献度)
         - `[[Partial Dependence Plots (PDP)]]`
         - `[[Individual Conditional Expectation (ICE) Plots]]`
      - `[[カウンターファクチュアル説明 (Counterfactual Explanations)]]` (「もし～だったら、結果は～だった」)
   - [[XAIの利点 (信頼向上、デバッグ、バイアス発見、規制遵守)]]
   - [[XAIの課題 (説明の忠実性と分かりやすさのトレードオフ)]]

## 4. [[アカウンタビリティとガバナンス (Accountability and Governance) MOC]]

### 4.1. [[AIのアカウンタビリティ (Accountability) MOC]]
   - [[アカウンタビリティの定義 (AIシステムの結果に対する説明責任)]]
   - `[[誰が責任を負うのか (開発者、運用者、所有者、利用者)]]`
   - `[[責任の連鎖とギャップ]]`
   - **アカウンタビリティを確保するためのメカニズム**
      - `[[監査証跡 (Audit Trails) とロギング]]`
      - `[[インパクトアセスメント (Impact Assessment)]]`
      - `[[独立した監査と認証制度]]`

### 4.2. [[AIガバナンス (AI Governance) MOC]]
   - [[AIガバナンスの定義 (AIの開発と利用を導くためのルール、実践、プロセスの体系)]]
   - **組織内AIガバナンス**
      - `[[AI倫理委員会の設置]]`
      - `[[AI開発ガイドラインと行動規範の策定]]`
      - `[[リスク管理フレームワークの構築]]`
      - `[[倫理トレーニングと教育]]`
      - `[[内部告発制度]]`
   - **[[AIインパクトアセスメント (AIA - AI Impact Assessment)]]**
      - [[AIAの目的とプロセス]]
   - **[[モデルカード (Model Cards) とデータセットのためのデータシート (Datasheets for Datasets) の実践]]**

### 4.3. [[AI倫理ガイドラインと法規制 MOC]]
   - **主要な国際的ガイドライン**
      - `[[OECD AI原則]]`
      - `[[G7 / G20 のAI原則]]`
      - `[[IEEE Ethically Aligned Design]]`
   - **各国の法規制動向**
      - **[[EU AI Act (AI法)]]**
         - `[[リスクベースアプローチ (許容できないリスク, ハイリスク, 限定的リスク, 最小リスク)]]`
         - `[[ハイリスクAIへの要求事項]]`
      - **[[アメリカのAI政策 (NIST AI RMFなど)]]**
      - **[[日本のAI戦略とガイドライン]]**
      - **[[中国のAI規制]]**
   - [[技術者として法規制を理解する重要性]]

## 5. [[プライバシー (Privacy) MOC]]
   - **[[AIとプライバシーの問題 MOC]]**
      - `[[大規模データ収集と個人の特定 (再識別化)]]`
      - `[[プロファイリングと行動予測]]`
      - `[[深層学習モデルからのデータ抽出攻撃]]`
      - `[[生成AIによるプライバシー侵害]]`
   - **[[プライバシー保護技術 (PETs - Privacy-Enhancing Technologies) MOC]]**
      - **[[匿名化 (Anonymization) と仮名化 (Pseudonymization)]]**
         - `[[k-匿名性 (k-Anonymity)]]`
         - `[[l-多様性 (l-Diversity), t-近接性 (t-Closeness)]]`
      - **[[差分プライバシー (Differential Privacy)]]**
         - `[[差分プライバシーの定義と保証]]`
         - `[[差分プライバシーの実装メカニズム (ラプラス機構、ガウス機構)]]`
      - **[[連合学習 (Federated Learning)]]**
         - `[[データを集約せずにモデルを学習する仕組み]]`
         - `[[連合学習とプライバシー]]`
      - **[[(オプション) 準同型暗号 (Homomorphic Encryption)]]** (暗号化したまま計算)
      - **[[(オプション) 安全なマルチパーティ計算 (Secure Multi-Party Computation - SMPC)]]**
   - **[[プライバシーバイデザイン (Privacy by Design) の原則]]**

## 6. [[堅牢性と安全性 (Robustness and Safety) MOC]]
   - **[[AIの安全性 (AI Safety) MOC]]**
      - `[[AI安全性の定義 (意図しない有害な振る舞いを引き起こさないこと)]]`
      - `[[仕様の不備 (Specification Gaming)]]`
      - `[[負の副作用 (Negative Side Effects)]]`
      - `[[報酬ハッキング (Reward Hacking)]]` (強化学習)
      - `[[スケーラブルな監督 (Scalable Oversight)]]`
      - `[[長期的なAI安全性と超知能のリスク]]` (アライメント問題 - 後述)
   - **[[AIの堅牢性 (AI Robustness) MOC]]**
      - **[[敵対的攻撃 (Adversarial Attacks)]]**
         - `[[敵対的攻撃の仕組み (微小な摂動による誤分類)]]`
         - `[[敵対的攻撃の種類 (FGSM, PGDなど)]]`
         - `[[ホワイトボックス攻撃とブラックボックス攻撃]]`
      - **[[敵対的堅牢性を高める手法]]**
         - `[[敵対的学習 (Adversarial Training)]]`
         - `[[防御的蒸留 (Defensive Distillation)]]`
         - `[[入力変換]]`
      - **[[分布外 (Out-of-Distribution - OOD) サンプルへの耐性]]**
      - **[[モデルの不確実性評価 (Uncertainty Quantification)]]**

## 7. [[人間中心のAIと価値との整合 MOC]]
   - **[[人間中心のAI設計 (Human-Centered AI Design) MOC]]**
      - [[ユーザーのニーズと価値観の理解]]
      - [[人間がAIをコントロールできること (Human-in-the-loop, Human-on-the-loop)]]
      - [[ユーザーへの適切なフィードバック]]
      - [[自動化バイアス (Automation Bias) の回避]]
      - [[UI/UXデザインとAI倫理]]
   - **[[価値整合 (Value Alignment) MOC]]** (アライメント問題)
      - `[[AIの目的関数を人間の価値観と整合させることの重要性と難しさ]]`
      - `[[逆強化学習 (Inverse Reinforcement Learning - IRL)]]`
      - `[[協調的逆強化学習 (Cooperative IRL)]]`
   - **[[人間とAIの協調 (Human-AI Collaboration) MOC]]**
      - `[[人間の能力を拡張するAI (Augmented Intelligence)]]`
      - `[[効果的な協調のためのインターフェース設計]]`
      - `[[責任の共有モデル]]`

## 8. [[AI倫理の応用分野とケーススタディ MOC]]
   - `[[顔認識技術におけるバイアスとプライバシー]]`
   - `[[採用・人事評価AIにおける公平性]]`
   - `[[金融分野 (融資審査、信用スコアリング) における公平性と説明可能性]]`
   - `[[医療AIにおける診断支援と責任問題]]`
   - `[[司法・法執行におけるAI (再犯予測、証拠分析) の課題]]`
   - `[[自動運転車における倫理的ジレンマ (トロッコ問題)]]`
   - `[[ソーシャルメディアの推薦アルゴリズムと社会への影響 (エコーチェンバー, フィルターバブル)]]`
   - `[[生成AI (Generative AI) の倫理的課題 (著作権, 偽情報, バイアス増幅, 悪用)]]`
   - `[[自律型致死兵器システム (LAWS) をめぐる議論]]`

## 9. [[AI倫理の将来と課題 MOC]]
   - **継続的な課題**
      - `[[技術の進歩と倫理・法規制のギャップ]]`
      - `[[グローバルな合意形成の難しさ]]`
      - `[[倫理原則の具体的な実装への落とし込み]]`
   - **将来の議論**
      - `[[汎用人工知能 (AGI) の倫理]]`
      - `[[AIの権利や意識の問題]]`
      - `[[持続可能性とAI (環境への影響)]]`
   - **AI倫理を学ぶためのリソース** (学会、カンファレンス、書籍、オンラインコース)
   - **技術者として倫理観を持ち続けるために**
