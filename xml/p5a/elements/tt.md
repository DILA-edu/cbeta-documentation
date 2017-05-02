# tt

雙語對照。這是 CBETA 自訂標記，TEI 無此元素。

校勘欄提供的巴利文對照，例 T01n0026.xml：

```xml
<cb:tt n="0635002" type="app">
  <cb:t resp="CBETA" xml:lang="zh">揵沓惒</cb:t>
  <cb:t resp="Taisho" xml:lang="pi" place="foot">Gandhabha.</cb:t>
</cb:tt>
```

上例中 t 元素的 place 屬性值為 foot 表示文字出現在校勘欄中。

悉漢雙行對照。例 T54n2133A, p. 1190a22

```xml
<cb:tt>
  <cb:t xml:lang="sa-Sidd" rend="margin-left:0em">
    <g ref="#SD-B064"/>
    <g ref="#SD-B5B1"/>
    <g ref="#SD-E355"/>
  </cb:t>
  <cb:t xml:lang="zh">天</cb:t>
</cb:tt>
```
