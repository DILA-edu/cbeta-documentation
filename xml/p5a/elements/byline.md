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
