# tt

雙語對照。這是 CBETA 自訂標記，TEI 無此元素。

## @type="app"

校勘欄提供的巴利文對照，例 T01n0026.xml：

```xml
<cb:tt n="0635002" type="app">
  <cb:t resp="CBETA" xml:lang="zh">揵沓惒</cb:t>
  <cb:t resp="Taisho" xml:lang="pi" place="foot">Gandhabha.</cb:t>
</cb:tt>
```

上例中 t 元素的 place 屬性值為 foot 表示文字出現在校勘欄中。

## 悉漢雙行對照

例 T54n2133A, p. 1190a22

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

## @place="inline"

行中悉漢對照。例 T19n0939.xml, p. 89c23

```xml
次從心想出<cb:tt place="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-E17C"/></cb:t>
  <cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>吽</cb:zi><cb:sg>引</cb:sg></cb:yin></cb:t>
</cb:tt><cb:tt rend="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-E1BD"/></cb:t>
  <cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>怛囕</cb:zi><cb:sg>二合</cb:sg></cb:yin></cb:t>
</cb:tt><cb:tt rend="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-E050"/></cb:t>
  <cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>紇陵</cb:zi><cb:sg>二合</cb:sg></cb:yin></cb:t>
</cb:tt><cb:tt rend="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFD4"/></cb:t>
  <cb:t xml:lang="zh-Hant">
<lb n="0089c24" ed="T"/>惡</cb:t></cb:tt>真言。
```

## @rend="normal"

不做多行對照，正常顯示。例 T54n2133A.xml, p. 1194c17

```xml
<cb:tt rend="normal">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-CBA7"/>...</cb:t>
  <lb n="1194c18" ed="T"/><cb:t xml:lang="zh-Hant">作　阿闍梨多　聞　三藏　法師　勝</cb:t>
  <lb n="1194c19" ed="T"/><cb:t xml:lang="san-tr">Kṛtir Ācārya-bahu-śruta-tripiṭa [ka] bhadanta-param:</cb:t>
</cb:tt>
```
