# tt

雙語對照。這是 CBETA 自訂標記，TEI 無此元素。

* [兩種結構](#兩種結構)
* [隔行對照（ttr 列式）](#隔行對照ttr-列式)
  * [基本規則](#基本規則)
  * [換行、換頁的位置](#換行換頁的位置)
  * [對齊用的空 t](#對齊用的空-t)
  * [ttr 中 t 以外的內容](#ttr-中-t-以外的內容)
* [@place="inline"](#placeinline)
* [@type](#type)
  * [type="app"](#typeapp)
  * [type="single-line"](#typesingle-line)
  * [type="tr"](#typetr)

## 兩種結構

`<cb:tt>` 的內容有兩種寫法：

1. **隔行對照（ttr 列式）**：`<cb:tt>` 底下放兩個 [`<cb:ttr>`](ttr.md)，每個 `<cb:ttr>` 是一行，裡面依序放多個 `<cb:t>`。用於原書上下兩行逐字對照的情形，例如悉曇字一行、漢字音譯一行。沒有 `@place`、`@type` 的 `<cb:tt>`，以及 `type="tr"`，都採用這種寫法。
2. **並列式（t 直接放在 tt 底下）**：`<cb:tt>` 底下直接放兩個以上的 `<cb:t>`，每個 `<cb:t>` 是同一段內容的不同語言版本。`place="inline"`、`type="app"`、`type="single-line"` 採用這種寫法。

> 2026-09 以前，隔行對照也是用並列式，每一組對照（例如一個悉曇字配一個漢字）各自包成一個 `<cb:tt>`。現在改成一整段（原書上下兩行）包成一個 `<cb:tt>`，以 `<cb:ttr>` 區分行。

## 隔行對照（ttr 列式）

例 T54n2133A.xml, p. 1190a22

```xml
<lb n="1190a22" ed="T"/>...
<p xml:id="pT54p1190a2201"><cb:tt>
  <cb:ttr>
    <cb:t xml:lang="sa-Sidd" style="margin-left:0em"><g ref="#SD-B064"/><g ref="#SD-B5B1"/><g ref="#SD-E355"/></cb:t>
    <cb:t xml:lang="sa-Sidd" style="margin-left:0em"><g ref="#SD-CBF7"/><g ref="#SD-A565"/><g ref="#SD-A5D0"/><g ref="#SD-E355"/></cb:t>
    <cb:t xml:lang="sa-Sidd" style="margin-left:0em"><g ref="#SD-E0F3"/><g ref="#SD-B769"/><g ref="#SD-E355"/></cb:t>
    <cb:t xml:lang="sa-Sidd" style="margin-left:0em"><g ref="#SD-A47C"/><g ref="#SD-E04B"/><g ref="#SD-E355"/></cb:t>
    <cb:t xml:lang="sa-Sidd" style="margin-left:0em"><g ref="#SD-DA7A"/><g ref="#SD-A5F2"/><g ref="#SD-E3BA"/><g ref="#SD-CFC6"/><g ref="#SD-A557"/><g ref="#SD-A5C0"/><g ref="#SD-E355"/></cb:t>
  </cb:ttr>
<lb n="1190a23" ed="T"/><cb:ttr>
    <cb:t xml:lang="zh-Hant">天</cb:t>
    <cb:t xml:lang="zh-Hant">地</cb:t>
    <cb:t xml:lang="zh-Hant">日</cb:t>
    <cb:t xml:lang="zh-Hant">月</cb:t>
    <cb:t xml:lang="zh-Hant">陰　陽</cb:t>
  </cb:ttr>
</cb:tt>
```

### 基本規則

* 一個 `<cb:tt>` 恰好有兩個 `<cb:ttr>`，對應原書的上下兩行。
* 兩個 `<cb:ttr>` 內的 `<cb:t>` 數量相同，依**位置**一一對應：第一行的第 n 個 `<cb:t>` 對應第二行的第 n 個 `<cb:t>`。上例中 `#SD-B064…` 對應「天」。
* 同一個 `<cb:ttr>` 內的 `<cb:t>` 都是同一種語言（`xml:lang` 相同），對齊用的空 `<cb:t/>` 除外。
* 兩行的語言順序依原書而定，常見的有：
  * `sa-Sidd`（悉曇）在上、`zh-Hant` 在下，大部分屬於此類。
  * `sa-Sidd` 在上、`zh-x-yy` 在下，例如 T54n2132。
  * `zh-Hant` 在上、`sa-x-rj`（蘭札）在下，例如 T51n2101。
  * `zh-Hant` 在上、`sa-Sidd` 在下，見 [type="tr"](#typetr)。

### 換行、換頁的位置

第二行開頭的 `<lb>`（若剛好換頁，還有 `<pb>`）放在兩個 `<cb:ttr>` 之間，是 `<cb:tt>` 的子元素。

例 T18n0914.xml, p. 936c01

```xml
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-DA42"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC8"/></cb:t>
  </cb:ttr>
<pb n="0936c" ed="T" xml:id="T18.0914.0936c"/>
<lb n="0936c01" ed="T"/><cb:ttr>
    <cb:t xml:lang="zh-Hant">曩</cb:t>
    <cb:t xml:lang="zh-Hant">麼</cb:t>
    ...
```

### 對齊用的空 t

某一行在該位置沒有對應的字時，以空的 `<cb:t/>`（不帶 `xml:lang`）佔位，維持兩行 `<cb:t>` 數量相同。

例 T21n1239.xml, p. 189b16

```xml
<lb n="0189b16" ed="T"/><cb:tt>
  <cb:ttr>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5C1"/><g ref="#SD-E046"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC1"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC1"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC1"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC1"/></cb:t>
    <cb:t/>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5F1"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5C1"/><g ref="#SD-E046"/></cb:t>
    <cb:t/>
  </cb:ttr>
<lb n="0189b17" ed="T"/><cb:ttr>
    <cb:t xml:lang="zh-Hant">𠰢</cb:t>
    <cb:t xml:lang="zh-Hant">吽</cb:t>
    <cb:t xml:lang="zh-Hant">吽</cb:t>
    <cb:t xml:lang="zh-Hant">吽</cb:t>
    <cb:t xml:lang="zh-Hant">吽</cb:t>
    <cb:t xml:lang="zh-Hant">善女功德</cb:t>
    <cb:t xml:lang="zh-Hant">耶</cb:t>
    <cb:t xml:lang="zh-Hant">𠰢</cb:t>
    <cb:t xml:lang="zh-Hant">降怨</cb:t>
  </cb:ttr>
</cb:tt>
```

也有以 `<cb:t xml:lang="zh-Hant"><space quantity="0"/></cb:t>` 佔位的寫法，見 [type="tr"](#typetr) 的例子。

### ttr 中 t 以外的內容

不屬於任何一組對照的文字（例如引號、標點、說明文字）直接放在 `<cb:ttr>` 中、`<cb:t>` 之外。

例 T10n0299.xml, p. 892c01，開頭的「「」：

```xml
<lb n="0892c01" ed="T"/><p xml:id="pT10p0892c0101" cb:type="dharani"><cb:tt>
  <cb:ttr>「<cb:t xml:lang="sa-Sidd"><g ref="#SD-A5A9"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A5F0"/></cb:t>
    ...
```

例 T20n1152.xml, p. 614b14，結尾的「　二字，」：

```xml
<lb n="0614b14" ed="T"/><p xml:id="pT20p0614b1401" cb:type="dharani"><cb:tt>
  <cb:ttr>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-E074"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-E1D5"/></cb:t>
  </cb:ttr>
<lb n="0614b15" ed="T"/><cb:ttr>
    <cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>唵</cb:zi><cb:sg>引</cb:sg></cb:yin></cb:t>
    <cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>提</cb:zi><cb:sg>引</cb:sg></cb:yin></cb:t>　二字，</cb:ttr>
</cb:tt></p>
```

`<cb:ttr>` 中也可能直接出現 `<note>`、`<app>`，例如 T20n1176.xml。

## @place="inline"

行中悉漢對照，維持並列式：每組對照一個 `<cb:tt>`，底下直接放 `<cb:t>`。例 T19n0939.xml, p. 89c23

```xml
<lb n="0089c23" ed="T"/>次，從心想出<cb:tt place="inline"><cb:t xml:lang="sa-Sidd"><g ref="#SD-E17C"/></cb:t><cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>吽</cb:zi><cb:sg>引</cb:sg></cb:yin></cb:t></cb:tt><cb:tt place="inline"><cb:t xml:lang="sa-Sidd"><g ref="#SD-E1BD"/></cb:t><cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>怛囕</cb:zi><cb:sg>二合</cb:sg></cb:yin></cb:t></cb:tt><cb:tt place="inline"><cb:t xml:lang="sa-Sidd"><g ref="#SD-E050"/></cb:t><cb:t xml:lang="zh-Hant"><cb:yin><cb:zi>紇陵</cb:zi><cb:sg>二合</cb:sg></cb:yin></cb:t></cb:tt><cb:tt place="inline"><cb:t xml:lang="sa-Sidd"><g ref="#SD-CFD4"/></cb:t><cb:t xml:lang="zh-Hant">
<lb n="0089c24" ed="T"/>惡</cb:t></cb:tt>真言，...
```

## @type

### type="app"

校勘欄提供的巴利文、梵文等對照，維持並列式。常與 `@n`（對應的校勘編號）一起出現，有時另帶 `@word-count`（對照的漢字字數）。例 T01n0026.xml, p. 635a07

```xml
<cb:tt n="0635002" type="app">
  <cb:t resp="CBETA" xml:lang="zh-Hant">揵沓
<lb n="0635a08" ed="T"/>惒</cb:t>
  <cb:t resp="Taisho" xml:lang="pi" place="foot">Gandhabha.</cb:t>
</cb:tt>
```

上例中 t 元素的 place 屬性值為 foot 表示文字出現在校勘欄中。

### type="single-line"

每個 `<cb:t>` 各自是一整行，不逐字對照，維持並列式。例 X59n1078.xml, p. 245b13

```xml
<lb ed="X" n="0245b13"/><lb ed="R104" n="0779b04"/><p xml:id="pX59p0245b1301" cb:type="dharani"><cb:tt type="single-line">
  <cb:t xml:lang="zh-Hant">唵麼抳鉢訥銘<note place="inline">二合</note>吽<note place="inline">心想梵字光明，又想自身完滿潔白徧有光明，心作思維曰：一
<lb ed="X" n="0245b14"/><lb ed="R104" n="0779b05"/>切眾生身中悉得清淨不染煩惱</note></cb:t>
<lb ed="X" n="0245b15"/><lb ed="R104" n="0779b06"/>
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-DA42"/><g ref="#SD-A5E5"/><g ref="#SD-A54D"/><g ref="#SD-A5B5"/><g ref="#SD-E243"/><note xml:lang="zh-Hant" place="inline">二合</note><g ref="#SD-E2F6"/></cb:t>
</cb:tt></p>
```

### type="tr"

這也是隔行對照，採用 ttr 列式，目前只見於 T20n1168B。漢字在上、悉曇在下。例 T20n1168B.xml, p. 676c18

```xml
<lb n="0676c18" ed="T"/><cb:tt type="tr">
  <cb:ttr>
    <cb:t xml:lang="zh-Hant">伽</cb:t>
    <cb:t xml:lang="zh-Hant">梵</cb:t>
    <cb:t xml:lang="zh-Hant">在</cb:t>
    <cb:t xml:lang="zh-Hant">布</cb:t>
    <cb:t xml:lang="zh-Hant">得</cb:t>
    <cb:t xml:lang="zh-Hant">攞</cb:t>
    <cb:t xml:lang="zh-Hant">迦</cb:t>
    <cb:t xml:lang="zh-Hant">山</cb:t>
    <cb:t xml:lang="zh-Hant"><space quantity="0"/></cb:t>
    <cb:t xml:lang="zh-Hant">住</cb:t>
    <cb:t xml:lang="zh-Hant"><space quantity="0"/></cb:t>
    <cb:t xml:lang="zh-Hant">觀</cb:t>
    <cb:t xml:lang="zh-Hant">自</cb:t>
    <cb:t xml:lang="zh-Hant">在</cb:t>
  </cb:ttr>
<lb n="0676c19" ed="T"/><cb:ttr>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A458"/></cb:t>
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-E2B7"/></cb:t>
    ...
    <cb:t xml:lang="sa-Sidd"><g ref="#SD-A656"/></cb:t>
  </cb:ttr>
</cb:tt>
```
