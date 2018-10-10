---
title: ブログ内部のリンクを貼る方法
description: 普通にMarkdownの記法でリンクを書くと失敗することがあります。そのときの対処法
image: machine
genre: Tips
tags: [リファレンス]
hashtags: [Jekyll]
---
{%- assign esc = "{%" -%}
{%- assign siteUrl2 = site.url | append: "/" | append: site.github.repository_name -%}

ブログの外に向けてリンクを貼りたい場合、Markdownでは以下の書き方を使うことができます

```
[Google](//www.google.com)
```
- 結果: [Google](//www.google.com)
  - -> `//www.google.com`

しかし、ブログ内の記事や固定ページなどに向けてリンクを貼りたい場合は、<br>
`_config.yml` の `ownDomain` の値によってURLが異なるため、上記の方法が使えない場合があります。

```
[Hello!](/HelloWorld)
```
- 結果: [Hello!](/HelloWorld)
  - -> `{{site.url}}/HelloWorld` 固定

これを回避するためには、以下のように書きます。

```
{{esc}} include jump.html url="/HelloWorld" text="Hello!" %}
```
- 結果: {% include jump.html url="/HelloWorld" text="Hello!" %}
  - -> `{{site.url}}/HelloWorld` か `{{siteUrl2}}/HelloWorld` に自動判別

これを使用することで、`ownDomain` の値によって以下のURLを先頭に付け足すことができます。

|ownDomain|URL|example|
|-|-|-|
|false|site.url + site.github.repository_name|`https://username.github.io/reponame/`|
|true|site.url|`https://username.github.io/`|
