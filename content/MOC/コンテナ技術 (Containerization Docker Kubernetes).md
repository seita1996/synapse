---
tags:
  - moc
enableToc: "true"
draft: "false"
permalink: moc/containerization
---
## 1. [[コンテナ技術入門 MOC]]
   - **コンテナとは何か**
      - [[コンテナの定義 (ホストOSのカーネルを共有し、プロセスやファイルシステムを隔離する軽量な仮想化技術)]]
      - [[コンテナの目的 (環境差異の吸収、ポータビリティの確保、迅速なデプロイ)]]
   - **[[コンテナ vs. 仮想マシン (VM) の比較 MOC]]**
      - `[[アーキテクチャの違い (ハイパーバイザ vs. コンテナエンジン、OSの有無)]]`
      - `[[起動速度とパフォーマンス]]`
      - `[[リソース効率と集約度]]`
      - `[[分離レベルとセキュリティ]]`
      - `[[ユースケースの比較]]`
   - **なぜコンテナ技術が重要か**
      - `[["私のマシンでは動く"問題の解決]]`
      - `[[DevOpsとマイクロサービスアーキテクチャの実現]]`
      - `[[CI/CDパイプラインの高速化と信頼性向上]]`
      - `[[クラウドネイティブアプリケーションの基盤]]`
   - **コンテナ技術の歴史**
      - `[[chrootからJails, Solaris Zones, LXCへ]]`
      - `[[Dockerの登場とコンテナの普及]]`
   - **[[Open Container Initiative (OCI) MOC]]**
      - `[[OCIの役割 (コンテナフォーマットとランタイムの標準化)]]`
      - `[[OCI Runtime Specification (runCなど)]]`
      - `[[OCI Image Format Specification]]`

## 2. [[Docker MOC]]

### 2.1. [[Docker入門 MOC]]
   - **Dockerとは**
      - [[Dockerの概要とエコシステム]]
      - [[Docker Engine, Docker CLI, Docker Hub, Docker Compose, Docker Desktop]]
   - **[[Dockerのアーキテクチャ MOC]]**
      - `[[クライアント/サーバーアーキテクチャ (Docker CLI, Dockerデーモン)]]`
      - `[[Dockerオブジェクト (イメージ, コンテナ, ボリューム, ネットワーク)]]`
      - `[[Dockerレジストリ]]`
   - **Dockerのインストールとセットアップ**
      - `[[各OS (Windows, macOS, Linux) へのインストール]]`

### 2.2. [[Dockerイメージ (Docker Images) MOC]]
   - [[Dockerイメージの定義 (コンテナ作成のための読み取り専用テンプレート)]]
   - **[[レイヤー (Layers) とコピーオンライト (Copy-on-Write)]]**
      - [[イメージレイヤーの仕組みと効率性]]
   - **[[Dockerfile MOC]]**
      - `[[Dockerfileの役割 (イメージのビルド手順を記述するテキストファイル)]]`
      - **[[主要なDockerfile命令]]**
         - `[[`FROM` (ベースイメージの指定)]]`
         - `[[`RUN` (コマンドの実行)]]`
         - `[[`CMD` (コンテナ起動時のデフォルトコマンド)]]`
         - `[[`ENTRYPOINT` (コンテナ起動時の実行コマンド)]]` (`CMD`との違い)
         - `[[`COPY` vs. `ADD`]]`
         - `[[`WORKDIR` (作業ディレクトリの指定)]]`
         - `[[`EXPOSE` (ポートの公開)]]`
         - `[[`ENV` (環境変数の設定)]]`
         - `[[`ARG` (ビルド時引数)]]`
         - `[[`VOLUME` (ボリュームのマウントポイント)]`
         - `[[`USER` (実行ユーザーの指定)]]`
         - `[[`HEALTHCHECK`]]`
      - **[[Dockerfileのベストプラクティス]]**
         - `[[軽量なベースイメージの選択 (Alpineなど)]]`
         - `[[レイヤー数の最小化]]`
         - `[[ビルドキャッシュの活用 (命令の順序)]]`
         - `[[マルチステージビルド (Multi-stage builds)]]` (ビルド環境と実行環境の分離)
         - `[[`.dockerignore` ファイルの活用]]`
         - `[[非rootユーザーでの実行]]`
   - **イメージのビルド、管理、操作**
      - `[[`docker build`]]`
      - `[[`docker images`]]`
      - `[[`docker pull`]]`
      - `[[`docker push`]]`
      - `[[`docker tag`]]`
      - `[[`docker rmi`]]`
      - `[[`docker history`]]`
      - `[[`docker save` / `docker load`]]`

