---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/machine-learning-concepts
---
## 1. [[機械学習入門 MOC]]
   - **機械学習とは何か**
      - [[機械学習の定義 (明示的なプログラミングなしに、データから学習する能力をコンピュータに与える研究分野)]] - Arthur Samuel / Tom M. Mitchell
      - [[機械学習の目的 (予測、分類、クラスタリング、異常検知など)]]
      - [[伝統的なプログラミングとの比較]] (ルールベース vs. データ駆動)
   - **なぜ機械学習が重要か**
      - [[複雑なパターンの発見と予測]]
      - [[大規模データの活用]]
      - [[タスクの自動化と効率化]]
      - [[パーソナライゼーションと推薦]]
   - **機械学習の歴史と進化**
      - `[[初期のAIと機械学習 (パーセプトロン、最近傍法など)]]`
      - `[[エキスパートシステムと冬の時代]]`
      - `[[統計的機械学習の台頭 (SVM、決定木)]]`
      - `[[深層学習 (Deep Learning) のブレークスルー]]`
   - **機械学習と関連分野**
      - `[[人工知能 (AI) との関係]]` (AI > ML > DL)
      - `[[データサイエンスとの関係]]`
      - `[[統計学との関係]]`
      - `[[データマイニングとの関係]]`

## 2. [[機械学習の種類 (学習方法による分類) MOC]]
   - **[[教師あり学習 (Supervised Learning) MOC]]**
      - `[[教師あり学習の定義 (ラベル付けされたデータ(正解)を用いてモデルを学習)]]`
      - **[[回帰 (Regression)]]**
         - [[回帰問題の定義 (連続値の予測)]]
         - `[[回帰の例 (株価予測、住宅価格予測、気温予測)]]`
      - **[[分類 (Classification)]]**
         - [[分類問題の定義 (離散的なカテゴリへの分類)]]
         - `[[二値分類 (Binary Classification)]]` (例: スパムメール判定、疾患の有無)
         - `[[多クラス分類 (Multiclass Classification)]]` (例: 手書き文字認識、画像のカテゴリ分類)
         - `[[(オプション) 多ラベル分類 (Multi-label Classification)]]`
   - **[[教師なし学習 (Unsupervised Learning) MOC]]**
      - `[[教師なし学習の定義 (ラベルのないデータから構造やパターンを発見)]]`
      - **[[クラスタリング (Clustering)]]**
         - [[クラスタリングの定義 (類似したデータ点のグループ化)]]
         - `[[クラスタリングの例 (顧客セグメンテーション、画像領域分割)]]`
      - **[[次元削減 (Dimensionality Reduction)]]**
         - [[次元削減の定義と目的 (特徴量の数を減らす、可視化)]]
         - `[[次元削減の例 (データ圧縮、特徴抽出)]]`
      - **[[異常検知 (Anomaly Detection)]]**
      - **[[関連ルール学習 (Association Rule Learning)]]** (例: アソシエーション分析)
   - **[[強化学習 (Reinforcement Learning - RL) MOC]]**
      - `[[強化学習の定義 (エージェントが環境との相互作用を通じて、報酬を最大化するように行動を学習)]]`
      - **[[強化学習の主要な概念]]**
         - `[[エージェント (Agent)]]`
         - `[[環境 (Environment)]]`
         - `[[状態 (State)]]`
         - `[[行動 (Action)]`
         - `[[報酬 (Reward)]]`
         - `[[方策 (Policy)]]`
         - `[[価値関数 (Value Function)]]`
      - `[[強化学習の例 (ゲームAI、ロボット制御、自動運転)]]`
   - **その他の学習パラダイム**
      - **[[半教師あり学習 (Semi-Supervised Learning)]]** (少量のラベル付きデータと大量のラベルなしデータを利用)
      - **[[自己教師あり学習 (Self-Supervised Learning)]]** (データ自身からラベルを生成して学習)
      - **[[転移学習 (Transfer Learning)]]** (あるタスクで学習したモデルを別のタスクに応用)
      - **[[(オプション) オンライン学習 (Online Learning) vs. バッチ学習 (Batch Learning)]]**

