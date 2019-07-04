# p

段落

參考：[TEI p 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-p.html)

## @rend

### bold
例 Y01n0001.xml
```xml
<p rend="bold">須菩提！當來之世，若有善...</p>
```

### inline

底本未分段，CBETA 加上的分段，例 T11n0310.xml, p. 323a12

```xml
<lb n="0323a12" ed="T"/>煮四大漸成。</p><p rend="inline">「第二七日處母胎時，所感業
<lb n="0323a13" ed="T"/>風名為遍滿。其風微細吹母左脇及以右脇，
<lb n="0323a14" ed="T"/>令歌羅邏身相漸現，狀如稠酪、或似凝酥，內
<lb n="0323a15" ed="T"/>熱煎煮便即轉為安浮陀身，如是四大漸漸
<lb n="0323a16" ed="T"/>成就。</p>
```

### kaiti 楷體
例 Y14n0014.xml
```xml
<p rend="kaiti">民國五十二年的春天，我曾應臺南佛教會的邀請，作了七天的講演。...</p>
```

### 多值
ex: Y25n0025.xml, p. 413a02
```xml
<p cb:type="head2" rend="kaiti bold">
  六祖慧能大師於韶州大梵寺施法壇經一卷
</p>
```
## @style

X79n1559.xml, p. 450a10

```xml
<p style="margin-left:1em;text-indent:-1em">舉。巴陵示眾。...</p>
```

## @type

### type="dharani" 咒語

T12n0375.xml, p. 609c04

```xml
<p cb:type="dharani">「『侘枳　咤咤羅侘枳　盧呵隷摩訶盧呵隸阿羅　遮羅　多羅　莎呵』</p>
```

### type="head1"

ex: B03n0002.xml, p. 30a04

```xml
<p cb:type="head1" xml:id="pB03p0030a0401">世主妙嚴品第一</p>
```
### type="head2"

ex: B01n0001.xml, p. 4a07

```xml
<p cb:type="head2"><note place="inline">1</note>生年的問題</p>
```

### type="head3"

ex: B08n0026.xml, p. 189b24

```xml
<p cb:type="head3">波逸提戒相頌　178條</p>
```

### type="head4"

ex: B02n0001.xml, p. 607a10

```xml
<p cb:type="head4">禮敬諸佛歌</p>
```

### type="head5"
ex: B08n0026.xml, p. 28a21
```xml
<p cb:type="head5">預白</p>
```

### type="head6"
ex: C056n1163.xml, p. 837c23
```xml
<p cb:type="head6">舌根聲<note place="inline">凡五字中第四字與第三字同而輕重微異</note></p>
```

### type="pre"

按原書換行

例 X66n1297, p. 266b23

```xml
<p cb:type="pre">...</p>
```
