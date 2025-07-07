---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/authentication-and-authorization
---
## 1. [[認証と認可入門 MOC]]
   - **認証と認可の基本**
      - **[[認証 (Authentication) の定義 (あなたは誰？ - Who you are)]]**
      - **[[認可 (Authorization) の定義 (あなたは何ができる？ - What you are allowed to do)]]**
      - [[認証と認可の明確な違いと比較]]
      - `[[(オプション) アカウンティング (Accounting) の定義 (あなたは何をした？ - What you did)]]`
      - `[[AAA (Authentication, Authorization, Accounting)]]`
   - **アイデンティティ (Identity) の概念**
      - `[[アイデンティティと属性]]`
      - `[[デジタルアイデンティティ]]`
      - `[[ID管理 (Identity Management - IdM / Identity and Access Management - IAM)]]`
   - **認証と認可の重要性** (セキュリティの第一防衛線)
   - **認証・認可の基本フロー** (ログイン→セッション/トークン発行→リソースへのアクセス要求→認可チェック)

## 2. [[認証 (Authentication) MOC]]

### 2.1. [[認証の要素 (Factors of Authentication) MOC]]
   - **知識情報 (Something you know)**: パスワード, PIN, 秘密の質問
   - **所持情報 (Something you have)**: スマートフォン, ハードウェアトークン, スマートカード, ICカード
   - **生体情報 (Something you are)**: 指紋, 顔, 虹彩, 静脈
   - **[[シングルファクタ認証 (SFA) vs. 多要素認証 (MFA)]]**

### 2.2. [[パスワードベース認証 MOC]]
   - **パスワード認証の仕組み** (ユーザー名とパスワードの検証)
   - **[[パスワードの安全な保存方法 MOC]]**
      - `[[平文保存 (絶対禁止)]]`
      - `[[ハッシュ化 (Hashing)]]`
      - **[[ソルト (Salt) の使用]]** (レインボーテーブル攻撃対策)
      - **[[ストレッチング (Stretching) / キー派生関数 (KDF)]]** (ブルートフォース攻撃対策)
         - `[[bcrypt]]`
         - `[[scrypt]]`
         - `[[Argon2]]` (現在の推奨)
         - `[[PBKDF2]]`
      - `[[(オプション) ペッパー (Pepper) の使用]]`
   - **[[パスワードポリシーの設計]]** (長さ、複雑性、有効期限の是非)
   - **[[安全なパスワードリセット機能の実装]]** (トークンベースのリセットフロー)
   - **パスワードベース認証への攻撃**
      - `[[ブルートフォース攻撃 (Brute-force Attack)]]`
      - `[[辞書攻撃 (Dictionary Attack)]]`
      - `[[クレデンシャルスタッフィング (Credential Stuffing)]]`
      - `[[キーロガー (Keylogger)]]`
      - `[[フィッシング (Phishing)]]`
   - **ブルートフォース攻撃対策**
      - `[[アカウントロックアウト]]`
      - `[[CAPTCHA / reCAPTCHA]]`
      - `[[レート制限]]`

### 2.3. [[多要素認証 (MFA - Multi-Factor Authentication) MOC]]
   - **MFAの定義と重要性**
   - `[[二要素認証 (2FA - Two-Factor Authentication)]]`
   - **MFAの要素と手法**
      - `[[SMS/電話認証]]` (利便性とSIMスワップのリスク)
      - `[[ワンタイムパスワード (OTP - One-Time Password)]]`
         - `[[TOTP (Time-based OTP)]]` (Google Authenticator, Microsoft Authenticatorなど)
         - `[[HOTP (HMAC-based OTP)]]`
      - `[[プッシュ通知認証 (Push Notification)]]`
      - `[[ハードウェアトークン / セキュリティキー]]` (FIDO/U2F)
      - `[[生体認証 (指紋, 顔など)]]`
   - `[[MFAの実装とユーザーオンボーディング]]`
   - `[[リカバリーコード]]`

