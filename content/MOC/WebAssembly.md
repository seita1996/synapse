---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/webassembly
---
## 1. [[WebAssembly入門 MOC]]
   - **WebAssemblyとは**
      - [[WebAssemblyの定義 (モダンWebブラウザで実行可能な低レベルなバイナリ命令フォーマット)]]
      - [[Wasmはプログラミング言語ではなく、コンパイルターゲットである]]
      - [[Wasmの歴史的背景 (asm.jsからの進化、主要ブラウザベンダーの協力)]]
   - **なぜWebAssemblyが必要か**
      - `[[JavaScriptのパフォーマンス上の限界 (動的型付け、JITコンパイルのオーバーヘッド)]]`
      - `[[既存のC/C++/RustなどのコードベースのWebへの移植]]`
      - `[[Web上でのCPU負荷の高い処理 (ゲーム、動画編集、科学技術計算) の実現]]`
      - `[[予測可能なパフォーマンスの提供]]`
   - **WebAssemblyの設計目標**
      - `[[高速性 (Fast) - ネイティブに近い実行速度]]`
      - `[[効率性 (Efficient) - コンパクトなバイナリフォーマット]]`
      - `[[安全性 (Safe) - サンドボックス化された実行環境]]`
      - `[[移植性 (Portable) - プラットフォーム非依存]]`
      - `[[デバッグ可能性 (Debuggable)]]`
      - `[[JavaScriptとの協調性 (Composable)]]`
   - **WebAssemblyとJavaScriptの関係**
      - [[WasmとJSは競合ではなく、補完関係にある]]
      - [[役割分担 (Wasm: 計算集約タスク, JS: UI操作/DOMアクセス/API連携)]]
      - [[JavaScriptからWasmを呼び出し、WasmからJavaScriptを呼び出す]]
   - **WebAssemblyの主なユースケース (概観)**
      - [[3Dグラフィックスとゲーム (Unity, Unreal Engine)]]
      - [[動画・音声処理 (エンコード/デコード、エフェクト)]]
      - [[科学技術計算とデータ可視化]]
      - [[デスクトップアプリケーションのWeb移植 (AutoCAD, Figma)]]
      - [[ブラウザ外での利用 (サーバーサイド、エッジコンピューティング)]]

## 2. [[WebAssemblyのコア技術 MOC]]

### 2.1. [[WebAssemblyモジュール (Wasm Module) MOC]]
   - [[Wasmモジュールの定義 (コンパイル済みのWasmコードの単位)]]
   - **モジュールの構造**
      - `[[セクション (Sections)]]` (Type, Import, Function, Table, Memory, Global, Export, Start, Element, Code, Dataなど)
      - **[[インポート (Imports)]]** (ホスト環境(JSなど)から提供される機能)
      - **[[エクスポート (Exports)]]** (ホスト環境に公開する機能 - 関数、メモリ、テーブル、グローバル変数)
      - [[関数 (Functions)]]
      - [[メモリ (Memory)]]
      - [[テーブル (Tables)]]
      - [[グローバル (Globals)]]
   - [[モジュールの検証 (Validation)]]
   - [[モジュールのインスタンス化 (Instantiation)]]

### 2.2. [[WebAssemblyのフォーマット MOC]]
   - **[[WebAssemblyバイナリフォーマット (.wasm) MOC]]**
      - `[[バイナリフォーマットの構造 (マジックナンバー, バージョン, セクション)]]`
      - `[[コンパクトさと高速なデコード]]`
      - `[[LEB128エンコーディング]]`
   - **[[WebAssemblyテキストフォーマット (.wat) MOC]]**
      - `[[WATの定義 (人間が読めるS式形式のテキスト表現)]]`
      - `[[WATの構文 (`module`, `func`, `import`, `export`, `memory`, `table`など)]]`
      - `[[WATの役割 (デバッグ、学習、手書きでの最適化)]]`
      - `[[WATとWasm間の相互変換ツール (wat2wasm, wasm2wat)]]`

### 2.3. [[WebAssemblyの実行モデル MOC]]
   - **[[スタックベース仮想マシン (Stack-based Virtual Machine)]]**
      - [[Wasmがスタックマシンであることの利点 (コードのコンパクトさ、実装の単純さ)]]
      - `[[オペランドスタックと命令の動作]]`
   - **[[命令セットアーキテクチャ (ISA)]]**
      - `[[制御フロー命令 (`block`, `loop`, `if`, `br`, `br_if`, `br_table`, `return`, `call`, `call_indirect`)]]`
      - `[[数値演算命令 (加減乗除、ビット演算、比較など)]]`
      - `[[メモリ操作命令 (`load`, `store`)]]`
      - `[[パラメータ操作命令]]`
   - **関数の呼び出し規約** (引数の渡し方、戻り値の返し方)