## 3. [[機械学習プロジェクトのワークフロー MOC]]
   - **1. 問題定義と目標設定**
      - `[[ビジネス課題の理解と機械学習問題への落とし込み]]`
      - `[[評価指標の決定]]`
      - `[[制約条件の確認 (計算リソース, 応答時間など)]]`
   - **2. データ収集 (Data Collection)**
      - `[[データソースの特定 (データベース, API, ログファイル, Webスクレイピング)]]`
      - `[[データの取得方法]]`
   - **3. データ理解と探索的データ分析 (EDA - Exploratory Data Analysis)**
      - `[[データの基本的な統計量の確認]]`
      - `[[データの可視化 (ヒストグラム, 散布図, 箱ひげ図)]]`
      - `[[相関分析]]`
      - `[[外れ値と欠損値の確認]]`
   - **4. データ前処理と特徴量エンジニアリング (Data Preprocessing and Feature Engineering)** (詳細は後述)
   - **5. モデルの選択と訓練 (Model Selection and Training)**
      - `[[適切なアルゴリズムの選択]]`
      - `[[訓練データ、検証データ、テストデータへの分割]]`
      - `[[モデルの訓練 (学習)]]`
   - **6. モデルの評価 (Model Evaluation)** (詳細は後述)
      - `[[テストデータを用いた性能評価]]`
      - `[[評価指標の計算と解釈]]`
   - **7. ハイパーパラメータチューニング (Hyperparameter Tuning)**
      - `[[グリッドサーチ (Grid Search)]]`
      - `[[ランダムサーチ (Random Search)]]`
      - `[[ベイズ最適化 (Bayesian Optimization)]]`
   - **8. モデルのデプロイと統合 (Model Deployment and Integration)**
      - `[[モデルのシリアライズ]]`
      - `[[APIとしての公開]]`
      - `[[バッチ推論とオンライン推論]]`
   - **9. モデルの運用と監視 (Model Operations and Monitoring)**
      - `[[パフォーマンスの継続的な監視]]`
      - `[[モデルの劣化 (Model Drift / Concept Drift) の検出]]`
      - `[[モデルの再学習と更新]]`
   - **[[MLOps (Machine Learning Operations) の概要]]** (開発と運用の連携)

## 4. [[機械学習のコアコンセプト MOC]]
   - **[[モデル (Model)]]**
      - [[モデルの定義 (データから学習したパターンや関係性の表現)]]
      - `[[パラメータ (Parameters)]]` (データから学習されるモデルの内部変数)
      - `[[ハイパーパラメータ (Hyperparameters)]]` (学習プロセスを制御するために人間が設定する変数)
   - **[[特徴量 (Features) とターゲット変数 (Target Variable)]]**
      - `[[特徴量 (説明変数、独立変数)]]` (入力データ)
      - `[[ターゲット変数 (目的変数、応答変数、ラベル)]]` (予測したい出力データ)
      - `[[特徴ベクトル (Feature Vector)]]`
   - **[[損失関数 (Loss Function / Cost Function / Objective Function)]]**
      - [[損失関数の定義 (モデルの予測と実際の値との誤差を測る関数)]]
      - `[[二乗誤差 (Mean Squared Error - MSE)]]` (回帰)
      - `[[平均絶対誤差 (Mean Absolute Error - MAE)]` (回帰)
      - `[[交差エントロピー誤差 (Cross-Entropy Loss)]]` (分類)
   - **[[最適化アルゴリズム (Optimization Algorithms) MOC]]**
      - **[[勾配降下法 (Gradient Descent)]]**
         - `[[勾配降下法の仕組み (損失関数の勾配を下る)]]`
         - `[[学習率 (Learning Rate)]]`
         - `[[バッチ勾配降下法 (Batch Gradient Descent)]]`
         - `[[確率的勾配降下法 (Stochastic Gradient Descent - SGD)]]`
         - `[[ミニバッチ勾配降下法 (Mini-batch Gradient Descent)]]`
      - `[[勾配降下法の発展形 (Momentum, AdaGrad, RMSprop, Adam)]]`
   - **[[仮説空間 (Hypothesis Space)]]** (モデルが表現しうる関数の集合)
   - **[[誘導バイアス (Inductive Bias)]]** (学習アルゴリズムが持つ仮定や制約)

