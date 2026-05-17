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

---

# 目的

SansaSphere は、ProjectSansa ecosystem 全体で共通利用される user / activity / governance 基盤を提供することを目的とします。

以下のような repository から利用されることを想定しています。

- SansaXR
- SansaVRM
- SansaVRM-Studio-AI
- SansaCloth

---

# repository federation

```text
ProjectSansa
├─ ecosystem architecture
├─ federation
└─ repository map

SansaSphere
├─ account
├─ authentication
├─ profile
├─ audit
├─ logging
├─ provenance
├─ analytics
└─ economy

SansaXR
├─ XR runtime
├─ networking
└─ OpenXR

SansaVRM
├─ avatar format
├─ validator
└─ adapters
```

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
- audit / provenance / governance を重視する
