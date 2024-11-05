# lem

lem 元素內容為底本用字，或 CBETA 依據各種版本選用最適當的用字。

例 T01n0001_p0001a15

```xml
<app n="0001005">
  <lem wit="【大】">韞</lem>
  <rdg resp="Taisho" wit="【宋】【元】">溫</rdg>
</app>
```

lem 的 wit 屬性值為【大】，表示《大正藏》使用「韞」字，而【宋】【元】二本使用「溫」字。

又如 T01n0001_p0002b13

```xml
<app n="0002016">
  <lem resp="CBETA.maha" wit="【CB】">牟</lem>
  <rdg wit="【大】">無</rdg>
  <rdg resp="Taisho" wit="【宋】【元】【明】">牟</rdg>
</app>尼
```

第一個 rdg 的 wit 屬性值為【大】，表示《大正藏》作「無」字；  
第二個 rdg 的屬性值為【宋】【元】【明】，表示此三本作「牟」字；  
而 lem 的 wit 屬性值為【CB】，表示 CBETA 採用「牟」字。

## 校勘範圍跨行

校勘範圍可能跨行，為了在切換「底本」及「CBETA版本」時都可以正常顯示行號，需同時在 lem（CB本）或 rdg（底本）裡面插入同樣的 lb。

例 T32n1644.xml, p. 189a21

```xml
<app n="0189001">
  <lem resp="CBETA.maha" wit="【CB】【磧-CB】">忉<lb n="0189a22" ed="T"/>利天<note type="cf1">Q27_p0016b17</note></lem>
  <rdg resp="Taisho" wit="【宋】【元】【明】">忉利天</rdg>
  <rdg wit="【大】">忉<lb n="0189a22" ed="T"/>利</rdg>
</app>
```

## lem contain div

ex: T16n0665_p0403a03

```xml
<app n="0403a0301">
  <lem wit="【CB】" resp="CBETA.ting" cb:provider="來函：萧苏晏 (2022-06-16)">
    <cb:div type="xu">
      <cb:mulu level="1" type="序">大唐龍興三藏聖教序</cb:mulu>
      <head>大唐龍興三藏聖教序</head>
      <byline cb:type="author">中宗孝皇帝製</byline>
      <p xml:id="T16p0403a030016" cb:place="inline">蓋聞蒼蒼者天⋯⋯又若斯焉。</p>
      ....
    </cb:div>
  </lem>
  <rdg wit="【大】"><space quantity="0"/></rdg>
</app>
```
