---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/android
---
## 1. [[Android開発入門 MOC]]
   - **Androidとは**
      - [[Android OSの定義と特徴 (Linuxカーネルベース、オープンソース)]]
      - [[Androidプラットフォームとエコシステム (Google Play Store)]]
      - [[Android開発者に必要なスキルセット]]
   - **Android開発の歴史と進化**
      - `[[Androidバージョン履歴 (Cupcakeから最新バージョンまで)]]` (APIレベルとの対応)
      - `[[JavaからKotlinファーストへの移行]]`
      - `[[UIフレームワークの変遷 (XML/ViewシステムからJetpack Composeへ)]]`
      - `[[主要な技術的変遷 (DalvikからARTへなど)]]`
   - **開発環境のセットアップ**
      - `[[Android Studioのインストールとセットアップ]]`
      - `[[Android SDK (Software Development Kit) のインストールと管理]]`
      - `[[JDK (Java Development Kit) の設定]]`
      - `[[Android Emulator (AVD - Android Virtual Device) の作成と利用]]`
      - `[[実機でのデバッグ設定 (USBデバッグ)]]`
   - **Androidプロジェクトの構造**
      - `[[Gradleビルドシステム]]` (詳細は後述)
      - `[[マニフェストファイル (AndroidManifest.xml)]]` (詳細は後述)
      - `[[ディレクトリ構造 (java, res, assetsなど)]]`
   - **Androidアプリのライフサイクル (概観)**
   - **Android開発の学習ロードマップ (例)**
   - **iOS開発との比較** (言語、ツール、デザイン思想、収益化など)

## 2. [[サーバーサイドプログラミング言語 (Android向け) MOC]]

### 2.1. [[Kotlin MOC]] (現代のAndroid開発推奨言語)
   - **Kotlinの基本**
      - [[Kotlinの概要と特徴 (静的型付け、Null安全、簡潔性、Javaとの100%相互運用性)]]
      - **[[基本構文]]**
         - `[[変数 (`val`, `var`)]]`
         - `[[基本的なデータ型]]`
         - `[[制御構文 (if, when, for, while)]]`
         - `[[関数 (fun)]]` (デフォルト引数、名前付き引数)
      - **[[Null安全性 (Null Safety)]]**
         - `[[Null許容型 (`?`)]]`
         - `[[セーフコール (`?.`)]]`
         - `[[エルビス演算子 (`?:`)]]`
         - `[[非Null表明 (`!!`)]]`
   - **Kotlinの主要機能**
      - `[[データクラス (Data Classes)]]`
      - `[[拡張関数と拡張プロパティ (Extension Functions/Properties)]]`
      - `[[高階関数とラムダ式 (Higher-Order Functions and Lambdas)]]`
      - `[[スコープ関数 (`let`, `run`, `with`, `apply`, `also`)]]`
      - `[[クラスと継承 (open, override)]]`
      - `[[インターフェース (Interface)]]`
      - `[[シールドクラス (Sealed Classes)]]` (状態表現に便利)
      - `[[オブジェクト (Objects) とコンパニオンオブジェクト (Companion Objects)]]`
      - `[[ジェネリクス (Generics)]]` (共変性 `out`, 反変性 `in`)
      - `[[デリゲーション (Delegation)]]`
   - **[[Kotlin Coroutines MOC]]** (非同期処理 - 詳細は後述)
   - **[[Flow MOC]]** (非同期データストリーム - 詳細は後述)
   - **[[Kotlin Multiplatform (KMP) MOC]]** (概要)

### 2.2. [[Java (Android向け) MOC]] (伝統的な言語)
   - **AndroidにおけるJava**
      - [[JavaのバージョンとAndroid APIレベルの関係]]
      - [[Java 8以降の言語機能のサポート状況 (desugaring)]]
   - **Javaの基本構文 (Kotlinとの対比)**
   - **Kotlinとの相互運用性**
      - [[JavaからKotlinを呼び出す]]
      - [[KotlinからJavaを呼び出す]]
   - **レガシーなJavaコードベースの保守とKotlinへの移行戦略**

## 3. [[UIフレームワーク MOC]]

