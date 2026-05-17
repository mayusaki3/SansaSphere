[README](../../../README.md) > docs/ja-JP > 01_要件定義

# 01_要件定義

## 概要

SansaSphere は、Project Sansa における共通バックエンド基盤サービスを提供するシステムである。

主に以下を責務とする。

- ユーザー認証
- セッション管理
- アカウント管理
- Webサービス基盤
- サーバー基盤
- 共通バックエンド機能
- Federation / Identity
- ログ・監査
- API基盤
- テスト基盤
- VN3 license 管理
- governance / provenance 管理

SansaSphere は、XR Runtime やゲームエンジン本体ではなく、
Project Sansa 全体を支えるバックエンド・サービス基盤を責務とする。

## 目的

SansaSphere の目的は、Project Sansa 全体で利用可能な共通バックエンド基盤を提供することである。

以下を主目的とする。

- 共通認証基盤の提供
- 共通アカウント管理の提供
- サービス間連携基盤の提供
- 共通API基盤の提供
- セキュアなセッション管理
- Federation / Identity 管理
- 共通監査・ロギング
- 共通テスト基盤
- 運用・監視基盤の統一
- 権利違反防止
- ライセンス整合性維持
- provenance / governance 管理

## 責務

### 認証・認可

- ログイン
- ログアウト
- セッション管理
- MFA
- WebAuthn
- Access Control
- Federation
- Token 管理

### ユーザー管理

- アカウント
- プロフィール
- Activity
- Visibility
- User Settings
- ユーザー状態管理

### Webサービス基盤

- REST API
- API Gateway
- Backend Services
- 共通エラーモデル
- 共通レスポンスモデル
- API Versioning

### 共通基盤

- Logging
- Audit
- Configuration
- DI
- Monitoring
- Metrics
- Traceability

### ライセンス・権利管理

- VN3 license 管理
- Rights metadata 管理
- License validation
- Provenance tracking
- Governance policy enforcement
- Asset usage visibility
- Federation policy coordination

### テスト基盤

- 単体テスト
- 結合テスト
- テストマトリクス
- 共通テストライブラリ
- テスト支援基盤

### サーバー基盤

- 開発環境
- 本番環境
- デプロイ
- 運用
- CI/CD
- Infrastructure

## 非責務

以下は SansaSphere の主責務ではない。

- O3DE Runtime
- OpenXR Runtime
- World Simulation
- Avatar Runtime
- Rendering Engine
- VR Runtime
- 3D Asset Runtime
- ゲームエンジン制御
- XR描画処理

これらは別システムまたは別リポジトリで管理する。

## 今後整理予定

今後、以下を要件定義から詳細化する。

- API仕様
- ドメイン仕様
- 共通仕様
- テスト仕様
- サーバー仕様
- 運用仕様
- governance / provenance 仕様
- VN3 license 仕様

現在は要点整理段階のため、目次から各詳細ドキュメントへのリンクは作成しない。

---

[README](../../../README.md) > docs/ja-JP > 01_要件定義