### 2.3. [[Dockerコンテナ (Docker Containers) MOC]]
   - [[Dockerコンテナの定義 (Dockerイメージの実行可能なインスタンス)]]
   - **コンテナのライフサイクル**
   - **コンテナの操作**
      - `[[`docker run`]]` (コンテナの作成と実行)
         - `[[主要なオプション (`-d`, `-it`, `-p`, `-v`, `--rm`, `--name`など)]]`
      - `[[`docker ps`]]` (実行中コンテナの一覧) (`-a`オプション)
      - `[[`docker start` / `docker stop` / `docker restart`]]`
      - `[[`docker exec -it <container_id> <command>`]]` (実行中コンテナ内でのコマンド実行)
      - `[[`docker logs`]]` (コンテナのログ表示)
      - `[[`docker inspect`]]` (コンテナの詳細情報表示)
      - `[[`docker rm`]]` (コンテナの削除)
      - `[[(オプション) `docker pause` / `docker unpause`]]`

### 2.4. [[Dockerのストレージ (Docker Storage) MOC]]
   - **コンテナの永続データ管理**
      - [[コンテナのファイルシステム (書き込み可能レイヤー) の揮発性]]
   - **[[ボリューム (Volumes)]]**
      - `[[ボリュームの概念と利点 (Dockerによる管理、永続性、共有)]]`
      - `[[名前付きボリュームと匿名ボリューム]]`
      - `[[`docker volume` コマンド]]`
   - **[[バインドマウント (Bind Mounts)]]**
      - `[[バインドマウントの概念 (ホストマシンのファイル/ディレクトリをマウント)]]`
      - `[[バインドマウントのユースケースと注意点]]`
   - **[[tmpfsマウント]]** (インメモリの一時ファイル)
   - **ボリューム vs. バインドマウントの比較と選択**

### 2.5. [[Dockerのネットワーキング (Docker Networking) MOC]]
   - **Dockerネットワークの基本**
   - **ネットワークドライバ**
      - `[[`bridge` (デフォルト)]]`
      - `[[`host`]]`
      - `[[`none`]]`
      - `[[`overlay` (Swarm向け)]]`
      - `[[`macvlan`]]`
   - **コンテナ間の通信**
      - `[[ブリッジネットワーク内でのコンテナ名による通信]]`
   - **ホストとのポートマッピング (`-p` オプション)**
   - `[[`docker network` コマンド]]`

### 2.6. [[Docker Compose MOC]]
   - [[Docker Composeの定義と目的 (複数のコンテナで構成されるアプリケーションの定義と実行)]]
   - **[[`docker-compose.yml` ファイル MOC]]**
      - `[[主要なキー (`version`, `services`, `networks`, `volumes`)]]`
      - `[[サービス定義 (`image`, `build`, `ports`, `volumes`, `environment`, `depends_on`など)]]`
   - **Docker Composeのコマンド**
      - `[[`docker-compose up`]]` (`-d`オプション)
      - `[[`docker-compose down`]]`
      - `[[`docker-compose ps`]]`
      - `[[`docker-compose logs`]]`
      - `[[`docker-compose exec`]]`
   - `[[複数コンテナアプリケーションの例 (Webサーバー + DB + キャッシュ)]]`
   - `[[開発環境としてのDocker Compose]]`

## 3. [[コンテナオーケストレーション (Container Orchestration) MOC]]
   - **なぜコンテナオーケストレーションが必要か**
      - `[[多数のコンテナの管理とライフサイクル]]`
      - `[[スケーリングと負荷分散]]`
      - `[[可用性と自己修復]]`
      - `[[サービスディスカバリ]]`
      - `[[デプロイメントの自動化]]`
   - **コンテナオーケストレーションツールの比較**
      - `[[Kubernetes]]` (デファクトスタンダード)
      - `[[Docker Swarm]]` (シンプルさ)
      - `[[Amazon ECS]]` (AWS統合)
      - `[[HashiCorp Nomad]]` (シンプル、柔軟)

## 4. [[Kubernetes (K8s) MOC]]

