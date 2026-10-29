# ttr

隔行對照中的一行（row）。這是 CBETA 自訂標記，TEI 無此元素。只出現在 [`<cb:tt>`](tt.md) 之內。

* 一個 `<cb:tt>` 恰好有兩個 `<cb:ttr>`，對應原書的上下兩行。
* 每個 `<cb:ttr>` 裡依序放多個 `<cb:t>`，兩個 `<cb:ttr>` 的 `<cb:t>` 數量相同，依位置一一對應。
* 同一個 `<cb:ttr>` 內的 `<cb:t>` 語言相同；沒有對應字的位置以空的 `<cb:t/>` 佔位。
* 第二行開頭的 `<lb>`（及 `<pb>`）放在兩個 `<cb:ttr>` 之間，不放在 `<cb:ttr>` 內。
* 不屬於對照的文字（引號、標點、說明文字）直接放在 `<cb:ttr>` 中、`<cb:t>` 之外。

`<cb:ttr>` 沒有屬性。詳細規則與範例見 [tt.md](tt.md#隔行對照ttr-列式)。

例 T54n2132.xml, p. 1187b23

```xml
<lb n="1187b23" ed="T"/><p xml:id="pT54p1187b2301"><cb:tt>
  <cb:ttr>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5A9"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5E5"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A67A"/></cb:t>
    ...
  </cb:ttr>
<lb n="1187b24" ed="T"/><cb:ttr>
    <cb:t xml:lang="zh-x-yy">娜</cb:t>
    <cb:t xml:lang="zh-x-yy">麼</cb:t>
    <cb:t xml:lang="zh-x-yy"><cb:yin><cb:zi>娑</cb:zi><cb:sg>上</cb:sg></cb:yin></cb:t>
    ...
  </cb:ttr>
</cb:tt>
```
