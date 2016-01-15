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