### 2.4. [[パスワードレス認証 (Passwordless Authentication) MOC]]
   - **パスワードレス認証の概念と利点**
   - **パスワードレス認証の手法**
      - `[[マジックリンク (Magic Links)]]`
      - `[[OTPによるログイン]]`
      - **[[FIDO (Fast IDentity Online) / WebAuthn (Web Authentication) MOC]]**
         - `[[FIDO2 (WebAuthn + CTAP)]]`
         - `[[公開鍵暗号に基づく強力な認証]]`
         - `[[フィッシング耐性]]`
      - `[[生体認証による直接ログイン]]`

### 2.5. [[トークンベース認証 (Token-based Authentication) MOC]]
   - [[トークンベース認証の仕組み (ステートレス認証)]]
   - **[[JSON Web Token (JWT) MOC]]**
      - `[[JWTの構造 (Header, Payload, Signature)]]`
      - `[[JWTのクレーム (Claims - iss, sub, aud, exp, nbf, iat, jti)]]`
      - `[[署名アルゴリズム (HMAC - HS256, RSA - RS256)]]`
      - `[[アクセストークン (Access Token) とリフレッシュトークン (Refresh Token)]]`
      - `[[JWTのセキュリティ考慮事項 (alg:none, 署名検証, 有効期限, 失効, XSS対策)]]`
      - `[[JWTのストレージ (Cookie vs. localStorage)]]`
   - `[[セッションベース認証 vs. トークンベース認証]]`

### 2.6. [[シングルサインオン (Single Sign-On - SSO) MOC]]
   - [[SSOの定義と利点 (利便性向上、パスワード管理の軽減、セキュリティ強化)]]
   - [[SSOの仕組み (代理認証)]]
   - [[IdP (Identity Provider) と SP (Service Provider)]]
   - **SSOの実現プロトコル**
      - `[[SAML (Security Assertion Markup Language)]]` (詳細は後述)
      - `[[OpenID Connect (OIDC)]]` (詳細は後述)
      - `[[Kerberos]]` (詳細は後述)
   - `[[ソーシャルログイン (Social Login)]]`

### 2.7. [[フェデレーション認証 (Federated Authentication) MOC]]
   - [[フェデレーションの定義 (異なる組織・ドメイン間でのID連携)]]
   - [[信頼の輪 (Circle of Trust)]]
   - [[フェデレーションとSSOの関係]]

### 2.8. [[API認証 (API Authentication) MOC]]
   - `[[APIキー (API Keys)]]` (単純だがセキュリティは限定的)
   - `[[Basic認証 (Basic Authentication)]]` (非推奨)
   - `[[HMAC認証 (HMAC Authentication)]]`
   - `[[OAuth 2.0によるAPI認証]]`
   - `[[mTLS (Mutual TLS) によるクライアント認証]]`

## 3. [[認可 (Authorization) MOC]]

### 3.1. [[認可の基本概念 MOC]]
   - `[[プリンシパル (Principal), パーミッション (Permission), リソース (Resource)]]`
   - `[[アクセスポリシー (Access Policy)]]`
   - `[[最小権限の原則 (Principle of Least Privilege)]]` (再掲・認可文脈)
   - `[[デフォルト拒否 (Default Deny)]]`

### 3.2. [[アクセスコントロールモデル (Access Control Models) MOC]]
   - **[[任意アクセス制御 (DAC - Discretionary Access Control)]]**
      - `[[リソースの所有者がアクセス権を制御 (例: ファイルシステムのパーミッション)]]`
   - **[[強制アクセス制御 (MAC - Mandatory Access Control)]]**
      - `[[システム管理者がセキュリティポリシーに基づいてアクセス権を強制 (例: SELinux)]]`
   - **[[ロールベースアクセス制御 (RBAC - Role-Based Access Control)]]** (最も一般的)
      - `[[ユーザー → ロール → パーミッションの割り当て]]`
      - `[[RBACの実装パターン]]`
   - **[[属性ベースアクセス制御 (ABAC - Attribute-Based Access Control)]]**
      - `[[ユーザー、リソース、環境の属性に基づいた動的なアクセス制御]]`
      - `[[ポリシー言語 (XACMLなど)]]`
   - `[[(オプション) ACL (Access Control List) vs. Capability-based Security]]`
   - `[[(オプション) 関係ベースアクセス制御 (ReBAC - Relationship-Based Access Control)]]` (Google Zanzibarなど)

