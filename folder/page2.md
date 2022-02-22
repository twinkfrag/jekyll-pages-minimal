---
layout: default
title: page2 title
permalink: /page2
---

- yaml front matterで各種メタデータを設定可能
- `layout: default`で`_layouts`ディレクトリ内のどのhtmlを使用するか
- `title`はページ内やレイアウト内で {{ page.title }} と呼び出せる
- `permalink`を指定すると，生成元のmdファイルと出力先を変えることができる
- 実用上は，`_config.yml`内で`defaults`指定でディレクトリ全体に設定をかけた方がいいと思われる
