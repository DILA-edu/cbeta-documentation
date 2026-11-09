# item

參考 [list](list.md)

參考：[TEI item 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-item.html)

## 編號直接寫在文本中

`item` 不使用 `@n` 屬性。原本 T18n0850.xml、T18n0862.xml 的 `item` 以 `n="（一）"` 記錄編號，已取消；編號「（一）」等直接寫在 `item` 的內文中。

T18n0850.xml, p. 87a14

```xml
<list xml:lang="sa-Sidd">
  <item xml:id="itemT18p0087a1401">（一）<g ref="#SD-E074"/><g ref="#SD-A5A9"/>...</item>
  <item xml:id="itemT18p0087a1601">（二）<g ref="#SD-E074"/><g ref="#SD-A67A"/>...</item>
  ...
</list>
```

## item 下有多個 p

例 X81n1570.xml, p. 329c23

```xml
<item>
  <p>燈史自傳聯普續廣五籍...敢曰樹天下萬世之防。</p>
  <p>按列聖徽猷...俱止三十七世。</p>
</item>
```
