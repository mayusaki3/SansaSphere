[目次](../README.md) > docs/ja-JP > 申し送り > SansaXR からの移管

# SansaXR からの移管

## 1. 概要

SansaSphere は、ProjectSansa ecosystem における ecosystem-level infrastructure repository として整理を進める。

SansaXR から、account / audit / logging / provenance / analytics 系統を移管する。

---

## 2. 受け入れ対象

### account / identity

- user account
- authentication
- federation identity
- profile
- session metadata

### audit / logging

- audit
- access log
- activity log
- moderation log
- operation trace
- distributed trace

### provenance / governance

- provenance
- ownership trace
- asset usage history
- creator history
- conversion history
- AI generation trace

### analytics / visibility

- dashboard
- usage visibility
- activity analytics
- creator analytics
- economy analytics

---

## 3. repository role

SansaSphere は以下を主責務とする。

- ecosystem-level infrastructure
- identity
- governance
- audit
- provenance
- analytics
- economy

runtime implementation は直接保持しない。

---

## 4. 他 repository との関係

```text
SansaXR
 └─ depends on SansaSphere

SansaVRM
 └─ depends on SansaSphere

SansaVRM-Studio-AI
 └─ depends on SansaSphere
```

SansaSphere は ecosystem-wide service infrastructure として扱う。

---

## 5. 目的

以下を実現する。

- ecosystem-wide identity
- audit integration
- provenance integration
- creator analytics
- usage visibility
- governance integration
- economy integration
- moderation integration

---

## 6. 今後の整理

### Phase 1

- responsibility 定義
- repository federation 更新
- handover document 作成

### Phase 2

- auth / audit / logging 再配置
- provenance 再配置
- analytics 再配置

### Phase 3

- ecosystem-wide infrastructure 統合
- cross-repository governance 強化

---

[目次](../README.md) > docs/ja-JP > 申し送り > SansaXR からの移管