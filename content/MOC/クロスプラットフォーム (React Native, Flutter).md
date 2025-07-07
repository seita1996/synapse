---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/cross-platform
---
## 1. [[クロスプラットフォーム開発入門 MOC]]
   - **クロスプラットフォーム開発とは**
      - [[クロスプラットフォーム開発の定義 (単一のコードベースから複数のプラットフォーム向けアプリを構築)]]
      - [[クロスプラットフォーム開発の目的 (開発効率、コスト削減、コード共通化)]]
   - **開発アプローチの比較**
      - **[[ネイティブ開発 vs. クロスプラットフォーム開発 vs. Webアプリ/PWA]]**
         - `[[パフォーマンスの比較]]`
         - `[[開発コストと速度の比較]]`
         - `[[UI/UXの一貫性とプラットフォーム固有性の比較]]`
         - `[[ネイティブ機能へのアクセス性の比較]]`
         - `[[保守性と将来性の比較]]`
   - **クロスプラットフォーム技術の分類**
      - `[[Web技術ベース (ハイブリッドアプリ - Ionic, Capacitor)]]`
      - `[[ネイティブブリッジ型 (React Native)]]`
      - `[[独自レンダリングエンジン型 (Flutter)]]`
      - `[[ビジネスロジック共有型 (Kotlin Multiplatform, .NET MAUI)]]`
   - **クロスプラットフォーム開発の利点と課題**
      - `[[利点: コードの再利用、開発チームの縮小、迅速な市場投入]]`
      - `[[課題: パフォーマンスのボトルネック、プラットフォーム固有機能への対応、OSアップデートへの追従、抽象化レイヤーのバグ]]`

## 2. [[React Native MOC]]

### 2.1. [[React Native入門 MOC]]
   - **React Nativeとは**
      - [[React Nativeの定義 (Reactの設計思想をネイティブアプリ開発にもたらすフレームワーク)]]
      - [[React Nativeの思想 ("Learn once, write anywhere")]]
   - **コアコンセプトとアーキテクチャ**
      - `[[Reactの概念 (コンポーネント, JSX, State, Props)]]` (再掲・RN文脈)
      - **[[React Nativeブリッジ (Bridge) アーキテクチャ]]** (伝統的なアーキテクチャ)
         - `[[JavaScriptスレッドとネイティブスレッド間の非同期通信]]`
         - `[[ブリッジの仕組みとパフォーマンス上のボトルネック]]`
      - **[[JSI (JavaScript Interface) と新しいアーキテクチャ (TurboModules, Fabric)]]**
         - `[[Fabricレンダラー]]`
         - `[[TurboModules]]`
   - **開発環境のセットアップ**
      - `[[React Native CLI vs. Expo]]`
      - `[[Node.js, Watchman, JDK, Android Studio, Xcodeのセットアップ]]`
      - `[[シミュレータ/エミュレータと実機での実行]]`

### 2.2. [[React Nativeの基本コンポーネントとAPI MOC]]
   - **基本的なUIコンポーネント**
      - `[[`View`, `Text`, `Image`, `TextInput`, `ScrollView`, `StyleSheet`]]`
   - **インタラクションコンポーネント**
      - `[[`Button`, `TouchableHighlight`, `TouchableOpacity`, `Pressable`]]`
   - **リストビュー**
      - `[[`FlatList`]]` (高性能リスト)
      - `[[`SectionList`]]` (セクション付きリスト)
   - **プラットフォーム固有のコンポーネントとAPI**
      - `[[`Platform` モジュール]]`
      - `[[プラットフォーム固有のファイル拡張子 (`.ios.js`, `.android.js`)]]`
   - **その他のコアAPI**
      - `[[Alert, Dimensions, Animated, PanResponder]]`

### 2.3. [[React Nativeにおけるスタイリング MOC]]
   - **[[StyleSheet API]]**
      - `[[CSS in JS のアプローチ]]`
      - `[[Flexboxによるレイアウト]]` (Web版との違い)
      - `[[プラットフォームごとのスタイル適用]]`
   - **スタイリングライブラリ**
      - `[[Styled Components for React Native]]`
      - `[[Restyle, Tamaguiなどのライブラリ]]`
      - `[[Tailwind CSSライクなアプローチ (NativeWind)]]`

### 2.4. [[React Nativeにおけるナビゲーション MOC]]
   - **ナビゲーションの概念** (スタック、タブ、ドロワー)
   - **主要なナビゲーションライブラリ**
      - **[[React Navigation MOC]]** (コミュニティ標準)
         - `[[Stack Navigator, Tab Navigator, Drawer Navigator]]`
         - `[[ナビゲータのネスト]]`
         - `[[パラメータの受け渡し]]`
         - `[[ヘッダのカスタマイズ]]`
      - `[[React Native Navigation (Wix)]]` (よりネイティブに近いパフォーマンス)

