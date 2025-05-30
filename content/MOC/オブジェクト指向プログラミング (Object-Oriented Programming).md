---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/object-oriented-programming
---
## 1. [[OOPの基本概念と歴史 MOC]]
   - **OOPの定義と目的**
      - [[オブジェクト指向プログラミングとは (現実世界の事物をモデル化)]]
      - [[OOPの主な目標 (再利用性、保守性、拡張性、柔軟性の向上)]]
      - [[オブジェクト指向の利点 (大規模開発への適性、理解しやすさ)]]
   - **OOPの歴史的背景**
      - [[Simula言語とオブジェクト指向の萌芽]]
      - [[Smalltalk言語と純粋なオブジェクト指向]]
      - [[C++とオブジェクト指向の普及 (C言語への拡張)]]
      - [[Javaとプラットフォーム非依存のオブジェクト指向]]
      - [[Python, Rubyなどスクリプト言語におけるOOP]]
      - [[その他の影響を与えた言語や概念]]
   - **他のプログラミングパラダイムとの比較**
      - [[手続き型プログラミングとオブジェクト指向プログラミングの違い]]
      - [[関数型プログラミングとオブジェクト指向プログラミングの比較と融合]]
   - **オブジェクト (Object) とクラス (Class) の基本**
      - [[オブジェクトとは (状態と振る舞いを持つ実体)]]
      - [[クラスとは (オブジェクトの設計図/テンプレート)]]
      - [[インスタンス (Instance) とは (クラスから生成されたオブジェクト)]]
      - [[メッセージパッシング (Message Passing) の概念]]

## 2. [[OOPの四大原則 (または三大原則 + 抽象化) MOC]]
   - **[[カプセル化 (Encapsulation) MOC]]**
      - [[カプセル化の定義 (データとそれを操作するメソッドの結合)]]
      - [[情報隠蔽 (Information Hiding) との関係]]
      - [[カプセル化の利点 (データ保護、モジュール性向上、インターフェースの安定化)]]
      - [[アクセス修飾子によるカプセル化の実現]]
   - **[[継承 (Inheritance) MOC]]**
      - [[継承の定義 (既存クラスの特性を引き継ぐ)]] (IS-A関係)
      - [[スーパークラス (Superclass) / 親クラス (Parent Class) / 基底クラス (Base Class)]]
      - [[サブクラス (Subclass) / 子クラス (Child Class) / 派生クラス (Derived Class)]]
      - [[継承の利点 (コードの再利用、階層構造の表現、拡張性)]]
      - [[継承の課題 (スーパークラスへの密結合、 fragile base class問題)]]
   - **[[ポリモーフィズム (Polymorphism) / 多態性 MOC]]**
      - [[ポリモーフィズムの定義 (同じインターフェースで異なる動作)]]
      - [[ポリモーフィズムの利点 (柔軟性、拡張性、疎結合)]]
      - [[静的ポリモーフィズムと動的ポリモーフィズム]]
   - **[[抽象化 (Abstraction) MOC]]**
      - [[抽象化の定義 (本質的な特徴の抽出、詳細の隠蔽)]]
      - [[データ抽象化と手続き抽象化]]
      - [[OOPにおける抽象化の役割 (インターフェース、抽象クラス)]]

