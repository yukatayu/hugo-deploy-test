# hugo-deploy-test
HugoとGitHubPagesのテスト

## メモ

tagとcategoryの設定

```yaml
date: "2015-09-05T16:40:41+09:00"
draft: false
title: "Hello!"
categories: [ "hugo" ]
tags: [ "hello", "world" ]
image: images/promotion.png
type: post
```

- `type: post` の物は，トップページの一覧の部分に表示される
- `type: featured` の物は，トップページの上部に表示される

静的コンテンツ(画像等)については， `static/` 以下に配置する。

about ページの gallery については，`data/gallery.yml` に一覧を記述する。

GitHubのリポジトリ設定で， Actions > General > Workflow permissions で，書き込み権限を与える。

ローカルでの動作確認は
```shell
hugo serve --disableFastRender
```
