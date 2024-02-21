# ref

參考 [TEI ref 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-ref.html)

## @cRef

### 參照 PTS

例 N01n0001_p0001a01

```xml
<ref cRef="PTS.Vin.3.1"/>律藏　　經分別（Sutta-Vibhaṅga）
```

## @target

### 參照本文件中的其他位置

例如 T49n2035.xml, p. 250d05

```xml
<ref target="#list4">天台智者禪師○</ref>
...(中略)...
<list xml:id="list4"><head>四祖天台智者大禪師</head>
```

### 參照其他文件

例如 T42n1828.xml，p. 311a06，《瑜伽論記》參照《瑜伽師地論》：

```xml
<ref target="../T30/T30n1579.xml#xpath2(//0279a03)">論本卷第一</ref>
```

其他用例參考下方 [@type](#type) 說明。

## @type

### @type='taisho'

印順法師著作，連結到大正藏的某一欄，例 Y20n0020.xml, p. 65a03

```xml
（大正<ref type="taisho" target="vol:51;page:p185b">五一．一八五中</ref>——下）
```

當 `type="taisho"` 時 target 屬性值的樣式有如下幾種：

* `no:307` 指向 T0307, 其他例子： `no:150A`, `no:150B`
* `no:99.782` 指向 T0099 第 782 小經
* `no:125.37.7` 指向 T0125 / 37 六重品 / 第 7 小經
* `vol:25` 標示 冊號
* `vol:51;page:p185b` 標示 冊號、頁碼、欄
* 特殊例子： `no:99.726 others`

### @type='taixu'

連結到太虛大師全書，例 Y02n0002.xml, p. 103a03

```xml
<ref type="taixu" target="vol:25;page:p98-99">(ref taixu::vol:25;page:p98-99)</ref>
```

### @type='wxzj'

連結卍續藏，例 Y37n0035.xml, p. 86a03

```xml
（續<ref type="wxzj" target="vol:21;page:p291c">三四．四一二上（卍新續二十一．二九一下）</ref>）
```

### @type='yinshun'

例 Y02n0002.xml, p. 114a12

```xml
<ref type="yinshun" target="vol:33;page:p217-218">(ref yinshun::vol:33;page:p217-218)</ref>
```
