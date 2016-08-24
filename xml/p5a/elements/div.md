# div

參考：[TEI div 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-div.html)

## 原文 type="orig" 與 解釋 type="commentary"

例如 B25n1045.xml, p. 725b20

```xml
<cb:div type="orig">
  <p xml:id="pB25p0725b2001">玉澗頌雲門北斗藏身因緣云⋯⋯</p>
</cb:div>
<cb:div type="commentary">
  <p xml:id="pB25p0726a0601" rend="margin-left:1em">師拈云北斗藏身話⋯⋯</p>
</cb:div>
```

## type="fen"

例 T01n0001.xml, p. 114b07

```xml
<cb:div type="fen">
  <cb:mulu level="1" type="分">4 分</cb:mulu>
  ...
</cb:div>
```

## type="hui"

例 T36n1742, p. 1053a28

```xml
<cb:div type="hui">
  <cb:mulu level="1" type="會">3 忉利天宮說六品三卷</cb:mulu>
  <head>第三會忉利天宮說六品三卷</head>
  ...
</cb:div>
```

## type="jing"

例 T01n0001.xml, p. 109c22

```xml
<cb:div type="jing">
  <cb:mulu level="2" type="經">28 布吒婆樓經</cb:mulu>
  <head>（二八）<title>佛說長阿含</title>第三分布吒婆樓經第九</head>
  ...
</cb:div>
```

## type="other"

例 X78n1553.xml, p. 420a11

```xml
<cb:div type="other">
  <cb:mulu type="其他" level="1">天聖廣燈錄都帙目錄 〔宋實〕</cb:mulu>
  <head>天聖廣燈錄都帙目錄　　　〔宋實〕</head>
  ...
</cb:div>
```

## type="pin"

例 T01n0001.xml, p. 114b07

```xml
<cb:div type="pin">
  <cb:mulu level="3" type="品">1 閻浮提州品</cb:mulu>
  <head>閻浮提州品第一</head>
  ...
</cb:div>
```

## 附文 type='w'

例 T85n2869, p. 1335c04

```xml
<lb n="1335c04" ed="T"/><cb:div type="w"><p xml:id="pT85p1335c0401">大業十三年。佛弟子張佛果為劉士章善友
<lb n="1335c05" ed="T"/>知識敬造寶車經一卷流通讀誦講說修行。
<lb n="1335c06" ed="T"/>願藉此大乘弘化之業俱遊勝境履踐妙迹
<lb n="1335c07" ed="T"/>背八邪道歸八正路。具首楞嚴三昧之力。獲
<lb n="1335c08" ed="T"/>四如意念處功德。願於將來無量劫中世世
<lb n="1335c09" ed="T"/>生生還共弟子深結善因菩提眷屬發大乘
<lb n="1335c10" ed="T"/>心求摩訶衍。具足智慧神通威德根力覺道
<lb n="1335c11" ed="T"/>皆悉成就。俱修梵行。同登種覺。</p></cb:div>
```

## type="xu" 序

例 X81n1570.xml, p. 327a19

```xml
<cb:div type="xu">
  <cb:mulu type="序" level="1">No. 1570-B 五燈全書目序</cb:mulu>
  <head>No. 1570-B 五燈全書目序</head>
  ...
</cb:div>
```
