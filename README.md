# mash3gt.github.io

## 目的

このリポジトリは、活動の入口となる Hub サイトです。
note、個人開発（AWS 側）、YouTube などの外部ページへの導線を集約します。

## 公開 URL

- https://mash3gt.github.io/

## 技術スタック

- HTML / CSS（ビルドなし）
- JavaScript（必要最小限）

## 運用フロー

1. Issue を作成（1 Issue = 1 変更）
2. Copilot / Agent に PR 作成を依頼
3. PR 差分を確認して承認・マージ
4. main 反映後に Pages 公開を確認

## セキュリティ方針

- API キー、トークン、個人情報はコミットしない
- 外部リンクで target="_blank" を使う場合は rel="noopener noreferrer" を付与
- 外部 script の埋め込みは原則最小化し、必要時のみ採用

## 更新手順（最短）

1. index.html のリンク・文言を更新
2. PR を作成してレビュー
3. main へマージ
4. 公開 URL を PC / スマホで確認

## ディレクトリ構成

- index.html: トップページ
- README.md: この説明
- js/sample_javascript.js: 補助 JavaScript
- images/: 画像アセット

## 現在の方針

- Hub 用途に特化
- おみくじ / Sandbox 機能は廃止方向
- アクセスカウンターは導入しない