### 4.1. [[Kubernetes入門 MOC]]
   - **Kubernetesとは**
      - `[[Kubernetesの定義と目的 (コンテナ化されたアプリケーションのデプロイ、スケーリング、管理を自動化するオープンソースプラットフォーム)]]`
      - `[[Kubernetesの歴史 (Google Borgからの進化)]]`
      - `[[宣言的APIと制御ループ]]`
   - **Kubernetesの基本概念**
      - `[[クラスタ (Cluster)]]`
      - `[[ノード (Node - Master/Control Plane, Worker)]]`
      - `[[ポッド (Pod)]]` (基本デプロイ単位)
      - `[[サービス (Service)]]` (ネットワーク抽象化)
      - `[[デプロイメント (Deployment)]]` (宣言的なアプリケーション管理)
   - **開発環境のセットアップ**
      - `[[kubectl (コマンドラインツール)]]`
      - `[[Minikube, kind, Docker Desktop Kubernetes (ローカルクラスタ)]]`

### 4.2. [[Kubernetesのアーキテクチャ MOC]]
   - **[[コントロールプレーン (Control Plane) のコンポーネント MOC]]**
      - `[[APIサーバー (kube-apiserver)]]`
      - `[[etcd (分散キーバリューストア)]]`
      - `[[スケジューラ (kube-scheduler)]]`
      - `[[コントローラーマネージャー (kube-controller-manager)]]`
      - `[[クラウドコントローラーマネージャー (cloud-controller-manager)]]`
   - **[[ワーカーノード (Worker Node) のコンポーネント MOC]]**
      - `[[kubelet]]`
      - `[[kube-proxy]]`
      - `[[コンテナランタイム (Container Runtime - containerd, CRI-O)]]`

