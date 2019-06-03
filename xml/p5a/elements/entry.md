# entry

參考：[TEI entry 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-entry.html) 包含字典中一個結構完善的辭條項目。

X64, No. 1261, 《祖庭事苑》, p0314b02

```xml
<entry>
  <form>師資</form>
  <def>
    <p>老氏曰。善人。不善人之師。不善人。善人之資。</p>
    <p>說者曰。善人有不善人。然後善救之功著。故曰資。</p>
  </def>
</entry>
```

## @place

### place="inline"

X64, No. 1263, p. 471a10

```xml
<entry cb:place="inline" style="margin-left:1em">
  <form>張</form>
  <cb:def>
    <p xml:id="pX64p0471a1005" rend="margin-left:1em;inline">施也。</p>
  </cb:def>
</entry>
```

## @style

ex: X22n0421.xml, p. 549b19

```xml
<entry cb:place="inline" style="margin-left:1em">
  <form>哆</form>
  <cb:def><p xml:id="pX22p0549b1906" cb:place="inline"><note place="inline">音掇</note>。</p></cb:def>
</entry>
```
