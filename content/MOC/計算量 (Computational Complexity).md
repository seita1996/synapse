---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/computational-complexity
---
## 1. [[計算量の基本概念 MOC]]
   - **定義と重要性**
      - [[計算量とは (アルゴリズムの効率性を測る指標)]]
      - [[なぜ計算量を学ぶのか (効率的なアルゴリズム設計の重要性)]]
      - [[アルゴリズムの計算量 vs 問題の計算量 (下限)]]
   - **計算モデル**
      - [[計算モデルとは (アルゴリズムの実行を抽象化する枠組み)]]
      - [[RAMモデル (Random Access Machine) の概要と仮定]]
      - [[(参考) チューリングマシン (Turing Machine) と計算量の関係]] (理論計算機科学の文脈で)
   - **入力サイズ (Input Size)**
      - [[入力サイズとは何か (計算量を表現する際の基準)]]
      - [[入力サイズの測り方 (ビット数、要素数など)]]
      - [[入力サイズと計算量の関係性]]
   - **基本操作 (Elementary Operation)**
      - [[基本操作とは (計算時間の単位となる操作)]]
      - [[アルゴリズムにおける基本操作の特定]]

## 2. [[時間計算量 (Time Complexity) MOC]]
   - **定義と計測**
      - [[時間計算量とは (アルゴリズムが終了するまでにかかる時間)]]
      - [[時間計算量の計測方法 (基本操作の実行回数カウント)]]
      - [[最悪ケース時間計算量 (Worst-case Time Complexity)]]
         - [[なぜ最悪ケースを重視するのか]]
      - [[平均ケース時間計算量 (Average-case Time Complexity)]]
         - [[平均ケース分析の難しさと仮定]]
         - [[入力データの分布の考慮]]
      - [[最良ケース時間計算量 (Best-case Time Complexity)]]
   - **具体例による時間計算量分析**
      - [[線形探索の時間計算量分析 (O(n))]]
      - [[二分探索の時間計算量分析 (O(log n))]]
      - [[基本的なソートアルゴリズムの時間計算量分析 (例: バブルソート O(n^2))]]
      - [[ループ構造のネストと時間計算量]]
   - **償却分析 (Amortized Analysis)**
      - [[償却分析とは (一連の操作における平均時間計算量)]]
      - [[償却分析が必要となるケース (例: 動的配列の拡張)]]
      - [[集計法 (Aggregate Method) による償却分析]]
      - [[会計法 (Accounting Method / Banker's Method) による償却分析]]
      - [[ポテンシャル法 (Potential Method) による償却分析]]
      - [[償却分析の具体例 (動的配列、Union-Findの経路圧縮)]]

## 3. [[空間計算量 (Space Complexity) MOC]]
   - **定義と計測**
      - [[空間計算量とは (アルゴリズムが実行中に使用するメモリ領域)]]
      - [[空間計算量の計測方法 (変数、データ構造、再帰スタックなど)]]
      - [[補助記憶域 (Auxiliary Space) と入力記憶域 (Input Space)]]
      - [[インプレースアルゴリズム (In-place Algorithm) とは (O(1)の補助記憶域)]]
   - **具体例による空間計算量分析**
      - [[基本的なアルゴリズムの空間計算量 (例: 線形探索、配列のソート)]]
      - [[再帰アルゴリズムの空間計算量 (再帰呼び出しスタック)]]
         - `[[マージソートの空間計算量]]`
         - `[[クイックソートの空間計算量]]`
   - **時間計算量と空間計算量のトレードオフ**
      - [[時間と空間のトレードオフとは (一方を改善すると他方が悪化する関係)]]
      - [[トレードオフの具体例 (ハッシュテーブル、動的計画法のテーブル)]]

## 4. [[オーダー記法 (Asymptotic Notation) MOC]]
   - **漸近的評価の必要性**
      - [[なぜ定数係数や低次項を無視するのか (入力サイズが大きい場合の本質的な挙動)]]
      - [[異なるマシンや言語での実行時間の普遍的な比較]]
   - **[[O記法 (Big O Notation) MOC]] (漸近的上限)**
      - [[O記法の数学的定義 (c * g(n) 以下)]]
      - [[O記法の直感的理解と使い方 (「高々これくらい」)]]
      - [[O記法の例 (O(1), O(log n), O(n), O(n log n), O(n^2), O(2^n), O(n!))]]
      - [[O記法の性質 (加法性、乗法性など)]]
      - [[よくあるO記法の誤解と正しい使い方]]
   - **[[Ω記法 (Omega Notation) MOC]] (漸近的下限)**
      - [[Ω記法の数学的定義 (c * g(n) 以上)]]
      - [[Ω記法の直感的理解と使い方 (「少なくともこれくらい」)]]
      - [[Ω記法の例とO記法との関係]]
   - **[[Θ記法 (Theta Notation) MOC]] (漸近的タイトな限界)**
      - [[Θ記法の数学的定義 (c1*g(n) 以上 c2*g(n) 以下)]]
      - [[Θ記法の直感的理解と使い方 (「ちょうどこれくらい」)]]
      - [[Θ記法の例とO記法、Ω記法との関係 (f(n) = Θ(g(n)) ⇔ f(n) = O(g(n)) かつ f(n) = Ω(g(n)))]]
   - **[[(オプション) o記法 (Little o Notation) MOC]] (漸近的真の上限)**
      - [[o記法の数学的定義 (c * g(n) より真に小さい)]]
      - [[o記法とO記法の違い (等号を含むか含まないか)]]
   - **[[(オプション) ω記法 (Little omega Notation) MOC]] (漸近的真の下限)**
      - [[ω記法の数学的定義 (c * g(n) より真に大きい)]]
      - [[ω記法とΩ記法の違い]]
   - **オーダー記法のまとめと使い分け**
      - [[各オーダー記法の比較表]]
      - [[アルゴリズム分析における適切な記法の選択]]
   - **一般的な関数の増加オーダー**
      - `[[log n vs n^c vs c^n vs n! の比較]]`
      - [[対数の底の変換とオーダー記法]]

## 5. [[計算量のクラス (Complexity Classes - アルゴリズム分析の観点から) MOC]]
   - *(理論計算機科学におけるP, NPなどのクラスとは異なり、アルゴリズムの性能を示す一般的な分類)*
   - **[[定数時間計算量 (Constant Time Complexity) - O(1)]]**
      - [[O(1)アルゴリズムの例 (配列の要素アクセス、ハッシュテーブルの平均的アクセス)]]
   - **[[対数時間計算量 (Logarithmic Time Complexity) - O(log n)]]**
      - [[O(log n)アルゴリズムの例 (二分探索、平衡二分探索木の操作)]]
      - [[対数時間の直感的理解 (問題サイズが倍になってもステップ数は少ししか増えない)]]
   - **[[線形時間計算量 (Linear Time Complexity) - O(n)]]**
      - [[O(n)アルゴリズムの例 (線形探索、配列の最大値検索)]]
   - **[[線形対数時間計算量 (Linearithmic Time Complexity) - O(n log n)]]**
      - [[O(n log n)アルゴリズムの例 (マージソート、クイックソートの平均、ヒープソート)]]
   - **[[多項式時間計算量 (Polynomial Time Complexity) - O(n^k)]]**
      - `[[O(n^2)アルゴリズムの例 (単純なソート、2重ループ)]]`
      - `[[O(n^3)アルゴリズムの例 (行列の乗算の単純な実装)]]`
      - [[多項式時間で解ける問題 (扱いやすい問題)]]
   - **[[指数時間計算量 (Exponential Time Complexity) - O(c^n), O(n!)]]**
      - `[[O(2^n)アルゴリズムの例 (全探索、巡回セールスマン問題の総当たり)]]`
      - `[[O(n!)アルゴリズムの例 (順列全探索)]]`
      - [[指数時間アルゴリズムの限界 (入力サイズが小さい場合のみ実用的)]]
   - **計算量クラス間の比較とグラフ**

## 6. [[再帰アルゴリズムの計算量分析 MOC]]
   - **再帰と漸化式**
      - [[再帰アルゴリズムとは]]
      - [[再帰アルゴリズムの計算量を表す漸化式の立式]]
         - `[[マージソートの漸化式: T(n) = 2T(n/2) + O(n)]]`
         - `[[二分探索の漸化式: T(n) = T(n/2) + O(1)]]`
         - `[[フィボナッチ数列の単純な再帰の漸化式: T(n) = T(n-1) + T(n-2) + O(1)]]`
   - **漸化式の解法**
      - **[[代入法 (Substitution Method) MOC]]**
         - [[代入法の考え方 (解を推測し数学的帰納法で証明)]]
         - [[代入法の具体例]]
      - **[[再帰木法 (Recursion Tree Method) MOC]]**
         - [[再帰木法の考え方 (再帰呼び出しを木構造で可視化しコストを合計)]]
         - [[再帰木法の具体例 (マージソートの再帰木)]]
      - **[[マスター定理 (Master Theorem) MOC]]**
         - [[マスター定理の形式 (T(n) = aT(n/b) + f(n))]]
         - [[マスター定理の3つのケースとその条件]]
         - [[マスター定理の適用例と限界]]
         - `[[(オプション) マスター定理の拡張版]]`

## 7. [[計算量の下限と最適性 MOC]]
   - **[[問題の下限 (Lower Bound of a Problem)]]**
      - [[問題の下限とは (その問題を解くために最低限必要な計算量)]]
      - [[決定木モデル (Decision Tree Model) と比較ソートの下限 (Ω(n log n))]]
      - [[情報理論的下限]]
   - **[[アルゴリズムの最適性 (Optimality of an Algorithm)]]**
      - [[最適アルゴリズムとは (そのアルゴリズムの時間計算量が問題の下限と一致する)]]
      - [[最適アルゴリズムの例 (比較ソートにおけるマージソートやヒープソート)]]
   - **[[ギャップ (Gap) - アルゴリズムの上限と問題の下限の間の差]]**

## 8. [[(参考) 理論計算機科学における計算複雑性クラス MOC]]
   - *(アルゴリズム分析の文脈からは少し発展的だが、関連として)*
   - [[Pクラス (Polynomial Time) とは (決定問題)]]
   - [[NPクラス (Nondeterministic Polynomial Time) とは]]
   - [[NP完全問題 (NP-complete Problems) とは]]
   - [[P vs NP問題の概要]]
   - [[これらのクラスとアルゴリズム設計の関係性 (NP困難問題へのアプローチ)]]

## 9. [[計算量の実践的な側面 MOC]]
   - **理論的計算量と実測時間**
      - [[定数係数や低次項の影響 (入力サイズが小さい場合)]]
      - [[キャッシュメモリ、パイプライン処理などハードウェアの影響]]
      - [[プログラミング言語やコンパイラの最適化の影響]]
      - [[理論的分析とプロファイリングによる実測の組み合わせの重要性]]
   - **データ構造の選択と計算量**
      - [[各データ構造の操作における計算量の違い]]
      - [[問題に適したデータ構造を選択することの重要性]]
   - **アルゴリズムの改善と計算量**
      - [[より効率的なアルゴリズムへの置き換え]]
      - [[ボトルネックの特定と最適化]]