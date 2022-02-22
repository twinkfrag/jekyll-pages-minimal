# jekyll-pages-minimal
JekyllによるGitHub Pagesのテスト

## 最低限必要なファイル
- `_config.yml`
- 各markdown (配置はビルド時に設定可能)

## 本プロジェクトの構成
- `index.md` -> `_layouts/default.html` -> `/index.html`
- `folder/page2.md` -> `_layouts/default.html` -> permalink設定により`/page2.html`
- ページやテンプレートでは，liquid templateを使って`{{ site.title }}`のようにメタデータを呼び出したり，`{%- include hoge.html -%}`のように命令を実行する

## ref
- https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/
- https://jekyll.github.io/github-metadata/site.github/
- https://jekyllrb.com/docs/configuration/options/

## output
- https://www.twinkfrag.net/jekyll-pages-minimal
