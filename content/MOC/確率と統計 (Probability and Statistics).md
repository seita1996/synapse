---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/probability-and-statistics
---
## 1. [[確率論と統計学の導入 MOC]]
   - **確率論とは何か、統計学とは何か**
      - [[確率論の定義 (不確実な現象の数学的記述)]]
      - [[統計学の定義 (データの収集、分析、解釈、提示)]]
      - [[確率論と統計学の関係 (確率論は統計学の基礎)]]
   - **コンピュータサイエンスにおける確率統計の重要性**
      - [[機械学習・AI (モデル構築、不確実性の表現、学習理論)]]
      - [[データマイニングとデータ分析 (パターンの発見、意思決定支援)]]
      - [[アルゴリズムの平均ケース分析とランダム化アルゴリズム]]
      - [[シミュレーションとモデリング]]
      - [[ネットワーク性能評価と信頼性工学]]
      - [[情報理論と符号化]]
      - [[A/Bテストと実験計画]]
   - **記述統計学と推測統計学の概要**

## 2. [[確率論 (Probability Theory) MOC]]

### 2.1. [[確率の基本概念 MOC]]
   - **試行 (Trial) と事象 (Event)**
      - [[試行の定義 (結果が偶然によって決まる実験や観測)]]
      - [[標本空間 (Sample Space - S, Ω) - 起こりうるすべての結果の集合]]
      - [[根元事象 (Elementary Event / Sample Point)]]
      - [[事象の定義 (標本空間の部分集合)]]
      - [[全事象 (Certain Event) と空事象 (Impossible Event)]]
   - **事象の演算**
      - [[和事象 (Union of Events - A ∪ B) - AまたはBが起こる]]
      - [[積事象 (Intersection of Events - A ∩ B) - AかつBが起こる]]
      - [[余事象 (Complementary Event - Aᶜ, Ā) - Aが起こらない]]
      - [[排反事象 (Mutually Exclusive Events / Disjoint Events) - 同時には起こらない事象]]
      - [[ド・モルガンの法則 (事象版)]]
      - [[ベン図による事象の表現]]
   - **確率の定義**
      - [[数学的確率 (ラプラスの定義 - 同様に確からしい場合)]] `P(A) = n(A) / n(S)`
      - [[統計的確率 (経験的確率 - 大数の法則の基礎)]]
      - **[[公理的確率 (コルモゴロフの公理)]]**
         - [[第一公理: P(A) ≥ 0]]
         - [[第二公理: P(S) = 1]]
         - [[第三公理: P(A₁ ∪ A₂ ∪ ...) = P(A₁) + P(A₂) + ... (互いに排反な場合 - 加法性)]]
   - **確率の基本性質 (公理からの導出)**
      - `[[P(∅) = 0]]`
      - `[[P(Aᶜ) = 1 - P(A)]]`
      - `[[A ⊆ B ⇒ P(A) ≤ P(B)]]`
      - `[[0 ≤ P(A) ≤ 1]]`
      - **[[加法定理 (Addition Rule)]]** `P(A ∪ B) = P(A) + P(B) - P(A ∩ B)`
      - [[3つ以上の事象の加法定理 (包除原理の応用)]]
   - **組合せ論と確率計算** (詳細は[[離散数学 MOC]] > [[組合せ論 MOC]]も参照)
      - [[順列を用いた確率計算]]
      - [[組合せを用いた確率計算]]
      - [[重複順列・重複組合せを用いた確率計算]]