## 5. [[モデルの評価と検証 (Model Evaluation and Validation) MOC]]

### 5.1. [[データセットの分割 MOC]]
   - `[[訓練データ (Training Set)]]`
   - `[[検証データ (Validation Set)]]` (ハイパーパラメータチューニング用)
   - `[[テストデータ (Test Set)]]` (モデルの最終的な性能評価用)
   - `[[データ分割の際の注意点 (シャッフル, 層化サンプリング)]]`
   - **[[交差検証 (Cross-Validation) MOC]]**
      - `[[k-分割交差検証 (k-Fold Cross-Validation)]]`
      - `[[層化k-分割交差検証 (Stratified k-Fold Cross-Validation)]]`
      - `[[(オプション) Leave-One-Out Cross-Validation (LOOCV)]]`

### 5.2. [[回帰モデルの評価指標 MOC]]
   - `[[平均絶対誤差 (MAE - Mean Absolute Error)]]`
   - `[[平均二乗誤差 (MSE - Mean Squared Error)]]`
   - `[[二乗平均平方根誤差 (RMSE - Root Mean Squared Error)]`
   - `[[決定係数 (R-squared / R²)]]`

### 5.3. [[分類モデルの評価指標 MOC]]
   - **[[混同行列 (Confusion Matrix)]]**
      - `[[真陽性 (TP - True Positive)]]`
      - `[[真陰性 (TN - True Negative)]]`
      - `[[偽陽性 (FP - False Positive) / 第一種の誤り]]`
      - `[[偽陰性 (FN - False Negative) / 第二種の誤り]]`
   - `[[正解率 (Accuracy)]]`
      - `[[不均衡データにおける正解率の問題点]]`
   - `[[適合率 (Precision)]]` (`TP / (TP + FP)`)
   - `[[再現率 (Recall) / 感度 (Sensitivity)]]` (`TP / (TP + FN)`)
   - `[[特異度 (Specificity)]]` (`TN / (TN + FP)`)
   - `[[F1スコア (F1-Score)]]` (適合率と再現率の調和平均)
   - **[[ROC曲線 (Receiver Operating Characteristic Curve)]]**
      - `[[ROC曲線の描画 (偽陽性率 vs. 真陽性率)]]`
   - **[[AUC (Area Under the ROC Curve)]]**
      - `[[AUCの解釈 (モデルの分類性能の指標)]]`
   - `[[(オプション) PR曲線 (Precision-Recall Curve)]]`
   - `[[(オプション) Log-loss (対数損失)]]`

## 6. [[過学習、未学習、バイアス-バリアンストレードオフ MOC]]
   - **[[過学習 (Overfitting)]]**
      - `[[過学習の定義 (訓練データに過剰に適合し、未知のデータに対する汎化性能が低い状態)]]`
      - `[[過学習の原因 (モデルが複雑すぎる, データが少なすぎる, ノイズが多い)]]`
      - `[[過学習の検出方法 (訓練誤差と検証誤差の乖離)]]`
   - **[[未学習 (Underfitting)]]**
      - `[[未学習の定義 (訓練データの特徴を十分に捉えきれていない状態)]]`
      - `[[未学習の原因 (モデルが単純すぎる, 特徴量が不足している)]]`
   - **[[バイアス-バリアンストレードオフ (Bias-Variance Tradeoff)]]**
      - `[[バイアス (Bias) とは (モデルの予測の体系的な誤り、単純なモデルほど高い)]]`
      - `[[バリアンス (Variance) とは (データセットの違いによるモデルの予測のばらつき、複雑なモデルほど高い)]]`
      - `[[モデルの複雑性とバイアス、バリアンスの関係]]`
      - `[[最適なモデル複雑度の追求]]`
   - **過学習への対策**
      - `[[訓練データを増やす (Data Augmentationなど)]]`
      - `[[モデルの複雑度を下げる]]`
      - **[[正則化 (Regularization)]]**
         - `[[L1正則化 (Lasso回帰)]]`
         - `[[L2正則化 (Ridge回帰)]]`
         - `[[Elastic Net]]`
      - `[[ドロップアウト (Dropout)]]` (ニューラルネットワーク)
      - `[[早期終了 (Early Stopping)]]`
      - `[[交差検証の活用]]`
      - `[[特徴量選択 (Feature Selection)]]`

