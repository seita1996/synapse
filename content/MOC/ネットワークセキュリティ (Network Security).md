---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/network-security
---
## 1. [[ネットワークセキュリティ入門 MOC]]
   - **ネットワークセキュリティとは**
      - [[ネットワークセキュリティの定義 (ネットワークインフラ、およびそれを行き来するトラフィックを不正アクセス、誤用、改ざん、破壊から保護する実践)]]
      - [[ネットワークセキュリティの目的 (CIAトライアドの確保)]]
         - `[[機密性 (Confidentiality) - 盗聴の防止]]`
         - `[[完全性 (Integrity) - 改ざんの防止]]`
         - `[[可用性 (Availability) - サービス妨害の防止]]`
   - **脅威アクターと攻撃動機**
      - [[攻撃者の種類 (ハクティビスト, サイバー犯罪者, 国家支援型攻撃者, 内部犯行者)]]
   - **攻撃の段階 (サイバーキルチェーン / ATT&CKフレームワーク)**
      - `[[偵察 → 武器化 → 配送 → 攻撃 → インストール → 遠隔操作 → 目的実行]]` (キルチェーンの例)
   - **ネットワークセキュリティの基本戦略**
      - **[[多層防御 (Defense in Depth / Layered Security)]]**
      - **[[ネットワークセグメンテーション (Network Segmentation)]]**
      - **[[最小権限の原則 (Principle of Least Privilege)]]** (ネットワークアクセスにおける)
      - **[[攻撃対象領域 (Attack Surface) の最小化]]**
   - **ネットワークトポロジとセキュリティ** (DMZ, 内部ネットワーク, 境界)

## 2. [[防御技術とツール MOC]]

### 2.1. [[ファイアウォール (Firewall) MOC]]
   - **ファイアウォールの基本**
      - [[ファイアウォールの定義と役割 (ネットワーク間のトラフィック制御)]]
      - [[デフォルト拒否 (Default Deny) vs. デフォルト許可 (Default Allow)]]
   - **ファイアウォールの種類**
      - **[[パケットフィルタリングファイアウォール (Packet-Filtering Firewall)]]**
         - `[[動作原理 (L3/L4ヘッダ情報に基づく制御)]]`
         - `[[ステートレス (Stateless)]]`
      - **[[ステートフルインスペクションファイアウォール (Stateful Inspection Firewall)]]**
         - `[[動作原理 (コネクションテーブルによる状態管理)]]`
      - **[[プロキシファイアウォール (Proxy Firewall) / アプリケーションゲートウェイ]]**
         - `[[動作原理 (アプリケーションレベルでの通信仲介)]]`
      - **[[次世代ファイアウォール (NGFW - Next-Generation Firewall)]]**
         - `[[NGFWの機能 (アプリケーション識別, IPS, 詳細な可視化)]]`
      - **[[Webアプリケーションファイアウォール (WAF - Web Application Firewall)]]** (詳細は後述)
   - **ファイアウォールの配置アーキテクチャ**
      - `[[境界ファイアウォール]]`
      - `[[DMZ (DeMilitarized Zone) / 非武装地帯]]`
      - `[[内部ファイアウォール (マイクロセグメンテーション)]]`
   - `[[パーソナルファイアウォールとホストベースファイアウォール]]`

### 2.2. [[侵入検知・防御システム (IDS/IPS) MOC]]
   - **[[侵入検知システム (IDS - Intrusion Detection System)]]**
      - [[IDSの定義と役割 (不正なアクティビティの検知と警告)]]
      - **[[ネットワーク型IDS (NIDS - Network IDS)]]**
      - **[[ホスト型IDS (HIDS - Host-based IDS)]]**
   - **[[侵入防止システム (IPS - Intrusion Prevention System)]]**
      - [[IPSの定義と役割 (不正なアクティビティの検知とブロック)]]
   - **検知手法**
      - `[[シグネチャベース検知 (Signature-based Detection)]]`
      - `[[アノマリーベース検知 (Anomaly-based Detection)]` (異常検知)
      - `[[ステートフルプロトコル分析]]`
   - `[[IDS/IPSの配置場所と注意点 (誤検知 - False Positive, 未検知 - False Negative)]]`
   - `[[SIEM (Security Information and Event Management) との連携]]`