### 2.2. [[条件付き確率と事象の独立性 MOC]]
   - **[[条件付き確率 (Conditional Probability)]]**
      - [[条件付き確率の定義 `P(B|A) = P(A ∩ B) / P(A)`]]
      - [[条件付き確率の直感的理解と応用例]]
   - **[[乗法定理 (Multiplication Rule)]]**
      - `[[P(A ∩ B) = P(A) * P(B|A) = P(B) * P(A|B)]]`
      - [[3つ以上の事象の乗法定理]]
   - **[[事象の独立性 (Independence of Events)]]**
      - [[2つの事象の独立性の定義 `P(A ∩ B) = P(A) * P(B)`]]
      - [[独立性と条件付き確率の関係 `P(B|A) = P(B)` (P(A)>0 の場合)]]
      - [[3つ以上の事象の独立性 (対独立と相互独立)]]
      - [[独立試行 (Independent Trials)]]
   - **[[全確率の法則 (Law of Total Probability)]]**
      - `[[P(B) = Σ P(B|Ai) * P(Ai)` (Aiが標本空間の分割の場合)]]
   - **[[ベイズの定理 (Bayes' Theorem) MOC]]**
      - **[[ベイズの定理の導出と公式]]** `P(Ai|B) = [P(B|Ai) * P(Ai)] / Σ P(B|Aj) * P(Aj)`
      - [[事前確率 (Prior Probability) と事後確率 (Posterior Probability)]]
      - [[尤度 (Likelihood)]]
      - [[ベイズの定理の応用例 (迷惑メールフィルタ、医療診断など)]]

### 2.3. [[確率変数 (Random Variables) MOC]]
   - **確率変数の定義**
      - [[確率変数とは (標本空間の各結果に数値を対応させる関数)]]
      - **[[離散確率変数 (Discrete Random Variable)]]** (値が可算個)
      - **[[連続確率変数 (Continuous Random Variable)]]** (値が連続的な区間)
   - **[[離散確率変数の確率分布 (Probability Distribution of Discrete Random Variables) MOC]]**
      - **[[確率質量関数 (PMF - Probability Mass Function) / 確率関数]]** `p(x) = P(X=x)`
         - [[PMFの性質 (p(x) ≥ 0, Σ p(x) = 1)]]
      - **[[累積分布関数 (CDF - Cumulative Distribution Function)]]** `F(x) = P(X ≤ x)` (離散版)
         - [[CDFの性質 (単調非減少、右連続など)]]
   - **[[連続確率変数の確率分布 (Probability Distribution of Continuous Random Variables) MOC]]**
      - **[[確率密度関数 (PDF - Probability Density Function)]]** `f(x)`
         - [[PDFの性質 (f(x) ≥ 0, ∫ f(x)dx = 1 over R)]]
         - `[[P(a ≤ X ≤ b) = ∫ f(x)dx from a to b]]`
         - `[[P(X=x) = 0` (連続変数の場合)]]
      - **[[累積分布関数 (CDF - Cumulative Distribution Function)]]** `F(x) = P(X ≤ x) = ∫ f(t)dt from -∞ to x` (連続版)
         - `[[f(x) = dF(x)/dx]]`
   - **[[期待値 (Expected Value / Mean) MOC]]**
      - [[離散確率変数の期待値 `E[X] = Σ x * p(x)`]]
      - [[連続確率変数の期待値 `E[X] = ∫ x * f(x)dx`]]
      - **[[期待値の性質]]**
         - `[[E[c] = c` (cは定数)]]
         - `[[E[cX] = cE[X]`]]
         - `[[E[X + Y] = E[X] + E[Y]` (線形性)]]
         - `[[E[g(X)]` (確率変数の関数の期待値)]]
      - [[期待値の解釈 (平均値、重心)]]
   - **[[分散 (Variance) と標準偏差 (Standard Deviation) MOC]]**
      - **[[分散の定義]]** `Var(X) = E[(X - E[X])^2] = E[X^2] - (E[X])^2`
         - [[離散確率変数の分散]]
         - [[連続確率変数の分散]]
      - **[[分散の性質]]**
         - `[[Var(c) = 0`]]
         - `[[Var(cX) = c^2 Var(X)`]]
         - `[[Var(X + c) = Var(X)`]]
         - `[[Var(X + Y) = Var(X) + Var(Y) + 2Cov(X,Y)`]] (独立なら `Var(X) + Var(Y)`)
      - **[[標準偏差の定義 `SD(X) = σ = sqrt(Var(X))`]]**
      - [[分散と標準偏差の解釈 (ばらつきの度合い)]]
      - [[(オプション) モーメント (Moment) と積率母関数 (Moment Generating Function - MGF)]]
      - [[(オプション) 特性関数 (Characteristic Function)]]
   - **[[チェビシェフの不等式 (Chebyshev's Inequality)]]** (平均と分散のみを用いた確率評価)
   - **[[確率変数の変換 (Transformation of Random Variables)]]** (1変数、2変数)

### 2.4. [[代表的な離散確率分布 MOC]]
   - **[[ベルヌーイ分布 (Bernoulli Distribution)]]** `Ber(p)`
      - [[PMF, 期待値, 分散]]
      - [[応用 (コイン投げなど単一試行)]]
   - **[[二項分布 (Binomial Distribution)]]** `B(n, p)`
      - [[PMF, 期待値, 分散]]
      - [[ベルヌーイ試行の繰り返し]]
      - [[二項分布の形状とパラメータ]]
   - **[[幾何分布 (Geometric Distribution)]]** `Geo(p)`
      - [[PMF (成功までの試行回数 or 失敗回数), 期待値, 分散]]
      - [[無記憶性 (Memoryless Property) - 離散版]]
   - **[[負の二項分布 (Negative Binomial Distribution) / パスカル分布]]**
      - [[PMF, 期待値, 分散]]
      - [[k回目の成功までの試行回数]]
   - **[[ポアソン分布 (Poisson Distribution)]]** `Po(λ)`
      - [[PMF, 期待値, 分散]]
      - [[稀な事象の発生回数 (例: 単位時間あたりの到着数)]]
      - [[二項分布のポアソン近似]]
   - **[[超幾何分布 (Hypergeometric Distribution)]]**
      - [[PMF, 期待値, 分散]]
      - [[非復元抽出]]
   - **[[離散一様分布 (Discrete Uniform Distribution)]]**

### 2.5. [[代表的な連続確率分布 MOC]]
   - **[[連続一様分布 (Continuous Uniform Distribution)]]** `U(a, b)`
      - [[PDF, CDF, 期待値, 分散]]
   - **[[正規分布 (Normal Distribution / Gaussian Distribution)]]** `N(μ, σ^2)`
      - [[PDF, 釣鐘型の形状]]
      - [[期待値 (μ) と分散 (σ^2)]]
      - **[[標準正規分布 (Standard Normal Distribution)]]** `N(0, 1)`
         - [[標準化 (Standardization) `Z = (X - μ) / σ`]]
         - [[標準正規分布表 (Z表) の使い方]]
      - [[正規分布の再生性 (和も正規分布)]]
      - [[正規分布の応用 (多くの自然現象、中心極限定理)]]
   - **[[指数分布 (Exponential Distribution)]]** `Exp(λ)`
      - [[PDF, CDF, 期待値, 分散]]
      - [[無記憶性 (Memoryless Property) - 連続版]]
      - [[ポアソン過程との関係 (事象の発生間隔)]]
   - **[[ガンマ分布 (Gamma Distribution)]]** (指数分布、カイ二乗分布を特殊ケースとして含む)
      - [[PDF, 期待値, 分散]]
   - **[[カイ二乗分布 (Chi-squared Distribution)]]** `χ^2(k)`
      - [[PDF, 期待値, 分散, 自由度k]]
      - [[正規分布に従う独立な確率変数の二乗和]]
      - [[統計的検定における利用]]
   - **[[t分布 (Student's t-Distribution)]]** `t(k)`
      - [[PDF, 期待値, 分散, 自由度k]]
      - [[正規分布の母平均の推定・検定 (母分散未知、小標本)]]
   - **[[F分布 (F-Distribution)]]** `F(k1, k2)`
      - [[PDF, 期待値, 分散, 自由度k1, k2]]
      - [[2つの正規分布の母分散の比の検定]] (分散分析)
   - **[[(オプション) ベータ分布 (Beta Distribution)]]**
   - **[[(オプション) ワイブル分布 (Weibull Distribution)]]** (信頼性工学)
   - **[[(オプション) 対数正規分布 (Log-normal Distribution)]]**

### 2.6. [[多次元確率変数と関連概念 MOC]]
   - **[[同時確率分布 (Joint Probability Distribution)]]**
      - [[離散の場合の同時確率質量関数 `p(x,y)`]]
      - [[連続の場合の同時確率密度関数 `f(x,y)`]]
   - **[[周辺確率分布 (Marginal Probability Distribution)]]**
      - [[同時分布からの導出]]
   - **[[条件付き確率分布 (Conditional Probability Distribution)]]**
      - `[[p(y|x) = p(x,y) / p_X(x)]]`
      - `[[f(y|x) = f(x,y) / f_X(x)]]`
   - **[[確率変数の独立性 (Independence of Random Variables)]]**
      - `[[p(x,y) = p_X(x) * p_Y(y)` または `f(x,y) = f_X(x) * f_Y(y)`]]
      - `[[E[XY] = E[X]E[Y]` (独立な場合)]]
   - **[[共分散 (Covariance)]]**
      - `[[Cov(X,Y) = E[(X-E[X])(Y-E[Y])] = E[XY] - E[X]E[Y]`]]
      - [[共分散の性質]]
      - [[独立ならば共分散は0 (逆は必ずしも真ならず)]]
   - **[[相関係数 (Correlation Coefficient)]]**
      - `[[ρ(X,Y) = Cov(X,Y) / (SD(X)SD(Y))`]]
      - [[相関係数の性質 (-1 ≤ ρ ≤ 1)]]
      - [[相関の強さと方向の解釈]]
      - [[無相関と独立の違い]]
   - **[[多変量正規分布 (Multivariate Normal Distribution)]]** (概要)
   - **[[(オプション) 確率変数の和の分布]]** (畳み込み)