### 3.3. [[OAuth 2.0 MOC]] (委譲認可のフレームワーク)
   - `[[OAuth 2.0の目的 (ユーザーの同意に基づき、サードパーティアプリケーションに限定的なリソースアクセス権限を与える)]]`
   - **OAuth 2.0のロール**
      - `[[リソースオーナー (Resource Owner)]]` (ユーザー)
      - `[[クライアント (Client)]]` (アプリケーション)
      - `[[認可サーバー (Authorization Server)]]`
      - `[[リソースサーバー (Resource Server)]]`
   - **OAuth 2.0のトークン**
      - `[[アクセストークン (Access Token)]]`
      - `[[リフレッシュトークン (Refresh Token)]]`
   - **[[OAuth 2.0の認可フロー (Grant Types) MOC]]**
      - **[[認可コードフロー (Authorization Code Flow)]]** (サーバーサイドWebアプリ向け)
         - `[[PKCE (Proof Key for Code Exchange) による拡張]]` (モバイル/SPA向け)
      - `[[インプリシットフロー (Implicit Flow)]]` (レガシー、非推奨)
      - `[[リソースオーナー・パスワード・クレデンシャルフロー (Resource Owner Password Credentials Flow)]]` (非推奨)
      - `[[クライアント・クレデンシャルフロー (Client Credentials Flow)]]` (M2M通信向け)
      - `[[(オプション) デバイス認可フロー (Device Authorization Flow)]]`
   - **[[スコープ (Scopes)]]** (権限の範囲)
   - **OAuth 2.0のセキュリティ考慮事項**
      - `[[リダイレクトURIの厳格な検証]]`
      - `[[stateパラメータによるCSRF対策]]`
      - `[[トークン漏洩対策]]`

## 4. [[主要なプロトコルと標準 MOC]]

### 4.1. [[OpenID Connect (OIDC) MOC]]
   - `[[OIDCの定義 (OAuth 2.0を基盤とした認証レイヤー)]]`
   - `[[OIDCとOAuth 2.0の違い (認証 vs. 認可)]]`
   - **[[IDトークン (ID Token)]]**
      - `[[IDトークンの形式 (JWT)]]`
      - `[[IDトークンのクレーム (iss, sub, aud, exp, iatなど)]]`
   - **OIDCのフロー**
      - `[[認可コードフロー (Authorization Code Flow)]]`
      - `[[インプリシットフロー (Implicit Flow)]]` (一部非推奨)
      - `[[ハイブリッドフロー (Hybrid Flow)]]`
   - **OIDCのエンドポイント**
      - `[[認可エンドポイント (Authorization Endpoint)]]`
      - `[[トークンエンドポイント (Token Endpoint)]]`
      - `[[UserInfoエンドポイント (UserInfo Endpoint)]]`
   - `[[OIDCのメタデータ (`.well-known/openid-configuration`)]]`
   - `[[OIDCのユースケース (ソーシャルログイン、SSO)]]`

### 4.2. [[SAML (Security Assertion Markup Language) MOC]]
   - `[[SAMLの定義 (XMLベースの認証・認可情報交換標準)]]`
   - `[[SAMLのユースケース (エンタープライズSSO)]]`
   - **SAMLの主要コンポーネント**
      - `[[アサーション (Assertion)]]`
      - `[[プロトコル (Protocol)]]`
      - `[[バインディング (Binding)]]`
   - **SAMLのフロー** (SP-Initiated SSO, IdP-Initiated SSO)
   - `[[SAMLとOIDCの比較]]`

