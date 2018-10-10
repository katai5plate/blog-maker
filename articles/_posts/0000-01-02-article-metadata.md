---
title: ページのメタデータ一覧
description: 記事や固定ページのMarkdownファイルの最初に記述可能なメタデータの一覧
image: machine
genre: Tips
tags: [リファレンス]
hashtags: [Jekyll]
---

# 共通
## 必須項目
### title
- ページのタイトル
### description
- ページの説明
## 任意項目(省略可)
### image
- ヘッダー画像識別名 または 画像URL
- 入力例: `image: random` `image: https://source.unsplash.com/random/400x200`
### hashtags
- ツイート時のハッシュタグ
- 入力例: `hashtags: [Windows, Mac, Linux]`
### permalink
- 強制的にURLを変更したい場合に使用
- 入力例: `permalink: /404.html` `permalink: /hoge/huga/index.html`

# 記事
## 必須項目
### genre
- 記事のカテゴリ名
### tags
- 記事のタグ名
- 入力例: `tags: [Windows, Mac, Linux]`
