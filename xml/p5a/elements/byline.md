# byline

包含作品的主要責任陳述，出現在題名頁或作品開頭或結尾處。

## @rend

### bold

ex: Y01n0001.xml, p. 1a02

```xml
<byline rend="bold">——民國三十一年春講於四川法王學院——</byline>
```
### kaiti 楷體

ex: Y30n0030.xml, p. a001a01

```xml
<byline cb:type="author" rend="kaiti">印順</byline>
```

## @type

### type="Author"

例 T01n0001.xml

```xml
<byline cb:type="Author">長安釋僧肇述</byline>
```

### type="Collector"

例 T04n0207.xml, p. 522b18

```xml
<byline cb:type="Collector">比丘道略集</byline>
```

### type="Editor"

例 X81n1571.xml, p. 402c05

```xml
<byline cb:type="Editor">京都聖感禪寺住持(臣)僧　(超永)　編輯</byline>
```

### type="Translator"

T12n0389.xml, p. 1110c15

```xml
<byline cb:type="Translator">後秦龜茲國三藏鳩摩羅什奉　詔譯</byline>
```

### type="較閱"

例 X81n1571.xml, p. 402c06

```xml
<byline cb:type="較閱">京都古華嚴寺住持(臣)僧　(超揆)　較閱　進呈</byline>
```

## byline 出現在 item 裡

ex: T51n2073_p0155c13

```xml
<list rend="no-marker">
  ...
  <item xml:id="itemT51p0155c1301">
    <title>如來興現經</title>四卷<note place="inline">是性起品無重頌偈仍將十忍品次後編之亦不題也</note>
    <byline>西晉元康年竺法護譯</byline>
  </item>
  ...
</list>
```

## byline 出現在 p 裡面

ex: T21n1239_p0202b01

```xml
<p xml:id="pT21p0202a2901">
  <note n="0202009" resp="Taisho" type="orig" place="foot text">此奧書甲本無，（（貞享…寂））五十六字＝（（應保三年三月四日移點了））十一字【乙】</note>
  <note n="0202009a" resp="CBETA" type="mod">（貞享…載）十九字【大】，應保三年三月四日移點了【乙】，此奧書甲本無</note>
  <app n="0202009a" cb:word-count="19">
    <lem wit="【大】">
      貞享四年中春十三一挍加批了
      <byline cb:type="other">淨嚴<note place="inline">四十九載</note></byline>
    </lem>
    <rdg resp="Taisho" wit="【乙】">應保三年三月四日移點了</rdg>
  </app>
  <note n="0202009a" type="rest" place="foot">此奧書甲本無</note>
</p>
```