## 3. [[クラスとオブジェクトの詳細 MOC]]
   - **クラスの定義**
      - [[クラスの構成要素]]
         - **[[属性 (Attribute) / フィールド (Field) / メンバ変数 (Member Variable) / プロパティ (Property)]]** (オブジェクトの状態)
            - [[インスタンス変数 (Instance Variable)]]
            - **[[クラス変数 (Class Variable) / 静的メンバ変数 (Static Member Variable)]]**
         - **[[メソッド (Method) / メンバ関数 (Member Function) / 操作 (Operation)]]** (オブジェクトの振る舞い)
            - [[インスタンスメソッド (Instance Method)]]
            - **[[クラスメソッド (Class Method) / 静的メソッド (Static Method)]]**
      - [[クラス定義の構文 (各言語での例)]]
   - **オブジェクトの生成と消滅**
      - **[[インスタンス化 (Instantiation)]]** (オブジェクトの生成プロセス)
      - **[[コンストラクタ (Constructor)]]**
         - [[コンストラクタの役割 (オブジェクトの初期化)]]
         - [[デフォルトコンストラクタ]]
         - [[パラメータ付きコンストラクタ]]
         - [[コンストラクタのオーバーロード]] (言語による)
         - [[コピーコンストラクタ]] (C++など)
      - **[[デストラクタ (Destructor) / ファイナライザ (Finalizer)]]** (言語による)
         - [[デストラクタの役割 (オブジェクトの解放処理)]]
         - [[ガベージコレクション (Garbage Collection) とデストラクタの関係]]
      - [[オブジェクトの生存期間 (Object Lifetime)]] (スタック確保とヒープ確保)
   - **`this` / `self` キーワード**
      - [[this/self の役割 (現在のオブジェクトインスタンスへの参照)]]
      - [[this/self の使い方 (メソッド内でのメンバアクセス、コンストラクタ呼び出し)]]
   - **アクセスメソッド (Access Methods)**
      - **[[アクセサ (Accessor) / ゲッター (Getter)]]** (属性値の取得)
      - **[[ミューテータ (Mutator) / セッター (Setter)]]** (属性値の設定)
      - [[プロパティ (Property) の概念]] (C#, Pythonなど)
   - **アクセス修飾子 (Access Modifiers) / 可視性 (Visibility)**
      - `[[public]]` (公開)
      - `[[private]]` (非公開)
      - `[[protected]]` (保護、サブクラスからのアクセス許可)
      - `[[package` / `internal` / `friend]]` (言語固有のアクセスレベル)
      - [[アクセス修飾子とカプセル化の関係]]
   - **[[(オプション) ネストクラス (Nested Class) / 内部クラス (Inner Class)]]**

## 4. [[カプセル化 (Encapsulation) の詳細 MOC]] (再掲・深掘り)
   - [[情報隠蔽の原則とデータ隠蔽]]
   - [[インターフェース (Interface) と実装 (Implementation) の分離]]
   - [[カプセル化の実現方法 (アクセス修飾子、アクセサ/ミューテータ)]]
   - [[カプセル化の利点 (保守性の向上、影響範囲の限定、再利用性の促進)]]
   - [[カプセル化の破綻 (過度なゲッター/セッターなど)]]

## 5. [[継承 (Inheritance) の詳細 MOC]] (再掲・深掘り)
   - **継承の種類**
      - **[[単一継承 (Single Inheritance)]]**
      - **[[多重継承 (Multiple Inheritance)]]** (C++, Pythonなど)
         - [[多重継承の利点と課題 (菱形継承問題 - Diamond Problem)]]
         - [[菱形継承問題の解決策 (仮想継承 - C++, Mixin - Python/Ruby)]]
      - [[多段階継承 (Multilevel Inheritance)]]
      - [[階層的継承 (Hierarchical Inheritance)]]
      - [[ハイブリッド継承 (Hybrid Inheritance)]]
   - **メソッドのオーバーライド (Method Overriding)**
      - [[オーバーライドの定義 (スーパークラスのメソッドをサブクラスで再定義)]]
      - [[オーバーライドのルール (シグネチャ、戻り値、アクセス修飾子 - 言語による)]]
      - `[[super` / `base]]` キーワードによるスーパークラスメソッドの呼び出し
      - [[アノテーション (Annotation) / 属性 (Attribute) によるオーバーライドの明示]] (例: `@Override` in Java)
   - **抽象クラス (Abstract Class) と抽象メソッド (Abstract Method)**
      - [[抽象クラスの定義 (インスタンス化できないクラス、純粋仮想関数を持つクラス)]]
      - [[抽象メソッドの定義 (実装を持たないメソッド、サブクラスでの実装を強制)]]
      - [[抽象クラスの役割 (共通インターフェースの提供、テンプレート)]]
   - **インターフェース (Interface)** (Java, C#など)
      - [[インターフェースの定義 (メソッドのシグネチャのみを定義)]]
      - [[インターフェースの実装 (implements / :)]]
      - [[インターフェースと抽象クラスの違いと比較]]
      - [[インターフェースの多重実装 (多重継承の代替)]]
      - [[デフォルトメソッドと静的メソッド (インターフェースの進化)]] (Java 8以降など)
   - **`final` / `sealed` キーワード**
      - `[[final` / `sealed` クラス (継承禁止)]]
      - `[[final` / `sealed` メソッド (オーバーライド禁止)]]
   - **継承の設計原則**
      - [[Liskovの置換原則 (LSP) と継承]] (詳細は設計原則にて)
      - **[[委譲 (Delegation) と継承の比較]]**
      - **[[集約 (Aggregation) とコンポジション (Composition) による「has-a」関係]]**
         - **[[「継承よりコンポジション (Composition over Inheritance)」の原則]]**