## 7. [[データ前処理と特徴量エンジニアリング MOC]]

### 7.1. [[データクリーニング (Data Cleaning) MOC]]
   - **[[欠損値 (Missing Values) の処理]]**
      - `[[欠損値の削除 (行/列)]]`
      - `[[欠損値の補完 (Imputation)]]` (平均値, 中央値, 最頻値, 固定値, モデルによる予測)
   - **[[外れ値 (Outliers) の検出と処理]]**
      - `[[外れ値の検出方法 (統計的手法, 可視化)]]`
      - `[[外れ値の除去、変換、またはモデルの選択]]`
   - **[[ノイズデータ (Noisy Data) の処理]]**
      - `[[ビニング (Binning)]]`
      - `[[クラスタリング]]`

### 7.2. [[特徴量エンジニアリング (Feature Engineering) MOC]]
   - **[[特徴量スケーリング (Feature Scaling)]]**
      - `[[標準化 (Standardization / Z-score Normalization)]]`
      - `[[正規化 (Normalization / Min-Max Scaling)]]`
      - `[[スケーリングが必要なアルゴリズム]]`
   - **[[カテゴリ変数のエンコーディング (Encoding Categorical Variables)]]**
      - `[[ラベルエンコーディング (Label Encoding)]]`
      - `[[ワンホットエンコーディング (One-Hot Encoding)]]`
      - `[[(オプション) ターゲットエンコーディング, 特徴量ハッシング]]`
   - **[[テキストデータの前処理]]**
      - `[[トークン化 (Tokenization)]]`
      - `[[ストップワード除去 (Stop Word Removal)]]`
      - `[[ステミング (Stemming) とレンマ化 (Lemmatization)]`
      - `[[Bag-of-Words (BoW)]]`
      - `[[TF-IDF (Term Frequency-Inverse Document Frequency)]]`
      - `[[単語埋め込み (Word Embeddings - Word2Vec, GloVe, FastText)]]` (概要)
   - **[[特徴量生成 (Feature Creation)]]** (交互作用特徴量, 多項式特徴量など)
   - **[[特徴量選択 (Feature Selection)]]**
      - `[[フィルタ法 (Filter Methods)]]` (相関係数、カイ二乗検定)
      - `[[ラッパー法 (Wrapper Methods)]]` (再帰的特徴量削減 - RFE)
      - `[[埋め込み法 (Embedded Methods)]]` (L1正則化など)
   - **[[次元削減 (Dimensionality Reduction)]]** (再掲・手法として)
      - `[[主成分分析 (PCA - Principal Component Analysis)]]`
      - `[[(オプション) t-SNE (t-distributed Stochastic Neighbor Embedding)]]` (可視化向け)

