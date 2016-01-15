# rdg

參考 [TEI rdg 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-rdg.html)

## type=="correctionRemark" (考偽)

大正藏校勘欄有註記這地方可能是個錯字，但是大正藏未予更正。

例如 T44n1480.xml, p. 137c27

```xml
<note n="0137011" resp="Taisho" place="foot text" type="orig">狹＝挾？</note>
<app n="0137011">
	<lem resp="Taisho" wit="【大】">狹</lem>
	<rdg resp="Taisho" wit="【大】" type="correctionRemark">挾</rdg>
</app>
```