## 6. [[ポリモーフィズム (Polymorphism) の詳細 MOC]] (再掲・深掘り)
   - **静的ポリモーフィズム (Static Polymorphism / Compile-time Polymorphism / Early Binding)**
      - **[[メソッドのオーバーロード (Method Overloading) / 関数のオーバーロード]]**
         - [[オーバーロードの定義 (同じ名前で異なるシグネチャのメソッド)]]
         - [[オーバーロードの解決メカニズム]]
      - **[[演算子のオーバーロード (Operator Overloading)]]** (C++, Pythonなど)
         - [[演算子オーバーロードの利点と注意点 (可読性)]]
      - **[[(オプション) ジェネリクス (Generics) / テンプレート (Templates) と静的ポリモーフィズム]]**
   - **動的ポリモーフィズム (Dynamic Polymorphism / Run-time Polymorphism / Late Binding)**
      - **[[メソッドのオーバーライド (Method Overriding) と動的ディスパッチ (Dynamic Dispatch / Virtual Method Invocation)]]**
         - [[仮想関数テーブル (vtable / vtbl) の概念]] (C++など)
      - [[抽象クラスやインターフェースを通じた動的ポリモーフィズムの実現]]
      - **[[ダックタイピング (Duck Typing)]]** (動的型付け言語 - Python, Rubyなど)
         - [[「アヒルのように歩き、アヒルのように鳴けば、それはアヒルである」]]
   - **ポリモーフィズムの具体例とユースケース**
      - [[図形描画プログラムにおけるポリモーフィズム]]
      - [[UIイベント処理におけるポリモーフィズム]]
      - [[プラグインアーキテクチャにおけるポリモーフィズム]]
   - **ポリモーフィズムの利点 (再掲)**