### 2.7. [[極限定理 (Limit Theorems) MOC]]
   - **[[大数の法則 (Law of Large Numbers - LLN)]]**
      - [[弱法則 (Weak LLN) と強法則 (Strong LLN)]]
      - [[標本平均が母平均に収束することの意味]]
   - **[[中心極限定理 (Central Limit Theorem - CLT)]]**
      - [[独立同分布に従う確率変数の和 (または平均) の分布が正規分布に近似できる]]
      - [[CLTの重要性と応用範囲]]
   - **[[(オプション) ド・モアブル–ラプラスの定理 (De Moivre–Laplace Theorem)]]** (二項分布の正規近似)

## 3. [[記述統計学 (Descriptive Statistics) MOC]]

### 3.1. [[データの種類と収集 MOC]]
   - **データの種類**
      - **[[質的データ (Qualitative Data / Categorical Data)]]**
         - [[名義尺度 (Nominal Scale)]]
         - [[順序尺度 (Ordinal Scale)]]
      - **[[量的データ (Quantitative Data / Numerical Data)]]**
         - [[間隔尺度 (Interval Scale)]]
         - [[比例尺度 (Ratio Scale)]]
      - [[離散データと連続データ]] (統計学における)
   - **データ収集の方法 (概要)** (観察研究、実験、調査など)
   - **標本化 (Sampling) の基本** (ランダムサンプリングなど - 推測統計学で詳述)