### 2.3. [[仮想プライベートネットワーク (VPN - Virtual Private Network) MOC]]
   - **VPNの定義と目的** (公衆網上に安全なプライベート通信路を構築)
   - **VPNの主要技術**
      - **[[IPsec (Internet Protocol Security) MOC]]**
         - `[[トンネルモードとトランスポートモード]]`
         - `[[AH (Authentication Header) と ESP (Encapsulating Security Payload)]]`
         - `[[IKE (Internet Key Exchange)]]`
      - **[[SSL/TLS VPN MOC]]**
         - `[[Webブラウザから利用できる利便性]]`
         - `[[OpenVPN, WireGuardなどの実装]]`
   - **VPNの種類**
      - `[[リモートアクセスVPN]]`
      - `[[サイト間VPN (Site-to-Site VPN)]]`
   - **VPNのセキュリティ考慮事項** (スプリットトンネリングなど)

### 2.4. [[Webアプリケーションファイアウォール (WAF) MOC]]
   - `[[WAFの定義と役割 (Webアプリケーションに特化した保護)]]`
   - `[[WAFが防御する主な攻撃 (SQLi, XSS, CSRFなど)]]`
   - `[[シグネチャベース vs. ポジティブセキュリティモデル (ホワイトリスト)]]`
   - `[[クラウド型WAF vs. アプライアンス型WAF]]`

### 2.5. [[その他の防御技術 MOC]]
   - `[[プロキシサーバー (Proxy Server)]]` (フォワードプロキシ, リバースプロキシ)
   - `[[ロードバランサ (Load Balancer) のセキュリティ機能]]`
   - `[[ネットワークアクセス制御 (NAC - Network Access Control)]]`
   - `[[サンドボックス (Sandbox)]]` (マルウェア解析)
   - `[[ハニーポット (Honeypot)]]`

## 3. [[一般的なネットワーク攻撃と対策 MOC]]

### 3.1. [[サービス妨害攻撃 (DoS/DDoS) MOC]]
   - **[[DoS (Denial of Service) / DDoS (Distributed DoS) 攻撃の目的]]** (サービス停止)
   - **攻撃の種類**
      - **ボリューム型攻撃**
         - `[[UDPフラッド, ICMPフラッド]]`
      - **プロトコル攻撃**
         - `[[SYNフラッド]]`
         - `[[Ping of Death]]`
      - **アプリケーション層攻撃**
         - `[[HTTPフラッド (Slowloris, RUDY)]]`
   - **[[DDoS対策]]**
      - `[[レート制限]]`
      - `[[IPアドレスのフィルタリング/ブロッキング]]`
      - `[[DDoS緩和サービス (Cloudflare, Akamaiなど)]]`
      - `[[CDNの活用]]`

### 3.2. [[盗聴と中間者攻撃 (Eavesdropping and Man-in-the-Middle) MOC]]
   - **[[盗聴 (Eavesdropping / Sniffing)]]**
      - `[[パケットキャプチャツール (Wireshark, tcpdump)]]`
      - `[[対策: 通信の暗号化 (HTTPS, SSH, VPN)]]`
   - **[[中間者攻撃 (MitM - Man-in-the-Middle Attack)]]**
      - `[[MitM攻撃の仕組み]]`
      - **[[ARPスプーフィング (ARP Spoofing / ARP Poisoning)]]**
      - `[[DNSスプーフィング (DNS Spoofing / DNS Cache Poisoning)]]`
      - `[[SSLストリッピング (SSL Stripping)]]`
      - `[[対策: HTTPS/HSTS, DNSSEC, 証明書検証, VPN]]`

