# rdg

參考 [TEI rdg 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-rdg.html)

* [一般用法](#一般用法)
* [correctionRemark](#typecorrectionremark-考偽)
* [variantRemark](#typevariantremark-校異)
* [cbetaRemark](#typecbetaremark)

## 一般用法

記錄不同版本用字，例如 T01n0001.xml：

```xml
<app n="0001005">
  <lem wit="【大】">韞</lem>
  <rdg resp="Taisho" wit="【宋】【元】">溫</rdg>
</app>
```

## type=="correctionRemark" (考偽)

### 大正藏 考偽

大正藏校勘欄有註記這地方可能是個錯字，但是大正藏未予更正。

例：T44n1840.xml, p. 137c27

```xml
<note n="0137011" resp="Taisho" place="foot text" type="orig">狹＝挾？</note>
<app n="0137011">
  <lem resp="Taisho" wit="【大】">狹</lem>
  <rdg resp="Taisho" wit="【大】" type="correctionRemark">挾</rdg>
</app>
```

在 CBReader 校勘表格呈現為：

【大】？ | 挾 
------- | ------
【大】 | 狹

### 底本 或 校對本 考偽

「底本」或某一「校對本」的註記中所作的勘誤 (考偽)

底本考偽 例：T43n1832.xml, p. 749c12

```xml
<note n="0749006" resp="Taisho" place="foot text" type="orig">二＝一ヵ【原】</note>
<app n="0749006">
  <lem resp="Taisho" wit="【大】">二</lem>
  <rdg resp="Taisho" wit="【原】" type="correctionRemark">一</rdg>
</app>
```

在 CBReader 校勘表格呈現為：

【大】 | 二
----- | ----
【原】ヵ | 一

校對本 考偽 例： T18n0895a.xml, p. 0721c28

```xml
<note n="0721021" resp="Taisho" place="foot text" type="orig">通＝施ヵ【乙】</note>
<app n="0721021">
  <lem resp="Taisho" wit="【大】">通</lem>
  <rdg resp="Taisho" wit="【乙】" type="correctionRemark">施</rdg>
</app>
```

在 CBReader 校勘表格呈現為：

【大】 | 通
----- | ----
【乙】ヵ | 施

### 同本多考偽 特例

T21n1203.xml, lb=0028a03

[1] 我＝等ヵ【原】，及ヵ【原】，為ヵ【原】，〔我〕－【甲】

## type=="variantRemark" (校異)

例三：T43n1831.xml, p. 641b03

```xml
<note n="0641001" resp="Taisho" place="foot text" type="orig">界＝義ィ【丙】</note>
<app n="0641001">
  <lem wit="【大】">界</lem>
  <rdg resp="Taisho" wit="【丙】" type="variantRemark">義</rdg>
</app>
```

在 CBReader 校勘表格呈現為：

【大】 | 界
----- | ----
【丙】ィ | 義

## type=="cbetaRemark"

CBETA 的修訂用字，但依文本授權方要求，不使用。

例 TX01n0001.xml：

```xml
<app n="0140a1201">
  <lem wit="【太虛】">歛</lem>
  <rdg resp="CBETA" type="cbetaRemark">斂</rdg>
</app>
```
