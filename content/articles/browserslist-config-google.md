---
title: "browserslist-config-google でモダンブラウザ向け最適化をする"
date: 2020-11-04T00:00:00+09:00
draft: false
---

browserslist のデフォルトは、IE 11 も含まれていてさすがにモダンじゃないなーと感じます。
個人的には Babel だけで自動的に IE 対応することは難しいと考えているため、
いっそのこと browserslist からレガシーブラウザを切り捨てます。

```bash
$ browserslist "defaults"
and_chr 85
and_ff 79
and_qq 10.4
and_uc 12.12
android 81
baidu 7.12
chrome 86
chrome 85
chrome 84
edge 86
edge 85
firefox 82
firefox 81
firefox 80
firefox 78
ie 11
ios_saf 14
ios_saf 13.4-13.7
ios_saf 13.3
ios_saf 12.2-12.4
kaios 2.5
op_mini all
op_mob 59
opera 71
opera 70
safari 14
safari 13.1
samsung 12.0
samsung 11.1-11.2
```

## browserslist-config-google を使う

どれくらい人気があるのでしょう？
https://www.npmjs.com/package/browserslist-config-google

```bash
$ browserslist "extends browserslist-config-google/no-ie"
and_chr 85
chrome 86
chrome 85
chrome 84
edge 86
edge 85
firefox 82
firefox 81
ios_saf 14
ios_saf 13.4-13.7
ios_saf 13.3
ios_saf 13.2
ios_saf 13.0-13.1
safari 14
safari 13.1
safari 13
```

うん、モダンだ。
