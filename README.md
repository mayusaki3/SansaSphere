# SansaSphere

SansaSphere は、ProjectSansa ecosystem における account / profile / audit / logging / provenance 基盤を担う repository です。

SansaSphere では、XR runtime に依存しない ecosystem-level service infrastructure を扱います。

---

# 主な責務

- account
- authentication
- profile
- audit
- logging
- provenance
- analytics
- moderation
- economy
- federation identity
- usage visibility
- governance
- federation trust

---

# 目的

SansaSphere は、ProjectSansa ecosystem 全体で共通利用される user / activity / governance 基盤を提供することを目的とします。

以下のような repository から利用されることを想定しています。

- SansaXR
- SansaVRM
- SansaVRM-Studio-AI
- SansaCloth

また、複数人が構築した SansaSphere 間で、audit / provenance / verification を共有できる federation trust 基盤を目指します。

---

# repository federation

```text
ProjectSansa
├─ ecosystem architecture
├─ federation
└─ repository map

SansaSphere
├─ federation hub
├─ repository coordination
├─ common specifications
└─ ecosystem governance

SansaSphere-Auth
├─ account
├─ authentication
└─ identity

SansaSphere-Audit
├─ audit
├─ moderation trace
└─ operation trace

SansaSphere-Logging
├─ logging
├─ distributed trace
└─ event collection

SansaSphere-Provenance
├─ provenance
├─ ownership trace
├─ creator history
└─ conversion history

SansaSphere-Analytics
├─ dashboard
├─ creator analytics
├─ usage analytics
└─ activity visibility

SansaSphere-Economy
├─ economy
├─ asset usage
├─ transaction trace
└─ ownership management

SansaSphere-Federation
├─ federation trust
├─ signed event
├─ verification
└─ distributed trust
```

---

# federation trust

SansaSphere では、改ざん検出や distributed trust を目的として、以下のような federation trust を扱う。

- signed audit event
- hash chain
- distributed verification
- provenance verification
- ownership verification
- distributed timestamp

全文ログ共有ではなく、以下を中心とする。

- hash
- signature
- minimal metadata

---

# dependency direction

```text
ProjectSansa
 ├─ SansaSphere
 │
 ├─ SansaXR
 │   └─ depends on SansaSphere
 │
 ├─ SansaVRM
 │   └─ depends on SansaSphere
 │
 ├─ SansaVRM-Studio-AI
 │   └─ depends on SansaSphere
 │
 └─ SansaCloth
     └─ depends on SansaSphere
```

SansaSphere は ecosystem-level infrastructure として扱う。

---

# ドキュメント

## 日本語ドキュメント目次

- [docs/ja-JP/目次.md](./docs/ja-JP/目次.md)

---

# 開発方針

- ドキュメントは HLDocS ベースで管理
- 仕様・テスト・コードの Traceability を重視
- ecosystem-level infrastructure を主責務とする
- runtime implementation を直接保持しない
- monorepo 化を避ける
- repository federation を前提とする
- audit / provenance / governance を重視する
- federation trust を重視する