## 8. [[主要な機械学習アルゴリズム概観 MOC]] (各アルゴリズム詳細MOCへのポータル)
   - **[[線形モデル (Linear Models) MOC]]** (線形回帰, ロジスティック回帰)
   - **[[決定木 (Decision Trees) MOC]]** (ID3, C4.5, CART)
   - **[[アンサンブル学習 (Ensemble Learning) MOC]]**
      - `[[バギング (Bagging) とランダムフォレスト (Random Forest)]]`
      - `[[ブースティング (Boosting) - AdaBoost, 勾配ブースティング (Gradient Boosting), XGBoost, LightGBM, CatBoost]]`
      - `[[スタッキング (Stacking)]]`
   - **[[サポートベクターマシン (SVM - Support Vector Machine) MOC]]** (マージン最大化, カーネルトリック)
   - **[[k-最近傍法 (k-Nearest Neighbors - k-NN) MOC]]** (インスタンスベース学習)
   - **[[ニューラルネットワークと深層学習 (Neural Networks and Deep Learning) MOC]]**
      - `[[パーセプトロン]]`
      - `[[多層パーセプトロン (MLP)]]`
      - `[[活性化関数 (Sigmoid, Tanh, ReLU)]]`
      - `[[順伝播と逆伝播 (Backpropagation)]]`
      - `[[畳み込みニューラルネットワーク (CNN - Convolutional Neural Network)]]` (画像認識)
      - `[[再帰型ニューラルネットワーク (RNN - Recurrent Neural Network)]]` (時系列データ)
         - `[[LSTM (Long Short-Term Memory), GRU (Gated Recurrent Unit)]]`
      - `[[Transformerモデル]]` (自然言語処理)
   - **[[クラスタリングアルゴリズム MOC]]**
      - `[[k-means法]]`
      - `[[階層的クラスタリング]]`
      - `[[DBSCAN]]`
   - **[[ベイズ学習 (Bayesian Learning) MOC]]** (ナイーブベイズ分類器)

## 9. [[機械学習における倫理と責任あるAI MOC]]
   - **[[AI倫理 (AI Ethics) の重要性]]**
   - **[[アルゴリズムのバイアス (Algorithmic Bias)]]**
      - `[[データバイアス (サンプリングバイアス、歴史的バイアスなど)]]`
      - `[[モデルバイアス]]`
      - `[[バイアスの検出と緩和手法]]`
   - **[[公平性 (Fairness)]]**
      - `[[公平性の定義 (個人、グループ)]]`
      - `[[公平性指標]]`
   - **[[説明可能性 (Explainability) と解釈可能性 (Interpretability) - XAI MOC]]**
      - `[[なぜモデルの説明可能性が必要か]]`
      - `[[モデルの解釈手法 (LIME, SHAPなど)]]`
      - `[[ホワイトボックスモデル vs. ブラックボックスモデル]]`
   - **[[透明性 (Transparency)]]**
   - **[[プライバシー (Privacy)]]**
      - `[[差分プライバシー (Differential Privacy)]]`
      - `[[連合学習 (Federated Learning)]]`
   - **[[アカウンタビリティ (Accountability) とガバナンス]]**
   - **[[堅牢性 (Robustness) と安全性 (Safety)]]** (敵対的攻撃 - Adversarial Attacks)
   - **[[責任あるAI開発のためのガイドライン]]**

## 10. [[機械学習ツールとエコシステム MOC]] (概要)
   - **プログラミング言語**
      - `[[Python (デファクトスタンダード)]]`
      - `[[R]]` (統計解析)
      - `[[Julia, Scala, Javaなど]]`
   - **主要なライブラリとフレームワーク**
      - `[[Scikit-learn]]` (総合機械学習ライブラリ)
      - `[[Pandas]]` (データ操作・分析)
      - `[[NumPy]]` (数値計算)
      - `[[Matplotlib / Seaborn]]` (データ可視化)
      - **深層学習フレームワーク**
         - `[[TensorFlow / Keras]]`
         - `[[PyTorch]]`
      - `[[XGBoost / LightGBM]]` (勾配ブースティング)
   - **実行環境**
      - `[[Jupyter Notebook / JupyterLab]]`
      - `[[Google Colaboratory]]`
   - **MLOpsプラットフォーム** (Kubeflow, MLflowなど - 概要)
   - **クラウドMLプラットフォーム** (AWS SageMaker, Google AI Platform/Vertex AI, Azure Machine Learning)
