# lg

偈頌

參考：[TEI lg 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-lg.html)

例如 T02n0125.xml 《增壹阿含經》

```xml
<lg>
  <l>「諸惡莫作，</l><l>諸善奉行，</l>
  <l>自淨其意，</l><l>是諸佛教。</l>
</lg>
```

## @place

### inline

偈頌不是從行首開始，例 T53n2121.xml

```xml
<lb n="0125c04" ed="T"/><p>夫言。</p><lg cb:place="inline"><l>是法未曾聞</l><l>而今聞汝說</l>
<lb n="0125c05" ed="T"/><l>何處聞正法</l><l>而不憂念子</l></lg>
```
## @rend

### bold

ex: Y07n0007.xml, p. 23a09

```xml
<lg type="abnormal" rend="bold">
  <l>
    歸命盡十方：最勝業遍知，色無礙自在，救世大悲者；
    及彼身體相，法性真如海，無量功德藏；如實修行等。
  </l>
</lg>
```

### kaiti 楷體

ex: Y25n0025.xml, p. 478a11

```xml
<lg style="margin-left:3em" type="abnormal" rend="kaiti">
  <l>吾來大唐國，　傳教救迷情，　一花開五葉，　結菓自然成。</l>
</lg>
```

### mingti 明體

ex: Y25n0025.xml, p. 417a06

```xml
<lg rend="mingti" style="margin-left:3em">
  <l>身是菩提樹，　心如明鏡臺，　時時勤拂拭，　莫使有塵埃！</l>
</lg>
```

## @style

ex: GA045n0049.xml, p. 236a10

```xml
<lg type="abnormal" cb:place="inline" style="text-indent:2em">
  <l>一聲吼破太虛空　爍爍禪光橫大有</l>
</lg>
```

## @type

### type="normal"

每行的第一個 `<l>` 前面空一格，之後的 `<l>` 前面空二格。
如果 `<l>` 有指定 rend 屬性，則依 rend 內容。

### type="abnormal" 不規則偈頌

`<l>` 預設不空格，除非有 rend 的設定，就依 rend。

例 T85n2829.xml, p. 1267b11, 

BM:

```
T85n2829_p1267b11T##║一切普誦　如來妙色身　世間無與等　無
T85n2829_p1267b12T##║比不思議　是故今敬禮　如來色無盡　智
T85n2829_p1267b13T##║慧亦復然　一切法常住　是故歸依敬禮常
T85n2829_p1267b14t##║住三寶
```

XML:

```xml
<lb n="1267b11" ed="T"/><lg type="abnormal"><l>一切普誦</l><l rend="text-indent:1em">如來妙色身</l><l rend="text-indent:1em">世間無與等</l><l rend="text-indent:1em">無
<lb n="1267b12" ed="T"/>比不思議</l><l rend="text-indent:1em">是故今敬禮</l><l rend="text-indent:1em">如來色無盡</l><l rend="text-indent:1em">智
<lb n="1267b13" ed="T"/>慧亦復然</l><l rend="text-indent:1em">一切法常住</l><l rend="text-indent:1em">是故歸依敬禮常
<lb n="1267b14" ed="T"/>住三寶</l></lg>
```

### type="note1" 夾註偈頌

例 X09n0243_p0343b16

![](images/lg-note1.png)

```xml
<lg type="note1">
  <l>種子生佛法</l><l>良田長白法</l><l>大地持世間</l>
  ...
</lg>
```


### type="note2"

雙行小字偈頌，例 X18n0332

![](images/lg-note2.png)

```xml
<lg type="note2">
  <l>筆底楞伽一字無</l><l>浮雲散去月明孤</l>
  <l>恩深欲報辭難盡</l><l>塵劫分身舌不枯</l>
</lg>
```

## l 的 parent 不是 lg

l 可能不是直接被包在 lg 裡，而是在 lem 裡面，計算第幾個 l 的時候要注意，例如 T18n0908.xml:

```xml
<lg>
	...
	<app n="0917005">
		<lem wit="【大】"><l>繒繫亦如上</l><l>舍那半三股</l><l>蓮座火焰光</l></lem>
		<rdg resp="Taisho" wit="【明】">智者應善知審諦無錯謬</rdg>
	</app>
	<app n="0917006">
		<lem wit="【大】"><l>智者應善知</l><l>審諦無錯謬</l></lem>
		<rdg resp="Taisho" wit="【明】">繒繫亦如上舍那半三股蓮座火焰光</rdg>
	</app>
</lg>
```