### 3.3. [[なりすまし (Spoofing) MOC]]
   - **[[IPスプーフィング (IP Spoofing)]]**
   - **[[MACスプーフィング (MAC Spoofing)]]**
   - **[[メールスプーフィング (Email Spoofing)]]** (SPF, DKIM, DMARCによる対策)
   - `[[DNSスプーフィング]]` (再掲)
   - `[[ARPスプーフィング]]` (再掲)

### 3.4. [[ポートスキャンと偵察 (Port Scanning and Reconnaissance) MOC]]
   - `[[ポートスキャンの目的と手法 (TCP Connect, SYN Scan, UDP Scanなど)]]`
   - `[[ネットワークマッピング]]`
   - `[[OSフィンガープリンティング]]`
   - `[[対策: ファイアウォールによる不要ポートの閉鎖, IDS/IPSによる検知]]`
   - `[[ツール (Nmap)]]`

### 3.5. [[セッションハイジャック (Session Hijacking) MOC]]
   - `[[セッションハイジャックの仕組み (セッショントークンの窃取)]]`
   - `[[攻撃手法 (XSS, Sniffing, セッション固定化)]]`
   - `[[対策: セキュアなセッション管理 (HttpOnly/Secure Cookie, トークン更新, IPアドレス/User-Agentの監視)]]`

## 4. [[無線LANセキュリティ (Wireless Network Security) MOC]]
   - **無線LANの脆弱性**
   - **Wi-Fi暗号化プロトコル**
      - `[[WEP (Wired Equivalent Privacy)]]` (脆弱、使用禁止)
      - `[[WPA (Wi-Fi Protected Access)]]` (TKIP)
      - **[[WPA2 (Wi-Fi Protected Access 2)]]** (AES/CCMP, 現在の標準)
      - **[[WPA3 (Wi-Fi Protected Access 3)]]** (最新規格, SAE, OWE)
   - **Wi-Fi認証方式**
      - `[[PSK (Pre-Shared Key) / パーソナルモード]]`
      - `[[IEEE 802.1X/EAP / エンタープライズモード]]` (RADIUSサーバ利用)
   - **無線LANに対する攻撃**
      - `[[盗聴 (Eavesdropping)]]`
      - `[[悪魔の双子 (Evil Twin) AP]]`
      - `[[KRACKs (Key Reinstallation Attacks)]]`
      - `[[Wi-Fiパスワードのブルートフォース攻撃]]`
      - `[[Wi-Fiジャミング]]`
   - **無線LANのセキュリティベストプラクティス**
      - `[[強力な暗号化 (WPA3/WPA2) の使用]]`
      - `[[強力なパスワードの設定]]`
      - `[[SSIDのステルス化 (限定的効果)]]`
      - `[[MACアドレスフィルタリング (限定的効果)]]`
      - `[[ゲストネットワークの分離]]`
      - `[[無線LAN侵入検知・防御システム (WIDS/WIPS)]]`

## 5. [[クラウドネットワークセキュリティ MOC]]
   - **[[責任共有モデル (Shared Responsibility Model) とネットワークセキュリティ]]**
   - **[[仮想ネットワークのセキュリティ]]**
      - `[[AWS VPC セキュリティ (セキュリティグループ vs. ネットワークACL)]]`
      - `[[Azure VNet セキュリティ (ネットワークセキュリティグループ - NSG, アプリケーションセキュリティグループ - ASG)]]`
      - `[[GCP VPC セキュリティ (ファイアウォールルール)]]`
   - **クラウドネイティブなファイアウォールとWAF**
      - `[[AWS WAF, Azure WAF, Google Cloud Armor]]`
   - **クラウドのロードバランサとセキュリティ**
   - **VPC間の接続とセキュリティ**
      - `[[VPCピアリング, Transit Gateway (AWS), VNet Peering (Azure), VPC Network Peering (GCP)]]`
   - **クラウド環境におけるマイクロセグメンテーション**
   - **クラウドのネットワーク監視**
      - `[[VPCフローログ (AWS), NSGフローログ (Azure), VPCフローログ (GCP)]]`

