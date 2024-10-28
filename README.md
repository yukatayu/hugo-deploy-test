# hugo-deploy-test
HugoとGitHubPagesのテスト

## メモ

tagとcategoryの設定

https://gohugo.io/content-management/front-matter/
```yaml
date: "2015-09-05T16:40:41+09:00"
draft: false
title: "Hello!"
categories: [ "hugo" ]
tags: [ "hello", "world" ]
image: images/promotion.png
type: post
summary: "tl;dr"
```

- `type: post` の物は，トップページの一覧の部分に表示される
- `type: featured` の物は，トップページの上部に表示される

静的コンテンツ(画像等)については， `static/` 以下に配置する。

about ページの gallery については，`data/gallery.yml` に一覧を記述する。

GitHubのリポジトリ設定で， Actions > General > Workflow permissions で，書き込み権限を与える。

ローカルでの動作確認は
```shell
hugo serve --disableFastRender --buildDrafts
```

`date:` に入れる時間は， [これ](https://yukatayu.tech/time.html) で取得すると早い

## やるべきこと
- `static/robots.txt` の `Sitemap` の URL を更新
- `config.toml` の `baseURL`, `title`, その他書き換えられそうな箇所を更新
