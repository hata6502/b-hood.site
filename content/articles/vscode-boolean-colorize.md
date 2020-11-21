---
title: "VSCode で true と false の色分け"
date: 2020-11-21T22:19:40+09:00
draft: false
---

boolean の mapping を書くと true と false が見づらいため、
VSCode で true を緑、false を 赤 で表示して見やすくします。

settings.json

```json
"editor.tokenColorCustomizations": {
  "textMateRules": [
    {
      "scope": "constant.language.boolean.false",
      "settings": {
        "foreground": "#D3569B"
      }
    },
    {
      "scope": "constant.language.boolean.true",
      "settings": {
        "foreground": "#9BD356"
      }
    },
  ]
}
```
