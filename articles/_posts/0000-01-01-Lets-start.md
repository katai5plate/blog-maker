---
title: １．まずはブログをWEBで見れるようにしてみよう
description: ざっくりチュートリアルその１
image: vista
genre: Tutorial
tags: [Basic, StartUp, Usage, 日本語]
hashtags: [blogmaker]
---
{%- assign gitAddress = site.github.owner_name | append: "/" | append: {{site.github.repository_name}} -%}

# ざっくりチュートリアル

## まずはブログをWEBで見れるようにしてみる
1. プロジェクトを `Folk` する

2. `_config.yml` を[開き](//github.com/{{gitAddress}}/blob/master/_config.yml)、以下の行の `blog-maker` を自分のブログの名前に変更する
```yml
siteName: blog-maker
```

3. `Settings` を開き、<br>
`Options` -> `GitHub Pages` -> `Source` のプルダウンから<br>
`master branch` を選んで `Save` を押す

4. 緑の枠で ` Your site is published at https://*****.github.io/blog-maker/`<br>
というようなメッセージが出たら成功。<br>
表示されたURLが公開先なので、[アクセス](//{{site.github.owner_name}}.github.io/blog-maker/)してみよう。

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
- [たとえば、こんなふうに](//raw.githubusercontent.com/{{gitAddress}}/master/fixed/hello.md)

5. 問題なければ、WEBに反映される
- 問題ある場合はメールで通知が来たりします
- [ここ](//github.com/{{gitAddress}}/commits/master)でコミットが `×` になってたら大抵失敗です

