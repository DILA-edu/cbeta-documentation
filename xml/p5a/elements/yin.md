# `yin`

這是 CBETA 自訂標記，TEI 無此元素。

## 整組 `yin` 元素表示「發音」

例： `T54n2135_p1241a25`

```xml
<cb:yin>
  <cb:zi>婆羅</cb:zi>
  <cb:sg>二合</cb:sg>
</cb:yin>
```

## `sg` 表示 `zi` 的發音

這種用法類似 `<cb:fan>`, 例 `T54n2132_p1188c06`： 

```xml
<cb:yin>
  <cb:zi>曜</cb:zi>
  <cb:sg type="fangie">庾告反</cb:sg>
</cb:yin>
```

## `yin` 包含兩個 `sg`

例： `T18n0868_p0278a20`

```xml
<cb:yin>
  <cb:zi>底</cb:zi>
  <cb:sg type="fangie">丁以反</cb:sg>
  <cb:sg>引</cb:sg>
</cb:yin>
```
