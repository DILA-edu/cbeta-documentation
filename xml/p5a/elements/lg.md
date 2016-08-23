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

## place="inline"

偈頌不是從行首開始，例 T53n2121.xml

```xml
<lb n="0125c04" ed="T"/><p>夫言。</p><lg cb:place="inline"><l>是法未曾聞</l><l>而今聞汝說</l>
<lb n="0125c05" ed="T"/><l>何處聞正法</l><l>而不憂念子</l></lg>
```

## type="normal"

每行的第一個 `<l>` 前面空一格，之後的 `<l>` 前面空二格。
如果 `<l>` 有指定 rend 屬性，則依 rend 內容。

## type="abnormal" 不規則偈頌

`<l>` 預設不空格，除非有 rend 的設定，就依 rend。

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
