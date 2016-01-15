# ref

參考 [TEI ref 元素](http://www.tei-c.org/release/doc/tei-p5-doc/zh-TW/html/ref-ref.html)

## 參照本文件中的其他位置

例如 T49n2035.xml, p. 250d05

```xml
<ref target="#list4">天台智者禪師○</ref>
...(中略)...
<list xml:id="list4"><head>四祖天台智者大禪師</head>
```

## 參照其他文件

例如 T42n1828.xml，p. 311a06，《瑜伽論記》參照《瑜伽師地論》：

```xml
<ref target="../T30/T30n1579.xml#xpath2(//0279a03)">論本卷第一</ref>
```