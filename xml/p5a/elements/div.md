# div

參考：[TEI div 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-div.html)

## @rend

### kaiti 楷體

ex: Y30n0030.xml, p. 1a05

```xml
<cb:div type="other" rend="kaiti">
  <cb:mulu level="3" type="其他">概述</cb:mulu>
  <p style="text-indent:2em">
    <note n="0001004" resp="釋印順" type="orig">凡正楷字是<title level="m">《論》</title>文。</note>
    事契經者，謂四阿笈摩：一者、雜阿笈摩，二者、中阿笈摩，三者、長阿笈摩，四者、增一阿笈摩。...
  </p>...
</cd:div>
```

## @type

type 屬性值 有這些：
* "chu"
* "commentary" (釋, 與 orig 相對)
* "di" (地)
* "fen" (分)
* "hui" (會)
* "jie"
* "jing" (經)
* "lg"
* "mu"
* "note"
* "orig" (original, 原文, 與 commentary 相對)
* "other"
* "pin" (品)
* "she" (攝) 只出現在 T30n1579.xml 《瑜伽師地論》
* "shi" (事) 只出現在 T30n1579.xml《瑜伽師地論》
* "toc"
* "w" (附文)
* "xiang"
* "xu" (序)
* "zhang"
* "廣釋"
* "續補"

### 原文 type="orig" 與 解釋 type="commentary"

例如 B25n1045.xml, p. 725b20

```xml
<cb:div type="orig">
  <p xml:id="pB25p0725b2001">玉澗頌雲門北斗藏身因緣云⋯⋯</p>
</cb:div>
<cb:div type="commentary">
  <p xml:id="pB25p0726a0601" rend="margin-left:1em">師拈云北斗藏身話⋯⋯</p>
</cb:div>
```
### type="dharani"

2025-03 開始，咒語都標在 p 元素上，不標在 div 上。

### type="di"

例 T30n1579.xml

```xml
<cb:div n="1" type="di">
  <cb:mulu n="1" level="2" type="其他">1 五識身相應地</cb:mulu>
...
</cb:div>
```

### type="fen"

例 T01n0001.xml, p. 114b07

```xml
<cb:div type="fen">
  <cb:mulu level="1" type="分">4 分</cb:mulu>
  ...
</cb:div>
```

### type="hui"

例 T36n1742, p. 1053a28

```xml
<cb:div type="hui">
  <cb:mulu level="1" type="會">3 忉利天宮說六品三卷</cb:mulu>
  <head>第三會忉利天宮說六品三卷</head>
  ...
</cb:div>
```

### type="jing"

例 T01n0001.xml, p. 109c22

```xml
<cb:div type="jing">
  <cb:mulu level="2" type="經">28 布吒婆樓經</cb:mulu>
  <head>（二八）<title>佛說長阿含</title>第三分布吒婆樓經第九</head>
  ...
</cb:div>
```

### type="other"

例 X78n1553.xml, p. 420a11

```xml
<cb:div type="other">
  <cb:mulu type="其他" level="1">天聖廣燈錄都帙目錄 〔宋實〕</cb:mulu>
  <head>天聖廣燈錄都帙目錄　　　〔宋實〕</head>
  ...
</cb:div>
```

### type="pin"

例 T01n0001.xml, p. 114b07

```xml
<cb:div type="pin">
  <cb:mulu level="3" type="品">1 閻浮提州品</cb:mulu>
  <head>閻浮提州品第一</head>
  ...
</cb:div>
```

### 附文 type='w'

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

### type="xu" 序

例 X81n1570.xml, p. 327a19

```xml
<cb:div type="xu">
  <cb:mulu type="序" level="1">No. 1570-B 五燈全書目序</cb:mulu>
  <head>No. 1570-B 五燈全書目序</head>
  ...
</cb:div>
```
