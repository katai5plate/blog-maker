---
title: Top
description: example for blog-maker
image: random
---
{%- assign yourName = site.github.owner_name -%}{%- if yourName == "katai5plate" -%}{%- assign yourName = "World" -%}{%- endif -%}

### Hello, {{yourName}}!
Welcome to blog-maker.

---

## Tutorial
1. {% include jump.html url="/Tutorial/1" text="まずはブログをWEBで見れるようにしてみよう" %}
2. {% include jump.html url="/Tutorial/2" text="新しい記事を書いてみよう" %}

---

{% include articleList.html %}