### 3.2. [[データの整理と視覚化 MOC]]
   - **度数分布表 (Frequency Distribution Table)**
      - [[階級 (Class)、階級値 (Class Mark)、度数 (Frequency)、相対度数 (Relative Frequency)、累積度数 (Cumulative Frequency)]]
   - **グラフによるデータの視覚化**
      - **[[ヒストグラム (Histogram)]]** (量的データ)
      - **[[度数多角形 (Frequency Polygon) / 度数折れ線]]**
      - **[[棒グラフ (Bar Chart / Bar Graph)]]** (質的データ、離散的量的データ)
      - **[[円グラフ (Pie Chart)]]** (構成割合)
      - **[[幹葉図 (Stem-and-Leaf Plot)]]**
      - **[[ドットプロット (Dot Plot)]]**
      - **[[箱ひげ図 (Box Plot / Box-and-Whisker Plot)]]** (後述)
      - **[[散布図 (Scatter Plot)]]** (2変量データ、後述)
      - **[[(オプション) Q-Qプロット (Quantile-Quantile Plot)]]** (正規性の確認など)
      - **[[(オプション) 時系列プロット (Time Series Plot)]]**

### 3.3. [[代表値 (Measures of Central Tendency) MOC]]
   - **[[平均 (Mean)]]**
      - [[算術平均 (Arithmetic Mean) / 標本平均 (Sample Mean) `x̄` と母平均 (Population Mean) `μ`]]
      - [[加重平均 (Weighted Mean)]]
      - [[幾何平均 (Geometric Mean)]]
      - [[調和平均 (Harmonic Mean)]]
      - [[トリム平均 (Trimmed Mean)]] (外れ値対策)
   - **[[中央値 (Median)]]**
      - [[データ数が奇数/偶数の場合の中央値の求め方]]
      - [[外れ値に対する頑健性]]
   - **[[最頻値 (Mode)]]**
      - [[単峰性、多峰性]]
   - **平均、中央値、最頻値の関係と分布の形状 (対称、右に歪む、左に歪む)**