## 7. [[オブジェクト指向設計原則 (Object-Oriented Design Principles) MOC]]
   - **[[SOLID原則 MOC]]**
      - **[[S: 単一責任の原則 (SRP - Single Responsibility Principle)]]**
         - [[SRPの定義 (クラスが持つべき責任は一つだけ)]]
         - [[SRP違反の兆候とリファクタリング]]
      - **[[O: オープン/クローズドの原則 (OCP - Open/Closed Principle)]]**
         - [[OCPの定義 (拡張に対して開いており、修正に対して閉じている)]]
         - [[OCPの実現方法 (抽象化、ポリモーフィズム、継承、戦略パターンなど)]]
      - **[[L: Liskovの置換原則 (LSP - Liskov Substitution Principle)]]**
         - [[LSPの定義 (サブクラスはスーパークラスの型に置換可能でなければならない)]]
         - [[LSP違反の兆候 (サブクラスでのメソッドの振る舞いの変更、事前条件の強化、事後条件の弱化)]]
      - **[[I: インターフェース分離の原則 (ISP - Interface Segregation Principle)]]**
         - [[ISPの定義 (クライアントに不要なインターフェースへの依存を強制しない)]]
         - [[ISP違反の兆候 (Fat Interface) とリファクタリング (インターフェースの分割)]]
      - **[[D: 依存性逆転の原則 (DIP - Dependency Inversion Principle)]]**
         - [[DIPの定義 (上位モジュールは下位モジュールに依存すべきではない。両者は抽象に依存すべき)]]
         - [[DIPの実現方法 (抽象インターフェース、依存性注入 - DI)]]
   - **その他の重要な設計原則**
      - **[[DRY原則 (Don't Repeat Yourself)]]**
      - **[[KISS原則 (Keep It Simple, Stupid)]]**
      - **[[YAGNI原則 (You Ain't Gonna Need It)]]**
      - **[[デメテルの法則 (Law of Demeter / Principle of Least Knowledge)]]** (最小知識の原則)
      - **[[Tell, Don't Askの原則]]**
      - **[[関心の分離 (SoC - Separation of Concerns)]]**
   - **[[(オプション) GRASP原則 (General Responsibility Assignment Software Patterns) MOC]]** (Information Expert, Creator, Controller, Low Coupling, High Cohesionなど)

## 8. [[デザインパターン (Design Patterns) - OOPの文脈で MOC]]
   - **デザインパターンとは**
      - [[デザインパターンの定義 (GoF - Gang of Four)]]
      - [[デザインパターンの利点 (共通語彙、再利用可能な設計知見、品質向上)]]
      - [[デザインパターンの分類 (生成、構造、振る舞い)]]
   - **[[生成に関するパターン (Creational Patterns) MOC]]**
      - [[Singletonパターン (シングルトン)]]
      - [[Factory Methodパターン (ファクトリーメソッド)]]
      - [[Abstract Factoryパターン (抽象ファクトリー)]]
      - [[Builderパターン (ビルダー)]]
      - [[Prototypeパターン (プロトタイプ)]]
      - [[(オプション) Object Poolパターン]]
   - **[[構造に関するパターン (Structural Patterns) MOC]]**
      - [[Adapterパターン (アダプター)]]
      - [[Decoratorパターン (デコレーター)]]
      - [[Compositeパターン (コンポジット)]]
      - [[Facadeパターン (ファサード)]]
      - [[Proxyパターン (プロキシ)]]
      - [[Bridgeパターン (ブリッジ)]]
      - [[Flyweightパターン (フライ級)]]
   - **[[振る舞いに関するパターン (Behavioral Patterns) MOC]]**
      - [[Observerパターン (オブザーバー) / Publish-Subscribeパターン]]
      - [[Strategyパターン (ストラテジー) / Policyパターン]]
      - [[Commandパターン (コマンド)]]
      - [[Iteratorパターン (イテレーター)]]
      - [[Template Methodパターン (テンプレートメソッド)]]
      - [[Stateパターン (ステート)]]
      - [[Chain of Responsibilityパターン (責任の連鎖)]]
      - [[Visitorパターン (ビジター)]]
      - [[Mediatorパターン (メディエーター)]]
      - [[Mementoパターン (メメント)]]
      - [[Interpreterパターン (インタープリター)]]
      - [[(オプション) Null Objectパターン]]
   - **デザインパターンの選択と適用**

## 9. [[OOPにおける関連概念と高度なトピック MOC]]
   - **オブジェクト間の関係**
      - [[関連 (Association)]] (Uses-A)
      - [[集約 (Aggregation)]] (Has-A, 弱い所有関係)
      - [[コンポジション (Composition)]] (Has-A, 強い所有関係、部品関係)
   - **例外処理 (Exception Handling) とOOP**
      - [[例外クラス階層]]
      - [[カスタム例外の定義]]
   - **ジェネリクス (Generics) / テンプレート (Templates) とOOP**
      - [[型安全なコレクション]]
      - [[ジェネリックアルゴリズム]]
   - **リフレクション (Reflection) とメタプログラミング (Metaprogramming)**
      - [[実行時のクラス情報取得と操作]]
      - [[アノテーション (Annotation) / 属性 (Attribute) とリフレクション]]
   - **オブジェクトのシリアライズ (Serialization) / デシリアライズ (Deserialization)**
   - **不変オブジェクト (Immutable Object)**
      - [[不変オブジェクトの利点 (スレッドセーフティ、予測可能性)]]
   - **値オブジェクト (Value Object) vs エンティティ (Entity)** (ドメイン駆動設計の文脈)
   - **契約による設計 (Design by Contract - DbC)** (事前条件、事後条件、不変条件 - Eiffel言語など)
   - **アスペクト指向プログラミング (AOP - Aspect-Oriented Programming)** (OOPを補完する概念 - 横断的関心事の分離)

## 10. [[OOPの利点と欠点 (再評価) MOC]]
   - **利点 (まとめ)**
      - [[再利用性、保守性、拡張性、柔軟性、モジュール性、理解しやすさ]]
   - **欠点と課題**
      - [[学習コストの高さ]]
      - [[過度な設計 (Over-engineering) の可能性]]
      - [[実行時オーバーヘッド (仮想メソッド呼び出しなど)]]
      - [[必ずしもすべての問題に適しているわけではない]]
      - [[継承の誤用による問題]]

## 11. [[プログラミング言語とOOP MOC]] (各言語での特徴的な実装や考え方)
   - [[JavaにおけるOOP (インターフェース、抽象クラス、final、GCなど)]]
   - [[C++におけるOOP (多重継承、仮想関数、RAII、手動メモリ管理)]]
   - [[PythonにおけるOOP (動的型付け、ダックタイピング、__init__, self, MRO, Mixin)]]
   - [[C#におけるOOP (プロパティ、イベント、デリゲート、LINQとの連携)]]
   - [[JavaScriptにおけるOOP (プロトタイプベース、ES6以降のclass構文)]]
   - [[RubyにおけるOOP (純粋なオブジェクト指向、Mixinモジュール、メタプログラミング)]]
   - [[SmalltalkにおけるOOP (純粋なオブジェクト指向、メッセージパッシング)]]
   - [[Scala / Kotlin におけるOOPと関数型の融合]]

## 12. [[(オプション) OOPアンチパターン MOC]]
   - [[神クラス (God Class / God Object)]]
   - [[貧血ドメインモデル (Anemic Domain Model)]]
   - [[循環依存 (Circular Dependency)]]
   - [[Lava Flow]]
   - [[Poltergeists]]
   - [[Yo-yo problem (ヨーヨー問題)]] (過度な継承階層)