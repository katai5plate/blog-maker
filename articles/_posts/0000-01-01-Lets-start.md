---
title: Let's Start
description: とりあえずスタートする方法
image: vista
genre: Tutorial
tags: [Basic, StartUp, Usage, 日本語]
hashtags: [blogmaker]
---

# ざっくりチュートリアル

## まずはブログをWEBで見れるようにしてみる
1. プロジェクトを `Folk` する
2. `Settings` を開き、<br>
`Options` -> `GitHub Pages` -> `Source` のプルダウンから<br>
`master branch` を選んで `Save` を押す
3. 緑の枠で ` Your site is published at https://*****.github.io/blog-maker/`<br>
というようなメッセージが出たら成功。<br>
表示されたURLが公開先なので、アクセスしてみよう。

## 新たな記事を書いてみる
1. `articles/_posts/` を開く
2. 以下の法則に基づいた名前のファイルを作成
```
2020-07-24-tokyo-olympic.md
年4桁-月2桁-日2桁-ハイフン区切り題名.md
```
3. 以下のメタデータをファイルの最初に書き込む
```yml
---
title: ここに記事のタイトル
description: ここに記事の説明
image: random か books か vista か machine か 任意のURL
genre: ここに記事のカテゴリ名
tags: [ここ, に, 記事の, タグ名]
hashtags: [ここに, ツイート時の, ハッシュタグ]
---
```
4. その下に、好きなようにMarkdown記法でブログを書いて保存する
- [こんなふうに]({{site.articleDir}}{{page.path}})
5. 問題なければ、WEBに反映される
- 問題ある場合はメールで通知が来たりします
- [ここ](//github.com/{{site.github.owner_name}}/{{site.github.repository_name}}/commits/master)でコミットが `×` になってたら大抵失敗です
