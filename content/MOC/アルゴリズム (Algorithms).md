---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/algorithms
---
## 1. [[アルゴリズムの基本 MOC]]
   - **定義と性質**
      - [[アルゴリズムとは (定義、明確性、有限性、実効性、入力、出力)]]
      - [[良いアルゴリズムの特性 (正当性、効率性、可読性、保守性)]]
      - [[アルゴリズムとプログラムの関係]]
   - **記述方法**
      - [[アルゴリズムの記述方法 (自然言語、フローチャート、構造化記述)]]
      - [[擬似コード (Pseudocode) の書き方と規約]]
   - **正当性の検証**
      - [[アルゴリズムの正当性とは]]
      - [[ループ不変量 (Loop Invariant) を用いた正当性証明のアイデア]]
      - [[数学的帰納法による正当性証明のアイデア]]
   - **効率性の分析 (計算量)**
      - [[計算量とは (アルゴリズムの性能評価指標)]]
      - **時間計算量 (Time Complexity)**
         - [[時間計算量の定義と測定方法 (ステップ数カウント)]]
         - [[命令ごとのコストと実行回数]]
      - **空間計算量 (Space Complexity)**
         - [[空間計算量の定義と測定方法 (作業領域)]]
         - [[入力サイズと補助記憶域]]
      - **オーダー記法 (Asymptotic Notation)**
         - [[オーダー記法の必要性 (漸近的挙動の評価)]]
         - [[O記法 (Big O notation) - 上限]]
         - [[Ω記法 (Omega notation) - 下限]]
         - [[Θ記法 (Theta notation) - タイトな限界]]
         - [[(オプション) o記法 (Little o notation) - 真の上限]]
         - [[(オプション) ω記法 (Little omega notation) - 真の下限]]
         - [[オーダー記法の数学的定義と性質]]
      - **計算量のクラス**
         - [[定数時間計算量 O(1)]]
         - [[対数時間計算量 O(log n)]]
         - [[線形時間計算量 O(n)]]
         - [[線形対数時間計算量 O(n log n)]]
         - [[多項式時間計算量 O(n^k)]] (例: O(n^2), O(n^3))
         - [[指数時間計算量 O(2^n), O(k^n)]]
         - [[階乗時間計算量 O(n!)]]
      - **分析のケース**
         - [[最良ケース分析 (Best-case analysis)]]
         - [[平均ケース分析 (Average-case analysis)]]
         - [[最悪ケース分析 (Worst-case analysis)]] (最も重要視されることが多い)
      - **償却分析 (Amortized Analysis)**
         - [[償却分析とは (一連の操作における平均コスト)]]
         - [[集計法 (Aggregate method)]]
         - [[会計法 (Accounting method / Banker's method)]]
         - [[ポテンシャル法 (Potential method)]]
         - [[償却分析の例 (動的配列、Union-Find)]]
      - **再帰アルゴリズムの分析**
         - [[漸化式 (Recurrence relation) の立式]]
         - [[代入法 (Substitution method)による漸化式の解法]]
         - [[再帰木法 (Recursion tree method)による漸化式の解法]]
         - [[マスター定理 (Master theorem)による漸化式の解法]]
   - **問題の種類**
      - [[探索問題 (Searching problems)]]
      - [[ソート問題 (Sorting problems)]]
      - [[最適化問題 (Optimization problems)]]
      - [[決定問題 (Decision problems)]]

## 2. [[アルゴリズム設計戦略 (Algorithm Design Paradigms) MOC]]
   - [[アルゴリズム設計戦略とは (問題解決のための一般的なアプローチ)]]
   - **[[総当たり法 (Brute-force Search / Exhaustive Search) MOC]]**
      - [[総当たり法の考え方と特徴]]
      - [[総当たり法の適用例 (単純な文字列探索、巡回セールスマン問題の単純解法)]]
      - [[総当たり法の限界 (計算量の爆発)]]
   - **[[分割統治法 (Divide and Conquer) MOC]]**
      - [[分割統治法の考え方 (分割・統治・結合)]]
      - [[分割統治法の設計手順]]
      - [[分割統治法の適用例]]
         - `[[マージソート]]` (詳細はソートアルゴリズムにて)
         - `[[クイックソート]]` (詳細はソートアルゴリズムにて)
         - `[[二分探索]]` (詳細は探索アルゴリズムにて)
         - [[最近傍点対問題の分割統治解法]]
         - [[大整数の乗算 (Karatsubaアルゴリズム)]]
         - [[行列の乗算 (Strassenアルゴリズム)]]
      - [[分割統治法の計算量分析 (マスター定理の適用)]]
   - **[[動的計画法 (Dynamic Programming - DP) MOC]]**
      - [[動的計画法とは (部分問題の重複と最適部分構造)]]
      - [[動的計画法の適用条件 (重複部分問題、最適部分構造)]]
      - [[動的計画法の設計アプローチ]]
         - [[メモ化再帰 (Memoization / Top-down DP)]]
         - [[テーブル法 (Tabulation / Bottom-up DP)]]
      - [[動的計画法の設計手順]]
         - [[状態の定義]]
         - [[漸化式の構築]]
         - [[初期条件の設定]]
         - [[計算順序の決定 (テーブル法の場合)]]
      - [[動的計画法の適用例]]
         - [[フィボナッチ数列の計算]]
         - [[最長共通部分列 (LCS) 問題]]
         - [[編集距離 (レーベンシュタイン距離) 問題]]
         - [[ナップサック問題 (0-1 ナップサック問題、個数制限なしナップサック問題)]]
         - [[行列連鎖乗算問題]]
         - [[最長増加部分列 (LIS) 問題]]
         - [[コイン問題 (最小枚数での支払い)]]
         - [[経路最適化問題 (例: グリッド上の最短経路)]]
      - [[動的計画法と分割統治法の違い]]
      - [[動的計画法と貪欲法の違い]]
   - **[[貪欲法 (Greedy Algorithms) MOC]]**
      - [[貪欲法とは (局所最適解の積み重ね)]]
      - [[貪欲法の適用条件 (貪欲選択性、最適部分構造)]]
      - [[貪欲法の正当性の証明の難しさ (交換論法など)]]
      - [[貪欲法の適用例]]
         - [[活動選択問題 (Interval Scheduling)]]
         - [[フラクショナルナップサック問題]]
         - [[ハフマン符号化 (Huffman Coding)]]
         - `[[クラスカル法]]` (最小全域木)
         - `[[プリム法]]` (最小全域木)
         - `[[ダイクストラ法]]` (単一始点最短経路)
         - [[コイン問題 (特定の条件下での最適解)]]
      - [[貪欲法が最適解を与えない例]]
   - **[[バックトラッキング法 (Backtracking) MOC]]**
      - [[バックトラッキング法とは (深さ優先探索に基づく解空間探索)]]
      - [[バックトラッキング法の設計手順 (状態空間木、枝刈り)]]
      - [[バックトラッキング法の適用例]]
         - [[Nクイーン問題]]
         - [[迷路探索問題]]
         - [[部分和問題 (Subset Sum Problem)]]
         - [[グラフのハミルトン閉路問題]]
         - [[数独ソルバー]]
         - [[順列生成、組み合わせ生成]]
   - **[[分岐限定法 (Branch and Bound) MOC]]**
      - [[分岐限定法とは (最適化問題のための状態空間探索)]]
      - [[分岐限定法の構成要素 (分岐操作、限定操作、探索戦略)]]
      - [[分岐限定法の適用例]]
         - [[巡回セールスマン問題 (TSP)]]
         - [[ナップサック問題]]
         - [[整数計画問題]]
      - [[バックトラッキング法との比較]]
   - **[[ランダム化アルゴリズム (Randomized Algorithms) MOC]]**
      - [[ランダム化アルゴリズムとは (アルゴリズム内で乱数を利用)]]
      - [[ラスベガス法 (Las Vegas Algorithm)]] (常に正しい解、実行時間は確率的)
      - [[モンテカルロ法 (Monte Carlo Algorithm)]] (確率的に正しい解、実行時間は確定的)
      - [[ランダム化アルゴリズムの適用例]]
         - `[[ランダム化クイックソート]]`
         - `[[ミラー・ラビン素数判定法]]`
         - [[モンテカルロ法による円周率の推定]]
         - [[Skip List]]
      - [[乱数生成の重要性]]
   - **[[近似アルゴリズム (Approximation Algorithms) MOC]]**
      - [[近似アルゴリズムとは (NP困難問題などに対する多項式時間での近似解法)]]
      - [[近似比 (Approximation Ratio / Performance Ratio)]]
      - [[近似アルゴリズムの適用例]]
         - [[巡回セールスマン問題の近似解法 (例: 最近追加法、MSTヒューリスティック)]]
         - [[頂点被覆問題の近似解法]]
         - [[集合被覆問題の近似解法 (貪欲法)]]
      - [[PTAS (Polynomial Time Approximation Scheme)]]
      - [[FPTAS (Fully Polynomial Time Approximation Scheme)]]
   - **[[ヒューリスティックアルゴリズム (Heuristic Algorithms) MOC]]**
      - [[ヒューリスティックアルゴリズムとは (経験則や発見的手法に基づく解法)]]
      - [[ヒューリスティックアルゴリズムの特徴 (最適性の保証なし、発見的探索)]]
      - [[メタヒューリスティクス (Metaheuristics)]]
         - [[局所探索法 (Local Search)]]
         - [[山登り法 (Hill Climbing)]]
         - [[焼きなまし法 (Simulated Annealing)]]
         - [[遺伝的アルゴリズム (Genetic Algorithm)]]
         - [[タブーサーチ (Tabu Search)]]
      - [[ヒューリスティックの適用例 (多くの複雑な最適化問題)]]

## 3. [[ソートアルゴリズム (Sorting Algorithms) MOC]]
   - [[ソートアルゴリズムとは (定義、目的、キー)]]
   - **分類**
      - [[内部ソート (Internal Sort) と外部ソート (External Sort)]]
      - [[安定ソート (Stable Sort) と不安定ソート (Unstable Sort)]]
      - [[比較ソート (Comparison Sort) と非比較ソート (Non-comparison Sort)]]
   - **基本的な比較ソートアルゴリズム (O(n^2))**
      - **[[バブルソート (Bubble Sort) MOC]]**
         - [[バブルソートのアルゴリズムと図解]]
         - [[バブルソートの計算量分析 (O(n^2)) と安定性]]
         - [[バブルソートの改良版 (早期終了、シェーカーソート)]]
      - **[[選択ソート (Selection Sort) MOC]]**
         - [[選択ソートのアルゴリズムと図解]]
         - [[選択ソートの計算量分析 (O(n^2)) と安定性 (実装による)]]
      - **[[挿入ソート (Insertion Sort) MOC]]**
         - [[挿入ソートのアルゴリズムと図解]]
         - [[挿入ソートの計算量分析 (O(n^2), ほぼソート済みならO(n)) と安定性]]
         - [[二分挿入ソート (Binary Insertion Sort)]]
   - **効率的な比較ソートアルゴリズム (O(n log n))**
      - **[[マージソート (Merge Sort) MOC]]**
         - [[マージソートのアルゴリズム (分割統治法)]]
         - [[マージソートのマージ処理 (Merge Procedure)]]
         - [[マージソートの計算量分析 (常にO(n log n)) と安定性]]
         - [[トップダウンマージソート (再帰)]]
         - [[ボトムアップマージソート (非再帰)]]
         - [[マージソートの空間計算量 (O(n) または O(log n) - 実装による)]]
      - **[[クイックソート (Quick Sort) MOC]]**
         - [[クイックソートのアルゴリズム (分割統治法)]]
         - [[クイックソートのパーティション処理 (Partitioning)]]
            - [[Lomutoパーティションスキーマ]]
            - [[Hoareパーティションスキーマ]]
         - [[クイックソートのピボット選択戦略 (先頭、末尾、中央値、ランダム)]]
         - [[クイックソートの計算量分析 (平均O(n log n), 最悪O(n^2))]]
         - [[クイックソートの最悪ケースを避ける方法 (ランダム化、イントロソート)]]
         - [[クイックソートの安定性 (一般に不安定)]]
         - [[クイックソートの空間計算量 (平均O(log n), 最悪O(n))]]
         - [[三分割クイックソート (3-way Quick Sort)]] (重複キーが多い場合に有効)
      - **[[ヒープソート (Heap Sort) MOC]]**
         - [[ヒープソートのアルゴリズム (ヒープデータ構造を利用)]]
         - [[ヒープソートのBuild-Heap処理とHeapify処理]]
         - [[ヒープソートの計算量分析 (常にO(n log n)) と安定性 (不安定)]]
         - [[ヒープソートのインプレース性 (In-place sort)]]
      - **[[(オプション) シェルソート (Shell Sort) MOC]]**
         - [[シェルソートのアルゴリズムと増分系列 (Gap sequence)]]
         - [[シェルソートの計算量分析 (複雑、増分系列による)]]
      - **[[(オプション) イントロソート (Introsort) MOC]]** (クイックソート、ヒープソート、挿入ソートのハイブリッド)
      - **[[(オプション) Timsort MOC]]** (マージソートと挿入ソートのハイブリッド、PythonやJavaで採用)
   - **非比較ソートアルゴリズム (線形時間ソート)**
      - [[比較ソートの下限 (Ω(n log n))]]
      - **[[カウントソート (Counting Sort) MOC]]**
         - [[カウントソートのアルゴリズム (キーが特定の範囲の整数)]]
         - [[カウントソートの計算量分析 (O(n+k)) と安定性]]
      - **[[基数ソート (Radix Sort) MOC]]**
         - [[基数ソートのアルゴリズム (LSD: Least Significant Digit first / MSD: Most Significant Digit first)]]
         - [[基数ソートの計算量分析 (O(d(n+k))) と安定性]]
         - [[基数ソートとカウントソートの関係]]
      - **[[バケットソート (Bucket Sort) / ビンソート (Bin Sort) MOC]]**
         - [[バケットソートのアルゴリズム (入力が一様分布している場合に有効)]]
         - [[バケットソートの計算量分析 (平均O(n+k))]]
         - [[バケットソートの安定性 (実装による)]]
   - **[[外部ソート (External Sorting) MOC]]** (データがメモリに収まらない場合)
      - [[外部ソートの必要性と課題]]
      - [[外部マージソートの考え方 (分割、内部ソート、マージ)]]
      - [[ポリフェーズマージソート]]
      - [[置換選択ソート (Replacement Selection)]]
   - **ソートアルゴリズムの選択基準と使い分け**
   - **各種ソートアルゴリズムの比較表 (計算量、安定性、空間など)**

## 4. [[探索アルゴリズム (Searching Algorithms) MOC]]
   - [[探索アルゴリズムとは (特定の要素を見つけるプロセス)]]
   - **基本的な探索アルゴリズム**
      - **[[線形探索 (Linear Search / Sequential Search) MOC]]**
         - [[線形探索のアルゴリズムと計算量 (O(n))]]
         - [[線形探索の適用範囲 (未ソート配列、連結リスト)]]
         - [[番兵を用いた線形探索の最適化]]
      - **[[二分探索 (Binary Search) MOC]]**
         - [[二分探索のアルゴリズム (ソート済み配列が前提)]]
         - [[二分探索の計算量 (O(log n))]]
         - [[二分探索の実装 (再帰版、反復版)]]
         - [[二分探索の境界条件とオフバイワンエラーの注意点]]
         - [[二分探索の応用 (特定の値の探索、条件を満たす最初の/最後の要素の探索、平方根の計算など)]]
      - **[[三分探索 (Ternary Search) MOC]]**
         - [[三分探索のアルゴリズム (単峰性関数が前提)]]
         - [[三分探索の計算量 (O(log3 n))]]
   - **[[(オプション) 補間探索 (Interpolation Search) MOC]]**
      - [[補間探索のアルゴリズム (データが一様分布している場合に有効)]]
      - [[補間探索の計算量 (平均O(log log n))]]
   - **[[(オプション) 指数探索 (Exponential Search) MOC]]**
      - [[指数探索のアルゴリズム (無限長の可能性のあるソート済み配列)]]
   - **ハッシュテーブルを用いた探索** (詳細は[[ハッシュテーブル MOC]]にて)
   - **木構造を用いた探索** (詳細は[[二分探索木 MOC]]などにて)
   - **グラフ探索** (詳細は[[グラフアルゴリズム MOC]]にて)

## 5. [[グラフアルゴリズム (Graph Algorithms) MOC]]
   - *(このセクションは[[データ構造 MOC]]の[[グラフ MOC]]内のアルゴリズム項目と重複・関連しますが、アルゴリズムの視点から詳細化・拡充します)*
   - [[グラフアルゴリズムの重要性と多様な応用]]
   - **グラフ探索 (Graph Traversal)**
      - **[[幅優先探索 (BFS) MOC]]**
         - [[BFSのアルゴリズム手順 (キューを使用)]]
         - [[BFSの性質 (最短経路 - 重みなしグラフ、連結成分判定)]]
         - [[BFSの実装例と計算量 (O(V+E))]]
         - [[BFSツリー]]
      - **[[深さ優先探索 (DFS) MOC]]**
         - [[DFSのアルゴリズム手順 (スタックまたは再帰を使用)]]
         - [[DFSの性質 (閉路検出、トポロジカルソート、強連結成分)]]
         - [[DFSの実装例と計算量 (O(V+E))]]
         - [[DFSツリーと辺の分類 (木辺、後退辺、前方辺、横断辺)]]
         - [[関節点と橋の発見 (DFSベース)]]
   - **最短経路問題 (Shortest Path Problems)**
      - **単一始点最短経路 (Single-Source Shortest Path - SSSP)**
         - **[[ダイクストラ法 (Dijkstra's Algorithm) MOC]]**
            - [[ダイクストラ法のアルゴリズム (非負の辺重み)]]
            - [[ダイクストラ法の優先度付きキューを用いた効率化 (O((V+E)logV) or O(E+VlogV))]]
            - [[ダイクストラ法の正当性の証明 (貪欲法)]]
         - **[[ベルマン・フォード法 (Bellman-Ford Algorithm) MOC]]**
            - [[ベルマン・フォード法のアルゴリズム (負の辺重み対応)]]
            - [[ベルマン・フォード法による負閉路の検出]]
            - [[ベルマン・フォード法の計算量 (O(VE))]]
         - **[[SPFA (Shortest Path Faster Algorithm) MOC]]** (ベルマン・フォード法のキューによる最適化、特定のケースで高速)
         - **[[有向非巡回グラフ (DAG) における単一始点最短経路アルゴリズム]]** (動的計画法/トポロジカルソート利用、O(V+E))
      - **全点対最短経路 (All-Pairs Shortest Path - APSP)**
         - **[[フロイド・ワーシャル法 (Floyd-Warshall Algorithm) MOC]]**
            - [[フロイド・ワーシャル法のアルゴリズム (動的計画法)]]
            - [[フロイド・ワーシャル法の計算量 (O(V^3)) と負閉路検出]]
         - **[[ジョンソン法 (Johnson's Algorithm) MOC]]** (疎なグラフ向け、ダイクストラ法とベルマン・フォード法の組み合わせ)
   - **最小全域木 (Minimum Spanning Tree - MST)**
      - [[最小全域木とは (定義、特性、カット特性、サイクル特性)]]
      - **[[プリム法 (Prim's Algorithm) MOC]]**
         - [[プリム法のアルゴリズム (貪欲法)]]
         - [[プリム法の優先度付きキューを用いた実装 (O((V+E)logV) or O(E+VlogV))]]
      - **[[クラスカル法 (Kruskal's Algorithm) MOC]]**
         - [[クラスカル法のアルゴリズム (貪欲法、Union-Findデータ構造を利用)]]
         - [[クラスカル法の計算量 (O(E log E) or O(E log V))]]
      - **[[(オプション) Reverse-Delete Algorithm]]**
   - **ネットワークフロー (Network Flow)**
      - [[フローネットワークの定義 (ソース、シンク、容量、フロー)]]
      - **[[最大フロー問題 (Maximum Flow Problem) MOC]]**
         - [[残余グラフ (Residual Graph) と増加道 (Augmenting Path)]]
         - **[[フォード・ファルカーソン法 (Ford-Fulkerson Algorithm) MOC]]** (増加道を繰り返し見つける汎用的な方法)
         - **[[エドモンズ・カープアルゴリズム (Edmonds-Karp Algorithm) MOC]]** (BFSで増加道を探す、O(VE^2))
         - **[[(オプション) Dinicのアルゴリズム (Dinic's Algorithm) MOC]]** (ブロッキングフロー、より高速)
      - **[[最小カット問題 (Minimum Cut Problem) MOC]]**
         - [[カットの定義と容量]]
         - [[最大フロー最小カット定理]]
      - **[[(オプション) 最小費用流問題 (Minimum Cost Flow Problem) MOC]]**
      - **[[(オプション) 二部グラフの最大マッチングと最大フローの関係]]**
   - **連結性 (Connectivity)**
      - [[無向グラフの連結成分の検出 (BFS/DFS/Union-Find)]]
      - **[[強連結成分 (Strongly Connected Components - SCC) MOC]]** (有向グラフ)
         - [[強連結成分の定義]]
         - [[コサラジュのアルゴリズム (Kosaraju's Algorithm)]] (2回のDFS)
         - [[タージャンのアルゴリズム (Tarjan's Algorithm)]] (1回のDFSとスタック)
      - **[[関節点 (Articulation Points / Cut Vertices) と橋 (Bridges / Cut Edges) の検出アルゴリズム]]** (DFSベース)
   - **トポロジカルソート (Topological Sort)**
      - [[トポロジカルソートの定義 (有向非巡回グラフ - DAG)]]
      - [[トポロジカルソートのアルゴリズム]]
         - [[DFSベースのトポロジカルソート]]
         - [[カーンのアルゴリズム (Kahn's Algorithm)]] (入次数ベース、キューを使用)
      - [[トポロジカルソートの一意性と複数解]]
   - **サイクル検出 (Cycle Detection)**
      - [[無向グラフにおけるサイクル検出 (DFS/Union-Find)]]
      - [[有向グラフにおけるサイクル検出 (DFS - 後退辺の検出)]]
   - **(オプション) その他のグラフ問題**
      - [[グラフ彩色問題 (Graph Coloring Problem)]] (NP困難)
      - [[ハミルトン路/ハミルトン閉路問題 (Hamiltonian Path/Cycle Problem)]] (NP困難)
      - [[巡回セールスマン問題 (Traveling Salesperson Problem - TSP)]] (NP困難、近似アルゴリズムで扱うことも)
      - [[グラフ同型問題 (Graph Isomorphism Problem)]]

## 6. [[文字列アルゴリズム (String Algorithms) MOC]]
   - [[文字列アルゴリズムの重要性と応用 (テキスト処理、バイオインフォマティクスなど)]]
   - **文字列探索 (String Matching / Pattern Searching)**
      - **[[単純な文字列探索アルゴリズム (Brute-force / Naive String Search) MOC]]**
         - [[単純文字列探索のアルゴリズムと計算量 (O(mn))]]
      - **[[KMP法 (Knuth-Morris-Pratt Algorithm) MOC]]**
         - [[KMP法のアイデア (不一致時の効率的なシフト)]]
         - [[KMP法のプレフィックス関数 (Prefix Function / π関数 / LPS配列) の構築と利用]]
         - [[KMP法の計算量 (O(m+n))]]
      - **[[ボイヤー・ムーア法 (Boyer-Moore Algorithm) MOC]]**
         - [[ボイヤー・ムーア法のアイデア (テキスト末尾からの比較、大きなシフト)]]
         - [[ボイヤー・ムーア法の悪い文字ヒューリスティック (Bad Character Heuristic)]]
         - [[ボイヤー・ムーア法の良い接尾辞ヒューリスティック (Good Suffix Heuristic / Strong Good Suffix Rule)]]
         - [[ボイヤー・ムーア法の計算量 (最良O(n/m), 最悪O(mn)だが実用上高速)]]
      - **[[ラビン・カープ法 (Rabin-Karp Algorithm) MOC]]**
         - [[ラビン・カープ法のアイデア (ハッシュ関数を利用した比較)]]
         - [[ローリングハッシュ (Rolling Hash) の仕組み]]
         - [[ラビン・カープ法の計算量 (平均O(m+n), 最悪O(mn) - ハッシュ衝突による)]]
      - **[[(オプション) Aho-Corasickアルゴリズム (Aho-Corasick Algorithm) MOC]]** (複数のパターンを同時に検索、トライ木ベース)
      - **[[(オプション) Zアルゴリズム (Z-Algorithm) MOC]]** (文字列内の自身の接頭辞と一致する部分文字列の長さ配列)
   - **文字列に関する問題**
      - **[[最長共通部分列 (Longest Common Subsequence - LCS) MOC]]**
         - [[LCS問題の定義と動的計画法による解法 (O(mn))]]
         - [[LCSの復元]]
      - **[[最長共通部分文字列 (Longest Common Substring) MOC]]**
         - [[Longest Common Substring問題の定義と動的計画法/接尾辞構造による解法]]
      - **[[編集距離 (Edit Distance / Levenshtein Distance) MOC]]**
         - [[編集距離の定義 (挿入、削除、置換)]]
         - [[編集距離の動的計画法による計算 (O(mn))]]
      - **[[回文 (Palindrome) 関連アルゴリズム]]**
         - [[文字列が回文かどうかの判定]]
         - [[最長回文部分文字列 (Longest Palindromic Substring)]] (Manacherアルゴリズムなど)
   - **高度な文字列データ構造**
      - **[[接尾辞木 (Suffix Tree) MOC]]**
         - [[接尾辞木の定義と構造]]
         - [[接尾辞木の構築アルゴリズム (Ukkonen's Algorithmなど - 概要)]]
         - [[接尾辞木の応用 (文字列検索、最長共通部分文字列、最長回文など)]]
      - **[[接尾辞配列 (Suffix Array) MOC]]**
         - [[接尾辞配列の定義とLCP配列 (Longest Common Prefix Array)]]
         - [[接尾辞配列の構築アルゴリズム (O(n log n) or O(n))]]
         - [[接尾辞配列とLCP配列の応用]]
      - **[[トライ木 (Trie)]]** (データ構造セクションでも触れるが、文字列処理における重要性)

## 7. [[数値計算アルゴリズム (Numerical Algorithms) MOC]] (基本的なもの)
   - [[数値計算アルゴリズムの概要と誤差の問題]]
   - **整数論的アルゴリズム**
      - **[[最大公約数 (GCD) の計算]]**
         - [[ユークリッドの互除法 (Euclidean Algorithm)]]
         - [[拡張ユークリッドの互除法 (Extended Euclidean Algorithm)]] (ax + by = gcd(a,b)の解)
      - **[[最小公倍数 (LCM) の計算]]** (GCDを利用)
      - **[[素数判定 (Primality Testing)]]**
         - [[試し割り法 (Trial Division)]]
         - [[エラトステネスの篩 (Sieve of Eratosthenes)]] (一定範囲の素数を列挙)
         - [[(オプション) セグメント化された篩]]
         - [[(オプション) ミラー・ラビン素数判定法 (Miller-Rabin Primality Test)]] (確率的アルゴリズム)
      - **[[素因数分解 (Integer Factorization)]]** (一般に困難)
         - [[試し割り法による素因数分解]]
         - [[(オプション) ポラード・ロー素因数分解法 (Pollard's rho algorithm)]]
      - **[[モジュラ演算 (Modular Arithmetic)]]**
         - [[合同式と剰余演算の性質]]
         - [[モジュラ逆数 (Modular Multiplicative Inverse)]] (拡張ユークリッドの互除法またはフェルマーの小定理利用)
      - **[[べき乗計算 (Exponentiation)]]**
         - [[繰り返し二乗法 (Exponentiation by Squaring / Binary Exponentiation)]] (a^n mod m を効率的に計算)
      - **[[(オプション) 中国剰余定理 (Chinese Remainder Theorem)]]**
   - **基本的な行列演算**
      - [[行列の加算、減算、スカラー倍]]
      - [[行列の乗算アルゴリズム (O(n^3) および Strassenアルゴリズム O(n^log2(7)))]]
      - [[(オプション) ガウスの消去法 (Gaussian Elimination)]] (連立一次方程式の解法)
   - **基本的な数値解析アルゴリズム**
      - [[方程式の求根アルゴリズム]]
         - [[二分法 (Bisection Method)]]
         - [[ニュートン法 (Newton-Raphson Method)]]
      - [[数値積分 (Numerical Integration)]]
         - [[長方形則 (Rectangle Rule)]]
         - [[台形則 (Trapezoidal Rule)]]
         - [[シンプソン則 (Simpson's Rule)]]
      - [[(オプション) 高速フーリエ変換 (FFT - Fast Fourier Transform)]] (多項式の乗算などに応用)

## 8. [[計算幾何学アルゴリズム (Computational Geometry Algorithms) MOC]] (基本的なもの)
   - [[計算幾何学の概要と基本要素 (点、線分、多角形)]]
   - **基本的な幾何学的プリミティブ**
      - [[点の表現と距離計算]]
      - [[ベクトルと内積・外積の計算とその幾何学的意味]]
      - [[線分の表現と交差判定]]
         - [[2線分の交差判定 (外積を利用)]]
      - [[多角形の表現 (頂点列)]]
   - **基本的な問題とアルゴリズム**
      - **[[点が多角形の内部にあるかどうかの判定]]**
         - [[交差数アルゴリズム (Crossing Number Algorithm / Ray Casting Algorithm)]]
         - [[回転数アルゴリズム (Winding Number Algorithm)]]
      - **[[凸包 (Convex Hull) の構築]]**
         - [[凸包の定義と性質]]
         - [[グラハムスキャン (Graham Scan Algorithm)]] (O(n log n))
         - [[ジャービスマーチ (Jarvis March Algorithm / Gift Wrapping Algorithm)]] (O(nh), hは凸包の頂点数)
         - [[(オプション) Monotone Chain Algorithm (Andrew's Algorithm)]] (O(n log n))
         - [[(オプション) Quickhull Algorithm]] (クイックソートに類似)
      - **[[最近傍点対問題 (Closest Pair of Points Problem)]]**
         - [[分割統治法による最近傍点対の発見 (O(n log n))]]
      - **[[(オプション) Voronoi図とDelaunay三角形分割]]** (概念と応用)
      - **[[(オプション) 線分アレンジメントと掃引線アルゴリズム (Sweep Line Algorithm)]]**

## 9. [[計算複雑性理論 (Computational Complexity Theory) MOC]] (アルゴリズムとの関連)
   - [[計算複雑性理論とは (計算問題の困難さの分類)]]
   - [[計算モデル (概要)]]
      - [[チューリングマシン (Turing Machine) の概念]]
      - [[RAMモデル (Random Access Machine)]]
   - **問題クラス**
      - **[[Pクラス (Polynomial Time)]]**
         - [[Pクラスの定義 (多項式時間で解ける決定問題)]]
         - [[Pクラスに属する問題の例]]
      - **[[NPクラス (Nondeterministic Polynomial Time)]]**
         - [[NPクラスの定義 (非決定性チューリングマシンで多項式時間 / 検証が多項式時間)]]
         - [[NPクラスに属する問題の例 (充足可能性問題SAT、ハミルトン閉路問題など)]]
   - **困難性の概念**
      - **[[還元 (Reduction)]]**
         - [[多項式時間還元 (Polynomial-time reduction)]]
      - **[[NP困難 (NP-hard)]]**
         - [[NP困難の定義 (NPクラスの任意の問題から多項式時間還元可能)]]
         - [[NP困難な問題の例 (巡回セールスマン問題の最適化版など)]]
      - **[[NP完全 (NP-complete)]]**
         - [[NP完全の定義 (NPクラスに属し、かつNP困難)]]
         - [[クック・レビンの定理 (Cook-Levin Theorem)]] (SATがNP完全であることの証明 - 概要)
         - [[代表的なNP完全問題のリストと還元関係]]
            - [[3-SAT]]
            - [[頂点被覆問題 (Vertex Cover Problem)]]
            - [[クリーク問題 (Clique Problem)]]
            - [[独立集合問題 (Independent Set Problem)]]
            - [[部分和問題 (Subset Sum Problem)]]
            - [[ハミルトン閉路問題 (Hamiltonian Cycle Problem)]]
            - [[巡回セールスマン問題 (TSP) の決定問題版]]
   - **[[P vs NP問題]]**
      - [[P vs NP問題とは (P=NPかP≠NPか)]]
      - [[P vs NP問題の重要性と影響]]
   - **NP困難問題へのアプローチ**
      - [[指数時間アルゴリズムによる厳密解法 (小規模なインスタンス向け)]]
      - `[[近似アルゴリズム]]`
      - `[[ランダム化アルゴリズム]]`
      - `[[ヒューリスティックアルゴリズム]]`
      - [[パラメータ化計算量 (Parameterized Complexity)]] (概要)
   - **(オプション) その他の複雑性クラス**
      - [[co-NPクラス]]
      - [[PSPACEクラス]]
      - [[EXPTIMEクラス]]