### 2.5. [[React Nativeにおける状態管理 MOC]]
   - **Reactの基本状態管理** (再掲・RN文脈)
      - `[[`useState`, `useReducer`, `useContext`]]`
   - **グローバル状態管理ライブラリ**
      - `[[Redux / Redux Toolkit]]` (再掲)
      - `[[Zustand]]`
      - `[[Jotai, Recoil]]`
   - **データフェッチと状態管理**
      - `[[React Query / TanStack Query]]`
      - `[[Apollo Client for GraphQL]]`
   - **永続化ストレージとの連携**
      - `[[AsyncStorage]]`
      - `[[MMKV, WatermelonDBなどのライブラリ]]`

### 2.6. [[React Nativeにおけるネイティブ連携 MOC]]
   - **ネイティブモジュール (Native Modules)**
      - `[[JavaScriptからネイティブコード (Java/Kotlin, Objective-C/Swift) を呼び出す]]`
      - `[[ネイティブモジュールの作成手順 (Android, iOS)]]`
   - **ネイティブUIコンポーネント (Native UI Components)**
      - `[[ネイティブのUIコンポーネントをReact Nativeコンポーネントとしてラップする]]`
      - `[[ネイティブUIコンポーネントの作成手順 (Android, iOS)]]`
   - **TurboModules と Fabric のためのネイティブコード** (新アーキテクチャ)
   - **既存のネイティブアプリへのReact Nativeの統合**

