# note

參考：[TEI note 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-note.html)

## place

### place="foot"

通常底本頁尾註的標記是：

```xml
<note place="foot text" type="orig">⋯⋯</note>
```

如果底本有頁尾註，卻在內文缺了註標，那麼 place 屬性裡就會沒有 text，變成這樣：

```xml
<note place="foot" type="orig">⋯⋯</note>
```

### place="inline"

行中夾註

T01n0001.xml, p. 30a17

```xml
<note place="inline">丹本注云問中應有何等時出家諸本並闕</note>
```

### place=" interlinear"

行間註解

例 X61n1165.xml, p. 793b24

```xml
如來我若欲見隨意即見<note place="interlinear">以下正明欲見即見之故</note>我能了知如來國土莊嚴
```

## type

### type="orig"

底本校勘註

例 T01n0001.xml, p. 1a02

```xml
<note n="0001001" resp="Taisho" type="orig" place="foot text">此序依宋元明三本ニ依テ載ス</note><head><title>長阿含經</title>序</head>
```

### type="orig_biao"

例 X19n0347.xml, p. 561b24

```xml
<note n="0561b15" resp="Xuzangjing" place="foot text" type="orig_biao">法身大士身心無倦聲聞結業者心雖樂法身有疲厭或發息止想而淨名懸得其心故床坐獨寢旨現于此矣因舍利弗何坐之問而發之</note>
```

### type="orig_ke"

例 X19n0343.xml, p. 161b13

```xml
<note n="0161k01" resp="Xuzangjing" place="foot text" type="orig_ke">四列名</note>
```

### type="equivalent"

例 T01n0001.xml, p. 11a06

```xml
（二）第一分<note n="0011004" resp="Taisho" type="orig" place="foot text">遊行經～D. 10. Mahāparinibbānasuttanta.</note>
<note n="0011004" place="foot" type="equivalent">遊行經～D. 10. Mahāparinibbānasuttanta.</note>遊行經第二
```

### type="mod"

經過 CBETA 修訂的校勘註

例 T01n0001.xml, p. 1b10

```xml
<byline cb:type="Translator">
  <note n="0001012" resp="Taisho" type="orig" place="foot text">後秦弘始年＝姚秦三藏法師【三】</note>
  <note n="0001012" resp="CBETA" type="mod">後秦弘始年＝姚秦三藏法師【宋】【元】【明】</note>
  <app n="0001012">
    <lem wit="【大】">後秦弘始年</lem>
    <rdg resp="Taisho" wit="【宋】【元】【明】">姚秦三藏法師</rdg>
  </app>佛陀耶舍共竺佛念譯
</byline>
```

### type="rest"

校勘註不能轉為 app 標記的部份，以 &lt;note type="rest"> 記錄。

例 T01n0026.xml, p. 578a25

```xml
<note n="0578006" resp="Taisho" type="orig" place="foot text">品末題在卷末題前行【三】，〔中阿含〕－【明】</note>
<note n="0578006" resp="CBETA" type="mod">品末題在卷末題前行【宋】【元】【明】，〔中阿含〕－【明】</note>
<app n="0578006">
  <lem wit="【大】">中阿含</lem>
  <rdg resp="Taisho" wit="【明】"><space quantity="0"/></rdg>
</app>
<note n="0578006" place="foot" type="rest">品末題在卷末題前行【宋】【元】【明】</note>穢品第三竟
```

## 校勘編號 n

一條校勘經 CBETA 修訂，可能拆成兩個，例 T85n2882, p. 1383c26:

```xml
<note n="1383062" resp="Taisho" type="orig" place="foot text">〔不得…枝〕二十四字－【甲】</note>
<note n="1383062a" resp="CBETA" type="mod">〔不得停止〕－【甲】</note>...
<note n="1383062b" resp="CBETA" type="mod">〔佛有…枝〕二十字－【甲】</note>
```

## resp="CBETA"

T01n0046, p. 835c11

```xml
No. 46 [No. 26(74), No. 125(42.6)]<note resp="CBETA.eva">CBETA按：這是大正藏的錯誤，因為 T02n0125《增一阿含》第41品並沒有第6經，而第42品第6經的內容的確與 T01n0046 相關。</note>
```

## note 夾在 l 之間

例 T18n0908, p. 920b08

```xml
...
<l>瀉杓長及圓</l>
<note n="0920048" resp="Taisho" place="foot text" type="orig">〔并及…相〕二偈－【甲】</note>
<note n="0920048" resp="CBETA" type="mod">〔并及刻鏤文皆如注杓相〕二偈－【甲】</note>
<l>并及刻鏤文</l>...
```