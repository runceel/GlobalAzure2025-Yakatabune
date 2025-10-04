---
marp: true
theme: default
paginate: true
header: "第7回 Azure Travelers 勉強会 東京の旅の前夜祭(屋台船で LT 大会)"
---

# Agent 作るときに何を選べばいいの…

2025/10/03
Kazuki Ota

---

<!-- _class: split -->

## 自己紹介

![bg right:35%](https://storage.googleapis.com/zenn-user-upload/avatar/8f78742c44.jpeg)

### Kazuki Ota (大田 一希)

- 日本マイクロソフトで働いています
- X(Twitter): [@okazuki](https://x.com/okazuki)
- GitHub: [@runceel](https://github.com/runceel)
- Zenn: [zenn.dev/okazuki](https://zenn.dev/okazuki)
- Blog: [blog.okazuki.jp](https://blog.okazuki.jp)

**好きなもの**
- 言語: C#
- クラウド: Azure
- その他: ASP.NET Core Blazor, Agent Framework

---

## Agent 開発の選択肢

本日紹介する5つのフレームワーク・ツール

1. **Microsoft Agent Framework**
2. **Semantic Kernel**
3. **AutoGen**
4. **Microsoft 365 Agents Toolkit**
5. **Microsoft 365 Agents SDK**

---

## 1. Microsoft Agent Framework

- **.NET/Python 対応**の公式 Agent フレームワーク
- Azure AI Foundry Agent、Azure OpenAI、OpenAI などに対応
- シンプルな Agent からカスタム Agent まで幅広く対応
- 複数の推論サービスをサポート

**特徴**
- 関数呼び出し
- マルチターン会話
- 構造化出力

---

## 2. Semantic Kernel

- **C#/Python/Java 対応**のエンタープライズ AI SDK
- Microsoft Agent Framework と統合可能
- プラグインシステムによる拡張性
- エンタープライズ対応（本番サポート、非破壊的変更）

**特徴**
- モジュラーな Agent コンポーネント
- Agent 間の協調動作
- プロセスオーケストレーション

---

## 3. AutoGen

- **Microsoft Research 製**のマルチエージェント研究 SDK
- **Python 対応**
- 最先端の Agent コラボレーションパターンを研究
- Azure AI Foundry Agent Service と互換性あり

**特徴**
- マルチエージェントシステム
- 自律的なワークフロー
- 研究段階の機能を試せる

---

## 4. Microsoft 365 Agents Toolkit

- **VS Code/Visual Studio 拡張機能**
- Agent/アプリのスキャフォールディング、テスト、デプロイ
- 旧 Teams Toolkit の進化版
- **Microsoft 365 Agents Playground** で簡単にテスト可能

**特徴**
- プロジェクトテンプレート
- ローカルデバッグ環境
- CI/CD 統合サポート

---

## 5. Microsoft 365 Agents SDK

- **フルスタック、マルチチャネル** Agent 構築用 SDK
- M365 Copilot、Teams、Web など複数チャネルに対応
- Semantic Kernel、LangChain などと統合可能
- **C#/JavaScript/Python 対応**

**特徴**
- モデル・オーケストレーター非依存
- カスタムオーケストレーション
- Agent 間通信のサポート

---

# で、どれを使えばいいの？？？

---

## 意外な事実！

### Microsoft 365 Agents SDK は...

**AI とやりとりする機能がない！**

M365 Agents SDK は、マルチチャネル展開のためのフレームワークであって、
AI のオーケストレーション機能は**含まれていない**

つまり...
- AI の実装には **Semantic Kernel** や **LangChain** などが必要
- M365 Agents SDK は「チャネル統合」を担当
- AI 処理は別のフレームワークと組み合わせる

---
