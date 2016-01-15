# milestone

參考：[TEI milestone 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-milestone.html)

例 T01n0001.xml

```xml
<pb n="0001a" ed="T" xml:id="T01.0001.0001a"/>
<lb n="0001a01" ed="T"/>
<milestone n="1" unit="juan"/><cb:docNumber>No. 1</cb:docNumber>
```

上面的 milestone 表示第一卷的開始。但是第一行的 pb 跟 lb，雖然在 milestone 的前面，但是其實是屬於第一卷。

在卷與卷之間更須注意，例如 T01n0001.xml

```xml
<lb n="0011a02" ed="T"/>
<milestone n="2" unit="juan"/>
<lb n="0011a03" ed="T"/>
```

第二卷是從 11a02 開始，而不是 11a03。

這樣的邏輯是有點奇怪，但是目前 CBETA XML 是這樣的情況。