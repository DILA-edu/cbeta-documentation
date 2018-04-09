# app

不同版本的不同用字

例如：T01, No. 1, p. 1，大正藏原文：

	T01n0001_p0001a14║言法歸。法歸者。蓋是萬善之淵府。總持之林
	T01n0001_p0001a15║苑。其為典也。淵博弘富。[05]韞而彌廣。明宣禍

校勘條目

	[05] 韞＝溫【宋】【元】

表示此處大正藏作「韞」字，而宋本、元本作「溫」字。

XML

```xml
<lb n="0001a15"/>苑。其為典也。淵博弘富。
<note n="0001005" resp="Taisho" type="orig" place="foot text">韞＝溫【宋】【元】</note>
<app n="0001005">
    <lem>韞</lem><!-- 大正藏用字 -->
    <rdg wit="【宋】【元】" resp="Taisho">溫</rdg><!-- 其他版用字 -->
</app>而彌廣。明宣禍
```

上面 rdg 元素的 wit 屬性請參考 [../attributes/wit.md](../attributes/wit.md)

## @type

### star_removed

type="star_removed" 表示底本有個星號「＊」校勘，CBETA 修訂拿掉這個「＊」校勘。
因為 CBETA 在這裡選擇跟底本不同的用字，已經不適用「下同」。

此類標記在呈現底本時顯示星號「＊」，呈現 CBETA 版本時則不顯示星號「＊」。

例如 T01n0023.xml, p. 303c29

```xml
<lb n="0303a10" ed="T"/>...<app n="0303004">...</app>
... (中略) ...
<lb n="0303c29" ed="T"/>...
<note n="0303c2901" resp="CBETA" type="add">越【CB】【磧-CB】，趣【大】，越【宋】【元】【明】</note>
<app type="star_removed" corresp="#0303004">
  <lem wit="【CB】【磧-CB】" resp="CBETA.maha">越<note type="cf1">Q18_p0745a18</note><note type="cf2">T01n0023_p0277b11</note></lem>
  <rdg wit="【大】">趣</rdg>
  <rdg resp="Taisho" wit="【宋】【元】【明】">越</rdg>
</app>
```