### 3.4. [[散布度 (Measures of Dispersion / Variability) MOC]]
   - **[[範囲 (Range)]]** (最大値 - 最小値)
   - **[[四分位数 (Quartiles) と四分位範囲 (IQR - Interquartile Range)]]**
      - [[Q1 (第1四分位数), Q2 (第2四分位数/中央値), Q3 (第3四分位数)]]
      - `[[IQR = Q3 - Q1`]]
      - [[外れ値の検出 (1.5 * IQRルール)]]
   - **[[分散 (Variance)]]**
      - **[[標本分散 (Sample Variance) `s^2`]]** (n-1で割る理由 - 不偏性)
      - **[[母分散 (Population Variance) `σ^2`]]** (Nで割る)
   - **[[標準偏差 (Standard Deviation)]]**
      - **[[標本標準偏差 (Sample Standard Deviation) `s`]]**
      - **[[母標準偏差 (Population Standard Deviation) `σ`]]**
   - **[[変動係数 (Coefficient of Variation - CV)]]** (平均に対する相対的なばらつき)
   - **[[(オプション) 平均絶対偏差 (Mean Absolute Deviation - MAD)]]**
   - **[[標準化得点 (Standard Score / Z-score)]]** `z = (x - μ) / σ` または `z = (x - x̄) / s`

### 3.5. [[データの要約と箱ひげ図 MOC]]
   - **[[5数要約 (Five-Number Summary)]]** (最小値, Q1, 中央値, Q3, 最大値)
   - **[[箱ひげ図の作成と解釈]]**
      - [[箱、ひげ、外れ値の表示]]
      - [[分布の形状、ばらつき、外れ値の視覚的把握]]

