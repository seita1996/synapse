---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/cryptography
---
# [[暗号技術 MOC]]

## 1. [[暗号技術入門 MOC]]
   - **暗号技術とは**
      - [[暗号技術の定義 (第三者が読み取れないように情報を変換する技術、およびその逆の技術)]]
      - [[暗号学 (Cryptology) = 暗号理論 (Cryptography) + 暗号解読 (Cryptanalysis)]]
   - **暗号の目的とセキュリティ目標**
      - **[[機密性 (Confidentiality)]]** (認可された者だけが情報にアクセスできる)
      - **[[完全性 (Integrity)]]** (情報が改ざんされていないことを保証)
      - **[[認証 (Authentication)]]** (通信相手が本人であることを確認)
      - **[[否認防止 (Non-repudiation)]]** (送信者が後で送信を否認できないようにする)
      - `[[(オプション) 可用性 (Availability), 匿名性 (Anonymity)など]]`
   - **暗号技術の基本用語**
      - `[[平文 (Plaintext)]]`
      - `[[暗号文 (Ciphertext)]]`
      - `[[暗号化 (Encryption)]]`
      - `[[復号 (Decryption)]]`
      - `[[鍵 (Key)]]`
      - `[[暗号アルゴリズム (Cipher / Algorithm)]]`
   - **[[ケルクホフスの原理 (Kerckhoffs's Principle)]]**
      - [[「暗号方式の安全性は、鍵以外の全てが公開されても保たれなければならない」]]
      - [[「隠蔽によるセキュリティ (Security by Obscurity)」の危険性]]
   - **暗号の分類**
      - `[[共通鍵暗号 vs. 公開鍵暗号]]`
      - `[[ブロック暗号 vs. ストリーム暗号]]`
      - `[[決定性暗号 vs. 確率的暗号]]`
   - **暗号技術の歴史**
      - `[[古典暗号 (シーザー暗号, 換字式暗号, 転置式暗号, ヴィジュネル暗号)]]`
      - `[[エニグマ (Enigma) と機械式暗号]]`
      - `[[シャノンの情報理論と現代暗号の基礎]]`
      - `[[DESの制定と公開鍵暗号の登場]]`

## 2. [[共通鍵暗号 (Symmetric-Key Cryptography) MOC]]
   - **共通鍵暗号の基本**
      - [[共通鍵暗号の仕組み (暗号化と復号に同じ鍵を使用)]]
      - `[[利点 (高速) と欠点 (鍵配送問題、鍵管理の複雑さ)]]`
   - **[[ストリーム暗号 (Stream Ciphers) MOC]]**
      - [[ストリーム暗号の仕組み (平文を1ビットまたは1バイト単位で暗号化)]]
      - `[[鍵ストリーム (Key Stream) とXOR演算]]`
      - `[[ワンタイムパッド (OTP - One-Time Pad)]]` (理論的に解読不能な暗号)
      - `[[擬似乱数生成器 (PRNG - Pseudo-Random Number Generator)]]`
      - `[[同期型 vs. 非同期型ストリーム暗号]]`
      - `[[代表的なアルゴリズム (RC4 (脆弱), ChaCha20)]]`
      - `[[鍵ストリームの再利用の危険性]]`
   - **[[ブロック暗号 (Block Ciphers) MOC]]**
      - [[ブロック暗号の仕組み (平文を固定長のブロックに分割して暗号化)]]
      - `[[ブロック長と鍵長]]`
      - `[[SPN構造 (Substitution-Permutation Network)]]`
      - `[[Feistel構造 (Feistel Network)]]`
      - **[[パディング (Padding)]]** (最後のブロックがブロック長に満たない場合の対処)
         - `[[PKCS#7 (旧PKCS#5) パディングなど]]`
      - **[[ブロック暗号の利用モード (Mode of Operation) MOC]]**
         - `[[ECB (Electronic Codebook) モード]]` (非推奨、同じ平文ブロックは同じ暗号文ブロックになる)
         - `[[CBC (Cipher Block Chaining) モード]]` (連鎖、初期化ベクトルIV)
         - `[[CFB (Cipher Feedback) モード]]` (ブロック暗号をストリーム暗号として利用)
         - `[[OFB (Output Feedback) モード]]` (ブロック暗号をストリーム暗号として利用)
         - `[[CTR (Counter) モード]]` (カウンタを暗号化しXOR、並列処理可能)
         - **[[認証付き暗号 (AEAD - Authenticated Encryption with Associated Data) MOC]]**
            - `[[GCM (Galois/Counter Mode)]]`
            - `[[CCM (Counter with CBC-MAC)]]`
            - `[[(オプション) OCB (Offset Codebook Mode)]]`
   - **代表的な共通鍵暗号アルゴリズム**
      - `[[DES (Data Encryption Standard)]]` (歴史的、脆弱)
      - `[[3DES (Triple DES)]]` (DESを3回適用、低速)
      - **[[AES (Advanced Encryption Standard / Rijndael)]]** (現在の標準)
         - `[[AESのブロック長と鍵長 (128, 192, 256ビット)]]`
         - `[[AESの内部構造 (SubBytes, ShiftRows, MixColumns, AddRoundKey)]]`
      - `[[(オプション) その他のアルゴリズム (Blowfish, Twofish, Camelliaなど)]]`

## 3. [[公開鍵暗号 (Asymmetric-Key Cryptography) MOC]]
   - **公開鍵暗号の基本**
      - [[公開鍵暗号の仕組み (公開鍵で暗号化し、秘密鍵で復号)]]
      - `[[公開鍵 (Public Key) と秘密鍵 (Private Key) のペア]]`
      - `[[利点 (鍵配送問題の解決) と欠点 (低速)]]`
      - [[ハイブリッド暗号 (Hybrid Cryptosystem)]] (公開鍵暗号で共通鍵を交換し、共通鍵暗号でデータを暗号化)
   - **公開鍵暗号の数理的基礎 (概要)**
      - **[[一方向性関数 (One-way Function)]]**
      - **[[落とし戸付き一方向性関数 (Trapdoor One-way Function)]]**
      - **[[計算困難な問題]]**
         - `[[素因数分解問題 (Integer Factorization Problem)]]` (RSAの基礎)
         - `[[離散対数問題 (Discrete Logarithm Problem - DLP)]]` (Diffie-Hellman, DSAの基礎)
         - `[[楕円曲線上の離散対数問題 (Elliptic Curve Discrete Logarithm Problem - ECDLP)]]` (ECCの基礎)
   - **代表的な公開鍵暗号アルゴリズム**
      - **[[RSA暗号 MOC]]** (Rivest-Shamir-Adleman)
         - `[[RSAの鍵生成、暗号化、復号のアルゴリズム]]`
         - `[[RSA暗号の安全性 (素因数分解の困難性)]]`
         - `[[パディングスキーム (OAEP)]]`
      - **[[Diffie-Hellman鍵交換 (DH鍵交換) MOC]]**
         - `[[DH鍵交換の仕組み (離散対数問題に基づく安全な鍵共有)]]`
         - `[[中間者攻撃 (Man-in-the-Middle Attack) に対する脆弱性]]` (認証が必要)
      - **[[ElGamal暗号]]** (離散対数問題に基づく)
   - **[[楕円曲線暗号 (ECC - Elliptic Curve Cryptography) MOC]]** (詳細は現代暗号で)
      - [[ECCの概要と利点 (短い鍵長で高い安全性)]]
      - `[[ECDH (Elliptic Curve Diffie-Hellman)]]`
      - `[[ECDSA (Elliptic Curve Digital Signature Algorithm)]]`

## 4. [[ハッシュ関数 (Cryptographic Hash Functions) MOC]]
   - **ハッシュ関数の基本**
      - [[ハッシュ関数の定義 (任意の長さのデータを固定長のハッシュ値に変換する関数)]]
      - [[ハッシュ関数と暗号化の違い]]
   - **暗号学的ハッシュ関数の重要な性質**
      - **[[原像計算困難性 (Preimage Resistance)]]** (ハッシュ値から元のデータを見つけるのが困難)
      - **[[第二原像計算困難性 (Second Preimage Resistance)]]** (あるデータと同じハッシュ値を持つ別のデータを見つけるのが困難)
      - **[[衝突困難性 (Collision Resistance)]]** (同じハッシュ値を持つ2つの異なるデータを見つけるのが困難)
   - **[[マークル・ダムガード構造 (Merkle–Damgård Construction)]]**
   - **代表的なハッシュ関数アルゴリズム**
      - `[[MD5 (Message Digest 5)]]` (脆弱、衝突発見済み、使用禁止)
      - `[[SHA-1 (Secure Hash Algorithm 1)]]` (脆弱、衝突発見済み、使用禁止)
      - **[[SHA-2ファミリー (SHA-256, SHA-384, SHA-512)]]** (現在広く利用)
      - **[[SHA-3 (Keccak)]]** (新しい標準)
      - `[[(オプション) BLAKE2/BLAKE3]]`
   - **ハッシュ関数の応用**
      - `[[データの完全性検証 (チェックサム)]]`
      - `[[デジタル署名]]`
      - `[[メッセージ認証コード (HMAC)]]`
      - `[[パスワードの保存]]`
         - `[[ソルト (Salt) の使用]]`
         - `[[ストレッチング (Stretching) / キー派生関数 (KDF)]]` (bcrypt, scrypt, Argon2, PBKDF2)
      - `[[ブロックチェーン (Proof of Work)]]`
      - `[[擬似乱数生成]]`

## 5. [[メッセージ認証とデジタル署名 MOC]]
   - **メッセージ認証の必要性 (完全性と認証)**
   - **[[メッセージ認証コード (MAC - Message Authentication Code) MOC]]**
      - [[MACの仕組み (メッセージと共通鍵から固定長のMAC値を生成)]]
      - **[[HMAC (Hash-based Message Authentication Code)]]**
         - `[[HMACの構造 (ハッシュ関数と鍵を使用)]]`
      - `[[CMAC (Cipher-based Message Authentication Code)]]`
      - `[[(AEADにおける認証タグ)]]`
   - **[[デジタル署名 (Digital Signature) MOC]]**
      - **[[デジタル署名の仕組み (秘密鍵で署名し、公開鍵で検証)]]**
      - `[[デジタル署名が提供するもの (認証, 完全性, 否認防止)]]`
      - **デジタル署名のプロセス**
         - `[[署名生成 (メッセージのハッシュ値を秘密鍵で暗号化)]]`
         - `[[署名検証 (公開鍵で復号し、ハッシュ値が一致するか確認)]]`
      - **代表的なデジタル署名アルゴリズム**
         - `[[RSA署名 (RSA-PSS)]]`
         - `[[DSA (Digital Signature Algorithm)]]`
         - `[[ECDSA (Elliptic Curve Digital Signature Algorithm)]]`
      - `[[MACとデジタル署名の違い (鍵の共有形態と否認防止の有無)]]`
      - `[[ブラインド署名 (Blind Signature)]]` (概要)

## 6. [[鍵管理と公開鍵基盤 (PKI) MOC]]
   - **[[鍵管理 (Key Management) MOC]]**
      - [[鍵管理の重要性とライフサイクル (生成, 配布, 保管, 更新, 破棄)]]
      - [[鍵配送問題 (Key Distribution Problem)]]
      - [[鍵合意プロトコル (Key Agreement Protocol)]] (Diffie-Hellmanなど)
      - [[鍵導出関数 (KDF - Key Derivation Function)]]
      - `[[ハードウェアセキュリティモジュール (HSM - Hardware Security Module)]]`
   - **[[公開鍵基盤 (PKI - Public Key Infrastructure) MOC]]**
      - [[PKIの定義と目的 (公開鍵の正当性を保証するための仕組み)]]
      - **[[デジタル証明書 (Digital Certificate) MOC]]**
         - `[[X.509証明書の構造 (バージョン, シリアル番号, 署名アルゴリズム, 発行者, 有効期間, 主体者, 公開鍵情報, CAの署名)]]`
      - **[[認証局 (CA - Certificate Authority)]]**
         - `[[CAの役割 (本人確認と証明書の発行)]]`
         - `[[ルートCAと中間CA (信頼の連鎖 - Chain of Trust)]]`
      - **[[登録局 (RA - Registration Authority)]]**
      - **[[リポジトリ (Repository)]]**
      - **[[証明書失効 (Certificate Revocation)]]**
         - `[[証明書失効リスト (CRL - Certificate Revocation List)]]`
         - `[[OCSP (Online Certificate Status Protocol)]]`
         - `[[(オプション) OCSP Stapling]]`
      - **[[証明書の種類]]**
         - `[[ドメイン認証 (DV - Domain Validated)]]`
         - `[[組織認証 (OV - Organization Validated)]`
         - `[[拡張認証 (EV - Extended Validation)]]`
      - **[[自己署名証明書 (Self-signed Certificate)]]**

## 7. [[暗号プロトコルと応用 MOC]]
   - **暗号プロトコルの定義 (暗号技術を組み合わせて特定のセキュリティ目標を達成するための通信手順)**
   - **[[TLS/SSL (Transport Layer Security / Secure Sockets Layer) MOC]]**
      - `[[TLS/SSLの役割 (TCP/IP上での安全な通信路の提供)]]`
      - **[[TLSハンドシェイクプロトコル]]**
         - `[[ClientHello, ServerHello, ServerCertificate, ServerHelloDone, ClientKeyExchange, ChangeCipherSpec, Finished]]`
         - `[[暗号スイート (Cipher Suite) のネゴシエーション]]`
         - `[[セッション鍵の生成]]`
      - `[[TLSレコードプロトコル]]`
      - `[[TLS 1.2 vs. TLS 1.3]]`
   - **[[SSH (Secure Shell) MOC]]**
      - `[[SSHの役割 (安全なリモートシェルアクセス、ポートフォワーディング)]]`
      - `[[SSHのアーキテクチャ (トランスポート層, ユーザー認証層, コネクション層)]]`
      - `[[SSHの認証方式 (パスワード認証, 公開鍵認証)]]`
   - **[[IPsec (Internet Protocol Security) MOC]]** (概要)
      - `[[AH (Authentication Header) と ESP (Encapsulating Security Payload)]]`
      - `[[トンネルモードとトランスポートモード]]`
   - **[[PGP (Pretty Good Privacy) / GnuPG (GPG) MOC]]**
      - `[[メール暗号化の仕組み]]`
      - `[[信頼の輪 (Web of Trust)]]`
   - **[[ブロックチェーンと暗号技術 MOC]]**
      - `[[ハッシュチェーン]]`
      - `[[デジタル署名によるトランザクションの正当性確保]]`
      - `[[Proof of Workとハッシュ関数]]`
      - `[[ゼロ知識証明の応用]]` (Zcashなど)
   - **[[Kerberos認証プロトコル]]** (概要)
   - **[[WPA2/WPA3 (Wi-Fi Protected Access)]]** (無線LANの暗号化)

## 8. [[現代暗号と将来の展望 MOC]]
   - **[[楕円曲線暗号 (ECC - Elliptic Curve Cryptography) MOC]]** (再掲・詳細)
      - `[[楕円曲線の数理]]` (概要)
      - `[[楕円曲線上の離散対数問題 (ECDLP)]]`
      - `[[ECCの利点 (短い鍵長でRSAと同等の安全性)]]`
      - `[[ECDH (Elliptic Curve Diffie-Hellman)]]`
      - `[[ECDSA (Elliptic Curve Digital Signature Algorithm)]]`
      - `[[(オプション) Edwards-curve Digital Signature Algorithm (EdDSA) - Ed25519]]`
   - **[[ペアリングベース暗号 (Pairing-Based Cryptography) MOC]]** (概要)
      - `[[IDベース暗号 (Identity-Based Encryption - IBE)]]`
      - `[[属性ベース暗号 (Attribute-Based Encryption - ABE)]]`
   - **[[量子コンピュータと暗号 MOC]]**
      - `[[量子コンピュータが既存暗号に与える脅威]]`
      - `[[Shorのアルゴリズム (素因数分解と離散対数問題を効率的に解く)]]` (RSA, ECCの解読)
      - `[[Groverのアルゴリズム (非構造化探索)]]` (共通鍵暗号の鍵長への影響)
   - **[[耐量子計算機暗号 (PQC - Post-Quantum Cryptography) MOC]]**
      - `[[PQCの目的とアプローチ]]`
      - `[[格子ベース暗号 (Lattice-based cryptography)]]`
      - `[[多変数公開鍵暗号 (Multivariate public-key cryptography)]]`
      - `[[ハッシュベース署名 (Hash-based signatures)]]`
      - `[[符号ベース暗号 (Code-based cryptography)]]`
      - `[[NISTによるPQC標準化動向]]`
   - **[[量子暗号 (Quantum Cryptography) MOC]]** (量子鍵配送 - QKD)
      - `[[BB84プロトコルなど]]`
      - `[[PQCとの違い]]`
   - **[[準同型暗号 (Homomorphic Encryption) MOC]]**
      - `[[暗号化したまま計算できる暗号]]`
      - `[[完全準同型暗号 (FHE) の概念と課題]]`
   - **[[ゼロ知識証明 (Zero-Knowledge Proof - ZKP) MOC]]**
      - `[[ZKPの定義 (命題が真であること以外の情報を明かさずに証明)]]`
      - `[[ZKPの性質 (完全性, 健全性, ゼロ知識性)]]`
      - `[[対話型 vs. 非対話型 (NIZK)]]`
      - `[[zk-SNARKs, zk-STARKs]]` (概要)
      - `[[ZKPの応用 (ブロックチェーン、認証)]]`
   - **[[安全なマルチパーティ計算 (Secure Multi-Party Computation - SMPC)]]**
      - `[[互いの入力を秘密にしたまま協調して計算するプロトコル]]`
   - **[[(オプション) 暗号通貨とウォレットのセキュリティ]]**
   - **[[(オプション) デジタル著作権管理 (DRM)]]`

## 9. [[暗号解読 (Cryptanalysis) MOC]] (概要)
   - **暗号解読の目的**
   - **攻撃モデル (攻撃者が利用可能な情報による分類)**
      - `[[暗号文単独攻撃 (Ciphertext-only Attack)]]`
      - `[[既知平文攻撃 (Known-plaintext Attack)]]`
      - `[[選択平文攻撃 (Chosen-plaintext Attack - CPA)]]`
      - `[[選択暗号文攻撃 (Chosen-ciphertext Attack - CCA)]]` (CCA1, CCA2)
   - **主な攻撃手法**
      - `[[ブルートフォース攻撃 (Brute-force Attack / 全数探索)]]`
      - `[[辞書攻撃 (Dictionary Attack)]]`
      - `[[頻度分析 (Frequency Analysis)]]` (古典暗号)
      - `[[差分解読法 (Differential Cryptanalysis)]]` (ブロック暗号)
      - `[[線形解読法 (Linear Cryptanalysis)]]` (ブロック暗号)
      - `[[中間者攻撃 (Man-in-the-Middle Attack - MitM)]]`
      - `[[リプレイ攻撃 (Replay Attack)]]`
      - **[[サイドチャネル攻撃 (Side-Channel Attack)]]**
         - `[[タイミング攻撃 (Timing Attack)]]`
         - `[[電力解析攻撃 (Power Analysis)]]`
         - `[[音響攻撃、電磁波攻撃]]`
      - `[[誕生日攻撃 (Birthday Attack)]]` (ハッシュ衝突)
