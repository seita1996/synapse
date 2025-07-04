---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/ios
---
## 1. [[iOS開発入門 MOC]]
   - **iOS開発とは**
      - [[iOS開発の定義 (iPhone, iPad, Apple Watch, Apple TVなどのAppleプラットフォーム向けアプリ開発)]]
      - [[iOSエコシステムとApp Store]]
      - [[iOS開発者に必要なスキルセット (技術、デザイン感覚、ビジネス理解)]]
   - **iOS開発の歴史と進化**
      - `[[iPhone OSからiOSへ]]`
      - `[[Objective-CからSwiftへの移行]]`
      - `[[UIフレームワークの変遷 (UIKitからSwiftUIへ)]]`
      - `[[主要なiOSバージョンの変遷と新機能]]`
   - **開発を始めるための準備**
      - `[[必要な機材 (Mac)]]`
      - `[[Apple Developer Programへの登録 (無料アカウントと有料アカウントの違い)]]`
      - `[[Xcodeのインストールとセットアップ]]`
      - `[[iOSシミュレータと実機でのテスト]]`
   - **iOSアプリのライフサイクル (概観)**
      - `[[アプリの状態 (Not Running, Inactive, Active, Background, Suspended)]]`
   - **iOS開発の学習ロードマップ (例)**

## 2. [[Swiftプログラミング言語 MOC]]

### 2.1. [[Swiftの基本 MOC]]
   - **Swiftとは**
      - [[Swiftの概要と特徴 (安全性, 高速性, 表現力豊かさ)]]
      - [[Objective-Cとの相互運用性]]
      - [[オープンソース言語としてのSwift]]
   - **基本構文**
      - `[[変数 (`var`) と定数 (`let`)]]`
      - `[[型推論 (Type Inference) と型アノテーション (Type Annotation)]]`
      - **[[基本的なデータ型]]** (`Int`, `Double`, `Float`, `Bool`, `String`, `Character`)
      - `[[型安全性 (Type Safety)]]`
      - `[[演算子 (算術, 比較, 論理, レンジなど)]]`
      - `[[文字列と文字 (String and Character)]]`
      - `[[コレクション型 (Array, Set, Dictionary)]]`
      - `[[制御構文 (if/else, switch, for-in, while, repeat-while, guard)]]`
      - `[[タプル (Tuples)]]`
   - **[[オプショナル (Optionals) MOC]]**
      - [[オプショナル型の概念 (値が存在しない可能性の明示)]]
      - `[[オプショナルバインディング (`if let`, `guard let`)]]`
      - `[[オプショナルチェイニング (`?`)]]`
      - `[[Nil結合演算子 (`??`)]]`
      - `[[強制アンラップ (`!`) とその危険性]]`
      - `[[暗黙的アンラップオプショナル (Implicitly Unwrapped Optionals)]]`

### 2.2. [[関数とクロージャ (Functions and Closures) MOC]]
   - **関数 (Functions)**
      - `[[関数の定義と呼び出し]]`
      - `[[引数ラベルとパラメータ名]]`
      - `[[デフォルト引数]]`
      - `[[可変長引数]]`
      - `[[in-out引数]]`
      - `[[関数型 (Function Types)]]`
      - `[[高階関数 (Higher-Order Functions)]]`
   - **クロージャ (Closures)**
      - `[[クロージャ式の構文]]`
      - `[[後置クロージャ (Trailing Closures)]]`
      - `[[キャプチャリスト (Capture Lists) と循環参照]]` (`[weak self]`, `[unowned self]`)
      - `[[エスケープクロージャ (`@escaping`)]]`
      - `[[オートクロージャ (`@autoclosure`)]]`

