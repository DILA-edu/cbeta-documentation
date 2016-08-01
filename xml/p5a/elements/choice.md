# choice

參考：[TEI choice 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-choice.html)

## 錯字訂正

T01n0001.xml, p. 1b02

```xml
涼州沙門佛<choice><corr>念</corr><sic>忘</sic></choice>為譯
```

## 註明 修訂人員

choice 元素加 cb:resp 屬性，例 T01n0001.xml, p. 2b01

```xml
<choice cb:resp="CBETA.say"><corr>娑</corr><sic>婆</sic></choice>羅＝博洛叉【宋】【元】【明】～Sāla.
```

## 註明 修訂依據

T01n0001.xml, p. 3a11

```xml
薩<choice cb:resp="CBETA.maha">
  <corr>尼<note type="cf1">T01n0001_p0002c29</note><note type="cf2">T50n2040_p0009a24</note><note type="cf3">T53n2122_p0335a24</note></corr>
  <sic>尸</sic>
</choice>
```

## type="shift"

T85n2871.xml, p. 1345a30

```xml
<choice type="shift" resp="CBETA.maha">
  <corr>大通方廣經卷上<note type="cf1">《大通方廣懺悔滅罪莊嚴成佛經》敦煌寶藏校勘版．法護編校增補．大藏文化出版社, 2004</note></corr>
  <sic><space quantity="0"/></sic>
</choice>
```

## 通用詞

T85n2893, p. 1411a09

```xml
<choice><orig>䠒跪</orig><reg type="通用詞">胡跪</reg></choice>合掌
```