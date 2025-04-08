# list

參考：[TEI list 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-list.html) 包含以列表方式呈現的任何連續項目。

例 T18n0225, p. 482b05

```xml
<list>
  <item xml:id="itemT08p0482b0501">天帝釋問品</item>
  <item xml:id="itemT08p0482b0506">持品</item>
  <item xml:id="itemT08p0482b0508">功德品</item>
  <item xml:id="itemT08p0482b0601">變謀明慧品</item>
</list>
```

## @rend

### no-marker

B17n0092.xml, p. 630a13

```xml
<list rend="no-marker">
  <item><p rend="margin-left:5em;text-indent:-2em">一、訪聞近日僧尼等⋯⋯準此酬賞。</p></item>
  <item><p rend="margin-left:5em;text-indent:-2em">一、此後如有修補寺宇功德⋯⋯</p></item>
  ⋯⋯
</list>
```

## list 出現在 夾注 裡

ex: T50n2054_p0286b20

```xml
<note place="inline">
  <list rend="no-marker">
    <item xml:id="itemT50p0286b2001">首座師雅</item>
    ...
    <item xml:id="itemT50p0286b2327">師正</item>
  </list>
</note>
```
