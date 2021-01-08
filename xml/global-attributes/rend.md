# rend attributes

## inline

T54n2132, p. 1186b04

```xml
<cb:tt rend="inline">
  <cb:t xml:lang="sa-Sidd"><g ref="#SD-CFC5">􆿅</g></cb:t>
  <cb:t xml:lang="zh-x-yy"><cb:yin><cb:zi>阿</cb:zi><cb:sg>上聲短呼</cb:sg></cb:yin></cb:t>
</cb:tt>
```

## no_nor: 不使用通用字

例如 T54n1896.xml, p. 863a05

```xml
二明稽首者古文為<term rend="no_nor"><g ref="#CB05129"/></term>
```

## pl-1 .. pl-8

例如 ZW01na003.xml, p. 27a20

```xml
<cell rend="pl-2">附：文軌及其著作</cell>
```

pl-2 對應的 CSS 是 padding-left:2em, 依此類推。
目前 (2021-01-08) 只有出現 pl-2 和 pl-4 這二種，CBReader 支援 pl-1 至 pl-8 八種。