### 3.6. [[2変量データの記述統計 (相関と回帰の導入) MOC]]
   - **[[散布図 (Scatter Plot) と相関の視覚的把握]]**
   - **[[共分散 (Covariance) - 記述統計版]]**
   - **[[ピアソンの積率相関係数 (Pearson Correlation Coefficient - r)]]**
      - [[相関係数の計算と解釈 (-1から1の値、相関の強さと方向)]]
      - [[相関関係と因果関係の違い]]
   - **[[単回帰分析 (Simple Linear Regression) - 記述的側面]]**
      - [[回帰直線 (最小二乗法による決定)]]
      - [[回帰係数 (傾きと切片) の解釈]]
      - **[[決定係数 (R-squared / R^2)]]** (当てはまりの良さ)
   - **[[(オプション) スピアマンの順位相関係数 (Spearman's Rank Correlation Coefficient)]]**

## 4. [[推測統計学 (Inferential Statistics) MOC]]

### 4.1. [[標本抽出と標本分布 MOC]]
   - **[[母集団 (Population) と標本 (Sample)]]**
   - **[[なぜ標本抽出を行うのか (全数調査の困難性)]]**
   - **[[確率標本抽出法 (Probability Sampling Methods)]]**
      - [[単純無作為抽出 (Simple Random Sampling)]]
      - [[系統抽出 (Systematic Sampling)]]
      - [[層化抽出 (Stratified Sampling)]]
      - [[集落抽出 (Cluster Sampling)]]
   - **[[(オプション) 非確率標本抽出法]]**
   - **[[標本誤差 (Sampling Error) と非標本誤差 (Non-sampling Error)]]**
   - **[[統計量 (Statistic) と母数 (Parameter)]]**
   - **[[標本分布 (Sampling Distribution)]]**
      - [[標本平均の標本分布]] (中心極限定理との関連)
      - [[標本比率の標本分布]]
      - [[標本分散の標本分布 (カイ二乗分布)]]
   - **[[標準誤差 (Standard Error)]]**

### 4.2. [[点推定 (Point Estimation) MOC]]
   - **[[推定量 (Estimator) と推定値 (Estimate)]]**
   - **望ましい推定量の性質**
      - **[[不偏性 (Unbiasedness)]]** (`E[θ̂] = θ`)
         - [[不偏推定量 (Unbiased Estimator)]] (例: 標本平均、不偏分散)
      - **[[有効性 (Efficiency) / 最小分散]]**
         - [[有効推定量 (Efficient Estimator)]]
      - **[[一致性 (Consistency)]]** (標本サイズ大で母数に収束)
      - **[[(オプション) 漸近正規性 (Asymptotic Normality)]]**
      - **[[(オプション) 十分性 (Sufficiency)]]**
   - **点推定の方法 (概要)**
      - [[モーメント法 (Method of Moments)]]
      - **[[最尤法 (Maximum Likelihood Estimation - MLE)]]**
         - [[尤度関数 (Likelihood Function)]]
         - [[最尤推定量の求め方]]
         - [[最尤推定量の性質 (一致性、漸近正規性、漸近有効性)]]

### 4.3. [[区間推定 (Interval Estimation) MOC]]
   - **[[区間推定とは (母数をある確率で含む区間を推定)]]**
   - **[[信頼区間 (Confidence Interval - CI)]]**
      - **[[信頼係数 (Confidence Level / Confidence Coefficient)]]** (例: 95%信頼区間)
      - [[信頼区間の解釈 (誤解しやすい点)]]
   - **母平均の信頼区間**
      - **[[母分散が既知の場合 (正規分布)]]** (Z分布利用)
      - **[[母分散が未知の場合 (正規分布)]]** (t分布利用)
      - [[大標本の場合 (中心極限定理による正規近似)]]
   - **母比率の信頼区間**
      - [[正規近似を用いた信頼区間]]
      - [[(オプション) 正確な信頼区間 (Clopper-Pearson interval)]]
   - **母分散の信頼区間** (カイ二乗分布利用)
   - **[[(オプション) 2つの母平均の差の信頼区間]]**
   - **[[(オプション) 2つの母比率の差の信頼区間]]**
   - **[[(オプション) 信頼区間の幅と標本サイズの関係]]**

### 4.4. [[仮説検定 (Hypothesis Testing) MOC]]
   - **仮説検定の基本概念**
      - [[仮説検定とは (母集団に関する仮説の当否を標本から判断)]]
      - **[[帰無仮説 (Null Hypothesis - H₀)]]** (棄却を目指す仮説)
      - **[[対立仮説 (Alternative Hypothesis - H₁ or Ha)]]** (帰無仮説が棄却された場合に採択される仮説)
      - **[[検定統計量 (Test Statistic)]]**
      - **[[棄却域 (Rejection Region / Critical Region) と採択域 (Acceptance Region)]]**
      - **[[有意水準 (Significance Level - α)]]** (第一種の誤りの確率の上限)
      - **[[第一種の誤り (Type I Error)]]** (真である帰無仮説を棄却する誤り `P(Reject H₀ | H₀ is true) = α`)
      - **[[第二種の誤り (Type II Error)]]** (偽である帰無仮説を採択する誤り `P(Accept H₀ | H₀ is false) = β`)
      - **[[検出力 (Power of a Test)]]** (`1 - β = P(Reject H₀ | H₀ is false)`)
      - **[[p値 (p-value)]]**
         - [[p値の定義と解釈 (帰無仮説の下で観測されたデータ以上に極端なデータが得られる確率)]]
         - [[p値と有意水準を用いた意思決定]]
      - **両側検定 (Two-tailed Test) と片側検定 (One-tailed Test)**
   - **仮説検定の手順**
   - **母平均に関する検定**
      - **[[母分散が既知の場合 (Z検定)]]**
      - **[[母分散が未知の場合 (t検定)]]**
   - **母比率に関する検定** (正規近似によるZ検定)
   - **母分散に関する検定** (カイ二乗検定)
   - **2つの母集団に関する検定**
      - **[[2つの母平均の差の検定]]**
         - [[対応のあるデータ (Paired t-test)]]
         - [[対応のない独立なデータ (等分散仮定/非等分散仮定 - Welchのt検定)]]
      - **[[2つの母比率の差の検定]]**
      - **[[2つの母分散の比の検定 (F検定)]]**
   - **[[(オプション) 適合度検定 (Goodness-of-Fit Test) - カイ二乗検定]]**
   - **[[(オプション) 独立性の検定 (Test of Independence) - カイ二乗検定]]** (分割表)
   - **[[(オプション) 分散分析 (ANOVA - Analysis of Variance)]]**
      - [[一元配置分散分析 (One-way ANOVA)]]
      - [[F検定の利用]]
   - **[[(オプション) ノンパラメトリック検定 (Nonparametric Tests)]]** (ウィルコクソンの符号順位検定、マン・ホイットニーのU検定など - 概要)
   - **[[(オプション) 検定の多重性とp値の調整]]** (ボンフェローニ補正など)

## 5. [[(オプション/概要) ベイズ統計学入門 MOC]]
   - **ベイズ統計学の考え方**
      - [[ベイズの定理の再訪 (パラメータ推定への応用)]]
      - [[事前分布 (Prior Distribution)]]
      - [[尤度関数 (Likelihood Function)]] (再掲)
      - [[事後分布 (Posterior Distribution)]] `Posterior ∝ Likelihood × Prior`
      - [[ベイズ推定 (点推定: 事後期待値/事後モード, 区間推定: 信用区間)]]
   - **[[主観確率と客観確率]]**
   - **[[ベイズ統計学と頻度論統計学 (古典的統計学) の違い]]**
   - **ベイズ更新 (Bayesian Updating)**
   - **[[(概要) マルコフ連鎖モンテカルロ法 (MCMC - Markov Chain Monte Carlo)]]** (事後分布の計算が困難な場合)
   - **ベイズ統計学の応用** (迷惑メールフィルタ、機械学習モデルなど)

## 6. [[(オプション/概要) モンテカルロ法入門 MOC]]
   - **モンテカルロ法とは (乱数を用いたシミュレーションによる数値計算法)**
   - **モンテカルロ法の基本手順**
   - **応用例**
      - [[数値積分 (モンテカルロ積分)]]
      - [[円周率の推定]]
      - [[確率分布からのサンプリング]]
      - [[物理シミュレーション]]
      - [[金融工学]]
   - **[[(概要) 擬似乱数生成 (Pseudo-random Number Generation)]]**
   - **[[(概要) ブートストラップ法 (Bootstrap Method)]]** (リサンプリングによる統計的推測)

## 7. [[確率と統計のコンピュータサイエンス応用例 MOC]] (各分野へのリンク)
   - **機械学習** (分類、回帰、クラスタリング、ベイズ分類器、確率モデル、損失関数)
   - **データマイニング** (相関ルール、異常検知)
   - **自然言語処理** (n-gramモデル、隠れマルコフモデル)
   - **コンピュータビジョン** (確率的画像モデル)
   - **アルゴリズム設計と分析** (ランダム化アルゴリズム、平均ケース分析)
   - **ネットワーク工学** (キューイング理論、トラフィックモデリング)
   - **ソフトウェアテスト** (統計的テスト、信頼性モデル)
   - **暗号理論** (確率的素数判定)
   - **シミュレーションとモデリング** (性能評価、システム分析)
   - **A/Bテストとウェブ解析**