### 4.3. [[Kubernetesの主要なオブジェクト (Core Kubernetes Objects) MOC]]
   - **オブジェクトの管理** (`[[YAMLマニフェストファイル]]`, `[[kubectl apply`]]`)
   - **[[ワークロード (Workloads) MOC]]**
      - **[[Pod (ポッド)]]**
         - `[[Podの概念 (1つ以上のコンテナのグループ、共有ストレージ/ネットワーク)]]`
         - `[[Podのライフサイクル]]`
         - `[[Podの定義 (YAML)]]`
      - **[[ReplicaSet]]**
      - **[[Deployment]]**
         - `[[宣言的なPodとReplicaSetの管理]]`
         - `[[ローリングアップデートとロールバック]]`
      - **[[StatefulSet]]** (ステートフルアプリケーション向け)
      - **[[DaemonSet]]** (全ノードでPodを実行)
      - **[[Job と CronJob]]** (バッチ処理、スケジュール実行)
   - **[[サービスディスカバリとネットワーク MOC]]**
      - **[[Service (サービス)]]**
         - `[[Serviceの役割 (Podへの安定したエンドポイント)]]`
         - `[[Serviceの種類 (`ClusterIP`, `NodePort`, `LoadBalancer`, `ExternalName`)]]`
      - `[[Headless Service]]`
      - **[[Ingress (イングレス)]]**
         - `[[HTTP/HTTPSルーティング、TLS終端、負荷分散]]`
         - `[[Ingress Controller]]` (Nginx Ingress, Traefikなど)
      - `[[Endpoint / EndpointSlice]]`
      - `[[NetworkPolicy]]` (Pod間の通信制御)
      - `[[KubernetesのDNS]]`
   - **[[ストレージ (Storage) MOC]]**
      - `[[Volume]]` (Pod内のコンテナ間データ共有)
         - `[[emptyDir, hostPath, configMap, secretなど]]`
      - **[[PersistentVolume (PV) と PersistentVolumeClaim (PVC)]]**
         - `[[永続ストレージの抽象化と動的プロビジョニング]]`
      - **[[StorageClass]]**
   - **[[コンフィギュレーションとシークレット MOC]]**
      - **[[ConfigMap]]** (設定データの管理)
      - **[[Secret]]** (機密データの管理)
      - `[[環境変数やボリュームとしてのマウント]]`

### 4.4. [[Kubernetesの運用と管理 MOC]]
   - **[[kubectl コマンドリファレンス MOC]]**
      - `[[`kubectl get`, `describe`, `logs`, `exec`, `apply`, `delete`など]]`
      - `[[コンテキストとネームスペース]]`
   - **[[ヘルスチェック (Health Checks)]]**
      - `[[Liveness Probe, Readiness Probe, Startup Probe]]`
   - **[[リソース要求 (Requests) と制限 (Limits)]]**
      - `[[CPUとメモリのリソース管理]]`
      - `[[Quality of Service (QoS) クラス (Guaranteed, Burstable, BestEffort)]]`
   - **[[Horizontal Pod Autoscaler (HPA)]]** (Podの自動スケーリング)
   - **ロギングとモニタリング**
      - `[[Kubernetesのロギングアーキテクチャ]]`
      - `[[PrometheusとGrafanaによるモニタリング]]`
      - `[[Fluentd/Fluent Bitによるログ収集]]`
   - **クラスタのアップグレード**

### 4.5. [[Kubernetesのツールとエコシステム MOC]]
   - **[[Helm (パッケージマネージャ)]]**
      - `[[Chart, Release, Repository]]`
   - **[[Kustomize (マニフェストのカスタマイズ)]]**
   - **[[Argo CD / Flux (GitOpsツール)]]**
   - **[[Istio / Linkerd (サービスメッシュ)]]**
   - **[[Knative (サーバーレス)]]**
   - **クラウドプロバイダーのマネージドKubernetesサービス** (EKS, AKS, GKE)

### 4.6. [[Kubernetesのセキュリティ MOC]]
   - **Kubernetesセキュリティの4C** (Cloud, Cluster, Container, Code)
   - **[[RBAC (Role-Based Access Control)]]** (`Role`, `ClusterRole`, `RoleBinding`, `ClusterRoleBinding`)
   - **[[Pod Security Standards / Pod Security Policies (非推奨)]]**
   - **[[NetworkPolicyによる通信制御]]** (再掲)
   - **[[Secretの暗号化と管理]]** (Vault連携など)
   - **コンテナイメージのセキュリティ** (脆弱性スキャン)
   - **コントロールプレーンのセキュリティ**
   - **[[(オプション) OPA (Open Policy Agent) / Gatekeeperによるポリシ制御]]**

## 5. [[コンテナレジストリ (Container Registries) MOC]]
   - [[コンテナレジストリの役割 (Dockerイメージの保存と配布)]]
   - **パブリックレジストリ**
      - `[[Docker Hub]]`
   - **プライベートレジストリ**
      - `[[セルフホスト型 (Harbor, Docker Registry)]]`
      - **クラウドプロバイダーのレジストリ**
         - `[[Amazon ECR (Elastic Container Registry)]]`
         - `[[Azure Container Registry (ACR)]]`
         - `[[Google Artifact Registry]]`
         - `[[GitHub Packages]]`
   - [[レジストリのセキュリティ]] (脆弱性スキャン、アクセス制御)

## 6. [[コンテナセキュリティ (全体像) MOC]]
   - **ビルド時のセキュリティ**
      - `[[ベースイメージの信頼性確保]]`
      - `[[脆弱性スキャン (SCA - Software Composition Analysis)]]`
      - `[[Dockerfileのセキュリティベストプラクティス]]` (非rootユーザーなど)
   - **デプロイ時のセキュリティ**
      - `[[コンテナレジストリのセキュリティ]]`
      - `[[オーケストレータのセキュリティ設定 (RBAC, NetworkPolicyなど)]]`
   - **ランタイム時のセキュリティ**
      - `[[コンテナランタイムセキュリティ (gVisor, Kata Containers)]]`
      - `[[コンテナサンドボックス]]`
      - `[[ランタイムセキュリティ監視 (Falco, Sysdig Secure)]]`
      - `[[ホストOSのセキュリティ強化]]`
   - **コンテナセキュリティのベストプラクティスまとめ**

## 7. [[コンテナとCI/CD MOC]]
   - [[CI/CDパイプラインにおけるコンテナの役割]]
   - **ビルドステージ**
      - `[[Dockerイメージのビルドとプッシュ]]`
   - **テストステージ**
      - `[[テスト環境のコンテナ化]]`
      - `[[インテグレーションテストでのDocker Compose利用]]`
   - **デプロイステージ**
      - `[[Kubernetesへの自動デプロイ]]`
      - `[[ブルー/グリーンデプロイメント、カナリアリリースの実現]]`
   - [[CI/CDツール (Jenkins, GitLab CI, GitHub Actions) との連携]]

## 8. [[サーバーレスコンテナ MOC]]
   - [[サーバーレスとコンテナの融合]]
   - **主なサービス**
      - `[[AWS Fargate]]`
      - `[[Azure Container Instances (ACI)]]`
      - `[[Google Cloud Run]]`
   - [[FaaSとの比較]]
   - [[サーバーレスコンテナのユースケース]]

## 9. [[コンテナ技術の将来とトレンド MOC]]
   - `[[WebAssembly (Wasm) とコンテナの共存・融合]]`
   - `[[コンテナセキュリティの進化 (eBPFなど)]]`
   - `[[エッジコンピューティングにおけるコンテナ]]`
   - `[[AI/MLワークロードのコンテナ化 (Kubeflowなど)]]`
   - `[[開発環境のコンテナ化 (Dev Containers, Gitpod, GitHub Codespaces)]]`
   - `[[Rootlessコンテナ]]`
