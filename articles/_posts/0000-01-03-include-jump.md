---
title: ブログ内部のリンクを貼る方法
description: 普通にMarkdownの記法でリンクを書くと失敗することがあります。そのときの対処法
image: machine
genre: Tips
tags: [リファレンス]
hashtags: [Jekyll]
---

ブログの外に向けてリンクを貼りたい場合、Markdownでは以下の書き方を使うことができます

```
[Google](//www.google.com)
```

しかし、ブログ内の記事や固定ページなどに向けてリンクを貼りたい場合は、
`_config.yml` の `ownDomain` の値によってURLが異なるため、上記の方法が使えない場合があります。

失敗する書き方：
```
[Hello!](/blog-maker/HelloWorld)
```

これを回避するためには、以下のように書きます。

成功する書き方：
{%- assign ex = '{% include jump.html url="/blog-maker/HelloWorld" text="Hello!" %}' -%}
```
{{ex}}
```

これを使用することで、`ownDomain` の値によって以下のURLを先頭に付け足すことができます。

|ownDomain|URL|example|
|-|-|-|
|true|site.url + site.github.repository_name|`https://username.github.io/reponame/`|
|false|site.url|`https://username.github.io/`|
