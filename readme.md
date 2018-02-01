ndc.js
========

## 概要
[日本十進分類(NDC; Nippon Dicimal Classification)](https://ja.wikipedia.org/wiki/%E6%97%A5%E6%9C%AC%E5%8D%81%E9%80%B2%E5%88%86%E9%A1%9E%E6%B3%95)のライブラリです。[CyberLibrarianさんのデータ](http://www.asahi-net.or.jp/~ax2s-kmtn/ref/ndc/ndc.html)を元に作成しました。

## 使い方
```html
<script src="ndc.js"></script>
```
```javascript
var NDC = require('ndc.js');
```

```javascript
var code = "913"; //NDC code
var version = "ndc9"; // "ndc9" or "ndc10"
NDC.getDescription(code, version);
// -> "小説. 物語"
NDC.getFullDescription(code, version);
// -> ["文学","日本文学","小説. 物語"]
//      ↑900,910,913が順に返る
```

```
NDC.dic
// -> {"100":{"ndc9":"哲学","ndc10":""},"101":{"ndc9":"哲学理論","ndc10":""}, ...
```

## その他

* ndc.js - 本体
* ndc.json - NDC.dicの中身
* ndc-9.json - NDC-9のみ
* ndc-10.json - NDC-10のみ
* example.html - 例

## License

MIT