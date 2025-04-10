# l

參考 [TEI &lt;l>](https://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-l.html) (詩行) 包含詩文的一行，也許是不完整的詩行。

## @style

ex: ZW01n0003.xml, p. 58a20

```xml
<lg type="abnormal">
  <l style="text-indent:4em">因日光明眼得見，</l>
  ...
</lg>
```

## l 出現在 夾注 裡

ex: T16n0657_p0206b27

```xml
<lg>
  ...
  <l>...</l>
  <lb n="0206b27" ed="T"/>
  <note place="inline">
    <l>
      <note n="0206023" resp="Taisho" type="orig" place="foot text">〔此下丹鄉有〕夾註－【三】【宮】</note>
      <note n="0206023" resp="CBETA" type="mod"><note place="inline">此下丹鄉有</note>【大】，〔－〕【宋】【元】【明】【宮】</note>
      <app n="0206023">
        <lem wit="【大】">此下丹、鄉有</lem>
        <rdg resp="Taisho" wit="【宋】【元】【明】【宮】"><space quantity="0"/></rdg>
      </app><caesura/>
      <note n="0206024" resp="Taisho" type="orig" place="foot text">（皆言…說）二十字為本文【三】【宮】</note>
      <note n="0206024" resp="CBETA" type="mod"><!--CBETA todo type: a--><!--CBETA todo type: newmod-->（皆言…說）二十字為本文【宋】【元】【明】【宮】</note>
      皆言云何
      <note n="0206025" resp="Taisho" type="orig" place="foot text">住＝入【三】【宮】</note>
      <note n="0206025" resp="CBETA" type="mod">住【大】，入【宋】【元】【明】【宮】</note>
      <app n="0206025">
        <lem wit="【大】">住</lem>
        <rdg resp="Taisho" wit="【宋】【元】【明】【宮】">入</rdg>
      </app>？<caesura/>云何而修學？
    </l><lb n="0206b28" ed="T"/>
    <l>從何得此法？<caesura/>今為我等說。</l>
  </note>
  <l>...</l>
  ...
</lg>
```
