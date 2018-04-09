# lem

校勘範圍可能跨行，為了在切換「底本」及「CBETA版本」時都可以正常顯示行號，需同時在 lem（CB本）或 rdg（底本）裡面插入同樣的 lb。

例 T32n1644.xml, p. 189a21

```xml
<app n="0189001">
  <lem resp="CBETA.maha" wit="【CB】【磧-CB】">忉<lb n="0189a22" ed="T"/>利天<note type="cf1">Q27_p0016b17</note></lem>
  <rdg resp="Taisho" wit="【宋】【元】【明】">忉利天</rdg>
  <rdg wit="【大】">忉<lb n="0189a22" ed="T"/>利</rdg>
</app>
```