### 2.3. [[クラス、構造体、列挙型 (Classes, Structures, and Enumerations) MOC]]
   - **[[クラス (Classes) と構造体 (Structures) の比較 MOC]]**
      - `[[共通点 (プロパティ、メソッド、イニシャライザ、サブスクリプト、エクステンション、プロトコル準拠)]]`
      - `[[相違点 (継承, 型キャスト, デイニシャライザ, 参照カウントはクラスのみ)]]`
      - **[[値型 (Value Types) vs. 参照型 (Reference Types)]]** (最も重要な違い)
      - `[[どちらをいつ使うか]]`
   - **プロパティ (Properties)**
      - `[[ストアドプロパティ (Stored Properties)]]`
      - `[[コンピューテッドプロパティ (Computed Properties)]]`
      - `[[プロパティオブザーバ (`willSet`, `didSet`)]]`
      - `[[型プロパティ (`static`)]]`
      - `[[遅延ストアドプロパティ (`lazy`)]]`
   - **メソッド (Methods)**
      - `[[インスタンスメソッド]]`
      - `[[型メソッド (`static` / `class`)]]`
      - `[[`mutating` メソッド (値型向け)]]`
   - **サブスクリプト (Subscripts)**
   - **継承 (Inheritance)** (クラスのみ)
      - `[[スーパークラスとサブクラス]]`
      - `[[オーバーライド (`override`)]]`
      - `[[`final` キーワード]]`
   - **イニシャライザ (Initializers)**
      - `[[指定イニシャライザ (Designated Initializer) と便宜イニシャライザ (Convenience Initializer)]]`
      - `[[必須イニシャライザ (`required`)]]`
      - `[[失敗可能イニシャライザ (`init?`)]]`
   - **デイニシャライザ (Deinitializers)** (`deinit`)
   - **[[列挙型 (Enumerations - Enums) MOC]]**
      - `[[基本的なenumの定義]]`
      - `[[関連値 (Associated Values)]]`
      - `[[Raw値 (Raw Values)]]`
      - `[[再帰的enum (`indirect`)]]`
      - `[[enumと`switch`文の組み合わせ]]`

### 2.4. [[プロトコルとエクステンション (Protocols and Extensions) MOC]]
   - **[[プロトコル (Protocols) MOC]]**
      - [[プロトコルの定義と役割 (特定の機能の設計図)]]
      - `[[プロパティ要件とメソッド要件]]`
      - `[[Mutatingメソッド要件]]`
      - `[[イニシャライザ要件]]`
      - `[[プロトコルを型として使用する]]`
      - `[[デリゲートパターン (Delegate Pattern)]]`
      - `[[プロトコル合成 (Protocol Composition)]]`
      - `[[プロトコル指向プログラミング (POP - Protocol-Oriented Programming)]]`
   - **[[エクステンション (Extensions) MOC]]**
      - [[エクステンションの定義と役割 (既存の型に機能を追加)]]
      - `[[コンピューテッドプロパティの追加]]`
      - `[[メソッドの追加]]`
      - `[[イニシャライザの追加]]`
      - `[[プロトコル準拠の追加]]`
   - **[[ジェネリクス (Generics) MOC]]**
      - [[ジェネリック関数とジェネリック型]]
      - `[[型制約 (Type Constraints)]]`
      - `[[関連型 (`associatedtype`) を持つプロトコル]]`

### 2.5. [[エラー処理 (Error Handling) MOC]]
   - `[[`Error` プロトコル]]`
   - `[[`throw`, `throws`]]`
   - `[[`do-catch` 文]]`
   - `[[`try?` と `try!`]]`
   - `[[`defer` 文]]`

### 2.6. [[非同期処理 (Concurrency) MOC]]
   - **[[Grand Central Dispatch (GCD) と OperationQueue MOC]]** (伝統的な手法)
      - `[[DispatchQueue (Serial vs. Concurrent)]]`
      - `[[`DispatchQueue.main` と `DispatchQueue.global()`]]`
      - `[[`async` と `sync`]]`
      - `[[Operation と OperationQueue]]`
   - **[[Swift Concurrency (Swift 5.5+) MOC]]**
      - `[[`async` / `await` 構文]]`
      - `[[非同期シーケンス (`AsyncSequence`)]]`
      - `[[構造化並行性 (Structured Concurrency - `Task`, `TaskGroup`)]]`
      - `[[アクター (Actors)]]` (状態の分離とスレッドセーフティ)
      - `[[`MainActor`]]` (UI更新の保証)
      - `[[`Sendable` プロトコル]]`

### 2.7. [[メモリ管理 (Memory Management) MOC]]
   - **[[自動参照カウント (ARC - Automatic Reference Counting)]]**
      - [[ARCの仕組み]]
      - **[[循環参照 (Strong Reference Cycles) とその解決策]]**
         - `[[弱参照 (`weak`)]]`
         - `[[非所有参照 (`unowned`)]]`
         - `[[クロージャにおけるキャプチャリスト]]` (再掲)
   - **値型と参照型のメモリ挙動**

### 2.8. [[Swift Package Manager (SPM) MOC]]
   - [[SPMの役割 (依存関係管理ツール)]]
   - `[[`Package.swift` マニフェストファイル]]`
   - [[パッケージの追加、更新、削除]]
   - [[Xcodeプロジェクトとの統合]]

