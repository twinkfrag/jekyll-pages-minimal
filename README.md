# jekyll-pages-minimal
JekyllによるGitHub Pagesのテスト

## 最低限必要なファイル
- `_config.yml`
- 各markdown (配置はビルド時に設定可能)

## 本プロジェクトの構成
- `index.md` -> `_layouts/default.html` -> `/index.html`
- `folder/page2.md` -> `_layouts/default.html` -> permalink設定により`/page2.html`
- ページやテンプレートでは，liquid templateを使って`{{ site.title }}`のようにメタデータを呼び出したり，`{%- include hoge.html -%}`のように命令を実行する
- リポジトリのSettings > PagesでPagesのデプロイを有効にする．Sourceはデフォルトブランチ，FolderはJekyllでビルドする場合関係ないので何でも良い
- 本プロジェクトは独自ドメイン下のサブディレクトリになっているため，気をつける事項がいくつかある．  
  構成が異なる場合も以下には従うと吉
  + md内の相対リンク(例: `folder/img.png`)はビルド時に修正してくれる模様
  + テンプレート内は修正してくれないので，相対パスを考慮して`{{ site.github.url }}/assets/main.css`のように書く必要がある
  + 上記のようにすることで，vscodeでの編集，ローカルでのビルド，Pagesでのサブディレクトリビルドの全てで参照が正しく維持される
- 一度設定してしまえば，編集やページ追加はGitHubのWeb上でも可能．最近ではvscode online等も利用可能．

## ref
- https://docs.github.com/ja/pages/setting-up-a-github-pages-site-with-jekyll/
- https://jekyll.github.io/github-metadata/site.github/
- https://jekyllrb.com/docs/configuration/options/

## output
- https://www.twinkfrag.net/jekyll-pages-minimal