### 2.4. [[WebAssemblyのメモリモデル MOC]]
   - **[[線形メモリ (Linear Memory)]]**
      - [[線形メモリの定義 (バイトの連続配列、サンドボックス化されたメモリ空間)]]
      - [[ページ単位での管理 (1ページ = 64KiB)]]
      - [[メモリの初期サイズと最大サイズ]]
      - [[`memory.grow` 命令による動的なメモリ拡張]]
   - **JavaScriptとのメモリ共有**
      - `[[ArrayBuffer` と `SharedArrayBuffer`]]`
      - [[JavaScriptからWasmメモリの読み書き]]
      - [[WasmメモリとJavaScriptのヒープは分離されている]]
   - **ポインタの概念** (Wasmにおけるポインタは線形メモリへのインデックス)
   - **スタックと線形メモリの関係** (Wasmの実行スタックは線形メモリとは別)

### 2.5. [[WebAssemblyのテーブルと関数参照 MOC]]
   - **[[テーブル (Tables)]]**
      - [[テーブルの定義と役割 (不透明な値(特に関数参照)の配列)]]
      - [[`anyfunc` / `funcref` 型]]
      - [[テーブルを通じた間接的な関数呼び出し (`call_indirect`)]]
   - **テーブルの利用例**
      - `[[関数ポインタの実装 (C/C++などから)]]`
      - `[[動的リンクの実現]]`
      - `[[JSからWasmに渡した関数の管理]]`

## 3. [[WebAssemblyの開発と利用 MOC]]

### 3.1. [[JavaScriptとWebAssemblyの連携 (JS/Wasm Interoperability) MOC]]
   - **Wasmモジュールのロードとインスタンス化**
      - `[[WebAssembly JavaScript API]]`
      - `[[`WebAssembly.instantiateStreaming()` (推奨)]]`
      - `[[`WebAssembly.instantiate()`]]`
      - `[[`WebAssembly.compileStreaming()` / `compile()` と `WebAssembly.instantiate()` の組み合わせ]]`
      - `[[インポートオブジェクトの提供]]`
   - **Wasm関数の呼び出し**
      - `[[エクスポートされた関数をJavaScriptから呼び出す]]`
   - **JavaScript関数の呼び出し**
      - `[[インポートオブジェクトを通じてJavaScript関数をWasmから呼び出す]]`
   - **データの受け渡し**
      - `[[数値型 (i32, i64, f32, f64) の直接的な受け渡し]]`
      - `[[複雑なデータ型 (文字列、配列、オブジェクト) の受け渡し]]`
         - `[[線形メモリを介したデータ共有]]`
         - `[[文字列のエンコード/デコード (UTF-8, UTF-16)]]`
         - `[[データのシリアライズ/デシリアライズ (JSONなど)]]`
   - **[[Wasm-bindgen / Glue Code (グルーコード) の役割]]**
      - [[JSとWasm間のデータ型変換や関数呼び出しを容易にするライブラリ]]

### 3.2. [[C/C++からWebAssemblyへのコンパイル MOC]]
   - **[[Emscriptenツールチェイン MOC]]**
      - [[Emscriptenの概要と役割 (LLVMベースのC/C++からWasmへのコンパイラ)]]
      - `[[Emscriptenのインストールと設定]]`
      - **[[コンパイルコマンド (`emcc`)]]**
         - `[[基本的なコンパイルオプション]]`
         - `[[出力形式 (`.js` + `.wasm`, スタンドアロンWasm)]]`
         - `[[最適化レベル (`-O1`, `-O2`, `-O3`)]]`
      - **[[Emscriptenが提供する機能]]**
         - `[[ファイルシステムエミュレーション (MEMFS, NODEFS)]]`
         - `[[C標準ライブラリ (libc) のサポート]]`
         - `[[C++標準ライブラリ (libc++) のサポート]]`
         - `[[SDL, OpenGL (WebGL経由) などのライブラリサポート]]`
         - `[[Embind` と `WebIDL Binder` (C++とJSの連携)]]`
      - `[[EmscriptenにおけるJSとC/C++の相互呼び出し]]` (`emscripten_run_script`, `EM_JS`マクロ)
   - `[[既存のC/C++プロジェクトのWasmへの移植]]`

### 3.3. [[RustからWebAssemblyへのコンパイル MOC]]
   - **[[RustとWebAssemblyの親和性]]** (メモリ安全性、パフォーマンス、低レベル制御)
   - **[[Rust Wasmツールチェイン MOC]]**
      - `[[`wasm32-unknown-unknown` ターゲット]]`
      - `[[`wasm-pack` の役割と使い方 (ビルド、テスト、パッケージング)]]`
      - `[[`cargo-generate` を用いたプロジェクトテンプレート]]`
   - **[[wasm-bindgen MOC]]**
      - `[[wasm-bindgenの役割 (RustとJavaScript間の高レベルな相互作用)]]`
      - `[[`#[wasm_bindgen]` アトリビュート]]`
      - `[[Rustの構造体とJSのクラスのマッピング]]`
      - `[[文字列、ベクタ、クロージャなどのデータ型の扱い]]`
      - `[[DOM APIやWeb APIへのアクセス]]`
   - `[[Rust Wasmプロジェクトのビルドとnpmパッケージとしての公開]]`
   - `[[Rustにおけるパフォーマンスとコードサイズの最適化 (wee_alloc, LTO, etc.)]]`

### 3.4. [[GoからWebAssemblyへのコンパイル MOC]]
   - [[GoのWebAssemblyサポート (標準ツールチェイン)]]
   - `[[コンパイルコマンド (`GOOS=js GOARCH=wasm go build`)]]`
   - `[[syscall/js` パッケージによるDOM操作とJS連携]]`
   - [[Go Wasmの現状と課題 (バイナリサイズ、ガベージコレクション)]]
   - `[[TinyGo`による軽量なWasmモジュールの生成]]`

### 3.5. [[その他の言語からWebAssemblyへ MOC]]
   - `[[AssemblyScript (TypeScriptライクな言語)]]`
   - `[[Blazor (C#/.NET)]]`
   - `[[Pyodide (Python)]]`
   - `[[SwiftWasm (Swift)]]`

### 3.6. [[WebAssembly System Interface (WASI) MOC]]
   - [[WASIの定義と目的 (ブラウザ外のシステムリソースへの標準化されたアクセス)]]
   - [[WASIのコンセプト (ケーパビリティベースセキュリティ)]]
   - [[WASIが提供するAPI (ファイルシステム、ネットワーク、クロックなど)]]
   - [[ブラウザ外のWasmランタイム]] (`[[Wasmtime]], [[Wasmer]], [[WAVM]], [[Node.js (WASIサポート)]]`)
   - [[WasmとWASIによるポータブルなサーバーサイドアプリケーション]]

### 3.7. [[WebAssemblyのデバッグ手法 MOC]]
   - [[ブラウザ開発者ツールでのデバッグ]]
      - `[[ソースマップ (Source Maps) の利用]]`
      - `[[ブレークポイント設定とステップ実行]]`
      - `[[メモリインスペクタ]]`
   - `[[`console.log` / `printf` スタイルのデバッグ]]`
   - [[各言語ツールチェインのデバッグ機能]]

## 4. [[WebAssemblyのパフォーマンス MOC]]
   - **Wasmが高速な理由**
      - `[[高速なパースとデコード]]` (バイナリフォーマット)
      - `[[コンパイルと最適化の効率]]` (静的型付け、シンプルな命令セット)
      - `[[ネイティブに近い実行速度]]`
      - `[[ガベージコレクションの不在 (コア仕様)]]`
   - **WasmとJavaScriptのパフォーマンス比較**
      - [[CPU集約的なタスクにおけるWasmの優位性]]
      - [[DOM操作や頻繁なJS/Wasm間呼び出しにおけるオーバーヘッド]]
   - **パフォーマンス最適化**
      - `[[コンパイラ最適化フラグの活用]]`
      - `[[コードサイズの削減 (Dead Code Elimination)]]`
      - `[[JS/Wasm間の呼び出し回数の最小化]]`
      - `[[メモリ管理の最適化]]`
      - `[[SIMDの活用 (将来機能)]]`
      - `[[ストリーミングコンパイルとインスタンス化]]`

## 5. [[WebAssemblyのセキュリティ MOC]]
   - **[[サンドボックス化実行環境 (Sandboxed Execution Environment)]]**
      - `[[Wasmコードはホストシステムの他の部分から隔離される]]`
   - **[[メモリ安全性 (Memory Safety)]]**
      - `[[線形メモリによるメモリ空間の隔離]]`
      - `[[ホスト環境のメモリへの直接アクセス不可]]`
   - **[[制御フローの完全性 (Control-Flow Integrity - CFI)]]**
      - `[[不正なジャンプや関数呼び出しの防止]]`
   - **[[ケーパビリティベースセキュリティ (Capability-Based Security)]]**
      - `[[Wasmモジュールは明示的に与えられた機能 (インポート) しか実行できない]]`
      - `[[WASIにおけるケーパビリティベースセキュリティ]]`
   - **WebAssemblyの脆弱性と攻撃ベクタ**
      - `[[モジュール内の脆弱性 (C/C++からの移植に伴うバッファオーバーフローなど)]]`
      - `[[ホスト(JS)との連携部分の脆弱性]]`
      - `[[サイドチャネル攻撃 (Spectreなど) の可能性]]`
   - **WasmとContent Security Policy (CSP)**

## 6. [[WebAssemblyのユースケースと応用分野 MOC]] (再掲・詳細)
   - `[[Web上での高性能ゲーム (Unity, Unreal Engine)]]`
   - `[[クリエイティブツール (Figma, AutoCAD Web, Adobe Photoshop Web)]]`
   - `[[動画・音声処理 (Zoom, Google Meetの背景ぼかし)]]`
   - `[[データ圧縮・解凍ライブラリ]]`
   - `[[暗号化・ハッシュ計算ライブラリ]]`
   - `[[物理シミュレーションと科学技術計算]]`
   - `[[レガシーアプリケーションのWeb移植]]`
   - `[[サーバーレスコンピューティング (Cloudflare Workers, Fastly Compute@Edge)]]`
   - `[[ブロックチェーンとスマートコントラクト]]`
   - `[[プラグインシステム (Envoy ProxyのWasmフィルタ)]]`
   - `[[IoTデバイスでの利用]]`

## 7. [[WebAssemblyのエコシステムとツール MOC]]
   - **コンパイラとツールチェイン** (再掲・集約)
      - `[[Emscripten (C/C++)]]`
      - `[[Rust Wasm toolchain (wasm-pack, wasm-bindgen)]]`
      - `[[TinyGo (Go)]]`
      - `[[AssemblyScript (TypeScript-like)]]`
   - **Wasmランタイム** (再掲・集約)
      - `[[ブラウザ内蔵エンジン]]`
      - `[[Wasmtime]]`
      - `[[Wasmer]]`
      - `[[WAVM]]`
      - `[[Node.js]]`
   - **関連ライブラリとフレームワーク**
      - `[[WASIライブラリ]]`
      - `[[JS連携を容易にするライブラリ]]`
   - **デバッグとプロファイリングツール**
   - **パッケージレジストリ** (`[[WAPM (WebAssembly Package Manager)]]`など)
   - **オンラインWasm/WATプレイグラウンド** (WABT, WebAssembly Studioなど)

## 8. [[WebAssemblyの将来と高度なトピック MOC]]
   - **[[W3C WebAssembly Working Group と Community Group]]**
   - **標準化プロセスとプロポーザルの段階**
   - **策定中の主要な将来機能 (Post-MVP Features)**
      - **[[スレッディング (Threading)]]** (`SharedArrayBuffer`と`Atomics`を利用した並列処理)
      - **[[SIMD (Single Instruction, Multiple Data)]]** (ベクトル演算によるパフォーマンス向上)
      - **[[ガベージコレクション (Garbage Collection - GC)]]** (Java, C#, PythonなどGCを持つ言語からのコンパイルを容易に)
      - **[[例外処理 (Exception Handling)]]** (Wasmネイティブの例外)
      - **[[末尾呼び出し (Tail Calls)]]** (再帰の最適化)
      - **[[参照型 (Reference Types)]]** (テーブルの`anyfunc`の汎用化、GCとの連携)
      - **[[モジュールリンキング (Module Linking)]]**
      - **[[インターフェース型 (Interface Types) / コンポーネントモデル (Component Model)]]** (異なる言語でコンパイルされたWasmモジュール間の高度な連携)
   - **Wasmのブラウザ外でのさらなる応用**
      - `[[サーバーサイドWasm (Krustlet - Kubernetes Kubelet in Rust for Wasm)]]`
      - `[[データベース内での実行 (UDF)]]`
      - `[[OSとしてのWasm (概念)]]`
   - **WebAssemblyの課題と展望**
