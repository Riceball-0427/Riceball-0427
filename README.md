# Ichiro Shimamoto (Riceball-0427) 👋

<p align="center">
  <img src="https://readme-typing-svg.demolab.com?font=Outfit&size=24&pause=1000&color=7aa2f7&background=00000000&width=550&height=45&vCenter=true&lines=Hello%2C+I'm+Ichiro+Shimamoto!+👋;Aspiring+Infrastructure+Engineer+🛠️;Security+Specialist+in+Training+🛡️" alt="Typing SVG" />
</p>

<p align="center">
  <strong>Proxmox VEやVPS、Dockerコンテナを用いたインフラ構築・サービス開発を楽しむ専門職大学生 / 見習いインフラエンジニア</strong>
</p>

<p align="center">
  <a href="https://github.com/Riceball-0427">
    <img src="https://komarev.com/ghpvc/?username=Riceball-0427&color=7aa2f7&style=flat-square&label=PROFILE+VIEWS" alt="Profile Views" />
  </a>
</p>

---

## 🙋‍♂️ About Me

高校時代にはゲーム系のプログラミングを学んでいましたが、そこからインフラ、ネットワーク、そしてセキュリティの深さに強く惹かれ、現在は情報系の専門職大学で情報セキュリティを専攻しています！

自宅の **Proxmox VE** によるプライベートクラウドや、各種レンタルVPS上で **Docker** コンテナを用いたサービス構築・運用を行い、日夜「動くインフラ」を創る楽しさに没頭しています。

- 🎓 **学業**: 情報系専門職大学（セキュリティ分野専攻）
- 🛡️ **興味領域**: ネットワークセキュリティ、アイデンティティ管理（IdP/OIDC/SAML）、コンテナオーケストレーション、ホームラボ構築
- 🚀 **モットー**: 「エンジニアでなくても直感的・安全に保守運用できるインフラ・プラットフォームの実現」

---

## 🛠️ Tech Stack & Skills

> シックなパステルカラーで統一されたモダンなスキルセットです。

### 🌐 Infrastructure & DevOps
<p align="left">
  <img src="https://img.shields.io/badge/Proxmox_VE-e0af68?style=flat-square&logo=proxmox&logoColor=white" alt="Proxmox" />
  <img src="https://img.shields.io/badge/Docker-73daca?style=flat-square&logo=docker&logoColor=white" alt="Docker" />
  <img src="https://img.shields.io/badge/Tailscale-7aa2f7?style=flat-square&logo=tailscale&logoColor=white" alt="Tailscale" />
  <img src="https://img.shields.io/badge/Cloudflare_Tunnel-e0af68?style=flat-square&logo=cloudflare&logoColor=white" alt="Cloudflare" />
  <img src="https://img.shields.io/badge/Caddy-bb9af3?style=flat-square&logo=caddy&logoColor=white" alt="Caddy" />
  <img src="https://img.shields.io/badge/OpenStack-f7768e?style=flat-square&logo=openstack&logoColor=white" alt="OpenStack" />
  <img src="https://img.shields.io/badge/GitHub_Actions-73daca?style=flat-square&logo=githubactions&logoColor=white" alt="GitHub Actions" />
  <img src="https://img.shields.io/badge/Linux_Ubuntu-e0af68?style=flat-square&logo=ubuntu&logoColor=white" alt="Ubuntu" />
</p>

### 🔑 Security & Identity
<p align="left">
  <img src="https://img.shields.io/badge/Keycloak-bb9af3?style=flat-square&logo=keycloak&logoColor=white" alt="Keycloak" />
  <img src="https://img.shields.io/badge/OAuth_2.0_%2F_OIDC-7aa2f7?style=flat-square&logo=openid&logoColor=white" alt="OIDC" />
  <img src="https://img.shields.io/badge/SAML_2.0-73daca?style=flat-square&logo=lock&logoColor=white" alt="SAML" />
</p>

### 💻 Languages & Frameworks
<p align="left">
  <img src="https://img.shields.io/badge/TypeScript-7aa2f7?style=flat-square&logo=typescript&logoColor=white" alt="TypeScript" />
  <img src="https://img.shields.io/badge/Go-73daca?style=flat-square&logo=go&logoColor=white" alt="Go" />
  <img src="https://img.shields.io/badge/Python-bb9af3?style=flat-square&logo=python&logoColor=white" alt="Python" />
  <img src="https://img.shields.io/badge/Next.js-1e2030?style=flat-square&logo=nextdotjs&logoColor=white" alt="Next.js" />
  <img src="https://img.shields.io/badge/NestJS-e0af68?style=flat-square&logo=nestjs&logoColor=white" alt="NestJS" />
  <img src="https://img.shields.io/badge/PostgreSQL-7aa2f7?style=flat-square&logo=postgresql&logoColor=white" alt="PostgreSQL" />
