[README](../../../README.md) > docs/ja-JP > 申し送り > HLDocS階層リンク起点整理

# HLDocS階層リンク起点整理

## 背景

SansaSphere のドキュメント整理において、`docs/ja-JP/目次.md` の階層リンク起点を検討した。

従来の以下の形式:

- `[目次](./目次.md)`

では、目次自身への自己参照となり、GitHub 上の repository navigation と整合しにくい問題があった。

## 検討結果

GitHub repository の入口である repository root `README.md` を起点とする構成を採用した。

例:

- `[README](../../README.md) > docs/ja-JP > 目次`
- `[README](../../../README.md) > docs/ja-JP > 01_要件定義`

## 理由

- GitHub UI の導線と一致する
- repository root を入口として統一できる
- docs 配下自己参照を避けられる
- 多言語構成との整合性が高い
- repository federation 運用と整合しやすい

## HLDocS仕様への申し送り

HLDocS では、階層リンクの起点定義を明文化する必要がある。

検討対象:

- repository root README 起点
- docs 配下目次起点
- 階層別 README 起点
- document_type 別起点

少なくとも GitHub repository 運用では、repository root README を主要入口として扱うケースが多いため、HLDocS仕様での正式化を検討する。

## SansaSphere 暫定運用

SansaSphere では、以下を暫定ルールとする。

- `docs/ja-JP/目次.md` は repository root README 起点とする
- 子ドキュメントも repository root README 起点とする
- docs 内自己参照リンクは避ける

---

[README](../../../README.md) > docs/ja-JP > 申し送り > HLDocS階層リンク起点整理