### 3.1. [[Jetpack Compose MOC]] (モダンな宣言的UIツールキット)
   - **Jetpack Composeの基本**
      - [[Composeの思想 (宣言的UI, リアクティブ, Kotlinベース)]]
      - [[XML/Viewシステムとの違いと比較]]
   - **主要な概念**
      - **[[コンポーザブル関数 (`@Composable`)]]** (UIの構成単位)
      - **[[修飾子 (Modifiers)]]** (レイアウト、外観、インタラクションの指定)
      - **[[状態管理 (State Management) in Compose]]**
         - `[[`remember` と `mutableStateOf`]]`
         - `[[状態のホイスティング (State Hoisting)]]`
         - `[[ViewModelとの連携 (`viewModel()`)]]`
      - **[[再コンポーズ (Recomposition)]]**
         - [[再コンポーズの仕組みと最適化]]
      - **[[副作用の処理 (Side Effects)]]**
         - `[[`LaunchedEffect`, `rememberCoroutineScope`]]`
         - `[[`DisposableEffect`]]`
         - `[[`SideEffect`]]`
   - **基本的なコンポーザブル**
      - `[[Text, Button, TextField, Image, Icon]]`
      - `[[Checkbox, RadioButton, Switch, Slider]]`
   - **レイアウトコンポーザブル**
      - `[[Row, Column, Box]]`
      - `[[Spacer, Divider]]`
      - `[[LazyColumn, LazyRow, LazyVerticalGrid]]`
      - `[[ConstraintLayout (Compose版)]]`
      - `[[Scaffold, TopAppBar, BottomAppBar]]`
   - **テーマとスタイリング**
      - **[[Material Design 3 in Compose]]**
      - `[[Theme.kt (Color, Typography, Shape)]]`
      - `[[動的カラー (Dynamic Color)]]`
   - **ナビゲーション (Navigation)**
      - `[[Navigation for Compose]]` (`NavController`, `NavHost`)
   - **アニメーション (Animation)**
      - `[[`animate*AsState`, `updateTransition`, `AnimatedVisibility`など]]`
   - **テスト (Testing Compose)**
      - `[[Composeテストライブラリの利用]]`
      - `[[セマンティクスツリー]]`
   - **XML/Viewシステムとの相互運用性**
      - `[[ComposeView` (XML内でComposeを使用)]]`
      - `[[AndroidView` (Compose内でViewを使用)]]`

### 3.2. [[XMLレイアウトとViewシステム MOC]] (伝統的な命令的UIツールキット)
   - **XMLレイアウトの基本**
      - [[XMLによるUI構造の定義]]
      - [[ViewとViewGroup]]
   - **主要なレイアウト (Layouts)**
      - `[[LinearLayout]]`
      - `[[RelativeLayout]]`
      - `[[FrameLayout]]`
      - `[[ConstraintLayout]]` (推奨)
         - [[制約の作成と管理]]
      - `[[CoordinatorLayout]]`
   - **主要なウィジェット (Widgets)**
      - `[[TextView, Button, EditText, ImageView]]`
      - `[[CheckBox, RadioButton, Switch, ToggleButton]]`
      - `[[ProgressBar, SeekBar]]`
   - **[[RecyclerView MOC]]** (効率的なリスト表示)
      - `[[ViewHolderパターン]]`
      - `[[Adapter]]`
      - `[[LayoutManager]]`
      - `[[DiffUtil]]`
   - **スタイリングとテーマ (Styles and Themes)**
      - `[[`styles.xml` と `themes.xml`]]`
      - `[[Material Design Components for Android]]`
   - **データバインディング (Data Binding) / ビューバインディング (View Binding)**
   - **イベント処理 (リスナー)**
   - **フラグメント (Fragment) とそのライフサイクル**
   - **ナビゲーション (Navigation Component)** (XML/Viewシステム向け)

## 4. [[Androidアプリの基本構成要素 MOC]]
   - **[[Activity MOC]]**
      - [[Activityの役割 (単一画面の提供)]]
      - `[[Activityのライフサイクル (`onCreate`, `onStart`, `onResume`, `onPause`, `onStop`, `onDestroy`)]]`
      - `[[IntentによるActivity間の遷移]]`
   - **[[Service MOC]]**
      - [[Serviceの役割 (バックグラウンド処理)]]
      - `[[Started Service, Bound Service, Foreground Service]]`
      - `[[Serviceのライフサイクル]]`
   - **[[Broadcast Receiver MOC]]**
      - [[Broadcast Receiverの役割 (システムやアプリからのブロードキャストメッセージの受信)]]
      - `[[静的レシーバと動的レシーバ]]`
   - **[[Content Provider MOC]]**
      - [[Content Providerの役割 (アプリ間でデータを共有)]]
   - **[[Applicationクラス MOC]]** (アプリ全体の状態管理)
   - **[[AndroidManifest.xml MOC]]**
      - [[マニフェストファイルの役割と構成要素 (コンポーネント宣言、権限、ハードウェア/ソフトウェア要件など)]]

## 5. [[Android Jetpackライブラリ MOC]]
   - **Jetpackの概要 (高品質なアプリ開発を支援するライブラリ群)**
   - **[[Foundationコンポーネント MOC]]**
      - `[[AppCompat]]` (後方互換性)
      - `[[Android KTX]]` (Kotlin拡張機能)
      - `[[Multidex]]`
   - **[[Architectureコンポーネント MOC]]** (アプリの堅牢性、テスト容易性、保守性の向上)
      - `[[Data Binding / View Binding]]`
      - `[[Lifecycle-aware Components]]` (`LifecycleOwner`, `LifecycleObserver`)
      - `[[LiveData]]` (監視可能なデータホルダークラス)
      - `[[Navigation Component]]` (アプリ内ナビゲーションの簡素化)
      - `[[Paging 3 Library]]` (大規模データセットの段階的読み込み)
      - `[[Room Persistence Library]]` (SQLiteのORM - 詳細は後述)
      - `[[ViewModel]]` (UI関連データのライフサイクル対応保存)
      - `[[WorkManager]]` (バックグラウンドタスクのスケジューリング - 詳細は後述)
      - `[[StateFlow` と `SharedFlow]]` (LiveDataの代替としてのKotlin Coroutines Flow)
   - **[[Behaviorコンポーネント MOC]]**
      - `[[Download Manager]]`
      - `[[Permissions]]`
      - `[[Notifications]]`
      - `[[Sharing]]`
   - **[[UIコンポーネント MOC]]**
      - `[[Fragment]]` (再掲)
      - `[[Layout]]` (ConstraintLayoutなど)
      - `[[Palette]]`
      - `[[Animation & Transition]]`

## 6. [[Androidアプリのアーキテクチャ MOC]]
   - **[[Google推奨のアプリ アーキテクチャ MOC]]**
      - **[[UIレイヤー (UI Layer)]]** (Activity/Fragment + ViewModel, UI状態管理)
      - **[[ドメインレイヤー (Domain Layer)]]** (オプション、ビジネスロジック)
         - [[ユースケース (Use Cases / Interactors)]]
      - **[[データレイヤー (Data Layer)]]** (リポジトリ、データソース)
         - **[[リポジトリパターン (Repository Pattern)]]**
         - `[[データソース (ネットワーク、ローカルDB)]]`
      - `[[単方向データフロー (Unidirectional Data Flow - UDF)]]`
   - **[[MVVM (Model-View-ViewModel) アーキテクチャ MOC]]** (Androidでの主流パターン)
   - **[[MVI (Model-View-Intent) アーキテクチャ MOC]]**
   - **[[Clean ArchitectureのAndroidへの適用 MOC]]**
   - **[[依存性の注入 (Dependency Injection - DI) MOC]]**
      - `[[なぜDIが必要か]]`
      - `[[Hilt (Android Jetpack推奨DIライブラリ)]]`
      - `[[Dagger 2]]` (高機能、高学習コスト)
      - `[[Koin]]` (純粋Kotlin製、サービスロケータに近い)

## 7. [[データ管理と永続化 MOC]]
   - **[[Room Persistence Library MOC]]**
      - [[Roomの概要 (SQLiteの抽象化レイヤー)]]
      - `[[エンティティ (Entity - `@Entity`)]]`
      - `[[DAO (Data Access Object - `@Dao`)]]`
      - `[[データベースクラス (`@Database`)]]`
      - `[[型コンバータ (Type Converters)]]`
      - `[[Coroutines/Flow/RxJavaとの連携]]`
      - `[[データベースマイグレーション]]`
   - **[[DataStore MOC]]** (SharedPreferencesの後継)
      - `[[Preferences DataStore` (Key-Value)]]`
      - `[[Proto DataStore` (型付けされたオブジェクト)]]`
      - `[[非同期API (`Flow`)]]`
   - **[[SharedPreferences MOC]]** (シンプルなKey-Value保存、非推奨となりつつある)
   - **[[ファイルシステムアクセス MOC]]**
      - `[[内部ストレージと外部ストレージ]]`
      - `[[Scoped Storage]]` (Android 10以降)
   - **[[BaaS (Backend as a Service) の活用]]**
      - `[[Firebase Realtime Database / Cloud Firestore]]`
      - `[[Firebase Storage]]`

## 8. [[ネットワーク通信 MOC]]
   - **[[Retrofit MOC]]** (型安全なHTTPクライアント)
      - [[インターフェースとアノテーションによるAPI定義]]
      - [[コンバータ (JSONなど)]]
      - [[Coroutines/RxJavaとの連携]]
   - **[[OkHttp MOC]]** (HTTPクライアント実装、Retrofitの基盤)
      - [[インターセプタ (Interceptors)]]
   - **[[Ktor Client MOC]]** (Kotlin Multiplatform対応のHTTPクライアント)
   - **JSONパーシングライブラリ**
      - `[[Kotlinx.serialization]]` (Kotlin公式)
      - `[[Moshi]]`
      - `[[Gson]]` (レガシーだが広く利用)
   - **ネットワークのベストプラクティス**
      - [[オフライン対応]]
      - [[ネットワーク状態の監視]]
      - [[エラーハンドリング]]

## 9. [[非同期処理 MOC]]

### 9.1. [[Kotlin Coroutines MOC]] (現代の標準)
   - [[コルーチンの概念 (軽量なスレッド)]]
   - `[[中断可能関数 (`suspend`)]]`
   - **[[コルーチンビルダー (`launch`, `async`)]]**
   - **[[コルーチンスコープ (`CoroutineScope`, `viewModelScope`, `lifecycleScope`)]]**
   - **[[ディスパッチャ (`Dispatchers.Main`, `Dispatchers.IO`, `Dispatchers.Default`)]]**
   - `[[Job` と `Deferred]]`
   - [[構造化された並行性 (Structured Concurrency)]]
   - [[例外処理 (try-catch, CoroutineExceptionHandler)]]

### 9.2. [[Flow MOC]] (Coroutinesベースの非同期ストリーム)
   - [[Flowの概念 (Cold Stream)]]
   - `[[Flowビルダー (`flow`, `flowOf`など)]]`
   - `[[中間オペレータ (`map`, `filter`, `onEach`など)]]`
   - `[[終端オペレータ (`collect`, `first`, `toList`など)]]`
   - **[[StateFlow と SharedFlow]]** (Hot Stream、UI状態管理向け)
   - `[[FlowとLiveDataの比較]]`

### 9.3. [[RxJava / RxKotlin MOC]] (リアクティブプログラミング)
   - [[Rxの基本概念 (Observable, Observer, Operator, Scheduler)]]
   - [[Coroutines/Flowとの比較]]
   - [[レガシーコードでの利用]]

## 10. [[Androidテスト MOC]]
   - **[[テストの基本とテストピラミッド]]** (再掲・Android文脈)
   - **[[ローカルテスト (Local Tests / Unit Tests)]]** (JVM上で実行)
      - `[[JUnit 4/5]]`
      - `[[Mockito / MockK` (モックライブラリ)]]`
      - `[[Robolectric]]` (Androidフレームワークをシャドウイング)
   - **[[インストルメンテーションテスト (Instrumented Tests)]]** (実機/エミュレータ上で実行)
      - `[[UIテスト (UI Tests)]]`
         - `[[Espresso]]` (Viewシステム向け)
         - `[[UI Automator]]` (アプリ間テスト)
         - `[[Composeテストライブラリ]]`
      - `[[インテグレーションテスト (Room, DataStoreなど)]]`
      - `[[Android Test Orchestrator]]`
   - **テストダブル (Test Doubles) の活用** (再掲)
   - **テストのアーキテクチャ** (テスト用DIモジュールなど)
   - **CI/CDパイプラインでのテスト実行**

## 11. [[アプリのリリースと運用 MOC]]

### 11.1. [[Google Play Console MOC]]
   - [[アプリの登録とストア掲載情報の管理]]
   - `[[テストトラック (内部テスト、クローズドテスト、オープンテスト)]]`
   - [[段階的な公開 (Staged Rollouts)]]
   - [[ユーザーレビューとフィードバックの管理]]
   - [[統計情報とアナリティクス]]
   - [[Android Vitals (クラッシュ、ANR)]]

### 11.2. [[ビルドと署名 MOC]]
   - **[[Gradleビルドシステム MOC]]**
      - `[[`build.gradle` ファイル (Groovy/Kotlin DSL)]]`
      - `[[依存関係の管理 (`dependencies`)]]`
      - `[[ビルドバリアント (Build Variants)]]` (`buildTypes` と `productFlavors`)
   - **[[アプリの署名 (App Signing)]]**
      - `[[キーストア (Keystore)]]`
      - `[[Google Play App Signing]]`
   - **[[Android App Bundle (.aab) MOC]]**
      - `[[Dynamic Delivery]]`
      - `[[APKとの違い]]`
   - **[[ProGuard / R8 によるコードの難読化と圧縮]]**

### 11.3. [[プッシュ通知とアプリ内課金 MOC]]
   - **[[Firebase Cloud Messaging (FCM)]]** (プッシュ通知)
   - **[[Google Play Billing Library]]** (アプリ内課金、定期購入)

## 12. [[主要なAndroidフレームワークとAPI MOC]]
   - **[[権限管理 (Permissions) MOC]]** (通常、危険、署名レベル。実行時権限リクエスト)
   - **[[バックグラウンド処理 MOC]]**
      - `[[WorkManager]]` (遅延可能で保証されたバックグラウンドタスク)
      - `[[Foreground Services]]`
   - **[[位置情報サービス (Location Services) MOC]]** (`FusedLocationProviderClient`)
   - **[[カメラ MOC]]** (`[[CameraX]]` (Jetpack), `Camera2 API`)
   - **[[センサーフレームワーク (Sensors Framework) MOC]]**
   - **[[通知 (Notifications) MOC]]** (通知チャネル、スタイル)
   - **[[マルチメディア MOC]]** (`[[ExoPlayer]]` (推奨), `MediaPlayer`)
   - **[[Android for Cars (Android Auto, Android Automotive OS)]]** (概要)
   - **[[Wear OS]]** (概要)
   - **[[Android TV]]** (概要)
   - **[[Google Play Services]]**

## 13. [[パフォーマンスとセキュリティ MOC]]

### 13.1. [[Androidパフォーマンス最適化 MOC]]
   - **[[アプリの起動時間短縮]]** (コールドスタート、ウォームスタート、ホットスタート)
   - **[[UIレンダリングパフォーマンス]]** (オーバードローの削減、レイアウトの最適化、Profile GPU Rendering)
   - **[[メモリ管理と最適化]]** (メモリリークの検出 - LeakCanary, Android Studio Profiler)
   - **[[バッテリー消費の最適化]]** (Dozeモード、App Standby、バックグラウンド実行の制限)
   - **[[ビルドパフォーマンスの改善]]** (Gradleの最適化)
   - **[[Android Studio Profilerの活用 (CPU, Memory, Network, Energy)]]**

### 13.2. [[Androidセキュリティ MOC]]
   - **[[アプリの権限 (Permissions)]]** (最小権限の原則)
   - **[[安全なデータストレージ]]** (暗号化、Keychain/Keystore)
   - **[[セキュアなネットワーク通信]]** (HTTPS, ネットワークセキュリティ構成)
   - **[[入力検証とインジェクション対策]]** (SQLi, Webviewの脆弱性)
   - **[[コードの難読化 (Obfuscation)]]**
   - **[[セキュアなIPC (Intent, Broadcast Receiver)]]**
   - **[[生体認証 (BiometricPrompt)]]**
   - **[[静的/動的セキュリティテスト]]**

## 14. [[Android開発のベストプラクティスとコミュニティ MOC]]
   - **[[Google公式の設計ガイドライン]]** (Material Designなど)
   - **[[クリーンアーキテクチャの実践]]**
   - **[[テスト可能なコードの書き方]]**
   - **[[マルチモジュールアーキテクチャの採用]]**
   - **[[依存関係の管理と最新化]]**
   - **[[Android開発におけるアンチパターン]]**
   - **主要なカンファレンス (Google I/O, DroidKaigiなど) とそのキャッチアップ**
   - **コミュニティリソース (ブログ、ポッドキャスト、ニュースレター)**
   - **オープンソースライブラリの活用と貢献**