## 6. [[ネットワークの監視とインシデント対応 MOC]]
   - **ネットワーク監視の重要性**
   - **監視対象とメトリクス**
      - `[[トラフィック量、レイテンシ、パケットロス、エラーレート]]`
      - `[[ファイアウォールやIDS/IPSのログ]]`
      - `[[フローデータ (NetFlow, sFlow)]]`
   - **[[SIEM (Security Information and Event Management) MOC]]**
      - [[ログの集中管理、相関分析、アラート]]
      - `[[主要なSIEM製品 (Splunk, QRadar, ArcSight)]]`
   - **[[PCAP (Packet Capture) 分析]]**
      - `[[Wiresharkによる詳細分析]]`
   - **[[ネットワークフォレンジック]]** (インシデント発生後の調査)
   - **インシデントレスポンス (Incident Response - IR)**
      - `[[インシデントレスポンスのライフサイクル (準備, 特定, 封じ込め, 根絶, 回復, 教訓)]]`
      - `[[IRチーム (CSIRT/CERT)]]`

## 7. [[セキュアなネットワーク設計とアーキテクチャ MOC]]
   - **多層防御アーキテクチャ** (再掲・設計観点)
   - **[[ネットワークセグメンテーション戦略 MOC]]**
      - `[[VLANによる論理的分割]]`
      - `[[サブネット分割]]`
      - `[[マイクロセグメンテーション]]` (コンテナ、仮想化環境)
      - `[[DMZの設計]]` (再掲)
   - **[[ゼロトラストネットワークアーキテクチャ (Zero Trust Network Architecture - ZTNA) MOC]]**
      - `[[ゼロトラストの基本原則 ("Never trust, always verify")]]`
      - `[[境界型セキュリティモデルとの違い]]`
      - `[[構成要素 (アイデンティティ中心, マイクロセグメンテーション, 動的なポリシー適用)]]`
      - `[[Software-Defined Perimeter (SDP)]]`
   - **リモートアクセスソリューションの設計**
   - **IoTデバイスのネットワークセキュリティ設計**
   - **IPv6セキュリティ** (概要)

## 8. [[セキュアなネットワークプロトコル MOC]] (再掲・ネットワークセキュリティ文脈)
   - **[[TLS/SSLによる通信の暗号化]]** (HTTPS, SMTPS, IMAPSなど)
   - **[[SSHによる安全なリモート管理]]**
   - **[[IPsecによるネットワーク層のセキュリティ]]** (VPNなど)
   - **[[DNSSEC (DNS Security Extensions)]]** (DNS応答の認証)
   - **[[セキュアなルーティングプロトコル (BGPsecなど)]]** (概要)
   - **[[時間同期プロトコルのセキュリティ (NTPsec)]]**

## 9. [[ネットワークセキュリティの管理と運用 MOC]]
   - **セキュリティポリシーと標準の策定**
   - **脆弱性管理プロセス**
      - `[[脆弱性スキャン]]`
      - `[[パッチマネジメント]]`
   - **構成管理と変更管理**
   - **セキュリティ意識向上トレーニング**
   - **定期的なセキュリティ監査とペネトレーションテスト**

## 10. [[ネットワークセキュリティの将来とトレンド MOC]]
   - **[[SASE (Secure Access Service Edge) と SSE (Security Service Edge)]]** (ネットワークとセキュリティのクラウド統合)
   - **AI/MLのネットワークセキュリティへの応用** (異常検知、脅威インテリジェンス)
   - **暗号化されたトラフィックの分析 (Encrypted Traffic Analysis - ETA)**
   - **5Gネットワークのセキュリティ**
   - **IoT/OTセキュリティの課題と対策**
   - **ポスト量子暗号 (PQC) のネットワークへの影響**
   - **自動化された脅威対応 (SOAR - Security Orchestration, Automation and Response)**