## 3. [[UIフレームワーク MOC]]

### 3.1. [[SwiftUI MOC]] (モダンな宣言的UIフレームワーク)
   - **SwiftUIの基本**
      - [[SwiftUIの思想 (宣言的構文、状態駆動、クロスプラットフォーム)]]
      - [[Viewプロトコルと`body`プロパティ]]
   - **基本的なView**
      - `[[Text, Image, Button, TextField, SecureField, Slider, Toggle, Picker]]`
   - **レイアウトコンテナ**
      - `[[VStack, HStack, ZStack]]`
      - `[[Spacer, Divider]]`
      - `[[ScrollView, List, Form]]`
      - `[[LazyVStack, LazyHStack, Grid]]`
      - `[[GeometryReader]]`
   - **状態管理 (State Management)**
      - `[[`@State`]]` (Viewローカルな状態)
      - `[[`@Binding`]]` (親子間の状態共有)
      - `[[`@ObservedObject`, `@StateObject`, `@EnvironmentObject`]]` (参照型の状態管理)
      - `[[ObservableObject` プロトコルと `@Published` プロパティラッパー]]`
      - `[[`@Environment`]]` (環境値)
   - **ナビゲーション**
      - `[[NavigationView / NavigationStack]]`
      - `[[NavigationLink]]`
      - `[[シート (Sheet) とモーダル表示]]`
      - `[[TabView]]`
   - **リストとデータ**
      - `[[`List` と `ForEach`]]`
      - `[[Identifiable` プロトコル]]`
   - **描画とグラフィックス**
      - `[[図形 (Shape - Rectangle, Circle, Path)]]`
      - `[[色 (Color) とグラデーション (Gradient)]]`
      - `[[Canvas]]`
   - **アニメーションとトランジション**
      - `[[暗黙的アニメーション (`.animation()`)]]`
      - `[[明示的アニメーション (`withAnimation`)]]`
      - `[[トランジション (`.transition()`)]]`
   - **SwiftUIとUIKit/AppKitの連携**
      - `[[`UIViewRepresentable`]]`
      - `[[`UIViewControllerRepresentable`]]`
   - **SwiftUIのライフサイクル (`@main` と `App`, `Scene`)**

### 3.2. [[UIKit MOC]] (伝統的な命令的UIフレームワーク)
   - **UIKitの基本**
      - [[UIKitの思想 (命令的、オブジェクト指向、MVCパターン)]]
      - `[[UIView` とそのサブクラス]]`
   - **主要なUIコンポーネント**
      - `[[UILabel, UIImageView, UIButton, UITextField, UITextView]]`
      - `[[UISwitch, UISlider, UIStepper]]`
      - `[[UITableView` と `UITableViewCell`]]`
      - `[[UICollectionView` と `UICollectionViewCell`]]`
      - `[[UIScrollView]]`
      - `[[UIStackView]]`
      - `[[UIAlertController]]`
   - **[[ViewController (UIViewController) MOC]]**
      - [[ViewControllerの役割とライフサイクル]] (`viewDidLoad`, `viewWillAppear`, `viewDidAppear`など)
   - **[[Auto Layout と制約 (Constraints) MOC]]**
      - [[Auto Layoutの概念と目的]]
      - [[Interface Builder (Storyboard/XIB) での制約設定]]
      - [[コードによる制約設定 (NSLayoutConstraint, Visual Format Language, Layout Anchors)]]
   - **[[ナビゲーション (Navigation) MOC]]**
      - `[[UINavigationController]]` (プッシュ/ポップ)
      - `[[UITabBarController]]`
      - `[[モーダル表示 (Present/Dismiss)]]`
      - `[[セグエ (Segue)]]`
   - **[[イベント処理 (Event Handling) MOC]]**
      - `[[ターゲット/アクション (Target/Action) パターン]]`
      - `[[デリゲート (Delegate) パターン]]`
      - `[[ジェスチャー認識 (`UIGestureRecognizer`)]]`
   - **[[テーブルビュー (UITableView) の詳細 MOC]]**
      - `[[UITableViewDataSource` と `UITableViewDelegate`]]`
      - `[[セルの再利用]]`
      - `[[カスタムセル]]`
   - **[[コレクションビュー (UICollectionView) の詳細 MOC]]**
      - `[[UICollectionViewDataSource` と `UICollectionViewDelegate`]]`
      - `[[レイアウト (`UICollectionViewFlowLayout`など)]]`
   - **描画とアニメーション**
      - `[[Core Graphics]]`
      - `[[Core Animation]]`
      - `[[UIViewアニメーション]]`
   - **Interface Builder (Storyboard, XIB/NIB)**
      - [[StoryboardとXIBの使い分け]]

### 3.3. [[SwiftUI vs. UIKit MOC]]
   - `[[宣言的 vs. 命令的]]`
   - `[[状態管理のアプローチ]]`
   - `[[学習曲線と生産性]]`
   - `[[パフォーマンスと柔軟性]]`
   - `[[相互運用性と移行戦略]]`
   - `[[どちらをいつ選ぶか]]`

## 4. [[iOSアプリのアーキテクチャ MOC]]
   - **アーキテクチャの重要性 (保守性、テスト容易性、拡張性)**
   - **[[MVC (Model-View-Controller) MOC]]** (Appleの伝統的パターン)
      - `[[Massive View Controller問題]]`
   - **[[MVVM (Model-View-ViewModel) MOC]]**
      - `[[ViewModelの役割 (ViewとModelの仲介、ビジネスロジック)]]`
      - `[[データバインディング (RxSwift/Combine, またはSwiftUIの仕組み)]]`
      - `[[MVVMとSwiftUI/UIKit]]`
   - **[[VIPER (View-Interactor-Presenter-Entity-Router) MOC]]**
      - `[[各コンポーネントの明確な責任分離]]`
      - `[[VIPERの利点と複雑性]]`
   - **[[Clean Architecture MOC]]** (iOSへの適用)
      - `[[レイヤー構造 (Entities, Use Cases, Interface Adapters, Frameworks & Drivers)]]`
      - `[[依存性のルール]]`
   - **[[TCA (The Composable Architecture) MOC]]** (SwiftUI向け)
      - `[[State, Action, Reducer, Environment, Store]]`
      - `[[関数型プログラミングの影響]]`
   - **[[ルーティング/ナビゲーションの設計 (Coordinatorパターンなど)]]**
   - **[[依存性の注入 (Dependency Injection - DI) の実践]]**

## 5. [[データ管理と永続化 MOC]]
   - **[[UserDefaults MOC]]** (少量のデータ保存)
   - **[[ファイルシステム (File System) MOC]]**
      - `[[`FileManager`]]`
      - `[[アプリのサンドボックスとディレクトリ構造 (Documents, Library, tmp)]]`
      - `[[Property List (`.plist`)]]`
   - **[[Core Data MOC]]** (Appleのオブジェクトグラフ管理フレームワーク)
      - `[[Core Dataスタック (NSManagedObjectModel, NSPersistentStoreCoordinator, NSManagedObjectContext)]]`
      - `[[NSManagedObject]]`
      - `[[データのフェッチ (`NSFetchRequest`)]]`
      - `[[Core DataとSwiftUI]]`
   - **[[Realm MOC]]** (モバイル向けデータベース)
      - `[[Realmの概要と特徴 (高速性、使いやすさ)]]`
      - `[[Realmオブジェクトとトランザクション]]`
   - **[[SQLite MOC]]** (低レベルなデータベースアクセス)
      - `[[FMDBなどのラッパーライブラリ]]`
   - **[[キーチェーン (Keychain) MOC]]** (パスワードやトークンなどの機密データ保存)
   - **[[CloudKit MOC]]** (iCloudとのデータ同期)
   - **[[Firebase Realtime Database / Firestore MOC]]** (BaaSの活用)

## 6. [[ネットワーク通信 MOC]]
   - **[[URLSession MOC]]** (HTTP/HTTPS通信の標準API)
      - `[[`URLSessionDataTask`, `URLSessionUploadTask`, `URLSessionDownloadTask`]]`
      - `[[`URLRequest` と `URLResponse`]]`
      - `[[デリゲートベースとクロージャベースのAPI]]`
      - `[[Swift Concurrencyとの連携 (`URLSession.shared.data(from:)`)]]`
   - **[[JSONのパース (Parsing) MOC]]**
      - `[[`Codable` プロトコル (`Encodable` & `Decodable`)]]`
      - `[[`JSONEncoder` と `JSONDecoder`]]`
   - **ネットワークライブラリの活用**
      - `[[Alamofire]]` (サードパーティライブラリ)
   - **APIクライアントの設計**
   - **ネットワーク状態の監視 (`Network.framework`)**
   - **GraphQLクライアント (`Apollo iOS`)**

## 7. [[iOSの主要なフレームワークとAPI MOC]]
   - **位置情報と地図**
      - `[[Core Location MOC]]` (GPS, Wi-Fi, ビーコンによる位置情報取得)
      - `[[MapKit MOC]]` (地図表示とアノテーション)
   - **マルチメディア**
      - `[[AVFoundation MOC]]` (音声・動画の再生と録画)
      - `[[Photos MOC]]` (写真ライブラリへのアクセス)
   - **センサー**
      - `[[Core Motion MOC]]` (加速度計、ジャイロスコープ)
   - **UI/UX拡張**
      - `[[Core Animation MOC]]` (高度なアニメーション)
      - `[[Core Graphics MOC]]` (2D描画)
   - **機械学習**
      - `[[Core ML MOC]]` (学習済みモデルの実行)
      - `[[Vision MOC]]` (画像分析)
      - `[[Natural Language MOC]]` (自然言語処理)
   - **拡張現実 (AR)**
      - `[[ARKit MOC]]`
   - **通知 (Notifications)**
      - `[[ローカル通知 (Local Notifications)]]`
      - `[[プッシュ通知 (Push Notifications - APNs)]]`
   - **バックグラウンド処理 (Background Modes)**
   - **App Extensions** (Today Widget, Share Extensionなど)

## 8. [[テストと品質保証 MOC]]
   - **[[XCTestフレームワーク MOC]]**
      - `[[ユニットテスト (`XCTestCase`)]]`
      - `[[UIテスト (`XCUIApplication`, `XCUIElement`)]]`
      - `[[パフォーマンステスト (`measure`)]]`
   - **テスト戦略**
      - `[[テストピラミッドの適用]]`
      - `[[TDD/BDDの実践]]`
   - **モックとスタブ**
      - `[[プロトコルを用いたモック作成]]`
   - **コードカバレッジ**
   - **CI/CDパイプラインとの統合**
   - **デバッグ手法**
      - `[[Xcodeデバッガ (LLDB) の活用]]`
      - `[[ブレークポイントと変数監視]]`
      - `[[Viewデバッギング]]`
      - `[[メモリグラフデバッガ]]`
   - **クラッシュレポートと分析 (Firebase Crashlyticsなど)**
   - **TestFlightによるベータテスト**

## 9. [[アプリのリリースと運用 MOC]]
   - **[[App Store Connect MOC]]**
      - `[[アプリの登録とメタデータ管理]]`
      - `[[スクリーンショットとプレビュー動画]]`
      - `[[ビルドのアップロードと管理]]`
   - **プロビジョニングとコード署名**
      - `[[証明書 (Certificates), 識別子 (Identifiers), プロファイル (Profiles)]]`
   - **ビルド構成とスキーム**
      - `[[DebugビルドとReleaseビルド]]`
      - `[[複数の環境 (開発、ステージング、本番) の管理]]`
   - **App Store審査ガイドライン**
      - `[[よくあるリジェクト理由]]`
   - **アプリ内課金 (In-App Purchase)**
   - **アプリの分析 (App Analytics)**
   - **アプリのアップデートとバージョニング**
   - **ユーザーレビューへの対応**

## 10. [[Objective-C MOC]] (レガシーと相互運用性)
   - **Objective-Cの基本**
      - `[[C言語のスーパーセットとしての特徴]]`
      - `[[メッセージ式構文 (`[receiver message]`)]]`
      - `[[ヘッダファイル (`.h`) と実装ファイル (`.m`)]]`
      - `[[ポインタとメモリ管理 (手動参照カウント - MRC)]]`
   - **Foundationフレームワーク** (`NSString`, `NSArray`, `NSDictionary`など)
   - **[[SwiftとObjective-Cの相互運用性 MOC]]**
      - `[[ブリッジングヘッダ (Bridging Header)]]` (SwiftからObjective-Cを呼び出す)
      - `[[`@objc` と `@objcMembers`]]` (Objective-CからSwiftを呼び出す)
   - **既存のObjective-Cコードベースの保守とSwiftへの移行戦略**

## 11. [[iOS開発のベストプラクティスとコミュニティ MOC]]
   - **Appleのヒューマンインターフェースガイドライン (HIG)**
   - **セキュアコーディングプラクティス**
   - **パフォーマンスチューニング**
   - **API設計のベストプラクティス (ライブラリ/フレームワーク作成時)**
   - **主要なカンファレンス (WWDCなど) とそのキャッチアップ**
   - **コミュニティリソース (ブログ、ポッドキャスト、ニュースレター)**
   - **オープンソースライブラリの活用と貢献**
   - **iOS開発におけるアンチパターン**