### 4.3. [[Kerberos MOC]]
   - `[[Kerberosの定義 (チケットベースのネットワーク認証プロトコル)]]`
   - `[[Kerberosのアーキテクチャ (KDC, AS, TGS)]]`
   - `[[Kerberosの認証フロー]]`
   - `[[Kerberosの利用例 (Active Directory)]]`

### 4.4. [[LDAP (Lightweight Directory Access Protocol) MOC]]
   - `[[LDAPの定義 (ディレクトリサービスへのアクセスプロトコル)]]`
   - `[[LDAPのデータモデル (DIT, DN, RDN, エントリ, 属性)]]`
   - `[[LDAPの操作 (bind, search, add, modify, delete)]]`
   - `[[LDAPの利用例 (中央集権的なユーザー情報管理)]]`

### 4.5. [[FIDO / WebAuthn MOC]] (再掲・プロトコルとして)
   - `[[FIDO Allianceの役割]]`
   - `[[WebAuthn (W3C標準) と CTAP (Client to Authenticator Protocol)]]`
   - `[[公開鍵暗号に基づく認証の仕組み]]`

## 5. [[実装と運用 MOC]]
   - **ID管理 (Identity Management - IdM) / Identity and Access Management (IAM)**
      - [[IAMシステムの機能 (IDライフサイクル管理, プロビジョニング, 認証, 認可, 監査)]]
      - `[[Cloud IAM (AWS, Azure, GCP)]]`
   - **セキュアな実装プラクティス**
      - `[[実績のあるライブラリやフレームワークの利用]]`
      - `[[認証・認可ロジックの集中管理]]`
      - `[[タイミング攻撃対策]]`
   - **セッション管理のセキュリティ** (再掲・重要)
      - `[[セキュアなCookie属性 (`HttpOnly`, `Secure`, `SameSite`)]]`
      - `[[セッション固定化対策]]`
      - `[[セッションハイジャック対策]]`
   - **Identity as a Service (IDaaS)**
      - `[[IDaaSの定義と利点]]`
      - `[[主要なIDaaSプロバイダー (Okta, Auth0 (by Okta), Microsoft Entra ID, Ping Identity)]]`
   - **ロギング、監査、監視**
      - `[[認証成功/失敗、認可失敗、パスワード変更などのイベントをログに記録]]`
      - `[[不審なアクティビティの監視とアラート]]`
      - `[[監査証跡 (Audit Trail)]]`

## 6. [[将来のトレンドと高度なトピック MOC]]
   - **[[分散型ID (Decentralized Identity - DID)]]**
      - `[[自己主権型アイデンティティ (Self-Sovereign Identity - SSI)]]`
      - `[[検証可能なクレデンシャル (Verifiable Credentials - VCs)]]`
      - `[[ブロックチェーンとDID]]`
   - **[[継続的認証 (Continuous Authentication) / Risk-Based Authentication]]**
      - `[[行動パターンやコンテキストに基づいた継続的なリスク評価]]`
   - **パスワードレス認証のさらなる普及**
   - **IoTデバイスの認証・認可**
   - **AI/MLを活用した異常検知と認証**
   - **プライバシー保護とID管理**

## 7. [[認証・認可アンチパターン MOC]]
   - `[[パスワードの平文保存]]`
   - `[[不安全なパスワードリセット]]`
   - `[[セッションIDのURL埋め込み]]`
   - `[[エラーメッセージによるユーザー存在有無の漏洩]]`
   - `[[クライアント側のみでの認可チェック]]`
   - `[[長時間有効なアクセストークン]]`
   - `[[リフレッシュトークンの不適切な管理]]`
   - `[[OAuth 2.0のImplicitフローの不適切な使用]]`
   - `[[自作の暗号/認証プロトコルの使用]]`