</p>

---

## 🚀 Featured Projects (注力した代表作)

採用選考やポートフォリオとしてアピールしたい、技術的工夫を凝らした主要プロジェクトです。

### 1. 🔑 OmusuBI (Open Source Identity Orchestrator)
> 独立したIDプロバイダー（IdP）や認証プロトコルをひとつのコントロールプレーンに統合するID認証ポータル基盤

| 項目 | 内容 |
| :--- | :--- |
| **概要** | 複雑な認証プロトコル（OIDC, SAML, LDAP等）を裏側に隠蔽し、非エンジニアの運用担当者でもWeb画面から直感的にユーザー管理、権限アサイン、コンテキストポリシー（接続元、MFA強度などによる制御）を保守・管理できるようにしたID連携オーケストレーターです。 |
| **使用技術** | **Keycloak**, **Go**, OpenID Connect, SAML 2.0, **Caddy (Forward Auth)**, **Tailscale**, **Cloudflare Tunnel**, Proxmox VE |
| **インフラ工夫点** | ポート開放を行えないセキュアなプライベートクラウド（Proxmox）環境から、Cloudflare TunnelとTailscaleのメッシュネットワークを駆使して外部VPS（OpenStack）上のWebアプリへ安全にID連携（SAML Federation）するトポロジーを設計・実装しました。 |

### 2. 📦 CNT-Connect (Unified IT Assets & Provisioning Platform)
> 社内備品管理、キッティング、MDMを統合し、リソース管理コストを削減する管理ポータル

| 項目 | 内容 |
| :--- | :--- |
| **概要** | 各企業で個別管理されがちなPC・デバイスなどの社内ハードウェア備品管理と、それらに紐づくMDM（モバイルデバイス管理）や自動キッティングプロビジョニングシステムをワンストップで統合・一元管理できるWebプラットフォームです。 |
| **使用技術** | **TypeScript**, **React**, **Next.js**, **NestJS (Node.js)**, **PostgreSQL**, **Docker**, Playwright (E2Eテスト) |
| **開発/インフラ工夫点** | **npm workspaces**を用いたモノレポ構成を採用し、スキーマ定義やAPIコントラクトを共通化してチーム開発の生産性を向上。Dockerを用いたローカル・ステージング検証環境の整備に加え、**Playwright**を活用したCIテストの自動化によりリリースの信頼性を高めました。 |

---

## 📊 GitHub Contribution & Stats

### 🗺️ 3D Contribution Graph
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="profile-3d-contrib/profile-night-rainbow.svg" />
    <source media="(prefers-color-scheme: light)" srcset="profile-3d-contrib/profile-season-animate.svg" />
    <img alt="3D Contribution Graph" src="profile-3d-contrib/profile-season-animate.svg" />
  </picture>
</p>

### 👾 Contribution Snake Game
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="https://raw.githubusercontent.com/Riceball-0427/Riceball-0427/output/github-contribution-grid-snake-dark.svg" />
    <source media="(prefers-color-scheme: light)" srcset="https://raw.githubusercontent.com/Riceball-0427/Riceball-0427/output/github-contribution-grid-snake.svg" />
    <img alt="Contribution Snake" src="https://raw.githubusercontent.com/Riceball-0427/Riceball-0427/output/github-contribution-grid-snake.svg" />
  </picture>
</p>

### 📈 Metrics & Stats
<p align="center">
  <picture>
    <source media="(prefers-color-scheme: dark)" srcset="output/metrics.svg" />
    <source media="(prefers-color-scheme: light)" srcset="output/metrics.svg" />
    <img alt="GitHub Metrics" src="output/metrics.svg" />
  </picture>
</p>

---

## 📬 Connect & Contact

気になる技術のお話や、インフラ・セキュリティに関する議論など、お気軽にご連絡ください！

- 📝 **ブログ**: [Note](https://note.com/riceball_0427)
- 🐦 **X (Twitter)**: [@ONIGIRI15236050](https://x.com/ONIGIRI15236050)
- 💚 **Qiita**: [@Riceball-0427](https://qiita.com/Riceball-0427)
- 💙 **Zenn**: [@riceball_5427](https://zenn.dev/riceball_5427)
- 📸 **Instagram**: [@riceball_5427](https://www.instagram.com/riceball_5427)
- 📘 **Facebook**: [riceball5427](https://www.facebook.com/riceball5427)
- 📧 **メール**: [info@nigiri-rice.com](mailto:info@nigiri-rice.com)

---

<p align="center">
  <em>Thank you for visiting my profile! Happy Hacking 💻</em>
</p>
