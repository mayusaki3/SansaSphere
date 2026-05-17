[目次](../README.md) > docs/ja-JP > 申し送り > SansaSphere 分割方針

# SansaSphere 分割方針

## 1. 概要

SansaSphere は、ProjectSansa ecosystem における ecosystem-level infrastructure を担う repository として整理を進める。

主に以下を扱う。

- account
- authentication
- profile
- audit
- logging
- provenance
- analytics
- governance
- economy
- federation identity
- usage visibility

---

## 2. 基本方針

SansaSphere は ecosystem-wide infrastructure を扱うが、単一 repository にすべてを集中させる monorepo 化は避ける。

そのため、必要に応じて以下のような repository federation 構成へ分離する前提で設計を進める。

```text
SansaSphere
SansaSphere-Auth
SansaSphere-Audit
SansaSphere-Logging
SansaSphere-Provenance
SansaSphere-Analytics
SansaSphere-Economy
SansaSphere-Federation
```

SansaSphere は ecosystem-level hub repository として扱い、各 repository を federation する。

---

## 3. repository federation

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

## 4. federation trust 方針

複数人が構築した SansaSphere 間で、audit / provenance / verification を共有できる構成を目指す。

### 想定内容

- signed audit event
- hash chain
- distributed verification
- provenance verification
- ownership verification
- moderation trace
- distributed timestamp

### 基本方針

全文ログ共有ではなく、以下を中心とする。

- hash
- signature
- minimal metadata

これにより、改ざん検出や distributed trust を実現する。

---

## 5. SansaXR との関係

```text
SansaXR
 └─ depends on SansaSphere
```

SansaXR は XR runtime repository として整理し、user / audit / provenance infrastructure は直接保持しない。

---

## 6. SansaVRM / Studio AI との関係

SansaSphere は以下とも連携する。

### SansaVRM

- ownership
- provenance
- creator identity
- conversion history

### SansaVRM-Studio-AI

- AI generation trace
- creator analytics
- asset provenance
- generation history
- rights trace

---

## 7. Cassandra / Web Service 方針

SansaSphere は service platform repository として、以下を主責務に含む。

- Web services
- Cassandra
- account management
- audit database
- logging infrastructure
- dashboard
- analytics

これらは XR runtime 固有ではなく ecosystem-wide infrastructure として扱う。

---

## 8. 今後の整理

### Phase 1

- responsibility 定義
- repository federation 整理
- handover document 作成

### Phase 2

- auth / logging / audit 分離
- provenance 分離
- analytics 分離

### Phase 3

- federation trust 強化
- distributed verification 強化
- ecosystem governance 統合

---

[目次](../README.md) > docs/ja-JP > 申し送り > SansaSphere 分割方針