### 2.7. [[React Nativeのテスト MOC]]
   - **[[Jestによるユニットテストとスナップショットテスト]]**
   - **[[React Native Testing Libraryによるコンポーネントテスト]]**
   - **[[E2Eテスト (Detox, Appium)]]`**
   - **モックライブラリの活用**

### 2.8. [[React Nativeのパフォーマンス最適化 MOC]]
   - `[[不要な再レンダリングの防止 (`React.memo`, `useCallback`, `useMemo`)]]`
   - `[[ブリッジの負荷軽減]]`
   - `[[画像最適化 (`react-native-fast-image`)]]`
   - `[[リストパフォーマンス (`FlatList`の最適化)]]`
   - `[[Hermesエンジンの利用]]`
   - `[[パフォーマンスプロファイリング (Flipper, React DevTools Profiler)]]`

### 2.9. [[React Nativeのデプロイとリリース MOC]]
   - `[[プラットフォームごとのビルドと署名]]`
   - **[[OTA (Over-the-Air) アップデート]]**
      - `[[CodePush (App Center), Expo Updates]]`
   - `[[CI/CDパイプラインの構築 (Fastlane, GitHub Actions)]]`

### 2.10. [[Expo MOC]]
   - **Expoとは** (React Nativeアプリを容易に開発・ビルド・デプロイするためのフレームワークとプラットフォーム)
   - **Expo Go (開発クライアント)**
   - **Managed Workflow vs. Bare Workflow**
   - **Expo SDK (ネイティブAPIへのアクセス)**
   - **EAS (Expo Application Services)** (ビルド、アップデート、サブミット)
   - **Expoの利点と制約**

## 3. [[Flutter MOC]]

### 3.1. [[Flutter入門 MOC]]
   - **Flutterとは**
      - [[Flutterの定義 (Google製のUIツールキット、単一コードベースからモバイル、Web、デスクトップアプリをビルド)]]
      - [[Flutterの思想 ("Everything is a widget", 独自のレンダリングエンジン)]]
   - **[[Dartプログラミング言語 MOC]]**
      - `[[Dartの概要と特徴 (クライアント最適化、JIT/AOTコンパイル、型安全性)]]`
      - `[[基本的な構文 (変数、型、関数、制御構文)]]`
      - `[[Null Safety]]`
      - `[[クラスとMixins]]`
      - `[[非同期処理 (`Future`, `Stream`, `async/await`)]]`
   - **コアコンセプトとアーキテクチャ**
      - `[[ウィジェットツリー (Widget Tree)]]`
      - `[[StatelessWidget vs. StatefulWidget]]`
      - `[[Flutterエンジン (Skia, Dart VM)]]`
      - `[[宣言的UIとリアクティブプログラミング]]`
   - **開発環境のセットアップ**
      - `[[Flutter SDKのインストール]]`
      - `[[Android Studio / VS Code の設定と拡張機能]]`
      - `[[`flutter doctor`]]`
      - `[[シミュレータ/エミュレータと実機での実行]]`
      - `[[ホットリロード (Hot Reload) とホットリスタート (Hot Restart)]]`

### 3.2. [[Flutterの基本ウィジェット MOC]]
   - **基本的なUIウィジェット**
      - `[[`Text`, `Icon`, `Image`, `Button`系ウィジェット]]`
      - `[[`TextField`, `Checkbox`, `Radio`, `Switch`, `Slider`]]`
   - **レイアウトウィジェット**
      - `[[`Container`, `Padding`, `Center`, `Align`, `SizedBox`]]`
      - `[[`Row`, `Column`]]` (Flexboxライク)
      - `[[`Stack`, `Positioned`]]`
      - `[[`Expanded`, `Flexible`]]`
      - `[[`Wrap`, `Chip`]]`
   - **リストビュー**
      - `[[`ListView`]]`
      - `[[`GridView`]]`
      - `[[`ListTile`]]`
   - **マテリアルデザイン (Material Design) とクパチーノ (Cupertino) ウィジェット**
      - `[[`Scaffold`, `AppBar`, `FloatingActionButton`]]` (Material)
      - `[[`CupertinoPageScaffold`, `CupertinoNavigationBar`]]` (iOS風)
      - [[プラットフォームに応じたウィジェットの出し分け]]

### 3.3. [[Flutterにおける状態管理 MOC]]
   - **状態管理の概要**
      - [[Ephemeral State vs. App State]]
   - **基本的な状態管理**
      - `[[`setState()` (`StatefulWidget`内)]]`
      - `[[InheritedWidget]]`
   - **主要な状態管理パッケージ**
      - **[[Provider MOC]]** (シンプル、DIコンテナとしても)
      - **[[Riverpod MOC]]** (Providerの進化形、コンパイルセーフ)
      - **[[BLoC (Business Logic Component) MOC]]** (イベント、ステート、ストリームベース)
      - **[[MobX MOC]]** (リアクティブ状態管理)
      - `[[GetX]]` (多機能ライブラリ)
      - [[状態管理ソリューションの選択]]

### 3.4. [[Flutterにおけるナビゲーションとルーティング MOC]]
   - **[[Navigator 1.0 (命令的API) MOC]]**
      - `[[`Navigator.push`, `Navigator.pop`]]`
      - `[[名前付きルート (Named Routes)]]`
   - **[[Navigator 2.0 (宣言的API) MOC]]**
      - `[[`Router`, `Page`, `RouteInformationParser`, `RouterDelegate`]]`
      - [[Web対応とディープリンクの強化]]
   - **主要なナビゲーションパッケージ**
      - `[[`go_router`]]` (宣言的、URLベース)
      - `[[`auto_route`]]` (コード生成ベース)

### 3.5. [[Flutterにおける非同期処理 MOC]]
   - **[[`Future`, `async`, `await`]]** (再掲・Dart/Flutter文脈)
   - **[[`Stream`]]** (非同期イベントシーケンス)
   - **[[`Isolate`]]** (並列処理、イベントループの分離)
   - **[[`Compute`]]** (重い処理を別Isolateで実行するヘルパー)

### 3.6. [[Flutterにおけるネイティブ連携 MOC]]
   - **[[プラットフォームチャネル (Platform Channels)]]**
      - `[[`MethodChannel`]]` (メソッド呼び出し)
      - `[[`EventChannel`]]` (イベントストリーム)
      - `[[`BasicMessageChannel`]]`
      - [[データ型とコーデック]]
   - **[[プラットフォームビュー (Platform Views)]]**
      - [[ネイティブUIコンポーネントをFlutterウィジェットツリーに埋め込む]]
   - **[[FFI (Foreign Function Interface)]]**
      - [[C/C++などのネイティブライブラリを直接呼び出す]]
   - **[[Pigeon]]** (型安全なプラットフォームチャネルコード生成ツール)

### 3.7. [[Flutterのテスト MOC]]
   - **テストの種類**
      - **[[ユニットテスト]]** (ロジックのテスト)
      - **[[ウィジェットテスト]]** (単一ウィジェットのテスト)
      - **[[インテグレーションテスト]]** (アプリ全体のテスト)
   - **テストパッケージ (`flutter_test`, `integration_test`)**
   - **モックライブラリ (`mockito`)**
   - **テストの実行とカバレッジ**

### 3.8. [[Flutterのパフォーマンス最適化 MOC]]
   - `[[不要な`setState`呼び出しとビルドの最小化]]`
   - `[[`const`ウィジェットの活用]]`
   - `[[リビルド範囲の特定 (DevTools)]]`
   - `[[レイアウトと描画の最適化]]`
   - `[[画像の最適化]]`
   - `[[パフォーマンスプロファイリング (Flutter DevTools)]]` (CPU, メモリ, ネットワーク, パフォーマンス)

### 3.9. [[Flutterのデプロイとリリース MOC]]
   - `[[ビルドモード (`debug`, `profile`, `release`)]]`
   - `[[Android / iOS 向けのビルドと署名]]`
   - `[[CI/CDパイプラインの構築 (Codemagic, Fastlane, GitHub Actions)]]`
   - **[[Flutter for Web, Desktop, Embedded]]** (概要)

### 3.10. [[Flutterエコシステムとパッケージ MOC]]
   - **[[Pub.dev (パッケージリポジトリ)]]**
   - **主要なパッケージカテゴリ**
      - `[[状態管理 (Provider, Riverpod, BLoCなど)]]`
      - `[[ネットワーク (`http`, `dio`)]]`
      - `[[データベース (`sqflite`, `hive`, `isar`)]]`
      - `[[DI (`get_it`)]]`
      - `[[アニメーション (`lottie`)]]`
      - `[[Firebase連携]]`

## 4. [[主要クロスプラットフォーム技術の比較 MOC]]

### 4.1. [[React Native vs. Flutter MOC]]
   - **言語**: `[[JavaScript/TypeScript vs. Dart]]`
   - **UIパラダイム**: `[[Reactの概念 vs. ウィジェットベース]]`
   - **アーキテクチャ**: `[[ネイティブブリッジ vs. 独自レンダリングエンジン (Skia)]]`
   - **パフォーマンス**: `[[ブリッジのオーバーヘッド vs. ネイティブコンパイルによる速度]]`
   - **UIの柔軟性と一貫性**: `[[ネイティブUIコンポーネント vs. カスタマイズ可能な独自ウィジェット]]`
   - **開発者体験**: `[[エコシステムとコミュニティの規模 vs. 公式ツールとホットリロードの速度]]`
   - **ネイティブ連携**: `[[各フレームワークのネイティブ連携方法の比較]]`
   - **成熟度と採用実績**: `[[React Nativeの先行 vs. Flutterの急速な成長]]`
   - **どちらをいつ選ぶべきか**

### 4.2. [[クロスプラットフォーム vs. ネイティブ開発 (再訪・深掘り) MOC]]
   - `[[パフォーマンスのトレードオフの具体例]]`
   - `[[OSアップデートへの追従性]]`
   - `[[長期的なメンテナンスコストの再評価]]`
   - `[[チーム構成とスキルセットへの影響]]`
   - `[[プロジェクト要件に応じた最適な選択]]`

## 5. [[その他のクロスプラットフォームソリューション MOC]] (概要)
   - **[[Kotlin Multiplatform (KMP) / Compose Multiplatform MOC]]**
      - `[[ビジネスロジックと(オプションで)UIの共有]]`
      - `[[ネイティブUIを維持するアプローチ]]`
   - **[[.NET MAUI (旧Xamarin) MOC]]**
      - `[[C#と.NETによるクロスプラットフォーム開発]]`
   - **[[Ionic / Capacitor MOC]]**
      - `[[Web技術 (Angular/React/Vue) を用いたハイブリッドアプリ開発]]`
      - `[[WebViewベースのアプローチ]]`
   - **[[(オプション) NativeScript]]**
   - **[[(オプション) PWA (Progressive Web Apps)]]** (クロスプラットフォーム戦略の一環として)

## 6. [[クロスプラットフォーム開発の共通トピックとベストプラクティス MOC]]
   - **UI/UXのプラットフォーム差異への対応戦略**
      - `[[単一デザイン vs. プラットフォーム適応デザイン]]`
   - **コード共有戦略**
      - `[[どの部分を共通化し、どの部分をプラットフォーム固有にするか]]`
   - **ネイティブモジュール連携の設計パターン**
      - `[[抽象インターフェースの定義]]`
   - **CI/CDパイプラインの構築**
      - `[[複数プラットフォーム向けのビルドとデプロイの自動化]]`
      - `[[Fastlaneの活用]]`
   - **クロスプラットフォーム開発におけるアンチパターン**
      - `[[プラットフォームの特性を完全に無視する]]`
      - `[[パフォーマンス問題を軽視する]]`
      - `[[ネイティブ連携を避けるために機能を妥協する]]`
      - `[[安易な「一度書けばどこでも動く」という考え]]`
   - **クロスプラットフォーム技術の将来動向**
